---
description: 了解详细信息：循环跟踪
title: 循环跟踪
ms.date: 03/30/2017
ms.assetid: 5ff139f9-8806-47bc-8f33-47fe6c436b92
ms.openlocfilehash: 4b50420c7eb0c6ca9bc6b3354c78e7922b00f16c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778745"
---
# <a name="circular-tracing"></a><span data-ttu-id="57a53-103">循环跟踪</span><span class="sxs-lookup"><span data-stu-id="57a53-103">Circular Tracing</span></span>

<span data-ttu-id="57a53-104">此示例演示如何实现循环缓冲区跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="57a53-104">This sample demonstrates the implementation of a circular buffer trace listener.</span></span> <span data-ttu-id="57a53-105">生产服务的一个常见方案是，拥有可以长时间使用的服务，并在较低级别启用跟踪日志记录。</span><span class="sxs-lookup"><span data-stu-id="57a53-105">A common scenario for production services is to have services that are available for long periods of time and to have trace logging enabled at a low level.</span></span> <span data-ttu-id="57a53-106">这些服务占用大量磁盘空间。</span><span class="sxs-lookup"><span data-stu-id="57a53-106">These services consume a lot of disk space.</span></span> <span data-ttu-id="57a53-107">在对某个服务进行疑难解答时，跟踪日志中的最新数据与解决问题相关。</span><span class="sxs-lookup"><span data-stu-id="57a53-107">When troubleshooting a service, the most recent data in the trace log is relevant to solving a problem.</span></span> <span data-ttu-id="57a53-108">此示例演示如何实现一个循环缓冲区跟踪侦听器，在该侦听器中，磁盘上仅保留最新的跟踪数据，最多可以保存可配置的数据量。</span><span class="sxs-lookup"><span data-stu-id="57a53-108">This sample demonstrates an implementation of a circular buffer trace listener in which only the most recent traces are kept on disk up to a configurable amount of data.</span></span> <span data-ttu-id="57a53-109">此示例基于 [入门](getting-started-sample.md) ，并包含自定义跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="57a53-109">This sample is based on the [Getting Started](getting-started-sample.md) and includes a custom tracing listener.</span></span>

> [!NOTE]
> <span data-ttu-id="57a53-110">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="57a53-110">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="57a53-111">本示例假定您熟悉 [跟踪和消息日志记录](tracing-and-message-logging.md) 示例，并阅读为 [跟踪和消息日志记录](tracing-and-message-logging.md) 示例提供的文档。</span><span class="sxs-lookup"><span data-stu-id="57a53-111">This sample assumes that you are familiar with the [Tracing and Message Logging](tracing-and-message-logging.md) sample and have read the documentation provided for the [Tracing and Message Logging](tracing-and-message-logging.md) sample.</span></span>

## <a name="circular-buffer-trace-listener"></a><span data-ttu-id="57a53-112">循环缓冲区跟踪侦听器</span><span class="sxs-lookup"><span data-stu-id="57a53-112">Circular Buffer Trace Listener</span></span>

<span data-ttu-id="57a53-113">实现循环缓冲区跟踪侦听器所涉及的概念是：拥有两个文件，每个文件最多可以存储所需跟踪日志总数据量的一半。</span><span class="sxs-lookup"><span data-stu-id="57a53-113">The concept behind the implementation of the Circular Buffer Trace Listener is to have two files that can each store up to half of the total desired trace log data.</span></span> <span data-ttu-id="57a53-114">侦听器创建一个文件并写入该文件，直到它达到其限制（即数据大小的一半），之后侦听器将切换到第二个文件。</span><span class="sxs-lookup"><span data-stu-id="57a53-114">The listener creates one file and writes to that file until it reaches the limit of half of the data size, at which point it switches to a second file.</span></span> <span data-ttu-id="57a53-115">当侦听器达到第二个文件的限制时，它会用新跟踪数据覆盖第一个文件。</span><span class="sxs-lookup"><span data-stu-id="57a53-115">When the listener reaches the limit for the second file - it overwrites the first file with new traces.</span></span>

<span data-ttu-id="57a53-116">此侦听器派生自 `XmlWriteTraceListener` ，并允许通过 [服务跟踪查看器工具 ( # A0) ](../service-trace-viewer-tool-svctraceviewer-exe.md)来查看日志。</span><span class="sxs-lookup"><span data-stu-id="57a53-116">This listener derives from the `XmlWriteTraceListener` and allows the logs to be viewed with the [Service Trace Viewer Tool (SvcTraceViewer.exe)](../service-trace-viewer-tool-svctraceviewer-exe.md).</span></span> <span data-ttu-id="57a53-117">在尝试查看日志时，可以通过在服务跟踪查看器工具中同时打开这两个日志文件来方便地进行重新合并。</span><span class="sxs-lookup"><span data-stu-id="57a53-117">When attempting to view the logs, the two log files can be easily recombined by opening both of the log files at the same time in the Service Trace Viewer tool.</span></span> <span data-ttu-id="57a53-118">服务跟踪查看器工具会自动负责对跟踪数据进行排序，以便它们按照正确的顺序显示。</span><span class="sxs-lookup"><span data-stu-id="57a53-118">The Service Trace Viewer tool automatically takes care of sorting the traces so that they appear in the correct order.</span></span>

## <a name="configuration"></a><span data-ttu-id="57a53-119">Configuration</span><span class="sxs-lookup"><span data-stu-id="57a53-119">Configuration</span></span>

<span data-ttu-id="57a53-120">通过为侦听器和源元素添加下面的代码可以将服务配置为使用循环缓冲区跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="57a53-120">A service can be configured to use the Circular Buffer Trace Listener by adding the following code for a listener and source elements.</span></span> <span data-ttu-id="57a53-121">最大文件大小是通过在循环跟踪侦听器的配置中设置 `maxFileSizeKB` 属性来指定的。</span><span class="sxs-lookup"><span data-stu-id="57a53-121">The max file size is specified by setting the `maxFileSizeKB` attribute in the circular trace listener's configuration.</span></span> <span data-ttu-id="57a53-122">下面的代码对此进行了演示。</span><span class="sxs-lookup"><span data-stu-id="57a53-122">This is demonstrated in the following code.</span></span>

```xml
<system.diagnostics>
  <sources>
    <source name="System.ServiceModel" switchValue="Information,ActivityTracing" propagateActivity="true">
      <listeners>
        <add name="CircularTraceListener" />
      </listeners>
    </source>
  </sources>
  <sharedListeners>
    <add name="CircularTraceListener" type="Microsoft. Samples.ServiceModel.CircularTraceListener,CircularTraceListener"
         initializeData="c:\logs\CircularTracing-service.svclog" maxFileSizeKB="100" />
  </sharedListeners>
  <trace autoflush="true" />
</system.diagnostics>
```

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="57a53-123">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="57a53-123">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="57a53-124">请确保已 [为 Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="57a53-124">Be sure you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="57a53-125">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="57a53-125">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="57a53-126">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="57a53-126">To run the sample in a single- or cross-computer configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57a53-127">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="57a53-127">The samples may already be installed on your computer.</span></span> <span data-ttu-id="57a53-128">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="57a53-128">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="57a53-129">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57a53-129">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="57a53-130">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="57a53-130">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\CircularTracing`

## <a name="see-also"></a><span data-ttu-id="57a53-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="57a53-131">See also</span></span>

- <span data-ttu-id="57a53-132">[AppFabric 监视示例](/previous-versions/appfabric/ff383407(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="57a53-132">[AppFabric Monitoring Samples](/previous-versions/appfabric/ff383407(v=azure.10))</span></span>

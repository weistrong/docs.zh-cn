---
description: 了解详细信息：服务调试行为
title: 服务调试行为
ms.date: 03/30/2017
ms.assetid: 9d8fd3fb-dc39-427a-8235-336a7e7162ba
ms.openlocfilehash: 3aae4a4cca53fce50bff8ec02896e748f430166f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793098"
---
# <a name="service-debug-behavior"></a><span data-ttu-id="27ccc-103">服务调试行为</span><span class="sxs-lookup"><span data-stu-id="27ccc-103">Service Debug Behavior</span></span>

<span data-ttu-id="27ccc-104">本示例演示如何配置服务调试行为设置。</span><span class="sxs-lookup"><span data-stu-id="27ccc-104">This sample demonstrates how service debug behavior settings can be configured.</span></span> <span data-ttu-id="27ccc-105">该示例基于实现服务协定的 [入门](getting-started-sample.md) `ICalculator` 。</span><span class="sxs-lookup"><span data-stu-id="27ccc-105">The sample is based on the [Getting Started](getting-started-sample.md), which implements the `ICalculator` service contract.</span></span> <span data-ttu-id="27ccc-106">本示例在配置文件中显式定义服务调试行为。</span><span class="sxs-lookup"><span data-stu-id="27ccc-106">This sample explicitly defines service debug behavior in the configuration file.</span></span> <span data-ttu-id="27ccc-107">也可以在代码中强制完成此操作。</span><span class="sxs-lookup"><span data-stu-id="27ccc-107">It can also be done imperatively in code.</span></span>

<span data-ttu-id="27ccc-108">在此示例中，客户端是一个控制台应用程序 (.exe)，服务是由 Internet 信息服务 (IIS) 承载的。</span><span class="sxs-lookup"><span data-stu-id="27ccc-108">In this sample, the client is a console application (.exe) and the service is hosted by Internet Information Services (IIS).</span></span>

> [!NOTE]
> <span data-ttu-id="27ccc-109">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="27ccc-109">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="27ccc-110">服务器的 Web.config 文件定义服务调试行为以启用帮助页和异常处理，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="27ccc-110">The Web.config file for the server defines the service debug behavior to enable the help page and exception handling as shown in the following sample.</span></span>

```xml
<behaviors>
     <serviceBehaviors>
         <behavior name="CalculatorServiceBehavior">
         <!-- WARNING: Setting includeExceptionDetailInFaults = "True" could result in leaking secured server information to the client.-->
         <!-- Please set this to false when deploying -->
             <serviceDebug includeExceptionDetailInFaults="True" httpHelpPageEnabled="True"/>
         </behavior>
     </serviceBehaviors>
</behaviors>
```

<span data-ttu-id="27ccc-111">[\<serviceDebug>](../../configure-apps/file-schema/wcf/servicedebug.md) 是允许更改服务调试行为属性的配置元素。</span><span class="sxs-lookup"><span data-stu-id="27ccc-111">[\<serviceDebug>](../../configure-apps/file-schema/wcf/servicedebug.md) is the configuration element that allows changing the service debug behavior properties.</span></span> <span data-ttu-id="27ccc-112">用户可以修改此行为以实现以下目标：</span><span class="sxs-lookup"><span data-stu-id="27ccc-112">The user can modify this behavior to achieve the following:</span></span>

- <span data-ttu-id="27ccc-113">这使服务可以返回应用程序代码引发的任何异常，即使未使用 <xref:System.ServiceModel.FaultContractAttribute> 声明该异常。</span><span class="sxs-lookup"><span data-stu-id="27ccc-113">This allows the service to return any exception that is thrown by the application code even if the exception is not declared using the <xref:System.ServiceModel.FaultContractAttribute>.</span></span> <span data-ttu-id="27ccc-114">为此，需要将 `includeExceptionDetailInFaults` 设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="27ccc-114">It is done by setting `includeExceptionDetailInFaults` to `true`.</span></span> <span data-ttu-id="27ccc-115">此设置在调试服务器引发意外异常的事例时很有用。</span><span class="sxs-lookup"><span data-stu-id="27ccc-115">This setting is useful when debugging cases where the server is throwing an unexpected exception.</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="27ccc-116">在生产环境中打开此设置会不安全。</span><span class="sxs-lookup"><span data-stu-id="27ccc-116">It is not secure to turn this setting on in a production environment.</span></span> <span data-ttu-id="27ccc-117">由于意外服务器异常可能具有某些不适用于客户端的信息，因此将 `includeExceptionDetailsInFaults` 设置为 `true` 可能导致信息泄露。</span><span class="sxs-lookup"><span data-stu-id="27ccc-117">An unexpected server exception may have some information that is not intended for the client and so setting `includeExceptionDetailsInFaults` to `true` might result in an information leak.</span></span>

- <span data-ttu-id="27ccc-118">[\<serviceDebug>](../../configure-apps/file-schema/wcf/servicedebug.md)还允许用户启用或禁用帮助页。</span><span class="sxs-lookup"><span data-stu-id="27ccc-118">The [\<serviceDebug>](../../configure-apps/file-schema/wcf/servicedebug.md) also allows a user to enable or disable the help page.</span></span> <span data-ttu-id="27ccc-119">每个服务可以选择公开一个帮助页，该帮助页包含有关服务的信息，其中包括要获取服务的 WSDL 的终结点。</span><span class="sxs-lookup"><span data-stu-id="27ccc-119">Each service can optionally expose a help page that contains information about the service including the endpoint to get WSDL for the service.</span></span> <span data-ttu-id="27ccc-120">通过将 `httpHelpPageEnabled` 设置为 `true` 可以启用该帮助页。</span><span class="sxs-lookup"><span data-stu-id="27ccc-120">This can be enabled by setting `httpHelpPageEnabled` to `true`.</span></span> <span data-ttu-id="27ccc-121">这将使帮助页返回到对服务基址的 GET 请求。</span><span class="sxs-lookup"><span data-stu-id="27ccc-121">This enables the help page to be returned to a GET request to the base address of the service.</span></span> <span data-ttu-id="27ccc-122">通过设置另一个属性 `httpHelpPageUrl`，可以更改此地址。</span><span class="sxs-lookup"><span data-stu-id="27ccc-122">You can change this address by setting another attribute `httpHelpPageUrl`.</span></span> <span data-ttu-id="27ccc-123">通过使用 HTTPS（而不是 HTTP）可以使其安全。</span><span class="sxs-lookup"><span data-stu-id="27ccc-123">You can make this secure by using HTTPS instead of HTTP.</span></span> <span data-ttu-id="27ccc-124">这可以通过设置 `httpsHelpPageEnabled` 和 `httpsHelpPageUrl` 来完成。</span><span class="sxs-lookup"><span data-stu-id="27ccc-124">This can be done by setting `httpsHelpPageEnabled` and `httpsHelpPageUrl`.</span></span>

<span data-ttu-id="27ccc-125">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="27ccc-125">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="27ccc-126">前三个操作（加、减和乘）都会成功。</span><span class="sxs-lookup"><span data-stu-id="27ccc-126">The first three operations (Add, Subtract and Multiply) must succeed.</span></span> <span data-ttu-id="27ccc-127">最后一个操作（“除”）由于除数为零异常而失败。</span><span class="sxs-lookup"><span data-stu-id="27ccc-127">The last operation ("divide") fails with a division by zero exception.</span></span>

### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="27ccc-128">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="27ccc-128">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="27ccc-129">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="27ccc-129">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="27ccc-130">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="27ccc-130">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="27ccc-131">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="27ccc-131">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27ccc-132">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="27ccc-132">The samples may already be installed on your machine.</span></span> <span data-ttu-id="27ccc-133">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="27ccc-133">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="27ccc-134">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27ccc-134">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="27ccc-135">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="27ccc-135">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Behaviors\ServiceDebug`

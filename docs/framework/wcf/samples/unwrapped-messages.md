---
description: 了解详细信息：未包装的消息
title: 未包装的消息
ms.date: 03/30/2017
ms.assetid: 019657bd-1f9b-4315-ad74-eaa4e7551ff6
ms.openlocfilehash: 5eeb81e9035856f6c13eed3ce54b4fb98de07e5c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798207"
---
# <a name="unwrapped-messages"></a><span data-ttu-id="69a2b-103">未包装的消息</span><span class="sxs-lookup"><span data-stu-id="69a2b-103">Unwrapped Messages</span></span>

<span data-ttu-id="69a2b-104">此示例演示未包装的消息。</span><span class="sxs-lookup"><span data-stu-id="69a2b-104">This sample demonstrates unwrapped messages.</span></span> <span data-ttu-id="69a2b-105">默认情况下，消息正文的格式设置为对服务操作的参数进行包装。</span><span class="sxs-lookup"><span data-stu-id="69a2b-105">By default, the message body is formatted such that the parameters to a service operation are wrapped.</span></span> <span data-ttu-id="69a2b-106">下面的示例演示一个包装模式下的对 `Add` 服务的 `ICalculator` 请求消息。</span><span class="sxs-lookup"><span data-stu-id="69a2b-106">The following sample shows an `Add` request message to the `ICalculator` service in wrapped mode.</span></span>  
  
```xml  
<s:Envelope
    xmlns:s="http://www.w3.org/2003/05/soap-envelope"  
    xmlns:a="http://schemas.xmlsoap.org/ws/2005/08/addressing">  
    <s:Header>  
        …  
    </s:Header>  
    <s:Body>  
      <Add xmlns="http://Microsoft.ServiceModel.Samples">  
        <n1>100</n1>  
        <n2>15.99</n2>  
      </Add>  
    </s:Body>  
</s:Envelope>  
```  
  
 <span data-ttu-id="69a2b-107">消息正文中的 `<Add>` 元素包装 `n1` 和 `n2` 参数。</span><span class="sxs-lookup"><span data-stu-id="69a2b-107">The `<Add>` element in the message body wraps the `n1` and `n2` parameters.</span></span> <span data-ttu-id="69a2b-108">相反，下面的示例则显示未包装模式下的等效消息。</span><span class="sxs-lookup"><span data-stu-id="69a2b-108">In contrast, the following sample shows the equivalent message in the unwrapped mode.</span></span>  
  
```xml  
<s:Envelope
    xmlns:s="http://www.w3.org/2003/05/soap-envelope"
    xmlns:a="http://schemas.xmlsoap.org/ws/2005/08/addressing">  
    <s:Header>  
        ….  
    </s:Header>  
    <s:Body>  
      <n1 xmlns="http://Microsoft.ServiceModel.Samples">100</n1>  
      <n2 xmlns="http://Microsoft.ServiceModel.Samples">15.99</n2>  
    </s:Body>  
  </s:Envelope>  
```  
  
 <span data-ttu-id="69a2b-109">未包装的消息不会包装包含元素中的 `n1` 和 `n2` 参数，这些参数是 SOAP 正文元素的直接子级。</span><span class="sxs-lookup"><span data-stu-id="69a2b-109">The unwrapped message does not wrap the `n1` and `n2` parameters in a containing element, they are direct children of the soap body element.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="69a2b-110">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="69a2b-110">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="69a2b-111">在此示例中，通过向服务操作参数类型和返回值类型应用 <xref:System.ServiceModel.MessageContractAttribute> 来创建未包装的消息，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="69a2b-111">In this sample, an unwrapped message is created by applying the <xref:System.ServiceModel.MessageContractAttribute> to the service operation parameter type and return value type as shown in the following sample code.</span></span>  
  
```csharp
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public interface ICalculator  
{  
    [OperationContract]  
    ResponseMessage Add(RequestMessage request);  
    [OperationContract]  
    ResponseMessage Subtract(RequestMessage request);  
    [OperationContract]  
    ResponseMessage Multiply(RequestMessage request);  
    [OperationContract]  
    ResponseMessage Divide(RequestMessage request);  
}  
  
//setting IsWrapped to false means the n1 and n2  
//members will be direct children of the soap body element  
[MessageContract(IsWrapped = false)]  
public class RequestMessage  
{  
    [MessageBodyMember]  
    private double n1;  
    [MessageBodyMember]  
    private double n2;  
    //…  
}  
  
//setting IsWrapped to false means the result  
//member will be a direct child of the soap body element  
[MessageContract(IsWrapped = false)]  
public class ResponseMessage  
{  
    [MessageBodyMember]  
    private double result;  
    //…  
}  
```  
  
 <span data-ttu-id="69a2b-112">为了让您看到正在发送和接收的消息，此示例使用了跟踪。</span><span class="sxs-lookup"><span data-stu-id="69a2b-112">To allow you to see the messages being sent and received, this sample uses tracing.</span></span> <span data-ttu-id="69a2b-113">此外，配置 <xref:System.ServiceModel.WSHttpBinding> 时没有使用安全性，以减少它记录的消息数。</span><span class="sxs-lookup"><span data-stu-id="69a2b-113">In addition, the <xref:System.ServiceModel.WSHttpBinding> has been configured without security, to reduce the number of messages it logs.</span></span>  
  
 <span data-ttu-id="69a2b-114">可以使用 [服务跟踪查看器工具 ( # A0) ](../service-trace-viewer-tool-svctraceviewer-exe.md)来查看生成的跟踪日志 (c:\logs\Message.log) 。</span><span class="sxs-lookup"><span data-stu-id="69a2b-114">The resulting trace log (c:\logs\Message.log) can be viewed by using the [Service Trace Viewer Tool (SvcTraceViewer.exe)](../service-trace-viewer-tool-svctraceviewer-exe.md).</span></span> <span data-ttu-id="69a2b-115">若要查看消息内容，请在服务跟踪查看器工具的左侧窗格和右侧窗格中选择 " **消息** "。</span><span class="sxs-lookup"><span data-stu-id="69a2b-115">To view message contents, select **Messages** in both the left and the right panes of the Service Trace Viewer tool.</span></span> <span data-ttu-id="69a2b-116">此示例中的跟踪日志配置为生成到 C:\LOGS 文件夹。</span><span class="sxs-lookup"><span data-stu-id="69a2b-116">Trace logs in this sample are configured to be generated into the C:\LOGS folder.</span></span> <span data-ttu-id="69a2b-117">请在运行此示例之前创建该文件夹，并为用户赋予对该目录的“网络服务”写权限。</span><span class="sxs-lookup"><span data-stu-id="69a2b-117">Create this folder before running the sample and give the user Network Service write permissions for this directory.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="69a2b-118">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="69a2b-118">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="69a2b-119">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="69a2b-119">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="69a2b-120">创建一个 C:\LOGS 目录，用于记录消息。</span><span class="sxs-lookup"><span data-stu-id="69a2b-120">Create a C:\LOGS directory for logging messages.</span></span> <span data-ttu-id="69a2b-121">向用户授予对该目录的“网络服务”写权限。</span><span class="sxs-lookup"><span data-stu-id="69a2b-121">Give the user Network Service write permissions for this directory.</span></span>  
  
3. <span data-ttu-id="69a2b-122">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="69a2b-122">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
4. <span data-ttu-id="69a2b-123">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="69a2b-123">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="69a2b-124">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="69a2b-124">The samples may already be installed on your machine.</span></span> <span data-ttu-id="69a2b-125">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="69a2b-125">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="69a2b-126">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="69a2b-126">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="69a2b-127">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="69a2b-127">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Contract\Message\Unwrapped`  

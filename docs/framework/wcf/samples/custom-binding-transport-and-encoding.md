---
description: 了解详细信息：自定义绑定传输和编码
title: 自定义绑定传输和编码
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 6c0b353d-79ee-4e61-b348-be49ad0e9a16
ms.openlocfilehash: d579414d77836abecc685b758e81d0775c3ca142
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99732678"
---
# <a name="custom-binding-transport-and-encoding"></a><span data-ttu-id="345bc-103">自定义绑定传输和编码</span><span class="sxs-lookup"><span data-stu-id="345bc-103">Custom Binding Transport and Encoding</span></span>

<span data-ttu-id="345bc-104">自定义绑定由离散绑定元素的有序列表定义。</span><span class="sxs-lookup"><span data-stu-id="345bc-104">A custom binding is defined by an ordered list of discrete binding elements.</span></span> <span data-ttu-id="345bc-105">本示例演示如何使用各种传输和消息编码元素配置自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="345bc-105">This sample demonstrates how to configure a custom binding with various transport and message encoding elements.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="345bc-106">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="345bc-106">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="345bc-107">此示例基于 [自宿主](self-host.md)，已修改为配置三个终结点，以支持具有自定义绑定的 HTTP、TCP 和 NamedPipe 传输。</span><span class="sxs-lookup"><span data-stu-id="345bc-107">This sample is based on the [Self-Host](self-host.md), and has been modified to configure three endpoints to support HTTP, TCP, and NamedPipe transports with custom bindings.</span></span> <span data-ttu-id="345bc-108">并对客户端配置进行了类似修改，将客户端代码更改为能与这三个终结点中的每一个进行通信。</span><span class="sxs-lookup"><span data-stu-id="345bc-108">The client configuration was similarly modified, and the client code changed to communicate with each of the three endpoints.</span></span>  
  
 <span data-ttu-id="345bc-109">本示例演示如何配置支持特定传输和消息编码的自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="345bc-109">The sample demonstrates a how to configure a custom binding that supports a particular transport and message encoding.</span></span> <span data-ttu-id="345bc-110">这是通过为 `binding` 元素配置传输和消息编码而实现的。</span><span class="sxs-lookup"><span data-stu-id="345bc-110">This is accomplished by configuring a transport and a message encoding for the `binding` element.</span></span> <span data-ttu-id="345bc-111">在定义自定义绑定时，绑定元素的排序非常重要，因为每个元素都表示通道堆栈中的一个层 (请参阅 [自定义绑定](../extending/custom-bindings.md)) 。</span><span class="sxs-lookup"><span data-stu-id="345bc-111">The ordering of binding elements is important in defining a custom binding, because each represents a layer in the channel stack (see [Custom Bindings](../extending/custom-bindings.md)).</span></span> <span data-ttu-id="345bc-112">本示例配置三个自定义绑定：使用文本编码的 HTTP 传输、使用文本编码的 TCP 传输和使用二进制编码的 NamedPipe 传输。</span><span class="sxs-lookup"><span data-stu-id="345bc-112">This sample configures three custom bindings: an HTTP transport with text encoding, a TCP transport with text encoding, and a NamedPipe transport with a binary encoding.</span></span>  
  
 <span data-ttu-id="345bc-113">服务配置按如下所示定义自定义绑定：</span><span class="sxs-lookup"><span data-stu-id="345bc-113">The service configuration defines the custom bindings as follows:</span></span>  
  
```xml  
<bindings>  
    <customBinding>  
        <binding name="HttpBinding" >  
            <textMessageEncoding
                messageVersion="Soap12Addressing10"/>  
            <httpTransport />  
        </binding>  
        <binding name="TcpBinding" >  
            <textMessageEncoding />  
            <tcpTransport />  
        </binding>  
        <binding name="NamedPipeBinding" >  
            <binaryMessageEncoding />  
            <namedPipeTransport />  
        </binding>  
    </customBinding>  
</bindings>  
```  
  
 <span data-ttu-id="345bc-114">运行示例时，操作请求和响应将显示在服务和客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="345bc-114">When you run the sample, the operation requests and responses are displayed in both the service and client console window.</span></span> <span data-ttu-id="345bc-115">客户端将逐一与三个终结点进行通信，首先访问 HTTP，接着是 TCP，最后为 NamedPipe。</span><span class="sxs-lookup"><span data-stu-id="345bc-115">The client communicates with each of the three endpoints, accessing first HTTP, then TCP, and finally NamedPipe.</span></span> <span data-ttu-id="345bc-116">在每个控制台窗口中按 Enter 可以关闭服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="345bc-116">Press ENTER in each console window to shut down the service and client.</span></span>  
  
 <span data-ttu-id="345bc-117">`namedPipeTransport` 绑定不支持计算机到计算机的操作。</span><span class="sxs-lookup"><span data-stu-id="345bc-117">The `namedPipeTransport` binding does not support machine-to-machine operations.</span></span> <span data-ttu-id="345bc-118">它仅用于同一计算机上的通信。</span><span class="sxs-lookup"><span data-stu-id="345bc-118">It is used only for communication on the same machine.</span></span> <span data-ttu-id="345bc-119">因此，当在跨计算机的方案中运行示例时，应注释掉客户端代码文件中的以下行：</span><span class="sxs-lookup"><span data-stu-id="345bc-119">Therefore, when running the sample in a cross-machine scenario, comment out the following lines in the client code file:</span></span>  
  
```csharp  
CalculatorClient client = new CalculatorClient("default");  
Console.WriteLine("Communicate with named pipe endpoint.");  
// Call operations.  
DoCalculations(client);  
//Closing the client gracefully closes the connection and cleans up resources  
client.Close();  
```  
  
```vb  
Dim client As New CalculatorClient("default")  
Console.WriteLine("Communicate with named pipe endpoint.")  
' call operations  
DoCalculations(client)  
'Closing the client gracefully closes the connection and cleans up resources  
client.Close()  
```  
  
> [!NOTE]
> <span data-ttu-id="345bc-120">如果使用 Svcutil.exe 为此示例重新生成配置，请确保在客户端配置中修改终结点名称以与客户端代码匹配。</span><span class="sxs-lookup"><span data-stu-id="345bc-120">If you use Svcutil.exe to regenerate the configuration for this sample, be sure to modify the endpoint name in the client configuration to match the client code.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="345bc-121">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="345bc-121">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="345bc-122">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="345bc-122">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="345bc-123">若要生成 c #、c + + 或 Visual Basic .NET 版本的解决方案，请按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="345bc-123">To build the C#, C++, or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="345bc-124">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="345bc-124">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="345bc-125">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="345bc-125">The samples may already be installed on your machine.</span></span> <span data-ttu-id="345bc-126">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="345bc-126">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="345bc-127">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="345bc-127">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="345bc-128">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="345bc-128">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Custom\Transport`  

---
description: 了解有关以下内容的详细信息： WS 双重 Http
title: WS 双向 Http
ms.date: 03/30/2017
ms.assetid: 9997eba5-29ec-48db-86f3-fa77b241fb1a
ms.openlocfilehash: 44245691a47982f427c82cf8ad81ac2dd8f0b557
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99714997"
---
# <a name="ws-dual-http"></a><span data-ttu-id="4296f-103">WS 双向 Http</span><span class="sxs-lookup"><span data-stu-id="4296f-103">WS Dual Http</span></span>

<span data-ttu-id="4296f-104">双向 Http 示例演示如何配置 `WSDualHttpBinding` 绑定。</span><span class="sxs-lookup"><span data-stu-id="4296f-104">The Dual Http sample demonstrates how to configure the `WSDualHttpBinding` binding.</span></span> <span data-ttu-id="4296f-105">此示例由客户端控制台程序 (.exe) 和 Internet 信息服务 (IIS) 所承载的服务库 (.dll) 组成。</span><span class="sxs-lookup"><span data-stu-id="4296f-105">This sample consists of a client console program (.exe) and a service library (.dll) hosted by Internet Information Services (IIS).</span></span> <span data-ttu-id="4296f-106">该服务实现双工协定。</span><span class="sxs-lookup"><span data-stu-id="4296f-106">The service implements a duplex contract.</span></span> <span data-ttu-id="4296f-107">该协定由 `ICalculatorDuplex` 接口定义，该接口公开数学运算（加、减、乘和除）。</span><span class="sxs-lookup"><span data-stu-id="4296f-107">The contract is defined by the `ICalculatorDuplex` interface, which exposes math operations (Add, Subtract, Multiply, and Divide).</span></span> <span data-ttu-id="4296f-108">在本示例中，`ICalculatorDuplex` 接口允许客户端执行数学运算，通过会话计算运行结果。</span><span class="sxs-lookup"><span data-stu-id="4296f-108">In this sample, the `ICalculatorDuplex` interface allows the client to perform math operations, calculating a running result over the session.</span></span> <span data-ttu-id="4296f-109">服务在 `ICalculatorDuplexCallback` 接口上单独返回结果。</span><span class="sxs-lookup"><span data-stu-id="4296f-109">Independently, the service returns results on the `ICalculatorDuplexCallback` interface.</span></span> <span data-ttu-id="4296f-110">双工协定需要会话，因为必须建立上下文才能将客户端和服务之间发送的一组消息关联在一起。</span><span class="sxs-lookup"><span data-stu-id="4296f-110">A duplex contract requires a session, because a context must be established to correlate the set of messages being sent between client and service.</span></span> <span data-ttu-id="4296f-111">`WSDualHttpBinding` 绑定支持双工通信。</span><span class="sxs-lookup"><span data-stu-id="4296f-111">The `WSDualHttpBinding` binding supports duplex communication.</span></span>

> [!NOTE]
> <span data-ttu-id="4296f-112">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="4296f-112">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4296f-113">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="4296f-113">The samples may already be installed on your machine.</span></span> <span data-ttu-id="4296f-114">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="4296f-114">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="4296f-115">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4296f-115">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="4296f-116">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="4296f-116">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\WS\DualHttp`

<span data-ttu-id="4296f-117">若要使用 `WSDualHttpBinding` 配置服务终结点，请在所示的终结点配置中指定绑定。</span><span class="sxs-lookup"><span data-stu-id="4296f-117">To configure a service endpoint with the `WSDualHttpBinding`, specify the binding in the endpoint configuration as shown.</span></span>

```xml
<endpoint address=""
         binding="wsDualHttpBinding"
         contract="Microsoft.ServiceModel.Samples.ICalculatorDuplex" />
```

<span data-ttu-id="4296f-118">在客户端上，必须配置一个服务器可用来连接客户端的地址，如下面的示例配置所示。</span><span class="sxs-lookup"><span data-stu-id="4296f-118">On the client, you must configure an address that the server can use to connect to the client as shown in the following sample configuration.</span></span>

```xml
<system.serviceModel>
  <client>
    <endpoint address=
         "http://localhost/servicemodelsamples/service.svc"
         binding="wsDualHttpBinding"
         bindingConfiguration="Binding1"
         contract="Microsoft.ServiceModel.Samples.ICalculatorDuplex" />
  </client>

  <bindings>
    <!-- Configure a WSDualHttpBinding that supports duplex -->
    <!-- communication. -->
    <wsDualHttpBinding>
      <binding name="Binding1"
               clientBaseAddress="http://localhost:8000/myClient/"
               useDefaultWebProxy="true"
               bypassProxyOnLocal="false">
      </binding>
    </wsDualHttpBinding>
  </bindings>
</system.serviceModel>
```

<span data-ttu-id="4296f-119">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="4296f-119">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="4296f-120">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="4296f-120">Press ENTER in the client window to shut down the client.</span></span>

```console
Press <ENTER> to terminate client once the output is displayed.

Result(100)
Result(50)
Result(882.5)
Result(441.25)
Equation(0 + 100 - 50 * 17.65 / 2 = 441.25)
```

<span data-ttu-id="4296f-121">当运行示例时，在回调接口上可以看到从服务发送的、返回到客户端的消息。</span><span class="sxs-lookup"><span data-stu-id="4296f-121">When you run the sample, you see the messages returned to the client on the callback interface sent from the service.</span></span> <span data-ttu-id="4296f-122">显示每个中间结果，最后在所有操作完成时显示整个公式。</span><span class="sxs-lookup"><span data-stu-id="4296f-122">Each intermediate result is displayed, followed by the entire equation upon completion of all operations.</span></span> <span data-ttu-id="4296f-123">按 Enter 可关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="4296f-123">Press ENTER to shut down the client.</span></span>

### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="4296f-124">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="4296f-124">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="4296f-125">使用以下命令安装 ASP.NET 4.0。</span><span class="sxs-lookup"><span data-stu-id="4296f-125">Install ASP.NET 4.0 using the following command.</span></span>

    ```console
    %windir%\Microsoft.NET\Framework\v4.0.XXXXX\aspnet_regiis.exe /i /enable
    ```

2. <span data-ttu-id="4296f-126">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="4296f-126">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

3. <span data-ttu-id="4296f-127">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="4296f-127">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

4. <span data-ttu-id="4296f-128">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="4296f-128">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4296f-129">在跨计算机配置中运行客户端时，请确保将 `address` [ \<endpoint> 的 \<client> ](../../configure-apps/file-schema/wcf/endpoint-of-client.md)和元素的元素的属性中的 localhost 替换为 `clientBaseAddress` [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) [\<wsDualHttpBinding>](../../configure-apps/file-schema/wcf/wsdualhttpbinding.md) 相应计算机的名称，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4296f-129">When running the client in a cross-machine configuration, be sure to replace localhost in both the `address` attribute of the [\<endpoint> of \<client>](../../configure-apps/file-schema/wcf/endpoint-of-client.md) element and the `clientBaseAddress` attribute of the [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element of the [\<wsDualHttpBinding>](../../configure-apps/file-schema/wcf/wsdualhttpbinding.md) element with the name of the appropriate machine, as shown:</span></span>

    ```xml
    <client>
        <endpoint name = ""
          address=
         "http://service_machine_name/servicemodelsamples/service.svc"
        />
    </client>
    ...
    <wsDualHttpBinding>
        <binding name="DuplexBinding" clientBaseAddress=
            "http://client_machine_name:8000/myClient/">
        </binding>
    </wsDualHttpBinding>
    ```

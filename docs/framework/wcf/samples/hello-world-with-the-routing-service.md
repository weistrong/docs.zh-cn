---
description: 了解详细信息：与路由服务 Hello World
title: 通过路由服务进行通信
ms.date: 03/30/2017
ms.assetid: 0f4b0d5b-6522-4ad5-9f3a-baa78316d7d1
ms.openlocfilehash: 1741c7d1f1e474864d66220fd160633997744876
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631965"
---
# <a name="hello-world-with-the-routing-service"></a><span data-ttu-id="ff23c-103">通过路由服务进行通信</span><span class="sxs-lookup"><span data-stu-id="ff23c-103">Hello World with the Routing Service</span></span>

<span data-ttu-id="ff23c-104">此示例演示了 Windows Communication Foundation (WCF) 路由服务。</span><span class="sxs-lookup"><span data-stu-id="ff23c-104">This sample demonstrates the Windows Communication Foundation (WCF) Routing Service.</span></span> <span data-ttu-id="ff23c-105">路由服务是一个 WCF 组件，使您可以轻松地在应用程序中包含基于内容的路由器。</span><span class="sxs-lookup"><span data-stu-id="ff23c-105">The Routing Service is a WCF component that makes it easy to include a content-based router in your application.</span></span> <span data-ttu-id="ff23c-106">此示例改编了标准 WCF 计算器示例，以使用路由服务进行通信。</span><span class="sxs-lookup"><span data-stu-id="ff23c-106">This sample adapts the standard WCF Calculator Sample to communicate using the Routing Service.</span></span> <span data-ttu-id="ff23c-107">在此示例中，计算器客户端配置为将消息发送到由路由器公开的一个终结点。</span><span class="sxs-lookup"><span data-stu-id="ff23c-107">In this sample, the Calculator client is configured to send messages to an endpoint exposed by the router.</span></span> <span data-ttu-id="ff23c-108">路由服务配置为接受发送给它的所有消息，然后将这些消息转发至与计算器服务对应的终结点。</span><span class="sxs-lookup"><span data-stu-id="ff23c-108">The Routing Service is configured to accept all messages sent to it and to forward them to an endpoint that corresponds to the Calculator service.</span></span> <span data-ttu-id="ff23c-109">因此，从客户端发送的消息将由路由器接收，并重新路由到实际的计算器服务。</span><span class="sxs-lookup"><span data-stu-id="ff23c-109">Thus messages sent from the client are received by the router and re-routed to the actual Calculator service.</span></span> <span data-ttu-id="ff23c-110">来自计算器服务的消息将发回到路由器，后者又将这些消息传回到计算器客户端。</span><span class="sxs-lookup"><span data-stu-id="ff23c-110">Messages from the Calculator service are sent back to the router, which in turn passes them back to the Calculator client.</span></span>

### <a name="to-use-this-sample"></a><span data-ttu-id="ff23c-111">使用此示例</span><span class="sxs-lookup"><span data-stu-id="ff23c-111">To use this sample</span></span>

1. <span data-ttu-id="ff23c-112">使用 Visual Studio 2012，打开 HelloRoutingService。</span><span class="sxs-lookup"><span data-stu-id="ff23c-112">Using Visual Studio 2012, open HelloRoutingService.sln.</span></span>

2. <span data-ttu-id="ff23c-113">按 F5 或 Ctrl+Shift+B。</span><span class="sxs-lookup"><span data-stu-id="ff23c-113">Press F5 or CTRL+SHIFT+B.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff23c-114">如果按 F5，则计算器客户端将自动启动。</span><span class="sxs-lookup"><span data-stu-id="ff23c-114">If you press F5, the Calculator Client automatically starts.</span></span> <span data-ttu-id="ff23c-115">如果按 Ctrl+Shift+B（生成），则您必须自己启动以下应用程序。</span><span class="sxs-lookup"><span data-stu-id="ff23c-115">If you press CTRL+SHIFT+B (build), you must start following applications yourself.</span></span>
    >
    > 1. <span data-ttu-id="ff23c-116">计算器客户端 (./CalculatorClient/bin/client.exe)</span><span class="sxs-lookup"><span data-stu-id="ff23c-116">Calculator client (./CalculatorClient/bin/client.exe</span></span>
    > 2. <span data-ttu-id="ff23c-117">计算器服务 (./CalculatorService/bin/service.exe)</span><span class="sxs-lookup"><span data-stu-id="ff23c-117">Calculator service (./CalculatorService/bin/service.exe)</span></span>
    > 3. <span data-ttu-id="ff23c-118">路由服务 (./RoutingService/bin/RoutingService.exe)</span><span class="sxs-lookup"><span data-stu-id="ff23c-118">Routing service (./RoutingService/bin/RoutingService.exe)</span></span>

3. <span data-ttu-id="ff23c-119">按 Enter 启动客户端。</span><span class="sxs-lookup"><span data-stu-id="ff23c-119">Press ENTER to start the client.</span></span>

     <span data-ttu-id="ff23c-120">应会看到以下输出：</span><span class="sxs-lookup"><span data-stu-id="ff23c-120">You should see the following output:</span></span>

    ```console
     Add(100,15.99) = 115.99

     Subtract(145,76.54) = 68.46

     Multiply(9,81.25) = 731.25

     Divide(22,7) = 3.14285714285714
    ```

## <a name="configurable-via-code-or-appconfig"></a><span data-ttu-id="ff23c-121">可通过代码或 App.Config 进行配置</span><span class="sxs-lookup"><span data-stu-id="ff23c-121">Configurable via Code or App.Config</span></span>

 <span data-ttu-id="ff23c-122">所提供的示例配置为使用 App.config 文件来定义路由器行为。</span><span class="sxs-lookup"><span data-stu-id="ff23c-122">The sample ships configured to use an App.config file to define the router’s behavior.</span></span> <span data-ttu-id="ff23c-123">也可将 App.config 文件的名称更改为无法识别的其他名称，并将对 ConfigureRouterViaCode() 的方法调用取消注释。</span><span class="sxs-lookup"><span data-stu-id="ff23c-123">You can also change the name of the App.config file to something else so that it is not recognized and uncomment the method call to ConfigureRouterViaCode().</span></span> <span data-ttu-id="ff23c-124">以上任一方法都可产生相同的路由器行为。</span><span class="sxs-lookup"><span data-stu-id="ff23c-124">Either method results in the same behavior from the router.</span></span>

### <a name="scenario"></a><span data-ttu-id="ff23c-125">方案</span><span class="sxs-lookup"><span data-stu-id="ff23c-125">Scenario</span></span>

 <span data-ttu-id="ff23c-126">此示例演示作为基本消息泵的路由器。</span><span class="sxs-lookup"><span data-stu-id="ff23c-126">This sample demonstrates the router acting as a basic message pump.</span></span> <span data-ttu-id="ff23c-127">路由服务用作透明的代理节点，该节点配置为将消息直接传递到目标终结点的预配置集。</span><span class="sxs-lookup"><span data-stu-id="ff23c-127">The routing service acts as a transparent proxy node configured to pass messages directly to a preconfigured set of destination endpoints.</span></span>

### <a name="real-world-scenario"></a><span data-ttu-id="ff23c-128">实际方案</span><span class="sxs-lookup"><span data-stu-id="ff23c-128">Real World Scenario</span></span>

 <span data-ttu-id="ff23c-129">Contoso 希望提高其服务的命名、寻址、配置和安全方面的灵活性。</span><span class="sxs-lookup"><span data-stu-id="ff23c-129">Contoso wants to increase the flexibility it has in the naming, addressing, configuration, and security of its services.</span></span> <span data-ttu-id="ff23c-130">为此，他们将基本消息泵放在其服务的前面，作为面向公共的终结点。</span><span class="sxs-lookup"><span data-stu-id="ff23c-130">To do this, they place a basic message pump in front of their services to act as a public facing endpoint.</span></span> <span data-ttu-id="ff23c-131">这样，他们就可以将附加安全性放在其实际服务的前面，以便以后更轻松地实现扩展的解决方案或服务版本控制。</span><span class="sxs-lookup"><span data-stu-id="ff23c-131">This allows them to place additional security in front of their actual services and make it easier to implement scaled out solutions or service versioning at a later date.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff23c-132">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="ff23c-132">The samples may already be installed on your computer.</span></span> <span data-ttu-id="ff23c-133">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="ff23c-133">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="ff23c-134">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ff23c-134">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ff23c-135">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="ff23c-135">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\RoutingServices\HelloRoutingService`  
  
## <a name="see-also"></a><span data-ttu-id="ff23c-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="ff23c-136">See also</span></span>

- <span data-ttu-id="ff23c-137">[AppFabric 承载和持久性示例](/previous-versions/appfabric/ff383418(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="ff23c-137">[AppFabric Hosting and Persistence Samples](/previous-versions/appfabric/ff383418(v=azure.10))</span></span>

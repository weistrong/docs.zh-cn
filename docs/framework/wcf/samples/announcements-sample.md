---
description: 了解详细信息：公告示例
title: 公告示例
ms.date: 03/30/2017
ms.assetid: 954a75e4-9a97-41d6-94fc-43765d4205a9
ms.openlocfilehash: 076efed31f862f6de68e924446528d682a62824a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778940"
---
# <a name="announcements-sample"></a><span data-ttu-id="75681-103">公告示例</span><span class="sxs-lookup"><span data-stu-id="75681-103">Announcements Sample</span></span>

<span data-ttu-id="75681-104">此示例显示如何使用发现功能的公告功能。</span><span class="sxs-lookup"><span data-stu-id="75681-104">This sample shows how to use the Announcement functionality of the Discovery feature.</span></span> <span data-ttu-id="75681-105">服务使用公告可以发出包含有关服务的元数据的公告消息。</span><span class="sxs-lookup"><span data-stu-id="75681-105">Announcements allow services to send out announcement messages that contain metadata about the service.</span></span> <span data-ttu-id="75681-106">默认情况下，服务启动时会发送 Hello 公告，服务关闭时会发送 Bye 公告。</span><span class="sxs-lookup"><span data-stu-id="75681-106">By default a hello announcement is sent when the service starts up and a bye announcement is sent when the service shuts down.</span></span> <span data-ttu-id="75681-107">这些公告可以进行多播，也可点到点发送。</span><span class="sxs-lookup"><span data-stu-id="75681-107">These announcements can be multicast or they can be sent point-to-point.</span></span> <span data-ttu-id="75681-108">此示例由两个项目组成，即服务项目和客户端项目。</span><span class="sxs-lookup"><span data-stu-id="75681-108">This sample consists of two projects service and client.</span></span>

## <a name="service"></a><span data-ttu-id="75681-109">服务</span><span class="sxs-lookup"><span data-stu-id="75681-109">Service</span></span>

<span data-ttu-id="75681-110">此项目包含一个自承载计算器服务。</span><span class="sxs-lookup"><span data-stu-id="75681-110">This project contains a self-hosted calculator service.</span></span> <span data-ttu-id="75681-111">在 `Main` 方法中，会创建一个服务主机，并向该主机添加服务终结点。</span><span class="sxs-lookup"><span data-stu-id="75681-111">In the `Main` method, a service host is created and a service endpoint is added to it.</span></span> <span data-ttu-id="75681-112">接下来创建 <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior>。</span><span class="sxs-lookup"><span data-stu-id="75681-112">Next, a <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior> is created.</span></span> <span data-ttu-id="75681-113">若要启用公告，必须向 <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior> 添加公告终结点。</span><span class="sxs-lookup"><span data-stu-id="75681-113">To enable announcements, an announcement endpoint must be added to the <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior>.</span></span> <span data-ttu-id="75681-114">在此例中，添加一个标准终结点（使用 UDP 多播）作为公告终结点。</span><span class="sxs-lookup"><span data-stu-id="75681-114">In this case a standard endpoint, using UDP multicast is added as the announcement endpoint.</span></span> <span data-ttu-id="75681-115">这会向已知的 UDP 地址广播公告。</span><span class="sxs-lookup"><span data-stu-id="75681-115">This broadcasts the announcements over a well-known UDP address.</span></span>

```csharp
Uri baseAddress = new Uri("http://localhost:8000/" + Guid.NewGuid().ToString());

// Create a ServiceHost for the CalculatorService type.
using (ServiceHost serviceHost = new ServiceHost(typeof(CalculatorService), baseAddress))
{
     serviceHost.AddServiceEndpoint(typeof(ICalculatorService), new WSHttpBinding(), String.Empty);

     ServiceDiscoveryBehavior serviceDiscoveryBehavior = new ServiceDiscoveryBehavior();

     // Announce the availability of the service over UDP multicast
    serviceDiscoveryBehavior.AnnouncementEndpoints.Add(new UdpAnnouncementEndpoint());

    // Make the service discoverable over UDP multicast.
    serviceHost.Description.Behaviors.Add(serviceDiscoveryBehavior);
    serviceHost.AddServiceEndpoint(new UdpDiscoveryEndpoint());
    serviceHost.Open();
    // ...
}
```

## <a name="client"></a><span data-ttu-id="75681-116">客户端</span><span class="sxs-lookup"><span data-stu-id="75681-116">Client</span></span>

<span data-ttu-id="75681-117">在此项目中请注意，客户端承载 <xref:System.ServiceModel.Discovery.AnnouncementService>。</span><span class="sxs-lookup"><span data-stu-id="75681-117">In this project, note that the client hosts an <xref:System.ServiceModel.Discovery.AnnouncementService>.</span></span> <span data-ttu-id="75681-118">此外，会向事件注册两个委托。</span><span class="sxs-lookup"><span data-stu-id="75681-118">Furthermore, two delegates are registered with events.</span></span> <span data-ttu-id="75681-119">这些事件指示客户端在接收到联机和脱机公告时执行的操作。</span><span class="sxs-lookup"><span data-stu-id="75681-119">These events dictate what the client does when online and offline announcements are received.</span></span>

```csharp
// Create an AnnouncementService instance
AnnouncementService announcementService = new AnnouncementService();

// Subscribe the announcement events
announcementService.OnlineAnnouncementReceived += OnOnlineEvent;
announcementService.OfflineAnnouncementReceived += OnOfflineEvent;
```

<span data-ttu-id="75681-120">`OnOnlineEvent` 和 `OnOfflineEvent` 方法分别处理 Hello 和 Bye 公告消息。</span><span class="sxs-lookup"><span data-stu-id="75681-120">The `OnOnlineEvent` and `OnOfflineEvent` methods handle the hello and bye announcement messages respectively.</span></span>

```csharp
static void OnOnlineEvent(object sender, AnnouncementEventArgs e)
{
    Console.WriteLine();
    Console.WriteLine("Received an online announcement from {0}:", e.AnnouncementMessage.EndpointDiscoveryMetadata.Address);
PrintEndpointDiscoveryMetadata(e.AnnouncementMessage.EndpointDiscoveryMetadata);
}

static void OnOfflineEvent(object sender, AnnouncementEventArgs e)
{
    Console.WriteLine();
    Console.WriteLine("Received an offline announcement from {0}:", e.AnnouncementMessage.EndpointDiscoveryMetadata.Address);
            PrintEndpointDiscoveryMetadata(e.AnnouncementMessage.EndpointDiscoveryMetadata);
}
```

#### <a name="to-use-this-sample"></a><span data-ttu-id="75681-121">使用此示例</span><span class="sxs-lookup"><span data-stu-id="75681-121">To use this sample</span></span>

1. <span data-ttu-id="75681-122">此示例使用 HTTP 终结点，若要运行此示例，必须添加正确的 URL ACL。</span><span class="sxs-lookup"><span data-stu-id="75681-122">This sample uses HTTP endpoints and to run this sample, proper URL ACLs must be added.</span></span> <span data-ttu-id="75681-123">有关详细信息，请参阅 [配置 HTTP 和 HTTPS](../feature-details/configuring-http-and-https.md)。</span><span class="sxs-lookup"><span data-stu-id="75681-123">For more information, see [Configuring HTTP and HTTPS](../feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="75681-124">使用提升的特权执行下面的命令应添加相应的 ACL。</span><span class="sxs-lookup"><span data-stu-id="75681-124">Executing the following command at an elevated privilege should add the appropriate ACLs.</span></span> <span data-ttu-id="75681-125">如果该命令无效，则可能需要使用你的域和用户名替换以下自变量。</span><span class="sxs-lookup"><span data-stu-id="75681-125">You may want to substitute your Domain and Username for the following arguments if the command does not work as is.</span></span> `netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%`

2. <span data-ttu-id="75681-126">生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="75681-126">Build the solution.</span></span>

3. <span data-ttu-id="75681-127">运行 client.exe 应用程序。</span><span class="sxs-lookup"><span data-stu-id="75681-127">Run the client.exe application.</span></span>

4. <span data-ttu-id="75681-128">运行 service.exe 应用程序。</span><span class="sxs-lookup"><span data-stu-id="75681-128">Run the service.exe application.</span></span> <span data-ttu-id="75681-129">请注意，客户端会接收联机公告。</span><span class="sxs-lookup"><span data-stu-id="75681-129">Note the client receives an online announcement.</span></span>

5. <span data-ttu-id="75681-130">关闭 service.exe 应用程序。</span><span class="sxs-lookup"><span data-stu-id="75681-130">Close the service.exe application.</span></span> <span data-ttu-id="75681-131">请注意，客户端会接收脱机公告。</span><span class="sxs-lookup"><span data-stu-id="75681-131">Note the client receives an offline announcement.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75681-132">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="75681-132">The samples may already be installed on your machine.</span></span> <span data-ttu-id="75681-133">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="75681-133">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="75681-134">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75681-134">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="75681-135">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="75681-135">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\Announcements`

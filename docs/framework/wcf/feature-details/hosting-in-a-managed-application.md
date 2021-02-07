---
description: 了解更多：托管应用程序中的托管
title: 在托管应用程序中承载
ms.date: 03/30/2017
ms.assetid: af70132d-e9e1-4f32-b20f-f0014629758a
ms.openlocfilehash: 14fd6b2dea1a4315567611f505f2898314a07908
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756196"
---
# <a name="hosting-in-a-managed-application"></a><span data-ttu-id="8b2e5-103">在托管应用程序中承载</span><span class="sxs-lookup"><span data-stu-id="8b2e5-103">Hosting in a Managed Application</span></span>

<span data-ttu-id="8b2e5-104">Windows Communication Foundation 可以在任何 .NET Framework 应用程序中承载 WCF) 服务 (。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-104">Windows Communication Foundation (WCF) services can be hosted in any .NET Framework application.</span></span> <span data-ttu-id="8b2e5-105">自承载服务是最灵活的宿主选项，因为此服务部署所需要的基础结构最少。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-105">Self-hosting services is the most flexible hosting option because it requires the least infrastructure to deploy.</span></span> <span data-ttu-id="8b2e5-106">不过，它也是最不可靠的宿主选项，因为托管应用程序未提供 WCF 中其他宿主选项（如 Internet Information Services (IIS) 和 Windows 服务）的高级宿主和管理功能。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-106">However, it is also the least robust hosting option, because managed applications do not provide the advanced hosting and management features of other hosting options in WCF, such as Internet Information Services (IIS) and Windows services.</span></span>  
  
 <span data-ttu-id="8b2e5-107">若要创建自承载服务，请创建并打开 <xref:System.ServiceModel.ServiceHost>的实例以启动侦听消息的服务。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-107">To create a self-hosted service, create and open an instance of the <xref:System.ServiceModel.ServiceHost>, which starts a service listening for messages.</span></span> <span data-ttu-id="8b2e5-108">有关详细信息，请参阅 [如何：在托管应用程序中托管 WCF 服务](../how-to-host-a-wcf-service-in-a-managed-application.md)。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-108">For more information, see [How to: Host a WCF Service in a Managed Application](../how-to-host-a-wcf-service-in-a-managed-application.md).</span></span>  
  
 <span data-ttu-id="8b2e5-109">有关如何定义协定、实现协定以及在托管应用程序内承载服务的完整示例，请参阅 [入门教程](../getting-started-tutorial.md) 和 [自承载](../samples/self-host.md)服务。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-109">For a complete example on how to define a contract, implement the contract, and host a service inside of a managed application see the [Getting Started Tutorial](../getting-started-tutorial.md) and the [Self-Host](../samples/self-host.md).</span></span>  
  
 <span data-ttu-id="8b2e5-110">以下各部分描述了使用此宿主选项的常见情况。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-110">The following sections describe common scenarios that use this hosting option.</span></span>  
  
## <a name="console-applications"></a><span data-ttu-id="8b2e5-111">控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="8b2e5-111">Console Applications</span></span>  

 <span data-ttu-id="8b2e5-112">自承载支持的常见方案是在控制台应用程序内部运行的 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-112">Common scenarios that self-hosting enables are WCF services running inside console applications.</span></span> <span data-ttu-id="8b2e5-113">在控制台应用程序内承载 WCF 服务通常在服务的开发阶段非常有用。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-113">Hosting a WCF service inside a console application is typically useful during the development phase of the service.</span></span> <span data-ttu-id="8b2e5-114">这使服务变得容易调试，从中跟踪信息以查明应用程序内发生的情况变得更加方便，以及通过将其复制到新的位置进行来回移动变得更加轻松。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-114">This makes them easy to debug, easy to get trace information from to find out what is happening inside of the application, and easy to move around by copying them to new locations.</span></span>  
  
## <a name="rich-client-applications"></a><span data-ttu-id="8b2e5-115">胖客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="8b2e5-115">Rich Client Applications</span></span>  

 <span data-ttu-id="8b2e5-116">自承载支持的其他常见方案是丰富的客户端应用程序，例如基于 Windows Presentation Foundation (WPF) 或 Windows 窗体 (WinForms) 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-116">Other common scenarios that self-hosting enables are rich client applications, such as those based on Windows Presentation Foundation (WPF) or Windows Forms (WinForms).</span></span> <span data-ttu-id="8b2e5-117">此宿主选项还使丰富的客户端应用程序（如 WPF 和 WinForms 应用程序）可以方便地与外界通信。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-117">This hosting option also makes it easy for rich client applications, such as WPF and WinForms applications, to communicate with the outside world.</span></span> <span data-ttu-id="8b2e5-118">例如，对等协作客户端使用 WPF 作为其用户界面并托管 WCF 服务，该服务允许其他客户端连接到它并共享信息。</span><span class="sxs-lookup"><span data-stu-id="8b2e5-118">For example, a peer-to-peer collaboration client that uses WPF for its user interface and also hosts a WCF service that allows other clients to connect to it and share information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b2e5-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8b2e5-119">See also</span></span>

- [<span data-ttu-id="8b2e5-120">承载服务</span><span class="sxs-lookup"><span data-stu-id="8b2e5-120">Hosting Services</span></span>](../hosting-services.md)
- [<span data-ttu-id="8b2e5-121">入门教程</span><span class="sxs-lookup"><span data-stu-id="8b2e5-121">Getting Started Tutorial</span></span>](../getting-started-tutorial.md)

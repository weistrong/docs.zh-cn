---
description: 了解更多：通道扩展性
title: 通道扩展性
ms.date: 03/30/2017
ms.assetid: 4cc3b20b-778a-4ae8-b58c-a3822fb13065
ms.openlocfilehash: 08c93ffa2e7c4645e4c49be619c0cb065ecdbff7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704064"
---
# <a name="channels-extensibility"></a><span data-ttu-id="d26be-103">通道扩展性</span><span class="sxs-lookup"><span data-stu-id="d26be-103">Channels Extensibility</span></span>

<span data-ttu-id="d26be-104">本节包含演示自定义通道的示例。</span><span class="sxs-lookup"><span data-stu-id="d26be-104">This section contains samples that demonstrate custom channels.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d26be-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="d26be-105">In This Section</span></span>  

 [<span data-ttu-id="d26be-106">本地通道</span><span class="sxs-lookup"><span data-stu-id="d26be-106">Local Channel</span></span>](local-channel.md)  
 <span data-ttu-id="d26be-107">演示本地通道，它是用于在同一个应用程序域内进行通信的 WCF 传输通道。</span><span class="sxs-lookup"><span data-stu-id="d26be-107">Demonstrates the local channel, a WCF transport channel that is used for communication within the same application domain.</span></span>  
  
 [<span data-ttu-id="d26be-108">可靠安全配置文件</span><span class="sxs-lookup"><span data-stu-id="d26be-108">Reliable Secure Profile</span></span>](reliable-secure-profile.md)  
 <span data-ttu-id="d26be-109">演示如何将 WCF 和可靠安全配置文件 (RSP) 组合在一起。</span><span class="sxs-lookup"><span data-stu-id="d26be-109">Demonstrates how to compose WCF and Reliable Secure Profile (RSP).</span></span>  
  
 [<span data-ttu-id="d26be-110">自定义通道调度程序</span><span class="sxs-lookup"><span data-stu-id="d26be-110">Custom Channel Dispatcher</span></span>](custom-channel-dispatcher.md)  
 <span data-ttu-id="d26be-111">演示如何通过直接实现 <xref:System.ServiceModel.ServiceHostBase> 以自定义方式生成通道堆栈，以及如何在 Web 主机环境中创建自定义通道调度程序。</span><span class="sxs-lookup"><span data-stu-id="d26be-111">Demonstrates how to build the channel stack in a custom way by implementing <xref:System.ServiceModel.ServiceHostBase> directly and how to create a custom channel dispatcher in Web host environment.</span></span>  
  
 [<span data-ttu-id="d26be-112">通道分块</span><span class="sxs-lookup"><span data-stu-id="d26be-112">Chunking Channel</span></span>](chunking-channel.md)  
 <span data-ttu-id="d26be-113">演示如何限制用于缓冲使用 WCF 发送的大型消息的内存量。</span><span class="sxs-lookup"><span data-stu-id="d26be-113">Demonstrates how to limit the amount of memory used to buffer large messages sent using WCF.</span></span>
  
 [<span data-ttu-id="d26be-114">HttpCookieSession</span><span class="sxs-lookup"><span data-stu-id="d26be-114">HttpCookieSession</span></span>](httpcookiesession.md)  
 <span data-ttu-id="d26be-115">演示如何生成自定义协议通道，以便使用 HTTP Cookie 进行会话管理。</span><span class="sxs-lookup"><span data-stu-id="d26be-115">Demonstrates how to build a custom protocol channel to use HTTP cookies for session management.</span></span>  
  
 [<span data-ttu-id="d26be-116">自定义消息拦截器</span><span class="sxs-lookup"><span data-stu-id="d26be-116">Custom Message Interceptor</span></span>](custom-message-interceptor.md)  
 <span data-ttu-id="d26be-117">演示如何实现可创建通道工厂和通道侦听器的自定义绑定元素，以便在运行时堆栈的特定点截获所有传入和传出消息。</span><span class="sxs-lookup"><span data-stu-id="d26be-117">Demonstrates how to implement a custom binding element that creates channel factories and channel listeners to intercept all incoming and outgoing messages at a particular point in the run-time stack.</span></span>

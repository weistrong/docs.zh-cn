---
description: 了解详细信息：发现路由器服务
title: 发现路由器服务
ms.date: 03/30/2017
ms.assetid: 3d30af47-b24f-40e5-833a-24d77125c9e6
ms.openlocfilehash: f5fa4cd19758bef0b867fafc5af4b9cf6df27028
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726710"
---
# <a name="discovery-router-service"></a><span data-ttu-id="ed28c-103">发现路由器服务</span><span class="sxs-lookup"><span data-stu-id="ed28c-103">Discovery Router Service</span></span>

<span data-ttu-id="ed28c-104">此示例演示如何将发现消息转发到另一个终结点。</span><span class="sxs-lookup"><span data-stu-id="ed28c-104">This sample demonstrates how to forward discovery messages to another endpoint.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="ed28c-105">演示</span><span class="sxs-lookup"><span data-stu-id="ed28c-105">Demonstrates</span></span>  

 <span data-ttu-id="ed28c-106">发现路由</span><span class="sxs-lookup"><span data-stu-id="ed28c-106">Discovery Routing</span></span>  
  
## <a name="discussion"></a><span data-ttu-id="ed28c-107">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="ed28c-107">Discussion</span></span>  

 <span data-ttu-id="ed28c-108">路由发现在以下方案中非常有用：客户端正在使用代理来查找服务，该代理不知道这种服务，但知道另一个代理。</span><span class="sxs-lookup"><span data-stu-id="ed28c-108">Discovery routing is useful in a scenario in which a client is looking for a service using a proxy and the proxy is unaware of such a service, but knows of another proxy.</span></span> <span data-ttu-id="ed28c-109">此代理可以将发现数据包从此客户端转发到第二个代理。</span><span class="sxs-lookup"><span data-stu-id="ed28c-109">This proxy can forward the discovery packet from this client to the second proxy.</span></span> <span data-ttu-id="ed28c-110">第二个代理可以查找该服务，然后将响应返回到原始客户端。</span><span class="sxs-lookup"><span data-stu-id="ed28c-110">The second proxy can look for the service and return the responses to the original client.</span></span>  
  
 <span data-ttu-id="ed28c-111">在此示例中，客户端将一条消息发送到发现路由组件。</span><span class="sxs-lookup"><span data-stu-id="ed28c-111">In this sample, a client sends a message to a discovery routing component.</span></span> <span data-ttu-id="ed28c-112">此消息将发送到发现路由器上的一个特定终结点。</span><span class="sxs-lookup"><span data-stu-id="ed28c-112">This message is sent to a specific endpoint on the discovery router.</span></span> <span data-ttu-id="ed28c-113">然后，该路由器将此消息转发到一个 UDP 多播终结点。</span><span class="sxs-lookup"><span data-stu-id="ed28c-113">The router then forwards the message to a UDP multicast endpoint.</span></span> <span data-ttu-id="ed28c-114">探测消息将到达该多播终结点，侦听 UDP 多播地址的服务将对该发现路由器做出响应。</span><span class="sxs-lookup"><span data-stu-id="ed28c-114">The probe message goes out to the multicast endpoint and a service listening on a UDP multicast address responds to that discovery router.</span></span> <span data-ttu-id="ed28c-115">发现路由器收集这些响应，然后将它们发送回客户端。</span><span class="sxs-lookup"><span data-stu-id="ed28c-115">The discovery router collects the responses and sends them back to the client.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ed28c-116">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="ed28c-116">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="ed28c-117">生成示例。</span><span class="sxs-lookup"><span data-stu-id="ed28c-117">Build the sample.</span></span>  
  
2. <span data-ttu-id="ed28c-118">运行 DiscoveryRouter 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="ed28c-118">Run the DiscoveryRouter executable.</span></span>  
  
3. <span data-ttu-id="ed28c-119">从生成目录运行服务可执行文件。</span><span class="sxs-lookup"><span data-stu-id="ed28c-119">Run the service executable from the build directory.</span></span>  
  
4. <span data-ttu-id="ed28c-120">运行客户端可执行文件。</span><span class="sxs-lookup"><span data-stu-id="ed28c-120">Run the client executable.</span></span> <span data-ttu-id="ed28c-121">请注意，客户端将查找服务。</span><span class="sxs-lookup"><span data-stu-id="ed28c-121">Note that the client locates the service.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="ed28c-122">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="ed28c-122">The samples may already be installed on your machine.</span></span> <span data-ttu-id="ed28c-123">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="ed28c-123">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="ed28c-124">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed28c-124">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ed28c-125">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="ed28c-125">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\DiscoveryRouter`

---
description: 详细了解：IPv6 路由
title: IPv6 路由
ms.date: 03/30/2017
ms.assetid: c98731b4-b542-46a2-9947-1cea63c186b2
ms.openlocfilehash: 75499a7380ab0ea7c38c83a6407a0c2a269b5fce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672031"
---
# <a name="ipv6-routing"></a><span data-ttu-id="86815-103">IPv6 路由</span><span class="sxs-lookup"><span data-stu-id="86815-103">IPv6 Routing</span></span>

<span data-ttu-id="86815-104">灵活的路由机制是 IPv6 的优势之一。</span><span class="sxs-lookup"><span data-stu-id="86815-104">A flexible routing mechanism is a benefit of IPv6.</span></span> <span data-ttu-id="86815-105">由于 IPv4 网络 ID 以前和现在的分配方式，需要由 Internet 主干网上的路由器来维护大型路由表。</span><span class="sxs-lookup"><span data-stu-id="86815-105">Due to the way in which IPv4 network IDs were and are allocated, large routing tables need to be maintained by the routers that are on the Internet backbones.</span></span> <span data-ttu-id="86815-106">这些路由器必须了解所有路由，才能转发可能定向到 Internet 任何节点的数据包。</span><span class="sxs-lookup"><span data-stu-id="86815-106">These routers must know all the routes in order to forward packets that are potentially directed to any node on the Internet.</span></span> <span data-ttu-id="86815-107">借助聚合地址的功能，IPv6 可以灵活寻址，并且大大减小路由表的大小。</span><span class="sxs-lookup"><span data-stu-id="86815-107">With its ability to aggregate addresses, IPv6 allows flexible addressing and drastically reduces the size of routing tables.</span></span> <span data-ttu-id="86815-108">在这种新型寻址体系结构中，中间路由器必须仅跟踪网络中的本地部分，才能恰当地转发消息。</span><span class="sxs-lookup"><span data-stu-id="86815-108">In this new addressing architecture, intermediate routers must keep track only of the local portion of their network in order to forward the messages appropriately.</span></span>  
  
## <a name="neighbor-discovery"></a><span data-ttu-id="86815-109">邻居发现</span><span class="sxs-lookup"><span data-stu-id="86815-109">Neighbor Discovery</span></span>  

 <span data-ttu-id="86815-110">邻居发现提供的一些功能是：</span><span class="sxs-lookup"><span data-stu-id="86815-110">Some of the features provided by Neighbor Discovery are:</span></span>  
  
- <span data-ttu-id="86815-111">路由器发现。</span><span class="sxs-lookup"><span data-stu-id="86815-111">Router discovery.</span></span> <span data-ttu-id="86815-112">这允许主机识别本地路由器。</span><span class="sxs-lookup"><span data-stu-id="86815-112">This allows hosts to identify local routers.</span></span>  
  
- <span data-ttu-id="86815-113">地址解析。</span><span class="sxs-lookup"><span data-stu-id="86815-113">Address resolution.</span></span> <span data-ttu-id="86815-114">这允许节点解析相应的下一跃点地址的链接层地址（地址解析协议 [ARP] 的替换）。</span><span class="sxs-lookup"><span data-stu-id="86815-114">This allows nodes to resolve a link-layer address for a corresponding next-hop address (a replacement for Address Resolution Protocol [ARP]).</span></span>  
  
- <span data-ttu-id="86815-115">地址自动配置。</span><span class="sxs-lookup"><span data-stu-id="86815-115">Address auto-configuration.</span></span> <span data-ttu-id="86815-116">这允许主机自动配置站点本地和全局地址。</span><span class="sxs-lookup"><span data-stu-id="86815-116">This allows hosts to automatically configure site-local and global addresses.</span></span>  
  
 <span data-ttu-id="86815-117">邻居发现使用 IPv6 的 Internet 控制消息协议 (ICMPv6) 消息，包括：</span><span class="sxs-lookup"><span data-stu-id="86815-117">Neighbor Discovery uses Internet Control Message Protocol for IPv6 (ICMPv6) messages that include:</span></span>  
  
- <span data-ttu-id="86815-118">路由器播发。</span><span class="sxs-lookup"><span data-stu-id="86815-118">Router advertisement.</span></span> <span data-ttu-id="86815-119">由路由器在伪周期基础上发送或作为路由器招标的响应发送。</span><span class="sxs-lookup"><span data-stu-id="86815-119">Sent by a router on a pseudo-periodic basis or in response to a router solicitation.</span></span> <span data-ttu-id="86815-120">IPv6 路由器使用路由器播发来播发其可用性、地址前缀和其他参数。</span><span class="sxs-lookup"><span data-stu-id="86815-120">IPv6 routers use router advertisements to advertise their availability, address prefixes, and other parameters.</span></span>  
  
- <span data-ttu-id="86815-121">路由器招标。</span><span class="sxs-lookup"><span data-stu-id="86815-121">Router solicitation.</span></span> <span data-ttu-id="86815-122">由主机发送以请求链接上的路由器立即发送路由器播发。</span><span class="sxs-lookup"><span data-stu-id="86815-122">Sent by a host to request that routers on the link send a router advertisement immediately.</span></span>  
  
- <span data-ttu-id="86815-123">邻居招标。</span><span class="sxs-lookup"><span data-stu-id="86815-123">Neighbor solicitation.</span></span> <span data-ttu-id="86815-124">由节点发送，以进行地址解析、重复地址检测或验证邻居是否仍可以访问。</span><span class="sxs-lookup"><span data-stu-id="86815-124">Sent by nodes for address resolution, duplicate address detection, or to verify that a neighbor is still reachable.</span></span>  
  
- <span data-ttu-id="86815-125">邻居播发。</span><span class="sxs-lookup"><span data-stu-id="86815-125">Neighbor advertisement.</span></span> <span data-ttu-id="86815-126">由节点发送，以响应邻居招标或通知邻居链接层地址的更改。</span><span class="sxs-lookup"><span data-stu-id="86815-126">Sent by nodes to respond to a neighbor solicitation or to notify neighbors of a change in link-layer address.</span></span>  
  
- <span data-ttu-id="86815-127">重定向。</span><span class="sxs-lookup"><span data-stu-id="86815-127">Redirect.</span></span> <span data-ttu-id="86815-128">由路由器发送，以指示特定目标的下一个更好的跃点地址，用于发送节点。</span><span class="sxs-lookup"><span data-stu-id="86815-128">Sent by routers to indicate a better next-hop address to a particular destination for a sending node.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86815-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="86815-129">See also</span></span>

- [<span data-ttu-id="86815-130">Internet 协议版本 6</span><span class="sxs-lookup"><span data-stu-id="86815-130">Internet Protocol Version 6</span></span>](internet-protocol-version-6.md)
- [<span data-ttu-id="86815-131">套接字</span><span class="sxs-lookup"><span data-stu-id="86815-131">Sockets</span></span>](sockets.md)

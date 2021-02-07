---
description: 了解详细信息： WCF 和 Websocket
title: WCF 和 WebSocket
ms.date: 03/30/2017
ms.assetid: 1e53b49e-022c-49c7-8984-4b21b53c05b3
ms.openlocfilehash: 6b0d8c33000a65bf3bbf834f66119d65768b3cb6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755975"
---
# <a name="wcf-and-websockets"></a><span data-ttu-id="39361-103">WCF 和 WebSocket</span><span class="sxs-lookup"><span data-stu-id="39361-103">WCF and WebSockets</span></span>

<span data-ttu-id="39361-104">.NET Framework 4.5 引入了对 Windows Communication Foundation 中的 WebSocket 的支持。</span><span class="sxs-lookup"><span data-stu-id="39361-104">The .NET Framework 4.5 introduces support for WebSockets in Windows Communication Foundation.</span></span>  <span data-ttu-id="39361-105">WebSocket 是一种高效的、基于标准的技术，可通过标准 HTTP 端口 80 和 443 实现双向通信。</span><span class="sxs-lookup"><span data-stu-id="39361-105">WebSockets is an efficient, standards-based technology that enables bidirectional communication over the standard HTTP ports 80 and 443.</span></span> <span data-ttu-id="39361-106">使用标准 HTTP 端口，WebSocket 可通过中介跨 Web 进行通信。</span><span class="sxs-lookup"><span data-stu-id="39361-106">The use of the standard HTTP ports allow WebSockets to communicate across the web through intermediaries.</span></span>  <span data-ttu-id="39361-107">添加了两个新的标准绑定以支持通过 WebSocket 传输进行的通信。</span><span class="sxs-lookup"><span data-stu-id="39361-107">Two new standard bindings have been added to support communication over a WebSocket transport.</span></span> <span data-ttu-id="39361-108"><xref:System.ServiceModel.NetHttpBinding> 和 <xref:System.ServiceModel.NetHttpsBinding>。</span><span class="sxs-lookup"><span data-stu-id="39361-108"><xref:System.ServiceModel.NetHttpBinding> and <xref:System.ServiceModel.NetHttpsBinding>.</span></span> <span data-ttu-id="39361-109">可以通过访问属性在上配置 Websocket 特定的设置 <xref:System.ServiceModel.Channels.HttpTransportBindingElement> <xref:System.ServiceModel.Channels.HttpTransportBindingElement.WebSocketSettings%2A> 。</span><span class="sxs-lookup"><span data-stu-id="39361-109">WebSockets-specific settings can be configured on the <xref:System.ServiceModel.Channels.HttpTransportBindingElement> by accessing the <xref:System.ServiceModel.Channels.HttpTransportBindingElement.WebSocketSettings%2A> property.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="39361-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="39361-110">In This Section</span></span>  

 [<span data-ttu-id="39361-111">使用 NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="39361-111">Using the NetHttpBinding</span></span>](using-the-nethttpbinding.md)  
 <span data-ttu-id="39361-112">讨论 <xref:System.ServiceModel.NetHttpBinding> 以及如何对其进行配置。</span><span class="sxs-lookup"><span data-stu-id="39361-112">Discusses the <xref:System.ServiceModel.NetHttpBinding> and how to configure it.</span></span>  
  
 [<span data-ttu-id="39361-113">如何：创建通过 WebSocket 进行通信的 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="39361-113">How to: Create a WCF Service that Communicates over WebSockets</span></span>](how-to-create-a-wcf-service-that-communicates-over-websockets.md)  
 <span data-ttu-id="39361-114">说明如何创建通过 Websocket 进行通信的 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="39361-114">Describes how to create a WCF service that communicates over Websockets.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="39361-115">参考</span><span class="sxs-lookup"><span data-stu-id="39361-115">Reference</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="39361-116">相关章节</span><span class="sxs-lookup"><span data-stu-id="39361-116">Related Sections</span></span>

---
description: 详细了解：传输 Windows Communication Foundation
title: Windows Communication Foundation 中的传输
ms.date: 03/30/2017
helpviewer_keywords:
- transports [WCF]
- WCF, transports
- Windows Communication Foundation, transports
ms.assetid: 005c894b-af70-48aa-a1c1-c99338083c27
ms.openlocfilehash: e80a1730de107c0433949b7d476944f38e386702
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752608"
---
# <a name="transports-in-windows-communication-foundation"></a><span data-ttu-id="19591-103">Windows Communication Foundation 中的传输</span><span class="sxs-lookup"><span data-stu-id="19591-103">Transports in Windows Communication Foundation</span></span>

<span data-ttu-id="19591-104">传输层是通道堆栈的最低层。</span><span class="sxs-lookup"><span data-stu-id="19591-104">The transport layer is at the lowest level of the channel stack.</span></span> <span data-ttu-id="19591-105">Windows Communication Foundation 中使用的主要传输 (WCF) 是 HTTP、HTTPS、TCP 和命名管道。</span><span class="sxs-lookup"><span data-stu-id="19591-105">The main transports used in Windows Communication Foundation (WCF) are HTTP, HTTPS, TCP, and named pipes.</span></span> <span data-ttu-id="19591-106">本节中的主题讨论如何选择传输、配置传输和设置优化属性。</span><span class="sxs-lookup"><span data-stu-id="19591-106">The topics in this section discuss choosing among these transports, configuring the transport, and setting tuning properties.</span></span>  
  
 <span data-ttu-id="19591-107">WCF 包括其他传输。</span><span class="sxs-lookup"><span data-stu-id="19591-107">WCF includes additional transports.</span></span> <span data-ttu-id="19591-108">有关消息队列 (也称为 MSMQ) 传输的信息，请参阅 [队列和可靠会话](queues-and-reliable-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="19591-108">For information about Message Queuing (also known as MSMQ) transport, see [Queues and Reliable Sessions](queues-and-reliable-sessions.md).</span></span> <span data-ttu-id="19591-109">有关对等传输的信息，请参阅对等 [网络](peer-to-peer-networking.md)。</span><span class="sxs-lookup"><span data-stu-id="19591-109">For information about peer-to-peer transport, see [Peer-to-Peer Networking](peer-to-peer-networking.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="19591-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="19591-110">In This Section</span></span>  

 [<span data-ttu-id="19591-111">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="19591-111">Choosing a Transport</span></span>](choosing-a-transport.md)  
 <span data-ttu-id="19591-112">说明三种主要传输和选择其中一种传输时的注意事项。</span><span class="sxs-lookup"><span data-stu-id="19591-112">Describes the three main transports and considerations in selecting one.</span></span>  
  
 [<span data-ttu-id="19591-113">选择消息编码器</span><span class="sxs-lookup"><span data-stu-id="19591-113">Choosing a Message Encoder</span></span>](choosing-a-message-encoder.md)  
 <span data-ttu-id="19591-114">说明选择消息编码绑定元素时要考虑的因素。</span><span class="sxs-lookup"><span data-stu-id="19591-114">Describes factors to consider when choosing a message-encoding binding element.</span></span>  
  
 [<span data-ttu-id="19591-115">流消息传输</span><span class="sxs-lookup"><span data-stu-id="19591-115">Streaming Message Transfer</span></span>](streaming-message-transfer.md)  
 <span data-ttu-id="19591-116">说明如何配置传输层进行流式处理。</span><span class="sxs-lookup"><span data-stu-id="19591-116">Describes how to configure the transport layer to do streaming.</span></span>  
  
 [<span data-ttu-id="19591-117">配置 HTTP 和 HTTPS</span><span class="sxs-lookup"><span data-stu-id="19591-117">Configuring HTTP and HTTPS</span></span>](configuring-http-and-https.md)  
 <span data-ttu-id="19591-118">说明如何配置 HTTP 和 HTTPS 传输绑定元素。</span><span class="sxs-lookup"><span data-stu-id="19591-118">Describes how to configure the HTTP and HTTPS transport binding elements.</span></span>  
  
 [<span data-ttu-id="19591-119">如何：用受限预留替换 WCF URL 预留</span><span class="sxs-lookup"><span data-stu-id="19591-119">How to: Replace the WCF URL Reservation with a Restricted Reservation</span></span>](how-to-replace-the-wcf-url-reservation-with-a-restricted-reservation.md)  
 <span data-ttu-id="19591-120">介绍如何使用 WCFURL 受限预订。</span><span class="sxs-lookup"><span data-stu-id="19591-120">Describes how to use WCFURL restricted reservations.</span></span>  
  
 [<span data-ttu-id="19591-121">传输配额</span><span class="sxs-lookup"><span data-stu-id="19591-121">Transport Quotas</span></span>](transport-quotas.md)  
 <span data-ttu-id="19591-122">说明设置传输层中可用配额时的注意事项。</span><span class="sxs-lookup"><span data-stu-id="19591-122">Describes considerations in setting the quotas available in the transport layer.</span></span>  
  
 [<span data-ttu-id="19591-123">使用 NAT 和防火墙</span><span class="sxs-lookup"><span data-stu-id="19591-123">Working with NATs and Firewalls</span></span>](working-with-nats-and-firewalls.md)  
 <span data-ttu-id="19591-124">说明在防火墙后发送或接收消息时或存在网络地址转换 (NAT) 时如何配置传输层。</span><span class="sxs-lookup"><span data-stu-id="19591-124">Describes how to configure the transport layer when messages are sent or received behind a firewall or when network address translation (NAT) is present.</span></span>  
  
 [<span data-ttu-id="19591-125">Net.TCP 端口共享</span><span class="sxs-lookup"><span data-stu-id="19591-125">Net.TCP Port Sharing</span></span>](net-tcp-port-sharing.md)  
 <span data-ttu-id="19591-126">介绍如何使用 WCF 的 Net.tcp 端口共享组件。</span><span class="sxs-lookup"><span data-stu-id="19591-126">Describes how to use the Net.TCP Port Sharing component of WCF.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="19591-127">参考</span><span class="sxs-lookup"><span data-stu-id="19591-127">Reference</span></span>  

 <xref:System.ServiceModel.Channels.HttpTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>  
  
## <a name="related-sections"></a><span data-ttu-id="19591-128">相关章节</span><span class="sxs-lookup"><span data-stu-id="19591-128">Related Sections</span></span>  

 [<span data-ttu-id="19591-129">绑定</span><span class="sxs-lookup"><span data-stu-id="19591-129">Bindings</span></span>](bindings.md)  
  
 [<span data-ttu-id="19591-130">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="19591-130">Extending Bindings</span></span>](../extending/extending-bindings.md)

---
description: 了解详细信息：可靠会话的最佳实践
title: 可靠会话的最佳做法
ms.date: 03/30/2017
ms.assetid: b94f6e01-8070-40b6-aac7-a2cb7b4cb4f2
ms.openlocfilehash: 4b05dd914d2c5b8ec7941417b727bec1e5b43ba4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643665"
---
# <a name="best-practices-for-reliable-sessions"></a><span data-ttu-id="8fe0a-103">可靠会话的最佳做法</span><span class="sxs-lookup"><span data-stu-id="8fe0a-103">Best Practices for Reliable Sessions</span></span>

<span data-ttu-id="8fe0a-104">本主题讨论可靠会话的最佳实践。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-104">This topic discusses best practices for reliable sessions.</span></span>

## <a name="setting-maxtransferwindowsize"></a><span data-ttu-id="8fe0a-105">设置 MaxTransferWindowSize</span><span class="sxs-lookup"><span data-stu-id="8fe0a-105">Setting MaxTransferWindowSize</span></span>

<span data-ttu-id="8fe0a-106">Windows Communication Foundation 中 (WCF) 的可靠会话使用传输窗口来保存客户端和服务上的消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-106">Reliable sessions in Windows Communication Foundation (WCF) use a transfer window to hold messages on the client and service.</span></span> <span data-ttu-id="8fe0a-107">可配置属性 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxTransferWindowSize%2A> 指示传输窗口可以保存多少条消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-107">The configurable property <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxTransferWindowSize%2A> indicates how many messages the transfer window can hold.</span></span>

<span data-ttu-id="8fe0a-108">在发送方上，此值指示在等待确认时传输窗口可以保持的消息数;在接收方上，它表示要为服务缓冲多少条消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-108">On the sender, this indicates how many messages the transfer window can hold while waiting for acknowledgements; on the receiver, it indicates how many messages to buffer for the service.</span></span>

<span data-ttu-id="8fe0a-109">选择适当的大小会影响网络的效率和服务的最佳容量。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-109">Choosing the right size impacts the efficiency of the network and the optimal capacity of the service.</span></span> <span data-ttu-id="8fe0a-110">以下各节详细说明了在为此属性选择值时应考虑的事项，以及值的影响。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-110">The following sections detail what to consider when choosing a value for this property and the impact of the value.</span></span>

<span data-ttu-id="8fe0a-111">默认传输窗口大小为8条消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-111">The default transfer window size is eight messages.</span></span>

### <a name="efficient-use-of-the-network"></a><span data-ttu-id="8fe0a-112">有效地使用网络</span><span class="sxs-lookup"><span data-stu-id="8fe0a-112">Efficient use of the network</span></span>

<span data-ttu-id="8fe0a-113">在这种情况下，术语 " *网络* " 对应于作为客户端 (发送方) 和服务 (接收方) 之间的通信基础的所有内容。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-113">In this context, the term *network* corresponds to everything used as the basis of communication between a client (sender) and a service (receiver).</span></span> <span data-ttu-id="8fe0a-114">这包括传输连接以及两者之间的任何中介或桥，包括 SOAP 路由器或 HTTP 代理/防火墙。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-114">This includes the transport connections and any intermediary or bridges in between, including SOAP routers or HTTP proxies/firewalls.</span></span>

<span data-ttu-id="8fe0a-115">有效使用网络可确保充分利用网络容量。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-115">Efficient use of the network ensures that network capacity is fully used.</span></span> <span data-ttu-id="8fe0a-116">每秒通过网络传输的数据量 (*数据速率*) 和将数据从发送方传输到接收方所需的时间 (*延迟*) 会影响网络的使用效率。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-116">Both the amount of data that can be transferred per second over the network (*data rate*) and the time it takes to transfer data from the sender to the receiver (*latency*) impact how effectively the network is utilized.</span></span>

<span data-ttu-id="8fe0a-117">在发送方，属性 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxTransferWindowSize%2A> 指示在等待确认消息时，其传输窗口可以保存多少条消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-117">On the sender, the property <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxTransferWindowSize%2A> indicates how many messages its transfer window can hold while waiting for acknowledgements.</span></span> <span data-ttu-id="8fe0a-118">如果网络延迟较高，且为了确保响应式发送方和有效的网络利用率，应增加传输窗口大小。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-118">If the network latency is high and in order to ensure a responsive sender and effective network utilization, you should increase the transfer window size.</span></span>

<span data-ttu-id="8fe0a-119">例如，如果发送方和接收方之间存在多个中介，则延迟可能会很高，或者数据必须通过有损的中介或网络。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-119">For example even if the sender keeps up with data rate, latency could be high if several intermediaries exist between the sender and receiver or the data must pass through a lossy intermediary or network.</span></span> <span data-ttu-id="8fe0a-120">因此，发送程序必须等待其传输窗口中的消息确认，然后才能接受要在网络上发送的新消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-120">Thus, the sender has to wait for acknowledgements for the messages in its transfer window before accepting new messages to send on the wire.</span></span> <span data-ttu-id="8fe0a-121">具有较高延迟的缓冲区越小，网络利用率就越低。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-121">The smaller the buffer with high latency, the less effective the network utilization.</span></span> <span data-ttu-id="8fe0a-122">另一方面，如果传输窗口太高，则可能会影响服务，因为该服务可能需要与客户端发送的数据的高速率最高。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-122">On the other hand, too high a transfer window size may impact the service because the service may need to catch up to the high rate of data sent by the client.</span></span>

### <a name="running-the-service-to-capacity"></a><span data-ttu-id="8fe0a-123">将服务运行到容量</span><span class="sxs-lookup"><span data-stu-id="8fe0a-123">Running the service to capacity</span></span>

<span data-ttu-id="8fe0a-124">尽可能有效地使用网络，理想情况下，您也希望服务以最佳容量运行。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-124">As much as the network is used efficiently, ideally you also want the service to run at optimal capacity.</span></span> <span data-ttu-id="8fe0a-125">接收方上的传输窗口大小属性指示接收方可以缓冲多少条消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-125">The transfer window size property on the receiver indicates how many messages the receiver can buffer.</span></span> <span data-ttu-id="8fe0a-126">此消息缓冲不仅帮助网络流控制，而且还可让服务满负荷运行。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-126">This message buffering helps not only the network flow control but also enables the service to run to full capacity.</span></span> <span data-ttu-id="8fe0a-127">例如，如果缓冲区是一条消息，并且消息到达的速度比服务可处理的消息的速度快，则网络可能会丢弃消息，容量可能会浪费或利用率。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-127">For example if the buffer is one message and messages arrive faster than the service can process them, then the network might drop messages and capacity might be wasted or underutilized.</span></span>

<span data-ttu-id="8fe0a-128">使用缓冲区可提高服务的可用性，因为它会在处理以前收到的消息时同时接收和缓冲消息。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-128">Using a buffer increases the availability of the service as it concurrently receives and buffers a message while processing the previously received messages.</span></span>

<span data-ttu-id="8fe0a-129">建议在 `MaxTransferWindowSize` 发送方和接收方均使用相同的。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-129">We recommended that you use the same `MaxTransferWindowSize` on both the sender and receiver.</span></span>

### <a name="enabling-flow-control"></a><span data-ttu-id="8fe0a-130">启用流控制</span><span class="sxs-lookup"><span data-stu-id="8fe0a-130">Enabling flow control</span></span>

<span data-ttu-id="8fe0a-131">*流控制* 是一种机制，可确保发送方和接收方彼此保持同步，也就是说，消息在生成时就会迅速消耗下来。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-131">*Flow control* is a mechanism that ensures that the sender and receiver keep pace with each other, that is, the messages are consumed and acted upon as fast as they're produced.</span></span> <span data-ttu-id="8fe0a-132">客户端和服务上的传输窗口大小可确保发送方和接收方在一个合理的同步窗口中。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-132">The transfer window size on the client and service ensures that the sender and receiver are within a reasonable window of synchronization.</span></span>

<span data-ttu-id="8fe0a-133">强烈建议在 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.FlowControlEnabled%2A> `true` wcf 客户端和 wcf 服务之间使用可靠会话时，将属性设置为。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-133">We highly recommended that you set the property <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.FlowControlEnabled%2A> to `true` when you're using a reliable session between a WCF client and a WCF service.</span></span>

## <a name="setting-maxpendingchannels"></a><span data-ttu-id="8fe0a-134">设置 MaxPendingChannels</span><span class="sxs-lookup"><span data-stu-id="8fe0a-134">Setting MaxPendingChannels</span></span>

<span data-ttu-id="8fe0a-135">当编写允许来自不同客户端的可靠会话通信的服务时，可能会有很多客户端同时与服务建立可靠会话。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-135">When writing a service that enables reliable session communication from different clients, it's possible to have many clients establish a reliable session to the service at the same time.</span></span> <span data-ttu-id="8fe0a-136">在这些情况下，服务的响应取决于 `MaxPendingChannels` 属性。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-136">The response of the service in these situations depends on the `MaxPendingChannels` property.</span></span>

<span data-ttu-id="8fe0a-137">当发送方创建到接收方的可靠会话通道时，发送方和接收方之间的握手将建立可靠会话。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-137">When the sender creates a reliable session channel to a receiver, a handshake between them establishes a reliable session.</span></span> <span data-ttu-id="8fe0a-138">建立可靠会话之后，该通道会放入到挂起的通道队列中以供服务接受。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-138">After the reliable session is established, the channel is put in a pending channel queue for acceptance by the service.</span></span> <span data-ttu-id="8fe0a-139">此 `MaxPendingChannels` 属性指示有多少个通道可以处于此状态。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-139">The `MaxPendingChannels` property indicates how many channels can be in this state.</span></span>

<span data-ttu-id="8fe0a-140">服务可能处于无法接受更多通道的状态。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-140">It's possible for the service to be in a state where it can't accept more channels.</span></span> <span data-ttu-id="8fe0a-141">如果队列已满，则会拒绝建立可靠会话的尝试，并且客户端必须重试。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-141">If the queue is full, an attempt to establish a reliable session is rejected, and the client must retry.</span></span>

<span data-ttu-id="8fe0a-142">队列中挂起的通道也可能会在队列中保留较长的持续时间。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-142">It's also possible that the pending channels in the queue remain in the queue for a longer duration.</span></span> <span data-ttu-id="8fe0a-143">同时，可能会发生可靠会话的非活动超时，导致通道转换到出错状态。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-143">In the meantime, an inactivity timeout on the reliable session may occur, causing the channel to transition to a faulted state.</span></span>

<span data-ttu-id="8fe0a-144">当编写服务来同时服务多个客户端时，应设置一个适合你的需要的值。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-144">When writing a service that services multiple clients simultaneously, you should set a value that's suitable for your needs.</span></span> <span data-ttu-id="8fe0a-145">为属性设置过高的值会 `MaxPendingChannels` 影响工作集。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-145">Setting too high a value for the `MaxPendingChannels` property impacts your working set.</span></span>

<span data-ttu-id="8fe0a-146">的默认值 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxPendingChannels%2A> 为四个通道。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-146">The default value for <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxPendingChannels%2A> is four channels.</span></span>

## <a name="reliable-sessions-and-hosting"></a><span data-ttu-id="8fe0a-147">可靠会话和托管</span><span class="sxs-lookup"><span data-stu-id="8fe0a-147">Reliable sessions and hosting</span></span>

<span data-ttu-id="8fe0a-148">当 web 托管使用可靠会话的服务时，应注意以下重要注意事项：</span><span class="sxs-lookup"><span data-stu-id="8fe0a-148">When web hosting a service that uses reliable sessions, you should keep the following important considerations in mind:</span></span>

- <span data-ttu-id="8fe0a-149">可靠会话是有状态的，而状态在 AppDomain 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-149">Reliable sessions are stateful, and state is maintained in the AppDomain.</span></span> <span data-ttu-id="8fe0a-150">这意味着，属于可靠会话的一部分的所有消息必须在同一个 AppDomain 中进行处理。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-150">This means that all messages that are part of a reliable session must be processed in the same AppDomain.</span></span> <span data-ttu-id="8fe0a-151">Web 场和网络园，其中场或菜园的大小大于一个节点无法保证此约束。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-151">Web farms and web gardens where the size of the farm or garden is greater than one node can't guarantee this constraint.</span></span>

- <span data-ttu-id="8fe0a-152">使用双 HTTP 通道的可靠会话 (例如，使用 `WsDualHttpBinding`) 可能要求每个客户端的默认值超过两个 http 连接的默认值。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-152">Reliable sessions using dual HTTP channels (for example, using `WsDualHttpBinding`) can require more than the default of two HTTP connections per-client.</span></span> <span data-ttu-id="8fe0a-153">这意味着，双工可靠会话最多可能需要两个连接，因为并发应用程序和协议消息可能会在任意给定时间传输。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-153">This means a duplex reliable session can require up to two connections each way because concurrent application and protocol messages may be transferring each way at any given time.</span></span> <span data-ttu-id="8fe0a-154">在某些情况下，具体取决于服务的消息交换模式，这意味着可以使用双 HTTP 和可靠会话来死锁 web 托管服务。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-154">Under certain conditions depending on the message exchange pattern of the service, this means that it's possible to deadlock a web-hosted service using dual HTTP and reliable sessions.</span></span> <span data-ttu-id="8fe0a-155">若要增加每个客户端允许的 HTTP 连接数，请将以下内容添加到相关的配置文件中 (例如 *web.config* 相关服务) ：</span><span class="sxs-lookup"><span data-stu-id="8fe0a-155">To increase the number of allowable HTTP connections per client, add the following to the relevant configuration file (for example, *web.config* of the service in question):</span></span>

  ```xml
  <configuration>
    <system.net>
      <connectionManagement>
        <add name="*" maxconnection="4" />
      </connectionManagement>
    </system.net>
  </configuration>
  ```

  <span data-ttu-id="8fe0a-156">属性的值 `maxconnection` 是所需的连接数。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-156">The value of the `maxconnection` attribute is the number of connections needed.</span></span> <span data-ttu-id="8fe0a-157">在这种情况下，最小值应为四个连接。</span><span class="sxs-lookup"><span data-stu-id="8fe0a-157">The minimum in this case should be four connections.</span></span>

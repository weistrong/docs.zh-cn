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
# <a name="best-practices-for-reliable-sessions"></a>可靠会话的最佳做法

本主题讨论可靠会话的最佳实践。

## <a name="setting-maxtransferwindowsize"></a>设置 MaxTransferWindowSize

Windows Communication Foundation 中 (WCF) 的可靠会话使用传输窗口来保存客户端和服务上的消息。 可配置属性 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxTransferWindowSize%2A> 指示传输窗口可以保存多少条消息。

在发送方上，此值指示在等待确认时传输窗口可以保持的消息数;在接收方上，它表示要为服务缓冲多少条消息。

选择适当的大小会影响网络的效率和服务的最佳容量。 以下各节详细说明了在为此属性选择值时应考虑的事项，以及值的影响。

默认传输窗口大小为8条消息。

### <a name="efficient-use-of-the-network"></a>有效地使用网络

在这种情况下，术语 " *网络* " 对应于作为客户端 (发送方) 和服务 (接收方) 之间的通信基础的所有内容。 这包括传输连接以及两者之间的任何中介或桥，包括 SOAP 路由器或 HTTP 代理/防火墙。

有效使用网络可确保充分利用网络容量。 每秒通过网络传输的数据量 (*数据速率*) 和将数据从发送方传输到接收方所需的时间 (*延迟*) 会影响网络的使用效率。

在发送方，属性 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxTransferWindowSize%2A> 指示在等待确认消息时，其传输窗口可以保存多少条消息。 如果网络延迟较高，且为了确保响应式发送方和有效的网络利用率，应增加传输窗口大小。

例如，如果发送方和接收方之间存在多个中介，则延迟可能会很高，或者数据必须通过有损的中介或网络。 因此，发送程序必须等待其传输窗口中的消息确认，然后才能接受要在网络上发送的新消息。 具有较高延迟的缓冲区越小，网络利用率就越低。 另一方面，如果传输窗口太高，则可能会影响服务，因为该服务可能需要与客户端发送的数据的高速率最高。

### <a name="running-the-service-to-capacity"></a>将服务运行到容量

尽可能有效地使用网络，理想情况下，您也希望服务以最佳容量运行。 接收方上的传输窗口大小属性指示接收方可以缓冲多少条消息。 此消息缓冲不仅帮助网络流控制，而且还可让服务满负荷运行。 例如，如果缓冲区是一条消息，并且消息到达的速度比服务可处理的消息的速度快，则网络可能会丢弃消息，容量可能会浪费或利用率。

使用缓冲区可提高服务的可用性，因为它会在处理以前收到的消息时同时接收和缓冲消息。

建议在 `MaxTransferWindowSize` 发送方和接收方均使用相同的。

### <a name="enabling-flow-control"></a>启用流控制

*流控制* 是一种机制，可确保发送方和接收方彼此保持同步，也就是说，消息在生成时就会迅速消耗下来。 客户端和服务上的传输窗口大小可确保发送方和接收方在一个合理的同步窗口中。

强烈建议在 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.FlowControlEnabled%2A> `true` wcf 客户端和 wcf 服务之间使用可靠会话时，将属性设置为。

## <a name="setting-maxpendingchannels"></a>设置 MaxPendingChannels

当编写允许来自不同客户端的可靠会话通信的服务时，可能会有很多客户端同时与服务建立可靠会话。 在这些情况下，服务的响应取决于 `MaxPendingChannels` 属性。

当发送方创建到接收方的可靠会话通道时，发送方和接收方之间的握手将建立可靠会话。 建立可靠会话之后，该通道会放入到挂起的通道队列中以供服务接受。 此 `MaxPendingChannels` 属性指示有多少个通道可以处于此状态。

服务可能处于无法接受更多通道的状态。 如果队列已满，则会拒绝建立可靠会话的尝试，并且客户端必须重试。

队列中挂起的通道也可能会在队列中保留较长的持续时间。 同时，可能会发生可靠会话的非活动超时，导致通道转换到出错状态。

当编写服务来同时服务多个客户端时，应设置一个适合你的需要的值。 为属性设置过高的值会 `MaxPendingChannels` 影响工作集。

的默认值 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.MaxPendingChannels%2A> 为四个通道。

## <a name="reliable-sessions-and-hosting"></a>可靠会话和托管

当 web 托管使用可靠会话的服务时，应注意以下重要注意事项：

- 可靠会话是有状态的，而状态在 AppDomain 中进行维护。 这意味着，属于可靠会话的一部分的所有消息必须在同一个 AppDomain 中进行处理。 Web 场和网络园，其中场或菜园的大小大于一个节点无法保证此约束。

- 使用双 HTTP 通道的可靠会话 (例如，使用 `WsDualHttpBinding`) 可能要求每个客户端的默认值超过两个 http 连接的默认值。 这意味着，双工可靠会话最多可能需要两个连接，因为并发应用程序和协议消息可能会在任意给定时间传输。 在某些情况下，具体取决于服务的消息交换模式，这意味着可以使用双 HTTP 和可靠会话来死锁 web 托管服务。 若要增加每个客户端允许的 HTTP 连接数，请将以下内容添加到相关的配置文件中 (例如 *web.config* 相关服务) ：

  ```xml
  <configuration>
    <system.net>
      <connectionManagement>
        <add name="*" maxconnection="4" />
      </connectionManagement>
    </system.net>
  </configuration>
  ```

  属性的值 `maxconnection` 是所需的连接数。 在这种情况下，最小值应为四个连接。

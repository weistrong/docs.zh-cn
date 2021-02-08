---
description: 了解详细信息：客户端：通道工厂和通道
title: 客户端：通道工厂和通道
ms.date: 03/30/2017
ms.assetid: ef245191-fdab-4468-a0da-7c6f25d2110f
ms.openlocfilehash: b61c37743899b8ba74ec18cc84397e4521e7bde7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803030"
---
# <a name="client-channel-factories-and-channels"></a><span data-ttu-id="91de9-103">客户端：通道工厂和通道</span><span class="sxs-lookup"><span data-stu-id="91de9-103">Client: Channel Factories and Channels</span></span>

<span data-ttu-id="91de9-104">本主题介绍通道工厂和通道的创建。</span><span class="sxs-lookup"><span data-stu-id="91de9-104">This topic discusses the creation of channel factories and channels.</span></span>  
  
## <a name="channel-factories-and-channels"></a><span data-ttu-id="91de9-105">通道工厂和通道</span><span class="sxs-lookup"><span data-stu-id="91de9-105">Channel Factories and Channels</span></span>  

 <span data-ttu-id="91de9-106">通道工厂负责创建通道。</span><span class="sxs-lookup"><span data-stu-id="91de9-106">Channel factories are responsible for creating channels.</span></span> <span data-ttu-id="91de9-107">由通道工厂创建的通道用于发送消息。</span><span class="sxs-lookup"><span data-stu-id="91de9-107">Channels created by channel factories are used for sending messages.</span></span> <span data-ttu-id="91de9-108">这些通道负责获取来自上一层的消息，对消息进行必要的处理，然后将消息发送到下一层。</span><span class="sxs-lookup"><span data-stu-id="91de9-108">These channels are responsible for getting the message from the layer above, performing whatever processing is necessary, then sending the message to the layer below.</span></span> <span data-ttu-id="91de9-109">下图演示此过程。</span><span class="sxs-lookup"><span data-stu-id="91de9-109">The following graphic illustrates this process.</span></span>  
  
 <span data-ttu-id="91de9-110">![客户端工厂和通道](./media/wcfc-wcfchannelsigure2highlevelfactgoriesc.gif "wcfc_WCFChannelsigure2HIghLevelFactgoriesc")</span><span class="sxs-lookup"><span data-stu-id="91de9-110">![Client Factories and Channels](./media/wcfc-wcfchannelsigure2highlevelfactgoriesc.gif "wcfc_WCFChannelsigure2HIghLevelFactgoriesc")</span></span>  
<span data-ttu-id="91de9-111">通道工厂创建通道。</span><span class="sxs-lookup"><span data-stu-id="91de9-111">A channel factory creates channels.</span></span>  
  
 <span data-ttu-id="91de9-112">通道工厂在关闭时负责关闭其创建的但尚未关闭的所有通道。</span><span class="sxs-lookup"><span data-stu-id="91de9-112">When closed, channel factories are responsible for closing any channels they created that are not yet closed.</span></span> <span data-ttu-id="91de9-113">请注意，此处的模型是非对称的，原因是当通道侦听器关闭时，它仅停止接受新通道，而使现有通道保持打开状态以便继续接收消息。</span><span class="sxs-lookup"><span data-stu-id="91de9-113">Note that the model is asymmetric here because when a channel listener is closed, it only stops accepting new channels but leaves existing channels open so that they can continue receiving messages.</span></span>  
  
 <span data-ttu-id="91de9-114">WCF 为此过程提供基类帮助程序。</span><span class="sxs-lookup"><span data-stu-id="91de9-114">WCF provides base class helpers for this process.</span></span> <span data-ttu-id="91de9-115"> (本主题中讨论的通道帮助器类的图示，请参阅 [通道模型概述](channel-model-overview.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="91de9-115">(For a diagram of the channel helper classes discussed in this topic, see [Channel Model Overview](channel-model-overview.md).)</span></span>  
  
- <span data-ttu-id="91de9-116"><xref:System.ServiceModel.Channels.CommunicationObject>类实现 <xref:System.ServiceModel.ICommunicationObject> 并强制执行[开发通道](developing-channels.md)的步骤2中所述的状态机。</span><span class="sxs-lookup"><span data-stu-id="91de9-116">The <xref:System.ServiceModel.Channels.CommunicationObject> class implements <xref:System.ServiceModel.ICommunicationObject> and enforces the state machine described in step 2 of [Developing Channels](developing-channels.md).</span></span>  
  
- <span data-ttu-id="91de9-117"><xref:System.ServiceModel.Channels.ChannelManagerBase> 类实现 <xref:System.ServiceModel.Channels.CommunicationObject> 并为 <xref:System.ServiceModel.Channels.ChannelFactoryBase?displayProperty=nameWithType> 和 <xref:System.ServiceModel.Channels.ChannelListenerBase?displayProperty=nameWithType> 提供统一的基类。</span><span class="sxs-lookup"><span data-stu-id="91de9-117">The <xref:System.ServiceModel.Channels.ChannelManagerBase> class implements <xref:System.ServiceModel.Channels.CommunicationObject> and provides a unified base class for <xref:System.ServiceModel.Channels.ChannelFactoryBase?displayProperty=nameWithType> and <xref:System.ServiceModel.Channels.ChannelListenerBase?displayProperty=nameWithType>.</span></span> <span data-ttu-id="91de9-118"><xref:System.ServiceModel.Channels.ChannelManagerBase> 类与 <xref:System.ServiceModel.Channels.ChannelBase>（用来实现 <xref:System.ServiceModel.Channels.IChannel> 的基类）结合使用。</span><span class="sxs-lookup"><span data-stu-id="91de9-118">The <xref:System.ServiceModel.Channels.ChannelManagerBase> class works in conjunction with <xref:System.ServiceModel.Channels.ChannelBase>, which is a base class that implements <xref:System.ServiceModel.Channels.IChannel>.</span></span>
  
- <span data-ttu-id="91de9-119"><xref:System.ServiceModel.Channels.ChannelFactoryBase>类实现 <xref:System.ServiceModel.Channels.ChannelManagerBase> 和 <xref:System.ServiceModel.Channels.IChannelFactory> ，并将重载合并 `CreateChannel` 到一个 `OnCreateChannel` 抽象方法中。</span><span class="sxs-lookup"><span data-stu-id="91de9-119">The <xref:System.ServiceModel.Channels.ChannelFactoryBase> class implements <xref:System.ServiceModel.Channels.ChannelManagerBase> and <xref:System.ServiceModel.Channels.IChannelFactory> and consolidates the `CreateChannel` overloads into one `OnCreateChannel` abstract method.</span></span>
  
- <span data-ttu-id="91de9-120"><xref:System.ServiceModel.Channels.ChannelListenerBase> 类实现 <xref:System.ServiceModel.Channels.IChannelListener>。</span><span class="sxs-lookup"><span data-stu-id="91de9-120">The <xref:System.ServiceModel.Channels.ChannelListenerBase> class implements <xref:System.ServiceModel.Channels.IChannelListener>.</span></span> <span data-ttu-id="91de9-121">它负责执行基本状态管理。</span><span class="sxs-lookup"><span data-stu-id="91de9-121">It takes care of basic state management.</span></span>
  
 <span data-ttu-id="91de9-122">以下讨论基于 [传输： UDP](../samples/transport-udp.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="91de9-122">The following discussion is based upon the [Transport: UDP](../samples/transport-udp.md) sample.</span></span>  
  
### <a name="creating-a-channel-factory"></a><span data-ttu-id="91de9-123">创建通道工厂</span><span class="sxs-lookup"><span data-stu-id="91de9-123">Creating a Channel Factory</span></span>  

 <span data-ttu-id="91de9-124">`UdpChannelFactory` 派生自 <xref:System.ServiceModel.Channels.ChannelFactoryBase>。</span><span class="sxs-lookup"><span data-stu-id="91de9-124">The `UdpChannelFactory` derives from <xref:System.ServiceModel.Channels.ChannelFactoryBase>.</span></span> <span data-ttu-id="91de9-125">该示例重写 <xref:System.ServiceModel.Channels.ChannelFactoryBase.GetProperty%2A> 以提供对消息编码器的消息版本的访问。</span><span class="sxs-lookup"><span data-stu-id="91de9-125">The sample overrides <xref:System.ServiceModel.Channels.ChannelFactoryBase.GetProperty%2A> to provide access to the message version of the message encoder.</span></span> <span data-ttu-id="91de9-126">该示例还重写 <xref:System.ServiceModel.Channels.ChannelFactoryBase.OnClose%2A> 以在状态机转变时拆开 <xref:System.ServiceModel.Channels.BufferManager> 的实例。</span><span class="sxs-lookup"><span data-stu-id="91de9-126">The sample also overrides <xref:System.ServiceModel.Channels.ChannelFactoryBase.OnClose%2A> to tear down our instance of <xref:System.ServiceModel.Channels.BufferManager> when the state machine transitions.</span></span>  
  
#### <a name="the-udp-output-channel"></a><span data-ttu-id="91de9-127">UDP 输出通道</span><span class="sxs-lookup"><span data-stu-id="91de9-127">The UDP Output Channel</span></span>  

 <span data-ttu-id="91de9-128">`UdpOutputChannel` 实现 <xref:System.ServiceModel.Channels.IOutputChannel>。</span><span class="sxs-lookup"><span data-stu-id="91de9-128">The `UdpOutputChannel` implements <xref:System.ServiceModel.Channels.IOutputChannel>.</span></span> <span data-ttu-id="91de9-129">构造函数对自变量进行验证，并基于传入的 <xref:System.Net.EndPoint> 来构造目标 <xref:System.ServiceModel.EndpointAddress> 对象。</span><span class="sxs-lookup"><span data-stu-id="91de9-129">The constructor validates the arguments and constructs a destination <xref:System.Net.EndPoint> object based on the <xref:System.ServiceModel.EndpointAddress> that is passed in.</span></span>  
  
 <span data-ttu-id="91de9-130">重写 <xref:System.ServiceModel.Channels.CommunicationObject.OnOpen%2A> 将创建用于向此 <xref:System.Net.EndPoint> 发送消息的套接字。</span><span class="sxs-lookup"><span data-stu-id="91de9-130">The override of <xref:System.ServiceModel.Channels.CommunicationObject.OnOpen%2A> creates a socket that is used to send messages to this <xref:System.Net.EndPoint>.</span></span>  
  
 ```csharp
this.socket = new Socket(  
this.remoteEndPoint.AddressFamily,
   SocketType.Dgram,
   ProtocolType.Udp
);  
```  

 <span data-ttu-id="91de9-131">通道可以正常关闭或非正常关闭。</span><span class="sxs-lookup"><span data-stu-id="91de9-131">The channel can be closed gracefully or ungracefully.</span></span> <span data-ttu-id="91de9-132">如果通道正常关闭，则套接字也将关闭，并调用基类 `OnClose` 方法。</span><span class="sxs-lookup"><span data-stu-id="91de9-132">If the channel is closed gracefully the socket is closed and a call is made to the base class `OnClose` method.</span></span> <span data-ttu-id="91de9-133">如果引发异常，则基础结构将调用 `Abort` 以确保清理该通道。</span><span class="sxs-lookup"><span data-stu-id="91de9-133">If this throws an exception, the infrastructure calls `Abort` to ensure the channel is cleaned up.</span></span>  
  
```csharp  
this.socket.Close();  
base.OnClose(timeout);  
```  
  
 <span data-ttu-id="91de9-134">实现 `Send()` 和 `BeginSend()` / `EndSend()` 。</span><span class="sxs-lookup"><span data-stu-id="91de9-134">Implement `Send()` and `BeginSend()`/`EndSend()`.</span></span> <span data-ttu-id="91de9-135">这将分解为两个主要部分。</span><span class="sxs-lookup"><span data-stu-id="91de9-135">This breaks down into two main sections.</span></span> <span data-ttu-id="91de9-136">首先，将消息序列化为字节数组：</span><span class="sxs-lookup"><span data-stu-id="91de9-136">First serialize the message into a byte array:</span></span>  
  
```csharp  
ArraySegment<byte> messageBuffer = EncodeMessage(message);  
```  
  
 <span data-ttu-id="91de9-137">然后，在网络上发送生成的数据：</span><span class="sxs-lookup"><span data-stu-id="91de9-137">Then send the resulting data on the wire:</span></span>  
  
```csharp  
this.socket.SendTo(  
  messageBuffer.Array,
  messageBuffer.Offset,
  messageBuffer.Count,
  SocketFlags.None,
  this.remoteEndPoint  
);  
```  
  
## <a name="see-also"></a><span data-ttu-id="91de9-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="91de9-138">See also</span></span>

- [<span data-ttu-id="91de9-139">开发通道</span><span class="sxs-lookup"><span data-stu-id="91de9-139">Developing Channels</span></span>](developing-channels.md)

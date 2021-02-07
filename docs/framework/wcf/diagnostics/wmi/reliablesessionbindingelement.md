---
description: 了解详细信息： ReliableSessionBindingElement
title: ReliableSessionBindingElement
ms.date: 03/30/2017
ms.assetid: effda125-b8d3-4de6-8c0e-f59f5ea8f6eb
ms.openlocfilehash: 582fd62a8751a31c2834b7d81219a237c9887236
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743858"
---
# <a name="reliablesessionbindingelement"></a><span data-ttu-id="79974-103">ReliableSessionBindingElement</span><span class="sxs-lookup"><span data-stu-id="79974-103">ReliableSessionBindingElement</span></span>

<span data-ttu-id="79974-104">ReliableSessionBindingElement</span><span class="sxs-lookup"><span data-stu-id="79974-104">ReliableSessionBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79974-105">语法</span><span class="sxs-lookup"><span data-stu-id="79974-105">Syntax</span></span>  
  
```csharp
class ReliableSessionBindingElement : BindingElement  
{  
  datetime AcknowledgementInterval;  
  boolean FlowControlEnabled;  
  datetime InactivityTimeout;  
  sint32 MaxPendingChannels;  
  sint32 MaxRetryCount;  
  sint32 MaxTransferWindowSize;  
  boolean Ordered;  
  integer ReliableMessagingVersion;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="79974-106">方法</span><span class="sxs-lookup"><span data-stu-id="79974-106">Methods</span></span>  

 <span data-ttu-id="79974-107">ReliableSessionBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="79974-107">The ReliableSessionBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="79974-108">属性</span><span class="sxs-lookup"><span data-stu-id="79974-108">Properties</span></span>  

 <span data-ttu-id="79974-109">ReliableSessionBindingElement 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="79974-109">The ReliableSessionBindingElement class has the following properties:</span></span>  
  
### <a name="acknowledgementinterval"></a><span data-ttu-id="79974-110">AcknowledgementInterval</span><span class="sxs-lookup"><span data-stu-id="79974-110">AcknowledgementInterval</span></span>  

 <span data-ttu-id="79974-111">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="79974-111">Data type: datetime</span></span>  
  
 <span data-ttu-id="79974-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-113">向工厂创建的可靠通道上的消息源发送确认之前目标等待的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="79974-113">The interval of time that a destination waits before sending an acknowledgement to the message source on reliable channels that are created by the factory.</span></span>  
  
### <a name="flowcontrolenabled"></a><span data-ttu-id="79974-114">FlowControlEnabled</span><span class="sxs-lookup"><span data-stu-id="79974-114">FlowControlEnabled</span></span>  

 <span data-ttu-id="79974-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="79974-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="79974-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-117">一个布尔值，指定是否启用流控制。</span><span class="sxs-lookup"><span data-stu-id="79974-117">A Boolean value that specifies whether flow control is enabled.</span></span>  
  
### <a name="inactivitytimeout"></a><span data-ttu-id="79974-118">InactivityTimeout</span><span class="sxs-lookup"><span data-stu-id="79974-118">InactivityTimeout</span></span>  

 <span data-ttu-id="79974-119">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="79974-119">Data type: datetime</span></span>  
  
 <span data-ttu-id="79974-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-121">指定通道出错之前，通道允许其他通信方不发送任何消息的最长持续时间。</span><span class="sxs-lookup"><span data-stu-id="79974-121">Specifies the maximum duration the channel is going to allow the other communicating party not to send any messages before faulting the channel.</span></span>  
  
### <a name="maxpendingchannels"></a><span data-ttu-id="79974-122">MaxPendingChannels</span><span class="sxs-lookup"><span data-stu-id="79974-122">MaxPendingChannels</span></span>  

 <span data-ttu-id="79974-123">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="79974-123">Data type: sint32</span></span>  
  
 <span data-ttu-id="79974-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-125">侦听器上可等待接受的最大通道数。</span><span class="sxs-lookup"><span data-stu-id="79974-125">The maximum number of channels that can wait to be accepted on the listener.</span></span>  
  
### <a name="maxretrycount"></a><span data-ttu-id="79974-126">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="79974-126">MaxRetryCount</span></span>  

 <span data-ttu-id="79974-127">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="79974-127">Data type: sint32</span></span>  
  
 <span data-ttu-id="79974-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-129">可靠通道未收到消息确认时，通过在其基础通道上调用 `Send` 尝试重新传输该消息的最多尝试次数。</span><span class="sxs-lookup"><span data-stu-id="79974-129">The maximum number of times a reliable channel attempts to retransmit a message it has not received an acknowledgement for, by calling `Send` on its underlying channel.</span></span>  
  
### <a name="maxtransferwindowsize"></a><span data-ttu-id="79974-130">MaxTransferWindowSize</span><span class="sxs-lookup"><span data-stu-id="79974-130">MaxTransferWindowSize</span></span>  

 <span data-ttu-id="79974-131">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="79974-131">Data type: sint32</span></span>  
  
 <span data-ttu-id="79974-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-133">可靠会话的最大传输窗口大小。</span><span class="sxs-lookup"><span data-stu-id="79974-133">The maximum transfer window size for the reliable session.</span></span>  
  
### <a name="ordered"></a><span data-ttu-id="79974-134">已订购</span><span class="sxs-lookup"><span data-stu-id="79974-134">Ordered</span></span>  

 <span data-ttu-id="79974-135">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="79974-135">Data type: boolean</span></span>  
  
 <span data-ttu-id="79974-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-137">一个布尔值，指定是否保证消息以其发送顺序抵达。</span><span class="sxs-lookup"><span data-stu-id="79974-137">A Boolean value that specifies whether messages are guaranteed to arrive in the order they were sent.</span></span>  
  
### <a name="reliablemessagingversion"></a><span data-ttu-id="79974-138">ReliableMessagingVersion</span><span class="sxs-lookup"><span data-stu-id="79974-138">ReliableMessagingVersion</span></span>  

 <span data-ttu-id="79974-139">数据类型：Integer</span><span class="sxs-lookup"><span data-stu-id="79974-139">Data type: integer</span></span>  
  
 <span data-ttu-id="79974-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="79974-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="79974-141">一个整数，指定可靠会话中使用的 WS-ReliableMessaging 协议版本。</span><span class="sxs-lookup"><span data-stu-id="79974-141">An integer that specifies the WS-ReliableMessaging protocol version used in the reliable session.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79974-142">要求</span><span class="sxs-lookup"><span data-stu-id="79974-142">Requirements</span></span>  
  
|<span data-ttu-id="79974-143">MOF</span><span class="sxs-lookup"><span data-stu-id="79974-143">MOF</span></span>|<span data-ttu-id="79974-144">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="79974-144">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="79974-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="79974-145">Namespace</span></span>|<span data-ttu-id="79974-146">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="79974-146">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="79974-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="79974-147">See also</span></span>

- <xref:System.ServiceModel.Channels.ReliableSessionBindingElement>

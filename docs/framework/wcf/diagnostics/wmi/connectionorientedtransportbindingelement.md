---
description: 了解详细信息： ConnectionOrientedTransportBindingElement
title: ConnectionOrientedTransportBindingElement
ms.date: 03/30/2017
ms.assetid: c1308313-f0e2-49e6-977d-6b4ce9ad35d1
ms.openlocfilehash: bd0c05fc86ad7bc95837cee7e22ea83975369b62
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757574"
---
# <a name="connectionorientedtransportbindingelement"></a><span data-ttu-id="53c76-103">ConnectionOrientedTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="53c76-103">ConnectionOrientedTransportBindingElement</span></span>

<span data-ttu-id="53c76-104">ConnectionOrientedTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="53c76-104">ConnectionOrientedTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53c76-105">语法</span><span class="sxs-lookup"><span data-stu-id="53c76-105">Syntax</span></span>  
  
```csharp
class ConnectionOrientedTransportBindingElement : TransportBindingElement  
{  
  datetime ChannelInitializationTimeout;  
  sint32 ConnectionBufferSize;  
  string HostNameComparisonMode;  
  sint32 MaxBufferSize;  
  datetime MaxOutputDelay;  
  sint32 MaxPendingAccepts;  
  sint32 MaxPendingConnections;  
  string TransferMode;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="53c76-106">方法</span><span class="sxs-lookup"><span data-stu-id="53c76-106">Methods</span></span>  

 <span data-ttu-id="53c76-107">ConnectionOrientedTransportBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="53c76-107">The ConnectionOrientedTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="53c76-108">属性</span><span class="sxs-lookup"><span data-stu-id="53c76-108">Properties</span></span>  

 <span data-ttu-id="53c76-109">ConnectionOrientedTransportBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="53c76-109">The ConnectionOrientedTransportBindingElement class has the following properties:</span></span>  
  
### <a name="channelinitializationtimeout"></a><span data-ttu-id="53c76-110">ChannelInitializationTimeout</span><span class="sxs-lookup"><span data-stu-id="53c76-110">ChannelInitializationTimeout</span></span>  

 <span data-ttu-id="53c76-111">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="53c76-111">Data type: datetime</span></span>  
  
 <span data-ttu-id="53c76-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-113">指定在超时前可用于完成通道初始化的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="53c76-113">The timespan that specifies how long the channel initialization has to complete before timing out.</span></span>  
  
### <a name="connectionbuffersize"></a><span data-ttu-id="53c76-114">ConnectionBufferSize</span><span class="sxs-lookup"><span data-stu-id="53c76-114">ConnectionBufferSize</span></span>  

 <span data-ttu-id="53c76-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="53c76-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="53c76-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-117">用于从客户端或服务传输网络上的序列化消息块的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="53c76-117">The size of the buffer used to transmit a chunk of the serialized message on the wire from the client or service.</span></span>  
  
### <a name="hostnamecomparisonmode"></a><span data-ttu-id="53c76-118">HostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="53c76-118">HostNameComparisonMode</span></span>  

 <span data-ttu-id="53c76-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53c76-119">Data type: string</span></span>  
  
 <span data-ttu-id="53c76-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-121">一个值，指示在对 URI 进行匹配时，是否使用主机名来访问服务。</span><span class="sxs-lookup"><span data-stu-id="53c76-121">A value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>  
  
### <a name="maxbuffersize"></a><span data-ttu-id="53c76-122">MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="53c76-122">MaxBufferSize</span></span>  

 <span data-ttu-id="53c76-123">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="53c76-123">Data type: sint32</span></span>  
  
 <span data-ttu-id="53c76-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-125">要使用的缓冲区最大大小。</span><span class="sxs-lookup"><span data-stu-id="53c76-125">The maximum size of the buffer to use.</span></span>  
  
### <a name="maxoutputdelay"></a><span data-ttu-id="53c76-126">MaxOutputDelay</span><span class="sxs-lookup"><span data-stu-id="53c76-126">MaxOutputDelay</span></span>  

 <span data-ttu-id="53c76-127">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="53c76-127">Data type: datetime</span></span>  
  
 <span data-ttu-id="53c76-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-129">消息块或完整消息在发出之前可以在内存中保持缓冲的最大时间间隔。</span><span class="sxs-lookup"><span data-stu-id="53c76-129">The maximum interval of time that a chunk of a message or a full message can remain buffered in memory before being sent out.</span></span>  
  
### <a name="maxpendingaccepts"></a><span data-ttu-id="53c76-130">MaxPendingAccepts</span><span class="sxs-lookup"><span data-stu-id="53c76-130">MaxPendingAccepts</span></span>  

 <span data-ttu-id="53c76-131">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="53c76-131">Data type: sint32</span></span>  
  
 <span data-ttu-id="53c76-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-133">可用于处理服务上的传入连接的最大挂起异步接受线程数。</span><span class="sxs-lookup"><span data-stu-id="53c76-133">The maximum number of pending asynchronous accept threads that are available for processing incoming connections on the service.</span></span>  
  
### <a name="maxpendingconnections"></a><span data-ttu-id="53c76-134">MaxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="53c76-134">MaxPendingConnections</span></span>  

 <span data-ttu-id="53c76-135">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="53c76-135">Data type: sint32</span></span>  
  
 <span data-ttu-id="53c76-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-137">最大挂起连接数。</span><span class="sxs-lookup"><span data-stu-id="53c76-137">The maximum number of pending connections.</span></span>  
  
### <a name="transfermode"></a><span data-ttu-id="53c76-138">TransferMode</span><span class="sxs-lookup"><span data-stu-id="53c76-138">TransferMode</span></span>  

 <span data-ttu-id="53c76-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53c76-139">Data type: string</span></span>  
  
 <span data-ttu-id="53c76-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53c76-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53c76-141">一个值，指定通过面向连接的传输对消息进行缓冲还是流处理。</span><span class="sxs-lookup"><span data-stu-id="53c76-141">A value that specifies whether the messages are buffered or streamed with the connection-oriented transport.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53c76-142">要求</span><span class="sxs-lookup"><span data-stu-id="53c76-142">Requirements</span></span>  
  
|<span data-ttu-id="53c76-143">MOF</span><span class="sxs-lookup"><span data-stu-id="53c76-143">MOF</span></span>|<span data-ttu-id="53c76-144">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="53c76-144">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="53c76-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="53c76-145">Namespace</span></span>|<span data-ttu-id="53c76-146">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="53c76-146">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="53c76-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="53c76-147">See also</span></span>

- <xref:System.ServiceModel.Channels.ConnectionOrientedTransportBindingElement>

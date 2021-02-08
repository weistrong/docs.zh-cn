---
description: 了解详细信息： MsmqBindingElementBase
title: MsmqBindingElementBase
ms.date: 03/30/2017
ms.assetid: 210d41ab-a2a4-4d7a-afd2-0916c08a4015
ms.openlocfilehash: 3aa5ec2343d73798f1cf5e3c7d4b5a8282f97ac9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803173"
---
# <a name="msmqbindingelementbase"></a><span data-ttu-id="131aa-103">MsmqBindingElementBase</span><span class="sxs-lookup"><span data-stu-id="131aa-103">MsmqBindingElementBase</span></span>

<span data-ttu-id="131aa-104">MsmqBindingElementBase</span><span class="sxs-lookup"><span data-stu-id="131aa-104">MsmqBindingElementBase</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="131aa-105">语法</span><span class="sxs-lookup"><span data-stu-id="131aa-105">Syntax</span></span>  
  
```csharp  
class MsmqBindingElementBase : TransportBindingElement  
{  
  string CustomDeadLetterQueue;  
  string DeadLetterQueue;  
  boolean Durable;  
  boolean ExactlyOnce;  
  sint32 MaxRetryCycles;  
  string ReceiveErrorHandling;  
  sint32 ReceiveRetryCount;  
  datetime RetryCycleDelay;  
  datetime TimeToLive;  
  boolean UseMsmqTracing;  
  boolean UseSourceJournal;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="131aa-106">方法</span><span class="sxs-lookup"><span data-stu-id="131aa-106">Methods</span></span>  

 <span data-ttu-id="131aa-107">MsmqBindingElementBase 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="131aa-107">The MsmqBindingElementBase class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="131aa-108">属性</span><span class="sxs-lookup"><span data-stu-id="131aa-108">Properties</span></span>  

 <span data-ttu-id="131aa-109">MsmqBindingElementBase 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="131aa-109">The MsmqBindingElementBase class has the following properties:</span></span>  
  
### <a name="customdeadletterqueue"></a><span data-ttu-id="131aa-110">CustomDeadLetterQueue</span><span class="sxs-lookup"><span data-stu-id="131aa-110">CustomDeadLetterQueue</span></span>  

 <span data-ttu-id="131aa-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="131aa-111">Data type: string</span></span>  
  
 <span data-ttu-id="131aa-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-113">一个 URI，其中包含每个应用程序的死信队列位置（用于放置已过期的消息或传输/传递失败的消息的位置）。</span><span class="sxs-lookup"><span data-stu-id="131aa-113">A URI that contains the location of the dead letter queue for each application, where messages that have expired or that have failed transfer or delivery are placed.</span></span>  
  
### <a name="deadletterqueue"></a><span data-ttu-id="131aa-114">DeadLetterQueue</span><span class="sxs-lookup"><span data-stu-id="131aa-114">DeadLetterQueue</span></span>  

 <span data-ttu-id="131aa-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="131aa-115">Data type: string</span></span>  
  
 <span data-ttu-id="131aa-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-117">一个枚举值，指示要使用的死信队列的类型。</span><span class="sxs-lookup"><span data-stu-id="131aa-117">An enumeration value that indicates the type of dead letter queue to use.</span></span>  
  
### <a name="durable"></a><span data-ttu-id="131aa-118">Durable</span><span class="sxs-lookup"><span data-stu-id="131aa-118">Durable</span></span>  

 <span data-ttu-id="131aa-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="131aa-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="131aa-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-121">一个值，指示此绑定处理的消息是持久的还是可变的。</span><span class="sxs-lookup"><span data-stu-id="131aa-121">A value that indicates whether the messages processed by this binding are durable or volatile.</span></span>  
  
### <a name="exactlyonce"></a><span data-ttu-id="131aa-122">ExactlyOnce</span><span class="sxs-lookup"><span data-stu-id="131aa-122">ExactlyOnce</span></span>  

 <span data-ttu-id="131aa-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="131aa-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="131aa-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-125">一个 Boolean 值，指示是否只接收过一次此绑定处理的消息。</span><span class="sxs-lookup"><span data-stu-id="131aa-125">A Boolean value that indicates whether messages processed by this binding are received exactly once.</span></span>  
  
### <a name="maxretrycycles"></a><span data-ttu-id="131aa-126">MaxRetryCycles</span><span class="sxs-lookup"><span data-stu-id="131aa-126">MaxRetryCycles</span></span>  

 <span data-ttu-id="131aa-127">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="131aa-127">Data type: sint32</span></span>  
  
 <span data-ttu-id="131aa-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-129">尝试向接收应用程序传递消息的最大重试周期数。</span><span class="sxs-lookup"><span data-stu-id="131aa-129">The maximum number of retry cycles to attempt delivery of messages to the receiving application.</span></span>  
  
### <a name="receiveerrorhandling"></a><span data-ttu-id="131aa-130">ReceiveErrorHandling</span><span class="sxs-lookup"><span data-stu-id="131aa-130">ReceiveErrorHandling</span></span>  

 <span data-ttu-id="131aa-131">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="131aa-131">Data type: string</span></span>  
  
 <span data-ttu-id="131aa-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-133">病毒消息处理设置。</span><span class="sxs-lookup"><span data-stu-id="131aa-133">The settings for poison message handling.</span></span>  
  
### <a name="receiveretrycount"></a><span data-ttu-id="131aa-134">ReceiveRetryCount</span><span class="sxs-lookup"><span data-stu-id="131aa-134">ReceiveRetryCount</span></span>  

 <span data-ttu-id="131aa-135">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="131aa-135">Data type: sint32</span></span>  
  
 <span data-ttu-id="131aa-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-137">从应用程序队列读取消息的最大立即重试次数。</span><span class="sxs-lookup"><span data-stu-id="131aa-137">The maximum number of immediate retry attempts on a message that is read from the application queue.</span></span>  
  
### <a name="retrycycledelay"></a><span data-ttu-id="131aa-138">RetryCycleDelay</span><span class="sxs-lookup"><span data-stu-id="131aa-138">RetryCycleDelay</span></span>  

 <span data-ttu-id="131aa-139">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="131aa-139">Data type: datetime</span></span>  
  
 <span data-ttu-id="131aa-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-141">一个值，指示尝试传递无法立即传递的消息时，重试周期之间的时间延迟。</span><span class="sxs-lookup"><span data-stu-id="131aa-141">A value that indicates the time delay between retry cycles when attempting to deliver a message that could not be delivered immediately.</span></span>  
  
### <a name="timetolive"></a><span data-ttu-id="131aa-142">timeToLive</span><span class="sxs-lookup"><span data-stu-id="131aa-142">TimeToLive</span></span>  

 <span data-ttu-id="131aa-143">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="131aa-143">Data type: datetime</span></span>  
  
 <span data-ttu-id="131aa-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-145">时间间隔，指示此绑定所处理的消息在过期之前可以保留在队列中的时间。</span><span class="sxs-lookup"><span data-stu-id="131aa-145">The interval of time that indicates how long the messages processed by this binding can be in the queue before they expire.</span></span>  
  
### <a name="usemsmqtracing"></a><span data-ttu-id="131aa-146">UseMsmqTracing</span><span class="sxs-lookup"><span data-stu-id="131aa-146">UseMsmqTracing</span></span>  

 <span data-ttu-id="131aa-147">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="131aa-147">Data type: boolean</span></span>  
  
 <span data-ttu-id="131aa-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-149">一个 Boolean 值，指示是否应跟踪此绑定处理的消息。</span><span class="sxs-lookup"><span data-stu-id="131aa-149">A Boolean value that indicates whether messages processed by this binding should be traced.</span></span>  
  
### <a name="usesourcejournal"></a><span data-ttu-id="131aa-150">UseSourceJournal</span><span class="sxs-lookup"><span data-stu-id="131aa-150">UseSourceJournal</span></span>  

 <span data-ttu-id="131aa-151">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="131aa-151">Data type: boolean</span></span>  
  
 <span data-ttu-id="131aa-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="131aa-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="131aa-153">一个 Boolean 值，指示此绑定所处理的消息副本是否应存储在源日志队列中。</span><span class="sxs-lookup"><span data-stu-id="131aa-153">A Boolean value that indicates whether copies of messages processed by this binding should be stored in the source journal queue.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="131aa-154">要求</span><span class="sxs-lookup"><span data-stu-id="131aa-154">Requirements</span></span>  
  
|<span data-ttu-id="131aa-155">MOF</span><span class="sxs-lookup"><span data-stu-id="131aa-155">MOF</span></span>|<span data-ttu-id="131aa-156">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="131aa-156">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="131aa-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="131aa-157">Namespace</span></span>|<span data-ttu-id="131aa-158">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="131aa-158">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="131aa-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="131aa-159">See also</span></span>

- <xref:System.ServiceModel.NetMsmqBinding>
- <xref:System.ServiceModel.MsmqBindingBase>

---
description: 了解详细信息： <serviceThrottling>
title: <serviceThrottling>
ms.date: 03/30/2017
ms.assetid: a337d064-1e64-4209-b4a9-db7fdb7e3eaf
ms.openlocfilehash: eb65f6d60a266a367789d87e4e6ea10ebfd2c7a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786676"
---
# \<serviceThrottling>

<span data-ttu-id="1dafb-102">指定 Windows Communication Foundation (WCF) 服务的限制机制。</span><span class="sxs-lookup"><span data-stu-id="1dafb-102">Specifies the throttling mechanism of a Windows Communication Foundation (WCF) service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceThrottling>**  
  
## <a name="syntax"></a><span data-ttu-id="1dafb-103">语法</span><span class="sxs-lookup"><span data-stu-id="1dafb-103">Syntax</span></span>  
  
```xml  
<serviceThrottling maxConcurrentCalls="Integer"
                   maxConcurrentInstances="Integer"
                   maxConcurrentSessions="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1dafb-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1dafb-104">Attributes and Elements</span></span>  

 <span data-ttu-id="1dafb-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1dafb-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1dafb-106">特性</span><span class="sxs-lookup"><span data-stu-id="1dafb-106">Attributes</span></span>  
  
|<span data-ttu-id="1dafb-107">属性</span><span class="sxs-lookup"><span data-stu-id="1dafb-107">Attribute</span></span>|<span data-ttu-id="1dafb-108">说明</span><span class="sxs-lookup"><span data-stu-id="1dafb-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1dafb-109">maxConcurrentCalls</span><span class="sxs-lookup"><span data-stu-id="1dafb-109">maxConcurrentCalls</span></span>|<span data-ttu-id="1dafb-110">一个正整数，用于限制当前在整个 <xref:System.ServiceModel.ServiceHost> 中处理的消息数目。</span><span class="sxs-lookup"><span data-stu-id="1dafb-110">A positive integer that limits the number of messages that currently process across a <xref:System.ServiceModel.ServiceHost>.</span></span> <span data-ttu-id="1dafb-111">超出此限制的调用将在队列中排队。</span><span class="sxs-lookup"><span data-stu-id="1dafb-111">Calls in excess of the limit are queued.</span></span> <span data-ttu-id="1dafb-112">将此值设置为 0 与将其设置为 Int32.MaxValue 等效。</span><span class="sxs-lookup"><span data-stu-id="1dafb-112">Setting this value to 0 is equivalent to setting it to Int32.MaxValue.</span></span> <span data-ttu-id="1dafb-113">默认值是 16 \* 处理器计数。</span><span class="sxs-lookup"><span data-stu-id="1dafb-113">The default is 16 \* processor count.</span></span>|  
|<span data-ttu-id="1dafb-114">maxConcurrentInstances</span><span class="sxs-lookup"><span data-stu-id="1dafb-114">maxConcurrentInstances</span></span>|<span data-ttu-id="1dafb-115">一个正整数，用于限制在整个 <xref:System.ServiceModel.InstanceContext> 中一次执行的 <xref:System.ServiceModel.ServiceHost> 对象数。</span><span class="sxs-lookup"><span data-stu-id="1dafb-115">A positive integer that limits the number of <xref:System.ServiceModel.InstanceContext> objects that execute at one time across a <xref:System.ServiceModel.ServiceHost>.</span></span> <span data-ttu-id="1dafb-116">用于创建其他实例的请求将会排队，并在出现低于该限值的槽时完成。</span><span class="sxs-lookup"><span data-stu-id="1dafb-116">Requests to create additional instances are queued and complete when a slot below the limit becomes available.</span></span> <span data-ttu-id="1dafb-117">默认值是 maxConcurrentSessions 和 MaxConcurrentCalls 的和</span><span class="sxs-lookup"><span data-stu-id="1dafb-117">The default is the sum of maxConcurrentSessions and MaxConcurrentCalls</span></span>|  
|<span data-ttu-id="1dafb-118">maxConcurrentSessions</span><span class="sxs-lookup"><span data-stu-id="1dafb-118">maxConcurrentSessions</span></span>|<span data-ttu-id="1dafb-119">一个正整数，用于限制 <xref:System.ServiceModel.ServiceHost> 对象可以接受的会话数。</span><span class="sxs-lookup"><span data-stu-id="1dafb-119">A positive integer that limits the number of sessions a <xref:System.ServiceModel.ServiceHost> object can accept.</span></span><br /><br /> <span data-ttu-id="1dafb-120">此服务将接受超出限制的连接，但是，只有处于限制范围之内的通道处于活动状态（会从此通道中读取消息）。</span><span class="sxs-lookup"><span data-stu-id="1dafb-120">The service will accept connections in excess of the limit, but only the channels below the limit are active (messages are read from the channel).</span></span> <span data-ttu-id="1dafb-121">将此值设置为 0 与将其设置为 Int32.MaxValue 等效。</span><span class="sxs-lookup"><span data-stu-id="1dafb-121">Setting this value to 0 is equivalent to setting it to Int32.MaxValue.</span></span> <span data-ttu-id="1dafb-122">默认值是 100 \* 处理器计数。</span><span class="sxs-lookup"><span data-stu-id="1dafb-122">The default is 100 \* processor count.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1dafb-123">子元素</span><span class="sxs-lookup"><span data-stu-id="1dafb-123">Child Elements</span></span>  

 <span data-ttu-id="1dafb-124">无。</span><span class="sxs-lookup"><span data-stu-id="1dafb-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1dafb-125">父元素</span><span class="sxs-lookup"><span data-stu-id="1dafb-125">Parent Elements</span></span>  
  
|<span data-ttu-id="1dafb-126">元素</span><span class="sxs-lookup"><span data-stu-id="1dafb-126">Element</span></span>|<span data-ttu-id="1dafb-127">说明</span><span class="sxs-lookup"><span data-stu-id="1dafb-127">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="1dafb-128">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="1dafb-128">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1dafb-129">备注</span><span class="sxs-lookup"><span data-stu-id="1dafb-129">Remarks</span></span>  

 <span data-ttu-id="1dafb-130">限制控件会对并发调用、实例或会话的数目施加限制以防止过度使用资源。</span><span class="sxs-lookup"><span data-stu-id="1dafb-130">Throttling controls place limits on the number of concurrent calls, instances, or sessions to prevent over-consumption of resources.</span></span>  
  
 <span data-ttu-id="1dafb-131">每次达到属性值时，就会记录一个跟踪。</span><span class="sxs-lookup"><span data-stu-id="1dafb-131">A trace is written every time the value of attributes is reached.</span></span> <span data-ttu-id="1dafb-132">第一个跟踪将记录为警告。</span><span class="sxs-lookup"><span data-stu-id="1dafb-132">The first trace is written as a warning.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1dafb-133">示例</span><span class="sxs-lookup"><span data-stu-id="1dafb-133">Example</span></span>  

 <span data-ttu-id="1dafb-134">下面的配置示例指定服务将最大并发调用数限制为 2，并将最大并发实例数限制为 10。</span><span class="sxs-lookup"><span data-stu-id="1dafb-134">The following configuration example specifies that the service limits the maximum concurrent calls to 2, and the maximum number of concurrent instances to 10.</span></span> <span data-ttu-id="1dafb-135">有关运行此示例的详细示例，请参阅 [限制](../../../wcf/samples/throttling.md)。</span><span class="sxs-lookup"><span data-stu-id="1dafb-135">For a detailed example of running this example, see [Throttling](../../../wcf/samples/throttling.md).</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDebug includeExceptionDetailInFaults="False" />
      <serviceMetadata httpGetEnabled="True" />
      <!-- Specify throttling behavior -->
      <serviceThrottling maxConcurrentCalls="2"
                         maxConcurrentInstances="10" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="1dafb-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="1dafb-136">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
- <xref:System.ServiceModel.Configuration.ServiceThrottlingElement>
- [<span data-ttu-id="1dafb-137">使用 ServiceThrottlingBehavior 控制 WCF 服务性能</span><span class="sxs-lookup"><span data-stu-id="1dafb-137">Using ServiceThrottlingBehavior to Control WCF Service Performance</span></span>](../../../wcf/feature-details/using-servicethrottlingbehavior-to-control-wcf-service-performance.md)

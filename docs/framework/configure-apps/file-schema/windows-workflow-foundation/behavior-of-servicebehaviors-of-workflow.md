---
description: 了解有关 <behavior> 工作流的详细信息 <serviceBehaviors>
title: <behavior><serviceBehaviors>工作流的
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 6a4b718a-1b40-4957-935a-f6122819ab3c
ms.openlocfilehash: 7504e9b307286871440bb6efdb672a59d3d13cb1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725280"
---
# <a name="behavior-of-servicebehaviors-of-workflow"></a><span data-ttu-id="06a68-103">\<behavior>\<serviceBehaviors>工作流的</span><span class="sxs-lookup"><span data-stu-id="06a68-103">\<behavior> of \<serviceBehaviors> of workflow</span></span>

<span data-ttu-id="06a68-104">**行为** 元素包含服务行为的设置集合。</span><span class="sxs-lookup"><span data-stu-id="06a68-104">The **behavior** element contains a collection of settings for the behavior of a service.</span></span> <span data-ttu-id="06a68-105">每个行为都按其 **名称** 编制索引。</span><span class="sxs-lookup"><span data-stu-id="06a68-105">Each behavior is indexed by its **name**.</span></span> <span data-ttu-id="06a68-106">服务可以使用元素的 **behaviorConfiguration** 特性通过此名称链接到每个行为 [\<endpoint>](../wcf/endpoint-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="06a68-106">Services can link to each behavior through this name using the **behaviorConfiguration** attribute of the [\<endpoint>](../wcf/endpoint-element.md) element.</span></span> <span data-ttu-id="06a68-107">这样，终结点可以共享公共行为配置而不用重新定义设置。</span><span class="sxs-lookup"><span data-stu-id="06a68-107">This allows endpoints to share common behavior configurations without redefining the settings.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<behavior>**  
  
## <a name="syntax"></a><span data-ttu-id="06a68-108">语法</span><span class="sxs-lookup"><span data-stu-id="06a68-108">Syntax</span></span>  
  
```xml  
<system.ServiceModel>  
  <behaviors>  
    <serviceBehaviors>  
      <behavior name="String">
        <bufferReceive maxPendingMessagesPerChannel="Integer" />
        <etwTracking profileName="String" />
        <sendMessageChannelCache allowUnsafeCaching="Boolean">
          <channelSettings idleTimeout="TimeSpan"
                           leaseTimeout="TimeSpan"
                           maxItemsInCache="Integer" />
          <factorySettings idleTimeout="TimeSpan"
                           leaseTimeout="TimeSpan"
                           maxItemsInCache="Integer" />
        </sendMessageChannelCache>
        <sqlWorkflowInstanceStore connectionStringName="String"
                                  hostLockRenewalPeriod="TimeSpan"
                                  instanceCompletionAction="DeleteNothing/DeleteAll"
                                  instanceEncodingAction="None/GZip"
                                  instanceLockedExceptionAction="NoRetry/BasicRetry/AggressiveRetry"
                                  runnableInstancesDetectionPeriod="TimeSpan" />
        <workflowIdle timeToPersist="TimeSpan"
                      timeToUnload="TimeSpan" />
        <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
      </behavior>
    </serviceBehaviors>  
  </behaviors>  
</system.ServiceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="06a68-109">特性和元素</span><span class="sxs-lookup"><span data-stu-id="06a68-109">Attributes and Elements</span></span>  

 <span data-ttu-id="06a68-110">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06a68-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="06a68-111">特性</span><span class="sxs-lookup"><span data-stu-id="06a68-111">Attributes</span></span>  
  
|<span data-ttu-id="06a68-112">属性</span><span class="sxs-lookup"><span data-stu-id="06a68-112">Attribute</span></span>|<span data-ttu-id="06a68-113">说明</span><span class="sxs-lookup"><span data-stu-id="06a68-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="06a68-114">name</span><span class="sxs-lookup"><span data-stu-id="06a68-114">name</span></span>|<span data-ttu-id="06a68-115">一个包含行为的配置名称的唯一字符串。</span><span class="sxs-lookup"><span data-stu-id="06a68-115">A unique string that contains the configuration name of the behavior.</span></span> <span data-ttu-id="06a68-116">此值是用户定义的一个字符串，该字符串必须是唯一的，因为它将充当元素的标识字符串。</span><span class="sxs-lookup"><span data-stu-id="06a68-116">This value is a user-defined string that must be unique, since it acts as the identification string for the element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="06a68-117">子元素</span><span class="sxs-lookup"><span data-stu-id="06a68-117">Child Elements</span></span>  
  
|<span data-ttu-id="06a68-118">元素</span><span class="sxs-lookup"><span data-stu-id="06a68-118">Element</span></span>|<span data-ttu-id="06a68-119">说明</span><span class="sxs-lookup"><span data-stu-id="06a68-119">Description</span></span>|  
|-------------|-----------------|  
|[\<bufferReceive>](bufferreceive.md)|<span data-ttu-id="06a68-120">一种服务行为，允许服务使用缓冲接收处理，以使工作流服务能够处理无序消息。</span><span class="sxs-lookup"><span data-stu-id="06a68-120">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>|  
|[\<routing>](../wcf/routing-of-servicebehavior.md)|<span data-ttu-id="06a68-121">一种服务行为，允许服务使用 <xref:System.Activities.Tracking.EtwTrackingParticipant> 来利用 ETW 跟踪。</span><span class="sxs-lookup"><span data-stu-id="06a68-121">A service behavior that allows a service to utilize ETW tracking using an <xref:System.Activities.Tracking.EtwTrackingParticipant>.</span></span>|  
|[\<sendMessageChannelCache>](sendmessagechannelcache.md)|<span data-ttu-id="06a68-122">一种服务行为，该行为支持缓存共享级别的自定义、通道工厂缓存的设置，以及使用 Send 消息传递活动将消息发送给服务终结点的工作流通道缓存的设置。</span><span class="sxs-lookup"><span data-stu-id="06a68-122">A service behavior that enables the customization of the cache sharing levels, the settings of the channel factory cache, and the settings of the channel cache for workflows that send messages to service endpoints using Send messaging activities.</span></span>|  
|[\<sqlWorkflowInstanceStore>](sqlworkflowinstancestore.md)|<span data-ttu-id="06a68-123">一种服务行为，它允许您配置 <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> 功能，该功能支持将工作流服务实例的状态信息保持到 SQL Server 2005 或 SQL Server 2008 数据库中。</span><span class="sxs-lookup"><span data-stu-id="06a68-123">A service behavior that allows you to configure the <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> feature, which supports persisting state information for workflow service instances into an SQL Server 2005 or SQL Server 2008 database.</span></span>|  
|[\<workflowIdle>](workflowidle.md)|<span data-ttu-id="06a68-124">一种服务行为，可以控制何时卸载和持久保存空闲工作流实例。</span><span class="sxs-lookup"><span data-stu-id="06a68-124">A service behavior that controls when idle workflow instances are unloaded and persisted.</span></span>|  
|[\<workflowInstanceManagement>](workflowinstancemanagement.md)|<span data-ttu-id="06a68-125">一种服务行为，可用于指定控制工作流实例如何运行的设置，包括持久性、未经处理的异常行为和空闲行为。</span><span class="sxs-lookup"><span data-stu-id="06a68-125">A service behavior that enables you to specify settings that control how workflow instances are run, including persistence, unhandled Exception behavior and idle behavior.</span></span>|  
|[\<workflowUnhandledException>](workflowunhandledexception.md)|<span data-ttu-id="06a68-126">一种服务行为，可用于指定工作流服务中发生未经处理的异常时所采取的操作。</span><span class="sxs-lookup"><span data-stu-id="06a68-126">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="06a68-127">父元素</span><span class="sxs-lookup"><span data-stu-id="06a68-127">Parent Elements</span></span>  
  
|<span data-ttu-id="06a68-128">元素</span><span class="sxs-lookup"><span data-stu-id="06a68-128">Element</span></span>|<span data-ttu-id="06a68-129">说明</span><span class="sxs-lookup"><span data-stu-id="06a68-129">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceBehaviors>](servicebehaviors-of-workflow.md)|<span data-ttu-id="06a68-130">服务行为元素的集合。</span><span class="sxs-lookup"><span data-stu-id="06a68-130">A collection of service behavior elements.</span></span>|

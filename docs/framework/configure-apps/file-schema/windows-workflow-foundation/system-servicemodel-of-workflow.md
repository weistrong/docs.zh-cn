---
description: 了解详细信息： <的工作流的 System.servicemodel>
title: <System.servicemodel> 工作流
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 6a8eb2bf-f925-40e1-ba5c-a49b1d3a3ac6
ms.openlocfilehash: 393c1055d6b136ed27a297e00133f5b53d12fd38
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681742"
---
# <a name="systemservicemodel-of-workflow"></a><span data-ttu-id="6bddf-103">\<system.serviceModel> 的工作流</span><span class="sxs-lookup"><span data-stu-id="6bddf-103">\<system.serviceModel> of workflow</span></span>

<span data-ttu-id="6bddf-104">此配置节包含所有工作流配置元素。</span><span class="sxs-lookup"><span data-stu-id="6bddf-104">This configuration section contains all the workflow configuration elements.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<system.ServiceModel>**  
  
## <a name="syntax"></a><span data-ttu-id="6bddf-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bddf-105">Syntax</span></span>  
  
```xml  
<system.ServiceModel>  
  <behaviors>  
    <serviceBehaviors>  
    <behavior name="String">  
      <bufferReceive maxPendingMessagesPerChannel="Integer" />  
      <etwTracking profileName="String" />  
     <sendMessageChannelCache allowUnsafeCaching="Boolean" >
        <channelSettings idleTimeout="TimeSpan" leaseTimeout="TimeSpan" maxItemsInCache="Integer" />  
        <factorySettings idleTimeout="TimeSpan" leaseTimeout="TimeSpan" maxItemsInCache="Integer" />  
     </sendMessageChannelCache>  
      <sqlWorkflowInstanceStore
          connectionStringName="String"
          hostLockRenewalPeriod="TimeSpan"  
          instanceCompletionAction="DeleteNothing/DeleteAll"  
          instanceEncodingAction="None/GZip"  
          instanceLockedExceptionAction="NoRetry/BasicRetry/AggressiveRetry"  
          runnableInstancesDetectionPeriod="TimeSpan" />  
      <workflowIdle timeToPersist="TimeSpan"  
          timeToUnload="TimeSpan" />  
      <workflowUnhandledExceptionAction="Abandon/AbandonAndSuspend/Cancel/Terminate" />  
    </behavior>  
    </serviceBehaviors>  
  </behaviors>  
  <tracking>
     <participants>
      <add name="String"
           profileName="String"  
           type="String" />
     </participants>
    <trackingProfile name="String">  
      <workflow activityDefinitionId="String">  
          <activityScheduledQueries>  
             <activityScheduledQuery activityName="String"  
                 childActivityName="String"/>  
          </activityScheduledQueries>  
             <activityStateQuery activityName="String" />  
                <arguments>  
                   <argument name="String"/>  
                </arguments>  
                <states>  
                   <state name="String"/>  
                </states>  
                <variables>  
                   <variable name="String"/>  
                </variables>  
          </activityStateQueries>  
          <bookmarkResumptionQueries>  
             <bookmarkResumptionQuery name="String" />  
          </bookmarkResumptionQueries>  
          <cancelRequestQueries>  
             <cancelRequestQuery activityName="String"  
                 childActivityName="String"/>  
          </cancelRequestQueries>  
          <customTrackingQueries>  
             <customTrackingQuery activityName="String"  
                 name="String"/>  
          </customTrackingQueries>  
          <faultPropagationQueries>  
             <faultPropagationQuery activityName="String"  
                 faultHandlerActivityName="String"/>  
          </faultPropagationQueries>  
         <workflowInstanceQueries>  
            <workflowInstanceQuery>  
              <states>  
                 <state name="String"/>  
              </states>  
          </workflowInstanceQuery>  
        </workflowInstanceQueries>  
      </workflow>  
    </trackingProfile>
   </profiles>  
  </tracking>  
</system.ServiceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6bddf-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6bddf-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6bddf-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6bddf-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6bddf-108">特性</span><span class="sxs-lookup"><span data-stu-id="6bddf-108">Attributes</span></span>  

 <span data-ttu-id="6bddf-109">无</span><span class="sxs-lookup"><span data-stu-id="6bddf-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6bddf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6bddf-110">Child Elements</span></span>  
  
|<span data-ttu-id="6bddf-111">元素</span><span class="sxs-lookup"><span data-stu-id="6bddf-111">Element</span></span>|<span data-ttu-id="6bddf-112">说明</span><span class="sxs-lookup"><span data-stu-id="6bddf-112">Description</span></span>|  
|-------------|-----------------|  
|[\<behaviors>](behaviors-of-workflow.md)|<span data-ttu-id="6bddf-113">本节定义 **serviceBehaviors** 集合。</span><span class="sxs-lookup"><span data-stu-id="6bddf-113">This section defines the **serviceBehaviors** collection.</span></span>  <span data-ttu-id="6bddf-114">集合中的每个元素定义服务所使用的行为元素。</span><span class="sxs-lookup"><span data-stu-id="6bddf-114">Each element in the collection defines behavior elements consumed by services.</span></span> <span data-ttu-id="6bddf-115">每个行为元素都由其唯一 **名称** 属性标识。</span><span class="sxs-lookup"><span data-stu-id="6bddf-115">Each behavior element is identified by its unique **name** attribute.</span></span>|  
|[\<tracking>](tracking.md)|<span data-ttu-id="6bddf-116">表示一个配置节，用于定义工作流服务的跟踪设置。</span><span class="sxs-lookup"><span data-stu-id="6bddf-116">Represents a configuration section for defining tracking settings for a workflow service.</span></span><br /><br /> <span data-ttu-id="6bddf-117">有关工作流跟踪及其配置的详细信息，请参阅工作流 [跟踪和跟踪](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) 和 [配置工作流跟踪](../../../windows-workflow-foundation/configuring-tracking-for-a-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="6bddf-117">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Configuring Tracking for a Workflow](../../../windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6bddf-118">父元素</span><span class="sxs-lookup"><span data-stu-id="6bddf-118">Parent Elements</span></span>  
  
|<span data-ttu-id="6bddf-119">元素</span><span class="sxs-lookup"><span data-stu-id="6bddf-119">Element</span></span>|<span data-ttu-id="6bddf-120">说明</span><span class="sxs-lookup"><span data-stu-id="6bddf-120">Description</span></span>|  
|-------------|-----------------|  
|[\<configuration>](../configuration-element.md)|<span data-ttu-id="6bddf-121">.NET 配置文件中的所有配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="6bddf-121">The root element for all configuration elements in a .NET configuration file.</span></span>|

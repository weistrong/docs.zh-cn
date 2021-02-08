---
description: 了解有关 WCF 的详细信息： <activityStateQueries>
title: <activityStateQueries> WCF 的
ms.date: 10/08/2018
ms.assetid: 9e45db49-ed85-4fdf-bd65-0d5477e31823
ms.openlocfilehash: 00795a26a37f62fae8aa884b5a4188be79453186
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782229"
---
# <a name="activitystatequeries-of-wcf"></a><span data-ttu-id="4a247-103">\<activityStateQueries> WCF 的</span><span class="sxs-lookup"><span data-stu-id="4a247-103">\<activityStateQueries> of WCF</span></span>

<span data-ttu-id="4a247-104">表示一个查询集合，这些查询用于跟踪构成工作流实例的活动的生命周期更改。</span><span class="sxs-lookup"><span data-stu-id="4a247-104">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="4a247-105">例如，你可能想要跟踪每次在工作流实例中完成 "发送电子邮件" 活动的时间。</span><span class="sxs-lookup"><span data-stu-id="4a247-105">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="4a247-106">跟踪参与者需要用此查询来订阅活动状态记录对象。</span><span class="sxs-lookup"><span data-stu-id="4a247-106">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="4a247-107">在 ActivityStates 中指定了要订阅的可用状态。</span><span class="sxs-lookup"><span data-stu-id="4a247-107">The available states to subscribe to are specified in ActivityStates.</span></span>

<span data-ttu-id="4a247-108">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="4a247-108">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<activityStateQueries>**  
  
## <a name="syntax"></a><span data-ttu-id="4a247-109">语法</span><span class="sxs-lookup"><span data-stu-id="4a247-109">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityStateQueries>
          <activityStateQuery activityName="String">
            <arguments>
              <argument name="String" />
            </arguments>
            <states>
              <state name="String" />
            </states>
            <variables>
              <variable name="String" />
            </variables>
          </activityStateQuery>
        </activityStateQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  

## <a name="attributes-and-elements"></a><span data-ttu-id="4a247-110">特性和元素</span><span class="sxs-lookup"><span data-stu-id="4a247-110">Attributes and elements</span></span>

<span data-ttu-id="4a247-111">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4a247-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a247-112">特性</span><span class="sxs-lookup"><span data-stu-id="4a247-112">Attributes</span></span>  

<span data-ttu-id="4a247-113">无。</span><span class="sxs-lookup"><span data-stu-id="4a247-113">None.</span></span>  

### <a name="child-elements"></a><span data-ttu-id="4a247-114">子元素</span><span class="sxs-lookup"><span data-stu-id="4a247-114">Child elements</span></span>

|<span data-ttu-id="4a247-115">元素</span><span class="sxs-lookup"><span data-stu-id="4a247-115">Element</span></span>|<span data-ttu-id="4a247-116">说明</span><span class="sxs-lookup"><span data-stu-id="4a247-116">Description</span></span>|
|-------------|-----------------|
|[\<activityStateQuery>](activitystatequery-of-wcf.md)|<span data-ttu-id="4a247-117">一个查询，用于跟踪在活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="4a247-117">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="4a247-118">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="4a247-118">This event occurs each time a FaultHandler processes a fault.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="4a247-119">父元素</span><span class="sxs-lookup"><span data-stu-id="4a247-119">Parent elements</span></span>

|<span data-ttu-id="4a247-120">元素</span><span class="sxs-lookup"><span data-stu-id="4a247-120">Element</span></span>|<span data-ttu-id="4a247-121">说明</span><span class="sxs-lookup"><span data-stu-id="4a247-121">Description</span></span>|
|-------------|-----------------|
|[\<workflow>](../windows-workflow-foundation/workflow.md)|<span data-ttu-id="4a247-122">一个配置元素，包含 `activityDefinitionId` 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="4a247-122">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|

## <a name="see-also"></a><span data-ttu-id="4a247-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="4a247-123">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityStateQuery>
- [<span data-ttu-id="4a247-124">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="4a247-124">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="4a247-125">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="4a247-125">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

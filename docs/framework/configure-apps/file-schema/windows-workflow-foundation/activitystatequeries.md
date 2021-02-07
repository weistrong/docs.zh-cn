---
description: 了解详细信息： <activityStateQueries>
title: <activityStateQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: bdd3c8ae-a13f-4df1-9b3c-a9d6c4bb1b5f
ms.openlocfilehash: ad324d88c481016d85b8e58ccc0857b7773d8328
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748955"
---
# \<activityStateQueries>

<span data-ttu-id="d2eae-102">表示一个查询集合，这些查询用于跟踪构成工作流实例的活动的生命周期更改。</span><span class="sxs-lookup"><span data-stu-id="d2eae-102">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="d2eae-103">例如，你可能想要跟踪每次在工作流实例中完成 "发送电子邮件" 活动的时间。</span><span class="sxs-lookup"><span data-stu-id="d2eae-103">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="d2eae-104">跟踪参与者需要用此查询来订阅活动状态记录对象。</span><span class="sxs-lookup"><span data-stu-id="d2eae-104">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="d2eae-105">在 ActivityStates 中指定了要订阅的可用状态。</span><span class="sxs-lookup"><span data-stu-id="d2eae-105">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
 <span data-ttu-id="d2eae-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="d2eae-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<activityStateQueries>**  
  
## <a name="syntax"></a><span data-ttu-id="d2eae-107">语法</span><span class="sxs-lookup"><span data-stu-id="d2eae-107">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String" />
        </arguments>
        <states>
          <state name="String" />
        </states>
        <variables>
         <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d2eae-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d2eae-108">Attributes and Elements</span></span>  

 <span data-ttu-id="d2eae-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2eae-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d2eae-110">特性</span><span class="sxs-lookup"><span data-stu-id="d2eae-110">Attributes</span></span>  

 <span data-ttu-id="d2eae-111">无。</span><span class="sxs-lookup"><span data-stu-id="d2eae-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d2eae-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d2eae-112">Child Elements</span></span>  
  
|<span data-ttu-id="d2eae-113">元素</span><span class="sxs-lookup"><span data-stu-id="d2eae-113">Element</span></span>|<span data-ttu-id="d2eae-114">说明</span><span class="sxs-lookup"><span data-stu-id="d2eae-114">Description</span></span>|  
|-------------|-----------------|  
|[\<activityStateQuery>](activitystatequery.md)|<span data-ttu-id="d2eae-115">一个查询，用于跟踪在活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="d2eae-115">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="d2eae-116">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="d2eae-116">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d2eae-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d2eae-117">Parent Elements</span></span>  
  
|<span data-ttu-id="d2eae-118">元素</span><span class="sxs-lookup"><span data-stu-id="d2eae-118">Element</span></span>|<span data-ttu-id="d2eae-119">说明</span><span class="sxs-lookup"><span data-stu-id="d2eae-119">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](workflow.md)|<span data-ttu-id="d2eae-120">一个配置元素，该元素包含由 **activityDefinitionId** 属性标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="d2eae-120">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d2eae-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2eae-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="d2eae-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="d2eae-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="d2eae-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="d2eae-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

---
description: 了解详细信息： <faultPropagationQueries>
title: <faultPropagationQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 00ff90ae-ebe0-4c85-a93f-61557288d0a3
ms.openlocfilehash: 13bd19a3673846bfbd641cd2f8eeafc20b8186f8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719065"
---
# \<faultPropagationQueries>

<span data-ttu-id="fca22-102">表示一个查询集合，这些查询用于跟踪在某个活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="fca22-102">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="fca22-103">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="fca22-103">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="fca22-104">应使用此类查询来跟踪对在活动中出现的错误进行的处理。</span><span class="sxs-lookup"><span data-stu-id="fca22-104">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="fca22-105">跟踪参与者需要用此查询来订阅错误传播记录。</span><span class="sxs-lookup"><span data-stu-id="fca22-105">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="fca22-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="fca22-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<faultPropagationQueries>**
  
## <a name="syntax"></a><span data-ttu-id="fca22-107">语法</span><span class="sxs-lookup"><span data-stu-id="fca22-107">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <faultPropagationQueries>
        <faultPropagationQuery activityName="String"
                               faultHandlerActivityName="String" />
      </faultPropagationQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fca22-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="fca22-108">Attributes and Elements</span></span>  

 <span data-ttu-id="fca22-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fca22-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fca22-110">特性</span><span class="sxs-lookup"><span data-stu-id="fca22-110">Attributes</span></span>  

 <span data-ttu-id="fca22-111">无。</span><span class="sxs-lookup"><span data-stu-id="fca22-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fca22-112">子元素</span><span class="sxs-lookup"><span data-stu-id="fca22-112">Child Elements</span></span>  
  
|<span data-ttu-id="fca22-113">元素</span><span class="sxs-lookup"><span data-stu-id="fca22-113">Element</span></span>|<span data-ttu-id="fca22-114">说明</span><span class="sxs-lookup"><span data-stu-id="fca22-114">Description</span></span>|  
|-------------|-----------------|  
|[\<faultPropagationQuery>](faultpropagationquery.md)|<span data-ttu-id="fca22-115">一个查询，用于跟踪在活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="fca22-115">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="fca22-116">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="fca22-116">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fca22-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fca22-117">Parent Elements</span></span>  
  
|<span data-ttu-id="fca22-118">元素</span><span class="sxs-lookup"><span data-stu-id="fca22-118">Element</span></span>|<span data-ttu-id="fca22-119">说明</span><span class="sxs-lookup"><span data-stu-id="fca22-119">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](workflow.md)|<span data-ttu-id="fca22-120">一个配置元素，该元素包含由 **activityDefinitionId** 属性标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="fca22-120">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fca22-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="fca22-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="fca22-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="fca22-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="fca22-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="fca22-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

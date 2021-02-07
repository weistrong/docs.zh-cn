---
description: 了解有关 WCF 的详细信息： <faultPropagationQueries>
title: <faultPropagationQueries> WCF 的
ms.date: 03/30/2017
ms.assetid: d85f66a7-e7b0-4dbb-83cc-89fa06fc9161
ms.openlocfilehash: e3ed504b3aada87246fabe54c0b32ef5ad60b34b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684433"
---
# <a name="faultpropagationqueries-of-wcf"></a><span data-ttu-id="db7be-103">\<faultPropagationQueries> WCF 的</span><span class="sxs-lookup"><span data-stu-id="db7be-103">\<faultPropagationQueries> of WCF</span></span>

<span data-ttu-id="db7be-104">表示一个查询集合，这些查询用于跟踪在某个活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="db7be-104">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="db7be-105">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="db7be-105">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="db7be-106">应使用此类查询来跟踪对在活动中出现的错误进行的处理。</span><span class="sxs-lookup"><span data-stu-id="db7be-106">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="db7be-107">跟踪参与者需要用此查询来订阅错误传播记录。</span><span class="sxs-lookup"><span data-stu-id="db7be-107">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="db7be-108">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="db7be-108">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<faultPropagationQueries>**  
  
## <a name="syntax"></a><span data-ttu-id="db7be-109">语法</span><span class="sxs-lookup"><span data-stu-id="db7be-109">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String"/>
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="db7be-110">特性和元素</span><span class="sxs-lookup"><span data-stu-id="db7be-110">Attributes and elements</span></span>

<span data-ttu-id="db7be-111">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db7be-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db7be-112">特性</span><span class="sxs-lookup"><span data-stu-id="db7be-112">Attributes</span></span>

<span data-ttu-id="db7be-113">无。</span><span class="sxs-lookup"><span data-stu-id="db7be-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db7be-114">子元素</span><span class="sxs-lookup"><span data-stu-id="db7be-114">Child elements</span></span>

|<span data-ttu-id="db7be-115">元素</span><span class="sxs-lookup"><span data-stu-id="db7be-115">Element</span></span>|<span data-ttu-id="db7be-116">说明</span><span class="sxs-lookup"><span data-stu-id="db7be-116">Description</span></span>|  
|-------------|-----------------|  
|[\<faultPropagationQuery>](faultpropagationquery-of-wcf.md)|<span data-ttu-id="db7be-117">一个查询，用于跟踪在活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="db7be-117">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="db7be-118">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="db7be-118">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="db7be-119">父元素</span><span class="sxs-lookup"><span data-stu-id="db7be-119">Parent elements</span></span>  
  
|<span data-ttu-id="db7be-120">元素</span><span class="sxs-lookup"><span data-stu-id="db7be-120">Element</span></span>|<span data-ttu-id="db7be-121">说明</span><span class="sxs-lookup"><span data-stu-id="db7be-121">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](../windows-workflow-foundation/workflow.md)|<span data-ttu-id="db7be-122">一个配置元素，包含 `activityDefinitionId` 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="db7be-122">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="db7be-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="db7be-123">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="db7be-124">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="db7be-124">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="db7be-125">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="db7be-125">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

---
description: 了解有关 WCF 的详细信息： <customTrackingQueries>
title: <customTrackingQueries> WCF 的
ms.date: 03/30/2017
ms.assetid: 14cfe47e-9935-4120-84f1-8f38de8ca4c1
ms.openlocfilehash: ac1cdcc074201b97344b3727f6957e1b62c88dab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754467"
---
# <a name="customtrackingqueries-of-wcf"></a><span data-ttu-id="86999-103">\<customTrackingQueries> WCF 的</span><span class="sxs-lookup"><span data-stu-id="86999-103">\<customTrackingQueries> of WCF</span></span>

<span data-ttu-id="86999-104">表示一个查询集合，这些查询用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="86999-104">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="86999-105">跟踪参与者需要用此查询来订阅自定义跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="86999-105">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
<span data-ttu-id="86999-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="86999-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<customTrackingQueries>**  

## <a name="syntax"></a><span data-ttu-id="86999-107">语法</span><span class="sxs-lookup"><span data-stu-id="86999-107">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <customTrackingQueries>
          <customTrackingQuery activityName="String"
                               name="String"/>
        </customTrackingQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="86999-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="86999-108">Attributes and elements</span></span>

<span data-ttu-id="86999-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="86999-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="86999-110">特性</span><span class="sxs-lookup"><span data-stu-id="86999-110">Attributes</span></span>

<span data-ttu-id="86999-111">无。</span><span class="sxs-lookup"><span data-stu-id="86999-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86999-112">子元素</span><span class="sxs-lookup"><span data-stu-id="86999-112">Child elements</span></span>
  
|<span data-ttu-id="86999-113">元素</span><span class="sxs-lookup"><span data-stu-id="86999-113">Element</span></span>|<span data-ttu-id="86999-114">说明</span><span class="sxs-lookup"><span data-stu-id="86999-114">Description</span></span>|  
|-------------|-----------------|  
|[\<customTrackingQuery>](customtrackingquery-of-wcf.md)|<span data-ttu-id="86999-115">一个查询，用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="86999-115">A query that is used to track events that you define in your code activities.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="86999-116">父元素</span><span class="sxs-lookup"><span data-stu-id="86999-116">Parent elements</span></span>  
  
|<span data-ttu-id="86999-117">元素</span><span class="sxs-lookup"><span data-stu-id="86999-117">Element</span></span>|<span data-ttu-id="86999-118">说明</span><span class="sxs-lookup"><span data-stu-id="86999-118">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](../windows-workflow-foundation/workflow.md)|<span data-ttu-id="86999-119">一个配置元素，包含 `activityDefinitionId` 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="86999-119">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="86999-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="86999-120">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="86999-121">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="86999-121">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="86999-122">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="86999-122">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

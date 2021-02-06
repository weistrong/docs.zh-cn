---
description: 了解详细信息： <cancelRequestedQuery>
title: <cancelRequestedQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8da9b1c4-338a-4f23-9830-6d257772d340
ms.openlocfilehash: efd908fb52d2bc32bf05fce9099c7105abdc9b1a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652635"
---
# \<cancelRequestedQuery>

<span data-ttu-id="188b4-102">表示一个查询，该查询用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="188b4-102">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="188b4-103">跟踪参与者需要用此查询来订阅取消请求记录对象。</span><span class="sxs-lookup"><span data-stu-id="188b4-103">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="188b4-104">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="188b4-104">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<cancelRequestedQueries>**](cancelrequestedqueries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<cancelRequestedQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="188b4-105">语法</span><span class="sxs-lookup"><span data-stu-id="188b4-105">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String"
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="188b4-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="188b4-106">Attributes and Elements</span></span>  

 <span data-ttu-id="188b4-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="188b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="188b4-108">特性</span><span class="sxs-lookup"><span data-stu-id="188b4-108">Attributes</span></span>  
  
|<span data-ttu-id="188b4-109">属性</span><span class="sxs-lookup"><span data-stu-id="188b4-109">Attribute</span></span>|<span data-ttu-id="188b4-110">说明</span><span class="sxs-lookup"><span data-stu-id="188b4-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="188b4-111">activityName</span><span class="sxs-lookup"><span data-stu-id="188b4-111">activityName</span></span>|<span data-ttu-id="188b4-112">一个字符串，指定正在请求取消的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="188b4-112">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="188b4-113">childActivityName</span><span class="sxs-lookup"><span data-stu-id="188b4-113">childActivityName</span></span>|<span data-ttu-id="188b4-114">一个字符串，指定已请求将其取消的子活动的名称。</span><span class="sxs-lookup"><span data-stu-id="188b4-114">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="188b4-115">子元素</span><span class="sxs-lookup"><span data-stu-id="188b4-115">Child Elements</span></span>  

 <span data-ttu-id="188b4-116">无。</span><span class="sxs-lookup"><span data-stu-id="188b4-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="188b4-117">父元素</span><span class="sxs-lookup"><span data-stu-id="188b4-117">Parent Elements</span></span>  
  
|<span data-ttu-id="188b4-118">元素</span><span class="sxs-lookup"><span data-stu-id="188b4-118">Element</span></span>|<span data-ttu-id="188b4-119">说明</span><span class="sxs-lookup"><span data-stu-id="188b4-119">Description</span></span>|  
|-------------|-----------------|  
|[\<faultPropagationQuery>](faultpropagationquery.md)|<span data-ttu-id="188b4-120">表示一个配置元素列表，这些元素用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="188b4-120">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="188b4-121">跟踪参与者需要用此查询来订阅取消请求记录对象。</span><span class="sxs-lookup"><span data-stu-id="188b4-121">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="188b4-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="188b4-122">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="188b4-123">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="188b4-123">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="188b4-124">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="188b4-124">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

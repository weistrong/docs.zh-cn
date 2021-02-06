---
description: 了解有关 WCF 的详细信息： <cancelRequestedQuery>
title: <cancelRequestedQuery> WCF 的
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: e477e33650eb901cf2e9275570d8538196c52b6b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639167"
---
# <a name="cancelrequestedquery-of-wcf"></a><span data-ttu-id="ba55d-103">\<cancelRequestedQuery> WCF 的</span><span class="sxs-lookup"><span data-stu-id="ba55d-103">\<cancelRequestedQuery> of WCF</span></span>

<span data-ttu-id="ba55d-104">表示一个查询，该查询用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="ba55d-104">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="ba55d-105">跟踪参与者需要用此查询来订阅取消请求记录对象。</span><span class="sxs-lookup"><span data-stu-id="ba55d-105">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="ba55d-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="ba55d-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<cancelRequestedQueries>**](cancelrequestedqueries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<cancelRequestedQuery>**  

## <a name="syntax"></a><span data-ttu-id="ba55d-107">语法</span><span class="sxs-lookup"><span data-stu-id="ba55d-107">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestedQueries>
          <cancelRequestedQuery activityName="String"
                                childActivityName="String" />
        </cancelRequestedQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ba55d-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ba55d-108">Attributes and elements</span></span>

<span data-ttu-id="ba55d-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba55d-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="ba55d-110">特性</span><span class="sxs-lookup"><span data-stu-id="ba55d-110">Attributes</span></span>  
  
|<span data-ttu-id="ba55d-111">属性</span><span class="sxs-lookup"><span data-stu-id="ba55d-111">Attribute</span></span>|<span data-ttu-id="ba55d-112">说明</span><span class="sxs-lookup"><span data-stu-id="ba55d-112">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="ba55d-113">一个字符串，指定正在请求取消的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="ba55d-113">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="ba55d-114">一个字符串，指定已请求将其取消的子活动的名称。</span><span class="sxs-lookup"><span data-stu-id="ba55d-114">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ba55d-115">子元素</span><span class="sxs-lookup"><span data-stu-id="ba55d-115">Child elements</span></span>

<span data-ttu-id="ba55d-116">无。</span><span class="sxs-lookup"><span data-stu-id="ba55d-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba55d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="ba55d-117">Parent elements</span></span>
  
|<span data-ttu-id="ba55d-118">元素</span><span class="sxs-lookup"><span data-stu-id="ba55d-118">Element</span></span>|<span data-ttu-id="ba55d-119">说明</span><span class="sxs-lookup"><span data-stu-id="ba55d-119">Description</span></span>|  
|-------------|-----------------|  
|[\<cancelRequestedQueries>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="ba55d-120">表示一个查询集合，这些查询用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="ba55d-120">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ba55d-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba55d-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="ba55d-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="ba55d-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="ba55d-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="ba55d-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

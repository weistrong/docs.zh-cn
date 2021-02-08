---
description: 了解有关 WCF 的详细信息： <faultPropagationQuery>
title: <faultPropagationQuery> WCF 的
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: cd26bf76fec54371ef0455b93c98650bdab19068
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782060"
---
# <a name="faultpropagationquery-of-wcf"></a><span data-ttu-id="269d3-103">\<faultPropagationQuery> WCF 的</span><span class="sxs-lookup"><span data-stu-id="269d3-103">\<faultPropagationQuery> of WCF</span></span>

<span data-ttu-id="269d3-104">表示一个用于跟踪在活动中发生的错误的处理的查询。</span><span class="sxs-lookup"><span data-stu-id="269d3-104">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="269d3-105">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="269d3-105">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="269d3-106">应使用此类查询来跟踪对在活动中出现的错误进行的处理。</span><span class="sxs-lookup"><span data-stu-id="269d3-106">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="269d3-107">跟踪参与者需要用此查询来订阅错误传播记录。</span><span class="sxs-lookup"><span data-stu-id="269d3-107">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>

<span data-ttu-id="269d3-108">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="269d3-108">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<faultPropagationQueries>**](faultpropagationqueries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<faultPropagationQuery>**  

## <a name="syntax"></a><span data-ttu-id="269d3-109">语法</span><span class="sxs-lookup"><span data-stu-id="269d3-109">Syntax</span></span>

```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String" />
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="269d3-110">特性和元素</span><span class="sxs-lookup"><span data-stu-id="269d3-110">Attributes and elements</span></span>

<span data-ttu-id="269d3-111">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="269d3-111">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="269d3-112">特性</span><span class="sxs-lookup"><span data-stu-id="269d3-112">Attributes</span></span>

|<span data-ttu-id="269d3-113">属性</span><span class="sxs-lookup"><span data-stu-id="269d3-113">Attribute</span></span>|<span data-ttu-id="269d3-114">说明</span><span class="sxs-lookup"><span data-stu-id="269d3-114">Description</span></span>|
|---------------|-----------------|
|`faultSourceActivityName`|<span data-ttu-id="269d3-115">一个字符串，指定传播错误的错误处理程序活动的名称。</span><span class="sxs-lookup"><span data-stu-id="269d3-115">A string that specifies the name of the fault handler activity that propagated the fault.</span></span> <span data-ttu-id="269d3-116">默认值为 \* ，指示为所有活动返回错误传播记录。</span><span class="sxs-lookup"><span data-stu-id="269d3-116">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|
|`faultHandlerActivityName`|<span data-ttu-id="269d3-117">一个字符串，指定导致错误的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="269d3-117">A string that specifies the name of the activity that was the source of the fault.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="269d3-118">子元素</span><span class="sxs-lookup"><span data-stu-id="269d3-118">Child elements</span></span>

<span data-ttu-id="269d3-119">无。</span><span class="sxs-lookup"><span data-stu-id="269d3-119">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="269d3-120">父元素</span><span class="sxs-lookup"><span data-stu-id="269d3-120">Parent elements</span></span>

|<span data-ttu-id="269d3-121">元素</span><span class="sxs-lookup"><span data-stu-id="269d3-121">Element</span></span>|<span data-ttu-id="269d3-122">说明</span><span class="sxs-lookup"><span data-stu-id="269d3-122">Description</span></span>|
|-------------|-----------------|
|[\<faultPropagationQueries>](faultpropagationqueries-of-wcf.md)|<span data-ttu-id="269d3-123">表示一个配置元素列表，这些元素用于跟踪某个活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="269d3-123">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="269d3-124">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="269d3-124">This event occurs each time a FaultHandler processes a fault.</span></span>|

## <a name="see-also"></a><span data-ttu-id="269d3-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="269d3-125">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="269d3-126">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="269d3-126">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="269d3-127">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="269d3-127">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

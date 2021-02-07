---
description: 了解详细信息： <bookmarkResumptionQuery>
title: <bookmarkResumptionQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 226de75d-d25c-48d5-b069-4b7d80a6852b
ms.openlocfilehash: 4e6637b6edd54d9c1cf1a44986b362eb616bf14d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725241"
---
# \<bookmarkResumptionQuery>

<span data-ttu-id="712d1-102">表示一个查询，该查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="712d1-102">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="712d1-103">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="712d1-103">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="712d1-104">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="712d1-104">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<bookmarkResumptionQueries>**](bookmarkresumptionqueries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<bookmarkResumptionQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="712d1-105">语法</span><span class="sxs-lookup"><span data-stu-id="712d1-105">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <bookmarkResumptionQueries>
        <bookmarkResumptionQuery name="String" />
      </bookmarkResumptionQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="712d1-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="712d1-106">Attributes and Elements</span></span>  

 <span data-ttu-id="712d1-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="712d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="712d1-108">特性</span><span class="sxs-lookup"><span data-stu-id="712d1-108">Attributes</span></span>  
  
|<span data-ttu-id="712d1-109">属性</span><span class="sxs-lookup"><span data-stu-id="712d1-109">Attribute</span></span>|<span data-ttu-id="712d1-110">说明</span><span class="sxs-lookup"><span data-stu-id="712d1-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="712d1-111">name</span><span class="sxs-lookup"><span data-stu-id="712d1-111">name</span></span>|<span data-ttu-id="712d1-112">一个字符串，指定要订阅的书签记录的名称。</span><span class="sxs-lookup"><span data-stu-id="712d1-112">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="712d1-113">子元素</span><span class="sxs-lookup"><span data-stu-id="712d1-113">Child Elements</span></span>  

 <span data-ttu-id="712d1-114">无。</span><span class="sxs-lookup"><span data-stu-id="712d1-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="712d1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="712d1-115">Parent Elements</span></span>  
  
|<span data-ttu-id="712d1-116">元素</span><span class="sxs-lookup"><span data-stu-id="712d1-116">Element</span></span>|<span data-ttu-id="712d1-117">说明</span><span class="sxs-lookup"><span data-stu-id="712d1-117">Description</span></span>|  
|-------------|-----------------|  
|[\<bookmarkResumptionQueries>](bookmarkresumptionqueries.md)|<span data-ttu-id="712d1-118">表示一个查询集合，这些查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="712d1-118">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="712d1-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="712d1-119">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="712d1-120">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="712d1-120">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="712d1-121">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="712d1-121">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

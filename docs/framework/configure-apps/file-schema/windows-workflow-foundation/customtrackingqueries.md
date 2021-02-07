---
description: 了解详细信息： <customTrackingQueries>
title: <customTrackingQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4e9e732d-911d-45a3-a569-4b5e9cd1ffbe
ms.openlocfilehash: 3601950742eb002f43969bea4612e830d8365509
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719053"
---
# \<customTrackingQueries>

<span data-ttu-id="1fd37-102">表示一个查询集合，这些查询用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="1fd37-102">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="1fd37-103">跟踪参与者需要用此查询来订阅自定义跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="1fd37-103">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="1fd37-104">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="1fd37-104">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<customTrackingQueries>**  
  
## <a name="syntax"></a><span data-ttu-id="1fd37-105">语法</span><span class="sxs-lookup"><span data-stu-id="1fd37-105">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <customTrackingQueries>
        <customTrackingQuery activityName="String"
                             name="String" />
      </customTrackingQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1fd37-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1fd37-106">Attributes and Elements</span></span>  

 <span data-ttu-id="1fd37-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1fd37-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1fd37-108">特性</span><span class="sxs-lookup"><span data-stu-id="1fd37-108">Attributes</span></span>  

 <span data-ttu-id="1fd37-109">无。</span><span class="sxs-lookup"><span data-stu-id="1fd37-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1fd37-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1fd37-110">Child Elements</span></span>  
  
|<span data-ttu-id="1fd37-111">元素</span><span class="sxs-lookup"><span data-stu-id="1fd37-111">Element</span></span>|<span data-ttu-id="1fd37-112">说明</span><span class="sxs-lookup"><span data-stu-id="1fd37-112">Description</span></span>|  
|-------------|-----------------|  
|[\<customTrackingQuery>](customtrackingquery.md)|<span data-ttu-id="1fd37-113">一个查询，用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="1fd37-113">A query that is used to track events that you define in your code activities.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1fd37-114">父元素</span><span class="sxs-lookup"><span data-stu-id="1fd37-114">Parent Elements</span></span>  
  
|<span data-ttu-id="1fd37-115">元素</span><span class="sxs-lookup"><span data-stu-id="1fd37-115">Element</span></span>|<span data-ttu-id="1fd37-116">说明</span><span class="sxs-lookup"><span data-stu-id="1fd37-116">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](workflow.md)|<span data-ttu-id="1fd37-117">一个配置元素，该元素包含由 **activityDefinitionId** 属性标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="1fd37-117">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1fd37-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="1fd37-118">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="1fd37-119">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="1fd37-119">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1fd37-120">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="1fd37-120">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

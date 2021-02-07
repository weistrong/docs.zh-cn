---
description: 了解详细信息： <variable>
title: <variable>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 46cc8cbc-10ec-4625-8813-3f5cd6c6afde
ms.openlocfilehash: 187aa0b1ab0494a9bad759c504b804580a60553e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697993"
---
# \<variable>

<span data-ttu-id="88bec-102">表示与此活动查询关联的变量的集合。</span><span class="sxs-lookup"><span data-stu-id="88bec-102">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="88bec-103">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="88bec-103">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQueries>**](activitystatequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQuery>**](activitystatequery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<variables>**](variables.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<variable>**  
  
## <a name="syntax"></a><span data-ttu-id="88bec-104">语法</span><span class="sxs-lookup"><span data-stu-id="88bec-104">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <variables>
          <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="88bec-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="88bec-105">Attributes and Elements</span></span>  

 <span data-ttu-id="88bec-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="88bec-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="88bec-107">特性</span><span class="sxs-lookup"><span data-stu-id="88bec-107">Attributes</span></span>  
  
|<span data-ttu-id="88bec-108">属性</span><span class="sxs-lookup"><span data-stu-id="88bec-108">Attribute</span></span>|<span data-ttu-id="88bec-109">说明</span><span class="sxs-lookup"><span data-stu-id="88bec-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="88bec-110">name</span><span class="sxs-lookup"><span data-stu-id="88bec-110">name</span></span>|<span data-ttu-id="88bec-111">一个字符串，指定变量的名称。</span><span class="sxs-lookup"><span data-stu-id="88bec-111">A string that specifies the name of the variable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="88bec-112">子元素</span><span class="sxs-lookup"><span data-stu-id="88bec-112">Child Elements</span></span>  

 <span data-ttu-id="88bec-113">无。</span><span class="sxs-lookup"><span data-stu-id="88bec-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="88bec-114">父元素</span><span class="sxs-lookup"><span data-stu-id="88bec-114">Parent Elements</span></span>  
  
|<span data-ttu-id="88bec-115">元素</span><span class="sxs-lookup"><span data-stu-id="88bec-115">Element</span></span>|<span data-ttu-id="88bec-116">说明</span><span class="sxs-lookup"><span data-stu-id="88bec-116">Description</span></span>|  
|-------------|-----------------|  
|[\<variable>](variable.md)|<span data-ttu-id="88bec-117">与活动状态查询相关联的变量。</span><span class="sxs-lookup"><span data-stu-id="88bec-117">A variable associated with an activity state query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="88bec-118">备注</span><span class="sxs-lookup"><span data-stu-id="88bec-118">Remarks</span></span>  

 <span data-ttu-id="88bec-119">ActivityStateQuery 的一项独特功能是能够在跟踪工作流的执行时提取数据。</span><span class="sxs-lookup"><span data-stu-id="88bec-119">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="88bec-120">这在访问跟踪记录后续执行时可提供其他上下文。</span><span class="sxs-lookup"><span data-stu-id="88bec-120">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="88bec-121">您可以使用 [\<arguments>](arguments.md) 、 [\<states>](states.md) 和 [\<states>](states.md) 元素从工作流中的任何活动提取任何变量或参数。</span><span class="sxs-lookup"><span data-stu-id="88bec-121">You can use the [\<arguments>](arguments.md), [\<states>](states.md) and [\<states>](states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="88bec-122">下面的示例演示用于在发出活动的 `Closed` 跟踪记录时提取变量和自变量的活动状态查询。</span><span class="sxs-lookup"><span data-stu-id="88bec-122">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="88bec-123">变量和参数只能通过 ActivityStateRecord 提取，因此使用在跟踪配置文件内进行订阅 [\<activityStateQuery>](activitystatequery.md) 。</span><span class="sxs-lookup"><span data-stu-id="88bec-123">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](activitystatequery.md).</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a><span data-ttu-id="88bec-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="88bec-124">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="88bec-125">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="88bec-125">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="88bec-126">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="88bec-126">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)

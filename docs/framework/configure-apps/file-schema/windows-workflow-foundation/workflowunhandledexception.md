---
description: 了解详细信息： <workflowUnhandledException>
title: <workflowUnhandledException>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 57adeab5-f06a-44b2-916b-0e177cf0f4a6
ms.openlocfilehash: b9258c986ffa154e490f80bead1dc53d8f7ef44d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697772"
---
# \<workflowUnhandledException>

<span data-ttu-id="5e23c-102">一种服务行为，可用于指定工作流服务中发生未经处理的异常时所采取的操作。</span><span class="sxs-lookup"><span data-stu-id="5e23c-102">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<workflowUnhandledException>**  
  
## <a name="syntax"></a><span data-ttu-id="5e23c-103">语法</span><span class="sxs-lookup"><span data-stu-id="5e23c-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e23c-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5e23c-104">Attributes and Elements</span></span>  

 <span data-ttu-id="5e23c-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5e23c-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e23c-106">特性</span><span class="sxs-lookup"><span data-stu-id="5e23c-106">Attributes</span></span>  
  
|<span data-ttu-id="5e23c-107">属性</span><span class="sxs-lookup"><span data-stu-id="5e23c-107">Attribute</span></span>|<span data-ttu-id="5e23c-108">说明</span><span class="sxs-lookup"><span data-stu-id="5e23c-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e23c-109">操作</span><span class="sxs-lookup"><span data-stu-id="5e23c-109">action</span></span>|<span data-ttu-id="5e23c-110">一个字符串，指定发生未经处理的异常时所采取的操作。</span><span class="sxs-lookup"><span data-stu-id="5e23c-110">A string that specifies the action to take when an unhandled exception occurs.</span></span> <span data-ttu-id="5e23c-111">此特性的类型为 <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span><span class="sxs-lookup"><span data-stu-id="5e23c-111">This attribute is of type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e23c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5e23c-112">Child Elements</span></span>  

 <span data-ttu-id="5e23c-113">无。</span><span class="sxs-lookup"><span data-stu-id="5e23c-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5e23c-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5e23c-114">Parent Elements</span></span>  
  
|<span data-ttu-id="5e23c-115">元素</span><span class="sxs-lookup"><span data-stu-id="5e23c-115">Element</span></span>|<span data-ttu-id="5e23c-116">说明</span><span class="sxs-lookup"><span data-stu-id="5e23c-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e23c-117">\<serviceBehaviors> 的 \<behavior></span><span class="sxs-lookup"><span data-stu-id="5e23c-117">\<behavior> of \<serviceBehaviors></span></span>](behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="5e23c-118">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="5e23c-118">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5e23c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="5e23c-119">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowUnhandledExceptionElement>

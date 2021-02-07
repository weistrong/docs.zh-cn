---
description: 了解详细信息： <workflowInstanceManagement>
title: <workflowInstanceManagement>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 63ac89ba-c844-4ae2-96ae-cd752a90a109
ms.openlocfilehash: 528c0c923be93d9581b8e3bfccc382eab11c5da1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697915"
---
# \<workflowInstanceManagement>

<span data-ttu-id="d3ca6-102">一种服务行为，可用于指定控制工作流实例如何运行的设置，包括持久性、未经处理的异常行为和空闲行为。</span><span class="sxs-lookup"><span data-stu-id="d3ca6-102">A service behavior that enables you to specify settings that control how workflow instances are run, including persistence, unhandled Exception behavior and idle behavior.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<workflowInstanceManagement>**  
  
## <a name="syntax"></a><span data-ttu-id="d3ca6-103">语法</span><span class="sxs-lookup"><span data-stu-id="d3ca6-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowInstanceManagement authorizedWindowsGroup="" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d3ca6-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d3ca6-104">Attributes and Elements</span></span>  

 <span data-ttu-id="d3ca6-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d3ca6-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d3ca6-106">特性</span><span class="sxs-lookup"><span data-stu-id="d3ca6-106">Attributes</span></span>  
  
|<span data-ttu-id="d3ca6-107">属性</span><span class="sxs-lookup"><span data-stu-id="d3ca6-107">Attribute</span></span>|<span data-ttu-id="d3ca6-108">说明</span><span class="sxs-lookup"><span data-stu-id="d3ca6-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d3ca6-109">authorizedWindowsGroup</span><span class="sxs-lookup"><span data-stu-id="d3ca6-109">authorizedWindowsGroup</span></span>||  
  
### <a name="child-elements"></a><span data-ttu-id="d3ca6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d3ca6-110">Child Elements</span></span>  

 <span data-ttu-id="d3ca6-111">无。</span><span class="sxs-lookup"><span data-stu-id="d3ca6-111">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d3ca6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d3ca6-112">Parent Elements</span></span>  
  
|<span data-ttu-id="d3ca6-113">元素</span><span class="sxs-lookup"><span data-stu-id="d3ca6-113">Element</span></span>|<span data-ttu-id="d3ca6-114">说明</span><span class="sxs-lookup"><span data-stu-id="d3ca6-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d3ca6-115">\<serviceBehaviors> 的 \<behavior></span><span class="sxs-lookup"><span data-stu-id="d3ca6-115">\<behavior> of \<serviceBehaviors></span></span>](behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="d3ca6-116">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="d3ca6-116">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d3ca6-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3ca6-117">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.WorkflowInstanceManagementBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowInstanceManagementElement>

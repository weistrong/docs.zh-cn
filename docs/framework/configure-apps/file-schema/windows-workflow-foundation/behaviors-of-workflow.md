---
description: 了解有关 <behaviors> 工作流的详细信息
title: <behaviors> 的工作流
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 3c6017b6-0c4f-4192-bd67-9515f5d1ec82
ms.openlocfilehash: 5154a389aded34065cc7bdb11d1c73d71ca9f9f5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698188"
---
# <a name="behaviors-of-workflow"></a><span data-ttu-id="da4ea-103">\<behaviors> 的工作流</span><span class="sxs-lookup"><span data-stu-id="da4ea-103">\<behaviors> of workflow</span></span>

<span data-ttu-id="da4ea-104">此元素包含 **serviceBehaviors** 集合。</span><span class="sxs-lookup"><span data-stu-id="da4ea-104">This element contains the **serviceBehaviors** collection.</span></span>  <span data-ttu-id="da4ea-105">集合中的每个元素定义工作流服务所使用的行为元素。</span><span class="sxs-lookup"><span data-stu-id="da4ea-105">Each element in the collection defines behavior elements consumed by workflow services.</span></span> <span data-ttu-id="da4ea-106">每个行为元素都由其唯一 **名称** 属性标识。</span><span class="sxs-lookup"><span data-stu-id="da4ea-106">Each behavior element is identified by its unique **name** attribute.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<behaviors>**  
  
## <a name="syntax"></a><span data-ttu-id="da4ea-107">语法</span><span class="sxs-lookup"><span data-stu-id="da4ea-107">Syntax</span></span>  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
  </serviceBehaviors>  
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="da4ea-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="da4ea-108">Attributes and Elements</span></span>  

 <span data-ttu-id="da4ea-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da4ea-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="da4ea-110">特性</span><span class="sxs-lookup"><span data-stu-id="da4ea-110">Attributes</span></span>  

 <span data-ttu-id="da4ea-111">无</span><span class="sxs-lookup"><span data-stu-id="da4ea-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="da4ea-112">子元素</span><span class="sxs-lookup"><span data-stu-id="da4ea-112">Child Elements</span></span>  
  
|<span data-ttu-id="da4ea-113">元素</span><span class="sxs-lookup"><span data-stu-id="da4ea-113">Element</span></span>|<span data-ttu-id="da4ea-114">说明</span><span class="sxs-lookup"><span data-stu-id="da4ea-114">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceBehaviors>](servicebehaviors-of-workflow.md)|<span data-ttu-id="da4ea-115">此配置节表示为特定工作流服务定义的所有行为。</span><span class="sxs-lookup"><span data-stu-id="da4ea-115">This configuration section represents all the behaviors defined for a specific workflow service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="da4ea-116">父元素</span><span class="sxs-lookup"><span data-stu-id="da4ea-116">Parent Elements</span></span>  
  
|<span data-ttu-id="da4ea-117">元素</span><span class="sxs-lookup"><span data-stu-id="da4ea-117">Element</span></span>|<span data-ttu-id="da4ea-118">说明</span><span class="sxs-lookup"><span data-stu-id="da4ea-118">Description</span></span>|  
|-------------|-----------------|  
|[\<system.serviceModel>](../wcf/system-servicemodel.md)|<span data-ttu-id="da4ea-119">所有工作流配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="da4ea-119">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="da4ea-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="da4ea-120">See also</span></span>

- <xref:System.ServiceModel.Configuration.BehaviorsSection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>
- [<span data-ttu-id="da4ea-121">使用行为配置和扩展运行时</span><span class="sxs-lookup"><span data-stu-id="da4ea-121">Configuring and Extending the Runtime with Behaviors</span></span>](../../../wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)

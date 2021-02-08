---
description: 了解详细信息： <endToEndTracing>
title: <endToEndTracing>
ms.date: 03/30/2017
ms.assetid: 5034f5de-bb60-4157-9ad4-58aaade094e0
ms.openlocfilehash: 2ac4a7563d7d7881cdb503e843d34f84fd9c95a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782112"
---
# \<endToEndTracing>

<span data-ttu-id="e39fb-102">一个配置元素，用于启用和禁用服务应用程序运行过程中端对端跟踪的不同方面。</span><span class="sxs-lookup"><span data-stu-id="e39fb-102">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<diagnostics>**](diagnostics.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<endToEndTracing>**  
  
## <a name="syntax"></a><span data-ttu-id="e39fb-103">语法</span><span class="sxs-lookup"><span data-stu-id="e39fb-103">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics>
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e39fb-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="e39fb-104">Attributes and Elements</span></span>  

 <span data-ttu-id="e39fb-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e39fb-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e39fb-106">特性</span><span class="sxs-lookup"><span data-stu-id="e39fb-106">Attributes</span></span>  
  
|<span data-ttu-id="e39fb-107">属性</span><span class="sxs-lookup"><span data-stu-id="e39fb-107">Attribute</span></span>|<span data-ttu-id="e39fb-108">说明</span><span class="sxs-lookup"><span data-stu-id="e39fb-108">Description</span></span>|  
|---------------|-----------------|  
|`activityTracing`|<span data-ttu-id="e39fb-109">一个布尔值，指定是否启用活动跟踪。</span><span class="sxs-lookup"><span data-stu-id="e39fb-109">A Boolean value that specifies whether activity tracing is enabled.</span></span>|  
|`messageFlowTracing`|<span data-ttu-id="e39fb-110">一个布尔值，指定是否启用消息流跟踪。</span><span class="sxs-lookup"><span data-stu-id="e39fb-110">A Boolean value that specifies whether message flow tracing in enabled.</span></span>|  
|`propagateActivity`|<span data-ttu-id="e39fb-111">一个布尔值，指定是否将传播特性设置为 true。</span><span class="sxs-lookup"><span data-stu-id="e39fb-111">A Boolean value that specifies whether the propagate attribute is set to true.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e39fb-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e39fb-112">Child Elements</span></span>  

 <span data-ttu-id="e39fb-113">无。</span><span class="sxs-lookup"><span data-stu-id="e39fb-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e39fb-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e39fb-114">Parent Elements</span></span>  
  
|<span data-ttu-id="e39fb-115">元素</span><span class="sxs-lookup"><span data-stu-id="e39fb-115">Element</span></span>|<span data-ttu-id="e39fb-116">说明</span><span class="sxs-lookup"><span data-stu-id="e39fb-116">Description</span></span>|  
|-------------|-----------------|  
|[\<diagnostics>](diagnostics.md)|<span data-ttu-id="e39fb-117">定义管理员运行时检查和控制的 WCF 设置。</span><span class="sxs-lookup"><span data-stu-id="e39fb-117">Defines WCF settings for runtime inspection and control for the administrator.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e39fb-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="e39fb-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.DiagnosticSection>
- <xref:System.ServiceModel.Diagnostics>
- <xref:System.ServiceModel.Configuration.DiagnosticSection.EndToEndTracing%2A>
- <xref:System.ServiceModel.Configuration.EndToEndTracingElement>
- [<span data-ttu-id="e39fb-119">端对端跟踪</span><span class="sxs-lookup"><span data-stu-id="e39fb-119">End-to-End Tracing</span></span>](../../../wcf/diagnostics/tracing/end-to-end-tracing.md)

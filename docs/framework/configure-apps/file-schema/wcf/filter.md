---
description: 了解详细信息： <filter>
title: <filter>
ms.date: 03/30/2017
ms.assetid: 3266700b-904b-44e4-93a7-e06a1a445100
ms.openlocfilehash: 993d2265ac3a714475e8cbe9e8a2c3f93c46bde2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664673"
---
# \<filter>

<span data-ttu-id="06c40-102">定义一个路由筛选器，该筛选器确定 <xref:System.ServiceModel.Dispatcher.MessageFilter> 要在评估传入消息时使用的 Windows Communication Foundation (WCF) ，以及筛选器所需的任何支持数据或参数。</span><span class="sxs-lookup"><span data-stu-id="06c40-102">Defines a routing filter, which determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well any supporting data or parameters required by the filter.</span></span>

[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<filters>**](filters-of-routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<filter>**  
  
## <a name="syntax"></a><span data-ttu-id="06c40-103">语法</span><span class="sxs-lookup"><span data-stu-id="06c40-103">Syntax</span></span>  
  
```xml  
<routing>
  <filters>
    <filter customType="String"
            filterData="String"
            filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
            name="String" />
  </filters>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="06c40-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="06c40-104">Attributes and elements</span></span>

<span data-ttu-id="06c40-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06c40-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="06c40-106">特性</span><span class="sxs-lookup"><span data-stu-id="06c40-106">Attributes</span></span>

| <span data-ttu-id="06c40-107">属性</span><span class="sxs-lookup"><span data-stu-id="06c40-107">Attribute</span></span>  | <span data-ttu-id="06c40-108">说明</span><span class="sxs-lookup"><span data-stu-id="06c40-108">Description</span></span> |
| ---------- | ----------- |
| <span data-ttu-id="06c40-109">customType</span><span class="sxs-lookup"><span data-stu-id="06c40-109">customType</span></span> | <span data-ttu-id="06c40-110">一个字符串，包含要用作筛选器的自定义类型的完全限定类型名称。</span><span class="sxs-lookup"><span data-stu-id="06c40-110">A string containing the fully qualified type name of the custom type to be used as a filter.</span></span> <span data-ttu-id="06c40-111">如果 `filterType` 设置为 `custom` ，则此特性包含要创建的类的完全限定类型名称。</span><span class="sxs-lookup"><span data-stu-id="06c40-111">If `filterType` is set to `custom`, this attribute contains the fully qualified type name of the class to create.</span></span>  <span data-ttu-id="06c40-112">`filterData` 还可以包含在计算自定义类型筛选器的过程中要使用的值。</span><span class="sxs-lookup"><span data-stu-id="06c40-112">`filterData` may also contain values to be used during evaluation of the custom type filter.</span></span> |
| <span data-ttu-id="06c40-113">filterData</span><span class="sxs-lookup"><span data-stu-id="06c40-113">filterData</span></span> | <span data-ttu-id="06c40-114">一个包含筛选器数据的字符串。</span><span class="sxs-lookup"><span data-stu-id="06c40-114">A string containing the filter data.</span></span> <span data-ttu-id="06c40-115">有关如何指定此特性的更多信息，请参见 <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>。</span><span class="sxs-lookup"><span data-stu-id="06c40-115">For more information on how to specify this attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="06c40-116">filterType</span><span class="sxs-lookup"><span data-stu-id="06c40-116">filterType</span></span> | <span data-ttu-id="06c40-117">一个包含筛选器类型的字符串。</span><span class="sxs-lookup"><span data-stu-id="06c40-117">A string containing the filter type.</span></span> <span data-ttu-id="06c40-118">此特性的类型为 <xref:System.ServiceModel.Routing.Configuration.FilterType>。</span><span class="sxs-lookup"><span data-stu-id="06c40-118">This attribute is of <xref:System.ServiceModel.Routing.Configuration.FilterType> type.</span></span>  <span data-ttu-id="06c40-119">有关如何使用此 `filterData` 特性的更多信息，请参见 <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>。</span><span class="sxs-lookup"><span data-stu-id="06c40-119">For more information on how this works with the `filterData` attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="06c40-120">name</span><span class="sxs-lookup"><span data-stu-id="06c40-120">name</span></span>       | <span data-ttu-id="06c40-121">一个字符串，包含此筛选器元素的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="06c40-121">A string containing the unique name of this filter element.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="06c40-122">子元素</span><span class="sxs-lookup"><span data-stu-id="06c40-122">Child elements</span></span>

<span data-ttu-id="06c40-123">无。</span><span class="sxs-lookup"><span data-stu-id="06c40-123">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="06c40-124">父元素</span><span class="sxs-lookup"><span data-stu-id="06c40-124">Parent elements</span></span>

| <span data-ttu-id="06c40-125">元素</span><span class="sxs-lookup"><span data-stu-id="06c40-125">Element</span></span> | <span data-ttu-id="06c40-126">说明</span><span class="sxs-lookup"><span data-stu-id="06c40-126">Description</span></span> |
| ------- | ----------- |
| [\<routing>](routing.md) | <span data-ttu-id="06c40-127">用于定义一组路由筛选器的配置节，这些筛选器确定 <xref:System.ServiceModel.Dispatcher.MessageFilter> 计算传入消息时要使用 (WCF) Windows Communication Foundation 的类型。</span><span class="sxs-lookup"><span data-stu-id="06c40-127">A configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span> |

## <a name="see-also"></a><span data-ttu-id="06c40-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="06c40-128">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterType?displayProperty=nameWithType>

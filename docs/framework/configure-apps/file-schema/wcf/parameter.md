---
description: 了解详细信息： <parameter>
title: <parameter>
ms.date: 03/30/2017
ms.assetid: 0fb41e2d-64f7-44ab-993e-05892eac6d82
ms.openlocfilehash: fb04cfb5bf451cdb99c23ae41ea8fafeb13f0d11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683809"
---
# \<parameter>

<span data-ttu-id="28faa-102">指定当声明类型是泛型类型时的泛型参数。</span><span class="sxs-lookup"><span data-stu-id="28faa-102">Specifies the generic parameter when a declared type is a generic type.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.serialization>**](system-runtime-serialization.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<dataContractSerializer>**](datacontractserializer.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<declaredTypes>**](declaredtypes.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add-of-declaredtypes-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<knownType>**](knowntype.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<parameter>**  
  
## <a name="syntax"></a><span data-ttu-id="28faa-103">语法</span><span class="sxs-lookup"><span data-stu-id="28faa-103">Syntax</span></span>  
  
```xml  
<parameter index="Integer"
           type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="28faa-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="28faa-104">Attributes and Elements</span></span>  

 <span data-ttu-id="28faa-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="28faa-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="28faa-106">特性</span><span class="sxs-lookup"><span data-stu-id="28faa-106">Attributes</span></span>  
  
|<span data-ttu-id="28faa-107">属性</span><span class="sxs-lookup"><span data-stu-id="28faa-107">Attribute</span></span>|<span data-ttu-id="28faa-108">说明</span><span class="sxs-lookup"><span data-stu-id="28faa-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="28faa-109">索引</span><span class="sxs-lookup"><span data-stu-id="28faa-109">index</span></span>|<span data-ttu-id="28faa-110">当声明类型是泛型类型时，指定将返回已知类型的泛型参数。</span><span class="sxs-lookup"><span data-stu-id="28faa-110">When the declared type is a generic type, specifies the generic parameter that will return the known type.</span></span>|  
|<span data-ttu-id="28faa-111">type</span><span class="sxs-lookup"><span data-stu-id="28faa-111">type</span></span>|<span data-ttu-id="28faa-112">一个字符串，描述用于序列化和反序列化的已知类型。</span><span class="sxs-lookup"><span data-stu-id="28faa-112">A string that describes the known type used for serialization and deserialization.</span></span>|  
  
## <a name="index-attribute"></a><span data-ttu-id="28faa-113">index 特性</span><span class="sxs-lookup"><span data-stu-id="28faa-113">index Attribute</span></span>  
  
|<span data-ttu-id="28faa-114">值</span><span class="sxs-lookup"><span data-stu-id="28faa-114">Value</span></span>|<span data-ttu-id="28faa-115">说明</span><span class="sxs-lookup"><span data-stu-id="28faa-115">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="28faa-116">"0"</span><span class="sxs-lookup"><span data-stu-id="28faa-116">"0"</span></span>|<span data-ttu-id="28faa-117">泛型类型中的第一个参数。</span><span class="sxs-lookup"><span data-stu-id="28faa-117">The first parameter in the generic type.</span></span> <span data-ttu-id="28faa-118">例如，一个 <xref:System.Collections.Generic.List%601> 仅有一个参数。</span><span class="sxs-lookup"><span data-stu-id="28faa-118">For example, a <xref:System.Collections.Generic.List%601> has only one parameter.</span></span> <span data-ttu-id="28faa-119">如果此参数用作声明类型，则将 index 特性设置为“0”。</span><span class="sxs-lookup"><span data-stu-id="28faa-119">If it is used as the declared type, the index would be set to "0".</span></span>|  
|<span data-ttu-id="28faa-120">"1"</span><span class="sxs-lookup"><span data-stu-id="28faa-120">"1"</span></span>|<span data-ttu-id="28faa-121">泛型类型中的第二个参数。</span><span class="sxs-lookup"><span data-stu-id="28faa-121">The second parameter in a generic type.</span></span> <span data-ttu-id="28faa-122">例如，一个 <xref:System.Collections.Generic.Dictionary%602> 有两个参数。</span><span class="sxs-lookup"><span data-stu-id="28faa-122">For example, a <xref:System.Collections.Generic.Dictionary%602> has two parameters.</span></span> <span data-ttu-id="28faa-123">如果通过第二个参数返回已知类型，则将 index 特性设置为“1”。</span><span class="sxs-lookup"><span data-stu-id="28faa-123">If the known type is returned by the second parameter, set the index attribute to "1".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="28faa-124">子元素</span><span class="sxs-lookup"><span data-stu-id="28faa-124">Child Elements</span></span>  

 <span data-ttu-id="28faa-125">无。</span><span class="sxs-lookup"><span data-stu-id="28faa-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="28faa-126">父元素</span><span class="sxs-lookup"><span data-stu-id="28faa-126">Parent Elements</span></span>  
  
|<span data-ttu-id="28faa-127">元素</span><span class="sxs-lookup"><span data-stu-id="28faa-127">Element</span></span>|<span data-ttu-id="28faa-128">说明</span><span class="sxs-lookup"><span data-stu-id="28faa-128">Description</span></span>|  
|-------------|-----------------|  
|[\<knownType>](knowntype.md)|<span data-ttu-id="28faa-129">指定一个可由声明类型的字段或属性返回的已知类型。</span><span class="sxs-lookup"><span data-stu-id="28faa-129">Specifies a known type that can be returned by a field or property of the declared type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28faa-130">备注</span><span class="sxs-lookup"><span data-stu-id="28faa-130">Remarks</span></span>  

 <span data-ttu-id="28faa-131">有关已知类型的详细信息，请参阅 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md) 和 <xref:System.Runtime.Serialization.DataContractSerializer> 。</span><span class="sxs-lookup"><span data-stu-id="28faa-131">For more information about known types, see [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="28faa-132">[\<dataContractSerializer>](datacontractserializer-element.md)有关使用此元素的示例，请参见。</span><span class="sxs-lookup"><span data-stu-id="28faa-132">See the [\<dataContractSerializer>](datacontractserializer-element.md) for an example of using this element.</span></span>  
  
 <span data-ttu-id="28faa-133">此配置元素不能同时具有两个属性。</span><span class="sxs-lookup"><span data-stu-id="28faa-133">This configuration element cannot have both attributes at the same time.</span></span> <span data-ttu-id="28faa-134">如果设置两个属性，则发生 <xref:System.Configuration.ConfigurationErrorsException>。</span><span class="sxs-lookup"><span data-stu-id="28faa-134">If both attributes are set, a <xref:System.Configuration.ConfigurationErrorsException> occurs.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28faa-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="28faa-135">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="28faa-136">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="28faa-136">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)
- [\<dataContractSerializer>](datacontractserializer-element.md)
- [\<add>](add-of-declaredtypes-element.md)

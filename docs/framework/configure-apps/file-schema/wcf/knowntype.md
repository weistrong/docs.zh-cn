---
description: 了解详细信息： <knownType>
title: <knownType>
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: 205f799c81263be3dd08aae9efefb975b06a0cc7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725501"
---
# \<knownType>

<span data-ttu-id="d74fc-102">指定在反序列化过程中将由 <xref:System.Runtime.Serialization.DataContractSerializer> 使用的类型。</span><span class="sxs-lookup"><span data-stu-id="d74fc-102">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="d74fc-103">该元素指定由某个“声明的类型”的字段或属性返回到“已知类型”。</span><span class="sxs-lookup"><span data-stu-id="d74fc-103">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="d74fc-104">有关详细信息，请参阅 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d74fc-104">For more information, see [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.serialization>**](system-runtime-serialization.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<dataContractSerializer>**](datacontractserializer.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<declaredTypes>**](declaredtypes.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add-of-declaredtypes-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<knownType>**  
  
## <a name="syntax"></a><span data-ttu-id="d74fc-105">语法</span><span class="sxs-lookup"><span data-stu-id="d74fc-105">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="d74fc-106">类型</span><span class="sxs-lookup"><span data-stu-id="d74fc-106">Type</span></span>  

 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d74fc-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d74fc-107">Attributes and Elements</span></span>  

 <span data-ttu-id="d74fc-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d74fc-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d74fc-109">特性</span><span class="sxs-lookup"><span data-stu-id="d74fc-109">Attributes</span></span>  
  
|<span data-ttu-id="d74fc-110">属性</span><span class="sxs-lookup"><span data-stu-id="d74fc-110">Attribute</span></span>|<span data-ttu-id="d74fc-111">说明</span><span class="sxs-lookup"><span data-stu-id="d74fc-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d74fc-112">type</span><span class="sxs-lookup"><span data-stu-id="d74fc-112">type</span></span>|<span data-ttu-id="d74fc-113">指定类型（包括命名空间）、程序集名称、版本、区域性和公钥标记。</span><span class="sxs-lookup"><span data-stu-id="d74fc-113">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d74fc-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d74fc-114">Child Elements</span></span>  
  
|<span data-ttu-id="d74fc-115">元素</span><span class="sxs-lookup"><span data-stu-id="d74fc-115">Element</span></span>|<span data-ttu-id="d74fc-116">说明</span><span class="sxs-lookup"><span data-stu-id="d74fc-116">Description</span></span>|  
|-------------|-----------------|  
|[\<parameter>](parameter.md)|<span data-ttu-id="d74fc-117">当声明类型为泛型类型时指定参数索引。</span><span class="sxs-lookup"><span data-stu-id="d74fc-117">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d74fc-118">父元素</span><span class="sxs-lookup"><span data-stu-id="d74fc-118">Parent Elements</span></span>  
  
|<span data-ttu-id="d74fc-119">元素</span><span class="sxs-lookup"><span data-stu-id="d74fc-119">Element</span></span>|<span data-ttu-id="d74fc-120">说明</span><span class="sxs-lookup"><span data-stu-id="d74fc-120">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-of-declaredtypes-element.md)|<span data-ttu-id="d74fc-121">向声明类型的集合中添加一个声明类型。</span><span class="sxs-lookup"><span data-stu-id="d74fc-121">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d74fc-122">备注</span><span class="sxs-lookup"><span data-stu-id="d74fc-122">Remarks</span></span>  

 <span data-ttu-id="d74fc-123">有关已知类型的详细信息，请参阅 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md) 和 <xref:System.Runtime.Serialization.DataContractSerializer> 。</span><span class="sxs-lookup"><span data-stu-id="d74fc-123">For more information about known types, see [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="d74fc-124">[\<dataContractSerializer>](datacontractserializer-element.md)有关使用此元素的示例，请参见。</span><span class="sxs-lookup"><span data-stu-id="d74fc-124">See the [\<dataContractSerializer>](datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d74fc-125">示例</span><span class="sxs-lookup"><span data-stu-id="d74fc-125">Example</span></span>  
  
```xml  
<add type="MyCompany.Library.Shape,
           MyAssembly, Version=2.0.0.0, Culture=neutral,
           PublicKeyToken=XXXXXX, processorArchitecture=MSIL">
  <knownType type="MyCompany.Library.Circle,
                   MyAssembly, Version=2.0.0.0, Culture=neutral,
                   PublicKeyToken=XXXXXX,
                   processorArchitecture=MSIL"/>
</add>
```  
  
## <a name="see-also"></a><span data-ttu-id="d74fc-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="d74fc-126">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="d74fc-127">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="d74fc-127">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)
- [\<dataContractSerializer>](datacontractserializer-element.md)
- [\<add>](add-of-declaredtypes-element.md)

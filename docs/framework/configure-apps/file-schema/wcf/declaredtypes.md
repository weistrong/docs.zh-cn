---
description: 了解详细信息： <declaredTypes>
title: <declaredTypes>
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- declaredTypes element
- DataContractSerializer
- KnownTypes
- <declaredTypes> element
ms.assetid: f35184e4-9d9e-4d37-8fb4-d5b58220eb3e
ms.openlocfilehash: e5f60209dd556edc7cf47b01b1a58c1f17d74eac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803927"
---
# \<declaredTypes>

<span data-ttu-id="0cbeb-102">包含在进行反序列化时 <xref:System.Runtime.Serialization.DataContractSerializer> 使用的已知类型。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-102">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span>  
  
 <span data-ttu-id="0cbeb-103">有关数据协定和已知类型的详细信息，请参阅 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md)。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-103">For more information about data contracts and known types, see [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.serialization>**](system-runtime-serialization.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<dataContractSerializer>**](datacontractserializer.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<declaredTypes>**  
  
## <a name="syntax"></a><span data-ttu-id="0cbeb-104">语法</span><span class="sxs-lookup"><span data-stu-id="0cbeb-104">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer>
      <declaredTypes>
        <add type="String ">
          <knownType type="String">
            <parameter index="Integer"/>
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0cbeb-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0cbeb-105">Attributes and Elements</span></span>  

 <span data-ttu-id="0cbeb-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0cbeb-107">特性</span><span class="sxs-lookup"><span data-stu-id="0cbeb-107">Attributes</span></span>  

 <span data-ttu-id="0cbeb-108">无。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0cbeb-109">子元素</span><span class="sxs-lookup"><span data-stu-id="0cbeb-109">Child Elements</span></span>  
  
|<span data-ttu-id="0cbeb-110">元素</span><span class="sxs-lookup"><span data-stu-id="0cbeb-110">Element</span></span>|<span data-ttu-id="0cbeb-111">说明</span><span class="sxs-lookup"><span data-stu-id="0cbeb-111">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-of-declaredtypes-element.md)|<span data-ttu-id="0cbeb-112">添加需要已知类型的类型。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-112">Adds types that require known types.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0cbeb-113">父元素</span><span class="sxs-lookup"><span data-stu-id="0cbeb-113">Parent Elements</span></span>  
  
|<span data-ttu-id="0cbeb-114">元素</span><span class="sxs-lookup"><span data-stu-id="0cbeb-114">Element</span></span>|<span data-ttu-id="0cbeb-115">说明</span><span class="sxs-lookup"><span data-stu-id="0cbeb-115">Description</span></span>|  
|-------------|-----------------|  
|[\<dataContractSerializer>](datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="0cbeb-116">包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的配置数据。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-116">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0cbeb-117">备注</span><span class="sxs-lookup"><span data-stu-id="0cbeb-117">Remarks</span></span>  

 <span data-ttu-id="0cbeb-118">有关已知类型的详细信息，请参阅 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md) 和 <xref:System.Runtime.Serialization.DataContractSerializer> 。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-118">For more information about known types, see [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0cbeb-119">示例</span><span class="sxs-lookup"><span data-stu-id="0cbeb-119">Example</span></span>  

 <span data-ttu-id="0cbeb-120">以下 XML 代码显示了已声明的类型和添加到元素的已知类型 `DataContractSerializer` 。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-120">The following XML code shows declared types and known types added to a `DataContractSerializer` element.</span></span> <span data-ttu-id="0cbeb-121">此示例演示要添加的三个类型。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-121">The example shows three types being added.</span></span> <span data-ttu-id="0cbeb-122">第一个类型是名为“Orders”的自定义类型，它使用一个名为“Item”的已知类型。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-122">The first is a custom type named "Orders" that uses a known type named "Item".</span></span> <span data-ttu-id="0cbeb-123">第二个声明类型 <xref:System.Collections.Generic.List%601>，它使用 `Item` 作为已知类型。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-123">The second declared type is a <xref:System.Collections.Generic.List%601> that uses `Item` as a known type.</span></span> <span data-ttu-id="0cbeb-124">最后，第三个声明类型是 <xref:System.Collections.Generic.Dictionary%602>。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-124">Finally the third declared type is a <xref:System.Collections.Generic.Dictionary%602>.</span></span> <span data-ttu-id="0cbeb-125"><xref:System.Collections.Generic.Dictionary%602> 类类型是泛型类型，并带有两个类型参数。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-125">The <xref:System.Collections.Generic.Dictionary%602> class type is a generic type, with two type parameters.</span></span> <span data-ttu-id="0cbeb-126">第一个参数表示键，第二个参数表示值。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-126">The first represents the key and the second represents the value.</span></span> <span data-ttu-id="0cbeb-127">下面的示例将第二个类型的 <xref:System.Collections.Generic.List%601>（值）添加到已知类型的列表中。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-127">The following example adds a <xref:System.Collections.Generic.List%601> of the second type (the value) to the list of known types.</span></span> <span data-ttu-id="0cbeb-128">必须使用 `index` 属性来指定在已知类型中使用的类型参数。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-128">You must use the `index` attribute to specify which type parameter to use in the known type.</span></span> <span data-ttu-id="0cbeb-129">在此例中，通过将 index 属性设置为“1”（基于零的集合）来指示值类型。</span><span class="sxs-lookup"><span data-stu-id="0cbeb-129">In this case, the value type is indicated by the index attribute set to "1" (the collection is zero-based).</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer>
      <declaredTypes>
        <add type="Examples.Types.Orders, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
          <knownType type="Examples.Types.Item, SerializationTypes, Version=2.0.0.0, Culture=neutral, PublicKey=null" />
        </add>
        <add type="System.Collections.Generic.List`1, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
          <knownType type="Examples.Types.Item, SerializationTypes, Version=2.0.0.0, Culture=neutral, PublicKey=null" />
        </add>
        <add type="System.Collections.Generic.Dictionary`2, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
          <knownType type="System.Collections.Generic.List`1, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
            <parameter index="1"/>
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="0cbeb-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="0cbeb-130">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [\<dataContractSerializer>](datacontractserializer-element.md)
- [<span data-ttu-id="0cbeb-131">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="0cbeb-131">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)
- [\<add>](add-of-declaredtypes-element.md)

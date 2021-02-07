---
description: 了解有关的详细信息，请参阅 <dataContractSerializer> <>
title: <dataContractSerializer> <的>
ms.date: 03/30/2017
ms.assetid: d9b3d625-be3f-4768-8e0d-1b7e6929f6a8
ms.openlocfilehash: 3755005782ea773344326d211b9f8f115a97f2ae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754415"
---
# <a name="datacontractserializer-of-systemruntimeserialization"></a><span data-ttu-id="8808a-103">\<dataContractSerializer> 的 \<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="8808a-103">\<dataContractSerializer> of \<system.runtime.serialization></span></span>

<span data-ttu-id="8808a-104">包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的配置数据。</span><span class="sxs-lookup"><span data-stu-id="8808a-104">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.serialization>**](system-runtime-serialization.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<dataContractSerializer>**  
  
## <a name="syntax"></a><span data-ttu-id="8808a-105">语法</span><span class="sxs-lookup"><span data-stu-id="8808a-105">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer"
                       type="String" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8808a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8808a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8808a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8808a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8808a-108">特性</span><span class="sxs-lookup"><span data-stu-id="8808a-108">Attributes</span></span>  
  
|<span data-ttu-id="8808a-109">元素</span><span class="sxs-lookup"><span data-stu-id="8808a-109">Element</span></span>|<span data-ttu-id="8808a-110">说明</span><span class="sxs-lookup"><span data-stu-id="8808a-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8808a-111">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="8808a-111">ignoreExtensionDataObject</span></span>|<span data-ttu-id="8808a-112">一个布尔值，指定在对终结点进行序列化或反序列化时，是否要忽略由该终结点提供的数据。</span><span class="sxs-lookup"><span data-stu-id="8808a-112">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="8808a-113">只可对 `<dataContractSerializer>` 元素下的 `<behavior>` 设置此属性。</span><span class="sxs-lookup"><span data-stu-id="8808a-113">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="8808a-114">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="8808a-114">maxItemsInObjectGraph</span></span>|<span data-ttu-id="8808a-115">一个整数，指定要序列化或反序列化的最大项数。</span><span class="sxs-lookup"><span data-stu-id="8808a-115">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="8808a-116">此属性为 65536。</span><span class="sxs-lookup"><span data-stu-id="8808a-116">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8808a-117">子元素</span><span class="sxs-lookup"><span data-stu-id="8808a-117">Child Elements</span></span>  
  
|<span data-ttu-id="8808a-118">元素</span><span class="sxs-lookup"><span data-stu-id="8808a-118">Element</span></span>|<span data-ttu-id="8808a-119">说明</span><span class="sxs-lookup"><span data-stu-id="8808a-119">Description</span></span>|  
|-------------|-----------------|  
|[\<declaredTypes>](declaredtypes.md)|<span data-ttu-id="8808a-120">包含在进行反序列化时 <xref:System.Runtime.Serialization.DataContractSerializer> 使用的已知类型。</span><span class="sxs-lookup"><span data-stu-id="8808a-120">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span><br /><br /> <span data-ttu-id="8808a-121">有关数据协定和已知类型的详细信息，请参阅 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md)。</span><span class="sxs-lookup"><span data-stu-id="8808a-121">For more information about data contracts and known types, see [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8808a-122">父元素</span><span class="sxs-lookup"><span data-stu-id="8808a-122">Parent Elements</span></span>  
  
|<span data-ttu-id="8808a-123">元素</span><span class="sxs-lookup"><span data-stu-id="8808a-123">Element</span></span>|<span data-ttu-id="8808a-124">说明</span><span class="sxs-lookup"><span data-stu-id="8808a-124">Description</span></span>|  
|-------------|-----------------|  
|[\<system.runtime.serialization>](system-runtime-serialization.md)|<span data-ttu-id="8808a-125">表示 <xref:System.Runtime.Serialization> 命名空间节的根元素，并包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的设置选项的元素。</span><span class="sxs-lookup"><span data-stu-id="8808a-125">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8808a-126">备注</span><span class="sxs-lookup"><span data-stu-id="8808a-126">Remarks</span></span>  

 <span data-ttu-id="8808a-127">有关已知类型的详细信息，请参阅 <xref:System.Runtime.Serialization.DataContractSerializer> 和 [数据协定已知类型](../../../wcf/feature-details/data-contract-known-types.md)。</span><span class="sxs-lookup"><span data-stu-id="8808a-127">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer> and [Data Contract Known Types](../../../wcf/feature-details/data-contract-known-types.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8808a-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="8808a-128">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- [<span data-ttu-id="8808a-129">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="8808a-129">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)

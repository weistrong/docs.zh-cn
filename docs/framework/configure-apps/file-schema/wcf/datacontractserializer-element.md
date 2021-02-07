---
description: 了解详细信息： <dataContractSerializer>
title: <dataContractSerializer>
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- <dataContractSerializer> element
- DataContractSerializer
- KnownTypes
ms.assetid: f41fb4d5-24e7-4059-8010-286a30bfea93
ms.openlocfilehash: 0705a40f55d76ef46a7debcd4ecfb5235c7c0d21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754428"
---
# \<dataContractSerializer>

<span data-ttu-id="1a72c-102">包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的配置数据。</span><span class="sxs-lookup"><span data-stu-id="1a72c-102">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="1a72c-103">此元素出现在两个不同的层次结构中。</span><span class="sxs-lookup"><span data-stu-id="1a72c-103">This element occurs in two different hierarchies.</span></span> <span data-ttu-id="1a72c-104">这两个层次结构分别在下面的“架构层次结构”一节和“备注”一节中列出。</span><span class="sxs-lookup"><span data-stu-id="1a72c-104">One is listed the following Schema Hierarchy section and the other is listed in the Remarks section.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<dataContractSerializer>**  
  
## <a name="syntax"></a><span data-ttu-id="1a72c-105">语法</span><span class="sxs-lookup"><span data-stu-id="1a72c-105">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1a72c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1a72c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="1a72c-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a72c-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1a72c-108">特性</span><span class="sxs-lookup"><span data-stu-id="1a72c-108">Attributes</span></span>  
  
|<span data-ttu-id="1a72c-109">元素</span><span class="sxs-lookup"><span data-stu-id="1a72c-109">Element</span></span>|<span data-ttu-id="1a72c-110">说明</span><span class="sxs-lookup"><span data-stu-id="1a72c-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1a72c-111">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="1a72c-111">ignoreExtensionDataObject</span></span>|<span data-ttu-id="1a72c-112">一个布尔值，指定在对终结点进行序列化或反序列化时，是否要忽略由该终结点提供的数据。</span><span class="sxs-lookup"><span data-stu-id="1a72c-112">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="1a72c-113">只可对 `<dataContractSerializer>` 元素下的 `<behavior>` 设置此属性。</span><span class="sxs-lookup"><span data-stu-id="1a72c-113">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="1a72c-114">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="1a72c-114">maxItemsInObjectGraph</span></span>|<span data-ttu-id="1a72c-115">一个整数，指定要序列化或反序列化的最大项数。</span><span class="sxs-lookup"><span data-stu-id="1a72c-115">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="1a72c-116">此属性为 65536。</span><span class="sxs-lookup"><span data-stu-id="1a72c-116">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1a72c-117">子元素</span><span class="sxs-lookup"><span data-stu-id="1a72c-117">Child Elements</span></span>  

 <span data-ttu-id="1a72c-118">无。</span><span class="sxs-lookup"><span data-stu-id="1a72c-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1a72c-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1a72c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="1a72c-120">元素</span><span class="sxs-lookup"><span data-stu-id="1a72c-120">Element</span></span>|<span data-ttu-id="1a72c-121">说明</span><span class="sxs-lookup"><span data-stu-id="1a72c-121">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-servicebehaviors.md)|<span data-ttu-id="1a72c-122">服务行为的设置集合。</span><span class="sxs-lookup"><span data-stu-id="1a72c-122">A collection of settings for the behavior of a service.</span></span>|  
|[\<system.runtime.serialization>](system-runtime-serialization.md)|<span data-ttu-id="1a72c-123">表示 <xref:System.Runtime.Serialization> 命名空间节的根元素，并包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的设置选项的元素。</span><span class="sxs-lookup"><span data-stu-id="1a72c-123">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a72c-124">备注</span><span class="sxs-lookup"><span data-stu-id="1a72c-124">Remarks</span></span>  

 <span data-ttu-id="1a72c-125">如本主题的简介中所述，这是在其中发生元素的第二个层次结构 \<X509Extension> 。</span><span class="sxs-lookup"><span data-stu-id="1a72c-125">As stated in the Introduction of this topic, this is the second hierarchy in which the \<X509Extension> element occurs.</span></span>  
  
 [\<system.runtime.serialization>](system-runtime-serialization.md)  
  
 [\<dataContractSerializer>](datacontractserializer-element.md)  
  
 <span data-ttu-id="1a72c-126">有关已知类型的更多信息，请参见 <xref:System.Runtime.Serialization.DataContractSerializer>。</span><span class="sxs-lookup"><span data-stu-id="1a72c-126">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a72c-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="1a72c-127">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- <xref:System.ServiceModel.Configuration.DataContractSerializerElement>
- [<span data-ttu-id="1a72c-128">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="1a72c-128">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="1a72c-129">数据传输和序列化</span><span class="sxs-lookup"><span data-stu-id="1a72c-129">Data Transfer and Serialization</span></span>](../../../wcf/feature-details/data-transfer-and-serialization.md)

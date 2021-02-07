---
description: 了解详细信息： dataContractSerializer
title: dataContractSerializer
ms.date: 03/30/2017
ms.assetid: a47513a4-a96c-4350-8586-daacb05dee71
ms.openlocfilehash: 5dee59ba97a1632c142179aee79058dd3ce8c349
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754402"
---
# <a name="datacontractserializer"></a><span data-ttu-id="fd750-103">dataContractSerializer</span><span class="sxs-lookup"><span data-stu-id="fd750-103">dataContractSerializer</span></span>

<span data-ttu-id="fd750-104">包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的配置数据。</span><span class="sxs-lookup"><span data-stu-id="fd750-104">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<dataContractSerializer>**  
  
## <a name="syntax"></a><span data-ttu-id="fd750-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd750-105">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fd750-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="fd750-106">Attributes and Elements</span></span>  

 <span data-ttu-id="fd750-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd750-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fd750-108">特性</span><span class="sxs-lookup"><span data-stu-id="fd750-108">Attributes</span></span>  
  
|<span data-ttu-id="fd750-109">元素</span><span class="sxs-lookup"><span data-stu-id="fd750-109">Element</span></span>|<span data-ttu-id="fd750-110">说明</span><span class="sxs-lookup"><span data-stu-id="fd750-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fd750-111">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="fd750-111">ignoreExtensionDataObject</span></span>|<span data-ttu-id="fd750-112">一个布尔值，指定在对终结点进行序列化或反序列化时，是否要忽略由该终结点提供的数据。</span><span class="sxs-lookup"><span data-stu-id="fd750-112">A Boolean value that specifies whether to ignore data supplied by the endpoint, when it is being serialized or deserialized.</span></span>|  
|<span data-ttu-id="fd750-113">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="fd750-113">maxItemsInObjectGraph</span></span>|<span data-ttu-id="fd750-114">一个整数，指定要序列化或反序列化的最大项数。</span><span class="sxs-lookup"><span data-stu-id="fd750-114">An integer that specifies the maximum number of items to serialize or deserialize.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fd750-115">子元素</span><span class="sxs-lookup"><span data-stu-id="fd750-115">Child Elements</span></span>  

 <span data-ttu-id="fd750-116">无。</span><span class="sxs-lookup"><span data-stu-id="fd750-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fd750-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fd750-117">Parent Elements</span></span>  
  
|<span data-ttu-id="fd750-118">元素</span><span class="sxs-lookup"><span data-stu-id="fd750-118">Element</span></span>|<span data-ttu-id="fd750-119">说明</span><span class="sxs-lookup"><span data-stu-id="fd750-119">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="fd750-120">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="fd750-120">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd750-121">备注</span><span class="sxs-lookup"><span data-stu-id="fd750-121">Remarks</span></span>  

 <span data-ttu-id="fd750-122">有关已知类型的更多信息，请参见 <xref:System.Runtime.Serialization.DataContractSerializer> 文档。</span><span class="sxs-lookup"><span data-stu-id="fd750-122">See the <xref:System.Runtime.Serialization.DataContractSerializer> documentation for more information about known types.</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="fd750-123">在配置文件中，`<dataContractSerializer>` 行为元素（如果有）应始终在 `<enableWebScript>` 行为元素之前出现。</span><span class="sxs-lookup"><span data-stu-id="fd750-123">The `<dataContractSerializer>` behavior element (if present) should always appear before the `<enableWebScript>` behavior element in the configuration file.</span></span> <span data-ttu-id="fd750-124">否则，产生的行为将是不确定的。</span><span class="sxs-lookup"><span data-stu-id="fd750-124">Otherwise, the resulting behavior is undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd750-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd750-125">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- <xref:System.ServiceModel.Configuration.DataContractSerializerElement>
- [<span data-ttu-id="fd750-126">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="fd750-126">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="fd750-127">数据传输和序列化</span><span class="sxs-lookup"><span data-stu-id="fd750-127">Data Transfer and Serialization</span></span>](../../../wcf/feature-details/data-transfer-and-serialization.md)

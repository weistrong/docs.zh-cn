---
description: 了解详细信息： <>
title: <system.runtime.serialization>
ms.date: 03/30/2017
ms.assetid: a8cebf4c-06d2-4667-8f5b-c3e1fc90df6f
ms.openlocfilehash: cf1d95c8650e4b6979d4f34b0bed1fa395911f2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786624"
---
# \<system.runtime.serialization>

<span data-ttu-id="16ac9-103">表示 <xref:System.Runtime.Serialization> 命名空间节的根元素，并包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的设置选项的元素。</span><span class="sxs-lookup"><span data-stu-id="16ac9-103">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<system.runtime.serialization>**  
  
## <a name="syntax"></a><span data-ttu-id="16ac9-104">语法</span><span class="sxs-lookup"><span data-stu-id="16ac9-104">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="16ac9-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="16ac9-105">Attributes and Elements</span></span>  

 <span data-ttu-id="16ac9-106">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="16ac9-106">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="16ac9-107">特性</span><span class="sxs-lookup"><span data-stu-id="16ac9-107">Attributes</span></span>  

 <span data-ttu-id="16ac9-108">无。</span><span class="sxs-lookup"><span data-stu-id="16ac9-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="16ac9-109">子元素</span><span class="sxs-lookup"><span data-stu-id="16ac9-109">Child Elements</span></span>  
  
|<span data-ttu-id="16ac9-110">元素</span><span class="sxs-lookup"><span data-stu-id="16ac9-110">Element</span></span>|<span data-ttu-id="16ac9-111">说明</span><span class="sxs-lookup"><span data-stu-id="16ac9-111">Description</span></span>|  
|-------------|-----------------|  
|[\<dataContractSerializer>](datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="16ac9-112">使得可以在反序列化时添加要使用的已知类型。</span><span class="sxs-lookup"><span data-stu-id="16ac9-112">Enables addition of known types to be used when deserialization.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="16ac9-113">父元素</span><span class="sxs-lookup"><span data-stu-id="16ac9-113">Parent Elements</span></span>  
  
|<span data-ttu-id="16ac9-114">元素</span><span class="sxs-lookup"><span data-stu-id="16ac9-114">Element</span></span>|<span data-ttu-id="16ac9-115">描述</span><span class="sxs-lookup"><span data-stu-id="16ac9-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="16ac9-116">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="16ac9-116">\<configuration> Element</span></span>](../configuration-element.md)|<span data-ttu-id="16ac9-117">配置的顶级元素。</span><span class="sxs-lookup"><span data-stu-id="16ac9-117">The top level element for configuration.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="16ac9-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="16ac9-118">See also</span></span>

- <xref:System.Runtime.Serialization>
- [<span data-ttu-id="16ac9-119">使用数据协定</span><span class="sxs-lookup"><span data-stu-id="16ac9-119">Using Data Contracts</span></span>](../../../wcf/feature-details/using-data-contracts.md)
- [<span data-ttu-id="16ac9-120">数据协定已知类型</span><span class="sxs-lookup"><span data-stu-id="16ac9-120">Data Contract Known Types</span></span>](../../../wcf/feature-details/data-contract-known-types.md)

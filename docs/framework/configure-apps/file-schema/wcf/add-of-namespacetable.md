---
description: 了解详细 <add> 信息： <namespaceTable>
title: <add> 的 <namespaceTable>
ms.date: 03/30/2017
ms.assetid: cf7b5b75-63bd-49a6-abac-4bfdab377e36
ms.openlocfilehash: b7804bdec4a1fb2199c81ba0dde031b80b451d2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750255"
---
# <a name="add-of-namespacetable"></a><span data-ttu-id="f8177-103">\<add> 的 \<namespaceTable></span><span class="sxs-lookup"><span data-stu-id="f8177-103">\<add> of \<namespaceTable></span></span>

<span data-ttu-id="f8177-104">表示一个配置元素，此元素包含随后可在 XPath 筛选器中用于路由的前缀映射的命名空间。</span><span class="sxs-lookup"><span data-stu-id="f8177-104">Represents a configuration element that contains a namespace to prefix mapping that can then be used in XPath filters for routing.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<namespaceTable>**](namespacetable.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="f8177-105">语法</span><span class="sxs-lookup"><span data-stu-id="f8177-105">Syntax</span></span>  
  
```xml  
<routing>
  <namespaceTable>
    <add namespace="String"
         prefix="String" />
  </namespaceTable>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f8177-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f8177-106">Attributes and Elements</span></span>  

 <span data-ttu-id="f8177-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f8177-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f8177-108">特性</span><span class="sxs-lookup"><span data-stu-id="f8177-108">Attributes</span></span>  
  
|<span data-ttu-id="f8177-109">属性</span><span class="sxs-lookup"><span data-stu-id="f8177-109">Attribute</span></span>|<span data-ttu-id="f8177-110">说明</span><span class="sxs-lookup"><span data-stu-id="f8177-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f8177-111">命名空间</span><span class="sxs-lookup"><span data-stu-id="f8177-111">namespace</span></span>|<span data-ttu-id="f8177-112">一个包含命名空间的字符串。</span><span class="sxs-lookup"><span data-stu-id="f8177-112">A string containing the namespace.</span></span>|  
|<span data-ttu-id="f8177-113">前缀</span><span class="sxs-lookup"><span data-stu-id="f8177-113">prefix</span></span>|<span data-ttu-id="f8177-114">一个包含此命名空间的前缀的字符串。</span><span class="sxs-lookup"><span data-stu-id="f8177-114">A string containing the prefix for this namespace.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f8177-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f8177-115">Child Elements</span></span>  

 <span data-ttu-id="f8177-116">无。</span><span class="sxs-lookup"><span data-stu-id="f8177-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f8177-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f8177-117">Parent Elements</span></span>  
  
|<span data-ttu-id="f8177-118">元素</span><span class="sxs-lookup"><span data-stu-id="f8177-118">Element</span></span>|<span data-ttu-id="f8177-119">说明</span><span class="sxs-lookup"><span data-stu-id="f8177-119">Description</span></span>|  
|-------------|-----------------|  
|[\<namespaceTable>](namespacetable.md)|<span data-ttu-id="f8177-120">表示用于定义一组元素的配置节，这些元素包含随后可在 XPath 筛选器中用于路由的前缀映射的命名空间。</span><span class="sxs-lookup"><span data-stu-id="f8177-120">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f8177-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8177-121">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.NamespaceElement?displayProperty=nameWithType>

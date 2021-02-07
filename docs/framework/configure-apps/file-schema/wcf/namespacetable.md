---
description: 了解详细信息： <namespaceTable>
title: <namespaceTable>
ms.date: 03/30/2017
ms.assetid: 64801766-01b7-4c65-9ce6-70ad5af67689
ms.openlocfilehash: 73bfac93fba3247c02c2d86d1482af2563015a76
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684082"
---
# \<namespaceTable>

<span data-ttu-id="d72c4-102">表示用于定义一组元素的配置节，这些元素包含随后可在 XPath 筛选器中用于路由的前缀映射的命名空间。</span><span class="sxs-lookup"><span data-stu-id="d72c4-102">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<namespaceTable>**  
  
## <a name="syntax"></a><span data-ttu-id="d72c4-103">语法</span><span class="sxs-lookup"><span data-stu-id="d72c4-103">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <namespaceTable>
      <add namespace="String"
           prefix="String" />
    </namespaceTable>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d72c4-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d72c4-104">Attributes and elements</span></span>

<span data-ttu-id="d72c4-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d72c4-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="d72c4-106">特性</span><span class="sxs-lookup"><span data-stu-id="d72c4-106">Attributes</span></span>

<span data-ttu-id="d72c4-107">无</span><span class="sxs-lookup"><span data-stu-id="d72c4-107">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="d72c4-108">子元素</span><span class="sxs-lookup"><span data-stu-id="d72c4-108">Child elements</span></span>

|     | <span data-ttu-id="d72c4-109">说明</span><span class="sxs-lookup"><span data-stu-id="d72c4-109">Description</span></span> |
| --- | ----------- |
| [**\<filter>**](filter.md) | <span data-ttu-id="d72c4-110">定义用于 XPath 表达式的命名空间前缀映射。</span><span class="sxs-lookup"><span data-stu-id="d72c4-110">Defines a namespace prefix mapping used for XPath expressions.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="d72c4-111">父元素</span><span class="sxs-lookup"><span data-stu-id="d72c4-111">Parent elements</span></span>

|     | <span data-ttu-id="d72c4-112">说明</span><span class="sxs-lookup"><span data-stu-id="d72c4-112">Description</span></span> |
| --- | ----------- |
| [**\<routing>**](routing.md) | <span data-ttu-id="d72c4-113">表示用于定义一组路由筛选器的配置节，这些筛选器确定计算传入消息时要使用的 Windows Communication Foundation 的类型 (WCF) ，以及用于 <xref:System.ServiceModel.Dispatcher.MessageFilter> 定义筛选器匹配时要将消息发送到的目标终结点的路由表。</span><span class="sxs-lookup"><span data-stu-id="d72c4-113">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d72c4-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d72c4-114">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.NamespaceElementCollection?displayProperty=nameWithType>

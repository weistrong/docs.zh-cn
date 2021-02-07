---
description: 了解详细信息： <routing>
title: <routing>
ms.date: 03/30/2017
ms.assetid: a210c209-3940-4288-9a8e-39b1e62606bc
ms.openlocfilehash: 62222b527a14310b66015d4fdc4503e6cff25c8a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683341"
---
# \<routing>

<span data-ttu-id="a7d7c-102">表示用于定义一组路由筛选器的配置节，这些筛选器确定计算传入消息时要使用的 Windows Communication Foundation 的类型 (WCF) ，以及用于 <xref:System.ServiceModel.Dispatcher.MessageFilter> 定义筛选器匹配时要将消息发送到的目标终结点的路由表。</span><span class="sxs-lookup"><span data-stu-id="a7d7c-102">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<routing>**
  
## <a name="syntax"></a><span data-ttu-id="a7d7c-103">语法</span><span class="sxs-lookup"><span data-stu-id="a7d7c-103">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
    <routingTables>
      <table name="String">
        <entries>
          <add endpoint="String"
               filterName="String"
               priority="Integer" />
        </entries>
      </table>
    </routingTables>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a7d7c-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a7d7c-104">Attributes and elements</span></span>

<span data-ttu-id="a7d7c-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a7d7c-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="a7d7c-106">特性</span><span class="sxs-lookup"><span data-stu-id="a7d7c-106">Attributes</span></span>

<span data-ttu-id="a7d7c-107">无</span><span class="sxs-lookup"><span data-stu-id="a7d7c-107">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="a7d7c-108">子元素</span><span class="sxs-lookup"><span data-stu-id="a7d7c-108">Child elements</span></span>

|     | <span data-ttu-id="a7d7c-109">说明</span><span class="sxs-lookup"><span data-stu-id="a7d7c-109">Description</span></span> |
| --- | ----------- |
| [**\<filters>**](filters-of-routing.md) | <span data-ttu-id="a7d7c-110">包含一组路由筛选器，用于确定在评估传入消息时将使用的 Windows Communication Foundation (WCF) MessageFilter 的类型。</span><span class="sxs-lookup"><span data-stu-id="a7d7c-110">Contains a set of routing filters that determine the type of Windows Communication Foundation (WCF) MessageFilter will be used when evaluating incoming messages.</span></span> |
| [**\<filterTables>**](filtertables.md) | <span data-ttu-id="a7d7c-111">包含路由筛选器和目标终结点之间的映射，以便指定在筛选器匹配时使用的终结点。</span><span class="sxs-lookup"><span data-stu-id="a7d7c-111">Contains mappings between the routing filters and the target endpoints to specify which endpoint to use when the filter matches.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="a7d7c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a7d7c-112">Parent elements</span></span>

|     | <span data-ttu-id="a7d7c-113">说明</span><span class="sxs-lookup"><span data-stu-id="a7d7c-113">Description</span></span> |
| --- | ----------- |
| **\<system.ServiceModel>** | <span data-ttu-id="a7d7c-114">所有 WCF 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="a7d7c-114">The root element of all WCF configuration elements.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a7d7c-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="a7d7c-115">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>

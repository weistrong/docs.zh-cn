---
description: 了解详细 <filters> 信息： <routing>
title: <filters> 的 <routing>
ms.date: 03/30/2017
ms.assetid: 7993cf90-9afd-4c3c-9608-184d5da1105c
ms.openlocfilehash: 41b51453f53fca042f53ca1ee8372413b8478ecd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782047"
---
# <a name="filters-of-routing"></a><span data-ttu-id="888a2-103">\<filters> 的 \<routing></span><span class="sxs-lookup"><span data-stu-id="888a2-103">\<filters> of \<routing></span></span>

<span data-ttu-id="888a2-104">表示用于定义一组路由筛选器的配置节，这些筛选器确定 <xref:System.ServiceModel.Dispatcher.MessageFilter> 计算传入消息时要使用 (WCF) Windows Communication Foundation 的类型。</span><span class="sxs-lookup"><span data-stu-id="888a2-104">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span>

[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**  
  
## <a name="syntax"></a><span data-ttu-id="888a2-105">语法</span><span class="sxs-lookup"><span data-stu-id="888a2-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="888a2-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="888a2-106">Attributes and elements</span></span>

<span data-ttu-id="888a2-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="888a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="888a2-108">特性</span><span class="sxs-lookup"><span data-stu-id="888a2-108">Attributes</span></span>

<span data-ttu-id="888a2-109">无</span><span class="sxs-lookup"><span data-stu-id="888a2-109">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="888a2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="888a2-110">Child elements</span></span>

|     | <span data-ttu-id="888a2-111">说明</span><span class="sxs-lookup"><span data-stu-id="888a2-111">Description</span></span> |
| --- | ----------- |
| [**\<filter>**](filter.md) | <span data-ttu-id="888a2-112">包含一个路由筛选器，该筛选器确定在 <xref:System.ServiceModel.Dispatcher.MessageFilter> 计算传入消息时将使用的 Windows Communication Foundation (WCF) 的类型。</span><span class="sxs-lookup"><span data-stu-id="888a2-112">Contains a routing filter that determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> will be used when evaluating incoming messages.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="888a2-113">父元素</span><span class="sxs-lookup"><span data-stu-id="888a2-113">Parent elements</span></span>

|     | <span data-ttu-id="888a2-114">说明</span><span class="sxs-lookup"><span data-stu-id="888a2-114">Description</span></span> |
| --- | ----------- |
| [**\<routing>**](routing.md) | <span data-ttu-id="888a2-115">表示用于定义一组路由筛选器的配置节，这些筛选器确定计算传入消息时要使用的 Windows Communication Foundation 的类型 (WCF) ，以及用于 <xref:System.ServiceModel.Dispatcher.MessageFilter> 定义筛选器匹配时要将消息发送到的目标终结点的路由表。</span><span class="sxs-lookup"><span data-stu-id="888a2-115">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="888a2-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="888a2-116">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>

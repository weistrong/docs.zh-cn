---
description: 了解详细信息： <entries>
title: <entries>
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: e5aefce4328c341b6d132765c8e726910241aae1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782099"
---
# \<entries>

<span data-ttu-id="3e165-102">一个路由项，包含路由筛选器与在筛选器匹配时消息要发送到的目标终结点之间的映射。</span><span class="sxs-lookup"><span data-stu-id="3e165-102">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<filterTables>**](filtertables.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<filterTable>**](filtertable.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<entries>**  
  
## <a name="syntax"></a><span data-ttu-id="3e165-103">语法</span><span class="sxs-lookup"><span data-stu-id="3e165-103">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
    <filterTable name="String">
      <entries>
        <add backupList="String"
             endpointName="String"
             filterName="String"
             priority="Integer" />
      </entries>
    </filterTable>
  </filterTables>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3e165-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="3e165-104">Attributes and Elements</span></span>  

 <span data-ttu-id="3e165-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3e165-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3e165-106">特性</span><span class="sxs-lookup"><span data-stu-id="3e165-106">Attributes</span></span>  

 <span data-ttu-id="3e165-107">无。</span><span class="sxs-lookup"><span data-stu-id="3e165-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="3e165-108">子元素</span><span class="sxs-lookup"><span data-stu-id="3e165-108">Child Elements</span></span>  
  
|<span data-ttu-id="3e165-109">元素</span><span class="sxs-lookup"><span data-stu-id="3e165-109">Element</span></span>|<span data-ttu-id="3e165-110">说明</span><span class="sxs-lookup"><span data-stu-id="3e165-110">Description</span></span>|  
|-------------|-----------------|  
|[\<filters>](filters-of-routing.md)|<span data-ttu-id="3e165-111">将筛选器映射到以前定义的客户端终结点。</span><span class="sxs-lookup"><span data-stu-id="3e165-111">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="3e165-112">与此筛选器匹配的消息将发送到此目标。</span><span class="sxs-lookup"><span data-stu-id="3e165-112">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3e165-113">父元素</span><span class="sxs-lookup"><span data-stu-id="3e165-113">Parent Elements</span></span>  
  
|<span data-ttu-id="3e165-114">元素</span><span class="sxs-lookup"><span data-stu-id="3e165-114">Element</span></span>|<span data-ttu-id="3e165-115">说明</span><span class="sxs-lookup"><span data-stu-id="3e165-115">Description</span></span>|  
|-------------|-----------------|  
|[\<routing>](routing.md)|<span data-ttu-id="3e165-116">一个包含路由表的配置节。</span><span class="sxs-lookup"><span data-stu-id="3e165-116">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3e165-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3e165-117">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>

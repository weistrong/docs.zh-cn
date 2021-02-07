---
description: 了解详细信息： <discoveryClient>
title: <discoveryClient>
ms.date: 03/30/2017
ms.assetid: a78f74c3-1152-4149-ab29-3f12d316caeb
ms.openlocfilehash: d04eee828bb16e56a65c39059665feb745f3006a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754389"
---
# \<discoveryClient>

<span data-ttu-id="b3852-102">一个用于创建自定义绑定的配置元素，通过该绑定，客户端应用程序能够自动搜索可检测服务，并能够在运行时查找服务地址。</span><span class="sxs-lookup"><span data-stu-id="b3852-102">A configuration element for creating a custom binding that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<discoveryClient>**  
  
## <a name="syntax"></a><span data-ttu-id="b3852-103">语法</span><span class="sxs-lookup"><span data-stu-id="b3852-103">Syntax</span></span>  
  
```xml  
<discoveryClient discoveryEndpoint="String">
  <findCriteria duration="TimeSpan"
                maxResults="Integer"
                scopeMatchBy="Uri">
    <contractTypeNames>
      <add name="String"
           namespace="String" />
    </contractTypeNames>
    <extensions />
    <scopes>
      <add scope="URI"/>
    </scopes>
  </findCriteria>
</discoveryClient>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b3852-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b3852-104">Attributes and Elements</span></span>  

 <span data-ttu-id="b3852-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b3852-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b3852-106">特性</span><span class="sxs-lookup"><span data-stu-id="b3852-106">Attributes</span></span>  
  
|<span data-ttu-id="b3852-107">属性</span><span class="sxs-lookup"><span data-stu-id="b3852-107">Attribute</span></span>|<span data-ttu-id="b3852-108">说明</span><span class="sxs-lookup"><span data-stu-id="b3852-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b3852-109">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3852-109">discoveryEndpoint</span></span>|<span data-ttu-id="b3852-110">一个包含发现终结点名称的字符串。通过此终结点，客户端应用程序能够自动搜索可检测服务，并能够在运行时查找服务地址。</span><span class="sxs-lookup"><span data-stu-id="b3852-110">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b3852-111">子元素</span><span class="sxs-lookup"><span data-stu-id="b3852-111">Child Elements</span></span>  
  
|<span data-ttu-id="b3852-112">元素</span><span class="sxs-lookup"><span data-stu-id="b3852-112">Element</span></span>|<span data-ttu-id="b3852-113">说明</span><span class="sxs-lookup"><span data-stu-id="b3852-113">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="b3852-114">一个配置元素，提供客户端应用程序用于搜索发现服务的一组条件。</span><span class="sxs-lookup"><span data-stu-id="b3852-114">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="b3852-115">可将这些条件划分为搜索条件（指定要查找的服务）和查找终止条件（搜索应持续的时长）。</span><span class="sxs-lookup"><span data-stu-id="b3852-115">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b3852-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b3852-116">Parent Elements</span></span>  
  
|<span data-ttu-id="b3852-117">元素</span><span class="sxs-lookup"><span data-stu-id="b3852-117">Element</span></span>|<span data-ttu-id="b3852-118">说明</span><span class="sxs-lookup"><span data-stu-id="b3852-118">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="b3852-119">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="b3852-119">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b3852-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b3852-120">See also</span></span>

- <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>
- <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientElement>

---
description: 了解详细信息： <discoveryClientSettings>
title: <discoveryClientSettings>
ms.date: 03/30/2017
ms.assetid: 02e1b823-a8bb-4074-90d5-8599f71e8f9d
ms.openlocfilehash: c2fda0dea33ffd6dbca24881eefab2e54e361f92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802289"
---
# \<discoveryClientSettings>

<span data-ttu-id="8be46-102">包含应用程序以客户端形式参与服务发现过程所需的设置。</span><span class="sxs-lookup"><span data-stu-id="8be46-102">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<dynamicEndpoint>**](dynamicendpoint.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<standardEndpoint>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<discoveryClientSettings>**  
  
## <a name="syntax"></a><span data-ttu-id="8be46-103">语法</span><span class="sxs-lookup"><span data-stu-id="8be46-103">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String"
                   namespace="String" />
            <contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI"/>
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      <standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8be46-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8be46-104">Attributes and Elements</span></span>  

 <span data-ttu-id="8be46-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8be46-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8be46-106">特性</span><span class="sxs-lookup"><span data-stu-id="8be46-106">Attributes</span></span>  
  
|<span data-ttu-id="8be46-107">属性</span><span class="sxs-lookup"><span data-stu-id="8be46-107">Attribute</span></span>|<span data-ttu-id="8be46-108">说明</span><span class="sxs-lookup"><span data-stu-id="8be46-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8be46-109">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="8be46-109">discoveryEndpoint</span></span>|<span data-ttu-id="8be46-110">一个包含发现终结点名称的字符串。通过此终结点，客户端应用程序能够自动搜索可检测服务，并能够在运行时查找服务地址。</span><span class="sxs-lookup"><span data-stu-id="8be46-110">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8be46-111">子元素</span><span class="sxs-lookup"><span data-stu-id="8be46-111">Child Elements</span></span>  
  
|<span data-ttu-id="8be46-112">元素</span><span class="sxs-lookup"><span data-stu-id="8be46-112">Element</span></span>|<span data-ttu-id="8be46-113">说明</span><span class="sxs-lookup"><span data-stu-id="8be46-113">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="8be46-114">一个配置元素，提供客户端应用程序用于搜索发现服务的一组条件。</span><span class="sxs-lookup"><span data-stu-id="8be46-114">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="8be46-115">可将这些条件划分为搜索条件（指定要查找的服务）和查找终止条件（搜索应持续的时长）。</span><span class="sxs-lookup"><span data-stu-id="8be46-115">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8be46-116">父元素</span><span class="sxs-lookup"><span data-stu-id="8be46-116">Parent Elements</span></span>  
  
|<span data-ttu-id="8be46-117">元素</span><span class="sxs-lookup"><span data-stu-id="8be46-117">Element</span></span>|<span data-ttu-id="8be46-118">说明</span><span class="sxs-lookup"><span data-stu-id="8be46-118">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="8be46-119">定义一个标准终结点，应用程序通过利用该终结点包含的信息，能够充当可在运行时动态查找终结点地址的客户端程序。</span><span class="sxs-lookup"><span data-stu-id="8be46-119">Defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8be46-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="8be46-120">See also</span></span>

- <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>
- <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientSettingsElement>

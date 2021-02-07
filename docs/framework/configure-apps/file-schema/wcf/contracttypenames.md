---
description: 了解详细信息： <contractTypeNames>
title: <contractTypeNames>
ms.date: 03/30/2017
ms.assetid: 5ec5efc6-87f8-4160-9be0-dcd2e01df3df
ms.openlocfilehash: 7521b16c097a8df75819654525c0663124a1ebd0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754441"
---
# \<contractTypeNames>

<span data-ttu-id="0b86d-102">一个指定协定类型名称列表的配置节，这些名称是所搜索服务的协定名称以及搜索服务时通常采用的条件。</span><span class="sxs-lookup"><span data-stu-id="0b86d-102">A configuration section that specifies a list of contract type names, which are the contract names of the services being searched for, and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="0b86d-103">如果指定多个协定名称，则只有与全部协定都匹配的服务终结点才会进行答复。</span><span class="sxs-lookup"><span data-stu-id="0b86d-103">If more than one contract name is specified, only service endpoints matching ALL contracts will reply.</span></span> <span data-ttu-id="0b86d-104">请注意，在 Windows Communication Foundation (WCF) ，终结点只能支持一个协定。</span><span class="sxs-lookup"><span data-stu-id="0b86d-104">Note that in Windows Communication Foundation (WCF), an endpoint can only support one contract.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<dynamicEndpoint>**](dynamicendpoint.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<standardEndpoint>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<discoveryClientSettings>**](discoveryclientsettings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<findCriteria>**](findcriteria.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<contractTypeNames>**  
  
## <a name="syntax"></a><span data-ttu-id="0b86d-105">语法</span><span class="sxs-lookup"><span data-stu-id="0b86d-105">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0b86d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0b86d-106">Attributes and Elements</span></span>  

 <span data-ttu-id="0b86d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b86d-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0b86d-108">特性</span><span class="sxs-lookup"><span data-stu-id="0b86d-108">Attributes</span></span>  

 <span data-ttu-id="0b86d-109">无。</span><span class="sxs-lookup"><span data-stu-id="0b86d-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0b86d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0b86d-110">Child Elements</span></span>  
  
|<span data-ttu-id="0b86d-111">元素</span><span class="sxs-lookup"><span data-stu-id="0b86d-111">Element</span></span>|<span data-ttu-id="0b86d-112">说明</span><span class="sxs-lookup"><span data-stu-id="0b86d-112">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](contracttypenames.md)|<span data-ttu-id="0b86d-113">协定类型名称是一个属性，它引用搜索服务时通常采用的条件集。</span><span class="sxs-lookup"><span data-stu-id="0b86d-113">A contract type name is a property that refers to the set of criteria typically used when searching for a service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0b86d-114">父元素</span><span class="sxs-lookup"><span data-stu-id="0b86d-114">Parent Elements</span></span>  
  
|<span data-ttu-id="0b86d-115">元素</span><span class="sxs-lookup"><span data-stu-id="0b86d-115">Element</span></span>|<span data-ttu-id="0b86d-116">说明</span><span class="sxs-lookup"><span data-stu-id="0b86d-116">Description</span></span>|  
|-------------|-----------------|  
|[\<findCriteria>](findcriteria.md)|<span data-ttu-id="0b86d-117">一个配置元素，提供客户端应用程序用于搜索发现服务的一组条件。</span><span class="sxs-lookup"><span data-stu-id="0b86d-117">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="0b86d-118">可将这些条件划分为搜索条件（指定要查找的服务）和查找终止条件（搜索应持续的时长）。</span><span class="sxs-lookup"><span data-stu-id="0b86d-118">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0b86d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="0b86d-119">See also</span></span>

- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
- <xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElementCollection>

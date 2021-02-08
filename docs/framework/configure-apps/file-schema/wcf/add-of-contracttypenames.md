---
description: 了解详细 <add> 信息： <contractTypeNames>
title: <add> 的 <contractTypeNames>
ms.date: 03/30/2017
ms.assetid: 03aff6be-5dfb-4a64-ada3-e36227cd43c7
ms.openlocfilehash: 0708aa277b4250cb4134a98ddf7af661840981a8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803992"
---
# <a name="add-of-contracttypenames"></a><span data-ttu-id="f61ce-103">\<add> 的 \<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="f61ce-103">\<add> of \<contractTypeNames></span></span>

<span data-ttu-id="f61ce-104">一个配置元素，指定要搜索的服务的协定名称以及搜索服务时通常使用的条件。</span><span class="sxs-lookup"><span data-stu-id="f61ce-104">A configuration element that specifies the contract name of the services being searched for, and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="f61ce-105">如果指定多个协定名称，则只有与全部协定都匹配的服务终结点才会进行答复。</span><span class="sxs-lookup"><span data-stu-id="f61ce-105">If more than one contract name is specified, only service endpoints matching ALL contracts will reply.</span></span> <span data-ttu-id="f61ce-106">请注意，在 Windows Communication Foundation (WCF) ，终结点只能支持一个协定。</span><span class="sxs-lookup"><span data-stu-id="f61ce-106">Note that in Windows Communication Foundation (WCF), an endpoint can only support one contract.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<dynamicEndpoint>**](dynamicendpoint.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<standardEndpoint>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<discoveryClientSettings>**](discoveryclientsettings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<findCriteria>**](findcriteria.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<contractTypeNames>**](contracttypenames.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="f61ce-107">语法</span><span class="sxs-lookup"><span data-stu-id="f61ce-107">Syntax</span></span>  
  
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
              <add name="String" namespace="String" />
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f61ce-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f61ce-108">Attributes and Elements</span></span>  

 <span data-ttu-id="f61ce-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f61ce-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f61ce-110">特性</span><span class="sxs-lookup"><span data-stu-id="f61ce-110">Attributes</span></span>  
  
|<span data-ttu-id="f61ce-111">属性</span><span class="sxs-lookup"><span data-stu-id="f61ce-111">Attribute</span></span>|<span data-ttu-id="f61ce-112">说明</span><span class="sxs-lookup"><span data-stu-id="f61ce-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f61ce-113">name</span><span class="sxs-lookup"><span data-stu-id="f61ce-113">name</span></span>|<span data-ttu-id="f61ce-114">一个字符串，指定协定类型的名称。</span><span class="sxs-lookup"><span data-stu-id="f61ce-114">A string that specifies the name of the contract type.</span></span>|  
|<span data-ttu-id="f61ce-115">命名空间</span><span class="sxs-lookup"><span data-stu-id="f61ce-115">namespace</span></span>|<span data-ttu-id="f61ce-116">一个字符串，指定协定类型的命名空间。</span><span class="sxs-lookup"><span data-stu-id="f61ce-116">A string that specifies the namespace of the contract type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f61ce-117">子元素</span><span class="sxs-lookup"><span data-stu-id="f61ce-117">Child Elements</span></span>  

 <span data-ttu-id="f61ce-118">无</span><span class="sxs-lookup"><span data-stu-id="f61ce-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f61ce-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f61ce-119">Parent Elements</span></span>  
  
|<span data-ttu-id="f61ce-120">元素</span><span class="sxs-lookup"><span data-stu-id="f61ce-120">Element</span></span>|<span data-ttu-id="f61ce-121">说明</span><span class="sxs-lookup"><span data-stu-id="f61ce-121">Description</span></span>|  
|-------------|-----------------|  
|[\<contractTypeNames>](contracttypenames.md)|<span data-ttu-id="f61ce-122">协定类型名称的集合。</span><span class="sxs-lookup"><span data-stu-id="f61ce-122">A collection of contract type names.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f61ce-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f61ce-123">See also</span></span>

- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
- <xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElement>

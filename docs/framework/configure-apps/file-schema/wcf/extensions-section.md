---
description: 了解详细信息： <extensions> 节
title: <extensions> 区
ms.date: 03/30/2017
ms.assetid: 53a59fb6-dede-47ec-9384-b3c2e8f0c1fa
ms.openlocfilehash: 65b1de76155b1e3fbd8e5f14a5f4a1cb8c180ec1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664686"
---
# <a name="extensions-section"></a><span data-ttu-id="93e48-103">\<extensions> 区</span><span class="sxs-lookup"><span data-stu-id="93e48-103">\<extensions> section</span></span>

<span data-ttu-id="93e48-104">此配置节包含一个扩展集合，这些扩展使用户能够创建扩展的用户定义绑定、行为和其他方面。</span><span class="sxs-lookup"><span data-stu-id="93e48-104">This configuration section contains a collection of extensions, which enable the user to create user-defined bindings, behaviors, and other aspects of extensions.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<extensions>**  
  
## <a name="syntax"></a><span data-ttu-id="93e48-105">语法</span><span class="sxs-lookup"><span data-stu-id="93e48-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <extensions>
    <bindingExtensions>
    </bindingExtensions>
    <behaviorExtensions>
    </behaviorExtensions>
    <bindingElementExtensions>
    </bindingElementExtensions>
    <endpointExtensions>
    </endpointExtensions>
  </extensions>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="93e48-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="93e48-106">Attributes and Elements</span></span>  

 <span data-ttu-id="93e48-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="93e48-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="93e48-108">特性</span><span class="sxs-lookup"><span data-stu-id="93e48-108">Attributes</span></span>  

 <span data-ttu-id="93e48-109">无。</span><span class="sxs-lookup"><span data-stu-id="93e48-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="93e48-110">子元素</span><span class="sxs-lookup"><span data-stu-id="93e48-110">Child Elements</span></span>  
  
|<span data-ttu-id="93e48-111">元素</span><span class="sxs-lookup"><span data-stu-id="93e48-111">Element</span></span>|<span data-ttu-id="93e48-112">说明</span><span class="sxs-lookup"><span data-stu-id="93e48-112">Description</span></span>|  
|-------------|-----------------|  
|[\<behaviorExtensions>](behaviorextensions.md)|<span data-ttu-id="93e48-113">本节包含子元素，这些子元素指定使用户可以自定义服务或终结点行为的行为扩展。</span><span class="sxs-lookup"><span data-stu-id="93e48-113">This section contains child elements that specify behavior extensions, which enable the user to customize service or endpoint behaviors.</span></span>|  
|[\<bindingElementExtensions>](bindingelementextensions.md)|<span data-ttu-id="93e48-114">本节为使用计算机或应用程序配置文件中的自定义绑定元素提供支持。</span><span class="sxs-lookup"><span data-stu-id="93e48-114">This section enables the use of a custom binding element from a machine or application configuration file.</span></span>|  
|[\<bindingExtensions>](bindingextensions.md)|<span data-ttu-id="93e48-115">本节包含子元素，这些子元素指定使用户可以自定义绑定的绑定扩展。</span><span class="sxs-lookup"><span data-stu-id="93e48-115">This section contains child elements that specify binding extensions, which enable the user to customize bindings.</span></span>|  
|[\<endpointExtensions>](endpointextensions.md)|<span data-ttu-id="93e48-116">本节包含元注册标准终结点的子元素。</span><span class="sxs-lookup"><span data-stu-id="93e48-116">This section contains child elements that registers standard endpoints.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="93e48-117">父元素</span><span class="sxs-lookup"><span data-stu-id="93e48-117">Parent Elements</span></span>  
  
|<span data-ttu-id="93e48-118">元素</span><span class="sxs-lookup"><span data-stu-id="93e48-118">Element</span></span>|<span data-ttu-id="93e48-119">说明</span><span class="sxs-lookup"><span data-stu-id="93e48-119">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="93e48-120">system.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="93e48-120">system.ServiceModel</span></span>|<span data-ttu-id="93e48-121">所有 WCF 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="93e48-121">The root element of all WCF configuration elements.</span></span>|

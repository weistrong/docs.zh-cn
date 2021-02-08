---
description: 了解详细信息： <services>
title: <services>
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: 6e8c0c5ad5390c097db7bf1be1f0d489e1c0d624
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786702"
---
# \<services>

<span data-ttu-id="56b9f-102">服务是在配置文件的 `services` 节中定义的。</span><span class="sxs-lookup"><span data-stu-id="56b9f-102">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="56b9f-103">每个服务都有自己的 `service` 配置节。</span><span class="sxs-lookup"><span data-stu-id="56b9f-103">Each service has its own `service` configuration section.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<services>**  
  
## <a name="syntax"></a><span data-ttu-id="56b9f-104">语法</span><span class="sxs-lookup"><span data-stu-id="56b9f-104">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service>
    </service>
  </services>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="56b9f-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="56b9f-105">Attributes and Elements</span></span>  

 <span data-ttu-id="56b9f-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="56b9f-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="56b9f-107">特性</span><span class="sxs-lookup"><span data-stu-id="56b9f-107">Attributes</span></span>  

 <span data-ttu-id="56b9f-108">无</span><span class="sxs-lookup"><span data-stu-id="56b9f-108">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="56b9f-109">子元素</span><span class="sxs-lookup"><span data-stu-id="56b9f-109">Child Elements</span></span>  
  
|<span data-ttu-id="56b9f-110">元素</span><span class="sxs-lookup"><span data-stu-id="56b9f-110">Element</span></span>|<span data-ttu-id="56b9f-111">说明</span><span class="sxs-lookup"><span data-stu-id="56b9f-111">Description</span></span>|  
|-------------|-----------------|  
|[\<service>](service.md)|<span data-ttu-id="56b9f-112">定义特定服务的服务协定、行为和终结点。</span><span class="sxs-lookup"><span data-stu-id="56b9f-112">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="56b9f-113">父元素</span><span class="sxs-lookup"><span data-stu-id="56b9f-113">Parent Elements</span></span>  
  
|<span data-ttu-id="56b9f-114">元素</span><span class="sxs-lookup"><span data-stu-id="56b9f-114">Element</span></span>|<span data-ttu-id="56b9f-115">说明</span><span class="sxs-lookup"><span data-stu-id="56b9f-115">Description</span></span>|  
|-------------|-----------------|  
|[\<system.serviceModel>](system-servicemodel.md)|<span data-ttu-id="56b9f-116">所有 Windows Communication Foundation (WCF) 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="56b9f-116">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="56b9f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="56b9f-117">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServicesSection>

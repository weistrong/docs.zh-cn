---
description: 了解详细信息： <transportConfigurationTypes>
title: <transportConfigurationTypes>
ms.date: 03/30/2017
ms.assetid: 929c8b0a-5460-4f66-a098-2cb8d4e10b69
ms.openlocfilehash: d6ef92cf3bdd10fdc9b374f10aaa748cf4300529
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749267"
---
# \<transportConfigurationTypes>

<span data-ttu-id="5b104-102">表示一个配置元素集合，这些元素标识了特定传输的类型。</span><span class="sxs-lookup"><span data-stu-id="5b104-102">Represents a collection of configuration elements that identify the type of a particular transport.</span></span> <span data-ttu-id="5b104-103">这可以用于添加自定义 WAS 协议。</span><span class="sxs-lookup"><span data-stu-id="5b104-103">This can be used to add custom WAS protocols.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceHostingEnvironment>**](servicehostingenvironment.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transportConfigurationTypes>**  
  
## <a name="syntax"></a><span data-ttu-id="5b104-104">语法</span><span class="sxs-lookup"><span data-stu-id="5b104-104">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5b104-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5b104-105">Attributes and Elements</span></span>  

 <span data-ttu-id="5b104-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b104-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5b104-107">特性</span><span class="sxs-lookup"><span data-stu-id="5b104-107">Attributes</span></span>  
  
|<span data-ttu-id="5b104-108">属性</span><span class="sxs-lookup"><span data-stu-id="5b104-108">Attribute</span></span>|<span data-ttu-id="5b104-109">说明</span><span class="sxs-lookup"><span data-stu-id="5b104-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5b104-110">name</span><span class="sxs-lookup"><span data-stu-id="5b104-110">name</span></span>|<span data-ttu-id="5b104-111">传输的名称</span><span class="sxs-lookup"><span data-stu-id="5b104-111">The name of the transport</span></span>|  
|<span data-ttu-id="5b104-112">transportConfigurationType</span><span class="sxs-lookup"><span data-stu-id="5b104-112">transportConfigurationType</span></span>|<span data-ttu-id="5b104-113">实现传输的类型</span><span class="sxs-lookup"><span data-stu-id="5b104-113">The type that implements the transport</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5b104-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5b104-114">Child Elements</span></span>  
  
|<span data-ttu-id="5b104-115">元素</span><span class="sxs-lookup"><span data-stu-id="5b104-115">Element</span></span>|<span data-ttu-id="5b104-116">说明</span><span class="sxs-lookup"><span data-stu-id="5b104-116">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-of-transportconfigurationtype.md)|<span data-ttu-id="5b104-117">添加一个用于标识特定传输的类型的配置元素。</span><span class="sxs-lookup"><span data-stu-id="5b104-117">Adds a configuration element that identifies the type of a particular transport.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5b104-118">父元素</span><span class="sxs-lookup"><span data-stu-id="5b104-118">Parent Elements</span></span>  
  
|<span data-ttu-id="5b104-119">元素</span><span class="sxs-lookup"><span data-stu-id="5b104-119">Element</span></span>|<span data-ttu-id="5b104-120">说明</span><span class="sxs-lookup"><span data-stu-id="5b104-120">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceHostingEnvironment>](servicehostingenvironment.md)|<span data-ttu-id="5b104-121">定义服务承载环境要为特定传输实例化的类型。</span><span class="sxs-lookup"><span data-stu-id="5b104-121">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5b104-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b104-122">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
- <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElementCollection>
- [<span data-ttu-id="5b104-123">承载</span><span class="sxs-lookup"><span data-stu-id="5b104-123">Hosting</span></span>](../../../wcf/feature-details/hosting.md)

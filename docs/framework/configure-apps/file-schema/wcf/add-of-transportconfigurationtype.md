---
description: 了解详细 <add> 信息： <transportConfigurationType>
title: <add> 的 <transportConfigurationType>
ms.date: 03/30/2017
ms.assetid: 03d79db9-571d-4534-acef-d05e5467b257
ms.openlocfilehash: 4a4a68e1f70bcb2ec7d55d5d6c3b530e71ddc55d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750008"
---
# <a name="add-of-transportconfigurationtype"></a><span data-ttu-id="cd64b-103">\<add> 的 \<transportConfigurationType></span><span class="sxs-lookup"><span data-stu-id="cd64b-103">\<add> of \<transportConfigurationType></span></span>

<span data-ttu-id="cd64b-104">此元素是一个键/值对，可标识特定传输的类型。</span><span class="sxs-lookup"><span data-stu-id="cd64b-104">This element is a key/value pair, which identifies the type of a particular transport.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceHostingEnvironment>**](servicehostingenvironment.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<transportConfigurationTypes>**](transportconfigurationtypes.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="cd64b-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd64b-105">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cd64b-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="cd64b-106">Attributes and Elements</span></span>  

 <span data-ttu-id="cd64b-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd64b-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cd64b-108">特性</span><span class="sxs-lookup"><span data-stu-id="cd64b-108">Attributes</span></span>  
  
|<span data-ttu-id="cd64b-109">属性</span><span class="sxs-lookup"><span data-stu-id="cd64b-109">Attribute</span></span>|<span data-ttu-id="cd64b-110">说明</span><span class="sxs-lookup"><span data-stu-id="cd64b-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cd64b-111">name</span><span class="sxs-lookup"><span data-stu-id="cd64b-111">name</span></span>|<span data-ttu-id="cd64b-112">必需的字符串属性。</span><span class="sxs-lookup"><span data-stu-id="cd64b-112">Required String attribute.</span></span><br /><br /> <span data-ttu-id="cd64b-113">包含一个唯一标识传输类型的用户定义的键。</span><span class="sxs-lookup"><span data-stu-id="cd64b-113">Contains a user-defined key that uniquely identifies the transport type.</span></span>|  
|<span data-ttu-id="cd64b-114">transportConfigurationType</span><span class="sxs-lookup"><span data-stu-id="cd64b-114">transportConfigurationType</span></span>|<span data-ttu-id="cd64b-115">一个包含实现特定传输的类型的字符串。</span><span class="sxs-lookup"><span data-stu-id="cd64b-115">A string that contains the type that implements the specific transport.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cd64b-116">子元素</span><span class="sxs-lookup"><span data-stu-id="cd64b-116">Child Elements</span></span>  

 <span data-ttu-id="cd64b-117">无</span><span class="sxs-lookup"><span data-stu-id="cd64b-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cd64b-118">父元素</span><span class="sxs-lookup"><span data-stu-id="cd64b-118">Parent Elements</span></span>  
  
|<span data-ttu-id="cd64b-119">元素</span><span class="sxs-lookup"><span data-stu-id="cd64b-119">Element</span></span>|<span data-ttu-id="cd64b-120">说明</span><span class="sxs-lookup"><span data-stu-id="cd64b-120">Description</span></span>|  
|-------------|-----------------|  
|[\<transportConfigurationTypes>](transportconfigurationtypes.md)|<span data-ttu-id="cd64b-121">一个实现特定传输的类型的集合。</span><span class="sxs-lookup"><span data-stu-id="cd64b-121">A collection of types that implement the specific transport.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="cd64b-122">示例</span><span class="sxs-lookup"><span data-stu-id="cd64b-122">Example</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="net.udp"
         transportConfigurationType="Microsoft.ServiceModel.Samples.Hosting.HostedUdpTransportConfiguration, UdpActivation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6fa904d2da1848d6" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="see-also"></a><span data-ttu-id="cd64b-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd64b-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
- [<span data-ttu-id="cd64b-124">承载</span><span class="sxs-lookup"><span data-stu-id="cd64b-124">Hosting</span></span>](../../../wcf/feature-details/hosting.md)

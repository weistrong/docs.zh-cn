---
description: 了解详细信息： <mexEndpoint>
title: <mexEndpoint>
ms.date: 03/30/2017
ms.assetid: c9823060-0a5d-4f9d-99d4-4d113b758247
ms.openlocfilehash: 1872b6104aaaaa2787ca3f359026552499bade9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684407"
---
# \<mexEndpoint>

<span data-ttu-id="e20be-102">此配置元素定义具有固定 IMetadataExchange 协定的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="e20be-102">This configuration element defines a standard endpoint with a fixed IMetadataExchange contract.</span></span> <span data-ttu-id="e20be-103">由于所有元数据交换终结点都指定 IMetadataExchange 作为其协定，因此可以使用此标准终结点，而不必定义您自己的终结点。</span><span class="sxs-lookup"><span data-stu-id="e20be-103">Since all metadata exchange endpoints specify IMetadataExchange as their contract, you can use this standard point instead of defining one for yourself.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<mexEndpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="e20be-104">语法</span><span class="sxs-lookup"><span data-stu-id="e20be-104">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <mexEndpoint>
      <standardEndpoint name="String" />
    </mexEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e20be-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="e20be-105">Attributes and Elements</span></span>  

 <span data-ttu-id="e20be-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e20be-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e20be-107">特性</span><span class="sxs-lookup"><span data-stu-id="e20be-107">Attributes</span></span>  
  
|<span data-ttu-id="e20be-108">属性</span><span class="sxs-lookup"><span data-stu-id="e20be-108">Attribute</span></span>|<span data-ttu-id="e20be-109">说明</span><span class="sxs-lookup"><span data-stu-id="e20be-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e20be-110">name</span><span class="sxs-lookup"><span data-stu-id="e20be-110">name</span></span>|<span data-ttu-id="e20be-111">一个字符串，指定标准终结点的配置的名称。</span><span class="sxs-lookup"><span data-stu-id="e20be-111">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="e20be-112">此名称在服务终结点的 `endpointConfiguration` 特性中用于将标准终结点链接到其配置。</span><span class="sxs-lookup"><span data-stu-id="e20be-112">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e20be-113">子元素</span><span class="sxs-lookup"><span data-stu-id="e20be-113">Child Elements</span></span>  

 <span data-ttu-id="e20be-114">无。</span><span class="sxs-lookup"><span data-stu-id="e20be-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e20be-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e20be-115">Parent Elements</span></span>  
  
|<span data-ttu-id="e20be-116">元素</span><span class="sxs-lookup"><span data-stu-id="e20be-116">Element</span></span>|<span data-ttu-id="e20be-117">说明</span><span class="sxs-lookup"><span data-stu-id="e20be-117">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="e20be-118">具有一个或多个固定属性（地址、绑定和协定）的预定义终结点的标准终结点集合。</span><span class="sxs-lookup"><span data-stu-id="e20be-118">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|

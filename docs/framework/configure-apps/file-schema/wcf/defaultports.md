---
description: 了解详细信息： <defaultPorts>
title: <defaultPorts>
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 7cd0635568bf80734900f5e54f918150ea657322
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803901"
---
# \<defaultPorts>

<span data-ttu-id="49b00-102">一个默认端口集合，列出客户端应用程序侦听的默认通信终结点。</span><span class="sxs-lookup"><span data-stu-id="49b00-102">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<useRequestHeadersForMetadataAddress>**](userequestheadersformetadataaddress.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<defaultPorts>**  
  
## <a name="syntax"></a><span data-ttu-id="49b00-103">语法</span><span class="sxs-lookup"><span data-stu-id="49b00-103">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="49b00-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="49b00-104">Attributes and Elements</span></span>  

 <span data-ttu-id="49b00-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49b00-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="49b00-106">特性</span><span class="sxs-lookup"><span data-stu-id="49b00-106">Attributes</span></span>  

 <span data-ttu-id="49b00-107">无。</span><span class="sxs-lookup"><span data-stu-id="49b00-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="49b00-108">子元素</span><span class="sxs-lookup"><span data-stu-id="49b00-108">Child Elements</span></span>  
  
|<span data-ttu-id="49b00-109">元素</span><span class="sxs-lookup"><span data-stu-id="49b00-109">Element</span></span>|<span data-ttu-id="49b00-110">说明</span><span class="sxs-lookup"><span data-stu-id="49b00-110">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="49b00-111">\<defaultPorts> 的 \<add></span><span class="sxs-lookup"><span data-stu-id="49b00-111">\<add> of \<defaultPorts></span></span>](add-of-defaultports.md)|<span data-ttu-id="49b00-112">客户端应用程序侦听的默认通信终结点。</span><span class="sxs-lookup"><span data-stu-id="49b00-112">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="49b00-113">父元素</span><span class="sxs-lookup"><span data-stu-id="49b00-113">Parent Elements</span></span>  
  
|<span data-ttu-id="49b00-114">元素</span><span class="sxs-lookup"><span data-stu-id="49b00-114">Element</span></span>|<span data-ttu-id="49b00-115">说明</span><span class="sxs-lookup"><span data-stu-id="49b00-115">Description</span></span>|  
|-------------|-----------------|  
|[\<useRequestHeadersForMetadataAddress>](userequestheadersformetadataaddress.md)|<span data-ttu-id="49b00-116">默认端口列表。</span><span class="sxs-lookup"><span data-stu-id="49b00-116">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="49b00-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="49b00-117">See also</span></span>

- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>

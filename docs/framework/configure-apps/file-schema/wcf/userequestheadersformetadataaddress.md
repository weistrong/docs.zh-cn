---
description: 了解详细信息： <useRequestHeadersForMetadataAddress>
title: <useRequestHeadersForMetadataAddress>
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: 53636b5890eb54095737e2ed62a75e9b81c1c1f1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664426"
---
# \<useRequestHeadersForMetadataAddress>

<span data-ttu-id="a9678-102">允许从请求消息头中检索元数据地址信息。</span><span class="sxs-lookup"><span data-stu-id="a9678-102">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<useRequestHeadersForMetadataAddress>**  
  
## <a name="syntax"></a><span data-ttu-id="a9678-103">语法</span><span class="sxs-lookup"><span data-stu-id="a9678-103">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a9678-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a9678-104">Attributes and Elements</span></span>  

 <span data-ttu-id="a9678-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a9678-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a9678-106">特性</span><span class="sxs-lookup"><span data-stu-id="a9678-106">Attributes</span></span>  

 <span data-ttu-id="a9678-107">无。</span><span class="sxs-lookup"><span data-stu-id="a9678-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a9678-108">子元素</span><span class="sxs-lookup"><span data-stu-id="a9678-108">Child Elements</span></span>  
  
|<span data-ttu-id="a9678-109">元素</span><span class="sxs-lookup"><span data-stu-id="a9678-109">Element</span></span>|<span data-ttu-id="a9678-110">说明</span><span class="sxs-lookup"><span data-stu-id="a9678-110">Description</span></span>|  
|-------------|-----------------|  
|[\<defaultPorts>](defaultports.md)|<span data-ttu-id="a9678-111">一个默认端口集合，列出客户端应用程序侦听的默认通信终结点。</span><span class="sxs-lookup"><span data-stu-id="a9678-111">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a9678-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a9678-112">Parent Elements</span></span>  
  
|<span data-ttu-id="a9678-113">元素</span><span class="sxs-lookup"><span data-stu-id="a9678-113">Element</span></span>|<span data-ttu-id="a9678-114">说明</span><span class="sxs-lookup"><span data-stu-id="a9678-114">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="a9678-115">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="a9678-115">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a9678-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9678-116">See also</span></span>

- <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>

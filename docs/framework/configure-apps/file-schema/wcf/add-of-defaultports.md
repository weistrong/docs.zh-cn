---
description: 了解详细 <add> 信息： <defaultPorts>
title: <add> 的 <defaultPorts>
ms.date: 03/30/2017
ms.assetid: f162ce42-963b-4779-96a7-d6d8b4ea0d2f
ms.openlocfilehash: 9db7afa5183b185eb842530b051d98236e7fa381
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803953"
---
# <a name="add-of-defaultports"></a><span data-ttu-id="eda2b-103">\<add> 的 \<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="eda2b-103">\<add> of \<defaultPorts></span></span>

<span data-ttu-id="eda2b-104">客户端应用程序侦听的默认通信终结点。</span><span class="sxs-lookup"><span data-stu-id="eda2b-104">A default communications endpoint that the client application listens to.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<useRequestHeadersForMetadataAddress>**](userequestheadersformetadataaddress.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<defaultPorts>**](defaultports.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="eda2b-105">语法</span><span class="sxs-lookup"><span data-stu-id="eda2b-105">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add port="Integer"
         scheme="String" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eda2b-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="eda2b-106">Attributes and Elements</span></span>  

 <span data-ttu-id="eda2b-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eda2b-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eda2b-108">特性</span><span class="sxs-lookup"><span data-stu-id="eda2b-108">Attributes</span></span>  
  
|<span data-ttu-id="eda2b-109">属性</span><span class="sxs-lookup"><span data-stu-id="eda2b-109">Attribute</span></span>|<span data-ttu-id="eda2b-110">说明</span><span class="sxs-lookup"><span data-stu-id="eda2b-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="eda2b-111">port</span><span class="sxs-lookup"><span data-stu-id="eda2b-111">port</span></span>|<span data-ttu-id="eda2b-112">一个整数，指定默认通信端口号。</span><span class="sxs-lookup"><span data-stu-id="eda2b-112">An integer that specifies the default communications port number</span></span>|  
|<span data-ttu-id="eda2b-113">scheme</span><span class="sxs-lookup"><span data-stu-id="eda2b-113">scheme</span></span>|<span data-ttu-id="eda2b-114">一个字符串，指定与通信端口关联的协议设置组。</span><span class="sxs-lookup"><span data-stu-id="eda2b-114">A string that specifies the group of protocol settings associated with a communications port.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eda2b-115">子元素</span><span class="sxs-lookup"><span data-stu-id="eda2b-115">Child Elements</span></span>  

 <span data-ttu-id="eda2b-116">无。</span><span class="sxs-lookup"><span data-stu-id="eda2b-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eda2b-117">父元素</span><span class="sxs-lookup"><span data-stu-id="eda2b-117">Parent Elements</span></span>  
  
|<span data-ttu-id="eda2b-118">元素</span><span class="sxs-lookup"><span data-stu-id="eda2b-118">Element</span></span>|<span data-ttu-id="eda2b-119">说明</span><span class="sxs-lookup"><span data-stu-id="eda2b-119">Description</span></span>|  
|-------------|-----------------|  
|[\<defaultPorts>](defaultports.md)|<span data-ttu-id="eda2b-120">一个默认端口集合，列出客户端应用程序侦听的默认通信终结点。</span><span class="sxs-lookup"><span data-stu-id="eda2b-120">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eda2b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="eda2b-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.DefaultPortElement>

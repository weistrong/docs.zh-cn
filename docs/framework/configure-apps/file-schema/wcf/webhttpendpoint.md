---
description: 了解详细信息： <webHttpEndpoint>
title: <webHttpEndpoint>
ms.date: 03/30/2017
ms.assetid: ecaaeb6f-ebd0-411d-8b53-92477cd45347
ms.openlocfilehash: d1bcda1fc97dece833c8163e5facbefe614af0ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682587"
---
# \<webHttpEndpoint>

<span data-ttu-id="6decb-102">此配置元素定义具有 [\<webHttpBinding>](webhttpbinding.md) 自动添加行为的固定绑定的标准终结点 [\<webHttp>](webhttp.md) 。</span><span class="sxs-lookup"><span data-stu-id="6decb-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](webhttpbinding.md) binding that automatically adds the [\<webHttp>](webhttp.md) behavior.</span></span> <span data-ttu-id="6decb-103">在编写 REST 服务时，请使用此终结点。</span><span class="sxs-lookup"><span data-stu-id="6decb-103">Use this endpoint when writing a REST service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<webHttpEndpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="6decb-104">语法</span><span class="sxs-lookup"><span data-stu-id="6decb-104">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webHttpEndpoint>
      <standardEndpoint automaticFormatSelectionEnabled="String"
                        defaultOutgoingResponseFormat="Xml/Json"
                        helpEnabled="Boolean"
                        webEndpointType="String" />
    </webHttpEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6decb-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6decb-105">Attributes and Elements</span></span>  

 <span data-ttu-id="6decb-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6decb-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6decb-107">特性</span><span class="sxs-lookup"><span data-stu-id="6decb-107">Attributes</span></span>  
  
|<span data-ttu-id="6decb-108">属性</span><span class="sxs-lookup"><span data-stu-id="6decb-108">Attribute</span></span>|<span data-ttu-id="6decb-109">说明</span><span class="sxs-lookup"><span data-stu-id="6decb-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6decb-110">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="6decb-110">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="6decb-111">一个布尔值，指示是否启用自动格式选择。</span><span class="sxs-lookup"><span data-stu-id="6decb-111">A Boolean value that indicates whether automatic format selection is enabled.</span></span><br /><br /> <span data-ttu-id="6decb-112">如果启用了自动格式选择，基础结构将分析请求消息的 `Accept` 标头，并确定最适合的响应格式。</span><span class="sxs-lookup"><span data-stu-id="6decb-112">When automatic format selection is enabled, the infrastructure parses the `Accept` header of the request message and determines the most appropriate response format.</span></span> <span data-ttu-id="6decb-113">如果 `Accept` 标头未指定适合的响应格式，则基础结构将使用请求消息的 `Content-Type`，或使用操作的默认响应格式。</span><span class="sxs-lookup"><span data-stu-id="6decb-113">If the `Accept` header does not specify a suitable response format, the infrastructure uses the `Content-Type` of the request message or the default response format of the operation.</span></span>|  
|<span data-ttu-id="6decb-114">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="6decb-114">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="6decb-115">一个指定默认传出响应格式的特性。</span><span class="sxs-lookup"><span data-stu-id="6decb-115">An attribute that specifies the default outgoing response format.</span></span> <span data-ttu-id="6decb-116">此特性的类型为 <xref:System.ServiceModel.Web.WebMessageFormat></span><span class="sxs-lookup"><span data-stu-id="6decb-116">This attribute is of the <xref:System.ServiceModel.Web.WebMessageFormat> type</span></span>|  
|<span data-ttu-id="6decb-117">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="6decb-117">helpEnabled</span></span>|<span data-ttu-id="6decb-118">一个布尔值，指示是否为终结点启用了 HTTP 帮助页。</span><span class="sxs-lookup"><span data-stu-id="6decb-118">A Boolean value that indicates whether the HTTP help page is enabled for the endpoint.</span></span>|  
|<span data-ttu-id="6decb-119">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="6decb-119">webEndpointType</span></span>|<span data-ttu-id="6decb-120">一个字符串，指定终结点的类型。</span><span class="sxs-lookup"><span data-stu-id="6decb-120">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6decb-121">子元素</span><span class="sxs-lookup"><span data-stu-id="6decb-121">Child Elements</span></span>  

 <span data-ttu-id="6decb-122">无。</span><span class="sxs-lookup"><span data-stu-id="6decb-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6decb-123">父元素</span><span class="sxs-lookup"><span data-stu-id="6decb-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6decb-124">元素</span><span class="sxs-lookup"><span data-stu-id="6decb-124">Element</span></span>|<span data-ttu-id="6decb-125">说明</span><span class="sxs-lookup"><span data-stu-id="6decb-125">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="6decb-126">具有一个或多个固定属性（地址、绑定和协定）的预定义终结点的标准终结点集合。</span><span class="sxs-lookup"><span data-stu-id="6decb-126">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6decb-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6decb-127">See also</span></span>

- <xref:System.ServiceModel.Description.WebHttpEndpoint>
- <xref:System.ServiceModel.Configuration.WebHttpEndpointElement>

---
description: 了解详细信息： <enableWebScript>
title: <enableWebScript>
ms.date: 03/30/2017
ms.assetid: 9c7e96e1-af70-4e6e-ac5c-d67929dddbaa
ms.openlocfilehash: f357bf1ab726cd434a16b2daa9c8115afe7d4430
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725878"
---
# \<enableWebScript>

<span data-ttu-id="9908f-102">通过此元素启用的终结点行为可以使用 ASP.NET AJAX 网页中的服务。</span><span class="sxs-lookup"><span data-stu-id="9908f-102">This element enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<enableWebScript>**  
  
## <a name="syntax"></a><span data-ttu-id="9908f-103">语法</span><span class="sxs-lookup"><span data-stu-id="9908f-103">Syntax</span></span>  
  
```xml  
<enableWebScript />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9908f-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9908f-104">Attributes and Elements</span></span>  

 <span data-ttu-id="9908f-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9908f-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9908f-106">特性</span><span class="sxs-lookup"><span data-stu-id="9908f-106">Attributes</span></span>  

 <span data-ttu-id="9908f-107">无。</span><span class="sxs-lookup"><span data-stu-id="9908f-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9908f-108">子元素</span><span class="sxs-lookup"><span data-stu-id="9908f-108">Child Elements</span></span>  

 <span data-ttu-id="9908f-109">无。</span><span class="sxs-lookup"><span data-stu-id="9908f-109">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9908f-110">父元素</span><span class="sxs-lookup"><span data-stu-id="9908f-110">Parent Elements</span></span>  
  
|<span data-ttu-id="9908f-111">元素</span><span class="sxs-lookup"><span data-stu-id="9908f-111">Element</span></span>|<span data-ttu-id="9908f-112">说明</span><span class="sxs-lookup"><span data-stu-id="9908f-112">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="9908f-113">指定终结点行为集。</span><span class="sxs-lookup"><span data-stu-id="9908f-113">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9908f-114">备注</span><span class="sxs-lookup"><span data-stu-id="9908f-114">Remarks</span></span>  

 <span data-ttu-id="9908f-115">此行为只应与 [\<webHttpBinding>](webhttpbinding.md) 标准绑定或 [\<webMessageEncoding>](webmessageencoding.md) 绑定元素一起使用。</span><span class="sxs-lookup"><span data-stu-id="9908f-115">This behavior should only be used in conjunction with either the [\<webHttpBinding>](webhttpbinding.md) standard binding, or the [\<webMessageEncoding>](webmessageencoding.md) binding element.</span></span>  <span data-ttu-id="9908f-116">有关此行为的更多信息，请参见 <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>。</span><span class="sxs-lookup"><span data-stu-id="9908f-116">For more information on this behavior, see <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9908f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9908f-117">See also</span></span>

- <xref:System.ServiceModel.Configuration.WebScriptEnablingElement>
- <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>
- [<span data-ttu-id="9908f-118">AJAX 集成和 JSON 支持</span><span class="sxs-lookup"><span data-stu-id="9908f-118">AJAX Integration and JSON Support</span></span>](../../../wcf/feature-details/ajax-integration-and-json-support.md)
- [\<webHttp>](webhttp.md)

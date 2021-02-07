---
description: 了解详细信息： <xmlElement>
title: <xmlElement>
ms.date: 03/30/2017
ms.assetid: 395205c2-d8c0-4a5e-90f3-7ce3c085fccd
ms.openlocfilehash: 891f1a95c1f6a79127d48a1572bc805574225530
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682002"
---
# \<xmlElement>

<span data-ttu-id="f487b-102">指定一个 XML 元素，请求令牌时，该元素在消息正文中发送到安全令牌服务。</span><span class="sxs-lookup"><span data-stu-id="f487b-102">Specifies an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<message>**](message-element-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<tokenRequestParameters>**](tokenrequestparameters.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<xmlElement>**  
  
## <a name="syntax"></a><span data-ttu-id="f487b-103">语法</span><span class="sxs-lookup"><span data-stu-id="f487b-103">Syntax</span></span>  
  
```xml  
<tokenRequestParameters>
  <xmlElement xmlElement="String" />
</tokenRequestParameters>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f487b-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f487b-104">Attributes and Elements</span></span>  

 <span data-ttu-id="f487b-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f487b-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f487b-106">特性</span><span class="sxs-lookup"><span data-stu-id="f487b-106">Attributes</span></span>  
  
|<span data-ttu-id="f487b-107">属性</span><span class="sxs-lookup"><span data-stu-id="f487b-107">Attribute</span></span>|<span data-ttu-id="f487b-108">说明</span><span class="sxs-lookup"><span data-stu-id="f487b-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f487b-109">xmlElement</span><span class="sxs-lookup"><span data-stu-id="f487b-109">xmlElement</span></span>|<span data-ttu-id="f487b-110">指定 XML 元素的字符串，请求令牌时，该元素在消息正文中发送到安全令牌服务。</span><span class="sxs-lookup"><span data-stu-id="f487b-110">A string specifying an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f487b-111">子元素</span><span class="sxs-lookup"><span data-stu-id="f487b-111">Child Elements</span></span>  

 <span data-ttu-id="f487b-112">无。</span><span class="sxs-lookup"><span data-stu-id="f487b-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f487b-113">父元素</span><span class="sxs-lookup"><span data-stu-id="f487b-113">Parent Elements</span></span>  
  
|<span data-ttu-id="f487b-114">元素</span><span class="sxs-lookup"><span data-stu-id="f487b-114">Element</span></span>|<span data-ttu-id="f487b-115">说明</span><span class="sxs-lookup"><span data-stu-id="f487b-115">Description</span></span>|  
|-------------|-----------------|  
|[\<tokenRequestParameters>](tokenrequestparameters.md)|<span data-ttu-id="f487b-116">令牌请求参数的集合。</span><span class="sxs-lookup"><span data-stu-id="f487b-116">A collection of token request parameters.</span></span> <span data-ttu-id="f487b-117">每个参数都是一个 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="f487b-117">Each parameter is an XML element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f487b-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="f487b-118">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.TokenRequestParameters%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.TokenRequestParameters%2A>
- [<span data-ttu-id="f487b-119">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="f487b-119">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="f487b-120">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="f487b-120">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="f487b-121">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="f487b-121">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="f487b-122">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="f487b-122">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="f487b-123">绑定</span><span class="sxs-lookup"><span data-stu-id="f487b-123">Bindings</span></span>](../../../wcf/bindings.md)

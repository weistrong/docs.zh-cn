---
description: 了解详细信息： <sslStreamSecurity>
title: <sslStreamSecurity>
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
ms.openlocfilehash: 77e08deb5263e330ead5df21ed1ef2dddbba28ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682691"
---
# \<sslStreamSecurity>

<span data-ttu-id="9f4e7-102">表示一个自定义绑定元素，它支持使用 SSL 流的通道安全。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-102">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<sslStreamSecurity>**  
  
## <a name="syntax"></a><span data-ttu-id="9f4e7-103">语法</span><span class="sxs-lookup"><span data-stu-id="9f4e7-103">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"
                   sslProtocols="Ssl3|Tls|Tls11|Tls12" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9f4e7-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9f4e7-104">Attributes and Elements</span></span>  

 <span data-ttu-id="9f4e7-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9f4e7-106">特性</span><span class="sxs-lookup"><span data-stu-id="9f4e7-106">Attributes</span></span>  
  
|<span data-ttu-id="9f4e7-107">属性</span><span class="sxs-lookup"><span data-stu-id="9f4e7-107">Attribute</span></span>|<span data-ttu-id="9f4e7-108">说明</span><span class="sxs-lookup"><span data-stu-id="9f4e7-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9f4e7-109">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9f4e7-109">requireClientCertificate</span></span>|<span data-ttu-id="9f4e7-110">一个布尔值，指定此绑定是否需要客户端证书。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-110">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="9f4e7-111">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-111">The default is `false`.</span></span>|  
|<span data-ttu-id="9f4e7-112">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="9f4e7-112">sslProtocols</span></span>|<span data-ttu-id="9f4e7-113">指定支持哪些 SslProtocols 的 SslProtocols 枚举标志值。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-113">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="9f4e7-114">默认值为 Ssl3&#124;Tls&#124;Tls11&#124;Tls12。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-114">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9f4e7-115">子元素</span><span class="sxs-lookup"><span data-stu-id="9f4e7-115">Child Elements</span></span>  

 <span data-ttu-id="9f4e7-116">无。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9f4e7-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9f4e7-117">Parent Elements</span></span>  
  
|<span data-ttu-id="9f4e7-118">元素</span><span class="sxs-lookup"><span data-stu-id="9f4e7-118">Element</span></span>|<span data-ttu-id="9f4e7-119">说明</span><span class="sxs-lookup"><span data-stu-id="9f4e7-119">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="9f4e7-120">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="9f4e7-120">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9f4e7-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f4e7-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>
- [<span data-ttu-id="9f4e7-122">绑定</span><span class="sxs-lookup"><span data-stu-id="9f4e7-122">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="9f4e7-123">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="9f4e7-123">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="9f4e7-124">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="9f4e7-124">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)

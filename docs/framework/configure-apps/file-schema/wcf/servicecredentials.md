---
description: 了解详细信息： <serviceCredentials>
title: <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 96db336c-4f7a-4193-81a5-910b8ffd804f
ms.openlocfilehash: c6fd39226ca2235d8f8253a7d2f2e363522870e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682860"
---
# \<serviceCredentials>

<span data-ttu-id="c6c5a-102">指定要用于对服务进行身份验证的凭据以及与客户端凭据验证相关的设置。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-102">Specifies the credential to be used in authenticating the service and the client credential validation-related settings.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceCredentials>**  
  
## <a name="syntax"></a><span data-ttu-id="c6c5a-103">语法</span><span class="sxs-lookup"><span data-stu-id="c6c5a-103">Syntax</span></span>  
  
```xml  
<serviceCredentials type="String">
  <clientCertificate>
  </clientCertificate>
  <issuedTokenAuthentication>
  </issuedTokenAuthentication>
  <peer>
  </peer>
  <secureConversationAuthentication>
  </secureConversationAuthentication>
  <serviceCertificate>
  </serviceCertificate>
  <userNameAuthentication>
  </userNameAuthentication>
  <windowsAuthentication>
  </windowsAuthentication>
</serviceCredentials>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c6c5a-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c6c5a-104">Attributes and Elements</span></span>  

 <span data-ttu-id="c6c5a-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c6c5a-106">特性</span><span class="sxs-lookup"><span data-stu-id="c6c5a-106">Attributes</span></span>  
  
|<span data-ttu-id="c6c5a-107">属性</span><span class="sxs-lookup"><span data-stu-id="c6c5a-107">Attribute</span></span>|<span data-ttu-id="c6c5a-108">说明</span><span class="sxs-lookup"><span data-stu-id="c6c5a-108">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="c6c5a-109">一个指定此配置元素的类型的字符串。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-109">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c6c5a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c6c5a-110">Child Elements</span></span>  
  
|<span data-ttu-id="c6c5a-111">元素</span><span class="sxs-lookup"><span data-stu-id="c6c5a-111">Element</span></span>|<span data-ttu-id="c6c5a-112">说明</span><span class="sxs-lookup"><span data-stu-id="c6c5a-112">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCertificate>](clientcertificate-of-servicecredentials.md)|<span data-ttu-id="c6c5a-113">指定证书，当可在带外使用客户端证书时，将使用该证书。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-113">Specifies the certificate to be used when the client certificate is available out-of-band.</span></span> <span data-ttu-id="c6c5a-114">此元素还指定客户端证书验证设置。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-114">This element also specifies client certificate validation settings.</span></span> <span data-ttu-id="c6c5a-115">此元素的类型为 <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-115">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>.</span></span>|  
|[\<issuedTokenAuthentication>](issuedtokenauthentication-of-servicecredentials.md)|<span data-ttu-id="c6c5a-116">指定此服务的当前颁发令牌。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-116">Specifies the current issued token for this service.</span></span> <span data-ttu-id="c6c5a-117">此元素的类型为 <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-117">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement>.</span></span>|  
|[\<peer>](peer-of-servicecredentials.md)|<span data-ttu-id="c6c5a-118">指定对等节点的当前凭据。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-118">Specifies the current credentials for a peer node.</span></span> <span data-ttu-id="c6c5a-119">此元素的类型为 <xref:System.ServiceModel.Configuration.PeerCredentialElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-119">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[\<secureConversationAuthentication>](secureconversationauthentication-of-servicecredential.md)|<span data-ttu-id="c6c5a-120">指定安全对话的当前凭据。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-120">Specifies the current credentials for a secure conversation.</span></span> <span data-ttu-id="c6c5a-121">此元素的类型为 <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-121">This element is of type <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>.</span></span>|  
|[\<serviceCertificate>](servicecertificate-of-servicecredentials.md)|<span data-ttu-id="c6c5a-122">指定服务用于标识自身的证书。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-122">Specifies a certificate used by a service to identify itself.</span></span> <span data-ttu-id="c6c5a-123">此元素的类型为 <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-123">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>.</span></span>|  
|[\<userNameAuthentication>](usernameauthentication.md)|<span data-ttu-id="c6c5a-124">指定用户名密码验证的设置。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-124">Specifies the settings for username password validation.</span></span> <span data-ttu-id="c6c5a-125">此元素的类型为 <xref:System.ServiceModel.Configuration.UserNameServiceElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-125">This element is of type <xref:System.ServiceModel.Configuration.UserNameServiceElement>.</span></span>|  
|[\<windowsAuthentication>](windowsauthentication-of-servicecredentials.md)|<span data-ttu-id="c6c5a-126">指定 Windows 凭据验证的设置。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-126">Specifies the settings for Windows credential validation.</span></span> <span data-ttu-id="c6c5a-127">此元素的类型为 <xref:System.ServiceModel.Configuration.WindowsServiceElement>。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-127">This element is of type <xref:System.ServiceModel.Configuration.WindowsServiceElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c6c5a-128">父元素</span><span class="sxs-lookup"><span data-stu-id="c6c5a-128">Parent Elements</span></span>  
  
|<span data-ttu-id="c6c5a-129">元素</span><span class="sxs-lookup"><span data-stu-id="c6c5a-129">Element</span></span>|<span data-ttu-id="c6c5a-130">说明</span><span class="sxs-lookup"><span data-stu-id="c6c5a-130">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="c6c5a-131">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="c6c5a-131">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c6c5a-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6c5a-132">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement>
- <xref:System.ServiceModel.Description.ServiceCredentials>
- [<span data-ttu-id="c6c5a-133">安全行为</span><span class="sxs-lookup"><span data-stu-id="c6c5a-133">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)

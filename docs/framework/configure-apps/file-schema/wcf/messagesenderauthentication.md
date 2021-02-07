---
description: 了解详细信息： <messageSenderAuthentication>
title: <messageSenderAuthentication>
ms.date: 03/30/2017
ms.assetid: ea62fc06-55fb-42e0-aa2b-8867bdf4b415
ms.openlocfilehash: e98388eafce24b0f19647364b6bbec94ee6ba135
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749313"
---
# \<messageSenderAuthentication>

<span data-ttu-id="bd0a2-102">指定消息发送方使用的对等证书的身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-102">Specifies authentication settings for peer certificate used by a message sender.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peer>**](peer-of-servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<messageSenderAuthentication>**  
  
## <a name="syntax"></a><span data-ttu-id="bd0a2-103">语法</span><span class="sxs-lookup"><span data-stu-id="bd0a2-103">Syntax</span></span>  
  
```xml  
<messageSenderAuthentication customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"
                             certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"
                             revocationMode="NoCheck/Online/Offline"
                             trustedStoreLocation="CurrentUser/LocalMachine" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd0a2-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bd0a2-104">Attributes and Elements</span></span>  

 <span data-ttu-id="bd0a2-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd0a2-106">特性</span><span class="sxs-lookup"><span data-stu-id="bd0a2-106">Attributes</span></span>  
  
|<span data-ttu-id="bd0a2-107">属性</span><span class="sxs-lookup"><span data-stu-id="bd0a2-107">Attribute</span></span>|<span data-ttu-id="bd0a2-108">说明</span><span class="sxs-lookup"><span data-stu-id="bd0a2-108">Description</span></span>|  
|---------------|-----------------|  
|`certificateValidationMode`|<span data-ttu-id="bd0a2-109">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-109">Optional enumeration.</span></span> <span data-ttu-id="bd0a2-110">指定用来验证凭据的五种模式之一。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-110">Specifies one of five modes used to validate credentials.</span></span> <span data-ttu-id="bd0a2-111">此属性的类型为 <xref:System.ServiceModel.Security.X509CertificateValidationMode>。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-111">This attribute is of type <xref:System.ServiceModel.Security.X509CertificateValidationMode>.</span></span> <span data-ttu-id="bd0a2-112">如果设置为 `Custom`，则还必须提供 `customCertificateValidator`。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-112">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|`customCertificateValidatorType`|<span data-ttu-id="bd0a2-113">可选的字符串。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-113">Optional string.</span></span> <span data-ttu-id="bd0a2-114">指定用于验证自定义类型的类型和程序集。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-114">Specifies a type and assembly used to validate a custom type.</span></span> <span data-ttu-id="bd0a2-115">当 `certificateValidationMode` 设置为 `Custom` 时，必须设置此属性。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-115">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span> <span data-ttu-id="bd0a2-116">此属性的类型为 <xref:System.IdentityModel.Selectors.X509CertificateValidator>。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-116">This attribute is of type <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="bd0a2-117">Windows Communication Foundation (WCF) 提供了一个默认的对等证书验证程序，用于根据受信任的人员存储来验证对等证书。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-117">Windows Communication Foundation (WCF) provides a default peer certificate validator that verifies the peer certificate against the trusted people store.</span></span> <span data-ttu-id="bd0a2-118">它还验证证书是否与有效的根相联系。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-118">It also verifies that the certificate chains up to a valid root.</span></span> <span data-ttu-id="bd0a2-119">您可以实现自定义验证程序以指定不同的行为，并使用该属性指向自定义验证程序。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-119">You can implement a custom validator to specify a different behavior and use this attribute to point to the custom validator.</span></span>|  
|`revocationMode`|<span data-ttu-id="bd0a2-120">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-120">Optional enumeration.</span></span> <span data-ttu-id="bd0a2-121">指定证书吊销模式。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-121">Specifies the certificate revocation mode.</span></span> <span data-ttu-id="bd0a2-122">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-122">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>.</span></span> <span data-ttu-id="bd0a2-123">系统通过在吊销证书列表中进行查找来验证对等证书尚未吊销。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-123">The system verifies that the peer certificate has not been revoked by looking it up in the revoked certificate list.</span></span> <span data-ttu-id="bd0a2-124">可以联机执行该检查，也可以根据缓存的吊销列表执行该检查。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-124">This check can be performed either by checking online or against a cached revocation list.</span></span> <span data-ttu-id="bd0a2-125">将此属性设置为 NoCheck 可禁用吊销检查。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-125">Revocation checking can be turned off by setting this attribute to NoCheck.</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="bd0a2-126">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-126">Optional enumeration.</span></span> <span data-ttu-id="bd0a2-127">指定 WCF 安全系统验证对等证书的受信任存储区位置。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-127">Specifies the trusted store location where the peer certificate is validated by the WCF security system.</span></span> <span data-ttu-id="bd0a2-128">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.StoreLocation>。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-128">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bd0a2-129">子元素</span><span class="sxs-lookup"><span data-stu-id="bd0a2-129">Child Elements</span></span>  

 <span data-ttu-id="bd0a2-130">无。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-130">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bd0a2-131">父元素</span><span class="sxs-lookup"><span data-stu-id="bd0a2-131">Parent Elements</span></span>  
  
|<span data-ttu-id="bd0a2-132">元素</span><span class="sxs-lookup"><span data-stu-id="bd0a2-132">Element</span></span>|<span data-ttu-id="bd0a2-133">说明</span><span class="sxs-lookup"><span data-stu-id="bd0a2-133">Description</span></span>|  
|-------------|-----------------|  
|[\<peer>](peer-of-servicecredentials.md)|<span data-ttu-id="bd0a2-134">指定对等节点的当前凭据。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-134">Specifies the current credentials for a peer node.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd0a2-135">备注</span><span class="sxs-lookup"><span data-stu-id="bd0a2-135">Remarks</span></span>  

 <span data-ttu-id="bd0a2-136">如果选择了消息身份验证，则必须配置此元素。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-136">This element must be configured if message authentication is chosen.</span></span> <span data-ttu-id="bd0a2-137">对于输出通道，每条消息都使用提供的证书进行签名 [\<certificate>](certificate-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-137">For output channels, each message is signed using the certificate provided by [\<certificate>](certificate-element.md).</span></span> <span data-ttu-id="bd0a2-138">在将任一消息传递到应用程序之前，都会使用由此元素的 `customCertificateValidatorType` 属性指定的验证程序对照消息凭据对其进行检查。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-138">All messages, before delivered to the application, are checked against the message credential using the validator specified by the `customCertificateValidatorType` attribute of this element.</span></span> <span data-ttu-id="bd0a2-139">验证程序可以接受或拒绝凭据。</span><span class="sxs-lookup"><span data-stu-id="bd0a2-139">The validator can either accept or reject the credential.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd0a2-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="bd0a2-140">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>
- <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>
- <xref:System.ServiceModel.Security.PeerCredential.MessageSenderAuthentication%2A>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.MessageSenderAuthentication%2A>
- [<span data-ttu-id="bd0a2-141">使用证书</span><span class="sxs-lookup"><span data-stu-id="bd0a2-141">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="bd0a2-142">对等网络</span><span class="sxs-lookup"><span data-stu-id="bd0a2-142">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="bd0a2-143">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="bd0a2-143">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="bd0a2-144">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="bd0a2-144">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="bd0a2-145">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="bd0a2-145">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)

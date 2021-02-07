---
description: 了解详细信息： <peerAuthentication>
title: <peerAuthentication>
ms.date: 03/30/2017
ms.assetid: ad545e6f-f06e-4549-ac92-09d758d5c636
ms.openlocfilehash: b640b4aac296c40fadcc5f4070ba58e5f92fd265
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683653"
---
# \<peerAuthentication>

<span data-ttu-id="70d4d-102">指定对等节点使用的对等证书的身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="70d4d-102">Specifies authentication settings for a peer certificate used by a peer node.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peer>**](peer-of-servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<peerAuthentication>**  
  
## <a name="syntax"></a><span data-ttu-id="70d4d-103">语法</span><span class="sxs-lookup"><span data-stu-id="70d4d-103">Syntax</span></span>  
  
```xml  
<peerAuthentication customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"
                    certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"
                    revocationMode="NoCheck/Online/Offline"
                    trustedStoreLocation="CurrentUser/LocalMachine" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70d4d-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="70d4d-104">Attributes and Elements</span></span>  

 <span data-ttu-id="70d4d-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70d4d-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70d4d-106">特性</span><span class="sxs-lookup"><span data-stu-id="70d4d-106">Attributes</span></span>  
  
|<span data-ttu-id="70d4d-107">属性</span><span class="sxs-lookup"><span data-stu-id="70d4d-107">Attribute</span></span>|<span data-ttu-id="70d4d-108">说明</span><span class="sxs-lookup"><span data-stu-id="70d4d-108">Description</span></span>|  
|---------------|-----------------|  
|`certificateValidationMode`|<span data-ttu-id="70d4d-109">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="70d4d-109">Optional enumeration.</span></span> <span data-ttu-id="70d4d-110">指定用来验证凭据的三种模式之一。</span><span class="sxs-lookup"><span data-stu-id="70d4d-110">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="70d4d-111">此属性的类型为 <xref:System.ServiceModel.Security.X509CertificateValidationMode>。</span><span class="sxs-lookup"><span data-stu-id="70d4d-111">This attribute is of type <xref:System.ServiceModel.Security.X509CertificateValidationMode>.</span></span> <span data-ttu-id="70d4d-112">如果设置为 `Custom`，则还必须提供 `customCertificateValidator`。</span><span class="sxs-lookup"><span data-stu-id="70d4d-112">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|`customCertificateValidatorType`|<span data-ttu-id="70d4d-113">可选的字符串。</span><span class="sxs-lookup"><span data-stu-id="70d4d-113">Optional string.</span></span> <span data-ttu-id="70d4d-114">指定用于验证自定义类型的类型和程序集。</span><span class="sxs-lookup"><span data-stu-id="70d4d-114">Specifies a type and assembly used to validate a custom type.</span></span> <span data-ttu-id="70d4d-115">当 `certificateValidationMode` 设置为 `Custom` 时，必须设置此属性。</span><span class="sxs-lookup"><span data-stu-id="70d4d-115">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span> <span data-ttu-id="70d4d-116">此属性的类型为 <xref:System.IdentityModel.Selectors.X509CertificateValidator>。</span><span class="sxs-lookup"><span data-stu-id="70d4d-116">This attribute is of type <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="70d4d-117">Windows Communication Foundation (WCF) 提供了一个默认的对等证书验证程序，用于根据受信任的人员存储来验证对等证书。</span><span class="sxs-lookup"><span data-stu-id="70d4d-117">Windows Communication Foundation (WCF) provides a default peer certificate validator that verifies the peer certificate against the trusted people store.</span></span> <span data-ttu-id="70d4d-118">它还验证证书是否与有效的根相联系。</span><span class="sxs-lookup"><span data-stu-id="70d4d-118">It also verifies that the certificate chains up to a valid root.</span></span> <span data-ttu-id="70d4d-119">您可以实现自定义验证程序以指定不同的行为，并使用该属性指向自定义验证程序。</span><span class="sxs-lookup"><span data-stu-id="70d4d-119">You can implement a custom validator to specify a different behavior and use this attribute to point to the custom validator.</span></span>|  
|`revocationMode`|<span data-ttu-id="70d4d-120">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="70d4d-120">Optional enumeration.</span></span> <span data-ttu-id="70d4d-121">指定证书吊销模式。</span><span class="sxs-lookup"><span data-stu-id="70d4d-121">Specifies the certificate revocation mode.</span></span> <span data-ttu-id="70d4d-122">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>。</span><span class="sxs-lookup"><span data-stu-id="70d4d-122">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>.</span></span> <span data-ttu-id="70d4d-123">系统通过在吊销证书列表中进行查找来验证对等证书尚未吊销。</span><span class="sxs-lookup"><span data-stu-id="70d4d-123">The system verifies that the peer certificate has not been revoked by looking it up in the revoked certificate list.</span></span> <span data-ttu-id="70d4d-124">可以联机执行该检查，也可以根据缓存的吊销列表执行该检查。</span><span class="sxs-lookup"><span data-stu-id="70d4d-124">This check can be performed either by checking online or against a cached revocation list.</span></span> <span data-ttu-id="70d4d-125">将此属性设置为 NoCheck 可禁用吊销检查。</span><span class="sxs-lookup"><span data-stu-id="70d4d-125">Revocation checking can be turned off by setting this attribute to NoCheck.</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="70d4d-126">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="70d4d-126">Optional enumeration.</span></span> <span data-ttu-id="70d4d-127">指定 WCF 安全系统验证对等证书的受信任存储区位置。</span><span class="sxs-lookup"><span data-stu-id="70d4d-127">Specifies the trusted store location where the peer certificate is validated by the WCF security system.</span></span> <span data-ttu-id="70d4d-128">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.StoreLocation>。</span><span class="sxs-lookup"><span data-stu-id="70d4d-128">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="70d4d-129">子元素</span><span class="sxs-lookup"><span data-stu-id="70d4d-129">Child Elements</span></span>  

 <span data-ttu-id="70d4d-130">无。</span><span class="sxs-lookup"><span data-stu-id="70d4d-130">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="70d4d-131">父元素</span><span class="sxs-lookup"><span data-stu-id="70d4d-131">Parent Elements</span></span>  
  
|<span data-ttu-id="70d4d-132">元素</span><span class="sxs-lookup"><span data-stu-id="70d4d-132">Element</span></span>|<span data-ttu-id="70d4d-133">说明</span><span class="sxs-lookup"><span data-stu-id="70d4d-133">Description</span></span>|  
|-------------|-----------------|  
|[\<peer>](peer-of-servicecredentials.md)|<span data-ttu-id="70d4d-134">指定对等节点的当前凭据。</span><span class="sxs-lookup"><span data-stu-id="70d4d-134">Specifies the current credentials for a peer node.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="70d4d-135">备注</span><span class="sxs-lookup"><span data-stu-id="70d4d-135">Remarks</span></span>  

 <span data-ttu-id="70d4d-136">`<authentication>` 元素与 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> 类相对应。</span><span class="sxs-lookup"><span data-stu-id="70d4d-136">The `<authentication>` element corresponds to the <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> class.</span></span> <span data-ttu-id="70d4d-137">此元素指定一个验证程序，在网格中执行邻居对等身份验证的过程中将调用该验证程序。</span><span class="sxs-lookup"><span data-stu-id="70d4d-137">This element specifies a validator, which is invoked during neighbor-to-neighbor authentication in the mesh.</span></span> <span data-ttu-id="70d4d-138">当新对等方尝试建立邻居连接时，它会将自己的凭据传递到响应的对等方。</span><span class="sxs-lookup"><span data-stu-id="70d4d-138">When a new peer tries to establish a neighbor connection, it passes its own credential to the responding peer.</span></span> <span data-ttu-id="70d4d-139">将调用响应方的验证程序来验证远程方的凭据。</span><span class="sxs-lookup"><span data-stu-id="70d4d-139">The validator of the responder is invoked to verify the credential of the remote party.</span></span> <span data-ttu-id="70d4d-140">每当在网格中建立对等连接时，对等方将会相互进行身份验证，这意味着会同时在两方调用验证程序。</span><span class="sxs-lookup"><span data-stu-id="70d4d-140">Whenever a peer connection is established in the mesh, both peers are mutually authenticated, meaning validators on both ends are invoked.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70d4d-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="70d4d-141">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>
- <xref:System.ServiceModel.Security.PeerCredential.PeerAuthentication%2A>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.PeerAuthentication%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>
- [<span data-ttu-id="70d4d-142">使用证书</span><span class="sxs-lookup"><span data-stu-id="70d4d-142">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="70d4d-143">对等网络</span><span class="sxs-lookup"><span data-stu-id="70d4d-143">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="70d4d-144">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="70d4d-144">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="70d4d-145">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="70d4d-145">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="70d4d-146">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="70d4d-146">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)

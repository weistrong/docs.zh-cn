---
description: 了解详细信息： <peerAuthentication> 元素
title: <peerAuthentication> 元素
ms.date: 03/30/2017
ms.assetid: 09a8a9ff-e395-42f6-8ceb-9d44bdc1cbe1
ms.openlocfilehash: 887b65a4a2a7da9d545bc25636be0ea6c646f6fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683718"
---
# <a name="peerauthentication-element"></a><span data-ttu-id="8a1b6-103">\<peerAuthentication> 元素</span><span class="sxs-lookup"><span data-stu-id="8a1b6-103">\<peerAuthentication> Element</span></span>

<span data-ttu-id="8a1b6-104">指定用于对等客户端的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-104">Specifies authentication options for peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="8a1b6-105">有关对等编程的详细信息，请参阅对等 [网络](../../../wcf/feature-details/peer-to-peer-networking.md)。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-105">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peer>**](peer-of-clientcredentials-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<peerAuthentication>**  
  
## <a name="syntax"></a><span data-ttu-id="8a1b6-106">语法</span><span class="sxs-lookup"><span data-stu-id="8a1b6-106">Syntax</span></span>  
  
```xml  
<peerAuthentication customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"
                    certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"
                    revocationMode="NoCheck/Online/Offline"
                    trustedStoreLocation="CurrentUser/LocalMachine" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8a1b6-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8a1b6-107">Attributes and Elements</span></span>  

 <span data-ttu-id="8a1b6-108">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-108">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8a1b6-109">特性</span><span class="sxs-lookup"><span data-stu-id="8a1b6-109">Attributes</span></span>  
  
|<span data-ttu-id="8a1b6-110">属性</span><span class="sxs-lookup"><span data-stu-id="8a1b6-110">Attribute</span></span>|<span data-ttu-id="8a1b6-111">说明</span><span class="sxs-lookup"><span data-stu-id="8a1b6-111">Description</span></span>|  
|---------------|-----------------|  
|`customCertificateValidatorType`|<span data-ttu-id="8a1b6-112">可选的字符串。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-112">Optional string.</span></span> <span data-ttu-id="8a1b6-113">一个用于验证自定义类型的类型和程序集。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-113">A type and assembly used to validate a custom type.</span></span> <span data-ttu-id="8a1b6-114">当 `certificateValidationMode` 设置为 `Custom` 时，必须设置此属性。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-114">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span>|  
|`certificateValidationMode`|<span data-ttu-id="8a1b6-115">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-115">Optional enumeration.</span></span> <span data-ttu-id="8a1b6-116">指定用来验证凭据的三种模式之一。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-116">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="8a1b6-117">如果设置为 `Custom`，则还必须提供 `customCertificateValidator`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-117">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span> <span data-ttu-id="8a1b6-118">默认值为 `ChainTrust`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-118">The default is `ChainTrust`.</span></span>|  
|`revocationMode`|<span data-ttu-id="8a1b6-119">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-119">Optional enumeration.</span></span> <span data-ttu-id="8a1b6-120">用于检查吊销证书列表 (CRL) 的一种模式。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-120">One of the modes used to check for a revoked certificate lists (CRL).</span></span> <span data-ttu-id="8a1b6-121">默认值为 `Online`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-121">The default is `Online`.</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="8a1b6-122">可选的枚举。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-122">Optional enumeration.</span></span> <span data-ttu-id="8a1b6-123">两个系统存储位置之一：`LocalMachine` 或 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-123">One of the two system store locations: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="8a1b6-124">在向客户端协商服务证书时使用此值。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-124">This value is used when a service certificate is negotiated to the client.</span></span> <span data-ttu-id="8a1b6-125">针对指定存储位置中的 " **受信任人** " 存储执行验证。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-125">Validation is performed against the **Trusted People** store in the specified store location.</span></span> <span data-ttu-id="8a1b6-126">默认值为 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-126">The default is `CurrentUser`.</span></span>|  
  
## <a name="customcertificatevalidatortype-attribute"></a><span data-ttu-id="8a1b6-127">customCertificateValidatorType 属性</span><span class="sxs-lookup"><span data-stu-id="8a1b6-127">customCertificateValidatorType Attribute</span></span>  
  
|<span data-ttu-id="8a1b6-128">值</span><span class="sxs-lookup"><span data-stu-id="8a1b6-128">Value</span></span>|<span data-ttu-id="8a1b6-129">说明</span><span class="sxs-lookup"><span data-stu-id="8a1b6-129">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8a1b6-130">字符串</span><span class="sxs-lookup"><span data-stu-id="8a1b6-130">String</span></span>|<span data-ttu-id="8a1b6-131">指定类型名称和程序集以及用于查找类型的其他数据。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-131">Specifies the type name and assembly and other data used to find the type.</span></span> <span data-ttu-id="8a1b6-132">至少需要命名空间和类型名称。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-132">At minimum, a namespace and type name are required.</span></span> <span data-ttu-id="8a1b6-133">可选信息包括：程序集名称、版本号、区域性和公钥标记。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-133">Optional information includes: assembly name, version number, culture, and public key token.</span></span>|  
  
## <a name="certificatevalidationmode-attribute"></a><span data-ttu-id="8a1b6-134">certificateValidationMode 属性</span><span class="sxs-lookup"><span data-stu-id="8a1b6-134">certificateValidationMode Attribute</span></span>  
  
|<span data-ttu-id="8a1b6-135">值</span><span class="sxs-lookup"><span data-stu-id="8a1b6-135">Value</span></span>|<span data-ttu-id="8a1b6-136">说明</span><span class="sxs-lookup"><span data-stu-id="8a1b6-136">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8a1b6-137">枚举</span><span class="sxs-lookup"><span data-stu-id="8a1b6-137">Enumeration</span></span>|<span data-ttu-id="8a1b6-138">下列值之一：`None`、`PeerTrust`、`ChainTrust`、`PeerOrChainTrust` 和 `Custom`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-138">One of the following values: `None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust`, `Custom`.</span></span> <span data-ttu-id="8a1b6-139">默认值为 `ChainTrust`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-139">The default is `ChainTrust`.</span></span><br /><br /> <span data-ttu-id="8a1b6-140">有关详细信息，请参阅使用 [证书](../../../wcf/feature-details/working-with-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-140">For more information, see [Working with Certificates](../../../wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="revocationmode-attribute"></a><span data-ttu-id="8a1b6-141">revocationMode 属性</span><span class="sxs-lookup"><span data-stu-id="8a1b6-141">revocationMode Attribute</span></span>  
  
|<span data-ttu-id="8a1b6-142">值</span><span class="sxs-lookup"><span data-stu-id="8a1b6-142">Value</span></span>|<span data-ttu-id="8a1b6-143">说明</span><span class="sxs-lookup"><span data-stu-id="8a1b6-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8a1b6-144">枚举</span><span class="sxs-lookup"><span data-stu-id="8a1b6-144">Enumeration</span></span>|<span data-ttu-id="8a1b6-145">下列值之一：`NoCheck`、`Online` 和 `Offline`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-145">One of the following values: `NoCheck`, `Online`, `Offline`.</span></span> <span data-ttu-id="8a1b6-146">默认值为 `Online`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-146">The default is `Online`.</span></span><br /><br /> <span data-ttu-id="8a1b6-147">有关详细信息，请参阅使用 [证书](../../../wcf/feature-details/working-with-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-147">For more information, see [Working with Certificates](../../../wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="trustedstorelocation-attribute"></a><span data-ttu-id="8a1b6-148">trustedStoreLocation 属性</span><span class="sxs-lookup"><span data-stu-id="8a1b6-148">trustedStoreLocation Attribute</span></span>  
  
|<span data-ttu-id="8a1b6-149">值</span><span class="sxs-lookup"><span data-stu-id="8a1b6-149">Value</span></span>|<span data-ttu-id="8a1b6-150">说明</span><span class="sxs-lookup"><span data-stu-id="8a1b6-150">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8a1b6-151">枚举</span><span class="sxs-lookup"><span data-stu-id="8a1b6-151">Enumeration</span></span>|<span data-ttu-id="8a1b6-152">以下值之一：`LocalMachine` 或 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-152">One of the following values: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="8a1b6-153">默认值为 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-153">The default is `CurrentUser`.</span></span> <span data-ttu-id="8a1b6-154">如果客户端应用程序在系统帐户下运行，则证书通常位于 `LocalMachine`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-154">If the client application is running under a system account then the certificate is typically under `LocalMachine`.</span></span> <span data-ttu-id="8a1b6-155">如果客户端应用程序在用户帐户下运行，则证书通常位于 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-155">If the client application is running under a user account then the certificate is typically in `CurrentUser`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8a1b6-156">子元素</span><span class="sxs-lookup"><span data-stu-id="8a1b6-156">Child Elements</span></span>  

 <span data-ttu-id="8a1b6-157">无。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-157">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8a1b6-158">父元素</span><span class="sxs-lookup"><span data-stu-id="8a1b6-158">Parent Elements</span></span>  
  
|<span data-ttu-id="8a1b6-159">元素</span><span class="sxs-lookup"><span data-stu-id="8a1b6-159">Element</span></span>|<span data-ttu-id="8a1b6-160">说明</span><span class="sxs-lookup"><span data-stu-id="8a1b6-160">Description</span></span>|  
|-------------|-----------------|  
|[\<peer>](peer-of-clientcredentials-element.md)|<span data-ttu-id="8a1b6-161">指定一个用于向对等服务证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-161">Specifies a credential used for authenticating the client to a peer service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a1b6-162">备注</span><span class="sxs-lookup"><span data-stu-id="8a1b6-162">Remarks</span></span>  

 <span data-ttu-id="8a1b6-163">`<authentication>` 元素与 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> 类相对应。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-163">The `<authentication>` element corresponds to the <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> class.</span></span> <span data-ttu-id="8a1b6-164">此元素指定一个验证程序，在网格中执行邻居对等身份验证的过程中将调用该验证程序。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-164">This element specifies a validator, which is invoked during neighbor-to-neighbor authentication in the mesh.</span></span> <span data-ttu-id="8a1b6-165">当新对等方尝试建立邻居连接时，它会将自己的凭据传递到响应的对等方。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-165">When a new peer tries to establish a neighbor connection, it passes its own credential to the responding peer.</span></span> <span data-ttu-id="8a1b6-166">将调用响应方的验证程序来验证远程方的凭据。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-166">The validator of the responder is invoked to verify the credential of the remote party.</span></span> <span data-ttu-id="8a1b6-167">每当在网格中建立对等连接时，对等方将会相互进行身份验证，这意味着会同时在两方调用验证程序。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-167">Whenever a peer connection is established in the mesh, both peers are mutually authenticated, meaning validators on both ends are invoked.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8a1b6-168">示例</span><span class="sxs-lookup"><span data-stu-id="8a1b6-168">Example</span></span>  

 <span data-ttu-id="8a1b6-169">下面的代码将证书验证模式设置为 `PeerOrChainTrust`。</span><span class="sxs-lookup"><span data-stu-id="8a1b6-169">The following code sets the certificate validation mode to `PeerOrChainTrust`.</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <peer>
          <certificate findValue="www.contoso.com"
                       storeLocation="LocalMachine"
                       x509FindType="FindByIssuerName" />
          <peerAuthentication certificateValidationMode="PeerOrChainTrust" />
          <messageSenderAuthentication certificateValidationMode="None" />
        </peer>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="8a1b6-170">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a1b6-170">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>
- <xref:System.ServiceModel.Security.PeerCredential.PeerAuthentication%2A>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.PeerAuthentication%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>
- [<span data-ttu-id="8a1b6-171">使用证书</span><span class="sxs-lookup"><span data-stu-id="8a1b6-171">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="8a1b6-172">对等网络</span><span class="sxs-lookup"><span data-stu-id="8a1b6-172">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="8a1b6-173">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="8a1b6-173">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="8a1b6-174">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="8a1b6-174">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="8a1b6-175">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="8a1b6-175">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)

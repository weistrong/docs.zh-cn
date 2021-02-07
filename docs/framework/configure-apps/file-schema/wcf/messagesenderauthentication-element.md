---
description: 了解详细信息： <messageSenderAuthentication> 元素
title: <messageSenderAuthentication> 元素
ms.date: 03/30/2017
ms.assetid: 8d979dfc-a6f9-42ec-96d5-7fbc13a48118
ms.openlocfilehash: 03c1cd626e7c3ad71026c076df3d757419810d74
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749332"
---
# <a name="messagesenderauthentication-element"></a><span data-ttu-id="a3157-103">\<messageSenderAuthentication> 元素</span><span class="sxs-lookup"><span data-stu-id="a3157-103">\<messageSenderAuthentication> element</span></span>

<span data-ttu-id="a3157-104">指定用于对等消息发送方的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="a3157-104">Specifies authentication options for peer-to-peer message senders.</span></span>  
  
 <span data-ttu-id="a3157-105">有关对等编程的详细信息，请参阅对等 [网络](../../../wcf/feature-details/peer-to-peer-networking.md)。</span><span class="sxs-lookup"><span data-stu-id="a3157-105">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peer>**](peer-of-clientcredentials-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<messageSenderAuthentication>**  
  
## <a name="syntax"></a><span data-ttu-id="a3157-106">语法</span><span class="sxs-lookup"><span data-stu-id="a3157-106">Syntax</span></span>  
  
```xml  
<messageSenderAuthentication customCertificateValidatorType= "namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"
                             certificateValidationMode = "ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"
                             revocationMode="NoCheck/Online/Offline"
                             trustedStoreLocation="CurrentUser/LocalMachine" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a3157-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a3157-107">Attributes and Elements</span></span>  

 <span data-ttu-id="a3157-108">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a3157-108">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a3157-109">特性</span><span class="sxs-lookup"><span data-stu-id="a3157-109">Attributes</span></span>  
  
|<span data-ttu-id="a3157-110">属性</span><span class="sxs-lookup"><span data-stu-id="a3157-110">Attribute</span></span>|<span data-ttu-id="a3157-111">说明</span><span class="sxs-lookup"><span data-stu-id="a3157-111">Description</span></span>|  
|---------------|-----------------|  
|`customCertificateValidatorType`|<span data-ttu-id="a3157-112">一个用于验证自定义类型的类型和程序集。</span><span class="sxs-lookup"><span data-stu-id="a3157-112">A type and assembly used to validate a custom type.</span></span> <span data-ttu-id="a3157-113">当 `certificateValidationMode` 设置为 `Custom` 时，必须设置此属性。</span><span class="sxs-lookup"><span data-stu-id="a3157-113">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span>|  
|`certificateValidationMode`|<span data-ttu-id="a3157-114">指定用来验证凭据的三种模式之一。</span><span class="sxs-lookup"><span data-stu-id="a3157-114">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="a3157-115">如果设置为 `Custom`，则还必须提供 `customCertificateValidator`。</span><span class="sxs-lookup"><span data-stu-id="a3157-115">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|`revocationMode`|<span data-ttu-id="a3157-116">用于检查吊销证书列表 (CRL) 的一种模式。</span><span class="sxs-lookup"><span data-stu-id="a3157-116">One of the modes used to check for a revoked certificate lists (CRL).</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="a3157-117">两个系统存储位置之一：`LocalMachine` 或 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="a3157-117">One of the two system store locations: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="a3157-118">在向客户端协商服务证书时使用此值。</span><span class="sxs-lookup"><span data-stu-id="a3157-118">This value is used when a service certificate is negotiated to the client.</span></span> <span data-ttu-id="a3157-119">针对指定存储位置中的 " **受信任人** " 存储执行验证。</span><span class="sxs-lookup"><span data-stu-id="a3157-119">Validation is performed against the **Trusted People** store in the specified store location.</span></span>|  
  
## <a name="customcertificatevalidatortype-attribute"></a><span data-ttu-id="a3157-120">customCertificateValidatorType 属性</span><span class="sxs-lookup"><span data-stu-id="a3157-120">customCertificateValidatorType Attribute</span></span>  
  
|<span data-ttu-id="a3157-121">值</span><span class="sxs-lookup"><span data-stu-id="a3157-121">Value</span></span>|<span data-ttu-id="a3157-122">说明</span><span class="sxs-lookup"><span data-stu-id="a3157-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a3157-123">字符串</span><span class="sxs-lookup"><span data-stu-id="a3157-123">String</span></span>|<span data-ttu-id="a3157-124">可选。</span><span class="sxs-lookup"><span data-stu-id="a3157-124">Optional.</span></span> <span data-ttu-id="a3157-125">指定类型名称和程序集以及用于查找类型的其他数据。</span><span class="sxs-lookup"><span data-stu-id="a3157-125">Specifies the type name and assembly and other data used to find the type.</span></span> <span data-ttu-id="a3157-126">至少需要命名空间和类型名称。</span><span class="sxs-lookup"><span data-stu-id="a3157-126">At minimum, a namespace and type name are required.</span></span> <span data-ttu-id="a3157-127">可选信息包括：程序集名称、版本号、区域性和公钥标记。</span><span class="sxs-lookup"><span data-stu-id="a3157-127">Optional information includes: assembly name, version number, culture, and public key token.</span></span>|  
  
## <a name="certificatevalidationmode-attribute"></a><span data-ttu-id="a3157-128">certificateValidationMode 属性</span><span class="sxs-lookup"><span data-stu-id="a3157-128">certificateValidationMode Attribute</span></span>  
  
|<span data-ttu-id="a3157-129">值</span><span class="sxs-lookup"><span data-stu-id="a3157-129">Value</span></span>|<span data-ttu-id="a3157-130">说明</span><span class="sxs-lookup"><span data-stu-id="a3157-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a3157-131">枚举</span><span class="sxs-lookup"><span data-stu-id="a3157-131">Enumeration</span></span>|<span data-ttu-id="a3157-132">可选。</span><span class="sxs-lookup"><span data-stu-id="a3157-132">Optional.</span></span> <span data-ttu-id="a3157-133">下列值之一：`None`、`PeerTrust`、`ChainTrust`、`PeerOrChainTrust` 和 `Custom`。</span><span class="sxs-lookup"><span data-stu-id="a3157-133">One of the following values: `None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust`, `Custom`.</span></span> <span data-ttu-id="a3157-134">默认值为 `ChainTrust`。</span><span class="sxs-lookup"><span data-stu-id="a3157-134">The default is `ChainTrust`.</span></span> <span data-ttu-id="a3157-135">默认值为 `ChainTrust`。</span><span class="sxs-lookup"><span data-stu-id="a3157-135">The default is `ChainTrust`.</span></span><br /><br /> <span data-ttu-id="a3157-136">有关详细信息，请参阅使用 [证书](../../../wcf/feature-details/working-with-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="a3157-136">For more information, see [Working with Certificates](../../../wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="revocationmode-attribute"></a><span data-ttu-id="a3157-137">revocationMode 属性</span><span class="sxs-lookup"><span data-stu-id="a3157-137">revocationMode Attribute</span></span>  
  
|<span data-ttu-id="a3157-138">值</span><span class="sxs-lookup"><span data-stu-id="a3157-138">Value</span></span>|<span data-ttu-id="a3157-139">说明</span><span class="sxs-lookup"><span data-stu-id="a3157-139">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a3157-140">枚举</span><span class="sxs-lookup"><span data-stu-id="a3157-140">Enumeration</span></span>|<span data-ttu-id="a3157-141">下列值之一：`NoCheck`、`Online` 和 `Offline`。</span><span class="sxs-lookup"><span data-stu-id="a3157-141">One of the following values: `NoCheck`, `Online`, `Offline`.</span></span> <span data-ttu-id="a3157-142">默认值为 `Online`。</span><span class="sxs-lookup"><span data-stu-id="a3157-142">The default is `Online`.</span></span><br /><br /> <span data-ttu-id="a3157-143">有关详细信息，请参阅使用 [证书](../../../wcf/feature-details/working-with-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="a3157-143">For more information, see [Working with Certificates](../../../wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="trustedstorelocation-attribute"></a><span data-ttu-id="a3157-144">trustedStoreLocation 属性</span><span class="sxs-lookup"><span data-stu-id="a3157-144">trustedStoreLocation Attribute</span></span>  
  
|<span data-ttu-id="a3157-145">值</span><span class="sxs-lookup"><span data-stu-id="a3157-145">Value</span></span>|<span data-ttu-id="a3157-146">说明</span><span class="sxs-lookup"><span data-stu-id="a3157-146">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a3157-147">枚举</span><span class="sxs-lookup"><span data-stu-id="a3157-147">Enumeration</span></span>|<span data-ttu-id="a3157-148">以下值之一：`LocalMachine` 或 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="a3157-148">One of the following values: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="a3157-149">默认值为 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="a3157-149">The default is `CurrentUser`.</span></span> <span data-ttu-id="a3157-150">如果客户端应用程序在系统帐户下运行，则证书通常位于 `LocalMachine`。</span><span class="sxs-lookup"><span data-stu-id="a3157-150">If the client application is running under a system account then the certificate is typically under `LocalMachine`.</span></span> <span data-ttu-id="a3157-151">如果客户端应用程序在用户帐户下运行，则证书通常位于 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="a3157-151">If the client application is running under a user account then the certificate is typically in `CurrentUser`.</span></span> <span data-ttu-id="a3157-152">默认值为 `CurrentUser`。</span><span class="sxs-lookup"><span data-stu-id="a3157-152">The default is `CurrentUser`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a3157-153">子元素</span><span class="sxs-lookup"><span data-stu-id="a3157-153">Child Elements</span></span>  

 <span data-ttu-id="a3157-154">无。</span><span class="sxs-lookup"><span data-stu-id="a3157-154">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a3157-155">父元素</span><span class="sxs-lookup"><span data-stu-id="a3157-155">Parent Elements</span></span>  
  
|<span data-ttu-id="a3157-156">元素</span><span class="sxs-lookup"><span data-stu-id="a3157-156">Element</span></span>|<span data-ttu-id="a3157-157">说明</span><span class="sxs-lookup"><span data-stu-id="a3157-157">Description</span></span>|  
|-------------|-----------------|  
|[\<peer>](peer-of-clientcredentials-element.md)|<span data-ttu-id="a3157-158">指定一个用于向对等服务证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="a3157-158">Specifies a credential used for authenticating the client to a peer service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a3157-159">备注</span><span class="sxs-lookup"><span data-stu-id="a3157-159">Remarks</span></span>  

 <span data-ttu-id="a3157-160">如果选择了消息身份验证，则必须配置此元素。</span><span class="sxs-lookup"><span data-stu-id="a3157-160">This element must be configured if message authentication is chosen.</span></span> <span data-ttu-id="a3157-161">对于输出通道，每条消息都使用提供的证书进行签名 [\<certificate>](certificate-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="a3157-161">For output channels, each message is signed using the certificate provided by [\<certificate>](certificate-element.md).</span></span> <span data-ttu-id="a3157-162">在将任一消息传递到应用程序之前，都会使用由此元素的 `customCertificateValidatorType` 属性指定的验证程序对照消息凭据对其进行检查。</span><span class="sxs-lookup"><span data-stu-id="a3157-162">All messages, before delivered to the application, are checked against the message credential using the validator specified by the `customCertificateValidatorType` attribute of this element.</span></span> <span data-ttu-id="a3157-163">验证程序可以接受或拒绝凭据。</span><span class="sxs-lookup"><span data-stu-id="a3157-163">The validator can either accept or reject the credential.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3157-164">示例</span><span class="sxs-lookup"><span data-stu-id="a3157-164">Example</span></span>  

 <span data-ttu-id="a3157-165">下面的代码将消息发送方验证模式设置为 `PeerOrChainTrust`。</span><span class="sxs-lookup"><span data-stu-id="a3157-165">The following code sets the message sender validation mode to `PeerOrChainTrust`.</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <peer>
          <certificate findValue="www.contoso.com"
                       storeLocation="LocalMachine"
                       x509FindType="FindByIssuerName" />
          <messageSenderAuthentication certificateValidationMode="PeerOrChainTrust" />
          <messageSenderAuthentication certificateValidationMode="None" />
        </peer>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="a3157-166">请参阅</span><span class="sxs-lookup"><span data-stu-id="a3157-166">See also</span></span>

- <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>
- <xref:System.ServiceModel.Security.PeerCredential.MessageSenderAuthentication%2A>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.MessageSenderAuthentication%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>
- [<span data-ttu-id="a3157-167">使用证书</span><span class="sxs-lookup"><span data-stu-id="a3157-167">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="a3157-168">对等网络</span><span class="sxs-lookup"><span data-stu-id="a3157-168">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="a3157-169">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a3157-169">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="a3157-170">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a3157-170">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="a3157-171">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="a3157-171">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)

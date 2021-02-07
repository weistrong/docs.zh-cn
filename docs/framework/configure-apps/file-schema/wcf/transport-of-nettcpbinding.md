---
description: 了解详细 <transport> 信息： <netTcpBinding>
title: <transport> 的 <netTcpBinding>
ms.date: 03/30/2017
ms.assetid: 49462e0a-66e1-463f-b3e1-c83a441673c6
ms.openlocfilehash: 9005de300b41c9f53c62875ee185d0f8a3ee8d7f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664543"
---
# <a name="transport-of-nettcpbinding"></a><span data-ttu-id="9948e-103">\<transport> 的 \<netTcpBinding></span><span class="sxs-lookup"><span data-stu-id="9948e-103">\<transport> of \<netTcpBinding></span></span>

<span data-ttu-id="9948e-104">为使用配置的终结点定义消息级安全性要求的类型 [\<netTcpBinding>](nettcpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="9948e-104">Defines the type of message-level security requirements for an endpoint configured with the [\<netTcpBinding>](nettcpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netTcpBinding>**](nettcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-nettcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="9948e-105">语法</span><span class="sxs-lookup"><span data-stu-id="9948e-105">Syntax</span></span>  
  
```xml  
<netTcpBinding>
  <binding>
    <security mode="None|Transport|Message|TransportWithMessageCredential">
      <transport clientCredentialType="None|Windows|Certificate"
                 protectionLevel="None|Sign|EncryptAndSign"
                 sslProtocols="Tls|Tls11|Tls12">
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</netTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9948e-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9948e-106">Attributes and Elements</span></span>  

 <span data-ttu-id="9948e-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9948e-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9948e-108">特性</span><span class="sxs-lookup"><span data-stu-id="9948e-108">Attributes</span></span>  
  
|<span data-ttu-id="9948e-109">属性</span><span class="sxs-lookup"><span data-stu-id="9948e-109">Attribute</span></span>|<span data-ttu-id="9948e-110">说明</span><span class="sxs-lookup"><span data-stu-id="9948e-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9948e-111">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="9948e-111">clientCredentialType</span></span>|<span data-ttu-id="9948e-112">可选。</span><span class="sxs-lookup"><span data-stu-id="9948e-112">Optional.</span></span> <span data-ttu-id="9948e-113">指定要在使用传输安全性执行客户端身份验证时使用的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="9948e-113">Specifies the type of credential to be used when performing client authentication using Transport security.</span></span><br /><br /> <span data-ttu-id="9948e-114">-默认值为 `Windows` 。</span><span class="sxs-lookup"><span data-stu-id="9948e-114">-   The default value is `Windows`.</span></span><br /><span data-ttu-id="9948e-115">-此属性的类型为 <xref:System.ServiceModel.TcpClientCredentialType> 。</span><span class="sxs-lookup"><span data-stu-id="9948e-115">-   This attribute is of type <xref:System.ServiceModel.TcpClientCredentialType>.</span></span>|  
|<span data-ttu-id="9948e-116">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="9948e-116">protectionLevel</span></span>|<span data-ttu-id="9948e-117">可选。</span><span class="sxs-lookup"><span data-stu-id="9948e-117">Optional.</span></span> <span data-ttu-id="9948e-118">定义 TCP 传输级别的安全性。</span><span class="sxs-lookup"><span data-stu-id="9948e-118">Defines security at the level of the TCP transport.</span></span> <span data-ttu-id="9948e-119">消息签名降低了在消息传输过程中第三方对消息进行篡改的风险。</span><span class="sxs-lookup"><span data-stu-id="9948e-119">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="9948e-120">加密为传输过程提供了数据级保密功能。</span><span class="sxs-lookup"><span data-stu-id="9948e-120">Encryption provides data-level privacy during transport.</span></span><br /><br /> <span data-ttu-id="9948e-121">默认值是 `EncryptAndSign`。</span><span class="sxs-lookup"><span data-stu-id="9948e-121">The default value is `EncryptAndSign`.</span></span>|  
|<span data-ttu-id="9948e-122">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="9948e-122">sslProtocols</span></span>|<span data-ttu-id="9948e-123">指定支持哪些 SslProtocols 的 SslProtocols 枚举标志值。</span><span class="sxs-lookup"><span data-stu-id="9948e-123">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="9948e-124">默认值为 Tls&#124;Tls11&#124;Tls12。</span><span class="sxs-lookup"><span data-stu-id="9948e-124">The default is Tls&#124;Tls11&#124;Tls12.</span></span>|  
|<span data-ttu-id="9948e-125">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="9948e-125">policyEnforcement</span></span>|<span data-ttu-id="9948e-126">此枚举指定应何时强制实施 <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy>。</span><span class="sxs-lookup"><span data-stu-id="9948e-126">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="9948e-127">1. 从不–不会强制实施策略 (禁用扩展保护) 。</span><span class="sxs-lookup"><span data-stu-id="9948e-127">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="9948e-128">WhenSupported-仅当客户端支持扩展保护时才强制实施策略。</span><span class="sxs-lookup"><span data-stu-id="9948e-128">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="9948e-129">3. always –始终强制实施策略。</span><span class="sxs-lookup"><span data-stu-id="9948e-129">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="9948e-130">不支持扩展保护的客户端将无法进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="9948e-130">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="9948e-131">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="9948e-131">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="9948e-132">值</span><span class="sxs-lookup"><span data-stu-id="9948e-132">Value</span></span>|<span data-ttu-id="9948e-133">说明</span><span class="sxs-lookup"><span data-stu-id="9948e-133">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="9948e-134">无</span><span class="sxs-lookup"><span data-stu-id="9948e-134">None</span></span>|<span data-ttu-id="9948e-135">客户端为匿名客户端。</span><span class="sxs-lookup"><span data-stu-id="9948e-135">The client is anonymous.</span></span> <span data-ttu-id="9948e-136">这需要服务证书。</span><span class="sxs-lookup"><span data-stu-id="9948e-136">This requires a certificate for the service.</span></span>|  
|<span data-ttu-id="9948e-137">Windows</span><span class="sxs-lookup"><span data-stu-id="9948e-137">Windows</span></span>|<span data-ttu-id="9948e-138">指定使用 SP 协商（Kerberos 协商）进行客户端 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="9948e-138">Specifies Windows authentication of the client using SP Negotiation (Kerberos negotiation).</span></span>|  
|<span data-ttu-id="9948e-139">证书</span><span class="sxs-lookup"><span data-stu-id="9948e-139">Certificate</span></span>|<span data-ttu-id="9948e-140">使用证书进行对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="9948e-140">The client is authenticated using a certificate.</span></span> <span data-ttu-id="9948e-141">这使用 SSL 协商并需要服务证书。</span><span class="sxs-lookup"><span data-stu-id="9948e-141">This uses SSL Negotiation and requires a certificate for the service.</span></span>|  
  
## <a name="protectionlevel-attribute"></a><span data-ttu-id="9948e-142">protectionLevel 属性</span><span class="sxs-lookup"><span data-stu-id="9948e-142">protectionLevel Attribute</span></span>  
  
|<span data-ttu-id="9948e-143">值</span><span class="sxs-lookup"><span data-stu-id="9948e-143">Value</span></span>|<span data-ttu-id="9948e-144">说明</span><span class="sxs-lookup"><span data-stu-id="9948e-144">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="9948e-145">无</span><span class="sxs-lookup"><span data-stu-id="9948e-145">None</span></span>|<span data-ttu-id="9948e-146">无保护。</span><span class="sxs-lookup"><span data-stu-id="9948e-146">No protection.</span></span>|  
|<span data-ttu-id="9948e-147">Sign</span><span class="sxs-lookup"><span data-stu-id="9948e-147">Sign</span></span>|<span data-ttu-id="9948e-148">对消息进行签名。</span><span class="sxs-lookup"><span data-stu-id="9948e-148">Messages are signed.</span></span>|  
|<span data-ttu-id="9948e-149">EncryptAndSign</span><span class="sxs-lookup"><span data-stu-id="9948e-149">EncryptAndSign</span></span>|<span data-ttu-id="9948e-150">-对消息进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="9948e-150">-   Messages are encrypted and signed.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9948e-151">子元素</span><span class="sxs-lookup"><span data-stu-id="9948e-151">Child Elements</span></span>  

 <span data-ttu-id="9948e-152">无</span><span class="sxs-lookup"><span data-stu-id="9948e-152">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9948e-153">父元素</span><span class="sxs-lookup"><span data-stu-id="9948e-153">Parent Elements</span></span>  
  
|<span data-ttu-id="9948e-154">元素</span><span class="sxs-lookup"><span data-stu-id="9948e-154">Element</span></span>|<span data-ttu-id="9948e-155">说明</span><span class="sxs-lookup"><span data-stu-id="9948e-155">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-nettcpbinding.md)|<span data-ttu-id="9948e-156">指定的安全功能 [\<netTcpBinding>](nettcpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="9948e-156">Specifies the security capabilities of the [\<netTcpBinding>](nettcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9948e-157">备注</span><span class="sxs-lookup"><span data-stu-id="9948e-157">Remarks</span></span>  

 <span data-ttu-id="9948e-158">使用传输安全性以获得 SOAP 消息的完整性和保密性以及相互身份验证。</span><span class="sxs-lookup"><span data-stu-id="9948e-158">Use Transport security for integrity and confidentiality of the SOAP message and for mutual authentication.</span></span> <span data-ttu-id="9948e-159">如果在绑定上选择此安全模式，则使用安全传输配置信道栈，并且使用传输安全性（如 Windows (Negotiate) 或 SSLL）保护 SOAP 消息安全通过 TCP 传递。</span><span class="sxs-lookup"><span data-stu-id="9948e-159">If this security mode is selected on a binding, the channel stack is configured using a secure transport and the SOAP messages are secured using transport security such as Windows (Negotiate) or SSL over TCP.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9948e-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="9948e-160">See also</span></span>

- <xref:System.ServiceModel.TcpTransportSecurity>
- <xref:System.ServiceModel.Configuration.NetTcpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.NetTcpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.NetTcpSecurityElement>
- [<span data-ttu-id="9948e-161">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="9948e-161">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="9948e-162">绑定</span><span class="sxs-lookup"><span data-stu-id="9948e-162">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="9948e-163">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="9948e-163">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="9948e-164">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="9948e-164">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

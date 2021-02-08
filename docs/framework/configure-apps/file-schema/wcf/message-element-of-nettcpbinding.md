---
description: 详细了解： <message> 的元素 <netTcpBinding>
title: <message> 的元素 <netTcpBinding>
ms.date: 03/30/2017
ms.assetid: 1d71edd9-c085-4c2e-b6d3-980c313366f9
ms.openlocfilehash: 10c1f2897bc880ca1f328b546357d3cf7cdb26a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802172"
---
# <a name="message-element-of-nettcpbinding"></a><span data-ttu-id="fcef2-103">\<message> 的元素 \<netTcpBinding></span><span class="sxs-lookup"><span data-stu-id="fcef2-103">\<message> element of \<netTcpBinding></span></span>

<span data-ttu-id="fcef2-104">为使用配置的终结点定义消息级安全性要求的类型 [\<netTcpBinding>](nettcpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="fcef2-104">Defines the type of message-level security requirements for an endpoint configured with the [\<netTcpBinding>](nettcpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netTcpBinding>**](nettcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-nettcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<message>**  
  
## <a name="syntax"></a><span data-ttu-id="fcef2-105">语法</span><span class="sxs-lookup"><span data-stu-id="fcef2-105">Syntax</span></span>  
  
```xml  
<message algorithmSuite="System.Servicemodel.Security.SecurityAlgorithmsuite"
         clientCredentialType="None/Windows/UserName/Certificate/IssuedToken" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fcef2-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="fcef2-106">Attributes and Elements</span></span>  

 <span data-ttu-id="fcef2-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fcef2-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fcef2-108">特性</span><span class="sxs-lookup"><span data-stu-id="fcef2-108">Attributes</span></span>  
  
|<span data-ttu-id="fcef2-109">属性</span><span class="sxs-lookup"><span data-stu-id="fcef2-109">Attribute</span></span>|<span data-ttu-id="fcef2-110">说明</span><span class="sxs-lookup"><span data-stu-id="fcef2-110">Description</span></span>|  
|---------------|-----------------|  
|`algorithmSuite`|<span data-ttu-id="fcef2-111">设置消息加密和密钥包装算法。</span><span class="sxs-lookup"><span data-stu-id="fcef2-111">Sets the message encryption and key-wrap algorithms.</span></span> <span data-ttu-id="fcef2-112">算法和密钥大小由 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> 类确定。</span><span class="sxs-lookup"><span data-stu-id="fcef2-112">The algorithms and the key sizes are determined by the <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> class.</span></span> <span data-ttu-id="fcef2-113">这些算法与“安全策略语言”(WS-SecurityPolicy) 规范中指定的算法一致。</span><span class="sxs-lookup"><span data-stu-id="fcef2-113">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span><br /><br /> <span data-ttu-id="fcef2-114">下表中显示了可能的值。</span><span class="sxs-lookup"><span data-stu-id="fcef2-114">Possible values are shown in the following table.</span></span> <span data-ttu-id="fcef2-115">默认值是 `Basic256`。</span><span class="sxs-lookup"><span data-stu-id="fcef2-115">The default value is `Basic256`.</span></span><br /><br /> <span data-ttu-id="fcef2-116">如果服务绑定指定的 `algorithmSuite` 值不等于默认值，并且你使用 Svcutil.exe 生成配置文件，则不会正确生成该文件，你必须手动编辑此配置文件，将此属性设置为所需的值。</span><span class="sxs-lookup"><span data-stu-id="fcef2-116">If the service binding specifies an `algorithmSuite` value that is not equal to the default, and you generate the configuration file using Svcutil.exe, then it is not generated correctly, and you must manually edit the configuration file to set this attribute to the desired value.</span></span>|  
|`clientCredentialType`|<span data-ttu-id="fcef2-117">指定要在使用基于消息的安全性执行客户端身份验证时使用的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="fcef2-117">Specifies the type of credential to be used when performing client authentication using Message-based security.</span></span> <span data-ttu-id="fcef2-118">下表中显示了可能的值。</span><span class="sxs-lookup"><span data-stu-id="fcef2-118">Possible values are shown in the following table.</span></span> <span data-ttu-id="fcef2-119">默认值是 `UserName`。</span><span class="sxs-lookup"><span data-stu-id="fcef2-119">The default value is `UserName`.</span></span> <span data-ttu-id="fcef2-120">此属性的类型为 <xref:System.ServiceModel.MessageCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="fcef2-120">This attribute is of type <xref:System.ServiceModel.MessageCredentialType>.</span></span>|  
  
## <a name="algorithmsuite-attribute"></a><span data-ttu-id="fcef2-121">algorithmSuite 属性</span><span class="sxs-lookup"><span data-stu-id="fcef2-121">algorithmSuite Attribute</span></span>  
  
|<span data-ttu-id="fcef2-122">值</span><span class="sxs-lookup"><span data-stu-id="fcef2-122">Value</span></span>|<span data-ttu-id="fcef2-123">说明</span><span class="sxs-lookup"><span data-stu-id="fcef2-123">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="fcef2-124">Basic128</span><span class="sxs-lookup"><span data-stu-id="fcef2-124">Basic128</span></span>|<span data-ttu-id="fcef2-125">使用 Aes128 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-125">Use Aes128 encryption, Sha1 for message digest, and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-126">Basic192</span><span class="sxs-lookup"><span data-stu-id="fcef2-126">Basic192</span></span>|<span data-ttu-id="fcef2-127">使用 Aes192 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-127">Use Aes192 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-128">Basic256</span><span class="sxs-lookup"><span data-stu-id="fcef2-128">Basic256</span></span>|<span data-ttu-id="fcef2-129">使用 Aes256 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-129">Use Aes256 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-130">Basic256Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-130">Basic256Rsa15</span></span>|<span data-ttu-id="fcef2-131">对消息加密使用 Aes256，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-131">Use Aes256 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-132">Basic192Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-132">Basic192Rsa15</span></span>|<span data-ttu-id="fcef2-133">对消息加密使用 Aes192，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-133">Use Aes192 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-134">TripleDes</span><span class="sxs-lookup"><span data-stu-id="fcef2-134">TripleDes</span></span>|<span data-ttu-id="fcef2-135">使用 TripleDes 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-135">Use TripleDes encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-136">Basic128Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-136">Basic128Rsa15</span></span>|<span data-ttu-id="fcef2-137">对消息加密使用 Aes128，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-137">Use Aes128 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-138">TripleDesRsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-138">TripleDesRsa15</span></span>|<span data-ttu-id="fcef2-139">使用 TripleDes 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-139">Use TripleDes encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-140">Basic128Sha256</span><span class="sxs-lookup"><span data-stu-id="fcef2-140">Basic128Sha256</span></span>|<span data-ttu-id="fcef2-141">对消息加密使用 Aes256，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-141">Use Aes256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-142">Basic192Sha256</span><span class="sxs-lookup"><span data-stu-id="fcef2-142">Basic192Sha256</span></span>|<span data-ttu-id="fcef2-143">对消息加密使用 Aes192，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-143">Use Aes192 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-144">Basic256Sha256</span><span class="sxs-lookup"><span data-stu-id="fcef2-144">Basic256Sha256</span></span>|<span data-ttu-id="fcef2-145">对消息加密使用 Aes256，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-145">Use Aes256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-146">TripleDesSha256</span><span class="sxs-lookup"><span data-stu-id="fcef2-146">TripleDesSha256</span></span>|<span data-ttu-id="fcef2-147">对消息加密使用 TripleDes，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="fcef2-147">Use TripleDes for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-148">Basic128Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-148">Basic128Sha256Rsa15</span></span>|<span data-ttu-id="fcef2-149">对消息加密使用 Aes128，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-149">Use Aes128 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-150">Basic192Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-150">Basic192Sha256Rsa15</span></span>|<span data-ttu-id="fcef2-151">对消息加密使用 Aes192，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-151">Use Aes192 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-152">Basic256Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-152">Basic256Sha256Rsa15</span></span>|<span data-ttu-id="fcef2-153">对消息加密使用 Aes256，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-153">Use Aes256 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="fcef2-154">TripleDesSha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="fcef2-154">TripleDesSha256Rsa15</span></span>|<span data-ttu-id="fcef2-155">对消息加密使用 TripleDes，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="fcef2-155">Use TripleDes for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="fcef2-156">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="fcef2-156">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="fcef2-157">值</span><span class="sxs-lookup"><span data-stu-id="fcef2-157">Value</span></span>|<span data-ttu-id="fcef2-158">说明</span><span class="sxs-lookup"><span data-stu-id="fcef2-158">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="fcef2-159">无</span><span class="sxs-lookup"><span data-stu-id="fcef2-159">None</span></span>|<span data-ttu-id="fcef2-160">允许服务与匿名客户端交互。</span><span class="sxs-lookup"><span data-stu-id="fcef2-160">This allows the service to interact with anonymous clients.</span></span> <span data-ttu-id="fcef2-161">对于服务，这表示服务不需要任何客户端凭据。</span><span class="sxs-lookup"><span data-stu-id="fcef2-161">On the service, this indicates that the service does not require any client credential.</span></span> <span data-ttu-id="fcef2-162">对于客户端，这表示客户端不提供任何客户端凭据。</span><span class="sxs-lookup"><span data-stu-id="fcef2-162">On the client, this indicates that the client does not provide any client credential.</span></span>|  
|<span data-ttu-id="fcef2-163">Windows</span><span class="sxs-lookup"><span data-stu-id="fcef2-163">Windows</span></span>|<span data-ttu-id="fcef2-164">允许 SOAP 交换在已通过身份验证的 Windows 凭据上下文中执行。</span><span class="sxs-lookup"><span data-stu-id="fcef2-164">Allows the SOAP exchanges to be under the authenticated context of a Windows credential.</span></span>|  
|<span data-ttu-id="fcef2-165">UserName</span><span class="sxs-lookup"><span data-stu-id="fcef2-165">UserName</span></span>|<span data-ttu-id="fcef2-166">允许服务要求使用 UserName 凭据对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="fcef2-166">Allows the service to require that the client be authenticated using a UserName credential.</span></span> <span data-ttu-id="fcef2-167">WCF 不支持发送密码摘要，也不支持使用密码派生密钥，然后用这些密钥来确保消息的安全性。</span><span class="sxs-lookup"><span data-stu-id="fcef2-167">WCF does not support sending a password digest or deriving keys using password and using such keys for message security.</span></span> <span data-ttu-id="fcef2-168">因此，在使用用户名凭据时，WCF 会强制保护传输。</span><span class="sxs-lookup"><span data-stu-id="fcef2-168">As such, WCF enforces that the transport is secured when using UserName credentials.</span></span> <span data-ttu-id="fcef2-169">这种凭据模式将产生可互操作的交换或不可互操作的协商，具体取决于 `negotiateServiceCredential` 属性。</span><span class="sxs-lookup"><span data-stu-id="fcef2-169">This credential mode results in either an interoperable exchange or a non-interoperable negotiation based on the `negotiateServiceCredential` attribute.</span></span>|  
|<span data-ttu-id="fcef2-170">证书</span><span class="sxs-lookup"><span data-stu-id="fcef2-170">Certificate</span></span>|<span data-ttu-id="fcef2-171">允许服务要求使用证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="fcef2-171">Allows the service to require that the client be authenticated using a certificate.</span></span> <span data-ttu-id="fcef2-172">如果使用消息安全模式并且将 `negotiateServiceCredential` 属性设置为 `false`，则必须向客户端提供服务证书。</span><span class="sxs-lookup"><span data-stu-id="fcef2-172">If message security mode is used and the `negotiateServiceCredential` attribute is set to `false`, the client must be provisioned with the service certificate.</span></span>|  
|<span data-ttu-id="fcef2-173">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="fcef2-173">IssuedToken</span></span>|<span data-ttu-id="fcef2-174">指定自定义令牌，该令牌通常由安全令牌服务 (STS) 颁发。</span><span class="sxs-lookup"><span data-stu-id="fcef2-174">Specifies a custom token, usually issued by a Security Token Service (STS).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fcef2-175">子元素</span><span class="sxs-lookup"><span data-stu-id="fcef2-175">Child Elements</span></span>  

 <span data-ttu-id="fcef2-176">无</span><span class="sxs-lookup"><span data-stu-id="fcef2-176">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fcef2-177">父元素</span><span class="sxs-lookup"><span data-stu-id="fcef2-177">Parent Elements</span></span>  
  
|<span data-ttu-id="fcef2-178">元素</span><span class="sxs-lookup"><span data-stu-id="fcef2-178">Element</span></span>|<span data-ttu-id="fcef2-179">说明</span><span class="sxs-lookup"><span data-stu-id="fcef2-179">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-nettcpbinding.md)|<span data-ttu-id="fcef2-180">定义 <xref:System.ServiceModel.Configuration.NetTcpBindingElement>的安全功能。</span><span class="sxs-lookup"><span data-stu-id="fcef2-180">Defines the security capabilities for the <xref:System.ServiceModel.Configuration.NetTcpBindingElement>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fcef2-181">备注</span><span class="sxs-lookup"><span data-stu-id="fcef2-181">Remarks</span></span>  

 <span data-ttu-id="fcef2-182">消息使用消息级安全性实现 SOAP 消息的完整性和保密性，还用于通信对等方的相互身份验证。</span><span class="sxs-lookup"><span data-stu-id="fcef2-182">Message uses message-level security for the integrity and confidentiality of the SOAP message, and for mutual authentication of the communication peers.</span></span> <span data-ttu-id="fcef2-183">如果在绑定上选择此安全模式，则使用消息安全性绑定元素配置信道堆栈，并且 SOAP 消息可按照 WS-Security\* 标准进行保护。</span><span class="sxs-lookup"><span data-stu-id="fcef2-183">If this security mode is selected on a binding, the channel stack is configured with message security binding elements and the SOAP messages are secured in compliance with WS-Security\* standards.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcef2-184">请参阅</span><span class="sxs-lookup"><span data-stu-id="fcef2-184">See also</span></span>

- <xref:System.ServiceModel.MessageSecurityOverTcp>
- <xref:System.ServiceModel.Configuration.NetTcpSecurityElement.Message%2A>
- <xref:System.ServiceModel.NetTcpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.NetTcpSecurityElement>
- [<span data-ttu-id="fcef2-185">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="fcef2-185">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="fcef2-186">绑定</span><span class="sxs-lookup"><span data-stu-id="fcef2-186">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="fcef2-187">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="fcef2-187">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="fcef2-188">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="fcef2-188">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

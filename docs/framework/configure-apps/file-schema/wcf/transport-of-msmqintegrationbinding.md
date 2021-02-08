---
description: 了解详细 <transport> 信息： <msmqIntegrationBinding>
title: <transport> 的 <msmqIntegrationBinding>
ms.date: 03/30/2017
ms.assetid: 054579e3-7fdd-47df-99ca-952706ba5c8e
ms.openlocfilehash: bcca714320f333a16d518248531efe8039ff566e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773519"
---
# <a name="transport-of-msmqintegrationbinding"></a><span data-ttu-id="6fe95-103">\<transport> 的 \<msmqIntegrationBinding></span><span class="sxs-lookup"><span data-stu-id="6fe95-103">\<transport> of \<msmqIntegrationBinding></span></span>

<span data-ttu-id="6fe95-104">定义消息队列集成传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="6fe95-104">Defines the security settings for the Message Queuing integration transport.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<msmqIntegrationBinding>**](msmqintegrationbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-msmqintegrationbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="6fe95-105">语法</span><span class="sxs-lookup"><span data-stu-id="6fe95-105">Syntax</span></span>  
  
```xml  
<security>
  <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
             msmqEncryptionAlgorithm="RC4Stream/AES"
             msmqProtectionLevel="None/Sign/EncryptAndSign"
             msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6fe95-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6fe95-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6fe95-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6fe95-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6fe95-108">特性</span><span class="sxs-lookup"><span data-stu-id="6fe95-108">Attributes</span></span>  
  
|<span data-ttu-id="6fe95-109">属性</span><span class="sxs-lookup"><span data-stu-id="6fe95-109">Attribute</span></span>|<span data-ttu-id="6fe95-110">说明</span><span class="sxs-lookup"><span data-stu-id="6fe95-110">Description</span></span>|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|<span data-ttu-id="6fe95-111">指定 MSMQ 传输必须采用什么方式对消息进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="6fe95-111">Specifies how the message must be authenticated by the MSMQ transport.</span></span> <span data-ttu-id="6fe95-112">如果将此属性设置为 `None`，则 `msmqProtectionLevel` 属性的值也必须设置为 `None`。</span><span class="sxs-lookup"><span data-stu-id="6fe95-112">If this is set to `None`, the value of the `msmqProtectionLevel` attribute must also be set to `None`.</span></span><br /><br /> <span data-ttu-id="6fe95-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="6fe95-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="6fe95-114">-None：无身份验证。</span><span class="sxs-lookup"><span data-stu-id="6fe95-114">-   None: No authentication.</span></span><br /><span data-ttu-id="6fe95-115">-WindowsDomain：身份验证机制使用 Active Directory 获取与消息关联的 SID 的 x.509 证书。</span><span class="sxs-lookup"><span data-stu-id="6fe95-115">-   WindowsDomain: The authentication mechanism uses Active Directory to get the X.509 certificate for the SID associated with the message.</span></span> <span data-ttu-id="6fe95-116">然后使用它来检查队列的 ACL 以确保用户有权写入队列。</span><span class="sxs-lookup"><span data-stu-id="6fe95-116">This is then used to check the ACL of the queue to ensure the user has permission to write to the queue.</span></span><br /><span data-ttu-id="6fe95-117">-Certificate：通道从证书存储区获取证书。</span><span class="sxs-lookup"><span data-stu-id="6fe95-117">-   Certificate: The channel gets the certificate from the certificate store.</span></span><br /><br /> <span data-ttu-id="6fe95-118">默认值为 WindowsDomain。</span><span class="sxs-lookup"><span data-stu-id="6fe95-118">The default value is WindowsDomain.</span></span> <span data-ttu-id="6fe95-119">此属性的类型为 <xref:System.ServiceModel.MsmqAuthenticationMode>。</span><span class="sxs-lookup"><span data-stu-id="6fe95-119">This attribute is of type <xref:System.ServiceModel.MsmqAuthenticationMode>.</span></span>|  
|`msmqEncryptionAlgorithm`|<span data-ttu-id="6fe95-120">指定在消息队列管理器之间传输消息时用于在网络上对消息进行加密的算法。</span><span class="sxs-lookup"><span data-stu-id="6fe95-120">Specifies the algorithm to be used for message encryption on the wire when transferring messages between message queue managers.</span></span> <span data-ttu-id="6fe95-121">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="6fe95-121">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="6fe95-122">-RC4Stream</span><span class="sxs-lookup"><span data-stu-id="6fe95-122">-   RC4Stream</span></span><br /><span data-ttu-id="6fe95-123">-AES</span><span class="sxs-lookup"><span data-stu-id="6fe95-123">-   AES</span></span><br /><br /> <span data-ttu-id="6fe95-124">默认值为 RC4Stream。</span><span class="sxs-lookup"><span data-stu-id="6fe95-124">The default value is RC4Stream.</span></span> <span data-ttu-id="6fe95-125">此属性的类型为 <xref:System.ServiceModel.MsmqEncryptionAlgorithm>。</span><span class="sxs-lookup"><span data-stu-id="6fe95-125">This attribute is of type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.</span></span>|  
|`msmqProtectionLevel`|<span data-ttu-id="6fe95-126">指定在 MSMQ 传输级别采用什么方式来保护消息。</span><span class="sxs-lookup"><span data-stu-id="6fe95-126">Specifies how the message is secured at the level of the MSMQ transport.</span></span> <span data-ttu-id="6fe95-127">加密可确保消息的完整性，同时 EncryptAndSign 可确保消息的完整性和不可否认性;也就是说，消息确实来自发件人，发件人是谁说。</span><span class="sxs-lookup"><span data-stu-id="6fe95-127">Encryption ensures message integrity while EncryptAndSign ensures both message integrity and non-repudiation; that is, the message indeed comes from the sender and the sender is who they say they are.</span></span><br /><br /> <span data-ttu-id="6fe95-128">-有效值包括：</span><span class="sxs-lookup"><span data-stu-id="6fe95-128">-   Valid values include the following:</span></span><br /><span data-ttu-id="6fe95-129">-None：无保护。</span><span class="sxs-lookup"><span data-stu-id="6fe95-129">-   None: No protection.</span></span><br /><span data-ttu-id="6fe95-130">-Sign：对消息进行签名。</span><span class="sxs-lookup"><span data-stu-id="6fe95-130">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="6fe95-131">-EncryptAndSign：对消息进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="6fe95-131">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="6fe95-132">默认值为 Sign。</span><span class="sxs-lookup"><span data-stu-id="6fe95-132">The default value is Sign.</span></span> <span data-ttu-id="6fe95-133">此属性的类型为 ProtectionLevel。</span><span class="sxs-lookup"><span data-stu-id="6fe95-133">This attribute is of type ProtectionLevel.</span></span>|  
|`msmqSecureHashAlgorithm`|<span data-ttu-id="6fe95-134">-指定要在签名中计算摘要时使用的算法。</span><span class="sxs-lookup"><span data-stu-id="6fe95-134">-   Specifies the algorithm to be used in computing the digest as part of signatures.</span></span> <span data-ttu-id="6fe95-135">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="6fe95-135">Valid values include the following:</span></span><br /><span data-ttu-id="6fe95-136">-MD5</span><span class="sxs-lookup"><span data-stu-id="6fe95-136">-   MD5</span></span><br /><span data-ttu-id="6fe95-137">-SHA1</span><span class="sxs-lookup"><span data-stu-id="6fe95-137">-   SHA1</span></span><br /><span data-ttu-id="6fe95-138">-SHA256</span><span class="sxs-lookup"><span data-stu-id="6fe95-138">-   SHA256</span></span><br /><span data-ttu-id="6fe95-139">-SHA512</span><span class="sxs-lookup"><span data-stu-id="6fe95-139">-   SHA512</span></span><br /><br /> <span data-ttu-id="6fe95-140">默认值为 SHA1。</span><span class="sxs-lookup"><span data-stu-id="6fe95-140">The default value is SHA1.</span></span> <span data-ttu-id="6fe95-141">此属性的类型为 <xref:System.ServiceModel.MsmqSecureHashAlgorithm>。</span><span class="sxs-lookup"><span data-stu-id="6fe95-141">This attribute is of type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.</span></span><br><span data-ttu-id="6fe95-142">由于 MD5 和 SHA1 出现冲突，Microsoft 建议 SHA256 或更好。</span><span class="sxs-lookup"><span data-stu-id="6fe95-142">Due to collision problems with MD5 and SHA1, Microsoft recommends SHA256 or better.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6fe95-143">子元素</span><span class="sxs-lookup"><span data-stu-id="6fe95-143">Child Elements</span></span>  

 <span data-ttu-id="6fe95-144">无</span><span class="sxs-lookup"><span data-stu-id="6fe95-144">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6fe95-145">父元素</span><span class="sxs-lookup"><span data-stu-id="6fe95-145">Parent Elements</span></span>  
  
|<span data-ttu-id="6fe95-146">元素</span><span class="sxs-lookup"><span data-stu-id="6fe95-146">Element</span></span>|<span data-ttu-id="6fe95-147">说明</span><span class="sxs-lookup"><span data-stu-id="6fe95-147">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-basichttpbinding.md)|<span data-ttu-id="6fe95-148">定义 MSMQ 绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="6fe95-148">Defines the security settings for a MSMQ binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6fe95-149">备注</span><span class="sxs-lookup"><span data-stu-id="6fe95-149">Remarks</span></span>  

 <span data-ttu-id="6fe95-150">此元素包装消息队列集成传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="6fe95-150">This element encapsulates the security settings for the Message Queuing integration transport.</span></span> <span data-ttu-id="6fe95-151">消息队列集成传输和排队传输的设置是相同的。</span><span class="sxs-lookup"><span data-stu-id="6fe95-151">The settings are the same for both the Message Queuing integration and queued transports.</span></span> <span data-ttu-id="6fe95-152">使用此元素可以设置身份验证模式、加密算法、安全哈希算法和保护级别。</span><span class="sxs-lookup"><span data-stu-id="6fe95-152">It enables you to set the Authentication Mode, Encryption Algorithm, Secure Hash Algorithm, and Protection Level.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fe95-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="6fe95-153">See also</span></span>

- <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>
- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.MsmqIntegrationSecurityElement.Transport%2A>
- <xref:System.ServiceModel.MsmqTransportSecurity>
- [<span data-ttu-id="6fe95-154">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="6fe95-154">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="6fe95-155">绑定</span><span class="sxs-lookup"><span data-stu-id="6fe95-155">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="6fe95-156">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="6fe95-156">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="6fe95-157">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="6fe95-157">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

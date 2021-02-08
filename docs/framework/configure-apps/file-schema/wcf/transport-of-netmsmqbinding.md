---
description: 了解详细 <transport> 信息： <netMsmqBinding>
title: <transport> 的 <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 72e1b338-39f0-4af1-a5d9-7a2fb79f6a0b
ms.openlocfilehash: 04768f259629277abd758d102f3873bb28f16514
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773493"
---
# <a name="transport-of-netmsmqbinding"></a><span data-ttu-id="efe92-103">\<transport> 的 \<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="efe92-103">\<transport> of \<netMsmqBinding></span></span>

<span data-ttu-id="efe92-104">定义传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="efe92-104">Defines the transport security settings.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netMsmqBinding>**](netmsmqbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-netmsmqbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="efe92-105">语法</span><span class="sxs-lookup"><span data-stu-id="efe92-105">Syntax</span></span>  
  
```xml  
<netMsmqBinding>
  <binding>
    <security>
      <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
                 msmqEncryptionAlgorithm="RC4Stream/AES"
                 msmqProtectionLevel="None/Sign/EncryptAndSign"
                 msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    </security>
  </binding>
</netMsmqBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="efe92-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="efe92-106">Attributes and Elements</span></span>  

 <span data-ttu-id="efe92-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="efe92-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="efe92-108">特性</span><span class="sxs-lookup"><span data-stu-id="efe92-108">Attributes</span></span>  
  
|<span data-ttu-id="efe92-109">属性</span><span class="sxs-lookup"><span data-stu-id="efe92-109">Attribute</span></span>|<span data-ttu-id="efe92-110">说明</span><span class="sxs-lookup"><span data-stu-id="efe92-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="efe92-111">msmqAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="efe92-111">msmqAuthenticationMode</span></span>|<span data-ttu-id="efe92-112">指定 MSMQ 传输必须采用什么方式对消息进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="efe92-112">Specifies how the message must be authenticated by the MSMQ transport.</span></span> <span data-ttu-id="efe92-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="efe92-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="efe92-114">-None：无身份验证。</span><span class="sxs-lookup"><span data-stu-id="efe92-114">-   None: No authentication.</span></span><br /><span data-ttu-id="efe92-115">-WindowsDomain：身份验证机制使用 Active Directory 检索与消息关联的安全标识符的 x.509 证书。</span><span class="sxs-lookup"><span data-stu-id="efe92-115">-   WindowsDomain: The authentication mechanism uses Active Directory to retrieve the X.509 certificate for the security identifier associated with the message.</span></span> <span data-ttu-id="efe92-116">然后使用它来检查队列的 ACL 以确保用户具有队列写权限。</span><span class="sxs-lookup"><span data-stu-id="efe92-116">This is then used to check the ACL of the queue to ensure the user has write permission for the queue.</span></span><br /><span data-ttu-id="efe92-117">-Certificate：通道从证书存储中检索证书。</span><span class="sxs-lookup"><span data-stu-id="efe92-117">-   Certificate: The channel retrieves the certificate from the certificate store.</span></span><br /><br /> <span data-ttu-id="efe92-118">默认值为 `WindowsDomain`。</span><span class="sxs-lookup"><span data-stu-id="efe92-118">The default is `WindowsDomain`.</span></span><br /><br /> <span data-ttu-id="efe92-119">如果将此属性设置为 `None`，则 `msmqProtectionLevel` 属性也必须设置为 `None`。</span><span class="sxs-lookup"><span data-stu-id="efe92-119">If this attribute is set to `None`, the `msmqProtectionLevel` attribute must also be set to `None`.</span></span> <span data-ttu-id="efe92-120">此特性的类型为 <xref:System.ServiceModel.MsmqAuthenticationMode></span><span class="sxs-lookup"><span data-stu-id="efe92-120">This attribute is of type <xref:System.ServiceModel.MsmqAuthenticationMode></span></span>|  
|<span data-ttu-id="efe92-121">msmqEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="efe92-121">msmqEncryptionAlgorithm</span></span>|<span data-ttu-id="efe92-122">指定在消息队列管理器之间传输消息时用于在网络上对消息进行加密的算法。</span><span class="sxs-lookup"><span data-stu-id="efe92-122">Specifies the algorithm to be used for message encryption on the wire when transferring messages between message queue managers.</span></span> <span data-ttu-id="efe92-123">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="efe92-123">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="efe92-124">-RC4Stream</span><span class="sxs-lookup"><span data-stu-id="efe92-124">-   RC4Stream</span></span><br /><span data-ttu-id="efe92-125">-AES</span><span class="sxs-lookup"><span data-stu-id="efe92-125">-   AES</span></span><br /><span data-ttu-id="efe92-126">-默认值为 `RC4Stream` 。</span><span class="sxs-lookup"><span data-stu-id="efe92-126">-   The default value is `RC4Stream`.</span></span> <span data-ttu-id="efe92-127">此属性的类型为 <xref:System.ServiceModel.MsmqEncryptionAlgorithm>。</span><span class="sxs-lookup"><span data-stu-id="efe92-127">This attribute is of type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.</span></span>|  
|<span data-ttu-id="efe92-128">msmqProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="efe92-128">msmqProtectionLevel</span></span>|<span data-ttu-id="efe92-129">指定在 MSMQ 传输级别采用什么方式来保护消息。</span><span class="sxs-lookup"><span data-stu-id="efe92-129">Specifies the way messages are secured at the level of the MSMQ transport.</span></span> <span data-ttu-id="efe92-130">加密可确保消息的完整性，而签名和加密不仅可以确保消息的完整性，还可以确保消息的不可否认性。</span><span class="sxs-lookup"><span data-stu-id="efe92-130">Encryption ensures message integrity, while sign and encrypt ensures both message integrity and non-repudiation.</span></span> <span data-ttu-id="efe92-131">也就是说，消息确实来自发件人，发件人是谁说。</span><span class="sxs-lookup"><span data-stu-id="efe92-131">That is, the message indeed came from the sender and the sender is who they say they are.</span></span> <span data-ttu-id="efe92-132">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="efe92-132">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="efe92-133">-None：无保护。</span><span class="sxs-lookup"><span data-stu-id="efe92-133">-   None: No protection.</span></span><br /><span data-ttu-id="efe92-134">-Sign：对消息进行签名。</span><span class="sxs-lookup"><span data-stu-id="efe92-134">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="efe92-135">-EncryptAndSign：对消息进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="efe92-135">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><span data-ttu-id="efe92-136">-默认值为 `Sign` 。</span><span class="sxs-lookup"><span data-stu-id="efe92-136">-   The default is `Sign`.</span></span>|  
|<span data-ttu-id="efe92-137">msmqSecureHashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="efe92-137">msmqSecureHashAlgorithm</span></span>|<span data-ttu-id="efe92-138">指定用于计算消息摘要的哈希算法。</span><span class="sxs-lookup"><span data-stu-id="efe92-138">Specifies the hash algorithm to be used for computing the message digest.</span></span> <span data-ttu-id="efe92-139">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="efe92-139">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="efe92-140">-MD5</span><span class="sxs-lookup"><span data-stu-id="efe92-140">-   MD5</span></span><br /><span data-ttu-id="efe92-141">-SHA1</span><span class="sxs-lookup"><span data-stu-id="efe92-141">-   SHA1</span></span><br /><span data-ttu-id="efe92-142">-SHA256</span><span class="sxs-lookup"><span data-stu-id="efe92-142">-   SHA256</span></span><br /><span data-ttu-id="efe92-143">-SHA512</span><span class="sxs-lookup"><span data-stu-id="efe92-143">-   SHA512</span></span><br /><br /> <span data-ttu-id="efe92-144">默认值为 `SHA1`。</span><span class="sxs-lookup"><span data-stu-id="efe92-144">The default is `SHA1`.</span></span> <span data-ttu-id="efe92-145">此属性的类型为 <xref:System.ServiceModel.MsmqSecureHashAlgorithm>。</span><span class="sxs-lookup"><span data-stu-id="efe92-145">This attribute is of type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.</span></span><br><span data-ttu-id="efe92-146">由于 MD5 和 SHA1 出现冲突，Microsoft 建议 SHA256 或更好。</span><span class="sxs-lookup"><span data-stu-id="efe92-146">Due to collision problems with MD5 and SHA1, Microsoft recommends SHA256 or better.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="efe92-147">子元素</span><span class="sxs-lookup"><span data-stu-id="efe92-147">Child Elements</span></span>  

 <span data-ttu-id="efe92-148">无</span><span class="sxs-lookup"><span data-stu-id="efe92-148">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="efe92-149">父元素</span><span class="sxs-lookup"><span data-stu-id="efe92-149">Parent Elements</span></span>  
  
|<span data-ttu-id="efe92-150">元素</span><span class="sxs-lookup"><span data-stu-id="efe92-150">Element</span></span>|<span data-ttu-id="efe92-151">说明</span><span class="sxs-lookup"><span data-stu-id="efe92-151">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-netmsmqbinding.md)|<span data-ttu-id="efe92-152">定义排队传输的传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="efe92-152">Defines the transport security settings for queued transports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="efe92-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="efe92-153">See also</span></span>

- <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Transport%2A>
- <xref:System.ServiceModel.NetMsmqSecurity.Transport%2A>
- <xref:System.ServiceModel.MsmqTransportSecurity>
- [<span data-ttu-id="efe92-154">WCF 中的队列</span><span class="sxs-lookup"><span data-stu-id="efe92-154">Queues in WCF</span></span>](../../../wcf/feature-details/queues-in-wcf.md)
- [<span data-ttu-id="efe92-155">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="efe92-155">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="efe92-156">绑定</span><span class="sxs-lookup"><span data-stu-id="efe92-156">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="efe92-157">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="efe92-157">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="efe92-158">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="efe92-158">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

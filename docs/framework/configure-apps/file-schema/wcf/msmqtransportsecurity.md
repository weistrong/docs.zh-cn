---
description: 了解详细信息： <msmqTransportSecurity>
title: <msmqTransportSecurity>
ms.date: 03/30/2017
ms.assetid: 092e911b-ab1b-4069-a26e-6134c3299e06
ms.openlocfilehash: d5a681c287749598c8c80470ea6d800f1687a80d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684160"
---
# \<msmqTransportSecurity>

<span data-ttu-id="cb788-102">指定自定义绑定的 MSMQ 传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="cb788-102">Specifies MSMQ transport security settings for a custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<msmqIntegration>**](msmqintegration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<msmqTransportSecurity>**  
  
## <a name="syntax"></a><span data-ttu-id="cb788-103">语法</span><span class="sxs-lookup"><span data-stu-id="cb788-103">Syntax</span></span>  
  
```xml  
<msmqTransportSecurity msmqAuthenticationMode="None/Windows/Certificate"
                       msmqEncryptionAlgorithm="RC4Stream/AES"
                       msmqProtectionLevel="None/Sign/EncryptAndSign"
                       msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
</msmqTransportSecurity>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cb788-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="cb788-104">Attributes and Elements</span></span>  

 <span data-ttu-id="cb788-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb788-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cb788-106">特性</span><span class="sxs-lookup"><span data-stu-id="cb788-106">Attributes</span></span>  
  
|<span data-ttu-id="cb788-107">属性</span><span class="sxs-lookup"><span data-stu-id="cb788-107">Attribute</span></span>|<span data-ttu-id="cb788-108">说明</span><span class="sxs-lookup"><span data-stu-id="cb788-108">Description</span></span>|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|<span data-ttu-id="cb788-109">指定 MSMQ 传输必须采用什么方式对消息进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="cb788-109">Specifies how the message must be authenticated by the MSMQ transport.</span></span> <span data-ttu-id="cb788-110">如果将此属性设置为 `None`，则 `msmqProtectionLevel` 属性的值也必须设置为 `None`。</span><span class="sxs-lookup"><span data-stu-id="cb788-110">If this is set to `None`, the value of the `msmqProtectionLevel` attribute must also be set to `None`.</span></span><br /><br /> <span data-ttu-id="cb788-111">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="cb788-111">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="cb788-112">-None：无身份验证。</span><span class="sxs-lookup"><span data-stu-id="cb788-112">-   None: No authentication.</span></span><br /><span data-ttu-id="cb788-113">-Windows：身份验证机制使用 Active Directory 获取与消息关联的 SID 的 x.509 证书。</span><span class="sxs-lookup"><span data-stu-id="cb788-113">-   Windows: The authentication mechanism uses Active Directory to get the X.509 certificate for the SID associated with the message.</span></span> <span data-ttu-id="cb788-114">然后使用它来检查队列的 ACL 以确保用户有权写入队列。</span><span class="sxs-lookup"><span data-stu-id="cb788-114">This is then used to check the ACL of the queue to ensure the user has permission to write to the queue.</span></span><br /><span data-ttu-id="cb788-115">-Certificate：通道从证书存储区获取证书。</span><span class="sxs-lookup"><span data-stu-id="cb788-115">-   Certificate: The channel gets the certificate from the certificate store.</span></span><br /><br /> <span data-ttu-id="cb788-116">默认值为 Windows。</span><span class="sxs-lookup"><span data-stu-id="cb788-116">The default value is Windows.</span></span> <span data-ttu-id="cb788-117">此属性的类型为 <xref:System.ServiceModel.MsmqAuthenticationMode>。</span><span class="sxs-lookup"><span data-stu-id="cb788-117">This attribute is of type <xref:System.ServiceModel.MsmqAuthenticationMode>.</span></span>|  
|`msmqEncryptionAlgorithm`|<span data-ttu-id="cb788-118">指定在消息队列管理器之间传输消息时用于在网络上对消息进行加密的算法。</span><span class="sxs-lookup"><span data-stu-id="cb788-118">Specifies the algorithm to be used for message encryption on the wire when transferring messages between message queue managers.</span></span> <span data-ttu-id="cb788-119">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="cb788-119">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="cb788-120">-RC4Stream</span><span class="sxs-lookup"><span data-stu-id="cb788-120">-   RC4Stream</span></span><br /><span data-ttu-id="cb788-121">-AES</span><span class="sxs-lookup"><span data-stu-id="cb788-121">-   AES</span></span><br /><br /> <span data-ttu-id="cb788-122">默认值为 RC4Stream。</span><span class="sxs-lookup"><span data-stu-id="cb788-122">The default value is RC4Stream.</span></span> <span data-ttu-id="cb788-123">此属性的类型为 <xref:System.ServiceModel.MsmqEncryptionAlgorithm>。</span><span class="sxs-lookup"><span data-stu-id="cb788-123">This attribute is of type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.</span></span>|  
|`msmqProtectionLevel`|<span data-ttu-id="cb788-124">指定在 MSMQ 传输级别采用什么方式来保护消息。</span><span class="sxs-lookup"><span data-stu-id="cb788-124">Specifies how the message is secured at the level of the MSMQ transport.</span></span> <span data-ttu-id="cb788-125">加密可确保消息的完整性，同时 EncryptAndSign 可确保消息的完整性和不可否认性;也就是说，消息确实来自发件人，发件人是谁说。</span><span class="sxs-lookup"><span data-stu-id="cb788-125">Encryption ensures message integrity while EncryptAndSign ensures both message integrity and non-repudiation; that is, the message indeed comes from the sender and the sender is who they say they are.</span></span> <span data-ttu-id="cb788-126">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="cb788-126">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="cb788-127">-None：无保护。</span><span class="sxs-lookup"><span data-stu-id="cb788-127">-   None: No protection.</span></span><br /><span data-ttu-id="cb788-128">-Sign：对消息进行签名。</span><span class="sxs-lookup"><span data-stu-id="cb788-128">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="cb788-129">-EncryptAndSign：对消息进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="cb788-129">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="cb788-130">默认值为 Sign。</span><span class="sxs-lookup"><span data-stu-id="cb788-130">The default value is Sign.</span></span> <span data-ttu-id="cb788-131">此属性的类型为 <xref:System.Net.Security.ProtectionLevel>。</span><span class="sxs-lookup"><span data-stu-id="cb788-131">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
|`msmqSecureHashAlgorithm`|<span data-ttu-id="cb788-132">指定用于计算签名中的摘要的算法。</span><span class="sxs-lookup"><span data-stu-id="cb788-132">Specifies the algorithm to be used in computing the digest as part of signatures.</span></span> <span data-ttu-id="cb788-133">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="cb788-133">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="cb788-134">-MD5</span><span class="sxs-lookup"><span data-stu-id="cb788-134">-   MD5</span></span><br /><span data-ttu-id="cb788-135">-SHA1</span><span class="sxs-lookup"><span data-stu-id="cb788-135">-   SHA1</span></span><br /><span data-ttu-id="cb788-136">-SHA256</span><span class="sxs-lookup"><span data-stu-id="cb788-136">-   SHA256</span></span><br /><span data-ttu-id="cb788-137">-SHA512</span><span class="sxs-lookup"><span data-stu-id="cb788-137">-   SHA512</span></span><br /><br /> <span data-ttu-id="cb788-138">默认值为 SHA1。</span><span class="sxs-lookup"><span data-stu-id="cb788-138">The default value is SHA1.</span></span> <span data-ttu-id="cb788-139">此属性的类型为 <xref:System.ServiceModel.MsmqSecureHashAlgorithm>。</span><span class="sxs-lookup"><span data-stu-id="cb788-139">This attribute is of type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.</span></span><br><span data-ttu-id="cb788-140">由于 MD5 和 SHA1 出现冲突，Microsoft 建议 SHA256 或更好。</span><span class="sxs-lookup"><span data-stu-id="cb788-140">Due to collision problems with MD5 and SHA1, Microsoft recommends SHA256 or better.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cb788-141">子元素</span><span class="sxs-lookup"><span data-stu-id="cb788-141">Child Elements</span></span>  

 <span data-ttu-id="cb788-142">无。</span><span class="sxs-lookup"><span data-stu-id="cb788-142">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cb788-143">父元素</span><span class="sxs-lookup"><span data-stu-id="cb788-143">Parent Elements</span></span>  
  
|<span data-ttu-id="cb788-144">元素</span><span class="sxs-lookup"><span data-stu-id="cb788-144">Element</span></span>|<span data-ttu-id="cb788-145">说明</span><span class="sxs-lookup"><span data-stu-id="cb788-145">Description</span></span>|  
|-------------|-----------------|  
|[\<msmqIntegration>](msmqintegration.md)|<span data-ttu-id="cb788-146">指定与消息队列 (MSMQ) 发送方或接收方进行交互所需的设置。</span><span class="sxs-lookup"><span data-stu-id="cb788-146">Specifies settings required for interaction with a Message Queuing (MSMQ) sender or receiver.</span></span>|  
|[\<msmqTransport>](msmqtransport.md)|<span data-ttu-id="cb788-147">指定使用本机 MSMQ 协议的 Windows Communication Foundation (WCF) 服务的队列通信属性。</span><span class="sxs-lookup"><span data-stu-id="cb788-147">Specifies the queuing communication properties for a Windows Communication Foundation (WCF) service that uses the native MSMQ protocol.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cb788-148">备注</span><span class="sxs-lookup"><span data-stu-id="cb788-148">Remarks</span></span>  

 <span data-ttu-id="cb788-149">有关传输安全的详细信息，请参阅 [传输安全性](../../../wcf/feature-details/transport-security.md)。</span><span class="sxs-lookup"><span data-stu-id="cb788-149">For more information on transport security, see [Transport Security](../../../wcf/feature-details/transport-security.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb788-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="cb788-150">See also</span></span>

- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>
- <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="cb788-151">WCF 中的队列</span><span class="sxs-lookup"><span data-stu-id="cb788-151">Queues in WCF</span></span>](../../../wcf/feature-details/queues-in-wcf.md)
- [<span data-ttu-id="cb788-152">传输</span><span class="sxs-lookup"><span data-stu-id="cb788-152">Transports</span></span>](../../../wcf/feature-details/transports.md)
- [<span data-ttu-id="cb788-153">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="cb788-153">Choosing a Transport</span></span>](../../../wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="cb788-154">绑定</span><span class="sxs-lookup"><span data-stu-id="cb788-154">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="cb788-155">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="cb788-155">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="cb788-156">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="cb788-156">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="cb788-157">传输安全</span><span class="sxs-lookup"><span data-stu-id="cb788-157">Transport Security</span></span>](../../../wcf/feature-details/transport-security.md)

---
description: 了解详细 <security> 信息： <msmqIntegrationBinding>
title: <security> 的 <msmqIntegrationBinding>
ms.date: 03/30/2017
ms.assetid: ae5c68a8-14a2-4c6e-b9e0-3e94e3e9135e
ms.openlocfilehash: 4ad4cb89599198661d764cfeb985609be027c0eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683198"
---
# <a name="security-of-msmqintegrationbinding"></a><span data-ttu-id="e4a24-103">\<security> 的 \<msmqIntegrationBinding></span><span class="sxs-lookup"><span data-stu-id="e4a24-103">\<security> of \<msmqIntegrationBinding></span></span>

<span data-ttu-id="e4a24-104">定义消息队列 (MSMQ) 集成通道的传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="e4a24-104">Defines the transport security settings for the Message Queuing (MSMQ) integration channel.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<msmqIntegrationBinding>**](msmqintegrationbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="e4a24-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4a24-105">Syntax</span></span>  
  
```xml  
<msmqIntegrationBinding>
  <binding>
    <security mode="None/Transport">
      <transport msmqAuthenticationMode="None/Windows/Certificate"
                 msmqEncryptionAlgorithm="RC4Stream/AES"
                 msmqProtectionLevel="None/Sign/EncryptAndSign"
                 msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
      <message algorithmSuite="Aes128/Aes192/Aes256/Rsa15Aes128/ Rsa15Aes256/TripleDes"
               clientCredentialType="None/Windows/UserName/Certificate/CardSpace"
               defaultProtectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</msmqIntegrationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e4a24-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="e4a24-106">Attributes and Elements</span></span>  

 <span data-ttu-id="e4a24-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e4a24-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e4a24-108">特性</span><span class="sxs-lookup"><span data-stu-id="e4a24-108">Attributes</span></span>  
  
|<span data-ttu-id="e4a24-109">属性</span><span class="sxs-lookup"><span data-stu-id="e4a24-109">Attribute</span></span>|<span data-ttu-id="e4a24-110">说明</span><span class="sxs-lookup"><span data-stu-id="e4a24-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e4a24-111">mode</span><span class="sxs-lookup"><span data-stu-id="e4a24-111">mode</span></span>|<span data-ttu-id="e4a24-112">指定使用消息队列集成通道控制完整性、保密性和身份验证的安全类型。</span><span class="sxs-lookup"><span data-stu-id="e4a24-112">Specifies the type of security that controls integrity, confidentiality and authentication with the Message Queuing integration channel.</span></span> <span data-ttu-id="e4a24-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="e4a24-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="e4a24-114">-None：这将禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="e4a24-114">-   None: This disables security.</span></span><br /><span data-ttu-id="e4a24-115">-Transport：传输提供保护和身份验证。</span><span class="sxs-lookup"><span data-stu-id="e4a24-115">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="e4a24-116">这适用于两个队列管理器之间的消息安全性。</span><span class="sxs-lookup"><span data-stu-id="e4a24-116">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="e4a24-117">未在应用程序和队列管理器之间提供安全性。</span><span class="sxs-lookup"><span data-stu-id="e4a24-117">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="e4a24-118">现有的 Msmq 应用程序与此类型的安全模式功能等效。</span><span class="sxs-lookup"><span data-stu-id="e4a24-118">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><br /> <span data-ttu-id="e4a24-119">默认值是 `Transport`。</span><span class="sxs-lookup"><span data-stu-id="e4a24-119">The default value is `Transport`.</span></span> <span data-ttu-id="e4a24-120">此属性的类型为 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="e4a24-120">This attribute is of type <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e4a24-121">子元素</span><span class="sxs-lookup"><span data-stu-id="e4a24-121">Child Elements</span></span>  
  
|<span data-ttu-id="e4a24-122">元素</span><span class="sxs-lookup"><span data-stu-id="e4a24-122">Element</span></span>|<span data-ttu-id="e4a24-123">说明</span><span class="sxs-lookup"><span data-stu-id="e4a24-123">Description</span></span>|  
|-------------|-----------------|  
|[\<transport>](transport-of-msmqintegrationbinding.md)|<span data-ttu-id="e4a24-124">定义消息队列集成传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="e4a24-124">Defines the security settings for the Message Queuing integration transport.</span></span> <span data-ttu-id="e4a24-125">此元素的类型为 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="e4a24-125">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e4a24-126">父元素</span><span class="sxs-lookup"><span data-stu-id="e4a24-126">Parent Elements</span></span>  
  
|<span data-ttu-id="e4a24-127">元素</span><span class="sxs-lookup"><span data-stu-id="e4a24-127">Element</span></span>|<span data-ttu-id="e4a24-128">说明</span><span class="sxs-lookup"><span data-stu-id="e4a24-128">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="e4a24-129">的绑定元素 [\<msmqIntegrationBinding>](msmqintegrationbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="e4a24-129">The binding element of the [\<msmqIntegrationBinding>](msmqintegrationbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e4a24-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4a24-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.MsmqIntegrationSecurityElement>
- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.MsmqIntegrationBindingElement.Security%2A>
- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>
- [<span data-ttu-id="e4a24-131">WCF 中的队列</span><span class="sxs-lookup"><span data-stu-id="e4a24-131">Queues in WCF</span></span>](../../../wcf/feature-details/queues-in-wcf.md)
- [<span data-ttu-id="e4a24-132">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="e4a24-132">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="e4a24-133">绑定</span><span class="sxs-lookup"><span data-stu-id="e4a24-133">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="e4a24-134">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="e4a24-134">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="e4a24-135">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="e4a24-135">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
- [\<msmqIntegrationBinding>](msmqintegrationbinding.md)

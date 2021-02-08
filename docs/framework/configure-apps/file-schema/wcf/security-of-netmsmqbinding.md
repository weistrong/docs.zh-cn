---
description: 了解详细 <security> 信息： <netMsmqBinding>
title: <security> 的 <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 001d11a9-7439-498c-b09d-fca20eaf8cd3
ms.openlocfilehash: 1b60d9e390e371555f4c3abf4988e79bb0f04fe8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786845"
---
# <a name="security-of-netmsmqbinding"></a><span data-ttu-id="beccc-103">\<security> 的 \<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="beccc-103">\<security> of \<netMsmqBinding></span></span>

<span data-ttu-id="beccc-104">定义 MSMQ 绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="beccc-104">Defines the security settings for a MSMQ binding.</span></span> <span data-ttu-id="beccc-105">它指定是否启用传输或 SOAP 安全；如果启用，还指定所使用的身份验证模式和保护级别。</span><span class="sxs-lookup"><span data-stu-id="beccc-105">It specifies whether transport or SOAP security is enabled and, if so, what authentication mode and protection levels are in use.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netMsmqBinding>**](netmsmqbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="beccc-106">语法</span><span class="sxs-lookup"><span data-stu-id="beccc-106">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/Both">
  <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
             msmqEncryptionAlgorithm="RC4Stream/AES"
             msmqProtectionLevel="None/Sign/EncryptAndSign"
             msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
             clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="beccc-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="beccc-107">Attributes and Elements</span></span>  

 <span data-ttu-id="beccc-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="beccc-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="beccc-109">特性</span><span class="sxs-lookup"><span data-stu-id="beccc-109">Attributes</span></span>  
  
|<span data-ttu-id="beccc-110">属性</span><span class="sxs-lookup"><span data-stu-id="beccc-110">Attribute</span></span>|<span data-ttu-id="beccc-111">说明</span><span class="sxs-lookup"><span data-stu-id="beccc-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="beccc-112">mode</span><span class="sxs-lookup"><span data-stu-id="beccc-112">mode</span></span>|<span data-ttu-id="beccc-113">指定用于控制完整性、保密性和身份验证的安全类型。</span><span class="sxs-lookup"><span data-stu-id="beccc-113">Specifies the type of security that controls integrity, confidentiality and authentication.</span></span> <span data-ttu-id="beccc-114">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="beccc-114">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="beccc-115">-None：这将禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-115">-   None: This disables security.</span></span><br /><span data-ttu-id="beccc-116">-Transport：传输提供保护和身份验证。</span><span class="sxs-lookup"><span data-stu-id="beccc-116">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="beccc-117">这适用于两个队列管理器之间的消息安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-117">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="beccc-118">未在应用程序和队列管理器之间提供安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-118">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="beccc-119">现有的 Msmq 应用程序与此类型的安全模式功能等效。</span><span class="sxs-lookup"><span data-stu-id="beccc-119">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><span data-ttu-id="beccc-120">-Message：指定端应用程序安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-120">-   Message: Specifies end-end application security.</span></span> <span data-ttu-id="beccc-121">未在传输层提供安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-121">There is no security offered at the transport layer.</span></span> <span data-ttu-id="beccc-122">这类似于其他标准绑定提供的安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-122">This is similar to the security offered by other standard bindings.</span></span><br /><span data-ttu-id="beccc-123">-Both：同时在传输和 SOAP 消息传送层上提供安全性。</span><span class="sxs-lookup"><span data-stu-id="beccc-123">-   Both: Offers security at both the transport and SOAP messaging layer.</span></span> <span data-ttu-id="beccc-124">在这两个层上需要相同的凭据。</span><span class="sxs-lookup"><span data-stu-id="beccc-124">The same credential is required at both the levels.</span></span><br /><br /> <span data-ttu-id="beccc-125">默认值为 Transport。</span><span class="sxs-lookup"><span data-stu-id="beccc-125">The default value is Transport.</span></span> <span data-ttu-id="beccc-126">此属性的类型为 <xref:System.ServiceModel.NetMsmqSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="beccc-126">This attribute is of type <xref:System.ServiceModel.NetMsmqSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="beccc-127">子元素</span><span class="sxs-lookup"><span data-stu-id="beccc-127">Child Elements</span></span>  
  
|<span data-ttu-id="beccc-128">元素</span><span class="sxs-lookup"><span data-stu-id="beccc-128">Element</span></span>|<span data-ttu-id="beccc-129">说明</span><span class="sxs-lookup"><span data-stu-id="beccc-129">Description</span></span>|  
|-------------|-----------------|  
|[\<message>](message-of-netmsmqbinding.md)|<span data-ttu-id="beccc-130">定义 SOAP 消息安全设置。</span><span class="sxs-lookup"><span data-stu-id="beccc-130">Defines the SOAP message security settings.</span></span> <span data-ttu-id="beccc-131">此元素的类型为 <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>。</span><span class="sxs-lookup"><span data-stu-id="beccc-131">This element is of type <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>.</span></span>|  
|[\<transport>](transport-of-netmsmqbinding.md)|<span data-ttu-id="beccc-132">定义 MSMQ 传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="beccc-132">Defines the security settings for the MSMQ transport.</span></span> <span data-ttu-id="beccc-133">此元素的类型为 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="beccc-133">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="beccc-134">父元素</span><span class="sxs-lookup"><span data-stu-id="beccc-134">Parent Elements</span></span>  
  
|<span data-ttu-id="beccc-135">元素</span><span class="sxs-lookup"><span data-stu-id="beccc-135">Element</span></span>|<span data-ttu-id="beccc-136">说明</span><span class="sxs-lookup"><span data-stu-id="beccc-136">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="beccc-137">binding</span><span class="sxs-lookup"><span data-stu-id="beccc-137">binding</span></span>|<span data-ttu-id="beccc-138">的绑定元素 [\<netMsmqBinding>](netmsmqbinding.md)</span><span class="sxs-lookup"><span data-stu-id="beccc-138">The binding element of the [\<netMsmqBinding>](netmsmqbinding.md)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="beccc-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="beccc-139">See also</span></span>

- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>
- <xref:System.ServiceModel.NetMsmqBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetMsmqBindingElement.Security%2A>
- <xref:System.ServiceModel.NetMsmqSecurity>
- [<span data-ttu-id="beccc-140">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="beccc-140">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="beccc-141">绑定</span><span class="sxs-lookup"><span data-stu-id="beccc-141">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="beccc-142">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="beccc-142">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="beccc-143">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="beccc-143">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
- [<span data-ttu-id="beccc-144">WCF 中的队列</span><span class="sxs-lookup"><span data-stu-id="beccc-144">Queues in WCF</span></span>](../../../wcf/feature-details/queues-in-wcf.md)

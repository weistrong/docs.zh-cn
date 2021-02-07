---
description: 了解详细 <message> 信息： <netMsmqBinding>
title: <message> 的 <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 6ebf0240-d7be-4493-b0fe-f00fd5989d77
ms.openlocfilehash: 0e8cf641ef8ba5361318f7b658d5d60beef6ce56
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749579"
---
# <a name="message-of-netmsmqbinding"></a><span data-ttu-id="bf6a1-103">\<message> 的 \<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="bf6a1-103">\<message> of \<netMsmqBinding></span></span>

<span data-ttu-id="bf6a1-104">在此 `netMsmqBinding` 绑定上定义 SOAP 消息安全设置。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-104">Defines the SOAP message security settings on this `netMsmqBinding` binding.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netMsmqBinding>**](netmsmqbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-netmsmqbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<message>**  

## <a name="syntax"></a><span data-ttu-id="bf6a1-105">语法</span><span class="sxs-lookup"><span data-stu-id="bf6a1-105">Syntax</span></span>

```xml
<netMsmqBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
    </security>
  </binding>
</netMsmqBinding>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bf6a1-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bf6a1-106">Attributes and Elements</span></span>

<span data-ttu-id="bf6a1-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="bf6a1-108">特性</span><span class="sxs-lookup"><span data-stu-id="bf6a1-108">Attributes</span></span>

|<span data-ttu-id="bf6a1-109">属性</span><span class="sxs-lookup"><span data-stu-id="bf6a1-109">Attribute</span></span>|<span data-ttu-id="bf6a1-110">说明</span><span class="sxs-lookup"><span data-stu-id="bf6a1-110">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="bf6a1-111">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="bf6a1-111">algorithmSuite</span></span>|<span data-ttu-id="bf6a1-112">设置消息加密和密钥包装算法，这些算法用于针对通过 MSMQ 传输发送的消息实现基于消息的安全性。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-112">Sets the message encryption and key-wrap algorithms that are used to achieve message-based security for messages sent over MSMQ transport.</span></span><br /><br /> <span data-ttu-id="bf6a1-113">默认值是 `Aes256`。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-113">The default value is `Aes256`.</span></span> <span data-ttu-id="bf6a1-114">此属性的类型为 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-114">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span></span>|
|<span data-ttu-id="bf6a1-115">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="bf6a1-115">clientCredentialType</span></span>|<span data-ttu-id="bf6a1-116">指定针对通过 MSMQ 传输发送的消息执行客户端身份验证时要使用的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-116">Specifies the type of credential to be used when performing client authentication for messages sent over the MSMQ transport.</span></span> <span data-ttu-id="bf6a1-117">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="bf6a1-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="bf6a1-118">-None：这允许服务与匿名客户端交互。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-118">-   None: This allows the service to interact with anonymous clients.</span></span> <span data-ttu-id="bf6a1-119">服务和客户端都不需要凭据。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-119">Neither the service nor the client requires a credential.</span></span><br /><span data-ttu-id="bf6a1-120">-Windows：这使得 SOAP 交换在 Windows 凭据的已验证上下文下。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-120">-   Windows: This enables the SOAP exchanges to be under the authenticated context of a Windows credential.</span></span> <span data-ttu-id="bf6a1-121">此设置总是执行基于 Kerberos 的身份验证。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-121">This always performs Kerberos-based authentication.</span></span><br /><span data-ttu-id="bf6a1-122">-UserName：这使服务可以要求使用用户名凭据对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-122">-   UserName: This enables the service to require that the client be authenticated using a UserName credential.</span></span> <span data-ttu-id="bf6a1-123">在这种情况下，需要使用以下行为指定 `clientCredentials` 凭据 **：**  Windows Communication Foundation (WCF) 不支持发送密码摘要，也不支持使用密码派生密钥并使用此类密钥来实现消息安全性。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-123">The credential in this case needs to be specified using the `clientCredentials` behavior **Caution:**  Windows Communication Foundation (WCF) does not support sending a password digest or deriving keys using password and using such keys for message security.</span></span> <span data-ttu-id="bf6a1-124">因此，在使用用户名凭据时，WCF 会强制使用交换。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-124">Therefore, WCF enforces that the exchange is secured when using UserName credentials.</span></span> <span data-ttu-id="bf6a1-125">此模式要求使用 `clientCredential` 行为和 `serviceCertificate` 在客户端指定服务证书。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-125">This mode requires that the service certificate be specified on the client side using `clientCredential` behavior and `serviceCertificate`.</span></span> <br /><br /> <span data-ttu-id="bf6a1-126">-Certificate：使服务可以要求使用证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-126">-   Certificate: This enables the service to require that the client be authenticated using a certificate.</span></span> <span data-ttu-id="bf6a1-127">在此情况下，需要使用 `clientCredentials` 行为指定客户端凭据。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-127">The client credential in this case needs to be specified using the `clientCredentials` behavior.</span></span> <span data-ttu-id="bf6a1-128">在此情况下，需要使用 `clientCredentials` 行为，通过指定 `serviceCertificate` 来指定服务凭据。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-128">The service credential in this case needs to be specified using the `clientCredentials` behavior by specifying the `serviceCertificate`.</span></span><br /><span data-ttu-id="bf6a1-129">-CardSpace：这允许服务要求使用 CardSpace 对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-129">-   CardSpace: This allows the service to require that the client be authenticated using a CardSpace.</span></span> <span data-ttu-id="bf6a1-130">必须在 `serviceCertificate` 行为中设置 `clientCredential`。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-130">The `serviceCertificate` must be provisioned in the `clientCredential` behavior.</span></span><br /><br /> <span data-ttu-id="bf6a1-131">默认值是 `Windows`。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-131">The default value is `Windows`.</span></span> <span data-ttu-id="bf6a1-132">此属性的类型为 <xref:System.ServiceModel.MessageCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-132">This attribute is of type <xref:System.ServiceModel.MessageCredentialType>.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="bf6a1-133">子元素</span><span class="sxs-lookup"><span data-stu-id="bf6a1-133">Child Elements</span></span>

<span data-ttu-id="bf6a1-134">无</span><span class="sxs-lookup"><span data-stu-id="bf6a1-134">None</span></span>

### <a name="parent-elements"></a><span data-ttu-id="bf6a1-135">父元素</span><span class="sxs-lookup"><span data-stu-id="bf6a1-135">Parent Elements</span></span>

|<span data-ttu-id="bf6a1-136">元素</span><span class="sxs-lookup"><span data-stu-id="bf6a1-136">Element</span></span>|<span data-ttu-id="bf6a1-137">说明</span><span class="sxs-lookup"><span data-stu-id="bf6a1-137">Description</span></span>|
|-------------|-----------------|
|[\<security>](security-of-netmsmqbinding.md)|<span data-ttu-id="bf6a1-138">定义绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-138">Defines the security settings for a binding.</span></span>|

## <a name="see-also"></a><span data-ttu-id="bf6a1-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="bf6a1-139">See also</span></span>

- <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Message%2A>
- <xref:System.ServiceModel.NetMsmqSecurity.Message%2A>
- <xref:System.ServiceModel.MessageSecurityOverMsmq>
- [<span data-ttu-id="bf6a1-140">WCF 中的队列</span><span class="sxs-lookup"><span data-stu-id="bf6a1-140">Queues in WCF</span></span>](../../../wcf/feature-details/queues-in-wcf.md)
- [<span data-ttu-id="bf6a1-141">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="bf6a1-141">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="bf6a1-142">绑定</span><span class="sxs-lookup"><span data-stu-id="bf6a1-142">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="bf6a1-143">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="bf6a1-143">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="bf6a1-144">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="bf6a1-144">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

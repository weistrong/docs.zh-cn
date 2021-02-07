---
description: 了解更多相关信息： Windows 客户端的消息安全性（不带凭据协商）
title: 没有凭据协商的 Windows 客户端的消息安全
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fc07a26c-cbee-41c5-8fb0-329085fef749
ms.openlocfilehash: e9edd63c80d868024d8a4b664c42456bb454cb69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99727009"
---
# <a name="message-security-with-a-windows-client-without-credential-negotiation"></a><span data-ttu-id="0cc5c-103">没有凭据协商的 Windows 客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="0cc5c-103">Message Security with a Windows Client without Credential Negotiation</span></span>

<span data-ttu-id="0cc5c-104">下面的方案演示了由 Kerberos 协议保护 Windows Communication Foundation (WCF) 客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-104">The following scenario shows a Windows Communication Foundation (WCF) client and service secured by the Kerberos protocol.</span></span>

<span data-ttu-id="0cc5c-105">服务和客户端位于相同的域或可信域。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-105">Both the service and the client are in the same domain or trusted domains.</span></span>

> [!NOTE]
> <span data-ttu-id="0cc5c-106">此方案与 [Windows 客户端的消息安全](message-security-with-a-windows-client.md) 之间的区别在于，在发送应用程序消息之前，此方案不会与服务协商服务凭据。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-106">The difference between this scenario and [Message Security with a Windows Client](message-security-with-a-windows-client.md) is that this scenario does not negotiate the service credential with the service prior to sending the application message.</span></span> <span data-ttu-id="0cc5c-107">此外，由于这需要 Kerberos 协议，所以此方案需要一个 Windows 域环境。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-107">Additionally, because this requires the Kerberos protocol, this scenario requires a Windows domain environment.</span></span>

<span data-ttu-id="0cc5c-108">![没有凭证协商的消息安全](media/0c9f9baa-2439-4ef9-92f4-43c242d85d0d.gif "0c9f9baa-2439-4ef9-92f4-43c242d85d0d")</span><span class="sxs-lookup"><span data-stu-id="0cc5c-108">![Message security without credential negotiation](media/0c9f9baa-2439-4ef9-92f4-43c242d85d0d.gif "0c9f9baa-2439-4ef9-92f4-43c242d85d0d")</span></span>

|<span data-ttu-id="0cc5c-109">特征</span><span class="sxs-lookup"><span data-stu-id="0cc5c-109">Characteristic</span></span>|<span data-ttu-id="0cc5c-110">说明</span><span class="sxs-lookup"><span data-stu-id="0cc5c-110">Description</span></span>|
|--------------------|-----------------|
|<span data-ttu-id="0cc5c-111">安全模式</span><span class="sxs-lookup"><span data-stu-id="0cc5c-111">Security Mode</span></span>|<span data-ttu-id="0cc5c-112">消息</span><span class="sxs-lookup"><span data-stu-id="0cc5c-112">Message</span></span>|
|<span data-ttu-id="0cc5c-113">互操作性</span><span class="sxs-lookup"><span data-stu-id="0cc5c-113">Interoperability</span></span>|<span data-ttu-id="0cc5c-114">是，WS-Security 使用 Kerberos 令牌配置文件兼容的客户端</span><span class="sxs-lookup"><span data-stu-id="0cc5c-114">Yes, WS-Security with Kerberos token-profile compatible clients</span></span>|
|<span data-ttu-id="0cc5c-115">身份验证（服务器）</span><span class="sxs-lookup"><span data-stu-id="0cc5c-115">Authentication (Server)</span></span>|<span data-ttu-id="0cc5c-116">服务器和客户端的相互身份验证</span><span class="sxs-lookup"><span data-stu-id="0cc5c-116">Mutual authentication of the server and client</span></span>|
|<span data-ttu-id="0cc5c-117">身份验证（客户端）</span><span class="sxs-lookup"><span data-stu-id="0cc5c-117">Authentication (Client)</span></span>|<span data-ttu-id="0cc5c-118">服务器和客户端的相互身份验证</span><span class="sxs-lookup"><span data-stu-id="0cc5c-118">Mutual authentication of the server and client</span></span>|
|<span data-ttu-id="0cc5c-119">完整性</span><span class="sxs-lookup"><span data-stu-id="0cc5c-119">Integrity</span></span>|<span data-ttu-id="0cc5c-120">是</span><span class="sxs-lookup"><span data-stu-id="0cc5c-120">Yes</span></span>|
|<span data-ttu-id="0cc5c-121">机密性</span><span class="sxs-lookup"><span data-stu-id="0cc5c-121">Confidentiality</span></span>|<span data-ttu-id="0cc5c-122">是</span><span class="sxs-lookup"><span data-stu-id="0cc5c-122">Yes</span></span>|
|<span data-ttu-id="0cc5c-123">Transport</span><span class="sxs-lookup"><span data-stu-id="0cc5c-123">Transport</span></span>|<span data-ttu-id="0cc5c-124">HTTP</span><span class="sxs-lookup"><span data-stu-id="0cc5c-124">HTTP</span></span>|
|<span data-ttu-id="0cc5c-125">绑定</span><span class="sxs-lookup"><span data-stu-id="0cc5c-125">Binding</span></span>|<xref:System.ServiceModel.WSHttpBinding>|

## <a name="service"></a><span data-ttu-id="0cc5c-126">服务</span><span class="sxs-lookup"><span data-stu-id="0cc5c-126">Service</span></span>

<span data-ttu-id="0cc5c-127">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-127">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="0cc5c-128">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="0cc5c-128">Do one of the following:</span></span>

- <span data-ttu-id="0cc5c-129">使用代码（而不使用配置）创建独立服务。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-129">Create a stand-alone service using the code with no configuration.</span></span>

- <span data-ttu-id="0cc5c-130">使用提供的配置创建服务，但不定义任何终结点。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-130">Create a service using the supplied configuration, but do not define any endpoints.</span></span>

### <a name="code"></a><span data-ttu-id="0cc5c-131">代码</span><span class="sxs-lookup"><span data-stu-id="0cc5c-131">Code</span></span>

<span data-ttu-id="0cc5c-132">下面的代码创建使用消息安全的服务终结点。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-132">The following code creates a service endpoint that uses message security.</span></span> <span data-ttu-id="0cc5c-133">代码禁用了服务凭据协商并禁止建立安全上下文令牌 (SCT)。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-133">The code disables service credential negotiation, and the establishment of a security context token (SCT).</span></span>

> [!NOTE]
> <span data-ttu-id="0cc5c-134">若要使用没有协商的 Windows 凭据类型，则服务的用户帐户必须能够访问在 Active Directory 域注册的服务主体名称 (SPN)。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-134">To use the Windows credential type without negotiation, the service's user account must have access to service principal name (SPN) that is registered with the Active Directory domain.</span></span> <span data-ttu-id="0cc5c-135">可通过两种方式实现此目的：</span><span class="sxs-lookup"><span data-stu-id="0cc5c-135">You can do this in two ways:</span></span>

1. <span data-ttu-id="0cc5c-136">使用 `NetworkService` 或 `LocalSystem` 帐户运行服务。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-136">Use the `NetworkService` or `LocalSystem` account to run your service.</span></span> <span data-ttu-id="0cc5c-137">由于这些帐户有权访问在计算机加入 Active Directory 域时建立的计算机 SPN，因此 WCF 将自动在服务的元数据中的服务终结点内生成正确的 SPN 元素 (Web 服务描述语言或 WSDL) 。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-137">Because those accounts have access to the machine SPN that is established when the machine joins the Active Directory domain, WCF automatically generates the proper SPN element inside the service's endpoint in the service's metadata (Web Services Description Language, or WSDL).</span></span>

2. <span data-ttu-id="0cc5c-138">使用任意 Active Directory 域帐户运行服务。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-138">Use an arbitrary Active Directory domain account to run your service.</span></span> <span data-ttu-id="0cc5c-139">在这种情况下，您需要为该域帐户建立一个 SPN。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-139">In this case, you need to establish an SPN for that domain account.</span></span> <span data-ttu-id="0cc5c-140">执行此操作的一种方法是使用 Setspn.exe 实用工具。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-140">One way of doing this is to use the Setspn.exe utility tool.</span></span> <span data-ttu-id="0cc5c-141">为服务帐户创建 SPN 后，将 WCF 配置为使用 (WSDL) 的元数据将该 SPN 发布到服务的客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-141">Once the SPN is created for the service's account, configure WCF to publish that SPN to the service's clients through its metadata (WSDL).</span></span> <span data-ttu-id="0cc5c-142">通过为公开的终结点设置终结点标识（或通过应用程序配置文件或代码）也可完成此操作。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-142">This is done by setting the endpoint identity for the exposed endpoint, either though an application configuration file or code.</span></span> <span data-ttu-id="0cc5c-143">下面的示例以编程方式发布标识。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-143">The following example publishes the identity programmatically.</span></span>

<span data-ttu-id="0cc5c-144">有关 Spn、Kerberos 协议和 Active Directory 的详细信息，请参阅 [适用于 Windows 的 Kerberos 技术补充](/previous-versions/msp-n-p/ff649429(v=pandp.10))。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-144">For more information about SPNs, the Kerberos protocol, and Active Directory, see [Kerberos Technical Supplement for Windows](/previous-versions/msp-n-p/ff649429(v=pandp.10)).</span></span> <span data-ttu-id="0cc5c-145">有关终结点标识的详细信息，请参阅 [SecurityBindingElement Authentication 模式](securitybindingelement-authentication-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-145">For more information about endpoint identities, see [SecurityBindingElement Authentication Modes](securitybindingelement-authentication-modes.md).</span></span>

[!code-csharp[C_SecurityScenarios#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#12)]
[!code-vb[C_SecurityScenarios#12](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#12)]

### <a name="configuration"></a><span data-ttu-id="0cc5c-146">Configuration</span><span class="sxs-lookup"><span data-stu-id="0cc5c-146">Configuration</span></span>

<span data-ttu-id="0cc5c-147">以下配置可代替代码使用。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-147">The following configuration can be used instead of the code.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <system.serviceModel>
    <behaviors />
    <services>
      <service behaviorConfiguration="" name="ServiceModel.Calculator">
        <endpoint address="http://localhost/Calculator"
                  binding="wsHttpBinding"
                  bindingConfiguration="KerberosBinding"
                  name="WSHttpBinding_ICalculator"
                  contract="ServiceModel.ICalculator"
                  listenUri="net.tcp://localhost/metadata" >
         <identity>
            <servicePrincipalName value="service_spn_name" />
         </identity>
        </endpoint>
      </service>
    </services>
    <bindings>
      <wsHttpBinding>
        <binding name="KerberosBinding">
          <security>
            <message negotiateServiceCredential="false"
                     establishSecurityContext="false" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
    <client />
  </system.serviceModel>
</configuration>
```

## <a name="client"></a><span data-ttu-id="0cc5c-148">客户端</span><span class="sxs-lookup"><span data-stu-id="0cc5c-148">Client</span></span>

<span data-ttu-id="0cc5c-149">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-149">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="0cc5c-150">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="0cc5c-150">Do one of the following:</span></span>

- <span data-ttu-id="0cc5c-151">使用代码（和客户端代码）创建独立客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-151">Create a stand-alone client using the code (and client code).</span></span>

- <span data-ttu-id="0cc5c-152">创建不定义任何终结点地址的客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-152">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="0cc5c-153">而使用将配置名称作为自变量的客户端构造函数。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-153">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="0cc5c-154">例如：</span><span class="sxs-lookup"><span data-stu-id="0cc5c-154">For example:</span></span>

  [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
  [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]

### <a name="code"></a><span data-ttu-id="0cc5c-155">代码</span><span class="sxs-lookup"><span data-stu-id="0cc5c-155">Code</span></span>

<span data-ttu-id="0cc5c-156">下面的代码将配置客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-156">The following code configures the client.</span></span> <span data-ttu-id="0cc5c-157">安全模式设置为 Message，客户端凭据类型设置为 Windows。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-157">The security mode is set to Message, and the client credential type is set to Windows.</span></span> <span data-ttu-id="0cc5c-158">请注意，<xref:System.ServiceModel.MessageSecurityOverHttp.NegotiateServiceCredential%2A> 和 <xref:System.ServiceModel.NonDualMessageSecurityOverHttp.EstablishSecurityContext%2A> 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-158">Note that the <xref:System.ServiceModel.MessageSecurityOverHttp.NegotiateServiceCredential%2A> and <xref:System.ServiceModel.NonDualMessageSecurityOverHttp.EstablishSecurityContext%2A> properties are set to `false`.</span></span>

> [!NOTE]
> <span data-ttu-id="0cc5c-159">若要使用没有协商的 Windows 凭据类型，则必须在开始与服务进行通信前使用服务的帐户 SPN 配置客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-159">To use Windows credential type without negotiation, the client must be configured with the service's account SPN prior to commencing the communication with the service.</span></span> <span data-ttu-id="0cc5c-160">客户端使用 SPN 获取 Kerberos 令牌对与服务的通信进行身份验证和保护。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-160">The client uses the SPN to get the Kerberos token to authenticate and secure the communication with the service.</span></span> <span data-ttu-id="0cc5c-161">下面的示例演示如何使用服务的 SPN 配置客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-161">The following sample shows how to configure the client with the service's SPN.</span></span> <span data-ttu-id="0cc5c-162">如果你使用的是 "工作的 [元数据实用工具" 工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 生成客户端，则服务的 SPN 将自动从服务的元数据 (WSDL) 传播到客户端（如果服务的元数据包含该信息）。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-162">If you are using the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to generate the client, the service's SPN will be automatically propagated to the client from the service's metadata (WSDL), if the service's metadata contains that information.</span></span> <span data-ttu-id="0cc5c-163">有关如何配置服务以在服务的元数据中包含其 SPN 的详细信息，请参阅本主题后面的 "服务" 一节。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-163">For more information about how to configure the service to include its SPN in the service's metadata, see the "Service" section later in this topic .</span></span>
>
> <span data-ttu-id="0cc5c-164">有关 Spn、Kerberos 和 Active Directory 的详细信息，请参阅 [适用于 Windows 的 Kerberos 技术补充](/previous-versions/msp-n-p/ff649429(v=pandp.10))。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-164">For more information about SPNs, Kerberos, and Active Directory, see [Kerberos Technical Supplement for Windows](/previous-versions/msp-n-p/ff649429(v=pandp.10)).</span></span> <span data-ttu-id="0cc5c-165">有关终结点标识的详细信息，请参阅 [SecurityBindingElement Authentication 模式](securitybindingelement-authentication-modes.md) 主题。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-165">For more information about endpoint identities, see [SecurityBindingElement Authentication Modes](securitybindingelement-authentication-modes.md) topic.</span></span>

[!code-csharp[C_SecurityScenarios#19](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#19)]
[!code-vb[C_SecurityScenarios#19](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#19)]

### <a name="configuration"></a><span data-ttu-id="0cc5c-166">Configuration</span><span class="sxs-lookup"><span data-stu-id="0cc5c-166">Configuration</span></span>

<span data-ttu-id="0cc5c-167">下面的代码将配置客户端。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-167">The following code configures the client.</span></span> <span data-ttu-id="0cc5c-168">请注意， [\<servicePrincipalName>](../../configure-apps/file-schema/wcf/serviceprincipalname.md) 必须将元素设置为与在 Active Directory 域中为服务帐户注册的服务 SPN 匹配。</span><span class="sxs-lookup"><span data-stu-id="0cc5c-168">Note that the [\<servicePrincipalName>](../../configure-apps/file-schema/wcf/serviceprincipalname.md) element must be set to match the service's SPN as registered for the service's account in the Active Directory domain.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <system.serviceModel>
    <bindings>
      <wsHttpBinding>
        <binding name="WSHttpBinding_ICalculator" >
          <security mode="Message">
            <message clientCredentialType="Windows"
                     negotiateServiceCredential="false"
                     establishSecurityContext="false" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
    <client>
      <endpoint address="http://localhost/Calculator"
                binding="wsHttpBinding"
                bindingConfiguration="WSHttpBinding_ICalculator"
                contract="ICalculator"
                name="WSHttpBinding_ICalculator">
        <identity>
          <servicePrincipalName value="service_spn_name" />
        </identity>
      </endpoint>
    </client>
  </system.serviceModel>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="0cc5c-169">请参阅</span><span class="sxs-lookup"><span data-stu-id="0cc5c-169">See also</span></span>

- [<span data-ttu-id="0cc5c-170">安全性概述</span><span class="sxs-lookup"><span data-stu-id="0cc5c-170">Security Overview</span></span>](security-overview.md)
- [<span data-ttu-id="0cc5c-171">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="0cc5c-171">Service Identity and Authentication</span></span>](service-identity-and-authentication.md)
- <span data-ttu-id="0cc5c-172">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="0cc5c-172">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>

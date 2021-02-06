---
description: 了解详细信息：如何：保护元数据终结点
title: 如何：保护元数据终结点
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9f71b6ae-737c-4382-8d89-0a7b1c7e182b
ms.openlocfilehash: bcce3fd0708049435c791cae5064f84133dfd612
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643301"
---
# <a name="how-to-secure-metadata-endpoints"></a><span data-ttu-id="2953c-103">如何：保护元数据终结点</span><span class="sxs-lookup"><span data-stu-id="2953c-103">How to: Secure Metadata Endpoints</span></span>

<span data-ttu-id="2953c-104">服务的元数据中可能包含恶意用户可以利用的关于您的应用程序的敏感信息。</span><span class="sxs-lookup"><span data-stu-id="2953c-104">Metadata for a service can contain sensitive information about your application that a malicious user can leverage.</span></span> <span data-ttu-id="2953c-105">服务使用者可能还要求一种用于获取关于服务的元数据的安全机制。</span><span class="sxs-lookup"><span data-stu-id="2953c-105">Consumers of your service may also require a secure mechanism for obtaining metadata about your service.</span></span> <span data-ttu-id="2953c-106">因此，有时需要使用安全终结点来发布元数据。</span><span class="sxs-lookup"><span data-stu-id="2953c-106">Therefore, it is sometimes necessary to publish your metadata using a secure endpoint.</span></span>

<span data-ttu-id="2953c-107">通常使用 Windows Communication Foundation 中定义的标准安全机制来保护元数据终结点， (WCF) 用于保护应用程序终结点。</span><span class="sxs-lookup"><span data-stu-id="2953c-107">Metadata endpoints are generally secured using the standard security mechanisms defined in Windows Communication Foundation (WCF) for securing application endpoints.</span></span> <span data-ttu-id="2953c-108">有关详细信息，请参阅[安全性概述](security-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="2953c-108">For more information, see [Security Overview](security-overview.md).</span></span>

<span data-ttu-id="2953c-109">本主题演示创建由安全套接字层 (SSL) 证书保护的终结点（换言之，HTTPS 终结点）的步骤。</span><span class="sxs-lookup"><span data-stu-id="2953c-109">This topic walks through the steps to create an endpoint secured by a Secure Sockets Layer (SSL) certificate or, in other words, an HTTPS endpoint.</span></span>

### <a name="to-create-a-secure-https-get-metadata-endpoint-in-code"></a><span data-ttu-id="2953c-110">在代码中创建安全的 HTTPS GET 元数据终结点</span><span class="sxs-lookup"><span data-stu-id="2953c-110">To create a secure HTTPS GET metadata endpoint in code</span></span>

1. <span data-ttu-id="2953c-111">使用适当的 X.509 证书配置端口。</span><span class="sxs-lookup"><span data-stu-id="2953c-111">Configure a port with an appropriate X.509 certificate.</span></span> <span data-ttu-id="2953c-112">该证书必须来自受信任的颁发机构，而且还必须有既定的“服务授权”用途。</span><span class="sxs-lookup"><span data-stu-id="2953c-112">The certificate must come from a trusted authority, and it must have an intended use of "Service Authorization."</span></span> <span data-ttu-id="2953c-113">必须使用 HttpCfg.exe 工具将该证书附加到该端口。</span><span class="sxs-lookup"><span data-stu-id="2953c-113">You must use the HttpCfg.exe tool to attach the certificate to the port.</span></span> <span data-ttu-id="2953c-114">请参阅 [如何：使用 SSL 证书配置端口](how-to-configure-a-port-with-an-ssl-certificate.md)。</span><span class="sxs-lookup"><span data-stu-id="2953c-114">See [How to: Configure a Port with an SSL Certificate](how-to-configure-a-port-with-an-ssl-certificate.md).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2953c-115">该证书或其域名系统 (DNS) 的主题必须与计算机的名称匹配。</span><span class="sxs-lookup"><span data-stu-id="2953c-115">The subject of the certificate or its Domain Name System (DNS) must match the name of the computer.</span></span> <span data-ttu-id="2953c-116">这一点非常重要，原因是 HTTPS 机制所执行的前几个步骤之一是检查是否将证书颁发给了在其上调用了该证书的地址的统一资源标识符 (URI)。</span><span class="sxs-lookup"><span data-stu-id="2953c-116">This is essential because one of the first steps the HTTPS mechanism performs is to check that the certificate is issued to the same Uniform Resource Identifier (URI) as the address upon which it is invoked.</span></span>

2. <span data-ttu-id="2953c-117">创建 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 类的新实例。</span><span class="sxs-lookup"><span data-stu-id="2953c-117">Create a new instance of the <xref:System.ServiceModel.Description.ServiceMetadataBehavior> class.</span></span>

3. <span data-ttu-id="2953c-118">将 <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetEnabled%2A> 类的 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="2953c-118">Set the <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetEnabled%2A> property of the <xref:System.ServiceModel.Description.ServiceMetadataBehavior> class to `true`.</span></span>

4. <span data-ttu-id="2953c-119">将 <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetUrl%2A> 属性设置为适当的 URL。</span><span class="sxs-lookup"><span data-stu-id="2953c-119">Set the <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetUrl%2A> property to an appropriate URL.</span></span> <span data-ttu-id="2953c-120">请注意，如果指定了绝对地址，则 URL 必须以方案开头 `https://` 。</span><span class="sxs-lookup"><span data-stu-id="2953c-120">Note that if you specify an absolute address, the URL must begin with the scheme `https://`.</span></span> <span data-ttu-id="2953c-121">如果指定相对地址，则必须为服务主机提供一个 HTTPS 基址。</span><span class="sxs-lookup"><span data-stu-id="2953c-121">If you specify a relative address, you must supply an HTTPS base address for your service host.</span></span> <span data-ttu-id="2953c-122">如果不设置此属性，则默认地址为 ""，或者直接为服务的 HTTPS 基址。</span><span class="sxs-lookup"><span data-stu-id="2953c-122">If this property is not set, the default address is "", or directly at the HTTPS base address for the service.</span></span>

5. <span data-ttu-id="2953c-123">将该实例添加到 <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> 类的 <xref:System.ServiceModel.Description.ServiceDescription> 属性返回的行为集合中，如下面的代码所示：</span><span class="sxs-lookup"><span data-stu-id="2953c-123">Add the instance to the behaviors collection that the <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> property of the <xref:System.ServiceModel.Description.ServiceDescription> class returns, as shown in the following code.</span></span>

    [!code-csharp[c_HowToSecureEndpoint#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtosecureendpoint/cs/source.cs#1)]
    [!code-vb[c_HowToSecureEndpoint#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtosecureendpoint/vb/source.vb#1)]

### <a name="to-create-a-secure-https-get-metadata-endpoint-in-configuration"></a><span data-ttu-id="2953c-124">在配置中创建安全的 HTTPS GET 元数据终结点</span><span class="sxs-lookup"><span data-stu-id="2953c-124">To create a secure HTTPS GET metadata endpoint in configuration</span></span>

1. <span data-ttu-id="2953c-125">将一个 [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) 元素添加到 [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) 服务的配置文件的元素中。</span><span class="sxs-lookup"><span data-stu-id="2953c-125">Add a [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) element to the [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) element of the configuration file for your service.</span></span>

2. <span data-ttu-id="2953c-126">向 [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) 元素添加元素 [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) 。</span><span class="sxs-lookup"><span data-stu-id="2953c-126">Add a [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) element to the [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) element.</span></span>

3. <span data-ttu-id="2953c-127">向 [\<behavior>](../../configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md) 元素添加元素 `<serviceBehaviors>` 。</span><span class="sxs-lookup"><span data-stu-id="2953c-127">Add a [\<behavior>](../../configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md) element to the `<serviceBehaviors>` element.</span></span>

4. <span data-ttu-id="2953c-128">将 `name` 元素的 `<behavior>` 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="2953c-128">Set the `name` attribute of the `<behavior>` element to an appropriate value.</span></span> <span data-ttu-id="2953c-129">需要 `name` 属性。</span><span class="sxs-lookup"><span data-stu-id="2953c-129">The `name` attribute is required.</span></span> <span data-ttu-id="2953c-130">下面的示例使用 `mySvcBehavior` 值。</span><span class="sxs-lookup"><span data-stu-id="2953c-130">The example below uses the value `mySvcBehavior`.</span></span>

5. <span data-ttu-id="2953c-131">将添加 [\<serviceMetadata>](../../configure-apps/file-schema/wcf/servicemetadata.md) 到 `<behavior>` 元素。</span><span class="sxs-lookup"><span data-stu-id="2953c-131">Add a [\<serviceMetadata>](../../configure-apps/file-schema/wcf/servicemetadata.md) to the `<behavior>` element.</span></span>

6. <span data-ttu-id="2953c-132">将 `httpsGetEnabled` 元素的 `<serviceMetadata>` 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="2953c-132">Set the `httpsGetEnabled` attribute of the `<serviceMetadata>` element to `true`.</span></span>

7. <span data-ttu-id="2953c-133">将 `httpsGetUrl` 元素的 `<serviceMetadata>` 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="2953c-133">Set the `httpsGetUrl` attribute of the `<serviceMetadata>` element to an appropriate value.</span></span> <span data-ttu-id="2953c-134">请注意，如果指定了绝对地址，则 URL 必须以方案开头 `https://` 。</span><span class="sxs-lookup"><span data-stu-id="2953c-134">Note that if you specify an absolute address, the URL must begin with the scheme `https://`.</span></span> <span data-ttu-id="2953c-135">如果指定相对地址，则必须为服务主机提供一个 HTTPS 基址。</span><span class="sxs-lookup"><span data-stu-id="2953c-135">If you specify a relative address, you must supply an HTTPS base address for your service host.</span></span> <span data-ttu-id="2953c-136">如果不设置此属性，则默认地址为 ""，或者直接为服务的 HTTPS 基址。</span><span class="sxs-lookup"><span data-stu-id="2953c-136">If this property is not set, the default address is "", or directly at the HTTPS base address for the service.</span></span>

8. <span data-ttu-id="2953c-137">若要将行为与服务一起使用，请将 `behaviorConfiguration` 元素的属性设置 [\<service>](../../configure-apps/file-schema/wcf/service.md) 为行为元素的 name 特性的值。</span><span class="sxs-lookup"><span data-stu-id="2953c-137">To use the behavior with a service, set the `behaviorConfiguration` attribute of the [\<service>](../../configure-apps/file-schema/wcf/service.md) element to the value of the name attribute of the behavior element.</span></span> <span data-ttu-id="2953c-138">下面的配置代码演示了一个完整的示例。</span><span class="sxs-lookup"><span data-stu-id="2953c-138">The following configuration code shows a complete example.</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
     <system.serviceModel>
      <behaviors>
       <serviceBehaviors>
        <behavior name="mySvcBehavior">
         <serviceMetadata httpsGetEnabled="true"
              httpsGetUrl="https://localhost:8036/calcMetadata" />
        </behavior>
       </serviceBehaviors>
      </behaviors>
     <services>
      <service behaviorConfiguration="mySvcBehavior"
            name="Microsoft.Security.Samples.Calculator">
       <endpoint address="http://localhost:8037/ServiceModelSamples/calculator"
       binding="wsHttpBinding" bindingConfiguration=""
       contract="Microsoft.Security.Samples.ICalculator" />
      </service>
     </services>
    </system.serviceModel>
    </configuration>
    ```

## <a name="example"></a><span data-ttu-id="2953c-139">示例</span><span class="sxs-lookup"><span data-stu-id="2953c-139">Example</span></span>

<span data-ttu-id="2953c-140">下面的示例创建 <xref:System.ServiceModel.ServiceHost> 类的一个实例并添加一个终结点。</span><span class="sxs-lookup"><span data-stu-id="2953c-140">The following example creates an instance of a <xref:System.ServiceModel.ServiceHost> class and adds an endpoint.</span></span> <span data-ttu-id="2953c-141">然后，该代码创建 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 类的一个实例并设置属性以创建一个安全的元数据交换点。</span><span class="sxs-lookup"><span data-stu-id="2953c-141">The code then creates an instance of the <xref:System.ServiceModel.Description.ServiceMetadataBehavior> class and sets the properties to create a secure metadata exchange point.</span></span>

[!code-csharp[c_HowToSecureEndpoint#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtosecureendpoint/cs/source.cs#0)]
[!code-vb[c_HowToSecureEndpoint#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtosecureendpoint/vb/source.vb#0)]

## <a name="compiling-the-code"></a><span data-ttu-id="2953c-142">编译代码</span><span class="sxs-lookup"><span data-stu-id="2953c-142">Compiling the Code</span></span>

<span data-ttu-id="2953c-143">该代码示例使用下列命名空间：</span><span class="sxs-lookup"><span data-stu-id="2953c-143">The code example uses the following namespaces:</span></span>

- <xref:System.ServiceModel?displayProperty=nameWithType>

- <xref:System.ServiceModel.Description?displayProperty=nameWithType>

## <a name="see-also"></a><span data-ttu-id="2953c-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="2953c-144">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetEnabled%2A>
- <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
- <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetUrl%2A>
- [<span data-ttu-id="2953c-145">如何：使用 SSL 证书配置端口</span><span class="sxs-lookup"><span data-stu-id="2953c-145">How to: Configure a Port with an SSL Certificate</span></span>](how-to-configure-a-port-with-an-ssl-certificate.md)
- [<span data-ttu-id="2953c-146">使用证书</span><span class="sxs-lookup"><span data-stu-id="2953c-146">Working with Certificates</span></span>](working-with-certificates.md)
- [<span data-ttu-id="2953c-147">元数据的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="2953c-147">Security Considerations with Metadata</span></span>](security-considerations-with-metadata.md)
- [<span data-ttu-id="2953c-148">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="2953c-148">Securing Services and Clients</span></span>](securing-services-and-clients.md)

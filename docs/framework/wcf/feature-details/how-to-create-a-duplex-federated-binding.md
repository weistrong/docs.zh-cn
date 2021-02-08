---
description: 了解详细信息：如何：创建双工联合绑定
title: 如何：创建双工联合绑定
ms.date: 03/30/2017
ms.assetid: 4331d2bc-5455-492a-9189-634a82597726
ms.openlocfilehash: 92d5eeeffab88d88aa245b51738048dced2d5d2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779902"
---
# <a name="how-to-create-a-duplex-federated-binding"></a><span data-ttu-id="2c365-103">如何：创建双工联合绑定</span><span class="sxs-lookup"><span data-stu-id="2c365-103">How to: Create a Duplex Federated Binding</span></span>

<span data-ttu-id="2c365-104"><xref:System.ServiceModel.WSFederationHttpBinding> 仅支持数据报和请求/答复消息交换协定。</span><span class="sxs-lookup"><span data-stu-id="2c365-104"><xref:System.ServiceModel.WSFederationHttpBinding> only supports the datagram and request/reply message exchange contracts.</span></span> <span data-ttu-id="2c365-105">若要使用双工消息交换协定，必须创建自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="2c365-105">To use the duplex message exchange contract, you must create a custom binding.</span></span> <span data-ttu-id="2c365-106">下面的过程演示如何使用 HTTP 和 TCP 传输协议的消息模式安全设置，以及使用 TCP 传输协议的混合模式安全设置，在配置中执行此操作。</span><span class="sxs-lookup"><span data-stu-id="2c365-106">The following procedures show how to do this in configuration, using Message mode security for the HTTP and TCP transports, and using mixed mode security for the TCP transport.</span></span> <span data-ttu-id="2c365-107">本主题的结尾是演示所有 3 个绑定的示例代码。</span><span class="sxs-lookup"><span data-stu-id="2c365-107">Sample code showing all 3 bindings is at the end of this topic.</span></span>

<span data-ttu-id="2c365-108">还可以在代码中创建绑定。</span><span class="sxs-lookup"><span data-stu-id="2c365-108">You can also create the binding in code.</span></span> <span data-ttu-id="2c365-109">有关要创建的绑定元素堆栈的说明，请参阅 [如何：使用 SecurityBindingElement 创建自定义绑定](how-to-create-a-custom-binding-using-the-securitybindingelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2c365-109">For a description of the binding elements stack to create, see [How to: Create a Custom Binding Using the SecurityBindingElement](how-to-create-a-custom-binding-using-the-securitybindingelement.md).</span></span>

## <a name="to-create-a-duplex-federated-custom-binding-with-http"></a><span data-ttu-id="2c365-110">使用 HTTP 创建双工联合自定义绑定</span><span class="sxs-lookup"><span data-stu-id="2c365-110">To create a duplex federated custom binding with HTTP</span></span>

1. <span data-ttu-id="2c365-111">在 [\<bindings>](../../configure-apps/file-schema/wcf/bindings.md) 配置文件的节点中，创建一个 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-111">In the [\<bindings>](../../configure-apps/file-schema/wcf/bindings.md) node of the configuration file, create a [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) element.</span></span>

2. <span data-ttu-id="2c365-112">在 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 元素内，创建一个 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) `name` 属性设置为的元素 `FederationDuplexHttpMessageSecurityBinding` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-112">Inside the [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) element, create a [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element with the `name` attribute set to `FederationDuplexHttpMessageSecurityBinding`.</span></span>

3. <span data-ttu-id="2c365-113">在 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) 元素内，创建一个 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) `authenticationMode` 属性设置为的元素 `SecureConversation` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-113">Inside the [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element, create a [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element with the `authenticationMode` attribute set to `SecureConversation`.</span></span>

4. <span data-ttu-id="2c365-114">在 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 元素内创建一个 [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) 元素，该元素的 `authenticationMode` 属性设置为 `IssuedTokenForCertificate` 或 `IssuedTokenForSslNegotiated` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-114">Inside the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element, create a [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) element with the `authenticationMode` attribute set to `IssuedTokenForCertificate` or `IssuedTokenForSslNegotiated`.</span></span>

5. <span data-ttu-id="2c365-115">在 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 元素后，创建一个空 [\<compositeDuplex>](../../configure-apps/file-schema/wcf/compositeduplex.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-115">Following the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element, create an empty [\<compositeDuplex>](../../configure-apps/file-schema/wcf/compositeduplex.md) element.</span></span>

6. <span data-ttu-id="2c365-116">在 [\<compositeDuplex>](../../configure-apps/file-schema/wcf/compositeduplex.md) 元素后，创建一个空 [\<oneWay>](../../configure-apps/file-schema/wcf/oneway.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-116">Following the [\<compositeDuplex>](../../configure-apps/file-schema/wcf/compositeduplex.md) element, create an empty [\<oneWay>](../../configure-apps/file-schema/wcf/oneway.md) element.</span></span>

7. <span data-ttu-id="2c365-117">在 [\<oneWay>](../../configure-apps/file-schema/wcf/oneway.md) 元素后，创建一个空 [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-117">Following the [\<oneWay>](../../configure-apps/file-schema/wcf/oneway.md) element, create an empty [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md) element.</span></span>

## <a name="to-create-a-duplex-federated-custom-binding-with-tcp-message-security-mode"></a><span data-ttu-id="2c365-118">使用 TCP 消息安全模式创建双工联合自定义绑定</span><span class="sxs-lookup"><span data-stu-id="2c365-118">To create a duplex federated custom binding with TCP message security mode</span></span>

1. <span data-ttu-id="2c365-119">在 [\<bindings>](../../configure-apps/file-schema/wcf/bindings.md) 配置文件的节点中，创建一个 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-119">In the [\<bindings>](../../configure-apps/file-schema/wcf/bindings.md) node of the configuration file, create a [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) element.</span></span>

2. <span data-ttu-id="2c365-120">在 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 元素内，创建一个 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) `name` 属性设置为的元素 `FederationDuplexTcpMessageSecurityBinding` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-120">Inside the [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) element, create a [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element with the `name` attribute set to `FederationDuplexTcpMessageSecurityBinding`.</span></span>

3. <span data-ttu-id="2c365-121">在 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) 元素内，创建一个 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) `authenticationMode` 属性设置为的元素 `SecureConversation` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-121">Inside the [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element, create a [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element with the `authenticationMode` attribute set to `SecureConversation`.</span></span>

4. <span data-ttu-id="2c365-122">在 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 元素内创建一个 [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) 元素，该元素的 `authenticationMode` 属性设置为 `IssuedTokenForCertificate` 或 `IssuedTokenForSslNegotiated` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-122">Inside the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element, create a [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) element with the `authenticationMode` attribute set to `IssuedTokenForCertificate` or `IssuedTokenForSslNegotiated`.</span></span>

5. <span data-ttu-id="2c365-123">在 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 元素后，创建一个空 [\<tcpTransport>](../../configure-apps/file-schema/wcf/tcptransport.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-123">Following the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element, create an empty [\<tcpTransport>](../../configure-apps/file-schema/wcf/tcptransport.md) element.</span></span>

## <a name="to-create-a-duplex-federated-custom-binding-with-tcp-mixed-security-mode"></a><span data-ttu-id="2c365-124">使用 TCP 混合安全模式创建双工联合自定义绑定</span><span class="sxs-lookup"><span data-stu-id="2c365-124">To create a duplex federated custom binding with TCP mixed security mode</span></span>

1. <span data-ttu-id="2c365-125">在 [\<bindings>](../../configure-apps/file-schema/wcf/bindings.md) 配置文件的节点中，创建一个 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-125">In the [\<bindings>](../../configure-apps/file-schema/wcf/bindings.md) node of the configuration file, create a [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) element.</span></span>

2. <span data-ttu-id="2c365-126">在 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 元素内，创建一个 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) `name` 属性设置为的元素 `FederationDuplexTcpTransportSecurityWithMessageCredentialBinding` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-126">Inside the [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) element, create a [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element with the `name` attribute set to `FederationDuplexTcpTransportSecurityWithMessageCredentialBinding`.</span></span>

3. <span data-ttu-id="2c365-127">在 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) 元素内，创建一个 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) `authenticationMode` 属性设置为的元素 `SecureConversation` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-127">Inside the [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) element, create a [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element with the `authenticationMode` attribute set to `SecureConversation`.</span></span>

4. <span data-ttu-id="2c365-128">在 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 元素内创建一个 [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) 元素，该元素的 `authenticationMode` 属性设置为 `IssuedTokenForCertificate` 或 `IssuedTokenForSslNegotiated` 。</span><span class="sxs-lookup"><span data-stu-id="2c365-128">Inside the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element, create a [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) element with the `authenticationMode` attribute set to `IssuedTokenForCertificate` or `IssuedTokenForSslNegotiated`.</span></span>

5. <span data-ttu-id="2c365-129">在 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 元素后，创建一个空 [\<sslStreamSecurity>](../../configure-apps/file-schema/wcf/sslstreamsecurity.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-129">Following the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) element, create an empty [\<sslStreamSecurity>](../../configure-apps/file-schema/wcf/sslstreamsecurity.md) element.</span></span>

6. <span data-ttu-id="2c365-130">在 [\<sslStreamSecurity>](../../configure-apps/file-schema/wcf/sslstreamsecurity.md) 元素后，创建一个空 [\<tcpTransport>](../../configure-apps/file-schema/wcf/tcptransport.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2c365-130">Following the [\<sslStreamSecurity>](../../configure-apps/file-schema/wcf/sslstreamsecurity.md) element, create an empty [\<tcpTransport>](../../configure-apps/file-schema/wcf/tcptransport.md) element.</span></span>

## <a name="code-sample"></a><span data-ttu-id="2c365-131">代码示例</span><span class="sxs-lookup"><span data-stu-id="2c365-131">Code Sample</span></span>

### <a name="sample-with-3-bindings"></a><span data-ttu-id="2c365-132">包含 3 个绑定的示例</span><span class="sxs-lookup"><span data-stu-id="2c365-132">Sample with 3 Bindings</span></span>

1. <span data-ttu-id="2c365-133">将以下代码插入到配置文件中。</span><span class="sxs-lookup"><span data-stu-id="2c365-133">Insert the following code into your configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="2c365-134">示例</span><span class="sxs-lookup"><span data-stu-id="2c365-134">Example</span></span>

```xml
<bindings>
   <customBinding>
      <binding name="FederationDuplexHttpMessageSecurityBinding">
<!-- duplex contract requires secure conversation with require cancellation = true -->
          <security authenticationMode="SecureConversation">
              <secureConversationBootstrap authenticationMode="IssuedTokenForSslNegotiated" />
          </security>
          <compositeDuplex />
          <oneWay />
          <httpTransport />
       </binding>
<!-- duplex over https is not supported -->
       <binding name="FederationDuplexTcpMessageSecurityBinding">
<!-- duplex contract requires secure conversation with require cancellation = true -->
          <security authenticationMode="SecureConversation">
              <secureConversationBootstrap authenticationMode="IssuedTokenForSslNegotiated" />
          </security>
          <tcpTransport />
       </binding>
       <binding name="FederationDuplexTcpTransportSecurityWithMessageCredentialsBinding">
<!-- duplex contract requires secure conversation with require cancellation = true -->
          <security authenticationMode="SecureConversation">
              <secureConversationBootstrap authenticationMode="IssuedTokenOverTransport" />
          </security>
<!-- requireClientCertificate = true or <windowsStreamSecurity /> can be used, but does not make sense for most scenarios -->
          <sslStreamSecurity />
          <tcpTransport />
       </binding>
    </customBinding>
</bindings>
```

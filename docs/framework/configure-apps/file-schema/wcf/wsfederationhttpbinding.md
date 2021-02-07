---
description: 了解详细信息： <wsFederationHttpBinding>
title: <wsFederationHttpBinding>
ms.date: 03/30/2017
helpviewer_keywords:
- wsFederationBinding element
ms.assetid: 9c3312b4-2137-4e71-bf3f-de1cf8e9be79
ms.openlocfilehash: 1217c4e46fe18ea5df478b8a790be4da33590c92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682093"
---
# \<wsFederationHttpBinding>

<span data-ttu-id="3411e-102">定义一个支持 WS-Federation 的绑定。</span><span class="sxs-lookup"><span data-stu-id="3411e-102">Defines a binding that supports WS-Federation.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<wsFederationHttpBinding>**  

## <a name="syntax"></a><span data-ttu-id="3411e-103">语法</span><span class="sxs-lookup"><span data-stu-id="3411e-103">Syntax</span></span>

```xml
<wsFederationHttpBinding>
  <binding bypassProxyOnLocal="Boolean"
           closeTimeout="TimeSpan"
           hostNameComparisonMode="StrongWildcard/Exact/WeakWildcard"
           maxBufferPoolSize="integer"
           maxReceivedMessageSize="integer"
           messageEncoding="Text/Mtom"
           name="string"
           openTimeout="TimeSpan"
           privacyNoticeAt="Uri"
           privacyNoticeVersion="Integer"
           proxyAddress="Uri"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan"
           textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/ Utf8TextEncoding"
           transactionFlow="Boolean"
           useDefaultWebProxy="Boolean">
    <security mode="None/Message/TransportWithMessageCredential">
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey"
               negotiateServiceCredential="Boolean">
        <claimTypeRequirements>
          <add claimType="URI"
               isOptional="Boolean" />
        </claimTypeRequirements>
        <issuer address="Uri" >
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuer>
        <issuerMetadata address="String">
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuerMetadata>
        <tokenRequestParameters>
          <xmlElement>
          </xmlElement>
        </tokenRequestParameters>
      </message>
    </security>
    <reliableSession ordered="Boolean"
                     inactivityTimeout="TimeSpan"
                     enabled="Boolean" />
    <readerQuotas maxArrayLength="Integer"
                  maxBytesPerRead="Integer"
                  maxDepth="Integer"
                  maxNameTableCharCount="Integer"
                  maxStringContentLength="Integer" />
  </binding>
</wsFederationBinding>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3411e-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="3411e-104">Attributes and Elements</span></span>

<span data-ttu-id="3411e-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3411e-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="3411e-106">特性</span><span class="sxs-lookup"><span data-stu-id="3411e-106">Attributes</span></span>

|<span data-ttu-id="3411e-107">属性</span><span class="sxs-lookup"><span data-stu-id="3411e-107">Attribute</span></span>|<span data-ttu-id="3411e-108">说明</span><span class="sxs-lookup"><span data-stu-id="3411e-108">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="3411e-109">bypassProxyOnLocal</span><span class="sxs-lookup"><span data-stu-id="3411e-109">bypassProxyOnLocal</span></span>|<span data-ttu-id="3411e-110">一个布尔值，指示是否对本地地址不使用代理服务器。</span><span class="sxs-lookup"><span data-stu-id="3411e-110">A Boolean value that indicates whether to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="3411e-111">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="3411e-111">The default is `false`.</span></span>|
|<span data-ttu-id="3411e-112">closeTimeout</span><span class="sxs-lookup"><span data-stu-id="3411e-112">closeTimeout</span></span>|<span data-ttu-id="3411e-113">一个 <xref:System.TimeSpan> 值，指定为完成关闭操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3411e-113">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="3411e-114">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="3411e-114">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="3411e-115">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="3411e-115">The default is 00:01:00.</span></span>|
|<span data-ttu-id="3411e-116">hostnameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="3411e-116">hostnameComparisonMode</span></span>|<span data-ttu-id="3411e-117">指定用于分析 URI 的 HTTP 主机名比较模式。</span><span class="sxs-lookup"><span data-stu-id="3411e-117">Specifies the HTTP hostname comparison mode used to parse URIs.</span></span> <span data-ttu-id="3411e-118">此属性的类型为 <xref:System.ServiceModel.HostNameComparisonMode>，指示在对 URI 进行匹配时，是否使用主机名来访问服务。</span><span class="sxs-lookup"><span data-stu-id="3411e-118">This attribute is of type <xref:System.ServiceModel.HostNameComparisonMode>, which indicates whether the hostname is used to reach the service when matching on the URI.</span></span> <span data-ttu-id="3411e-119">默认值为 <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>，表示忽略匹配项中的主机名。</span><span class="sxs-lookup"><span data-stu-id="3411e-119">The default value is <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, which ignores the hostname in the match.</span></span>|
|<span data-ttu-id="3411e-120">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="3411e-120">maxBufferPoolSize</span></span>|<span data-ttu-id="3411e-121">一个整数，指定此绑定的最大缓冲池大小。</span><span class="sxs-lookup"><span data-stu-id="3411e-121">An integer that specifies the maximum buffer pool size for this binding.</span></span> <span data-ttu-id="3411e-122">默认值为 524,288 字节 (512 \* 1024)。</span><span class="sxs-lookup"><span data-stu-id="3411e-122">The default is 524,288 bytes (512 \* 1024).</span></span> <span data-ttu-id="3411e-123">Windows Communication Foundation (WCF) 的许多部件使用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="3411e-123">Many parts of Windows Communication Foundation (WCF) use buffers.</span></span> <span data-ttu-id="3411e-124">每次使用缓冲区时，创建和销毁它们都将占用大量资源，而缓冲区的垃圾回收过程也是如此。</span><span class="sxs-lookup"><span data-stu-id="3411e-124">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="3411e-125">利用缓冲池，可以从缓冲池中获得缓冲区，使用缓冲区，然后在完成工作后将其返回给缓冲池。</span><span class="sxs-lookup"><span data-stu-id="3411e-125">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="3411e-126">这样就避免了创建和销毁缓冲区的系统开销。</span><span class="sxs-lookup"><span data-stu-id="3411e-126">Thus the overhead in creating and destroying buffers is avoided.</span></span>|
|<span data-ttu-id="3411e-127">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="3411e-127">maxReceivedMessageSize</span></span>|<span data-ttu-id="3411e-128">一个正整数，指定采用此绑定配置的通道上可以接收的最大消息大小（字节），包括消息头。</span><span class="sxs-lookup"><span data-stu-id="3411e-128">A positive integer that specifies the maximum message size, in bytes, including headers, that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="3411e-129">如果消息超出此限制，则发送方将收到 SOAP 错误。</span><span class="sxs-lookup"><span data-stu-id="3411e-129">The sender of a message exceeding this limit will receive a SOAP fault.</span></span> <span data-ttu-id="3411e-130">接收方将删除该消息，并在跟踪日志中创建事件项。</span><span class="sxs-lookup"><span data-stu-id="3411e-130">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="3411e-131">默认值为 65536。</span><span class="sxs-lookup"><span data-stu-id="3411e-131">The default is 65536.</span></span>|
|<span data-ttu-id="3411e-132">messageEncoding</span><span class="sxs-lookup"><span data-stu-id="3411e-132">messageEncoding</span></span>|<span data-ttu-id="3411e-133">定义用于对消息进行编码的编码器。</span><span class="sxs-lookup"><span data-stu-id="3411e-133">Defines the encoder used to encode the message.</span></span> <span data-ttu-id="3411e-134">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="3411e-134">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="3411e-135">-Text：使用文本消息编码器。</span><span class="sxs-lookup"><span data-stu-id="3411e-135">-   Text: Use a text message encoder.</span></span><br /><span data-ttu-id="3411e-136">-Mtom：使用消息传输组织机制 1.0 (MTOM) 编码器。</span><span class="sxs-lookup"><span data-stu-id="3411e-136">-   Mtom: Use a Message Transmission Organization Mechanism 1.0 (MTOM) encoder.</span></span><br /><br /> <span data-ttu-id="3411e-137">默认值为 Text。</span><span class="sxs-lookup"><span data-stu-id="3411e-137">The default is Text.</span></span><br /><br /> <span data-ttu-id="3411e-138">此属性的类型为 <xref:System.ServiceModel.WSMessageEncoding>。</span><span class="sxs-lookup"><span data-stu-id="3411e-138">This attribute is of type <xref:System.ServiceModel.WSMessageEncoding>.</span></span>|
|<span data-ttu-id="3411e-139">name</span><span class="sxs-lookup"><span data-stu-id="3411e-139">name</span></span>|<span data-ttu-id="3411e-140">一个包含绑定的配置名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="3411e-140">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="3411e-141">因为此值用作绑定的标识，所以它应该是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3411e-141">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="3411e-142">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="3411e-142">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="3411e-143">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="3411e-143">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|
|<span data-ttu-id="3411e-144">openTimeout</span><span class="sxs-lookup"><span data-stu-id="3411e-144">openTimeout</span></span>|<span data-ttu-id="3411e-145">一个 <xref:System.TimeSpan> 值，指定为完成打开操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3411e-145">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="3411e-146">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="3411e-146">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="3411e-147">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="3411e-147">The default is 00:01:00.</span></span>|
|<span data-ttu-id="3411e-148">privacyNoticeAt</span><span class="sxs-lookup"><span data-stu-id="3411e-148">privacyNoticeAt</span></span>|<span data-ttu-id="3411e-149">一个字符串，指定隐私声明位于的 URI。</span><span class="sxs-lookup"><span data-stu-id="3411e-149">A String that specifies a URI at which the privacy notice is located.</span></span>|
|<span data-ttu-id="3411e-150">privacyNoticeVersion</span><span class="sxs-lookup"><span data-stu-id="3411e-150">privacyNoticeVersion</span></span>|<span data-ttu-id="3411e-151">一个整数，指定当前隐私声明的版本。</span><span class="sxs-lookup"><span data-stu-id="3411e-151">An integer that specifies the version of the current privacy notice.</span></span>|
|<span data-ttu-id="3411e-152">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="3411e-152">proxyAddress</span></span>|<span data-ttu-id="3411e-153">一个指定 HTTP 代理的地址的 URI。</span><span class="sxs-lookup"><span data-stu-id="3411e-153">A URI that specifies the address of the HTTP proxy.</span></span> <span data-ttu-id="3411e-154">如果 `useDefaultWebProxy` 为 `true`，则此设置必须为 `null`。</span><span class="sxs-lookup"><span data-stu-id="3411e-154">If `useDefaultWebProxy` is `true`, this setting must be `null`.</span></span> <span data-ttu-id="3411e-155">默认值为 `null`。</span><span class="sxs-lookup"><span data-stu-id="3411e-155">The default is `null`.</span></span>|
|<span data-ttu-id="3411e-156">receiveTimeout</span><span class="sxs-lookup"><span data-stu-id="3411e-156">receiveTimeout</span></span>|<span data-ttu-id="3411e-157">一个 <xref:System.TimeSpan> 值，指定为完成接收操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3411e-157">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="3411e-158">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="3411e-158">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="3411e-159">默认值为 00:10:00。</span><span class="sxs-lookup"><span data-stu-id="3411e-159">The default is 00:10:00.</span></span>|
|<span data-ttu-id="3411e-160">sendTimeout</span><span class="sxs-lookup"><span data-stu-id="3411e-160">sendTimeout</span></span>|<span data-ttu-id="3411e-161">一个 <xref:System.TimeSpan> 值，指定为完成发送操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3411e-161">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="3411e-162">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="3411e-162">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="3411e-163">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="3411e-163">The default is 00:01:00.</span></span>|
|<span data-ttu-id="3411e-164">textEncoding</span><span class="sxs-lookup"><span data-stu-id="3411e-164">textEncoding</span></span>|<span data-ttu-id="3411e-165">设置要用来在绑定上发出消息的字符集编码。</span><span class="sxs-lookup"><span data-stu-id="3411e-165">Sets the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="3411e-166">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="3411e-166">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="3411e-167">-BigEndianUnicode： Unicode BigEndian 编码。</span><span class="sxs-lookup"><span data-stu-id="3411e-167">-   BigEndianUnicode: Unicode BigEndian encoding.</span></span><br /><span data-ttu-id="3411e-168">-Unicode：16位编码。</span><span class="sxs-lookup"><span data-stu-id="3411e-168">-   Unicode: 16-bit encoding.</span></span><br /><span data-ttu-id="3411e-169">-UTF8：8位编码</span><span class="sxs-lookup"><span data-stu-id="3411e-169">-   UTF8: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="3411e-170">默认编码为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="3411e-170">The default is UTF8.</span></span> <span data-ttu-id="3411e-171">此属性的类型为 <xref:System.Text.Encoding>。</span><span class="sxs-lookup"><span data-stu-id="3411e-171">This attribute is of type <xref:System.Text.Encoding>..</span></span>|
|<span data-ttu-id="3411e-172">transactionFlow</span><span class="sxs-lookup"><span data-stu-id="3411e-172">transactionFlow</span></span>|<span data-ttu-id="3411e-173">一个布尔值，指定绑定是否支持流动 WS-Transactions。</span><span class="sxs-lookup"><span data-stu-id="3411e-173">A Boolean value that specifies whether the binding supports flowing WS-Transactions.</span></span> <span data-ttu-id="3411e-174">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="3411e-174">The default is `false`.</span></span>|
|<span data-ttu-id="3411e-175">useDefaultWebProxy</span><span class="sxs-lookup"><span data-stu-id="3411e-175">useDefaultWebProxy</span></span>|<span data-ttu-id="3411e-176">一个布尔值，指示是否使用系统的自动配置 HTTP 代理。</span><span class="sxs-lookup"><span data-stu-id="3411e-176">A Boolean value that indicates whether the system’s auto-configured HTTP proxy is used.</span></span> <span data-ttu-id="3411e-177">如果此属性为 `null`，则代理地址必须为 `true`（即，不设置代理地址）。</span><span class="sxs-lookup"><span data-stu-id="3411e-177">The proxy address must be `null` (that is, not set) if this attribute is `true`.</span></span> <span data-ttu-id="3411e-178">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="3411e-178">The default is `true`.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="3411e-179">子元素</span><span class="sxs-lookup"><span data-stu-id="3411e-179">Child Elements</span></span>

|<span data-ttu-id="3411e-180">元素</span><span class="sxs-lookup"><span data-stu-id="3411e-180">Element</span></span>|<span data-ttu-id="3411e-181">说明</span><span class="sxs-lookup"><span data-stu-id="3411e-181">Description</span></span>|
|-------------|-----------------|
|[\<security>](security-of-wsfederationhttpbinding.md)|<span data-ttu-id="3411e-182">定义消息的安全设置。</span><span class="sxs-lookup"><span data-stu-id="3411e-182">Defines the security settings for the message.</span></span> <span data-ttu-id="3411e-183">此元素的类型为 <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="3411e-183">This element is of type <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>.</span></span>|
|[\<readerQuotas>](/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="3411e-184">定义可由采用此绑定配置的终结点进行处理的 SOAP 消息的复杂性约束。</span><span class="sxs-lookup"><span data-stu-id="3411e-184">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="3411e-185">此元素的类型为 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>。</span><span class="sxs-lookup"><span data-stu-id="3411e-185">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|
|[\<reliableSession>](/previous-versions/ms731375(v=vs.90))|<span data-ttu-id="3411e-186">指定是否在通道终结点之间建立可靠会话。</span><span class="sxs-lookup"><span data-stu-id="3411e-186">Specifies if reliable sessions are established between channel endpoints.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="3411e-187">父元素</span><span class="sxs-lookup"><span data-stu-id="3411e-187">Parent Elements</span></span>

|<span data-ttu-id="3411e-188">元素</span><span class="sxs-lookup"><span data-stu-id="3411e-188">Element</span></span>|<span data-ttu-id="3411e-189">说明</span><span class="sxs-lookup"><span data-stu-id="3411e-189">Description</span></span>|
|-------------|-----------------|
|[\<bindings>](bindings.md)|<span data-ttu-id="3411e-190">此元素包含标准绑定和自定义绑定的集合。</span><span class="sxs-lookup"><span data-stu-id="3411e-190">This element holds a collection of standard and custom bindings.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3411e-191">备注</span><span class="sxs-lookup"><span data-stu-id="3411e-191">Remarks</span></span>

<span data-ttu-id="3411e-192">联合是一种可以在多个系统通过共享标识进行身份验证和授权的功能。</span><span class="sxs-lookup"><span data-stu-id="3411e-192">Federation is the ability to share identities across multiple systems for authentication and authorization.</span></span> <span data-ttu-id="3411e-193">这些标识可以指用户，也可以指计算机。</span><span class="sxs-lookup"><span data-stu-id="3411e-193">These identities can refer to users or to machines.</span></span> <span data-ttu-id="3411e-194">联合 HTTP 支持 SOAP 安全以及混合模式安全，但不支持以独占方式使用传输安全。</span><span class="sxs-lookup"><span data-stu-id="3411e-194">Federated HTTP supports SOAP security as well as mixed-mode security, but it does not support exclusively using transport security.</span></span> <span data-ttu-id="3411e-195">此绑定为 WS-Federation 协议提供 Windows Communication Foundation (WCF) 支持。</span><span class="sxs-lookup"><span data-stu-id="3411e-195">This binding provides Windows Communication Foundation (WCF) support for the WS-Federation protocol.</span></span> <span data-ttu-id="3411e-196">配置了此绑定的服务必须使用 HTTP 传输。</span><span class="sxs-lookup"><span data-stu-id="3411e-196">Services configured with this binding must use the HTTP transport.</span></span>

<span data-ttu-id="3411e-197">绑定由绑定元素堆栈组成。</span><span class="sxs-lookup"><span data-stu-id="3411e-197">Bindings consist of a stack of binding elements.</span></span> <span data-ttu-id="3411e-198">满足下面的条件时，</span><span class="sxs-lookup"><span data-stu-id="3411e-198">The stack of binding elements in</span></span>

<span data-ttu-id="3411e-199">`wsFederationHttpBinding` 中的绑定元素的堆栈与 `wsHttpBinding`</span><span class="sxs-lookup"><span data-stu-id="3411e-199">`wsFederationHttpBinding` is the same as that contained in `wsHttpBinding`</span></span>

<span data-ttu-id="3411e-200">当 [\<security>](security-of-wsfederationhttpbinding.md) 设置为的默认值时 <xref:System.ServiceModel.WSFederationHttpSecurityMode.Message> 。</span><span class="sxs-lookup"><span data-stu-id="3411e-200">when [\<security>](security-of-wsfederationhttpbinding.md) is set to the default value of <xref:System.ServiceModel.WSFederationHttpSecurityMode.Message>.</span></span>

<span data-ttu-id="3411e-201">`wsFederationHttpBinding`控制中消息安全设置的详细信息 [\<message>](message-element-of-wsfederationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="3411e-201">The `wsFederationHttpBinding` controls the details of the message security settings in [\<message>](message-element-of-wsfederationhttpbinding.md).</span></span> <span data-ttu-id="3411e-202">请注意， [\<security>](security-of-wsfederationhttpbinding.md) 元素只提供 get 访问权限，因为在创建绑定后，不能更改绑定使用的安全性。</span><span class="sxs-lookup"><span data-stu-id="3411e-202">Note that the [\<security>](security-of-wsfederationhttpbinding.md) element provides get access only as the security used by the binding cannot be changed once the binding is created.</span></span>

<span data-ttu-id="3411e-203">`wsFederationHttpBinding`还提供了一个 privacyNoticeAt 属性，用于设置和检索隐私声明所在的 URI。</span><span class="sxs-lookup"><span data-stu-id="3411e-203">The `wsFederationHttpBinding` also provides a privacyNoticeAt attribute to set and retrieve the URI at which the privacy notice is located.</span></span>

<span data-ttu-id="3411e-204">保持策略安全在联合方案中特别重要。</span><span class="sxs-lookup"><span data-stu-id="3411e-204">Keeping policy secure is especially important in federation scenarios.</span></span> <span data-ttu-id="3411e-205">建议使用某种形式的安全机制（如 HTTPS）以防止策略遭受恶意用户的攻击。</span><span class="sxs-lookup"><span data-stu-id="3411e-205">The recommendation is to use some form of security, such as HTTPS, to protect the policy from malicious users.</span></span>

<span data-ttu-id="3411e-206">在使用此绑定的联合方案中，服务策略可能具有重要信息，例如要用于对颁发的 (SAML) 令牌进行加密的密钥和要放置在令牌中的声明的类型等等。</span><span class="sxs-lookup"><span data-stu-id="3411e-206">In federation scenarios using this binding, the service policy potentially has important information such as the key to use to encrypt the issued (SAML) token, the type of claims to put in the token, and so forth.</span></span> <span data-ttu-id="3411e-207">如果此策略被篡改，则攻击者可能会发现已颁发令牌的密钥，从而导致策略被进一步篡改、信息泄露和其他恶意行为。</span><span class="sxs-lookup"><span data-stu-id="3411e-207">If this policy is tampered with, an attacker could discover the key of the issued token leading to further tampering, info disclosure and other malicious behavior.</span></span> <span data-ttu-id="3411e-208">为了帮助防止此情况发生，必须从服务中安全地（例如使用 HTTPS）获取策略。</span><span class="sxs-lookup"><span data-stu-id="3411e-208">To help prevent this, the policy must be obtained securely (for example using HTTPS) from the service.</span></span>

<span data-ttu-id="3411e-209">有关此绑定的详细信息，请参阅 [如何：创建 WSFederationHttpBinding](../../../wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)。</span><span class="sxs-lookup"><span data-stu-id="3411e-209">For more information on this binding, see [How to: Create a WSFederationHttpBinding](../../../wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md).</span></span>

## <a name="example"></a><span data-ttu-id="3411e-210">示例</span><span class="sxs-lookup"><span data-stu-id="3411e-210">Example</span></span>

```xml
<configuration>
  <system.ServiceModel>
    <bindings>
      <wsFederationHttpBinding>
        <binding bypassProxyOnLocal="false"
                 transactionFlow="false"
                 hostNameComparisonMode="WeakWildcard"
                 maxReceivedMessageSize="1000"
                 messageEncoding="Mtom"
                 proxyAddress="http://foo/bar"
                 textEncoding="Utf16TextEncoding"
                 useDefaultWebProxy="false">
          <reliableSession ordered="false"
                           inactivityTimeout="00:02:00"
                           enabled="true" />
          <security mode="None">
            <message negotiateServiceCredential="false"
                     algorithmSuite="Aes128"
                     issuedTokenType="saml"
                     issuedKeyType="PublicKey">
              <issuer address="http://localhost/Sts" />
            </message>
          </security>
        </binding>
      </wsFederationBinding>
    </bindings>
  </system.ServiceModel>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="3411e-211">请参阅</span><span class="sxs-lookup"><span data-stu-id="3411e-211">See also</span></span>

- <xref:System.ServiceModel.WSFederationHttpBinding>
- <xref:System.ServiceModel.Configuration.WSFederationHttpBindingElement>
- [<span data-ttu-id="3411e-212">如何：创建 WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="3411e-212">How to: Create a WSFederationHttpBinding</span></span>](../../../wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)
- [<span data-ttu-id="3411e-213">绑定</span><span class="sxs-lookup"><span data-stu-id="3411e-213">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="3411e-214">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="3411e-214">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="3411e-215">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="3411e-215">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

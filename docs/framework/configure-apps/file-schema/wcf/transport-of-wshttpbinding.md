---
description: 了解详细 <transport> 信息： <wsHttpBinding>
title: <transport> 的 <wsHttpBinding>
ms.date: 03/30/2017
ms.assetid: 21e38acf-450a-4bda-82b6-de305e1f7cd8
ms.openlocfilehash: 7801148d76aaa9c074eeb7a83c1dd2fa152d871c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749293"
---
# <a name="transport-of-wshttpbinding"></a><span data-ttu-id="dad3d-103">\<transport> 的 \<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="dad3d-103">\<transport> of \<wsHttpBinding></span></span>

<span data-ttu-id="dad3d-104">定义 HTTP 传输的身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="dad3d-104">Defines authentication settings for the HTTP transport.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsHttpBinding>**](wshttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wshttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  

## <a name="syntax"></a><span data-ttu-id="dad3d-105">语法</span><span class="sxs-lookup"><span data-stu-id="dad3d-105">Syntax</span></span>

```xml
<wsHttpBinding>
  <binding>
    <security mode="None|Transport|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="Basic|Certificate|Digest|None|Ntlm|Windows"
                 proxyCredentialType="Basic|Digest|None|Ntlm|Windows"
                 realm="string" />
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</wsHttpBinding>
```

## <a name="type"></a><span data-ttu-id="dad3d-106">类型</span><span class="sxs-lookup"><span data-stu-id="dad3d-106">Type</span></span>

<xref:System.ServiceModel.HttpTransportSecurity>

## <a name="attributes-and-elements"></a><span data-ttu-id="dad3d-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="dad3d-107">Attributes and Elements</span></span>

<span data-ttu-id="dad3d-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dad3d-108">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="dad3d-109">特性</span><span class="sxs-lookup"><span data-stu-id="dad3d-109">Attributes</span></span>

|<span data-ttu-id="dad3d-110">属性</span><span class="sxs-lookup"><span data-stu-id="dad3d-110">Attribute</span></span>|<span data-ttu-id="dad3d-111">说明</span><span class="sxs-lookup"><span data-stu-id="dad3d-111">Description</span></span>|
|---------------|-----------------|
|`clientCredentialType`|<span data-ttu-id="dad3d-112">指定用于向服务证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="dad3d-112">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="dad3d-113">此属性的类型为 <xref:System.ServiceModel.HttpClientCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="dad3d-113">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|
|`proxyCredentialType`|<span data-ttu-id="dad3d-114">指定用于向域代理证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="dad3d-114">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="dad3d-115">此属性的类型为 <xref:System.ServiceModel.HttpProxyCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="dad3d-115">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|
|`realm`|<span data-ttu-id="dad3d-116">一个字符串，指定摘要式或基本身份验证的身份验证领域。</span><span class="sxs-lookup"><span data-stu-id="dad3d-116">A string that specifies the authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="dad3d-117">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="dad3d-117">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="dad3d-118">身份验证领域至少指定执行身份验证的主机的名称。</span><span class="sxs-lookup"><span data-stu-id="dad3d-118">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="dad3d-119">它还可以指定具有访问权限的用户的集合。</span><span class="sxs-lookup"><span data-stu-id="dad3d-119">It can also specify a collection of users that has access.</span></span> <span data-ttu-id="dad3d-120">用户可以查询身份验证领域，以确定多个可能的用户名和密码中哪一个可以使用。</span><span class="sxs-lookup"><span data-stu-id="dad3d-120">A user can query the authentication realm to ascertain which one of the several possible usernames and passwords can be used.</span></span>|
|`policyEnforcement`|<span data-ttu-id="dad3d-121">此枚举指定应何时强制实施 <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy>。</span><span class="sxs-lookup"><span data-stu-id="dad3d-121">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="dad3d-122">1. 从不–不会强制实施策略 (禁用扩展保护) 。</span><span class="sxs-lookup"><span data-stu-id="dad3d-122">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="dad3d-123">WhenSupported-仅当客户端支持扩展保护时才强制实施策略。</span><span class="sxs-lookup"><span data-stu-id="dad3d-123">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="dad3d-124">3. always –始终强制实施策略。</span><span class="sxs-lookup"><span data-stu-id="dad3d-124">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="dad3d-125">不支持扩展保护的客户端将无法进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-125">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|

## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="dad3d-126">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="dad3d-126">clientCredentialType Attribute</span></span>

|<span data-ttu-id="dad3d-127">值</span><span class="sxs-lookup"><span data-stu-id="dad3d-127">Value</span></span>|<span data-ttu-id="dad3d-128">说明</span><span class="sxs-lookup"><span data-stu-id="dad3d-128">Description</span></span>|
|-----------|-----------------|
|`None`|<span data-ttu-id="dad3d-129">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="dad3d-129">Security is disabled.</span></span>|
|`Basic`|<span data-ttu-id="dad3d-130">使用基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-130">Uses basic authentication.</span></span>|
|`Digest`|<span data-ttu-id="dad3d-131">使用摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-131">Uses digest authentication.</span></span>|
|`Ntlm`|<span data-ttu-id="dad3d-132">对 Windows 域使用 NTLM 身份验证作为回退。</span><span class="sxs-lookup"><span data-stu-id="dad3d-132">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|
|`Windows`|<span data-ttu-id="dad3d-133">使用集成 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-133">Uses integrated Windows authentication.</span></span>|
|`Certificate`|<span data-ttu-id="dad3d-134">使用 X.509 证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-134">Uses X.509 certificates to authenticate the client.</span></span>|

## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="dad3d-135">proxyCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="dad3d-135">proxyCredentialType Attribute</span></span>

|<span data-ttu-id="dad3d-136">值</span><span class="sxs-lookup"><span data-stu-id="dad3d-136">Value</span></span>|<span data-ttu-id="dad3d-137">说明</span><span class="sxs-lookup"><span data-stu-id="dad3d-137">Description</span></span>|
|-----------|-----------------|
|`None`|<span data-ttu-id="dad3d-138">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="dad3d-138">Security is disabled.</span></span>|
|`Basic`|<span data-ttu-id="dad3d-139">使用基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-139">Uses basic authentication.</span></span>|
|`Digest`|<span data-ttu-id="dad3d-140">使用摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-140">Uses digest authentication.</span></span>|
|`Ntlm`|<span data-ttu-id="dad3d-141">对 Windows 域使用 NTLM 作为回退。</span><span class="sxs-lookup"><span data-stu-id="dad3d-141">Uses NTLM as a fallback with a Windows domain.</span></span>|
|`Windows`|<span data-ttu-id="dad3d-142">使用集成 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-142">Uses integrated Windows authentication.</span></span>|
|`Certificate`|<span data-ttu-id="dad3d-143">使用 X.509 证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="dad3d-143">Uses X.509 certificates to authenticate the client.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="dad3d-144">子元素</span><span class="sxs-lookup"><span data-stu-id="dad3d-144">Child Elements</span></span>

<span data-ttu-id="dad3d-145">无。</span><span class="sxs-lookup"><span data-stu-id="dad3d-145">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="dad3d-146">父元素</span><span class="sxs-lookup"><span data-stu-id="dad3d-146">Parent Elements</span></span>

|<span data-ttu-id="dad3d-147">元素</span><span class="sxs-lookup"><span data-stu-id="dad3d-147">Element</span></span>|<span data-ttu-id="dad3d-148">说明</span><span class="sxs-lookup"><span data-stu-id="dad3d-148">Description</span></span>|
|-------------|-----------------|
|[\<security>](security-of-wshttpbinding.md)|<span data-ttu-id="dad3d-149">表示的安全功能 [\<wsHttpBinding>](wshttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="dad3d-149">Represents the security capabilities of the [\<wsHttpBinding>](wshttpbinding.md).</span></span>|

## <a name="see-also"></a><span data-ttu-id="dad3d-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="dad3d-150">See also</span></span>

- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- [<span data-ttu-id="dad3d-151">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="dad3d-151">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="dad3d-152">绑定</span><span class="sxs-lookup"><span data-stu-id="dad3d-152">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="dad3d-153">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="dad3d-153">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="dad3d-154">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="dad3d-154">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

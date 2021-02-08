---
description: 了解详细 <transport> 信息： <ws2007HttpBinding>
title: <transport> 的 <ws2007HttpBinding>
ms.date: 03/30/2017
ms.assetid: 692befa3-8b0b-4ec5-b601-755874e98eb0
ms.openlocfilehash: 8c6890bc291458ba0849ab7a206487431b279576
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773428"
---
# <a name="transport-of-ws2007httpbinding"></a><span data-ttu-id="92eb8-103">\<transport> 的 \<ws2007HttpBinding></span><span class="sxs-lookup"><span data-stu-id="92eb8-103">\<transport> of \<ws2007HttpBinding></span></span>

<span data-ttu-id="92eb8-104">定义 HTTP 传输的身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="92eb8-104">Defines authentication settings for the HTTP transport.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<ws2007HttpBinding>**](ws2007httpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-ws2007httpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="92eb8-105">语法</span><span class="sxs-lookup"><span data-stu-id="92eb8-105">Syntax</span></span>  
  
```xml  
<transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
           proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
           realm="string" />
```  
  
## <a name="type"></a><span data-ttu-id="92eb8-106">类型</span><span class="sxs-lookup"><span data-stu-id="92eb8-106">Type</span></span>  

 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="92eb8-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="92eb8-107">Attributes and Elements</span></span>  

 <span data-ttu-id="92eb8-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92eb8-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="92eb8-109">特性</span><span class="sxs-lookup"><span data-stu-id="92eb8-109">Attributes</span></span>  
  
|<span data-ttu-id="92eb8-110">属性</span><span class="sxs-lookup"><span data-stu-id="92eb8-110">Attribute</span></span>|<span data-ttu-id="92eb8-111">说明</span><span class="sxs-lookup"><span data-stu-id="92eb8-111">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="92eb8-112">指定用于向服务证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="92eb8-112">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="92eb8-113">此属性的类型为 <xref:System.ServiceModel.HttpClientCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="92eb8-113">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="92eb8-114">指定用于向域代理证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="92eb8-114">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="92eb8-115">此属性的类型为 <xref:System.ServiceModel.HttpProxyCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="92eb8-115">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="92eb8-116">摘要式或基本身份验证的身份验证领域。</span><span class="sxs-lookup"><span data-stu-id="92eb8-116">The authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="92eb8-117">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="92eb8-117">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="92eb8-118">身份验证领域至少指定执行身份验证的主机的名称。</span><span class="sxs-lookup"><span data-stu-id="92eb8-118">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="92eb8-119">它还可以指定具有访问权限的用户集合。</span><span class="sxs-lookup"><span data-stu-id="92eb8-119">It can also specify a collection of users who have access.</span></span> <span data-ttu-id="92eb8-120">用户可以查询身份验证领域，以确定多个可能的用户名和密码中哪一个可以使用。</span><span class="sxs-lookup"><span data-stu-id="92eb8-120">A user can query the authentication realm to determine which one of the several possible usernames and passwords can be used.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="92eb8-121">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="92eb8-121">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="92eb8-122">值</span><span class="sxs-lookup"><span data-stu-id="92eb8-122">Value</span></span>|<span data-ttu-id="92eb8-123">说明</span><span class="sxs-lookup"><span data-stu-id="92eb8-123">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="92eb8-124">无</span><span class="sxs-lookup"><span data-stu-id="92eb8-124">None</span></span>|<span data-ttu-id="92eb8-125">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="92eb8-125">Security is disabled.</span></span>|  
|<span data-ttu-id="92eb8-126">基本</span><span class="sxs-lookup"><span data-stu-id="92eb8-126">Basic</span></span>|<span data-ttu-id="92eb8-127">使用基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-127">Uses basic authentication.</span></span>|  
|<span data-ttu-id="92eb8-128">摘要</span><span class="sxs-lookup"><span data-stu-id="92eb8-128">Digest</span></span>|<span data-ttu-id="92eb8-129">使用摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-129">Uses digest authentication.</span></span>|  
|<span data-ttu-id="92eb8-130">Ntlm</span><span class="sxs-lookup"><span data-stu-id="92eb8-130">Ntlm</span></span>|<span data-ttu-id="92eb8-131">对 Windows 域使用 NTLM 身份验证作为回退。</span><span class="sxs-lookup"><span data-stu-id="92eb8-131">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="92eb8-132">Windows</span><span class="sxs-lookup"><span data-stu-id="92eb8-132">Windows</span></span>|<span data-ttu-id="92eb8-133">使用集成 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-133">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="92eb8-134">证书</span><span class="sxs-lookup"><span data-stu-id="92eb8-134">Certificate</span></span>|<span data-ttu-id="92eb8-135">使用 X.509 证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-135">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="92eb8-136">proxyCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="92eb8-136">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="92eb8-137">值</span><span class="sxs-lookup"><span data-stu-id="92eb8-137">Value</span></span>|<span data-ttu-id="92eb8-138">说明</span><span class="sxs-lookup"><span data-stu-id="92eb8-138">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="92eb8-139">无</span><span class="sxs-lookup"><span data-stu-id="92eb8-139">None</span></span>|<span data-ttu-id="92eb8-140">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="92eb8-140">Security is disabled.</span></span>|  
|<span data-ttu-id="92eb8-141">基本</span><span class="sxs-lookup"><span data-stu-id="92eb8-141">Basic</span></span>|<span data-ttu-id="92eb8-142">使用基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-142">Uses basic authentication.</span></span>|  
|<span data-ttu-id="92eb8-143">摘要</span><span class="sxs-lookup"><span data-stu-id="92eb8-143">Digest</span></span>|<span data-ttu-id="92eb8-144">使用摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-144">Uses digest authentication.</span></span>|  
|<span data-ttu-id="92eb8-145">Ntlm</span><span class="sxs-lookup"><span data-stu-id="92eb8-145">Ntlm</span></span>|<span data-ttu-id="92eb8-146">对 Windows 域使用 NTLM 作为回退。</span><span class="sxs-lookup"><span data-stu-id="92eb8-146">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="92eb8-147">Windows</span><span class="sxs-lookup"><span data-stu-id="92eb8-147">Windows</span></span>|<span data-ttu-id="92eb8-148">使用集成 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-148">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="92eb8-149">证书</span><span class="sxs-lookup"><span data-stu-id="92eb8-149">Certificate</span></span>|<span data-ttu-id="92eb8-150">使用 X.509 证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="92eb8-150">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="92eb8-151">子元素</span><span class="sxs-lookup"><span data-stu-id="92eb8-151">Child Elements</span></span>  

 <span data-ttu-id="92eb8-152">无</span><span class="sxs-lookup"><span data-stu-id="92eb8-152">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="92eb8-153">父元素</span><span class="sxs-lookup"><span data-stu-id="92eb8-153">Parent Elements</span></span>  
  
|<span data-ttu-id="92eb8-154">元素</span><span class="sxs-lookup"><span data-stu-id="92eb8-154">Element</span></span>|<span data-ttu-id="92eb8-155">说明</span><span class="sxs-lookup"><span data-stu-id="92eb8-155">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-ws2007httpbinding.md)|<span data-ttu-id="92eb8-156">表示元素的安全功能 [\<ws2007HttpBinding>](ws2007httpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="92eb8-156">Represents the security capabilities of the [\<ws2007HttpBinding>](ws2007httpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="92eb8-157">请参阅</span><span class="sxs-lookup"><span data-stu-id="92eb8-157">See also</span></span>

- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.WSHttpTransportSecurityElement>
- [<span data-ttu-id="92eb8-158">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="92eb8-158">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="92eb8-159">绑定</span><span class="sxs-lookup"><span data-stu-id="92eb8-159">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="92eb8-160">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="92eb8-160">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="92eb8-161">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="92eb8-161">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

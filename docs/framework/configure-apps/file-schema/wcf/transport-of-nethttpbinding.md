---
description: 了解详细 <transport> 信息： <netHttpBinding>
title: <transport> 的 <netHttpBinding>
ms.date: 03/30/2017
ms.assetid: 3b180006-1661-43bf-a699-96fd3da469af
ms.openlocfilehash: 1c2029fcbc57632b828fa180ba0ffbbf6b974775
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773506"
---
# <a name="transport-of-nethttpbinding"></a><span data-ttu-id="55fa2-103">\<transport> 的 \<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="55fa2-103">\<transport> of \<netHttpBinding></span></span>

<span data-ttu-id="55fa2-104">为 HTTP 传输定义控制身份验证参数的属性。</span><span class="sxs-lookup"><span data-stu-id="55fa2-104">Defines properties that control authentication parameters for the HTTP transport.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netHttpBinding>**](nethttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-nethttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="55fa2-105">语法</span><span class="sxs-lookup"><span data-stu-id="55fa2-105">Syntax</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <security mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"
                 proxyCredentialType="None|Basic|Digest|Ntlm|Windows"
                 realm="string">
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</netHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="55fa2-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="55fa2-106">Attributes and Elements</span></span>  

 <span data-ttu-id="55fa2-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="55fa2-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="55fa2-108">特性</span><span class="sxs-lookup"><span data-stu-id="55fa2-108">Attributes</span></span>  
  
|<span data-ttu-id="55fa2-109">属性</span><span class="sxs-lookup"><span data-stu-id="55fa2-109">Attribute</span></span>|<span data-ttu-id="55fa2-110">说明</span><span class="sxs-lookup"><span data-stu-id="55fa2-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="55fa2-111">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="55fa2-111">clientCredentialType</span></span>|<span data-ttu-id="55fa2-112">-指定执行使用 HTTP 身份验证的客户端身份验证时要使用的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="55fa2-112">-   Specifies the type of credential to be used when performing client authentication using HTTP authentication.</span></span>  <span data-ttu-id="55fa2-113">默认值为 `None`。</span><span class="sxs-lookup"><span data-stu-id="55fa2-113">The default is `None`.</span></span> <span data-ttu-id="55fa2-114">此属性的类型为 <xref:System.ServiceModel.HttpClientCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="55fa2-114">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|<span data-ttu-id="55fa2-115">proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="55fa2-115">proxyCredentialType</span></span>|<span data-ttu-id="55fa2-116">-指定使用代理通过 HTTP 在域中执行客户端身份验证时使用的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="55fa2-116">-   Specifies the type of credential to be used when performing client authentication from within a domain using a proxy over HTTP.</span></span> <span data-ttu-id="55fa2-117">只有当父 `mode` 元素的 `security` 属性为 `Transport` 或 `TransportCredentialsOnly` 时，此属性才适用。</span><span class="sxs-lookup"><span data-stu-id="55fa2-117">This attribute is applicable only when the `mode` attribute of the parent `security` element is `Transport` or `TransportCredentialsOnly`.</span></span> <span data-ttu-id="55fa2-118">此属性的类型为 <xref:System.ServiceModel.HttpProxyCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="55fa2-118">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|<span data-ttu-id="55fa2-119">realm</span><span class="sxs-lookup"><span data-stu-id="55fa2-119">realm</span></span>|<span data-ttu-id="55fa2-120">一个字符串，指定摘要式或基本身份验证的 HTTP 身份验证方案所使用的领域。</span><span class="sxs-lookup"><span data-stu-id="55fa2-120">A string that specifies the realm that is used by the HTTP authentication scheme for digest or basic authentication.</span></span> <span data-ttu-id="55fa2-121">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="55fa2-121">The default is an empty string.</span></span>|  
|<span data-ttu-id="55fa2-122">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="55fa2-122">policyEnforcement</span></span>|<span data-ttu-id="55fa2-123">此枚举指定应何时强制实施 <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy>。</span><span class="sxs-lookup"><span data-stu-id="55fa2-123">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="55fa2-124">1. 从不–不会强制实施策略 (禁用扩展保护) 。</span><span class="sxs-lookup"><span data-stu-id="55fa2-124">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="55fa2-125">WhenSupported-仅当客户端支持扩展保护时才强制实施策略。</span><span class="sxs-lookup"><span data-stu-id="55fa2-125">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="55fa2-126">3. always –始终强制实施策略。</span><span class="sxs-lookup"><span data-stu-id="55fa2-126">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="55fa2-127">不支持扩展保护的客户端将无法进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-127">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
|<span data-ttu-id="55fa2-128">protectionScenario</span><span class="sxs-lookup"><span data-stu-id="55fa2-128">protectionScenario</span></span>|<span data-ttu-id="55fa2-129">此枚举指定此策略强制实施的保护方案。</span><span class="sxs-lookup"><span data-stu-id="55fa2-129">This enumeration specifies the protection scenario enforced by the policy.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="55fa2-130">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="55fa2-130">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="55fa2-131">值</span><span class="sxs-lookup"><span data-stu-id="55fa2-131">Value</span></span>|<span data-ttu-id="55fa2-132">说明</span><span class="sxs-lookup"><span data-stu-id="55fa2-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="55fa2-133">无</span><span class="sxs-lookup"><span data-stu-id="55fa2-133">None</span></span>|<span data-ttu-id="55fa2-134">在传输过程中不能保证消息的安全。</span><span class="sxs-lookup"><span data-stu-id="55fa2-134">Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="55fa2-135">基本</span><span class="sxs-lookup"><span data-stu-id="55fa2-135">Basic</span></span>|<span data-ttu-id="55fa2-136">指定基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-136">Specifies basic authentication.</span></span>|  
|<span data-ttu-id="55fa2-137">摘要</span><span class="sxs-lookup"><span data-stu-id="55fa2-137">Digest</span></span>|<span data-ttu-id="55fa2-138">指定摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-138">Specifies digest authentication.</span></span>|  
|<span data-ttu-id="55fa2-139">Ntlm</span><span class="sxs-lookup"><span data-stu-id="55fa2-139">Ntlm</span></span>|<span data-ttu-id="55fa2-140">指定 NTLM 身份验证（如果可能且 Windows 身份验证失败）。</span><span class="sxs-lookup"><span data-stu-id="55fa2-140">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="55fa2-141">Windows</span><span class="sxs-lookup"><span data-stu-id="55fa2-141">Windows</span></span>|<span data-ttu-id="55fa2-142">指定 Windows 集成身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-142">Specifies Windows integrated authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="55fa2-143">proxyCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="55fa2-143">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="55fa2-144">值</span><span class="sxs-lookup"><span data-stu-id="55fa2-144">Value</span></span>|<span data-ttu-id="55fa2-145">说明</span><span class="sxs-lookup"><span data-stu-id="55fa2-145">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="55fa2-146">无</span><span class="sxs-lookup"><span data-stu-id="55fa2-146">None</span></span>|<span data-ttu-id="55fa2-147">-传输过程中消息不受保护。</span><span class="sxs-lookup"><span data-stu-id="55fa2-147">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="55fa2-148">基本</span><span class="sxs-lookup"><span data-stu-id="55fa2-148">Basic</span></span>|<span data-ttu-id="55fa2-149">指定“RFC 2617 – HTTP 身份验证：基本和摘要式身份验证”所定义的基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-149">Specifies basic authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="55fa2-150">摘要</span><span class="sxs-lookup"><span data-stu-id="55fa2-150">Digest</span></span>|<span data-ttu-id="55fa2-151">指定“RFC 2617 – HTTP 身份验证：基本和摘要式身份验证”所定义的摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-151">Specifies digest authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="55fa2-152">Ntlm</span><span class="sxs-lookup"><span data-stu-id="55fa2-152">Ntlm</span></span>|<span data-ttu-id="55fa2-153">指定 NTLM 身份验证（如果可能且 Windows 身份验证失败）。</span><span class="sxs-lookup"><span data-stu-id="55fa2-153">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="55fa2-154">Windows</span><span class="sxs-lookup"><span data-stu-id="55fa2-154">Windows</span></span>|<span data-ttu-id="55fa2-155">指定 Windows 集成身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-155">Specifies Windows integrated authentication.</span></span>|  
|<span data-ttu-id="55fa2-156">证书</span><span class="sxs-lookup"><span data-stu-id="55fa2-156">Certificate</span></span>|<span data-ttu-id="55fa2-157">使用证书执行客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="55fa2-157">Performs client authentication using a certificate.</span></span> <span data-ttu-id="55fa2-158">此选项只在父 `Mode` 元素的 `security` 属性设置为“Transport”时才起作用，如果该属性设置为“TransportCredentialOnly”，则此选项将不起作用。</span><span class="sxs-lookup"><span data-stu-id="55fa2-158">This option works only if the `Mode` attribute of the parent `security` element is set to Transport, and will not work if it is set to TransportCredentialOnly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="55fa2-159">子元素</span><span class="sxs-lookup"><span data-stu-id="55fa2-159">Child Elements</span></span>  

 <span data-ttu-id="55fa2-160">无</span><span class="sxs-lookup"><span data-stu-id="55fa2-160">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="55fa2-161">父元素</span><span class="sxs-lookup"><span data-stu-id="55fa2-161">Parent Elements</span></span>  
  
|<span data-ttu-id="55fa2-162">元素</span><span class="sxs-lookup"><span data-stu-id="55fa2-162">Element</span></span>|<span data-ttu-id="55fa2-163">说明</span><span class="sxs-lookup"><span data-stu-id="55fa2-163">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-nethttpbinding.md)|<span data-ttu-id="55fa2-164">定义的安全功能 [\<netHttpBinding>](nethttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="55fa2-164">Defines the security capabilities for the [\<netHttpBinding>](nethttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="55fa2-165">示例</span><span class="sxs-lookup"><span data-stu-id="55fa2-165">Example</span></span>  

 <span data-ttu-id="55fa2-166">下面的示例演示如何对基本绑定使用 SSL 传输安全。</span><span class="sxs-lookup"><span data-stu-id="55fa2-166">The following example demonstrates the use of SSL transport security with the basic binding.</span></span> <span data-ttu-id="55fa2-167">默认情况下，基本绑定支持 HTTP 通信。</span><span class="sxs-lookup"><span data-stu-id="55fa2-167">By default, the basic binding supports HTTP communication.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service type="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <endpoint address=""
                binding="netHttpBinding"
                bindingConfiguration="Binding1"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
    </service>
  </services>
  <bindings>
    <netHttpBinding>
      <!-- Configure basicHttpBinding with Transport security -->
      <!-- mode and clientCredentialType set to None. -->
      <binding name="Binding1">
        <security mode="Transport">
          <transport clientCredentialType="None"
                     proxyCredentialType="None">
            <extendedProtectionPolicy policyEnforcement="WhenSupported"
                                      protectionScenario="TransportSelected">
              <customServiceNames>
              </customServiceNames>
            </extendedProtectionPolicy>
          </transport>
        </security>
      </binding>
    </netHttpBinding>
  </bindings>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="55fa2-168">请参阅</span><span class="sxs-lookup"><span data-stu-id="55fa2-168">See also</span></span>

- <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- <xref:System.ServiceModel.HttpTransportSecurity>
- [<span data-ttu-id="55fa2-169">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="55fa2-169">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="55fa2-170">绑定</span><span class="sxs-lookup"><span data-stu-id="55fa2-170">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="55fa2-171">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="55fa2-171">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="55fa2-172">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="55fa2-172">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)

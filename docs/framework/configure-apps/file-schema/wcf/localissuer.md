---
description: 了解详细信息： <localIssuer>
title: <localIssuer>
ms.date: 03/30/2017
ms.assetid: 26bdd0df-0e7d-4b9e-bbeb-f28c53769385
ms.openlocfilehash: 38928f1bfd7740aa902de46958740a1e8fe63e5a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725475"
---
# \<localIssuer>

<span data-ttu-id="af35f-102">指定要用于颁发安全令牌的本地颁发者的地址和绑定。</span><span class="sxs-lookup"><span data-stu-id="af35f-102">Specifies the address and binding of the local issuer to be used to obtain a security token.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<issuedToken>**](issuedtoken.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<localIssuer>**  
  
## <a name="syntax"></a><span data-ttu-id="af35f-103">语法</span><span class="sxs-lookup"><span data-stu-id="af35f-103">Syntax</span></span>  
  
```xml  
<localIssuer address="String"
             binding="String"
             bindingConfiguration="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="af35f-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="af35f-104">Attributes and Elements</span></span>  

 <span data-ttu-id="af35f-105">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af35f-105">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="af35f-106">特性</span><span class="sxs-lookup"><span data-stu-id="af35f-106">Attributes</span></span>  
  
|<span data-ttu-id="af35f-107">属性</span><span class="sxs-lookup"><span data-stu-id="af35f-107">Attribute</span></span>|<span data-ttu-id="af35f-108">说明</span><span class="sxs-lookup"><span data-stu-id="af35f-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="af35f-109">address</span><span class="sxs-lookup"><span data-stu-id="af35f-109">address</span></span>|<span data-ttu-id="af35f-110">必选字符串。</span><span class="sxs-lookup"><span data-stu-id="af35f-110">Required string.</span></span> <span data-ttu-id="af35f-111">指定本地颁发者的 URI。</span><span class="sxs-lookup"><span data-stu-id="af35f-111">Specifies the URI of the local issuer.</span></span>|  
|<span data-ttu-id="af35f-112">binding</span><span class="sxs-lookup"><span data-stu-id="af35f-112">binding</span></span>|<span data-ttu-id="af35f-113">可选的字符串。</span><span class="sxs-lookup"><span data-stu-id="af35f-113">Optional string.</span></span> <span data-ttu-id="af35f-114">系统提供的一个绑定。</span><span class="sxs-lookup"><span data-stu-id="af35f-114">One of the system-provided bindings.</span></span> <span data-ttu-id="af35f-115">有关列表，请参阅 [系统提供的绑定](../../../wcf/system-provided-bindings.md)。</span><span class="sxs-lookup"><span data-stu-id="af35f-115">For a list, see [System-Provided Bindings](../../../wcf/system-provided-bindings.md).</span></span>|  
|<span data-ttu-id="af35f-116">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="af35f-116">bindingConfiguration</span></span>|<span data-ttu-id="af35f-117">可选的字符串。</span><span class="sxs-lookup"><span data-stu-id="af35f-117">Optional string.</span></span> <span data-ttu-id="af35f-118">指定在配置文件中找到的绑定配置。</span><span class="sxs-lookup"><span data-stu-id="af35f-118">Specifies a binding configuration found in the configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="af35f-119">子元素</span><span class="sxs-lookup"><span data-stu-id="af35f-119">Child Elements</span></span>  
  
|<span data-ttu-id="af35f-120">元素</span><span class="sxs-lookup"><span data-stu-id="af35f-120">Element</span></span>|<span data-ttu-id="af35f-121">说明</span><span class="sxs-lookup"><span data-stu-id="af35f-121">Description</span></span>|  
|-------------|-----------------|  
|[\<identity>](identity.md)|<span data-ttu-id="af35f-122">指定此本地颁发者的标识信息。</span><span class="sxs-lookup"><span data-stu-id="af35f-122">Specifies identity information for the local issuer.</span></span>|  
|[\<headers>](headers-element.md)|<span data-ttu-id="af35f-123">地址头的集合，要正确书写本地颁发者的地址必须使用这些地址头。</span><span class="sxs-lookup"><span data-stu-id="af35f-123">A collection of address headers that are required in order to correctly address the local issuer.</span></span> <span data-ttu-id="af35f-124">可以使用 `add` 关键字向此集合添加标头。</span><span class="sxs-lookup"><span data-stu-id="af35f-124">You can use the `add` keyword to add a header to this collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="af35f-125">父元素</span><span class="sxs-lookup"><span data-stu-id="af35f-125">Parent Elements</span></span>  
  
|<span data-ttu-id="af35f-126">元素</span><span class="sxs-lookup"><span data-stu-id="af35f-126">Element</span></span>|<span data-ttu-id="af35f-127">说明</span><span class="sxs-lookup"><span data-stu-id="af35f-127">Description</span></span>|  
|-------------|-----------------|  
|[\<issuedToken>](issuedtoken.md)|<span data-ttu-id="af35f-128">指定用于向服务验证客户端身份的自定义令牌。</span><span class="sxs-lookup"><span data-stu-id="af35f-128">Specifies a custom token used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="af35f-129">备注</span><span class="sxs-lookup"><span data-stu-id="af35f-129">Remarks</span></span>  

 <span data-ttu-id="af35f-130">从安全令牌服务 (STS) 获取已颁发的令牌时，必须使用地址和绑定配置客户端应用程序，以将其用于与 STS 进行通信。</span><span class="sxs-lookup"><span data-stu-id="af35f-130">When obtaining an issued token from a Security Token Service (STS), the client application must be configured with the address and binding to use to communicate with the STS.</span></span> <span data-ttu-id="af35f-131">如果没有 <xref:System.ServiceModel.WSFederationHttpBinding> 为 security token service 提供 URL，或者联合绑定的颁发者地址为 `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` 或时 `null` ，则客户端的 Windows Communication Foundation (WCF) 通道使用和指定的值 `address` `binding` 来与 STS 通信，以获取已颁发的令牌。</span><span class="sxs-lookup"><span data-stu-id="af35f-131">When the <xref:System.ServiceModel.WSFederationHttpBinding> does not supply a URL for the security token service, or when the issuer address of a federated binding is `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` or `null`, the client's Windows Communication Foundation (WCF) channel uses the values specified by `address` and `binding` to communicate with the STS to obtain the issued token.</span></span> <span data-ttu-id="af35f-132">有关配置本地颁发者的详细信息，请参阅 [如何：配置本地颁发者](../../../wcf/feature-details/how-to-configure-a-local-issuer.md)。</span><span class="sxs-lookup"><span data-stu-id="af35f-132">For more information on configuring a local issuer, see [How to: Configure a Local Issuer](../../../wcf/feature-details/how-to-configure-a-local-issuer.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="af35f-133">示例</span><span class="sxs-lookup"><span data-stu-id="af35f-133">Example</span></span>  

 <span data-ttu-id="af35f-134">下面的示例设置 `address` 元素的 `binding`、`bindingConfiguration` 和 `localIssuer` 属性。</span><span class="sxs-lookup"><span data-stu-id="af35f-134">The following example sets the `address`, `binding`, and `bindingConfiguration` attributes of a `localIssuer` element.</span></span>  
  
```xml  
<system.serviceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior name="MyEndpointBehavior">
        <clientCredentials>
          <issuedToken cacheIssuedTokens="false"
                       defaultKeyEntropyMode="ClientEntropy">
            <localIssuer address="net.tcp://cohowinery/tokens"
                         binding="netTcpBinding"
                         bindingConfiguration="myTcpBindingConfig" />
          </issuedToken>
        </clientCredentials>
      </behavior>
    </endpointBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="af35f-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="af35f-135">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.LocalIssuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential>
- [<span data-ttu-id="af35f-136">安全行为</span><span class="sxs-lookup"><span data-stu-id="af35f-136">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="af35f-137">如何：配置本地颁发者</span><span class="sxs-lookup"><span data-stu-id="af35f-137">How to: Configure a Local Issuer</span></span>](../../../wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="af35f-138">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="af35f-138">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="af35f-139">安全行为</span><span class="sxs-lookup"><span data-stu-id="af35f-139">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="af35f-140">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="af35f-140">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="af35f-141">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="af35f-141">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="af35f-142">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="af35f-142">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="af35f-143">如何：创建联合客户端</span><span class="sxs-lookup"><span data-stu-id="af35f-143">How to: Create a Federated Client</span></span>](../../../wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="af35f-144">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="af35f-144">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)

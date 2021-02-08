---
description: 了解详细信息： <issuerNameRegistry>
title: <issuerNameRegistry>
ms.date: 03/30/2017
ms.assetid: 58b39d12-c953-40c4-88af-d7eb3343ca28
author: BrucePerlerMS
ms.openlocfilehash: 73eb0d9d4d19f8e25f2db501e8cb3858d346ac2c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803849"
---
# \<issuerNameRegistry>

<span data-ttu-id="2f477-102">配置标记处理程序集合中的处理程序使用的颁发者名称注册表。</span><span class="sxs-lookup"><span data-stu-id="2f477-102">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlerConfiguration>**](securitytokenhandlerconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<issuerNameRegistry>**  
  
## <a name="syntax"></a><span data-ttu-id="2f477-103">语法</span><span class="sxs-lookup"><span data-stu-id="2f477-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry type=xs:string>  
          <optionalCustomConfigurationElements />  
        </issuerNameRegistry>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2f477-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2f477-104">Attributes and Elements</span></span>  

 <span data-ttu-id="2f477-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f477-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2f477-106">特性</span><span class="sxs-lookup"><span data-stu-id="2f477-106">Attributes</span></span>  
  
|<span data-ttu-id="2f477-107">属性</span><span class="sxs-lookup"><span data-stu-id="2f477-107">Attribute</span></span>|<span data-ttu-id="2f477-108">说明</span><span class="sxs-lookup"><span data-stu-id="2f477-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2f477-109">type</span><span class="sxs-lookup"><span data-stu-id="2f477-109">type</span></span>|<span data-ttu-id="2f477-110">派生自类的类型 <xref:System.IdentityModel.Tokens.IssuerNameRegistry> 。</span><span class="sxs-lookup"><span data-stu-id="2f477-110">A type that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="2f477-111">有关如何指定自定义的详细信息 `type` ，请参阅 [自定义类型引用]。</span><span class="sxs-lookup"><span data-stu-id="2f477-111">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2f477-112">子元素</span><span class="sxs-lookup"><span data-stu-id="2f477-112">Child Elements</span></span>  
  
|<span data-ttu-id="2f477-113">元素</span><span class="sxs-lookup"><span data-stu-id="2f477-113">Element</span></span>|<span data-ttu-id="2f477-114">说明</span><span class="sxs-lookup"><span data-stu-id="2f477-114">Description</span></span>|  
|-------------|-----------------|  
|[\<trustedIssuers>](trustedissuers.md)|<span data-ttu-id="2f477-115">当 `type` 属性指定基于配置的颁发者名称注册表 (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> 类) 时， [\<trustedIssuers>](trustedissuers.md) 必须指定元素。</span><span class="sxs-lookup"><span data-stu-id="2f477-115">When the `type` attribute specifies the configuration-based issuer name registry (the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class), the [\<trustedIssuers>](trustedissuers.md) element must be specified.</span></span> <span data-ttu-id="2f477-116">[\<trustedIssuers>](trustedissuers.md)元素可以将 `<add>` 、 `<clear>` 或 `<remove>` 元素作为子元素。</span><span class="sxs-lookup"><span data-stu-id="2f477-116">The [\<trustedIssuers>](trustedissuers.md) element can take `<add>`, `<clear>`, or `<remove>` elements as child elements.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2f477-117">父元素</span><span class="sxs-lookup"><span data-stu-id="2f477-117">Parent Elements</span></span>  
  
|<span data-ttu-id="2f477-118">元素</span><span class="sxs-lookup"><span data-stu-id="2f477-118">Element</span></span>|<span data-ttu-id="2f477-119">说明</span><span class="sxs-lookup"><span data-stu-id="2f477-119">Description</span></span>|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="2f477-120">为安全标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="2f477-120">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2f477-121">备注</span><span class="sxs-lookup"><span data-stu-id="2f477-121">Remarks</span></span>  

 <span data-ttu-id="2f477-122">使用颁发者名称注册表验证所有颁发者令牌。</span><span class="sxs-lookup"><span data-stu-id="2f477-122">All issuer tokens are validated using an issuer name registry.</span></span> <span data-ttu-id="2f477-123">这是从类派生的对象 <xref:System.IdentityModel.Tokens.IssuerNameRegistry> 。</span><span class="sxs-lookup"><span data-stu-id="2f477-123">This is an object that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="2f477-124">颁发者名称注册表用于将助记键名称关联到验证相应颁发者生成的令牌签名所需的加密材料。</span><span class="sxs-lookup"><span data-stu-id="2f477-124">The issuer name registry is used to associate a mnemonic name to the cryptographic material that is needed to verify the signatures of tokens produced by the corresponding issuer.</span></span> <span data-ttu-id="2f477-125">颁发者名称注册表维护依赖方 (RP) 应用程序信任的颁发者的列表。</span><span class="sxs-lookup"><span data-stu-id="2f477-125">The issuer name registry maintains a list of issuers that are trusted by the relying party (RP) application.</span></span> <span data-ttu-id="2f477-126">颁发者名称注册表的类型是使用属性指定的 `type` 。</span><span class="sxs-lookup"><span data-stu-id="2f477-126">The type of the issuer name registry is specified using the `type` attribute.</span></span> <span data-ttu-id="2f477-127">`<issuerNameRegistry>`元素可以有一个或多个子元素，这些子元素提供指定类型的配置。</span><span class="sxs-lookup"><span data-stu-id="2f477-127">The `<issuerNameRegistry>` element can have one or more child elements that provide configuration for the specified type.</span></span> <span data-ttu-id="2f477-128">通过重写方法来提供处理这些子元素的逻辑 <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> 。</span><span class="sxs-lookup"><span data-stu-id="2f477-128">You provide the logic that processes these child elements by overriding the <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> method.</span></span>  
  
 <span data-ttu-id="2f477-129">WIF 提供单一颁发者名称注册表类型，即 <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> 类。</span><span class="sxs-lookup"><span data-stu-id="2f477-129">WIF provides a single issuer name registry type out of the box, the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class.</span></span> <span data-ttu-id="2f477-130">此类使用在配置中指定的一组受信任的颁发者证书。</span><span class="sxs-lookup"><span data-stu-id="2f477-130">This class uses a set of trusted issuer certificates that are specified in configuration.</span></span> <span data-ttu-id="2f477-131">它需要一个子配置元素， `<trustedIssuers>` 在该元素下配置受信任的颁发者证书的集合。</span><span class="sxs-lookup"><span data-stu-id="2f477-131">It requires a child configuration element, `<trustedIssuers>`, under which the collection of trusted issuer certificates is configured.</span></span> <span data-ttu-id="2f477-132">受信任的证书是使用 "证书指纹" 的 "ASN" 编码形式指定的，并且通过使用 `<add>` 、或元素在集合中添加或删除 `<clear>` `<remove>` 。</span><span class="sxs-lookup"><span data-stu-id="2f477-132">Trusted certificates are specified using the ASN.1 encoded form of the certificate thumbprint and are added or removed from the collection by using `<add>`, `<clear>`, or `<remove>` elements.</span></span>  
  
 <span data-ttu-id="2f477-133">`<issuerNameRegistry>`元素由 <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="2f477-133">The `<issuerNameRegistry>` element is represented by the <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> class.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2f477-134">将 `<issuerNameRegistry>` 元素指定为元素的子元素 [\<identityConfiguration>](identityconfiguration.md) 已不推荐使用，但仍支持向后兼容。</span><span class="sxs-lookup"><span data-stu-id="2f477-134">Specifying the `<issuerNameRegistry>` element as a child element of the [\<identityConfiguration>](identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="2f477-135">元素上的设置将 `<securityTokenHandlerConfiguration>` 替代元素上的设置 `<identityConfiguration>` 。</span><span class="sxs-lookup"><span data-stu-id="2f477-135">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2f477-136">示例</span><span class="sxs-lookup"><span data-stu-id="2f477-136">Example</span></span>  

 <span data-ttu-id="2f477-137">下面的 XML 演示如何指定基于配置的颁发者名称注册表。</span><span class="sxs-lookup"><span data-stu-id="2f477-137">The following XML shows how to specify the configuration based issuer name registry.</span></span>  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB … 1EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a><span data-ttu-id="2f477-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f477-138">See also</span></span>

- <xref:System.IdentityModel.Tokens.IssuerNameRegistry>
- <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>

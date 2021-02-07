---
description: 了解详细信息： <serviceTokenResolver>
title: <serviceTokenResolver>
ms.date: 03/30/2017
ms.assetid: 6e9001e1-e064-4f47-84b2-46225c177746
author: BrucePerlerMS
ms.openlocfilehash: ab24c92eee43324365adb3bb3a64c8a765017a53
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698292"
---
# \<serviceTokenResolver>

<span data-ttu-id="2a2a1-102">注册令牌处理程序集合中的处理程序使用的服务令牌解析程序。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-102">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="2a2a1-103">服务令牌解析器用于解析传入令牌和消息的加密令牌。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-103">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlerConfiguration>**](securitytokenhandlerconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceTokenResolver>**  
  
## <a name="syntax"></a><span data-ttu-id="2a2a1-104">语法</span><span class="sxs-lookup"><span data-stu-id="2a2a1-104">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <serviceTokenResolver type=xs:string>  
        </serviceTokenResolver>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2a2a1-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2a2a1-105">Attributes and Elements</span></span>  

 <span data-ttu-id="2a2a1-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2a2a1-107">特性</span><span class="sxs-lookup"><span data-stu-id="2a2a1-107">Attributes</span></span>  
  
|<span data-ttu-id="2a2a1-108">属性</span><span class="sxs-lookup"><span data-stu-id="2a2a1-108">Attribute</span></span>|<span data-ttu-id="2a2a1-109">说明</span><span class="sxs-lookup"><span data-stu-id="2a2a1-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2a2a1-110">type</span><span class="sxs-lookup"><span data-stu-id="2a2a1-110">type</span></span>|<span data-ttu-id="2a2a1-111">指定服务令牌解析程序的类型。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-111">Specifies the type of the service token resolver.</span></span> <span data-ttu-id="2a2a1-112"><xref:System.IdentityModel.Selectors.SecurityTokenResolver>类型或派生自类的类型 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-112">Either the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> type or a type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span> <span data-ttu-id="2a2a1-113">有关如何指定属性的详细信息 `type` ，请参阅 [自定义类型引用]。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-113">For more information about how to specify the `type` attribute, see [Custom Type References].</span></span> <span data-ttu-id="2a2a1-114">必需。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-114">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2a2a1-115">子元素</span><span class="sxs-lookup"><span data-stu-id="2a2a1-115">Child Elements</span></span>  

 <span data-ttu-id="2a2a1-116">无</span><span class="sxs-lookup"><span data-stu-id="2a2a1-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2a2a1-117">父元素</span><span class="sxs-lookup"><span data-stu-id="2a2a1-117">Parent Elements</span></span>  
  
|<span data-ttu-id="2a2a1-118">元素</span><span class="sxs-lookup"><span data-stu-id="2a2a1-118">Element</span></span>|<span data-ttu-id="2a2a1-119">说明</span><span class="sxs-lookup"><span data-stu-id="2a2a1-119">Description</span></span>|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="2a2a1-120">为安全标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-120">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2a2a1-121">备注</span><span class="sxs-lookup"><span data-stu-id="2a2a1-121">Remarks</span></span>  

 <span data-ttu-id="2a2a1-122">服务令牌解析程序可用于解析传入令牌和消息的加密令牌。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-122">The service token resolver can be used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="2a2a1-123">它用于检索应该用于解密传入令牌的密钥。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-123">It is used to retrieve the key that should be used to decrypt incoming tokens.</span></span> <span data-ttu-id="2a2a1-124">您必须指定 `type` 属性。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-124">You must specify the `type` attribute.</span></span> <span data-ttu-id="2a2a1-125">指定的类型可以是 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 或从类派生的自定义类型 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-125">The type specified can be either <xref:System.IdentityModel.Selectors.SecurityTokenResolver> or a custom type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span>  
  
 <span data-ttu-id="2a2a1-126">某些标记处理程序允许您在配置中指定服务令牌解析器设置。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-126">Some token handlers allow you to specify service token resolver settings in configuration.</span></span> <span data-ttu-id="2a2a1-127">各个标记处理程序上的设置将替代在安全令牌处理程序集合中指定的设置。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-127">Settings on individual token handlers override those specified on the security token handler collection.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2a2a1-128">将 `<serviceTokenResolver>` 元素指定为元素的子元素 [\<identityConfiguration>](identityconfiguration.md) 已不推荐使用，但仍支持向后兼容。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-128">Specifying the `<serviceTokenResolver>` element as a child element of the [\<identityConfiguration>](identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="2a2a1-129">元素上的设置将 `<securityTokenHandlerConfiguration>` 替代元素上的设置 `<identityConfiguration>` 。</span><span class="sxs-lookup"><span data-stu-id="2a2a1-129">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2a2a1-130">示例</span><span class="sxs-lookup"><span data-stu-id="2a2a1-130">Example</span></span>  
  
```xml  
<serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
```

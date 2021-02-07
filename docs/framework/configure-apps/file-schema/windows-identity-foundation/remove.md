---
description: 了解详细信息： <remove>
title: <remove>
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: 942148f677e10bbab7b86acfba2d0fdfb1b10ca7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664062"
---
# \<remove>

<span data-ttu-id="7a418-102">从标记处理程序集合中删除指定的安全令牌处理程序。</span><span class="sxs-lookup"><span data-stu-id="7a418-102">Removes the specified security token handler from the token handler collection.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**  
  
## <a name="syntax"></a><span data-ttu-id="7a418-103">语法</span><span class="sxs-lookup"><span data-stu-id="7a418-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <remove type=xs:string >  
      </remove>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7a418-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7a418-104">Attributes and Elements</span></span>  

 <span data-ttu-id="7a418-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a418-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7a418-106">特性</span><span class="sxs-lookup"><span data-stu-id="7a418-106">Attributes</span></span>  
  
|<span data-ttu-id="7a418-107">属性</span><span class="sxs-lookup"><span data-stu-id="7a418-107">Attribute</span></span>|<span data-ttu-id="7a418-108">说明</span><span class="sxs-lookup"><span data-stu-id="7a418-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7a418-109">type</span><span class="sxs-lookup"><span data-stu-id="7a418-109">type</span></span>|<span data-ttu-id="7a418-110">要移除的令牌处理程序的 CLR 类型名称。</span><span class="sxs-lookup"><span data-stu-id="7a418-110">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="7a418-111">有关如何指定属性的详细信息 `type` ，请参阅 [自定义类型引用](/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references)。</span><span class="sxs-lookup"><span data-stu-id="7a418-111">For more information about how to specify the `type` attribute, see [Custom Type References](/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references).</span></span> <span data-ttu-id="7a418-112">必需。</span><span class="sxs-lookup"><span data-stu-id="7a418-112">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7a418-113">子元素</span><span class="sxs-lookup"><span data-stu-id="7a418-113">Child Elements</span></span>  

 <span data-ttu-id="7a418-114">无</span><span class="sxs-lookup"><span data-stu-id="7a418-114">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7a418-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7a418-115">Parent Elements</span></span>  
  
|<span data-ttu-id="7a418-116">元素</span><span class="sxs-lookup"><span data-stu-id="7a418-116">Element</span></span>|<span data-ttu-id="7a418-117">说明</span><span class="sxs-lookup"><span data-stu-id="7a418-117">Description</span></span>|  
|-------------|-----------------|  
|[\<securityTokenHandlers>](securitytokenhandlers.md)|<span data-ttu-id="7a418-118">指定注册到终结点的安全令牌处理程序的集合。</span><span class="sxs-lookup"><span data-stu-id="7a418-118">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="7a418-119">示例</span><span class="sxs-lookup"><span data-stu-id="7a418-119">Example</span></span>  

 <span data-ttu-id="7a418-120">下面的 XML 演示 `<add>` 如何使用和元素将 `<remove>` 默认会话标记处理程序替换为自定义会话标记处理程序。</span><span class="sxs-lookup"><span data-stu-id="7a418-120">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="7a418-121">XML 是从示例获取的 `ClaimsAwareWebFarm` 。</span><span class="sxs-lookup"><span data-stu-id="7a418-121">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```

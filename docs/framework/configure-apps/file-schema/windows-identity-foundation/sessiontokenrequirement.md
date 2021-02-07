---
description: 了解详细信息： <sessionTokenRequirement>
title: <sessionTokenRequirement>
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 8f2868df4939dc0dc7c779eb9ca5a35a6b996fc6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698266"
---
# \<sessionTokenRequirement>

<span data-ttu-id="ad63e-102">提供 <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> 类或派生类的配置。</span><span class="sxs-lookup"><span data-stu-id="ad63e-102">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<sessionTokenRequirement>**  
  
## <a name="syntax"></a><span data-ttu-id="ad63e-103">语法</span><span class="sxs-lookup"><span data-stu-id="ad63e-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">  
        <sessionTokenRequirement lifetime=TimeSpan >  
        </sessionTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ad63e-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ad63e-104">Attributes and Elements</span></span>  

 <span data-ttu-id="ad63e-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ad63e-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ad63e-106">特性</span><span class="sxs-lookup"><span data-stu-id="ad63e-106">Attributes</span></span>  
  
|<span data-ttu-id="ad63e-107">属性</span><span class="sxs-lookup"><span data-stu-id="ad63e-107">Attribute</span></span>|<span data-ttu-id="ad63e-108">说明</span><span class="sxs-lookup"><span data-stu-id="ad63e-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ad63e-109">lifetime</span><span class="sxs-lookup"><span data-stu-id="ad63e-109">lifetime</span></span>|<span data-ttu-id="ad63e-110">指定会话令牌的生存期。</span><span class="sxs-lookup"><span data-stu-id="ad63e-110">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ad63e-111">子元素</span><span class="sxs-lookup"><span data-stu-id="ad63e-111">Child Elements</span></span>  

 <span data-ttu-id="ad63e-112">无</span><span class="sxs-lookup"><span data-stu-id="ad63e-112">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ad63e-113">父元素</span><span class="sxs-lookup"><span data-stu-id="ad63e-113">Parent Elements</span></span>  
  
|<span data-ttu-id="ad63e-114">元素</span><span class="sxs-lookup"><span data-stu-id="ad63e-114">Element</span></span>|<span data-ttu-id="ad63e-115">说明</span><span class="sxs-lookup"><span data-stu-id="ad63e-115">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add.md)|<span data-ttu-id="ad63e-116">将指定的安全令牌处理程序添加到令牌处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="ad63e-116">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ad63e-117">示例</span><span class="sxs-lookup"><span data-stu-id="ad63e-117">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```

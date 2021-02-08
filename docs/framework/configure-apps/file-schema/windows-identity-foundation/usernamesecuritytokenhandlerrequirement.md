---
description: 了解详细信息： <userNameSecurityTokenHandlerRequirement>
title: <userNameSecurityTokenHandlerRequirement>
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: c2bca086d06738699517fe140173f321a3233a4a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786494"
---
# \<userNameSecurityTokenHandlerRequirement>

<span data-ttu-id="9d8d7-102">提供 <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> 类或派生类的配置。</span><span class="sxs-lookup"><span data-stu-id="9d8d7-102">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<userNameSecurityTokenHandlerRequirement>**  
  
## <a name="syntax"></a><span data-ttu-id="9d8d7-103">语法</span><span class="sxs-lookup"><span data-stu-id="9d8d7-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
        <userNameSecurityTokenHandlerRequirement membershipProviderName=xs:string >  
        </userNameSecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9d8d7-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9d8d7-104">Attributes and Elements</span></span>  

 <span data-ttu-id="9d8d7-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9d8d7-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9d8d7-106">特性</span><span class="sxs-lookup"><span data-stu-id="9d8d7-106">Attributes</span></span>  
  
|<span data-ttu-id="9d8d7-107">属性</span><span class="sxs-lookup"><span data-stu-id="9d8d7-107">Attribute</span></span>|<span data-ttu-id="9d8d7-108">说明</span><span class="sxs-lookup"><span data-stu-id="9d8d7-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9d8d7-109">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="9d8d7-109">membershipProviderName</span></span>|<span data-ttu-id="9d8d7-110">指定 <xref:System.Web.Security.MembershipProvider> 应该由安全令牌处理程序使用的。</span><span class="sxs-lookup"><span data-stu-id="9d8d7-110">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9d8d7-111">子元素</span><span class="sxs-lookup"><span data-stu-id="9d8d7-111">Child Elements</span></span>  

 <span data-ttu-id="9d8d7-112">无</span><span class="sxs-lookup"><span data-stu-id="9d8d7-112">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9d8d7-113">父元素</span><span class="sxs-lookup"><span data-stu-id="9d8d7-113">Parent Elements</span></span>  
  
|<span data-ttu-id="9d8d7-114">元素</span><span class="sxs-lookup"><span data-stu-id="9d8d7-114">Element</span></span>|<span data-ttu-id="9d8d7-115">说明</span><span class="sxs-lookup"><span data-stu-id="9d8d7-115">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add.md)|<span data-ttu-id="9d8d7-116">将指定的安全令牌处理程序添加到令牌处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="9d8d7-116">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9d8d7-117">备注</span><span class="sxs-lookup"><span data-stu-id="9d8d7-117">Remarks</span></span>  

 <span data-ttu-id="9d8d7-118">`<userNameSecurityTokenHandlerRequirement>` <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> 从配置中初始化对象时，元素设置属性。</span><span class="sxs-lookup"><span data-stu-id="9d8d7-118">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9d8d7-119">示例</span><span class="sxs-lookup"><span data-stu-id="9d8d7-119">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```

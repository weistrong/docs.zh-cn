---
description: 了解详细信息： <caches>
title: <caches>
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: ebc2fa66ab8b657f7cc3741668c9f27fc60510b4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681833"
---
# \<caches>

<span data-ttu-id="552e2-102">注册用于会话令牌和令牌重播检测的缓存。</span><span class="sxs-lookup"><span data-stu-id="552e2-102">Registers the caches used for session tokens and token replay detection.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<caches>**  
  
## <a name="syntax"></a><span data-ttu-id="552e2-103">语法</span><span class="sxs-lookup"><span data-stu-id="552e2-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="552e2-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="552e2-104">Attributes and Elements</span></span>  

 <span data-ttu-id="552e2-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="552e2-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="552e2-106">特性</span><span class="sxs-lookup"><span data-stu-id="552e2-106">Attributes</span></span>  

 <span data-ttu-id="552e2-107">无</span><span class="sxs-lookup"><span data-stu-id="552e2-107">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="552e2-108">子元素</span><span class="sxs-lookup"><span data-stu-id="552e2-108">Child Elements</span></span>  
  
|<span data-ttu-id="552e2-109">元素</span><span class="sxs-lookup"><span data-stu-id="552e2-109">Element</span></span>|<span data-ttu-id="552e2-110">说明</span><span class="sxs-lookup"><span data-stu-id="552e2-110">Description</span></span>|  
|-------------|-----------------|  
|[\<sessionSecurityTokenCache>](sessionsecuritytokencache.md)|<span data-ttu-id="552e2-111">使用服务或安全标记处理程序集合为会话令牌注册缓存。</span><span class="sxs-lookup"><span data-stu-id="552e2-111">Registers a cache for session tokens with a service or a security token handler collection.</span></span>|  
|[\<tokenReplayCache>](tokenreplaycache.md)|<span data-ttu-id="552e2-112">向服务或安全标记处理程序集合注册令牌重播缓存。</span><span class="sxs-lookup"><span data-stu-id="552e2-112">Registers a token replay cache with a service or a security token handler collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="552e2-113">父元素</span><span class="sxs-lookup"><span data-stu-id="552e2-113">Parent Elements</span></span>  
  
|<span data-ttu-id="552e2-114">元素</span><span class="sxs-lookup"><span data-stu-id="552e2-114">Element</span></span>|<span data-ttu-id="552e2-115">说明</span><span class="sxs-lookup"><span data-stu-id="552e2-115">Description</span></span>|  
|-------------|-----------------|  
|[\<identityConfiguration>](identityconfiguration.md)|<span data-ttu-id="552e2-116">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="552e2-116">Specifies service-level identity settings.</span></span>|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="552e2-117">为安全标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="552e2-117">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="552e2-118">备注</span><span class="sxs-lookup"><span data-stu-id="552e2-118">Remarks</span></span>  

 <span data-ttu-id="552e2-119">可以在元素 `<caches>` 下的服务级别指定元素， `<identityConfiguration>` 或在元素下的安全令牌处理程序集合级别指定元素 `<securityTokenHandlerConfiguration>` 。</span><span class="sxs-lookup"><span data-stu-id="552e2-119">A `<caches>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="552e2-120">标记处理程序集合上的设置将重写服务上指定的设置。</span><span class="sxs-lookup"><span data-stu-id="552e2-120">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="552e2-121">`<caches>`元素由 <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="552e2-121">The `<caches>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> class.</span></span> <span data-ttu-id="552e2-122">配置的缓存由 <xref:System.IdentityModel.Configuration.IdentityModelCaches> 类表示。</span><span class="sxs-lookup"><span data-stu-id="552e2-122">The configured caches are represented by the <xref:System.IdentityModel.Configuration.IdentityModelCaches> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="552e2-123">示例</span><span class="sxs-lookup"><span data-stu-id="552e2-123">Example</span></span>  

 <span data-ttu-id="552e2-124">下面的 XML 演示了如何配置自定义缓存，用于保存)  (的会话安全令牌 <xref:System.IdentityModel.Tokens.SessionSecurityToken> 。</span><span class="sxs-lookup"><span data-stu-id="552e2-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="552e2-125">此配置取自 `ClaimsAwareWebFarm` 示例。</span><span class="sxs-lookup"><span data-stu-id="552e2-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```

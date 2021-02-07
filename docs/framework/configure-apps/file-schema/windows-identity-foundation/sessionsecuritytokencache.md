---
description: 了解详细信息： <sessionSecurityTokenCache>
title: <sessionSecurityTokenCache>
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: 6fc0bb518f546ffd80c68df95a9c0fab145423b8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698279"
---
# \<sessionSecurityTokenCache>

<span data-ttu-id="0c5ec-102">使用服务或安全标记处理程序集合为会话令牌注册缓存。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-102">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<caches>**](caches.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<sessionSecurityTokenCache>**  
  
## <a name="syntax"></a><span data-ttu-id="0c5ec-103">语法</span><span class="sxs-lookup"><span data-stu-id="0c5ec-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <sessionSecurityTokenCache type=xs:string>  
      </sessionSecurityTokenCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c5ec-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0c5ec-104">Attributes and Elements</span></span>  

 <span data-ttu-id="0c5ec-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0c5ec-106">特性</span><span class="sxs-lookup"><span data-stu-id="0c5ec-106">Attributes</span></span>  
  
|<span data-ttu-id="0c5ec-107">属性</span><span class="sxs-lookup"><span data-stu-id="0c5ec-107">Attribute</span></span>|<span data-ttu-id="0c5ec-108">说明</span><span class="sxs-lookup"><span data-stu-id="0c5ec-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0c5ec-109">type</span><span class="sxs-lookup"><span data-stu-id="0c5ec-109">type</span></span>|<span data-ttu-id="0c5ec-110">派生自类的类型 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> 。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-110">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0c5ec-111">子元素</span><span class="sxs-lookup"><span data-stu-id="0c5ec-111">Child Elements</span></span>  

 <span data-ttu-id="0c5ec-112">无</span><span class="sxs-lookup"><span data-stu-id="0c5ec-112">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0c5ec-113">父元素</span><span class="sxs-lookup"><span data-stu-id="0c5ec-113">Parent Elements</span></span>  
  
|<span data-ttu-id="0c5ec-114">元素</span><span class="sxs-lookup"><span data-stu-id="0c5ec-114">Element</span></span>|<span data-ttu-id="0c5ec-115">说明</span><span class="sxs-lookup"><span data-stu-id="0c5ec-115">Description</span></span>|  
|-------------|-----------------|  
|[\<caches>](caches.md)|<span data-ttu-id="0c5ec-116">注册服务使用的缓存或安全标记处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-116">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0c5ec-117">示例</span><span class="sxs-lookup"><span data-stu-id="0c5ec-117">Example</span></span>  

 <span data-ttu-id="0c5ec-118">下面的 XML 演示了如何配置自定义缓存，用于保存)  (的会话安全令牌 <xref:System.IdentityModel.Tokens.SessionSecurityToken> 。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-118">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="0c5ec-119">此配置取自 `ClaimsAwareWebFarm` 示例。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-119">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="0c5ec-120">有关此示例的详细信息，请参阅 [WIF 代码示例索引](/previous-versions/dotnet/framework/security/wif-code-sample-index)。</span><span class="sxs-lookup"><span data-stu-id="0c5ec-120">For more information about this sample, see [WIF Code Sample Index](/previous-versions/dotnet/framework/security/wif-code-sample-index).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0c5ec-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c5ec-121">See also</span></span>

- <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>

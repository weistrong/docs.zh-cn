---
description: 了解详细信息： <tokenReplayCache>
title: <tokenReplayCache>
ms.date: 03/30/2017
ms.assetid: 1572ab23-6933-41b5-bfb4-0c4548145500
author: BrucePerlerMS
ms.openlocfilehash: 793b1f88a9eeb0ebce4cd440e248e81377f17e9b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748994"
---
# \<tokenReplayCache>

<span data-ttu-id="f8254-102">向服务或安全标记处理程序集合注册令牌重播缓存。</span><span class="sxs-lookup"><span data-stu-id="f8254-102">Registers a token replay cache with a service or a security token handler collection.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<caches>**](caches.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<tokenReplayCache>**  
  
## <a name="syntax"></a><span data-ttu-id="f8254-103">语法</span><span class="sxs-lookup"><span data-stu-id="f8254-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <tokenReplayCache type=xs:string>  
      </tokenReplayCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f8254-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f8254-104">Attributes and Elements</span></span>  

 <span data-ttu-id="f8254-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f8254-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f8254-106">特性</span><span class="sxs-lookup"><span data-stu-id="f8254-106">Attributes</span></span>  
  
|<span data-ttu-id="f8254-107">属性</span><span class="sxs-lookup"><span data-stu-id="f8254-107">Attribute</span></span>|<span data-ttu-id="f8254-108">说明</span><span class="sxs-lookup"><span data-stu-id="f8254-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f8254-109">type</span><span class="sxs-lookup"><span data-stu-id="f8254-109">type</span></span>|<span data-ttu-id="f8254-110">派生自类的类型 <xref:System.IdentityModel.Tokens.TokenReplayCache> 。</span><span class="sxs-lookup"><span data-stu-id="f8254-110">A type that derives from the <xref:System.IdentityModel.Tokens.TokenReplayCache> class.</span></span> <span data-ttu-id="f8254-111">有关如何指定自定义的详细信息 `type` ，请参阅 [自定义类型引用]。</span><span class="sxs-lookup"><span data-stu-id="f8254-111">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8254-112">子元素</span><span class="sxs-lookup"><span data-stu-id="f8254-112">Child Elements</span></span>  

 <span data-ttu-id="f8254-113">无</span><span class="sxs-lookup"><span data-stu-id="f8254-113">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f8254-114">父元素</span><span class="sxs-lookup"><span data-stu-id="f8254-114">Parent Elements</span></span>  
  
|<span data-ttu-id="f8254-115">元素</span><span class="sxs-lookup"><span data-stu-id="f8254-115">Element</span></span>|<span data-ttu-id="f8254-116">说明</span><span class="sxs-lookup"><span data-stu-id="f8254-116">Description</span></span>|  
|-------------|-----------------|  
|[\<caches>](caches.md)|<span data-ttu-id="f8254-117">注册服务使用的缓存或安全标记处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="f8254-117">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f8254-118">备注</span><span class="sxs-lookup"><span data-stu-id="f8254-118">Remarks</span></span>  

 <span data-ttu-id="f8254-119">令牌重播缓存用于检测重播的标记。</span><span class="sxs-lookup"><span data-stu-id="f8254-119">The token replay cache is used to detect replayed tokens.</span></span> <span data-ttu-id="f8254-120">令牌重播检测由 [\<tokenReplayDetection>](tokenreplaydetection.md) 元素启用，该元素还指定了令牌的最长到期时间。</span><span class="sxs-lookup"><span data-stu-id="f8254-120">Token replay detection is enabled by the [\<tokenReplayDetection>](tokenreplaydetection.md) element, which also specifies the maximum expiration time for tokens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f8254-121">示例</span><span class="sxs-lookup"><span data-stu-id="f8254-121">Example</span></span>  

 <span data-ttu-id="f8254-122">下面的 XML 演示了用于检测重播令牌的自定义缓存配置。</span><span class="sxs-lookup"><span data-stu-id="f8254-122">The following XML shows the configuration of a custom cache for detecting replayed tokens.</span></span>  
  
```xml  
<caches>  
  <tokenReplayCache type="MyCacheLibrary.MyTokenReplayCache, MyCacheLibrary">  
  </tokenReplayCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f8254-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8254-123">See also</span></span>

- <xref:System.IdentityModel.Tokens.TokenReplayCache>
- [\<tokenReplayDetection>](tokenreplaydetection.md)

---
description: 了解详细信息： <tokenReplayDetection>
title: <tokenReplayDetection>
ms.date: 03/30/2017
ms.assetid: ac3f588e-5f75-4275-b969-2d492ecc3b47
author: BrucePerlerMS
ms.openlocfilehash: a8a6b754a3282afe4f2932296b06b84c09fb6f1a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786533"
---
# \<tokenReplayDetection>

<span data-ttu-id="73905-102">启用令牌重播检测并指定令牌的过期时间。</span><span class="sxs-lookup"><span data-stu-id="73905-102">Enables token replay detection and specifies the expiration time for tokens.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<tokenReplayDetection>**  
  
## <a name="syntax"></a><span data-ttu-id="73905-103">语法</span><span class="sxs-lookup"><span data-stu-id="73905-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <tokenReplayDetection enabled=xs:boolean expirationPeriod=TimeSpan>  
    </tokenReplayDetection>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="type"></a><span data-ttu-id="73905-104">类型</span><span class="sxs-lookup"><span data-stu-id="73905-104">Type</span></span>  

 <xref:System.IdentityModel.Configuration.TokenReplayDetectionElement>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="73905-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="73905-105">Attributes and Elements</span></span>  

 <span data-ttu-id="73905-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="73905-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="73905-107">特性</span><span class="sxs-lookup"><span data-stu-id="73905-107">Attributes</span></span>  
  
|<span data-ttu-id="73905-108">属性</span><span class="sxs-lookup"><span data-stu-id="73905-108">Attribute</span></span>|<span data-ttu-id="73905-109">说明</span><span class="sxs-lookup"><span data-stu-id="73905-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="73905-110">enabled</span><span class="sxs-lookup"><span data-stu-id="73905-110">enabled</span></span>|<span data-ttu-id="73905-111">一个值，该值指定是否启用令牌重放检测;"true" 表示启用令牌重播检测。</span><span class="sxs-lookup"><span data-stu-id="73905-111">A value that specifies whether token replay detection is enabled; "true" to enable token replay detection.</span></span>|  
|<span data-ttu-id="73905-112">expirationPeriod</span><span class="sxs-lookup"><span data-stu-id="73905-112">expirationPeriod</span></span>|<span data-ttu-id="73905-113">一个 <xref:System.TimeSpan> ，指定项目被视为过期并从缓存中删除之前的最大时间量。</span><span class="sxs-lookup"><span data-stu-id="73905-113">A <xref:System.TimeSpan> that specifies the maximum amount of time before an item is considered expired and removed from the cache.</span></span>  <span data-ttu-id="73905-114">有关如何指定值的详细信息 <xref:System.TimeSpan> ，请参阅 [Timespan 值](../windows-workflow-foundation/index.md)。</span><span class="sxs-lookup"><span data-stu-id="73905-114">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="73905-115">子元素</span><span class="sxs-lookup"><span data-stu-id="73905-115">Child Elements</span></span>  

 <span data-ttu-id="73905-116">无</span><span class="sxs-lookup"><span data-stu-id="73905-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="73905-117">父元素</span><span class="sxs-lookup"><span data-stu-id="73905-117">Parent Elements</span></span>  
  
|<span data-ttu-id="73905-118">元素</span><span class="sxs-lookup"><span data-stu-id="73905-118">Element</span></span>|<span data-ttu-id="73905-119">说明</span><span class="sxs-lookup"><span data-stu-id="73905-119">Description</span></span>|  
|-------------|-----------------|  
|[\<identityConfiguration>](identityconfiguration.md)|<span data-ttu-id="73905-120">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="73905-120">Specifies service-level identity settings.</span></span>|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="73905-121">为安全标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="73905-121">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="73905-122">备注</span><span class="sxs-lookup"><span data-stu-id="73905-122">Remarks</span></span>  

 <span data-ttu-id="73905-123">可以在元素 `<tokenReplayDetection>` 下的服务级别指定元素， `<identityConfiguration>` 或在元素下的安全令牌处理程序集合级别指定元素 `<securityTokenHandlerConfiguration>` 。</span><span class="sxs-lookup"><span data-stu-id="73905-123">A `<tokenReplayDetection>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="73905-124">标记处理程序集合上的设置将重写服务上指定的设置。</span><span class="sxs-lookup"><span data-stu-id="73905-124">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="73905-125">令牌重播缓存的类型由 [\<tokenReplayCache>](tokenreplaycache.md) 元素指定。</span><span class="sxs-lookup"><span data-stu-id="73905-125">The type of the token replay cache is specified by the [\<tokenReplayCache>](tokenreplaycache.md) element.</span></span>

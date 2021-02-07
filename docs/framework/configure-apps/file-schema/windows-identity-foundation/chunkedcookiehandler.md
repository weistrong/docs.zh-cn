---
description: 了解详细信息： <chunkedCookieHandler>
title: <chunkedCookieHandler>
ms.date: 03/30/2017
ms.assetid: 7220de45-1d14-4aec-a29e-4a2ea8ac861f
author: BrucePerlerMS
ms.openlocfilehash: b0090706d3d7a9f62e17ae63ec16e4b3a869a812
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664283"
---
# \<chunkedCookieHandler>

<span data-ttu-id="0dbbf-102">配置 <xref:System.IdentityModel.Services.ChunkedCookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-102">Configures the <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span></span> <span data-ttu-id="0dbbf-103">仅当 `mode` 元素的属性 `<cookieHandler>` 为 "默认值" 或 "分块" 时，此元素才能存在。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-103">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Default" or "Chunked".</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel.services>**](system-identitymodel-services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<federationConfiguration>**](federationconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<cookieHandler>**](cookiehandler.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<chunkedCookieHandler>**  
  
## <a name="syntax"></a><span data-ttu-id="0dbbf-104">语法</span><span class="sxs-lookup"><span data-stu-id="0dbbf-104">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Chunked||Default" >  
      <chunkedCookieHandler size=xs:int >  
      </chunkedCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0dbbf-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0dbbf-105">Attributes and Elements</span></span>  

 <span data-ttu-id="0dbbf-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0dbbf-107">特性</span><span class="sxs-lookup"><span data-stu-id="0dbbf-107">Attributes</span></span>  
  
|<span data-ttu-id="0dbbf-108">属性</span><span class="sxs-lookup"><span data-stu-id="0dbbf-108">Attribute</span></span>|<span data-ttu-id="0dbbf-109">说明</span><span class="sxs-lookup"><span data-stu-id="0dbbf-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0dbbf-110">chunkSize</span><span class="sxs-lookup"><span data-stu-id="0dbbf-110">chunkSize</span></span>|<span data-ttu-id="0dbbf-111">任何一个 HTTP cookie 的 HTTP cookie 数据的最大大小（字符数）。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-111">The maximum size, in characters, of the HTTP cookie data for any one HTTP cookie.</span></span> <span data-ttu-id="0dbbf-112">调整块区大小时必须小心谨慎。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-112">You must be careful when adjusting the chunk size.</span></span> <span data-ttu-id="0dbbf-113">Web 浏览器对 cookie 和每个域允许的数量有不同的限制。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-113">Web browsers have different limits on the size of cookies and number allowed per domain.</span></span> <span data-ttu-id="0dbbf-114">例如，原始 Netscape 规范规定这些限制： 300 cookie 总数、每个 cookie 标头4096个字节 (包括元数据，而不仅仅是 cookie 值) 和每个域20个 cookie。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-114">For example, the original Netscape specification stipulated these limits: 300 cookies total, 4096 bytes per cookie header (including metadata, not just the cookie value), and 20 cookies per domain.</span></span> <span data-ttu-id="0dbbf-115">默认为 2000。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-115">The default is 2000.</span></span> <span data-ttu-id="0dbbf-116">必需。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-116">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0dbbf-117">子元素</span><span class="sxs-lookup"><span data-stu-id="0dbbf-117">Child Elements</span></span>  

 <span data-ttu-id="0dbbf-118">无</span><span class="sxs-lookup"><span data-stu-id="0dbbf-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0dbbf-119">父元素</span><span class="sxs-lookup"><span data-stu-id="0dbbf-119">Parent Elements</span></span>  
  
|<span data-ttu-id="0dbbf-120">元素</span><span class="sxs-lookup"><span data-stu-id="0dbbf-120">Element</span></span>|<span data-ttu-id="0dbbf-121">说明</span><span class="sxs-lookup"><span data-stu-id="0dbbf-121">Description</span></span>|  
|-------------|-----------------|  
|[\<cookieHandler>](cookiehandler.md)|<span data-ttu-id="0dbbf-122">配置 <xref:System.IdentityModel.Services.CookieHandler> <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) 用于读取和写入 cookie 的。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-122">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0dbbf-123">备注</span><span class="sxs-lookup"><span data-stu-id="0dbbf-123">Remarks</span></span>  

 <span data-ttu-id="0dbbf-124"><xref:System.IdentityModel.Services.ChunkedCookieHandler>通过将 `mode` 元素的属性设置 `<cookieHandler>` 为 "默认值" 或 "分块" 指定时，可以指定 cookie 处理程序用来读取和写入 cookie 的块区大小，方法是包含一个 `<chunkedCookieHandler>` 子元素并设置其 `chunkSize` 属性。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-124">When you specify a <xref:System.IdentityModel.Services.ChunkedCookieHandler> by setting the `mode` attribute of the `<cookieHandler>` element to "Default" or "Chunked", you can specify the chunk size that the cookie handler uses to read and write cookies by including a `<chunkedCookieHandler>` child element and setting its `chunkSize` attribute.</span></span> <span data-ttu-id="0dbbf-125">如果该 `<chunkedCookieHandler>` 元素不存在，则使用默认的块区大小（2000字节）。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-125">If the `<chunkedCookieHandler>` element is not present, the default chunk size of 2000 bytes is used.</span></span> <span data-ttu-id="0dbbf-126">当 `mode` 特性设置为 "Custom" 时，不能指定此元素。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-126">This element cannot be specified when the `mode` attribute is set to "Custom".</span></span>  
  
 <span data-ttu-id="0dbbf-127">`<chunkedCookieHandler>`元素由 <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-127">The `<chunkedCookieHandler>` element is represented by the <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0dbbf-128">示例</span><span class="sxs-lookup"><span data-stu-id="0dbbf-128">Example</span></span>  

 <span data-ttu-id="0dbbf-129">下面的示例配置一个分块 cookie 处理程序，该处理程序以3000字节的块写入 cookie。</span><span class="sxs-lookup"><span data-stu-id="0dbbf-129">The following example configures a chunked cookie handler that writes cookies in chunks of 3000 bytes.</span></span>  
  
```xml  
<cookieHandler mode="Chunked">  
    <chunkedCookieHandler chunkSize=3000/>  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0dbbf-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="0dbbf-130">See also</span></span>

- <xref:System.IdentityModel.Services.ChunkedCookieHandler>

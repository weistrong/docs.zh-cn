---
description: 了解详细信息： <cookieHandler>
title: <cookieHandler>
ms.date: 03/30/2017
ms.assetid: bfdc127f-8d94-4566-8bef-f583c6ae7398
author: BrucePerlerMS
ms.openlocfilehash: 036646ca5c8aaedebba9466ecb8c9232e87a773d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786572"
---
# \<cookieHandler>

<span data-ttu-id="52a72-102">配置 <xref:System.IdentityModel.Services.CookieHandler> <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) 用于读取和写入 cookie 的。</span><span class="sxs-lookup"><span data-stu-id="52a72-102">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) uses to read and write cookies.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel.services>**](system-identitymodel-services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<federationConfiguration>**](federationconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<cookieHandler>**  
  
## <a name="syntax"></a><span data-ttu-id="52a72-103">语法</span><span class="sxs-lookup"><span data-stu-id="52a72-103">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler name=xs:string  
        path=Path  
        mode="Chunked||Custom||Default"  
        persistentSessionLifetime=xs:string  
        hideFromScript=xs:boolean  
        requireSSL=xs:boolean  
        domain=xs:string  
      <chunkedCookieHandler size=xs:int />  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="52a72-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="52a72-104">Attributes and Elements</span></span>  

 <span data-ttu-id="52a72-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52a72-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="52a72-106">特性</span><span class="sxs-lookup"><span data-stu-id="52a72-106">Attributes</span></span>  
  
|<span data-ttu-id="52a72-107">属性</span><span class="sxs-lookup"><span data-stu-id="52a72-107">Attribute</span></span>|<span data-ttu-id="52a72-108">说明</span><span class="sxs-lookup"><span data-stu-id="52a72-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="52a72-109">name</span><span class="sxs-lookup"><span data-stu-id="52a72-109">name</span></span>|<span data-ttu-id="52a72-110">指定写入的任何 cookie 的基名称。</span><span class="sxs-lookup"><span data-stu-id="52a72-110">Specifies the base name for any cookies written.</span></span> <span data-ttu-id="52a72-111">默认值为 "FedAuth"。</span><span class="sxs-lookup"><span data-stu-id="52a72-111">The default is "FedAuth".</span></span>|  
|<span data-ttu-id="52a72-112">path</span><span class="sxs-lookup"><span data-stu-id="52a72-112">path</span></span>|<span data-ttu-id="52a72-113">指定写入的任何 cookie 的路径值。</span><span class="sxs-lookup"><span data-stu-id="52a72-113">Specifies the path value for any cookies written.</span></span> <span data-ttu-id="52a72-114">默认值为 "HttpRuntime. AppDomainAppVirtualPath"。</span><span class="sxs-lookup"><span data-stu-id="52a72-114">The default is "HttpRuntime.AppDomainAppVirtualPath".</span></span>|  
|<span data-ttu-id="52a72-115">mode</span><span class="sxs-lookup"><span data-stu-id="52a72-115">mode</span></span>|<span data-ttu-id="52a72-116"><xref:System.IdentityModel.Services.CookieHandlerMode>值之一，它指定 SAM 使用的 cookie 处理程序的类型。</span><span class="sxs-lookup"><span data-stu-id="52a72-116">One of the <xref:System.IdentityModel.Services.CookieHandlerMode> values that specifies the kind of cookie handler used by the SAM.</span></span> <span data-ttu-id="52a72-117">可以使用以下值：</span><span class="sxs-lookup"><span data-stu-id="52a72-117">The following values may be used:</span></span><br /><br /> <span data-ttu-id="52a72-118">-"Default"-与 "分块" 相同。</span><span class="sxs-lookup"><span data-stu-id="52a72-118">-   "Default" — The same as "Chunked".</span></span><br /><span data-ttu-id="52a72-119">-"分块"-使用类的实例 <xref:System.IdentityModel.Services.ChunkedCookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="52a72-119">-   "Chunked" — Uses an instance of the <xref:System.IdentityModel.Services.ChunkedCookieHandler> class.</span></span> <span data-ttu-id="52a72-120">此 cookie 处理程序可确保各个 cookie 不会超过设置的最大大小。</span><span class="sxs-lookup"><span data-stu-id="52a72-120">This cookie handler ensures that individual cookies do not exceed a set maximum size.</span></span> <span data-ttu-id="52a72-121">它通过将一个逻辑 cookie "分块" 为多个网络中的多个 cookie 来实现这一点。</span><span class="sxs-lookup"><span data-stu-id="52a72-121">It accomplishes this by potentially "chunking" one logical cookie into a number of cookies on-the-wire.</span></span><br /><span data-ttu-id="52a72-122">-"Custom"-使用派生自的自定义类的实例 <xref:System.IdentityModel.Services.CookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="52a72-122">-   "Custom" — Uses an instance of a custom class derived from <xref:System.IdentityModel.Services.CookieHandler>.</span></span> <span data-ttu-id="52a72-123">派生类由 `<customCookieHandler>` 子元素引用。</span><span class="sxs-lookup"><span data-stu-id="52a72-123">The derived class is referenced by the `<customCookieHandler>` child element.</span></span><br /><br /> <span data-ttu-id="52a72-124">默认值为 "Default"。</span><span class="sxs-lookup"><span data-stu-id="52a72-124">The default is "Default".</span></span>|  
|<span data-ttu-id="52a72-125">persistentSessionLifetime</span><span class="sxs-lookup"><span data-stu-id="52a72-125">persistentSessionLifetime</span></span>|<span data-ttu-id="52a72-126">指定持久会话的生存期。</span><span class="sxs-lookup"><span data-stu-id="52a72-126">Specifies the lifetime of persistent sessions.</span></span> <span data-ttu-id="52a72-127">如果为零，将始终使用瞬变会话。</span><span class="sxs-lookup"><span data-stu-id="52a72-127">If zero, transient sessions are always used.</span></span> <span data-ttu-id="52a72-128">默认值为 "0:0:0"，该值指定暂时性会话。</span><span class="sxs-lookup"><span data-stu-id="52a72-128">The default value is "0:0:0", which specifies a transient session.</span></span> <span data-ttu-id="52a72-129">最大值为 "365:0:0"，该值指定的会话为365天。</span><span class="sxs-lookup"><span data-stu-id="52a72-129">The maximum value is "365:0:0", which specifies a session of 365 days.</span></span> <span data-ttu-id="52a72-130">应根据以下限制指定值： `<xs:pattern value="([0-9.]+:){0,1}([0-9]+:){0,1}[0-9.]+" />` ，其中最左端的值指定天，中间值 (如果存在) 指定小时数，最右侧的值 (如果存在) 指定分钟。</span><span class="sxs-lookup"><span data-stu-id="52a72-130">The value should be specified according to the following restriction: `<xs:pattern value="([0-9.]+:){0,1}([0-9]+:){0,1}[0-9.]+" />`, where the leftmost value specifies days, the middle value (if present) specifies hours, and the rightmost value (if present) specifies minutes.</span></span>|  
|<span data-ttu-id="52a72-131">requireSsl</span><span class="sxs-lookup"><span data-stu-id="52a72-131">requireSsl</span></span>|<span data-ttu-id="52a72-132">指定是否为写入的任何 cookie 发出 "Secure" 标志。</span><span class="sxs-lookup"><span data-stu-id="52a72-132">Specifies whether the "Secure" flag is emitted for any cookies written.</span></span> <span data-ttu-id="52a72-133">如果设置了此值，则只能通过 HTTPS 使用登录会话 cookie。</span><span class="sxs-lookup"><span data-stu-id="52a72-133">If this value is set, the sign-in session cookies will only be available over HTTPS.</span></span> <span data-ttu-id="52a72-134">默认值为“true”。</span><span class="sxs-lookup"><span data-stu-id="52a72-134">The default is "true".</span></span>|  
|<span data-ttu-id="52a72-135">hideFromScript</span><span class="sxs-lookup"><span data-stu-id="52a72-135">hideFromScript</span></span>|<span data-ttu-id="52a72-136">控制是否为写入的任何 cookie 发出 "HttpOnly" 标志。</span><span class="sxs-lookup"><span data-stu-id="52a72-136">Controls whether the "HttpOnly" flag is emitted for any cookies written.</span></span> <span data-ttu-id="52a72-137">某些 web 浏览器通过保持客户端脚本访问 cookie 值来服从此标志。</span><span class="sxs-lookup"><span data-stu-id="52a72-137">Certain web browsers honor this flag by keeping client-side script from accessing the cookie value.</span></span> <span data-ttu-id="52a72-138">默认值为“true”。</span><span class="sxs-lookup"><span data-stu-id="52a72-138">The default is "true".</span></span>|  
|<span data-ttu-id="52a72-139">域</span><span class="sxs-lookup"><span data-stu-id="52a72-139">domain</span></span>|<span data-ttu-id="52a72-140">写入的任何 cookie 的域值。</span><span class="sxs-lookup"><span data-stu-id="52a72-140">The domain value for any cookies written.</span></span> <span data-ttu-id="52a72-141">默认值为 ""。</span><span class="sxs-lookup"><span data-stu-id="52a72-141">The default is "".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="52a72-142">子元素</span><span class="sxs-lookup"><span data-stu-id="52a72-142">Child Elements</span></span>  
  
|<span data-ttu-id="52a72-143">元素</span><span class="sxs-lookup"><span data-stu-id="52a72-143">Element</span></span>|<span data-ttu-id="52a72-144">说明</span><span class="sxs-lookup"><span data-stu-id="52a72-144">Description</span></span>|  
|-------------|-----------------|  
|[\<chunkedCookieHandler>](chunkedcookiehandler.md)|<span data-ttu-id="52a72-145">配置 <xref:System.IdentityModel.Services.ChunkedCookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="52a72-145">Configures the <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span></span> <span data-ttu-id="52a72-146">仅当 `mode` 元素的属性 `<cookieHandler>` 为 "默认值" 或 "分块" 时，此元素才能存在。</span><span class="sxs-lookup"><span data-stu-id="52a72-146">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Default" or "Chunked".</span></span>|  
|[\<customCookieHandler>](customcookiehandler.md)|<span data-ttu-id="52a72-147">设置自定义 cookie 处理程序类型。</span><span class="sxs-lookup"><span data-stu-id="52a72-147">Sets the custom cookie handler type.</span></span> <span data-ttu-id="52a72-148">如果 `mode` 元素的属性 `<cookieHandler>` 为 "Custom"，则此元素必须存在。</span><span class="sxs-lookup"><span data-stu-id="52a72-148">This element must be present if the `mode` attribute of the `<cookieHandler>` element is "Custom".</span></span> <span data-ttu-id="52a72-149">此属性的任何其他值不能出现此情况 `mode` 。</span><span class="sxs-lookup"><span data-stu-id="52a72-149">It cannot be present for any other values of the `mode` attribute.</span></span> <span data-ttu-id="52a72-150">自定义类型必须派生自 <xref:System.IdentityModel.Services.CookieHandler> 类。</span><span class="sxs-lookup"><span data-stu-id="52a72-150">The custom type must be derived from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="52a72-151">父元素</span><span class="sxs-lookup"><span data-stu-id="52a72-151">Parent Elements</span></span>  
  
|<span data-ttu-id="52a72-152">元素</span><span class="sxs-lookup"><span data-stu-id="52a72-152">Element</span></span>|<span data-ttu-id="52a72-153">说明</span><span class="sxs-lookup"><span data-stu-id="52a72-153">Description</span></span>|  
|-------------|-----------------|  
|[\<federationConfiguration>](federationconfiguration.md)|<span data-ttu-id="52a72-154">包含配置 <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) 和 <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) 的设置。</span><span class="sxs-lookup"><span data-stu-id="52a72-154">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="52a72-155">备注</span><span class="sxs-lookup"><span data-stu-id="52a72-155">Remarks</span></span>  

 <span data-ttu-id="52a72-156"><xref:System.IdentityModel.Services.CookieHandler>负责在 HTTP 协议级别读取和写入原始 cookie。</span><span class="sxs-lookup"><span data-stu-id="52a72-156">The <xref:System.IdentityModel.Services.CookieHandler> is responsible for reading and writing raw cookies at the HTTP protocol level.</span></span> <span data-ttu-id="52a72-157">可以配置 <xref:System.IdentityModel.Services.ChunkedCookieHandler> 从类派生的或自定义 cookie 处理程序 <xref:System.IdentityModel.Services.CookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="52a72-157">You can configure either a <xref:System.IdentityModel.Services.ChunkedCookieHandler> or a custom cookie handler derived from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="52a72-158">若要配置分块 cookie 处理程序，请将 mode 属性设置为 "分块" 或 "Default"。</span><span class="sxs-lookup"><span data-stu-id="52a72-158">To configure a chunked cookie handler, set the mode attribute to "Chunked" or "Default".</span></span> <span data-ttu-id="52a72-159">默认块区大小为2000个字节，但您可以选择通过包括子元素来指定不同的区块大小 `<chunkedCookieHandler>` 。</span><span class="sxs-lookup"><span data-stu-id="52a72-159">The default chunk size is 2000 bytes, but you may optionally specify a different chunk size by including a `<chunkedCookieHandler>` child element.</span></span>  
  
 <span data-ttu-id="52a72-160">若要配置自定义 cookie 处理程序，请将 mode 属性设置为 "Custom"。</span><span class="sxs-lookup"><span data-stu-id="52a72-160">To configure a custom cookie handler, set the mode attribute to "Custom".</span></span> <span data-ttu-id="52a72-161">还必须指定 `<customCookieHandler>` 引用自定义处理程序的类型的子元素。</span><span class="sxs-lookup"><span data-stu-id="52a72-161">You must also specify a `<customCookieHandler>` child element that references the type of your custom handler.</span></span>  
  
 <span data-ttu-id="52a72-162">`<cookieHandler>`元素由 <xref:System.IdentityModel.Services.CookieHandlerElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="52a72-162">The `<cookieHandler>` element is represented by the <xref:System.IdentityModel.Services.CookieHandlerElement> class.</span></span> <span data-ttu-id="52a72-163">在配置中指定的 cookie 处理程序可通过 <xref:System.IdentityModel.Services.Configuration.FederationConfiguration.CookieHandler%2A> <xref:System.IdentityModel.Services.Configuration.FederationConfiguration> 属性上设置的对象的属性获得 <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfiguration%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="52a72-163">The cookie handler that was specified in configuration is available from the <xref:System.IdentityModel.Services.Configuration.FederationConfiguration.CookieHandler%2A> property of the <xref:System.IdentityModel.Services.Configuration.FederationConfiguration> object set on the <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfiguration%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="52a72-164">示例</span><span class="sxs-lookup"><span data-stu-id="52a72-164">Example</span></span>  

 <span data-ttu-id="52a72-165">下面的 XML 显示了一个 `<cookieHandler>` 元素。</span><span class="sxs-lookup"><span data-stu-id="52a72-165">The following XML shows a `<cookieHandler>` element.</span></span> <span data-ttu-id="52a72-166">在此示例中，由于 `mode` 未指定属性，SAM 将使用默认的 cookie 处理程序。</span><span class="sxs-lookup"><span data-stu-id="52a72-166">In this example, because the `mode` attribute is not specified, the default cookie handler will be used by the SAM.</span></span> <span data-ttu-id="52a72-167">这是类的实例 <xref:System.IdentityModel.Services.ChunkedCookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="52a72-167">This is an instance of the <xref:System.IdentityModel.Services.ChunkedCookieHandler> class.</span></span> <span data-ttu-id="52a72-168">由于 `<chunkedCookieHandler>` 未指定子元素，将使用默认的块区大小。</span><span class="sxs-lookup"><span data-stu-id="52a72-168">Because the `<chunkedCookieHandler>` child element is not specified, the default chunk size will be used.</span></span> <span data-ttu-id="52a72-169">不需要 HTTPS，因为 `requireSsl` 已设置属性 `false` 。</span><span class="sxs-lookup"><span data-stu-id="52a72-169">HTTPS will not be required because the `requireSsl` attribute is set `false`.</span></span>  
  
> [!WARNING]
> <span data-ttu-id="52a72-170">在此示例中，无需 HTTPS 即可写入会话 cookie。</span><span class="sxs-lookup"><span data-stu-id="52a72-170">In this example, HTTPS is not required to write session cookies.</span></span> <span data-ttu-id="52a72-171">这是因为 `requireSsl` 元素上的特性 `<cookieHandler>` 设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="52a72-171">This is because the `requireSsl` attribute on the `<cookieHandler>` element is set to `false`.</span></span> <span data-ttu-id="52a72-172">对于大多数生产环境，不建议使用此设置，因为这可能会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="52a72-172">This setting is not recommended for most production environments as it may present a security risk.</span></span>  
  
```xml  
<cookieHandler requireSsl="false" />  
```  
  
## <a name="see-also"></a><span data-ttu-id="52a72-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="52a72-173">See also</span></span>

- <xref:System.IdentityModel.Services.CookieHandler>
- <xref:System.IdentityModel.Services.ChunkedCookieHandler>
- <xref:System.IdentityModel.Services.SessionAuthenticationModule>

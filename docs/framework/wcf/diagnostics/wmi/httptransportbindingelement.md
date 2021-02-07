---
description: 了解详细信息： HttpTransportBindingElement
title: HttpTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 088a7bce-6bb2-4839-ad74-f68d4b1aa0f9
ms.openlocfilehash: 6c516dd7124d52828145787d55421d12031c2d36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757366"
---
# <a name="httptransportbindingelement"></a><span data-ttu-id="14831-103">HttpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="14831-103">HttpTransportBindingElement</span></span>

<span data-ttu-id="14831-104">HttpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="14831-104">HttpTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="14831-105">语法</span><span class="sxs-lookup"><span data-stu-id="14831-105">Syntax</span></span>  
  
```csharp
class HttpTransportBindingElement : TransportBindingElement  
{  
  boolean AllowCookies;  
  string AuthenticationScheme;  
  boolean BypassProxyOnLocal;  
  string HostNameComparisonMode;  
  boolean KeepAliveEnabled;  
  sint32 MaxBufferSize;  
  string ProxyAddress;  
  string ProxyAuthenticationScheme;  
  string Realm;  
  string TransferMode;  
  boolean UnsafeConnectionNtlmAuthentication;  
  boolean UseDefaultWebProxy;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="14831-106">方法</span><span class="sxs-lookup"><span data-stu-id="14831-106">Methods</span></span>  

 <span data-ttu-id="14831-107">HttpTransportBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="14831-107">The HttpTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="14831-108">属性</span><span class="sxs-lookup"><span data-stu-id="14831-108">Properties</span></span>  

 <span data-ttu-id="14831-109">HttpTransportBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="14831-109">The HttpTransportBindingElement class has the following properties:</span></span>  
  
### <a name="allowcookies"></a><span data-ttu-id="14831-110">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="14831-110">AllowCookies</span></span>  

 <span data-ttu-id="14831-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="14831-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="14831-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-113">一个值，指示客户端是否接受 cookie 并根据将来的请求对其进行传播。</span><span class="sxs-lookup"><span data-stu-id="14831-113">A value that indicates whether the client accepts cookies and propagates them on future requests.</span></span>  
  
### <a name="authenticationscheme"></a><span data-ttu-id="14831-114">AuthenticationScheme</span><span class="sxs-lookup"><span data-stu-id="14831-114">AuthenticationScheme</span></span>  

 <span data-ttu-id="14831-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="14831-115">Data type: string</span></span>  
  
 <span data-ttu-id="14831-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-117">用来验证 HTTP 侦听器正在处理的客户端请求的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="14831-117">The authentication scheme used to authenticate client requests being processed by an HTTP listener.</span></span>  
  
### <a name="bypassproxyonlocal"></a><span data-ttu-id="14831-118">BypassProxyOnLocal</span><span class="sxs-lookup"><span data-stu-id="14831-118">BypassProxyOnLocal</span></span>  

 <span data-ttu-id="14831-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="14831-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="14831-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-121">一个值，指示是否忽略本地地址的代理。</span><span class="sxs-lookup"><span data-stu-id="14831-121">A value that indicates whether proxies are ignored for local addresses.</span></span>  
  
### <a name="hostnamecomparisonmode"></a><span data-ttu-id="14831-122">HostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="14831-122">HostNameComparisonMode</span></span>  

 <span data-ttu-id="14831-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="14831-123">Data type: string</span></span>  
  
 <span data-ttu-id="14831-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-125">一个值，指示在对 URI 进行匹配时，是否使用主机名来访问服务。</span><span class="sxs-lookup"><span data-stu-id="14831-125">A value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>  
  
### <a name="keepaliveenabled"></a><span data-ttu-id="14831-126">KeepAliveEnabled</span><span class="sxs-lookup"><span data-stu-id="14831-126">KeepAliveEnabled</span></span>  

 <span data-ttu-id="14831-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="14831-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="14831-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-129">启用后，HTTP 连接将保持活动状态，无论是什么活动级别。</span><span class="sxs-lookup"><span data-stu-id="14831-129">When enabled, HTTP connections are kept alive regardless of activity level.</span></span>  
  
### <a name="maxbuffersize"></a><span data-ttu-id="14831-130">MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="14831-130">MaxBufferSize</span></span>  

 <span data-ttu-id="14831-131">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="14831-131">Data type: sint32</span></span>  
  
 <span data-ttu-id="14831-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-133">缓冲池的最大大小。</span><span class="sxs-lookup"><span data-stu-id="14831-133">The maximum size of the buffer pool.</span></span>  
  
### <a name="proxyaddress"></a><span data-ttu-id="14831-134">ProxyAddress</span><span class="sxs-lookup"><span data-stu-id="14831-134">ProxyAddress</span></span>  

 <span data-ttu-id="14831-135">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="14831-135">Data type: string</span></span>  
  
 <span data-ttu-id="14831-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-137">一个 URI，包含用于 HTTP 请求的代理地址。</span><span class="sxs-lookup"><span data-stu-id="14831-137">A URI that contains the address of the proxy to use for HTTP requests.</span></span>  
  
### <a name="proxyauthenticationscheme"></a><span data-ttu-id="14831-138">ProxyAuthenticationScheme</span><span class="sxs-lookup"><span data-stu-id="14831-138">ProxyAuthenticationScheme</span></span>  

 <span data-ttu-id="14831-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="14831-139">Data type: string</span></span>  
  
 <span data-ttu-id="14831-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-141">用来验证 HTTP 代理正在处理的客户端请求的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="14831-141">The authentication scheme used to authenticate client requests being processed by an HTTP proxy.</span></span>  
  
### <a name="realm"></a><span data-ttu-id="14831-142">领域</span><span class="sxs-lookup"><span data-stu-id="14831-142">Realm</span></span>  

 <span data-ttu-id="14831-143">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="14831-143">Data type: string</span></span>  
  
 <span data-ttu-id="14831-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-145">身份验证领域。</span><span class="sxs-lookup"><span data-stu-id="14831-145">The authentication realm.</span></span>  
  
### <a name="transfermode"></a><span data-ttu-id="14831-146">TransferMode</span><span class="sxs-lookup"><span data-stu-id="14831-146">TransferMode</span></span>  

 <span data-ttu-id="14831-147">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="14831-147">Data type: string</span></span>  
  
 <span data-ttu-id="14831-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-149">一个值，指定对消息进行缓冲处理还是流式处理，或者指定消息是请求还是响应。</span><span class="sxs-lookup"><span data-stu-id="14831-149">A value that specifies whether messages are buffered or streamed or a request or response.</span></span>  
  
### <a name="unsafeconnectionntlmauthentication"></a><span data-ttu-id="14831-150">UnsafeConnectionNtlmAuthentication</span><span class="sxs-lookup"><span data-stu-id="14831-150">UnsafeConnectionNtlmAuthentication</span></span>  

 <span data-ttu-id="14831-151">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="14831-151">Data type: boolean</span></span>  
  
 <span data-ttu-id="14831-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-153">一个值，指示服务器上是否启用了不安全连接共享。</span><span class="sxs-lookup"><span data-stu-id="14831-153">A value that indicates whether Unsafe Connection Sharing is enabled on the server.</span></span>  
  
### <a name="usedefaultwebproxy"></a><span data-ttu-id="14831-154">UseDefaultWebProxy</span><span class="sxs-lookup"><span data-stu-id="14831-154">UseDefaultWebProxy</span></span>  

 <span data-ttu-id="14831-155">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="14831-155">Data type: boolean</span></span>  
  
 <span data-ttu-id="14831-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="14831-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="14831-157">一个值，指示是否使用计算机范围的代理设置，而不使用用户特定的设置。</span><span class="sxs-lookup"><span data-stu-id="14831-157">A value that indicates whether the machine-wide proxy settings are used rather than the user specific settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="14831-158">要求</span><span class="sxs-lookup"><span data-stu-id="14831-158">Requirements</span></span>  
  
|<span data-ttu-id="14831-159">MOF</span><span class="sxs-lookup"><span data-stu-id="14831-159">MOF</span></span>|<span data-ttu-id="14831-160">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="14831-160">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="14831-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="14831-161">Namespace</span></span>|<span data-ttu-id="14831-162">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="14831-162">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="14831-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="14831-163">See also</span></span>

- <xref:System.ServiceModel.Channels.HttpTransportBindingElement>

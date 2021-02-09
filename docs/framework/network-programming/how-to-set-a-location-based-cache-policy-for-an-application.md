---
description: 详细了解：操作说明：为应用程序设置基于位置的缓存策略
title: 如何：为应用程序设置基于位置的缓存策略
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- explicitly defining cache behavior
- location-based cache policies
- local cache
- request cache policies
- cache [.NET Framework], location-based policies
ms.assetid: 683bb88e-3411-4f46-9686-3411b6ba511c
ms.openlocfilehash: d86e40e24eacb6ce3107e50213941c1169191943
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662775"
---
# <a name="how-to-set-a-location-based-cache-policy-for-an-application"></a><span data-ttu-id="1ccec-103">如何：为应用程序设置基于位置的缓存策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-103">How to: Set a Location-Based Cache Policy for an Application</span></span>

<span data-ttu-id="1ccec-104">基于位置的缓存策略允许应用程序基于所请求资源的位置显式定义缓存行为。</span><span class="sxs-lookup"><span data-stu-id="1ccec-104">Location-based cache policies allow an application to explicitly define caching behavior based on the location of the requested resource.</span></span> <span data-ttu-id="1ccec-105">本主题演示如何以编程方式设置缓存策略。</span><span class="sxs-lookup"><span data-stu-id="1ccec-105">This topic demonstrates setting the cache policy programmatically.</span></span> <span data-ttu-id="1ccec-106">有关使用配置文件为应用程序设置策略的信息，请参阅 [\<requestCaching> 元素（网络设置）](../configure-apps/file-schema/network/requestcaching-element-network-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="1ccec-106">For information on setting the policy for an application using the configuration files, see [\<requestCaching> Element (Network Settings)](../configure-apps/file-schema/network/requestcaching-element-network-settings.md).</span></span>  
  
### <a name="to-set-a-location-based-cache-policy-for-an-application"></a><span data-ttu-id="1ccec-107">为应用程序设置基于位置的缓存策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-107">To set a location-based cache policy for an application</span></span>  
  
1. <span data-ttu-id="1ccec-108">创建 <xref:System.Net.Cache.RequestCachePolicy> 或 <xref:System.Net.Cache.HttpRequestCachePolicy> 对象。</span><span class="sxs-lookup"><span data-stu-id="1ccec-108">Create a <xref:System.Net.Cache.RequestCachePolicy> or <xref:System.Net.Cache.HttpRequestCachePolicy> object.</span></span>  
  
2. <span data-ttu-id="1ccec-109">将策略对象设置为应用程序域的默认对象。</span><span class="sxs-lookup"><span data-stu-id="1ccec-109">Set the policy object as the default for the application domain.</span></span>  
  
### <a name="to-set-a-policy-that-takes-requested-resources-from-a-cache"></a><span data-ttu-id="1ccec-110">设置获取来自缓存的请求资源的策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-110">To set a policy that takes requested resources from a cache</span></span>  
  
- <span data-ttu-id="1ccec-111">创建获取来自缓存的请求资源的策略（若可用），否则通过将缓存级别设置为 <xref:System.Net.Cache.HttpRequestCacheLevel.CacheIfAvailable> 向服务器发送请求。</span><span class="sxs-lookup"><span data-stu-id="1ccec-111">Create a policy that takes requested resources from a cache if available, and otherwise, sends requests to the server, by setting the cache level to <xref:System.Net.Cache.HttpRequestCacheLevel.CacheIfAvailable>.</span></span> <span data-ttu-id="1ccec-112">可以由客户端和服务器之间的任何缓存实现请求，包括远程缓存。</span><span class="sxs-lookup"><span data-stu-id="1ccec-112">A request can be fulfilled by any cache between the client and server, including remote caches.</span></span>  
  
    ```csharp  
    public static void UseCacheIfAvailable()  
    {  
        HttpRequestCachePolicy policy = new HttpRequestCachePolicy  
            (HttpRequestCacheLevel.CacheIfAvailable);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub UseCacheIfAvailable()  
        Dim policy As New HttpRequestCachePolicy _  
             (HttpRequestCacheLevel.CacheIfAvailable)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-prevents-any-cache-from-supplying-resources"></a><span data-ttu-id="1ccec-113">设置防止任何缓存提供资源的策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-113">To set a policy that prevents any cache from supplying resources</span></span>  
  
- <span data-ttu-id="1ccec-114">通过将缓存级别设置为 <xref:System.Net.Cache.HttpRequestCacheLevel.NoCacheNoStore>，创建防止缓存提供请求的资源的策略。</span><span class="sxs-lookup"><span data-stu-id="1ccec-114">Create a policy that prevents any cache from supplying requested resources by setting the cache level to <xref:System.Net.Cache.HttpRequestCacheLevel.NoCacheNoStore>.</span></span> <span data-ttu-id="1ccec-115">此策略级别从本地缓存中删除资源（如果存在），并指示远程缓存也应删除资源。</span><span class="sxs-lookup"><span data-stu-id="1ccec-115">This policy level removes the resource from the local cache if it is present and indicates to remote caches that they should also remove the resource.</span></span>  
  
    ```csharp  
    public static void DoNotUseCache()  
    {  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy
            (HttpRequestCacheLevel.NoCacheNoStore);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub DoNotUseCache()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.NoCacheNoStore)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-returns-requested-resources-only-if-they-are-in-the-local-cache"></a><span data-ttu-id="1ccec-116">设置仅当请求的资源在本地缓存中时返回请求的资源的策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-116">To set a policy that returns requested resources only if they are in the local cache</span></span>  
  
- <span data-ttu-id="1ccec-117">通过将缓存级别设置为 <xref:System.Net.Cache.HttpRequestCacheLevel.CacheOnly>，创建仅当请求的资源在本地缓存中时返回请求的资源的策略。</span><span class="sxs-lookup"><span data-stu-id="1ccec-117">Create a policy that returns requested resources only if they are in the local cache by setting the cache level to <xref:System.Net.Cache.HttpRequestCacheLevel.CacheOnly>.</span></span> <span data-ttu-id="1ccec-118">如果请求的资源不在缓存中，将引发 <xref:System.Net.WebException> 异常。</span><span class="sxs-lookup"><span data-stu-id="1ccec-118">If the requested resource is not in the cache, a <xref:System.Net.WebException> exception is thrown.</span></span>  
  
    ```csharp  
    public static void OnlyUseCache()  
    {  
        HttpRequestCachePolicy policy = new HttpRequestCachePolicy
            (HttpRequestCacheLevel.CacheOnly);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub OnlyUseCache()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.CacheOnly)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-prevents-the-local-cache-from-supplying-resources"></a><span data-ttu-id="1ccec-119">设置防止本地缓存提供资源的策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-119">To set a policy that prevents the local cache from supplying resources</span></span>  
  
- <span data-ttu-id="1ccec-120">通过将缓存级别设置为 <xref:System.Net.Cache.HttpRequestCacheLevel.Refresh>，创建防止本地缓存提供请求的资源的策略。</span><span class="sxs-lookup"><span data-stu-id="1ccec-120">Create a policy that prevents the local cache from supplying requested resources by setting the cache level to <xref:System.Net.Cache.HttpRequestCacheLevel.Refresh>.</span></span> <span data-ttu-id="1ccec-121">如果请求的资源是中间缓存并已成功重新验证，中间缓存可提供请求的资源。</span><span class="sxs-lookup"><span data-stu-id="1ccec-121">If the requested resource is in an intermediate cache and is successfully revalidated, the intermediate cache can supply the requested resource.</span></span>  
  
    ```csharp  
    public static void DoNotUseLocalCache()  
    {  
     HttpRequestCachePolicy policy = new HttpRequestCachePolicy
            (HttpRequestCacheLevel.Refresh);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub DoNotUseLocalCache()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.Refresh)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-prevents-any-cache-from-supplying-requested-resources"></a><span data-ttu-id="1ccec-122">设置防止任何缓存提供请求的资源的策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-122">To set a policy that prevents any cache from supplying requested resources</span></span>  
  
- <span data-ttu-id="1ccec-123">通过将缓存级别设置为 <xref:System.Net.Cache.HttpRequestCacheLevel.Reload>，创建防止缓存提供请求的资源的策略。</span><span class="sxs-lookup"><span data-stu-id="1ccec-123">Create a policy that prevents any cache from supplying requested resources by setting the cache level to <xref:System.Net.Cache.HttpRequestCacheLevel.Reload>.</span></span> <span data-ttu-id="1ccec-124">服务器返回的资源可以存储在缓存中。</span><span class="sxs-lookup"><span data-stu-id="1ccec-124">The resource returned by the server can be stored in the cache.</span></span>  
  
    ```csharp  
    public static void SendToServer()  
    {  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy
            (HttpRequestCacheLevel.Reload);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub SendToServer()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.Reload)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-allows-any-cache-to-supply-requested-resources-if-the-resource-on-the-server-is-not-newer-than-the-cached-copy"></a><span data-ttu-id="1ccec-125">设置当服务器上的资源不比缓存副本新时，允许任何缓存提供请求的资源的策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-125">To set a policy that allows any cache to supply requested resources if the resource on the server is not newer than the cached copy</span></span>  
  
- <span data-ttu-id="1ccec-126">通过将缓存级别设置为 <xref:System.Net.Cache.HttpRequestCacheLevel.Revalidate>，创建当服务器上的资源不比缓存副本新时，允许任何缓存提供请求的资源的策略。</span><span class="sxs-lookup"><span data-stu-id="1ccec-126">Create a policy that allows any cache to supply requested resources if the resource on the server is not newer than the cached copy by setting the cache level to <xref:System.Net.Cache.HttpRequestCacheLevel.Revalidate>.</span></span>  
  
    ```csharp  
    public static void CheckServer()  
    {  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy  
             (HttpRequestCacheLevel.Revalidate);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub CheckServer()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.Revalidate)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="1ccec-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1ccec-127">See also</span></span>

- [<span data-ttu-id="1ccec-128">网络应用程序的缓存管理</span><span class="sxs-lookup"><span data-stu-id="1ccec-128">Cache Management for Network Applications</span></span>](cache-management-for-network-applications.md)
- [<span data-ttu-id="1ccec-129">缓存策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-129">Cache Policy</span></span>](cache-policy.md)
- [<span data-ttu-id="1ccec-130">基于位置的缓存策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-130">Location-Based Cache Policies</span></span>](location-based-cache-policies.md)
- [<span data-ttu-id="1ccec-131">基于时间的缓存策略</span><span class="sxs-lookup"><span data-stu-id="1ccec-131">Time-Based Cache Policies</span></span>](time-based-cache-policies.md)
- [<span data-ttu-id="1ccec-132">\<requestCaching> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="1ccec-132">\<requestCaching> Element (Network Settings)</span></span>](../configure-apps/file-schema/network/requestcaching-element-network-settings.md)

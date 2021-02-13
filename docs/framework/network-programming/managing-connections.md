---
title: 管理连接
description: 了解将 HTTP 用于数据资源的应用程序如何使用 .NET Framework ServicePoint 和 ServicePointManager 类管理连接。
ms.date: 01/25/2021
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Internet, connections
- HTTP, classes for connecting
- requesting data from Internet, connections
- sending data, connections
- receiving data, connections
- ServicePoint class, about ServicePoint class
- response to Internet request, connections
- connections [.NET Framework], classes
- network resources, connections
- downloading Internet resources, connections
- ServicePointManager class, about ServicePointManager class
ms.assetid: 9b3d3de7-189f-4f7d-81ae-9c29c441aaaa
ms.openlocfilehash: 9ea93c3a9c484fd2a3de58b4d484b1e8445da155
ms.sourcegitcommit: 4df8e005c074ceb1f978f007b222fe253be2baf3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "99548053"
---
# <a name="managing-connections"></a><span data-ttu-id="2e034-103">管理连接</span><span class="sxs-lookup"><span data-stu-id="2e034-103">Managing Connections</span></span>

<span data-ttu-id="2e034-104">使用 HTTP 连接到数据资源的应用程序可使用 .NET Framework 的 <xref:System.Net.ServicePoint> 和 <xref:System.Net.ServicePointManager> 类管理与 Internet 的连接并有助于实现最优规模和最佳性能。</span><span class="sxs-lookup"><span data-stu-id="2e034-104">Applications that use HTTP to connect to data resources can use the .NET Framework's <xref:System.Net.ServicePoint> and <xref:System.Net.ServicePointManager> classes to manage connections to the Internet and to help them achieve optimum scale and performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="2e034-105">`ServicePoint` 和 `ServicePointManager` 在 .NET Core、.NET 5 及更高版本上被认为是旧的。</span><span class="sxs-lookup"><span data-stu-id="2e034-105">`ServicePoint` and `ServicePointManager` are considered legacy on .NET Core, .NET 5, and later versions.</span></span> <span data-ttu-id="2e034-106">它们的大多数属性和方法在这些版本中都没有实现。</span><span class="sxs-lookup"><span data-stu-id="2e034-106">Most of their properties and methods are not implemented in these versions.</span></span> <span data-ttu-id="2e034-107">如果被实现，它们不会影响或跟踪有关 `HttpClient` 网络 API 的任何内容。</span><span class="sxs-lookup"><span data-stu-id="2e034-107">When they are implemented, they don't affect or track anything about `HttpClient` networking APIs.</span></span>
  
 <span data-ttu-id="2e034-108">ServicePoint 类给应用程序提供了终结点，应用程序连接到终结点即可访问 Internet 资源。</span><span class="sxs-lookup"><span data-stu-id="2e034-108">The **ServicePoint** class provides an application with an endpoint to which the application can connect to access Internet resources.</span></span> <span data-ttu-id="2e034-109">每个 ServicePoint 都包含信息，该信息有助于通过共享连接之间的优化信息改进性能，优化与 Internet 服务器的连接。</span><span class="sxs-lookup"><span data-stu-id="2e034-109">Each **ServicePoint** contains information that helps optimize connections with an Internet server by sharing optimization information between connections to improve performance.</span></span>  
  
 <span data-ttu-id="2e034-110">每个 ServicePoint 都由统一资源标识符 (URI) 标识，并根据方案标识符和 URI 的主机片段分类。</span><span class="sxs-lookup"><span data-stu-id="2e034-110">Each **ServicePoint** is identified by a Uniform Resource Identifier (URI) and is categorized according to the scheme identifier and host fragments of the URI.</span></span> <span data-ttu-id="2e034-111">例如，将由同一 ServicePoint 实例提供对 URI `http://www.contoso.com/index.htm` 和 `http://www.contoso.com/news.htm?date=today` 的请求，因为它们具有相同的方案标识符片段 (http) 和主机片段(`www.contoso.com`)。</span><span class="sxs-lookup"><span data-stu-id="2e034-111">For example, the same **ServicePoint** instance would provide requests to the URIs `http://www.contoso.com/index.htm` and `http://www.contoso.com/news.htm?date=today` since they have the same scheme identifier (http) and host fragments (`www.contoso.com`).</span></span> <span data-ttu-id="2e034-112">如果应用程序已具有与服务器 `www.contoso.com` 的持久连接，它使用该连接检索两个请求，避免创建两个连接。</span><span class="sxs-lookup"><span data-stu-id="2e034-112">If the application already has a persistent connection to the server `www.contoso.com`, it uses that connection to retrieve both requests, avoiding the need to create two connections.</span></span>  
  
 <span data-ttu-id="2e034-113">ServicePointManager 是管理 ServicePoint 实例的创建和析构的静态类。</span><span class="sxs-lookup"><span data-stu-id="2e034-113">**ServicePointManager** is a static class that manages the creation and destruction of **ServicePoint** instances.</span></span> <span data-ttu-id="2e034-114">如果应用程序请求一个不在现有  ServicePoint 实例集合里的 Internet 资源， ServicePointManager 将会创建 ServicePoint。</span><span class="sxs-lookup"><span data-stu-id="2e034-114">The **ServicePointManager** creates a **ServicePoint** when the application requests an Internet resource that is not in the collection of existing **ServicePoint** instances.</span></span> <span data-ttu-id="2e034-115">在 ServicePoint 实例超出最长空闲时间或现有数量超过应用程序的 ServicePoint 实例最大数量时，将销毁 ServicePoint 实例  。</span><span class="sxs-lookup"><span data-stu-id="2e034-115">**ServicePoint** instances are destroyed when they have exceeded their maximum idle time or when the number of existing **ServicePoint** instances exceeds the maximum number of **ServicePoint** instances for the application.</span></span> <span data-ttu-id="2e034-116">可通过设置 ServicePointManager 上的 <xref:System.Net.ServicePointManager.MaxServicePointIdleTime%2A> 和 <xref:System.Net.ServicePointManager.MaxServicePoints%2A> 属性，来控制默认空闲时间的最大值和 ServicePoint 实例的最大数量。</span><span class="sxs-lookup"><span data-stu-id="2e034-116">You can control both the default maximum idle time and the maximum number of **ServicePoint** instances by setting the <xref:System.Net.ServicePointManager.MaxServicePointIdleTime%2A> and <xref:System.Net.ServicePointManager.MaxServicePoints%2A> properties on the **ServicePointManager**.</span></span>  
  
 <span data-ttu-id="2e034-117">客户端和服务器之间的连接数可能会对应用程序吞吐量产生重大影响。</span><span class="sxs-lookup"><span data-stu-id="2e034-117">The number of connections between a client and server can have a dramatic impact on application throughput.</span></span> <span data-ttu-id="2e034-118">默认情况下，使用 <xref:System.Net.HttpWebRequest> 类的应用程序最多使用与给定服务器的两个持久连接，但是，可以基于每个应用程序设置最大连接数。</span><span class="sxs-lookup"><span data-stu-id="2e034-118">By default, an application using the <xref:System.Net.HttpWebRequest> class uses a maximum of two persistent connections to a given server, but you can set the maximum number of connections on a per-application basis.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2e034-119">HTTP/1.1 规范将一个应用程序中的连接数限制为每个服务器两个连接。</span><span class="sxs-lookup"><span data-stu-id="2e034-119">The HTTP/1.1 specification limits the number of connections from an application to two connections per server.</span></span>  
  
 <span data-ttu-id="2e034-120">连接的最佳数目取决于应用程序运行的实际情况。</span><span class="sxs-lookup"><span data-stu-id="2e034-120">The optimum number of connections depends on the actual conditions in which the application runs.</span></span> <span data-ttu-id="2e034-121">增加应用程序的可用连接数可能不影响应用程序性能。</span><span class="sxs-lookup"><span data-stu-id="2e034-121">Increasing the number of connections available to the application may not affect application performance.</span></span> <span data-ttu-id="2e034-122">要确定更多连接的影响，请在改变连接数时运行性能测试。</span><span class="sxs-lookup"><span data-stu-id="2e034-122">To determine the impact of more connections, run performance tests while varying the number of connections.</span></span> <span data-ttu-id="2e034-123">在应用程序初始化时改变 ServicePointManager 类上的静态 <xref:System.Net.ServicePointManager.DefaultConnectionLimit%2A> 属性，可以更改应用程序使用的连接数，如以下代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="2e034-123">You can change the number of connections that an application uses by changing the static <xref:System.Net.ServicePointManager.DefaultConnectionLimit%2A> property on the **ServicePointManager** class at application initialization, as shown in the following code sample.</span></span>  
  
```csharp  
// Set the maximum number of connections per server to 4.  
ServicePointManager.DefaultConnectionLimit = 4;  
```  
  
```vb  
' Set the maximum number of connections per server to 4.  
ServicePointManager.DefaultConnectionLimit = 4  
```  
  
 <span data-ttu-id="2e034-124">更改  ServicePointManager.DefaultConnectionLimit 属性不会影响之前初始化的 ServicePoint 实例。</span><span class="sxs-lookup"><span data-stu-id="2e034-124">Changing the **ServicePointManager.DefaultConnectionLimit** property does not affect previously initialized **ServicePoint** instances.</span></span> <span data-ttu-id="2e034-125">下面的代码演示如何将服务器 `http://www.contoso.com` 现有 ServicePoint 上的连接限制更改为存储在 `newLimit` 中的值。</span><span class="sxs-lookup"><span data-stu-id="2e034-125">The following code demonstrates changing the connection limit on an existing **ServicePoint** for the server `http://www.contoso.com` to the value stored in `newLimit`.</span></span>  
  
```csharp  
Uri uri = new Uri("http://www.contoso.com/");  
ServicePoint sp = ServicePointManager.FindServicePoint(uri);  
sp.ConnectionLimit = newLimit;  
```  
  
```vb  
Dim uri As New Uri("http://www.contoso.com/")  
Dim sp As ServicePoint = ServicePointManager.FindServicePoint(uri)  
sp.ConnectionLimit = newLimit  
```  
  
## <a name="see-also"></a><span data-ttu-id="2e034-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="2e034-126">See also</span></span>

- [<span data-ttu-id="2e034-127">连接分组</span><span class="sxs-lookup"><span data-stu-id="2e034-127">Connection Grouping</span></span>](connection-grouping.md)
- [<span data-ttu-id="2e034-128">使用应用程序协议</span><span class="sxs-lookup"><span data-stu-id="2e034-128">Using Application Protocols</span></span>](using-application-protocols.md)

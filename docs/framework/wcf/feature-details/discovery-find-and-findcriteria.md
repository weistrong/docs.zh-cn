---
description: 了解详细信息：发现查找和 s
title: Discovery Find 和 FindCriteria
ms.date: 03/30/2017
ms.assetid: 99016fa4-1778-495b-b4cc-0e22fbec42c6
ms.openlocfilehash: 3a4428a89ba4122f528d1c01e4b5a6b8ea8d2935
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756313"
---
# <a name="discovery-find-and-findcriteria"></a><span data-ttu-id="8673a-103">Discovery Find 和 FindCriteria</span><span class="sxs-lookup"><span data-stu-id="8673a-103">Discovery Find and FindCriteria</span></span>

<span data-ttu-id="8673a-104">发现查找操作是发现功能中的主要操作之一，它由客户端启动，用于发现一个或多个服务。</span><span class="sxs-lookup"><span data-stu-id="8673a-104">A discovery find operation is initiated by a client to discover one or more services and is one of the main actions in discovery.</span></span> <span data-ttu-id="8673a-105">执行查找时将通过网络发送一条 WS-Discovery Probe 消息。</span><span class="sxs-lookup"><span data-stu-id="8673a-105">Performing a find sends a WS-Discovery Probe message over the network.</span></span> <span data-ttu-id="8673a-106">与指定条件匹配的服务通过 WS-Discovery ProbeMatch 消息进行答复。</span><span class="sxs-lookup"><span data-stu-id="8673a-106">Services that match the criteria specified reply with WS-Discovery ProbeMatch messages.</span></span> <span data-ttu-id="8673a-107">有关发现消息的详细信息，请参阅 [WS 发现规范](http://schemas.xmlsoap.org/ws/2004/10/discovery/ws-discovery.pdf)。</span><span class="sxs-lookup"><span data-stu-id="8673a-107">For more information about discovery messages, see the [WS-Discovery specification](http://schemas.xmlsoap.org/ws/2004/10/discovery/ws-discovery.pdf).</span></span>

## <a name="discoveryclient"></a><span data-ttu-id="8673a-108">DiscoveryClient</span><span class="sxs-lookup"><span data-stu-id="8673a-108">DiscoveryClient</span></span>

<span data-ttu-id="8673a-109"><xref:System.ServiceModel.Discovery.DiscoveryClient> 类提供执行查找操作的机制，并简化了发现客户端操作的执行过程。</span><span class="sxs-lookup"><span data-stu-id="8673a-109">The <xref:System.ServiceModel.Discovery.DiscoveryClient> class provides the mechanism to perform find operations and makes performing discovery client operations easy.</span></span> <span data-ttu-id="8673a-110">该类包含 <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A> 方法和 <xref:System.ServiceModel.Discovery.DiscoveryClient.FindAsync%2A> 方法，前者用于执行（阻塞的）同步查找，后者用于启动非阻塞的异步查找。</span><span class="sxs-lookup"><span data-stu-id="8673a-110">It contains a <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A> method, which performs a (blocking) synchronous find, and a <xref:System.ServiceModel.Discovery.DiscoveryClient.FindAsync%2A> method, which initiates a non-blocking asynchronous find.</span></span> <span data-ttu-id="8673a-111">这两个方法均采用 <xref:System.ServiceModel.Discovery.FindCriteria> 参数，并通过 <xref:System.ServiceModel.Discovery.FindResponse> 对象将结果提供给用户。</span><span class="sxs-lookup"><span data-stu-id="8673a-111">Both methods take a <xref:System.ServiceModel.Discovery.FindCriteria> parameter, and provide results to the user through a <xref:System.ServiceModel.Discovery.FindResponse> object.</span></span>

## <a name="findcriteria"></a><span data-ttu-id="8673a-112">FindCriteria</span><span class="sxs-lookup"><span data-stu-id="8673a-112">FindCriteria</span></span>

<span data-ttu-id="8673a-113"><xref:System.ServiceModel.Discovery.FindCriteria> 包含若干属性，可将这些属性划分为搜索条件（指定要查找的服务）和查找终止条件（搜索应持续的时长）。</span><span class="sxs-lookup"><span data-stu-id="8673a-113"><xref:System.ServiceModel.Discovery.FindCriteria> has several properties, which can be grouped into search criteria, which specify what services you are looking for, and find termination criteria (how long the search should last).</span></span> <span data-ttu-id="8673a-114"><xref:System.ServiceModel.Discovery.FindCriteria> 可包含多个搜索条件。</span><span class="sxs-lookup"><span data-stu-id="8673a-114">A <xref:System.ServiceModel.Discovery.FindCriteria> can contain multiple search criteria.</span></span> <span data-ttu-id="8673a-115">默认情况下，服务必须与所有组件匹配，否则不会将其自身视为匹配的服务。</span><span class="sxs-lookup"><span data-stu-id="8673a-115">By default, the service has to match all of the components otherwise it does not consider itself a matching service.</span></span> <span data-ttu-id="8673a-116">如果要查找仅与某些条件匹配的服务，您可以对服务实现自定义查找逻辑，也可以使用多个查询。</span><span class="sxs-lookup"><span data-stu-id="8673a-116">If you want to find services that only match some of the criteria, you can implement custom find logic on the service or you can use multiple queries.</span></span>

<span data-ttu-id="8673a-117">搜索条件包括：</span><span class="sxs-lookup"><span data-stu-id="8673a-117">Search criteria include:</span></span>

- <span data-ttu-id="8673a-118"><xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElement> - 可选项。</span><span class="sxs-lookup"><span data-stu-id="8673a-118"><xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElement> - Optional.</span></span> <span data-ttu-id="8673a-119">要搜索的服务的协定名称以及搜索服务时通常采用的条件。</span><span class="sxs-lookup"><span data-stu-id="8673a-119">The contract name of the service being searched for and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="8673a-120">如果指定了多个协定名称，则只有与所有协定均匹配的服务终结点才会进行答复。</span><span class="sxs-lookup"><span data-stu-id="8673a-120">If more than one contract name is specified, only service endpoints matching ALL contracts reply.</span></span> <span data-ttu-id="8673a-121">请注意，在 WCF 中，一个终结点只能支持一个协定。</span><span class="sxs-lookup"><span data-stu-id="8673a-121">Note that in WCF an endpoint can only support one contract.</span></span>

- <span data-ttu-id="8673a-122"><xref:System.ServiceModel.Discovery.Configuration.ScopeElement> - 可选项。</span><span class="sxs-lookup"><span data-stu-id="8673a-122"><xref:System.ServiceModel.Discovery.Configuration.ScopeElement> - Optional.</span></span> <span data-ttu-id="8673a-123">范围表示对各服务终结点进行分类所使用的绝对 URI。</span><span class="sxs-lookup"><span data-stu-id="8673a-123">Scopes are absolute URIs that are used to categorize individual service endpoints.</span></span> <span data-ttu-id="8673a-124">如果多个终结点公开同一协定，并且您希望采用某种方法来搜索终结点的子集，则您可能希望使用此搜索条件。</span><span class="sxs-lookup"><span data-stu-id="8673a-124">You may want to use this in scenarios where multiple endpoints expose the same contract and you want a way to search for a subset of the endpoints.</span></span> <span data-ttu-id="8673a-125">如果指定了多个范围，则只有与所有范围匹配的服务终结点才会进行答复。</span><span class="sxs-lookup"><span data-stu-id="8673a-125">If more than one scope is specified, only service endpoints matching ALL scopes reply.</span></span>

- <span data-ttu-id="8673a-126"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchBy%2A> - 指定当对 Probe 消息中的范围和终结点中的范围进行匹配时采用的匹配算法。</span><span class="sxs-lookup"><span data-stu-id="8673a-126"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchBy%2A> - Specifies the matching algorithm to use while matching the scopes in the Probe message with that of the endpoint.</span></span> <span data-ttu-id="8673a-127">支持以下五种范围匹配规则：</span><span class="sxs-lookup"><span data-stu-id="8673a-127">There are five supported scope-matching rules:</span></span>

  - <span data-ttu-id="8673a-128"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByExact?displayProperty=nameWithType> 执行区分大小写的基本字符串比较。</span><span class="sxs-lookup"><span data-stu-id="8673a-128"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByExact?displayProperty=nameWithType> does a basic case-sensitive string comparison.</span></span>

  - <span data-ttu-id="8673a-129"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByPrefix?displayProperty=nameWithType> 按由 "/" 分隔的段匹配。</span><span class="sxs-lookup"><span data-stu-id="8673a-129"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByPrefix?displayProperty=nameWithType> matches by segments separated by "/".</span></span> <span data-ttu-id="8673a-130">搜索与 `http://contoso/building1` 作用域的服务匹配 `http://contoso/building/floor1` 。</span><span class="sxs-lookup"><span data-stu-id="8673a-130">A search for `http://contoso/building1` matches a service with scope `http://contoso/building/floor1`.</span></span> <span data-ttu-id="8673a-131">请注意，它不匹配， `http://contoso/building100` 因为最后两个段不匹配。</span><span class="sxs-lookup"><span data-stu-id="8673a-131">Note that it does not match `http://contoso/building100` because the last two segments do not match.</span></span>

  - <span data-ttu-id="8673a-132"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByLdap?displayProperty=nameWithType> 按使用 LDAP URL 的段来匹配范围。</span><span class="sxs-lookup"><span data-stu-id="8673a-132"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByLdap?displayProperty=nameWithType> matches scopes by segments using an LDAP URL.</span></span>

  - <span data-ttu-id="8673a-133"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByUuid?displayProperty=nameWithType> 通过使用 UUID 字符串来完全匹配范围。</span><span class="sxs-lookup"><span data-stu-id="8673a-133"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByUuid?displayProperty=nameWithType> matches scopes exactly using a UUID string.</span></span>

  - <span data-ttu-id="8673a-134"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByNone?displayProperty=nameWithType> 仅匹配那些未指定范围的服务。</span><span class="sxs-lookup"><span data-stu-id="8673a-134"><xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByNone?displayProperty=nameWithType> matches only those services that do not specify a scope.</span></span>

  <span data-ttu-id="8673a-135">如果未指定范围匹配规则，则使用 <xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByPrefix>。</span><span class="sxs-lookup"><span data-stu-id="8673a-135">If a scope-matching rule is not specified, <xref:System.ServiceModel.Discovery.FindCriteria.ScopeMatchByPrefix> is used.</span></span>

<span data-ttu-id="8673a-136">终止条件包括：</span><span class="sxs-lookup"><span data-stu-id="8673a-136">Termination criteria include:</span></span>

1. <span data-ttu-id="8673a-137"><xref:System.ServiceModel.Discovery.FindCriteria.Duration%2A> - 等待网络上的服务所发送答复的最长时间。</span><span class="sxs-lookup"><span data-stu-id="8673a-137"><xref:System.ServiceModel.Discovery.FindCriteria.Duration%2A> - The maximum time to wait for replies from services on the network.</span></span> <span data-ttu-id="8673a-138">默认持续时间为 20 秒。</span><span class="sxs-lookup"><span data-stu-id="8673a-138">The default duration is 20 seconds.</span></span>

2. <span data-ttu-id="8673a-139"><xref:System.ServiceModel.Discovery.FindCriteria.MaxResults%2A> - 等待的答复的最大数目。</span><span class="sxs-lookup"><span data-stu-id="8673a-139"><xref:System.ServiceModel.Discovery.FindCriteria.MaxResults%2A> - The maximum number of replies to wait for.</span></span> <span data-ttu-id="8673a-140">如果在经过 <xref:System.ServiceModel.Discovery.FindCriteria.MaxResults%2A> 之前收到了 <xref:System.ServiceModel.Discovery.FindCriteria.Duration%2A> 答复，查找操作将结束。</span><span class="sxs-lookup"><span data-stu-id="8673a-140">If <xref:System.ServiceModel.Discovery.FindCriteria.MaxResults%2A> replies are received before <xref:System.ServiceModel.Discovery.FindCriteria.Duration%2A> has elapsed, the find operation ends.</span></span>

## <a name="findresponse"></a><span data-ttu-id="8673a-141">FindResponse</span><span class="sxs-lookup"><span data-stu-id="8673a-141">FindResponse</span></span>

<span data-ttu-id="8673a-142"><xref:System.ServiceModel.Discovery.FindResponse> 具有一个 <xref:System.ServiceModel.Discovery.FindResponse.Endpoints%2A> 集合属性，该集合属性包含网络上的匹配服务发送的所有答复。</span><span class="sxs-lookup"><span data-stu-id="8673a-142"><xref:System.ServiceModel.Discovery.FindResponse> has an <xref:System.ServiceModel.Discovery.FindResponse.Endpoints%2A> collection property that contains any replies sent by matching services on the network.</span></span> <span data-ttu-id="8673a-143">如果没有任何服务进行答复，该集合将为空。</span><span class="sxs-lookup"><span data-stu-id="8673a-143">If no services replied, the collection is empty.</span></span> <span data-ttu-id="8673a-144">如果一个或多个服务进行了答复，则各答复将分别存储在一个 <xref:System.ServiceModel.Discovery.EndpointDiscoveryMetadata> 对象中，该对象包含有关服务的地址、协定以及某些其他信息。</span><span class="sxs-lookup"><span data-stu-id="8673a-144">If one or more services replied, each reply is stored in an <xref:System.ServiceModel.Discovery.EndpointDiscoveryMetadata> object, which contains the address, contract, and some additional information about the service.</span></span>

<span data-ttu-id="8673a-145">下面的示例演示如何在代码中执行查找操作。</span><span class="sxs-lookup"><span data-stu-id="8673a-145">The following example shows how to perform a find operation in code.</span></span>

```csharp
// Create DiscoveryClient
DiscoveryClient discoveryClient = new DiscoveryClient(new UdpDiscoveryEndpoint());

// Create FindCriteria
FindCriteria findCriteria = new FindCriteria(typeof(IPrinterService));
findCriteria.Scopes.Add(new Uri("http://www.contoso.com/building1/floor1"));
findCriteria.Duration = TimeSpan.FromSeconds(10);

// Find ICalculatorService endpoints
FindResponse findResponse = discoveryClient.Find(findCriteria);

Console.WriteLine("Found {0} ICalculatorService endpoint(s).", findResponse.Endpoints.Count)
```

## <a name="see-also"></a><span data-ttu-id="8673a-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="8673a-146">See also</span></span>

- [<span data-ttu-id="8673a-147">WCF Discovery 概述</span><span class="sxs-lookup"><span data-stu-id="8673a-147">WCF Discovery Overview</span></span>](wcf-discovery-overview.md)
- [<span data-ttu-id="8673a-148">使用 Discovery 客户端通道</span><span class="sxs-lookup"><span data-stu-id="8673a-148">Using the Discovery Client Channel</span></span>](using-the-discovery-client-channel.md)
- [<span data-ttu-id="8673a-149">通过范围进行发现</span><span class="sxs-lookup"><span data-stu-id="8673a-149">Discovery with Scopes</span></span>](../samples/discovery-with-scopes-sample.md)
- [<span data-ttu-id="8673a-150">基本</span><span class="sxs-lookup"><span data-stu-id="8673a-150">Basic</span></span>](../samples/basic-sample.md)

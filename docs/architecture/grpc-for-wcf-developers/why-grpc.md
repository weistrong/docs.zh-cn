---
title: 为什么我们建议为 wcf 开发人员 gRPC-gRPC for WCF 开发人员
description: 讨论为什么 gRPC 非常适合要迁移到现代体系结构和平台的 WCF 开发人员。
ms.date: 12/15/2020
ms.openlocfilehash: 058f85297610116e96c8580fcefb10ee6dfcf935
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97937969"
---
# <a name="why-we-recommend-grpc-for-wcf-developers"></a><span data-ttu-id="24b7d-103">我们为什么建议适用于 WCF 开发人员的 gRPC</span><span class="sxs-lookup"><span data-stu-id="24b7d-103">Why we recommend gRPC for WCF developers</span></span>

<span data-ttu-id="24b7d-104">在深入探讨 gRPC 的语言和技术之前，有必要讨论为什么 gRPC 是要迁移到 .NET 的 Windows Communication Foundation (WCF) 开发人员的正确解决方案。</span><span class="sxs-lookup"><span data-stu-id="24b7d-104">Before we dive deeply into the language and techniques of gRPC, it's worth discussing why gRPC is the right solution for Windows Communication Foundation (WCF) developers who want to migrate to .NET.</span></span>

## <a name="similarity-to-wcf"></a><span data-ttu-id="24b7d-105">与 WCF 的相似性</span><span class="sxs-lookup"><span data-stu-id="24b7d-105">Similarity to WCF</span></span>

<span data-ttu-id="24b7d-106">尽管 gRPC 的实现和方法不同，但对于 WCF 开发人员来说，通过 gRPC 开发和使用服务的体验应该是直观的。</span><span class="sxs-lookup"><span data-stu-id="24b7d-106">Although the implementation and approach are different for gRPC, the experience of developing and consuming services with gRPC should be intuitive for WCF developers.</span></span> <span data-ttu-id="24b7d-107">基本目标是相同的：可以将客户端和服务器置于相同平台上，而无需担心网络。</span><span class="sxs-lookup"><span data-stu-id="24b7d-107">The underlying goal is the same: make it possible to code as though the client and server are on the same platform, without needing to worry about networking.</span></span>

<span data-ttu-id="24b7d-108">这两个平台共享声明并实现接口的原则，即使用于声明该接口的过程不同。</span><span class="sxs-lookup"><span data-stu-id="24b7d-108">Both platforms share the principle of declaring and then implementing an interface, even though the process for declaring that interface is different.</span></span> <span data-ttu-id="24b7d-109">正如你将在第5章中看到的那样，gRPC 支持映射到 WCF 服务可使用的绑定的不同类型的 RPC 调用。</span><span class="sxs-lookup"><span data-stu-id="24b7d-109">And as you'll see in chapter 5, the different types of RPC calls that gRPC supports map well to the bindings available to WCF services.</span></span>

## <a name="benefits-of-grpc"></a><span data-ttu-id="24b7d-110">gRPC 的优点</span><span class="sxs-lookup"><span data-stu-id="24b7d-110">Benefits of gRPC</span></span>

<span data-ttu-id="24b7d-111">由于以下原因，gRPC 会出现在其他解决方案之上。</span><span class="sxs-lookup"><span data-stu-id="24b7d-111">gRPC stands above other solutions for the following reasons.</span></span>

### <a name="performance"></a><span data-ttu-id="24b7d-112">性能</span><span class="sxs-lookup"><span data-stu-id="24b7d-112">Performance</span></span>

<span data-ttu-id="24b7d-113">使用 HTTP/2 而不是 HTTP/1.1 将不再要求用户可读的消息，而是使用更快、更快的二进制协议。</span><span class="sxs-lookup"><span data-stu-id="24b7d-113">Using HTTP/2 rather than HTTP/1.1 removes the requirement for human-readable messages and instead uses the smaller, faster binary protocol.</span></span> <span data-ttu-id="24b7d-114">这更有效率于计算机进行分析。</span><span class="sxs-lookup"><span data-stu-id="24b7d-114">This is more efficient for computers to parse.</span></span> <span data-ttu-id="24b7d-115">HTTP/2 还支持通过单个连接进行多路复用请求。</span><span class="sxs-lookup"><span data-stu-id="24b7d-115">HTTP/2 also supports multiplexing requests over a single connection.</span></span> <span data-ttu-id="24b7d-116">通过此支持，可以在无需在队列中等待即可立即发送响应。</span><span class="sxs-lookup"><span data-stu-id="24b7d-116">This support enables responses to be sent as soon as they're ready without the need to wait in a queue.</span></span> <span data-ttu-id="24b7d-117"> (在 HTTP/1.1 中，此问题称为 " (住) 阻止"。) 在使用 gRPC 时需要较少的资源，这使其成为适用于移动设备和速度较慢的网络的良好解决方案。</span><span class="sxs-lookup"><span data-stu-id="24b7d-117">(In HTTP/1.1, this issue is known as "head-of-line (HOL) blocking.") You need fewer resources when using gRPC, which makes it a good solution to use for mobile devices and over slower networks.</span></span>

### <a name="interoperability"></a><span data-ttu-id="24b7d-118">互操作性</span><span class="sxs-lookup"><span data-stu-id="24b7d-118">Interoperability</span></span>

<span data-ttu-id="24b7d-119">对于所有主要的编程语言和平台，都有 gRPC 工具和库，包括 .NET、Java、Python、Go、C++、Node.js、Swift、Dart、Ruby 以及 PHP。</span><span class="sxs-lookup"><span data-stu-id="24b7d-119">There are gRPC tools and libraries for all major programming languages and platforms, including .NET, Java, Python, Go, C++, Node.js, Swift, Dart, Ruby, and PHP.</span></span> <span data-ttu-id="24b7d-120">由于协议缓冲区的二进制网络格式和每个平台的有效代码生成，开发人员可以构建具有高性能的应用程序，同时仍享有完全的跨平台支持。</span><span class="sxs-lookup"><span data-stu-id="24b7d-120">Thanks to the Protocol Buffers binary wire format and the efficient code generation for each platform, developers can build performant apps while still enjoying full cross-platform support.</span></span>

### <a name="usability-and-productivity"></a><span data-ttu-id="24b7d-121">易用性和工作效率</span><span class="sxs-lookup"><span data-stu-id="24b7d-121">Usability and productivity</span></span>

<span data-ttu-id="24b7d-122">gRPC 是一个全面的 RPC 解决方案。</span><span class="sxs-lookup"><span data-stu-id="24b7d-122">gRPC is a comprehensive RPC solution.</span></span> <span data-ttu-id="24b7d-123">它可以跨多种语言和平台一致地工作。</span><span class="sxs-lookup"><span data-stu-id="24b7d-123">It works consistently across multiple languages and platforms.</span></span> <span data-ttu-id="24b7d-124">它还提供了极佳的工具，其中包含自动生成的很多必要样板代码。</span><span class="sxs-lookup"><span data-stu-id="24b7d-124">It also provides excellent tooling, with much of the necessary boilerplate code automatically generated.</span></span> <span data-ttu-id="24b7d-125">因此，更多的开发人员时间更多，可以专注于业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="24b7d-125">So more developer time is freed up to focus on business logic.</span></span>

### <a name="streaming"></a><span data-ttu-id="24b7d-126">流式处理</span><span class="sxs-lookup"><span data-stu-id="24b7d-126">Streaming</span></span>

<span data-ttu-id="24b7d-127">gRPC 具有完全双向流式处理，这为 WCF 的全双工服务提供了类似的功能。</span><span class="sxs-lookup"><span data-stu-id="24b7d-127">gRPC has full bidirectional streaming, which provides similar functionality to WCF's full-duplex services.</span></span> <span data-ttu-id="24b7d-128">gRPC 流式传输可以通过常规的 Internet 连接、负载均衡器和服务网格运行。</span><span class="sxs-lookup"><span data-stu-id="24b7d-128">gRPC streaming can operate over regular internet connections, load balancers, and service meshes.</span></span>

### <a name="deadlinetimeouts-and-cancellation"></a><span data-ttu-id="24b7d-129">截止时间/超时和取消</span><span class="sxs-lookup"><span data-stu-id="24b7d-129">Deadline/timeouts and cancellation</span></span>

<span data-ttu-id="24b7d-130">gRPC 允许客户端指定 RPC 完成的最长时间。</span><span class="sxs-lookup"><span data-stu-id="24b7d-130">gRPC allows clients to specify a maximum time for an RPC to finish.</span></span> <span data-ttu-id="24b7d-131">如果超过了指定的截止时间，服务器可以独立于客户端取消操作。</span><span class="sxs-lookup"><span data-stu-id="24b7d-131">If the specified deadline is exceeded, the server can cancel the operation independently of the client.</span></span> <span data-ttu-id="24b7d-132">截止时间和取消可通过进一步的 gRPC 调用进行传播，以帮助强制实施资源使用限制。</span><span class="sxs-lookup"><span data-stu-id="24b7d-132">Deadlines and cancellations can be propagated through further gRPC calls to help enforce resource usage limits.</span></span> <span data-ttu-id="24b7d-133">当超过截止时间时，客户端还可以停止操作，如有必要，还可以在需要时停止操作 (例如，因为用户交互) 。</span><span class="sxs-lookup"><span data-stu-id="24b7d-133">Clients can also stop operations when a deadline is exceeded, or earlier if necessary (for example, because of a user interaction).</span></span>

### <a name="security"></a><span data-ttu-id="24b7d-134">安全性</span><span class="sxs-lookup"><span data-stu-id="24b7d-134">Security</span></span>

<span data-ttu-id="24b7d-135">当 gRPC 在 TLS 端到端加密连接上使用 HTTP/2 时，它会隐式保护。</span><span class="sxs-lookup"><span data-stu-id="24b7d-135">gRPC is implicitly secure when it's using HTTP/2 over a TLS end-to-end encrypted connection.</span></span> <span data-ttu-id="24b7d-136"> (的客户端证书身份验证支持，请参阅 [第6章](security.md)) 进一步提高客户端和服务器之间的安全性和信任。</span><span class="sxs-lookup"><span data-stu-id="24b7d-136">Support for client certificate authentication (see [chapter 6](security.md)) further increases security and trust between client and server.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="24b7d-137">[上一页](network-protocols.md)
>[下一页](protocol-buffers.md)</span><span class="sxs-lookup"><span data-stu-id="24b7d-137">[Previous](network-protocols.md)
[Next](protocol-buffers.md)</span></span>

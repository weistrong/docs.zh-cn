---
title: 网络协议-适用于 WCF 开发人员的 gRPC
description: GRPC 网络协议的概述。
ms.date: 09/02/2019
ms.openlocfilehash: 801d57c95aec748e5dcf667ca480775ff945b55c
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938554"
---
# <a name="network-protocols"></a><span data-ttu-id="6e65b-103">网络协议</span><span class="sxs-lookup"><span data-stu-id="6e65b-103">Network protocols</span></span>

<span data-ttu-id="6e65b-104">与 Windows Communication Foundation (WCF) 不同，gRPC 使用 HTTP/2 作为其网络的基础。</span><span class="sxs-lookup"><span data-stu-id="6e65b-104">Unlike Windows Communication Foundation (WCF), gRPC uses HTTP/2 as a base for its networking.</span></span> <span data-ttu-id="6e65b-105">与 WCF 和 SOAP 相比，此协议具有明显的优势，只能在 HTTP/1.1 上操作。</span><span class="sxs-lookup"><span data-stu-id="6e65b-105">This protocol offers significant advantages over WCF and SOAP, which operate only on HTTP/1.1.</span></span> <span data-ttu-id="6e65b-106">对于想要使用 gRPC 的开发人员，如果没有 HTTP/2 的替代方法，则似乎更详细地探讨 HTTP/2，并识别使用 gRPC 的其他优点。</span><span class="sxs-lookup"><span data-stu-id="6e65b-106">For developers wanting to use gRPC, given that there's no alternative to HTTP/2, it would seem to be the ideal moment to explore HTTP/2 in more detail and identify additional benefits of using gRPC.</span></span>

<span data-ttu-id="6e65b-107">HTTP/2 （由2015中的 Internet 工程任务组发布）派生自 Google 已在使用的实验 SPDY 协议。</span><span class="sxs-lookup"><span data-stu-id="6e65b-107">HTTP/2, released by Internet Engineering Task Force in 2015, was derived from the experimental SPDY protocol, which was already being used by Google.</span></span> <span data-ttu-id="6e65b-108">它经过专门设计，比 HTTP/1.1 更高效、更快、更安全。</span><span class="sxs-lookup"><span data-stu-id="6e65b-108">It was specifically designed to be more efficient, faster, and more secure than HTTP/1.1.</span></span>

## <a name="key-features-of-http2"></a><span data-ttu-id="6e65b-109">HTTP/2 的主要功能</span><span class="sxs-lookup"><span data-stu-id="6e65b-109">Key features of HTTP/2</span></span>

<span data-ttu-id="6e65b-110">此列表显示了 HTTP/2 的一些主要功能和优势：</span><span class="sxs-lookup"><span data-stu-id="6e65b-110">This list shows some of the key features and advantages of HTTP/2:</span></span>

### <a name="binary-protocol"></a><span data-ttu-id="6e65b-111">二进制协议</span><span class="sxs-lookup"><span data-stu-id="6e65b-111">Binary protocol</span></span>

<span data-ttu-id="6e65b-112">请求/响应周期不再需要文本命令。</span><span class="sxs-lookup"><span data-stu-id="6e65b-112">Request/response cycles no longer need text commands.</span></span> <span data-ttu-id="6e65b-113">此活动简化并加速了命令的实现。</span><span class="sxs-lookup"><span data-stu-id="6e65b-113">This activity simplifies and speeds up the implementation of commands.</span></span> <span data-ttu-id="6e65b-114">具体而言，分析数据的速度更快，使用的内存更少，网络延迟会因速度的明显相关改进而降低，同时还能提供更好的网络资源。</span><span class="sxs-lookup"><span data-stu-id="6e65b-114">Specifically, parsing data is faster and uses less memory, network latency is reduced with obvious related improvements to speed, and there's an overall better use of network resources.</span></span>

### <a name="streams"></a><span data-ttu-id="6e65b-115">流</span><span class="sxs-lookup"><span data-stu-id="6e65b-115">Streams</span></span>

<span data-ttu-id="6e65b-116">流允许你在发送方和接收方之间创建长时间连接，可以通过这些连接以异步方式发送多个消息或帧。</span><span class="sxs-lookup"><span data-stu-id="6e65b-116">Streams allow you to create long-lived connections between sender and receiver, over which multiple messages or frames can be sent asynchronously.</span></span> <span data-ttu-id="6e65b-117">多个流可以独立于单个 HTTP/2 连接进行操作。</span><span class="sxs-lookup"><span data-stu-id="6e65b-117">Multiple streams can operate independently over a single HTTP/2 connection.</span></span>

### <a name="request-multiplexing-over-a-single-tcp-connection"></a><span data-ttu-id="6e65b-118">通过单个 TCP 连接请求多路复用</span><span class="sxs-lookup"><span data-stu-id="6e65b-118">Request multiplexing over a single TCP connection</span></span>

<span data-ttu-id="6e65b-119">此功能是 HTTP/2 最重要的一项创新。</span><span class="sxs-lookup"><span data-stu-id="6e65b-119">This feature is one of the most important innovations of HTTP/2.</span></span> <span data-ttu-id="6e65b-120">因为它允许对数据进行多次并行请求，所以现在可以从一台服务器同时下载 web 文件。</span><span class="sxs-lookup"><span data-stu-id="6e65b-120">Because it allows multiple parallel requests for data, it's now possible to download web files concurrently from a single server.</span></span> <span data-ttu-id="6e65b-121">网站加载速度更快，并减少了优化需求。</span><span class="sxs-lookup"><span data-stu-id="6e65b-121">Websites load faster, and the need for optimization is reduced.</span></span> <span data-ttu-id="6e65b-122">线路外 (住) 阻止的情况下，如果已准备就绪的响应，则必须等待发送 (，直至之前的请求完成为止，即使在 TCP 传输级别) ，仍可进行阻止。</span><span class="sxs-lookup"><span data-stu-id="6e65b-122">Head-of-line (HOL) blocking, where responses that are ready must wait to be sent until an earlier request is completed, is also mitigated (although HOL blocking can still occur at the TCP-transport level).</span></span>

### <a name="nettcp-like-performance-cross-platform"></a><span data-ttu-id="6e65b-123">Net.tcp 类似的性能，跨平台</span><span class="sxs-lookup"><span data-stu-id="6e65b-123">Net.TCP-like performance, cross-platform</span></span>

<span data-ttu-id="6e65b-124">从根本上讲，gRPC 和 HTTP/2 的组合为开发人员提供了与 WCF 的 Net.tcp 绑定相同的速度和效率，在某些情况下，其速度更快，效率更高。</span><span class="sxs-lookup"><span data-stu-id="6e65b-124">Fundamentally, the combination of gRPC and HTTP/2 offers developers at least the equivalent speed and efficiency of Net.TCP bindings for WCF, and in some cases even greater speed and efficiency.</span></span> <span data-ttu-id="6e65b-125">但与 Net.tcp 不同，HTTP/2 上的 gRPC 不会被限制为 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="6e65b-125">But, unlike Net.TCP, gRPC over HTTP/2 isn't constrained to .NET applications.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="6e65b-126">[上一页](interface-definition-language.md)
>[下一页](why-grpc.md)</span><span class="sxs-lookup"><span data-stu-id="6e65b-126">[Previous](interface-definition-language.md)
[Next](why-grpc.md)</span></span>

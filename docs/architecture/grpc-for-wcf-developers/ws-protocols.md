---
title: WS-* 协议-适用于 WCF 开发人员的 gRPC
description: 查看 WCF 支持的 WS-* 协议和 gRPC 提供的替代项
author: markrendle
ms.date: 12/15/2020
ms.openlocfilehash: d6fffdd5153c799c78ad949a3b16fa72e9612e43
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938476"
---
# <a name="ws--protocols"></a><span data-ttu-id="9424d-103">WS \* 协议</span><span class="sxs-lookup"><span data-stu-id="9424d-103">WS-\* protocols</span></span>

<span data-ttu-id="9424d-104">使用 Windows Communication Foundation (WCF) 的一个真正的好处是它支持许多现有的 _WS \*_ 标准协议。</span><span class="sxs-lookup"><span data-stu-id="9424d-104">One of the real benefits of working with Windows Communication Foundation (WCF) was that it supported many of the existing _WS-\*_ standard protocols.</span></span> <span data-ttu-id="9424d-105">本部分将简要介绍 gRPC 如何管理相同的 WS \* 协议，并讨论在没有替代方法时可用的选项。</span><span class="sxs-lookup"><span data-stu-id="9424d-105">This section will briefly cover how gRPC manages the same WS-\* protocols and discuss what options are available when there's no alternative.</span></span>

## <a name="metadata-exchange-ws-policy-ws-discovery-and-so-on"></a><span data-ttu-id="9424d-106">元数据交换： WS 策略、WS 发现等</span><span class="sxs-lookup"><span data-stu-id="9424d-106">Metadata exchange: WS-Policy, WS-Discovery, and so on</span></span>

<span data-ttu-id="9424d-107">SOAP 服务 (WSDL) 架构文档公开了 Web 服务描述语言，并提供了数据格式、操作或通信选项等信息。</span><span class="sxs-lookup"><span data-stu-id="9424d-107">SOAP services expose Web Services Description Language (WSDL) schema documents with information such as data formats, operations, or communication options.</span></span> <span data-ttu-id="9424d-108">您可以使用此架构来生成客户端代码。</span><span class="sxs-lookup"><span data-stu-id="9424d-108">You can use this schema to generate the client code.</span></span>

<span data-ttu-id="9424d-109">如果从相同文件生成服务器和客户端，则 gRPC 的效果最好 `.proto` ，但服务器反射可选扩展提供了一种方式，用于从正在运行的服务器中公开动态信息。</span><span class="sxs-lookup"><span data-stu-id="9424d-109">gRPC works best when servers and clients are generated from the same `.proto` files, but a Server Reflection optional extension does provide a way to expose dynamic information from a running server.</span></span> <span data-ttu-id="9424d-110">有关详细信息，请参阅 [Grpc](https://nuget.org/packages/Grpc.Reflection) NuGet 包和 [Grpc c # 服务器反射](https://github.com/grpc/grpc/blob/master/doc/csharp/server_reflection.md) 一文。</span><span class="sxs-lookup"><span data-stu-id="9424d-110">For more information, see the [Grpc.Reflection](https://nuget.org/packages/Grpc.Reflection) NuGet package and the [gRPC C# Server Reflection](https://github.com/grpc/grpc/blob/master/doc/csharp/server_reflection.md) article.</span></span>

<span data-ttu-id="9424d-111">WS-Discovery 协议用于在本地网络上查找服务。</span><span class="sxs-lookup"><span data-stu-id="9424d-111">The WS-Discovery protocol is used to locate services on a local network.</span></span> <span data-ttu-id="9424d-112">gRPC services 通过 DNS 或服务注册表（如 Consul 或 ZooKeeper）进行查找。</span><span class="sxs-lookup"><span data-stu-id="9424d-112">gRPC services are located through DNS or a service registry such as Consul or ZooKeeper.</span></span>

## <a name="security-ws-security-ws-federation-xml-encryption-and-so-on"></a><span data-ttu-id="9424d-113">安全性： WS 安全性、WS 联合身份验证、XML 加密等</span><span class="sxs-lookup"><span data-stu-id="9424d-113">Security: WS-Security, WS-Federation, XML Encryption, and so on</span></span>

<span data-ttu-id="9424d-114">[第6章](security.md)中更详细地介绍了安全性、身份验证和授权。</span><span class="sxs-lookup"><span data-stu-id="9424d-114">Security, authentication, and authorization are covered in much more detail in [chapter 6](security.md).</span></span> <span data-ttu-id="9424d-115">但在此，值得注意的是，与 WCF 不同，gRPC 不支持 WS 安全性、WS 联合身份验证或 XML 加密。</span><span class="sxs-lookup"><span data-stu-id="9424d-115">But it's worth noting here that, unlike WCF, gRPC doesn't support WS-Security, WS-Federation, or XML Encryption.</span></span> <span data-ttu-id="9424d-116">尽管如此，gRPC 也能提供卓越的安全性。</span><span class="sxs-lookup"><span data-stu-id="9424d-116">Even so, gRPC provides excellent security.</span></span> <span data-ttu-id="9424d-117">所有 gRPC 网络流量在使用 HTTP/2 over TLS 时自动进行加密。</span><span class="sxs-lookup"><span data-stu-id="9424d-117">All gRPC network traffic is automatically encrypted when it's using HTTP/2 over TLS.</span></span> <span data-ttu-id="9424d-118">您可以使用 X509 证书进行相互的客户端/服务器身份验证。</span><span class="sxs-lookup"><span data-stu-id="9424d-118">You can use X509 certificates for mutual client/server authentication.</span></span>

## <a name="ws-reliablemessaging"></a><span data-ttu-id="9424d-119">WS-ReliableMessaging</span><span class="sxs-lookup"><span data-stu-id="9424d-119">WS-ReliableMessaging</span></span>

<span data-ttu-id="9424d-120">gRPC 未提供与 WS-RELIABLEMESSAGING 等效的。</span><span class="sxs-lookup"><span data-stu-id="9424d-120">gRPC does not provide an equivalent to WS-ReliableMessaging.</span></span> <span data-ttu-id="9424d-121">应该在代码中处理重试语义，如 [Polly](https://github.com/App-vNext/Polly)。</span><span class="sxs-lookup"><span data-stu-id="9424d-121">Retry semantics should be handled in code, possibly with a library like [Polly](https://github.com/App-vNext/Polly).</span></span> <span data-ttu-id="9424d-122">当你在 Kubernetes 或类似的业务流程环境中运行时， [服务网格](service-mesh.md) 还有助于在服务之间提供可靠的消息传送。</span><span class="sxs-lookup"><span data-stu-id="9424d-122">When you're running in Kubernetes or similar orchestration environments, [service meshes](service-mesh.md) can also help to provide reliable messaging between services.</span></span>

## <a name="ws-transaction-ws-coordination"></a><span data-ttu-id="9424d-123">WS 事务，WS-Coordination</span><span class="sxs-lookup"><span data-stu-id="9424d-123">WS-Transaction, WS-Coordination</span></span>

<span data-ttu-id="9424d-124">WCF 对分布式事务的实现使用 Microsoft 分布式事务处理协调器 (MSDTC) 。</span><span class="sxs-lookup"><span data-stu-id="9424d-124">WCF's implementation of distributed transactions uses Microsoft Distributed Transaction Coordinator (MSDTC).</span></span> <span data-ttu-id="9424d-125">它适用于专门支持的资源管理器，例如 SQL Server、MSMQ 或 Windows 文件系统。</span><span class="sxs-lookup"><span data-stu-id="9424d-125">It works with resource managers that specifically support it, like SQL Server, MSMQ, or Windows file systems.</span></span> <span data-ttu-id="9424d-126">由于使用的技术范围更广，因此在现代微服务世界上没有任何等效项。</span><span class="sxs-lookup"><span data-stu-id="9424d-126">There's no equivalent yet in the modern microservices world, in part due to the wider range of technologies in use.</span></span> <span data-ttu-id="9424d-127">有关事务的讨论，请参阅 [附录 a](appendix.md)。</span><span class="sxs-lookup"><span data-stu-id="9424d-127">For a discussion of transactions, see [Appendix A](appendix.md).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="9424d-128">[上一页](error-handling.md)
>[下一页](migrate-wcf-to-grpc.md)</span><span class="sxs-lookup"><span data-stu-id="9424d-128">[Previous](error-handling.md)
[Next](migrate-wcf-to-grpc.md)</span></span>

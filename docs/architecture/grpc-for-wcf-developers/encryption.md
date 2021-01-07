---
title: 加密和网络安全-gRPC for WCF 开发人员
description: 有关 gRPC 中的网络安全和加密的一些注意事项
ms.date: 01/06/2021
ms.openlocfilehash: cf4d30ff862e64aadfeacf45ed3768fc14737800
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970136"
---
# <a name="encryption-and-network-security"></a><span data-ttu-id="62d2b-103">加密和网络安全</span><span class="sxs-lookup"><span data-stu-id="62d2b-103">Encryption and network security</span></span>

<span data-ttu-id="62d2b-104">Windows Communication Foundation 的网络安全模型 (WCF) 非常复杂。</span><span class="sxs-lookup"><span data-stu-id="62d2b-104">The network security model for Windows Communication Foundation (WCF) is extensive and complex.</span></span> <span data-ttu-id="62d2b-105">它包括使用 HTTPS 或经由 TCP 的传输级安全性和通过使用 WS-Security 规范对单个消息进行加密的消息级安全性。</span><span class="sxs-lookup"><span data-stu-id="62d2b-105">It includes transport-level security by using HTTPS or TLS-over-TCP, and message-level security by using the WS-Security specification to encrypt individual messages.</span></span>

<span data-ttu-id="62d2b-106">gRPC 会将安全网络留给基础 HTTP/2 协议，你可以使用 TLS 证书来保护这一点。</span><span class="sxs-lookup"><span data-stu-id="62d2b-106">gRPC leaves secure networking to the underlying HTTP/2 protocol, which you can secure by using TLS certificates.</span></span>

<span data-ttu-id="62d2b-107">Web 浏览器坚持使用 HTTP/2 的 TLS 连接，但大多数编程客户端（包括）都是如此。网络 `HttpClient` ，可以通过未加密的连接使用 HTTP/2。</span><span class="sxs-lookup"><span data-stu-id="62d2b-107">Web browsers insist on using TLS connections for HTTP/2, but most programmatic clients, including .NET's `HttpClient`, can use HTTP/2 over unencrypted connections.</span></span>

<span data-ttu-id="62d2b-108">对于公共 Api，应始终使用 TLS 连接，并从适当的 SSL 机构为你的服务提供有效的证书。</span><span class="sxs-lookup"><span data-stu-id="62d2b-108">For public APIs, you should always use TLS connections, and provide valid certificates for your services from a proper SSL authority.</span></span> <span data-ttu-id="62d2b-109">[LetsEncrypt](https://letsencrypt.org) 提供免费的自动 SSL 证书，并且目前大多数托管基础结构都支持具有通用插件或扩展的 LetsEncrypt 标准。</span><span class="sxs-lookup"><span data-stu-id="62d2b-109">[LetsEncrypt](https://letsencrypt.org) provides free, automated SSL certificates, and most hosting infrastructure today supports the LetsEncrypt standard with common plug-ins or extensions.</span></span>

<span data-ttu-id="62d2b-110">对于跨企业网络的内部服务，还应考虑使用 TLS 来保护进出 gRPC services 的网络流量。</span><span class="sxs-lookup"><span data-stu-id="62d2b-110">For internal services across a corporate network, you should still consider using TLS to secure network traffic to and from your gRPC services.</span></span>

<span data-ttu-id="62d2b-111">如果需要在 Kubernetes 中运行的服务之间使用显式 TLS，请考虑使用群集内证书颁发机构和证书管理器控制器（如 [cert 管理器](https://docs.cert-manager.io/en/latest/)）。</span><span class="sxs-lookup"><span data-stu-id="62d2b-111">If you need to use explicit TLS between services running in Kubernetes, consider using an in-cluster certificate authority and a certificate manager controller like [cert-manager](https://docs.cert-manager.io/en/latest/).</span></span> <span data-ttu-id="62d2b-112">然后，你可以在部署时自动将证书分配给服务。</span><span class="sxs-lookup"><span data-stu-id="62d2b-112">You can then automatically assign certificates to services at deployment time.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="62d2b-113">[上一页](channel-credentials.md)
>[下一页](grpc-in-production.md)</span><span class="sxs-lookup"><span data-stu-id="62d2b-113">[Previous](channel-credentials.md)
[Next](grpc-in-production.md)</span></span>

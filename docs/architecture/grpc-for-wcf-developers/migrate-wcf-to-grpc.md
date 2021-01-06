---
title: 将 WCF 解决方案迁移到 WCF 开发人员的 gRPC-gRPC
description: 如何将不同类型的 WCF 服务迁移到 gRPC 中的等效类型。
ms.date: 12/15/2020
ms.openlocfilehash: 3bd35cb6119368ff3db3be9ab5fabf89f2652b29
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97937956"
---
# <a name="migrate-a-wcf-solution-to-grpc"></a><span data-ttu-id="76eda-103">将 WCF 解决方案迁移到 gRPC</span><span class="sxs-lookup"><span data-stu-id="76eda-103">Migrate a WCF solution to gRPC</span></span>

<span data-ttu-id="76eda-104">本章介绍如何使用 ASP.NET Core 5.0 gRPC 项目，并演示如何将不同类型的 Windows Communication Foundation (WCF) 服务迁移到 gRPC 等效项：</span><span class="sxs-lookup"><span data-stu-id="76eda-104">This chapter will describe how to work with ASP.NET Core 5.0 gRPC projects and demonstrate migrating different types of Windows Communication Foundation (WCF) services to the gRPC equivalent:</span></span>

- <span data-ttu-id="76eda-105">创建 ASP.NET Core 5.0 gRPC 项目。</span><span class="sxs-lookup"><span data-stu-id="76eda-105">Create an ASP.NET Core 5.0 gRPC project.</span></span>
- <span data-ttu-id="76eda-106">简单的请求-答复操作到 gRPC 一元 RPC。</span><span class="sxs-lookup"><span data-stu-id="76eda-106">Simple request-reply operations to gRPC unary RPC.</span></span>
- <span data-ttu-id="76eda-107">用于 gRPC 客户端流式处理 RPC 的单向操作。</span><span class="sxs-lookup"><span data-stu-id="76eda-107">One-way operations to gRPC client streaming RPC.</span></span>
- <span data-ttu-id="76eda-108">全双工服务，gRPC 双向流式处理 RPC。</span><span class="sxs-lookup"><span data-stu-id="76eda-108">Full-duplex services to gRPC bidirectional streaming RPC.</span></span>

<span data-ttu-id="76eda-109">还比较了如何使用流式处理服务与重复字段来返回数据集，并在本章末尾讨论了如何使用客户端库。</span><span class="sxs-lookup"><span data-stu-id="76eda-109">There's also a comparison of using streaming services versus repeated fields for returning datasets, and there's a discussion of the use of client libraries at the end of the chapter.</span></span>

<span data-ttu-id="76eda-110">示例 WCF 应用程序是一组股票交易服务的最小存根。</span><span class="sxs-lookup"><span data-stu-id="76eda-110">The sample WCF application is a minimal stub of a set of stock trading services.</span></span> <span data-ttu-id="76eda-111">它使用 (IoC) 名为 Autofac 的容器库进行依赖关系注入的开源反转控制。</span><span class="sxs-lookup"><span data-stu-id="76eda-111">It uses the open-source Inversion of Control (IoC) container library called Autofac for dependency injection.</span></span> <span data-ttu-id="76eda-112">它包括三个服务，每个服务类型一个。</span><span class="sxs-lookup"><span data-stu-id="76eda-112">It includes three services, one for each WCF service type.</span></span> <span data-ttu-id="76eda-113">以下部分将更详细地讨论服务。</span><span class="sxs-lookup"><span data-stu-id="76eda-113">The services will be discussed in more detail in the following sections.</span></span> <span data-ttu-id="76eda-114">可以从 GitHub 上的 [dotnet/grpc-for wcf 开发人员](https://github.com/dotnet-architecture/grpc-for-wcf-developers) 下载解决方案。</span><span class="sxs-lookup"><span data-stu-id="76eda-114">You can download the solutions from [dotnet-architecture/grpc-for-wcf-developers](https://github.com/dotnet-architecture/grpc-for-wcf-developers) on GitHub.</span></span> <span data-ttu-id="76eda-115">服务使用虚设数据来最大程度地减少外部依赖项。</span><span class="sxs-lookup"><span data-stu-id="76eda-115">The services use fake data to minimize external dependencies.</span></span>

<span data-ttu-id="76eda-116">这些示例包括每个服务的 WCF 和 gRPC 实现。</span><span class="sxs-lookup"><span data-stu-id="76eda-116">The samples include the WCF and gRPC implementations of each service.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="76eda-117">[上一页](ws-protocols.md)
>[下一页](create-project.md)</span><span class="sxs-lookup"><span data-stu-id="76eda-117">[Previous](ws-protocols.md)
[Next](create-project.md)</span></span>

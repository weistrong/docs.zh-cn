---
title: Azure 和 .NET 入门
description: 学习了解 Azure 和 .NET 所需的基础知识。
ms.date: 06/20/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: b5766012b77da88ae9a696939b6e498ebc421522
ms.sourcegitcommit: 5d9cee27d9ffe8f5670e5f663434511e81b8ac38
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "98025037"
---
# <a name="introduction-to-azure-and-net"></a><span data-ttu-id="c0f63-103">Azure 和 .NET 简介</span><span class="sxs-lookup"><span data-stu-id="c0f63-103">Introduction to Azure and .NET</span></span>

## <a name="what-is-azure"></a><span data-ttu-id="c0f63-104">什么是 Azure？</span><span class="sxs-lookup"><span data-stu-id="c0f63-104">What is Azure?</span></span>

<span data-ttu-id="c0f63-105">Azure 是一个云平台，旨在简化构建新式应用程序的过程。</span><span class="sxs-lookup"><span data-stu-id="c0f63-105">Azure is a cloud platform designed to simplify the process of building modern applications.</span></span>  <span data-ttu-id="c0f63-106">无论是选择完全在 Azure 中托管应用程序，还是使用 Azure 服务扩展本地应用程序，Azure 都可以帮助你创建可缩放且可维护的可靠应用程序。</span><span class="sxs-lookup"><span data-stu-id="c0f63-106">Whether you choose to host your applications entirely in Azure or extend your on-premises applications with Azure services, Azure helps you create applications that are scalable, reliable, and maintainable.</span></span>  <span data-ttu-id="c0f63-107">凭借你已在使用的工具（如 Visual Studio 和 Visual Studio Code）和综合性 SDK 库中的广泛支持，Azure 旨在使 .NET 开发人员从一开始就高效工作。</span><span class="sxs-lookup"><span data-stu-id="c0f63-107">With extensive support in tools you already use like Visual Studio and Visual Studio Code and a comprehensive SDK library, Azure is designed to make you, the .NET developer productive right from the start.</span></span>

## <a name="application-development-scenarios-on-azure"></a><span data-ttu-id="c0f63-108">Azure 上的应用程序开发方案</span><span class="sxs-lookup"><span data-stu-id="c0f63-108">Application development scenarios on Azure</span></span>

<span data-ttu-id="c0f63-109">可以根据需要以不同方式将 Azure 集成到应用程序中。</span><span class="sxs-lookup"><span data-stu-id="c0f63-109">You can incorporate Azure into your application in different ways depending on your needs.</span></span>

- <span data-ttu-id="c0f63-110">**在 Azure 上托管的应用程序 -** Azure 可以托管整个应用程序堆栈（从 Web 应用程序和 API 到数据库，再到存储服务）。</span><span class="sxs-lookup"><span data-stu-id="c0f63-110">**Application hosting on Azure -** Azure can host your entire application stack from web applications and APIs to databases to storage services.</span></span> <span data-ttu-id="c0f63-111">Azure 支持各种托管模型（从完全托管的服务到容器，再到虚拟机）。</span><span class="sxs-lookup"><span data-stu-id="c0f63-111">Azure supports a variety of hosting models from fully managed services to containers to virtual machines.</span></span> <span data-ttu-id="c0f63-112">使用完全托管的 Azure 服务时，应用程序可以利用 Azure 内置的可伸缩性、高可用性和安全性。</span><span class="sxs-lookup"><span data-stu-id="c0f63-112">When using fully managed Azure services, your applications can take advantage of the scalability, high-availability, and security built in to Azure.</span></span>

- <span data-ttu-id="c0f63-113">**在应用程序中使用云服务 -** 现有应用可以纳入 Azure 服务以扩展其功能。</span><span class="sxs-lookup"><span data-stu-id="c0f63-113">**Consuming cloud services from applications -** Existing apps can incorporate Azure services to extend their capabilities.</span></span>  <span data-ttu-id="c0f63-114">这可能包括通过 [Azure 认知搜索](/azure/search/search-what-is-azure-search)添加全文搜索功能、将应用程序机密安全存储在 [Azure Key Vault](/azure/key-vault/) 中或通过 [Azure 认知服务](/azure/cognitive-services/)添加视觉、语音和语言理解功能。</span><span class="sxs-lookup"><span data-stu-id="c0f63-114">This could include adding full-text searching capability with [Azure Cognitive Search](/azure/search/search-what-is-azure-search), securely storing application secrets in [Azure Key Vault](/azure/key-vault/) or adding vision, speech and language understanding capabilities with [Azure Cognitive Services](/azure/cognitive-services/).</span></span>  <span data-ttu-id="c0f63-115">这些服务由 Azure 完全托管，可轻松添加到应用程序中，而无需更改当前的应用程序体系结构或部署模型。</span><span class="sxs-lookup"><span data-stu-id="c0f63-115">These services are fully managed by Azure and can be easily added to your application without changing your current application architecture or deployment model.</span></span>

- <span data-ttu-id="c0f63-116">**新式无服务器体系结构 -** Azure Functions 对构建用于处理事件驱动的工作流的解决方案进行了简化，无论是响应 HTTP 请求、处理 Blob 存储中的文件上传，还是处理队列中的事件，都有涉及。</span><span class="sxs-lookup"><span data-stu-id="c0f63-116">**Modern serverless architectures -** Azure Functions simplify building solutions to handle event-driven workflows, whether responding to HTTP requests, handling file uploads in Blob storage, or processing events in a queue.</span></span>  <span data-ttu-id="c0f63-117">只需编写处理事件所需的代码，而不必担心服务器或框架代码。</span><span class="sxs-lookup"><span data-stu-id="c0f63-117">You write only the code necessary to handle your event without worrying about servers or framework code.</span></span>  <span data-ttu-id="c0f63-118">此外，可以利用 250 多个连接器连接到其他 Azure 和第三方服务，以解决最棘手的集成问题。</span><span class="sxs-lookup"><span data-stu-id="c0f63-118">Further, you can take advantage of over 250 connectors to other Azure and third-party services to tackle your toughest integration problems.</span></span>

## <a name="access-azure-services-from-net-applications"></a><span data-ttu-id="c0f63-119">从 .NET 应用程序访问 Azure 服务</span><span class="sxs-lookup"><span data-stu-id="c0f63-119">Access Azure services from .NET applications</span></span>

<span data-ttu-id="c0f63-120">无论应用托管在 Azure 还是本地，均可通过用于 .NET 的 Azure SDK 提供对大多数 Azure 服务的访问权限。</span><span class="sxs-lookup"><span data-stu-id="c0f63-120">Whether your app is hosted in Azure or on-premises, access to most Azure services is provided through the **Azure SDK for .NET**.</span></span>  <span data-ttu-id="c0f63-121">用于 .NET 的 Azure SDK 以一系列 NuGet 包的形式提供，可以在 .NET Core（2.1 及更高版本）和 .NET Framework（4.6.1 及更高版本）应用程序中使用。</span><span class="sxs-lookup"><span data-stu-id="c0f63-121">The Azure SDK for .NET is provided as a series of NuGet packages and can be used in both .NET Core (2.1 and higher) and .NET Framework (4.6.1 and higher) applications.</span></span> <span data-ttu-id="c0f63-122">用于 .NET 的 Azure SDK 使将 Azure 服务整合到应用程序中变得就像安装正确的 NuGet 包、实例化客户端对象和调用适当方法那样轻松。</span><span class="sxs-lookup"><span data-stu-id="c0f63-122">The Azure SDK for .NET makes incorporating Azure services into your application as easy as installing the correct NuGet package, instantiating a client object and calling the appropriate methods.</span></span> <span data-ttu-id="c0f63-123">可以在[用于 .NET 的 Azure SDK 概述](./sdk/azure-sdk-for-dotnet.md)中找到有关用于 .NET 的 Azure SDK 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c0f63-123">More information on the Azure SDK for .NET can be found in the [Azure SDK for .NET Overview](./sdk/azure-sdk-for-dotnet.md).</span></span>

![显示 .NET 应用程序如何使用 Azure SDK 访问 Azure 服务的示意图](./media/azure-sdk-for-dotnet-overview.png)

## <a name="next-steps"></a><span data-ttu-id="c0f63-125">后续步骤</span><span class="sxs-lookup"><span data-stu-id="c0f63-125">Next steps</span></span>

<span data-ttu-id="c0f63-126">接下来，了解用于 .NET 开发的[最常用的 Azure 服务](./key-azure-services.md)。</span><span class="sxs-lookup"><span data-stu-id="c0f63-126">Next, learn about the most [commonly used Azure services](./key-azure-services.md) for .NET development.</span></span>

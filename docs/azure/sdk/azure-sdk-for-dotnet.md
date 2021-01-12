---
title: 用于 .NET 的 Azure SDK 概述
description: 概述什么是用于 .NET 的 Azure SDK 以及在 .NET 应用程序中使用 SDK 的基本步骤
ms.date: 11/30/2020
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 3ec1ee9e8da3a6e03581ce2a29a655ec0d68fe54
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700888"
---
# <a name="azure-sdk-for-net-overview"></a><span data-ttu-id="ecea3-103">用于 .NET 的 Azure SDK 概述</span><span class="sxs-lookup"><span data-stu-id="ecea3-103">Azure SDK for .NET overview</span></span>

## <a name="what-is-the-azure-sdk-for-net"></a><span data-ttu-id="ecea3-104">什么是用于 .NET 的 Azure SDK</span><span class="sxs-lookup"><span data-stu-id="ecea3-104">What is the Azure SDK for .NET</span></span>

<span data-ttu-id="ecea3-105">用于 .NET 的 Azure SDK 旨在让用户能够轻松从 .NET 应用程序使用 Azure 服务。</span><span class="sxs-lookup"><span data-stu-id="ecea3-105">The **Azure SDK for .NET** is designed to make it easy to use Azure services from your .NET applications.</span></span>  <span data-ttu-id="ecea3-106">无论是向 Blob 存储上传和下载文件、从 Azure Key Vault 检索应用程序机密，还是从 Azure 事件中心处理通知，用于 .NET 的 Azure SDK 都会提供一个一致且熟悉的界面来访问 Azure 服务。</span><span class="sxs-lookup"><span data-stu-id="ecea3-106">Whether it is uploading and downloading files to Blob Storage, retrieving application secrets from Azure Key Vault, or processing notifications from Azure Event Hubs, the Azure SDK for .NET provides a consistent and familiar interface to access Azure services.</span></span>  

<span data-ttu-id="ecea3-107">用于 .NET 的 Azure SDK 以一系列 NuGet 包的形式提供，可以在 .NET Core（2.1 及更高版本）和 .NET Framework（4.6.1 及更高版本）应用程序中使用。</span><span class="sxs-lookup"><span data-stu-id="ecea3-107">The Azure SDK for .NET is available as series of NuGet packages that can be used in both .NET Core (2.1 and higher) and .NET Framework (4.6.1 and higher) applications.</span></span>

![显示 .NET 应用程序如何使用 Azure SDK 访问 Azure 服务的示意图](./media/azure-sdk-for-dotnet-overview.png)

## <a name="use-the-azure-sdk-for-net-in-your-applications"></a><span data-ttu-id="ecea3-109">在应用程序中使用用于 .NET 的 Azure SDK</span><span class="sxs-lookup"><span data-stu-id="ecea3-109">Use the Azure SDK for .NET in your applications</span></span>

<span data-ttu-id="ecea3-110">若要在某一款 .NET 应用程序中使用 Azure SDK 包，则需要按照以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="ecea3-110">To use an Azure SDK package in one of your .NET applications, you want to follow these steps.</span></span>

1. <span data-ttu-id="ecea3-111">**找到相应的 SDK 包 -** 使用[包列表](../packages.md)查找适合你正在使用的 Azure 服务的包。</span><span class="sxs-lookup"><span data-stu-id="ecea3-111">**Locate the appropriate SDK package -** Use the [package list](../packages.md) to find the appropriate package for the Azure service you are working with.</span></span>  <span data-ttu-id="ecea3-112">请注意，大多数服务都具有用于处理服务的客户端包和用于创建和管理服务实例的管理包。</span><span class="sxs-lookup"><span data-stu-id="ecea3-112">Be advised that most services have a client package for working with the service and a management package for creating and managing instances of the service.</span></span>  <span data-ttu-id="ecea3-113">大多数情况下，你将需要客户端包。</span><span class="sxs-lookup"><span data-stu-id="ecea3-113">In most cases, you will want the client package.</span></span>  <span data-ttu-id="ecea3-114">使用 NuGet 在应用程序中安装此包。</span><span class="sxs-lookup"><span data-stu-id="ecea3-114">Install this package in your application using NuGet.</span></span>

2. <span data-ttu-id="ecea3-115">**为应用程序设置身份验证 -** 若要访问 Azure 资源，应用程序将需要具有在 Azure 中分配的适当凭据和访问权限。</span><span class="sxs-lookup"><span data-stu-id="ecea3-115">**Set up authentication for your application -** To access Azure resources, your application will need to have the appropriate credentials and access rights assigned in Azure.</span></span>  <span data-ttu-id="ecea3-116">在[向 Azure 对 .NET 应用程序进行身份验证](../authentication.md)中了解如何配置身份验证。</span><span class="sxs-lookup"><span data-stu-id="ecea3-116">Learn how to configure authentication in [Authenticating .NET applications to Azure](../authentication.md).</span></span>

3. <span data-ttu-id="ecea3-117">**在应用程序中使用 SDK 编写代码 -** 使用 Azure 服务时，代码将首先创建一个客户端对象来处理服务，然后调用该客户端对象上的方法来与服务交互。</span><span class="sxs-lookup"><span data-stu-id="ecea3-117">**Write code using the SDK in your application -** When working with Azure services, your code will first create a client object to work with the service and then call methods on that client object to interact with the service.</span></span>  <span data-ttu-id="ecea3-118">同时提供同步和异步方法。</span><span class="sxs-lookup"><span data-stu-id="ecea3-118">Both synchronous and asynchronous methods are provided.</span></span>  <span data-ttu-id="ecea3-119">Azure 文档中提供了有关使用每个 SDK 包的示例。</span><span class="sxs-lookup"><span data-stu-id="ecea3-119">Examples of using each individual SDK package are provided throughout the Azure documentation.</span></span>

4. <span data-ttu-id="ecea3-120">**为 SDK 配置日志记录（可选）-** 如果需要诊断应用程序与 Azure 之间的问题，则可以[在用于 .NET 的 Azure SDK 中启用日志记录](./logging.md)。</span><span class="sxs-lookup"><span data-stu-id="ecea3-120">**Configure logging for the SDK (optional) -** If you need to diagnose issues between your application and Azure, you can [enable logging in the Azure SDK for .NET](./logging.md).</span></span>

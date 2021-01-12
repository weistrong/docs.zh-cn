---
title: Azure 和 .NET 入门
description: 学习了解 Azure 和 .NET 所需的基础知识。
ms.date: 06/20/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 5d14bd0d9930d41a8c60b58b9f5b0522f0c0e398
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700765"
---
# <a name="introduction-to-azure-and-net"></a>Azure 和 .NET 简介

## <a name="what-is-azure"></a>什么是 Azure？

Azure 是一个云平台，旨在简化构建新式应用程序的过程。  无论是选择完全在 Azure 中托管应用程序，还是使用 Azure 服务扩展本地应用程序，Azure 都可以帮助你创建可缩放且可维护的可靠应用程序。  凭借对你已在使用的工具（如 Visual Studio 和 Visual Studio Code）和综合性 SDK 库的广泛支持，Azure 旨在使 .NET 开发人员从一开始就高效工作。

## <a name="application-development-scenarios-on-azure"></a>Azure 上的应用程序开发方案

可以根据需要以不同方式将 Azure 集成到应用程序中。

- **在 Azure 上托管的应用程序 -** Azure 可以托管整个应用程序堆栈（从 Web 应用程序和 API 到数据库，再到存储服务）。 Azure 支持各种托管模型（从完全托管的服务到容器，再到虚拟机）。 使用完全托管的 Azure 服务时，应用程序可以利用 Azure 内置的可伸缩性、高可用性和安全性。

- **在应用程序中使用云服务 -** 现有应用可以纳入 Azure 服务以扩展其功能。  这可能包括通过 [Azure 认知搜索](/azure/search/search-what-is-azure-search)添加全文搜索功能、将应用程序机密安全存储在 [Azure Key Vault](/azure/key-vault/) 中或通过 [Azure 认知服务](/azure/cognitive-services/)添加视觉、语音和语言理解功能。  这些服务由 Azure 完全托管，可轻松添加到应用程序中，而无需更改当前的应用程序体系结构或部署模型。

- **新式无服务器体系结构 -** Azure Functions 对构建用于处理事件驱动的工作流的解决方案进行了简化，无论是响应 HTTP 请求、处理 Blob 存储中的文件上传，还是处理队列中的事件，都有涉及。  只需编写处理事件所需的代码，而不必担心服务器或框架代码。  此外，可以利用 250 多个连接器连接到其他 Azure 和第三方服务，以解决最棘手的集成问题。

## <a name="access-azure-services-from-net-applications"></a>从 .NET 应用程序访问 Azure 服务

无论应用托管在 Azure 还是本地，均可通过用于 .NET 的 Azure SDK 提供对大多数 Azure 服务的访问权限。  用于 .NET 的 Azure SDK 以一系列 NuGet 包的形式提供，可以在 .NET Core（2.1 及更高版本）和 .NET Framework（4.6.1 及更高版本）应用程序中使用。 用于 .NET 的 Azure SDK 使将 Azure 服务整合到应用程序中变得就像安装正确的 NuGet 包、实例化客户端对象和调用适当方法那样轻松。 可以在[用于 .NET 的 Azure SDK 概述](./sdk/azure-sdk-for-dotnet.md)中找到有关用于 .NET 的 Azure SDK 的详细信息。

![显示 .NET 应用程序如何使用 Azure SDK 访问 Azure 服务的示意图](./media/azure-sdk-for-dotnet-overview.png)

## <a name="next-steps"></a>后续步骤

接下来，了解用于 .NET 开发的[最常用的 Azure 服务](./key-azure-services.md)。

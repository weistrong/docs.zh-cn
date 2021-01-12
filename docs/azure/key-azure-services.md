---
title: 面向 .NET 开发人员的主要 Azure 服务
description: Azure 提供的服务超过 100 种，但本文重点介绍 .NET 开发人员最常使用的大约 8 种服务
ms.date: 11/30/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 452f09aa93760b21fdb56583025cc421b8d86e44
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700895"
---
# <a name="key-azure-services-for-net-developers"></a>面向 .NET 开发人员的主要 Azure 服务

尽管 Azure 包含超过 100 种服务，但以下 Azure 服务是 .NET 开发人员最常使用的服务。

| **服务** |         | **说明**      |
| :--:|:------|:------------|
| ![应用服务图标](./media/app-services.svg) | **Azure 应用服务** | Azure 应用服务是一个完全托管的平台，用于在 Azure 中托管 Web 应用程序和 API。  它在高可用性环境中提供自动负载均衡和自动缩放功能。  你只需为使用的计算资源付费，并且可使用免费层级。 |
| ![Azure Functions 图标](./media/azure-functions.svg) | **Azure Functions** | Azure Functions 是一种无服务器计算服务，使你可在无需管理任何服务器或运行时的情况下编写和运行代码。  Functions 可以由不同类型的事件触发，而你只需编写处理事件所需的代码即可。        |
| ![Azure SQL 图标](./media/azure-sql.svg) | **Azure SQL**            | Azure SQL 是一种完全托管的基于云的 SQL Server 版本。 Azure 自动执行传统的管理任务（如修补和备份），并提供内置高可用性功能。  |
| ![Cosmos DB 图标](./media/cosmos-db.svg) | **Azure Cosmos DB**      | Azure Cosmos DB 是一种完全托管的 NoSQL 数据库，具有个位数的响应时间、自动缩放功能以及与 MongoDB 兼容的 API。                    |
| ![Azure 存储 Blob 图标](./media/storage-blobs.svg) | **Azure Blob 存储**   | Azure Blob 存储允许应用程序在云中存储和检索文件。  Azure 存储具有高度可缩放性，可存储大量数据，数而据可冗余存储，以确保高可用性。 |
| ![Azure 服务总线图标](./media/service-bus.svg) | **Azure 服务总线**   | Azure 服务总线是一个完全托管的企业消息中转站，支持点到点集成和发布-订阅集成。  这是构建分离式应用程序、基于队列的负载均衡或促进微服务之间通信的理想选择。   |
| ![Azure Key Vault 图标](./media/azure-key-vault.svg) | **Azure Key Vault**   | 每个应用程序都有其必须存储的应用程序机密，例如连接字符串和 API 密钥。  Azure Key Vault 可帮助你在具有受限访问权限的加密保管库中安全地存储和访问这些机密，以确保机密和应用程序不会遭到泄露。   |
| ![认知服务图标](./media/cognitive-services.svg) | **认知服务**   | Azure 认知服务是基于云的服务的集合，使你可向应用程序添加基于 AI 的功能。  示例包括计算机视觉、语音识别、语言理解和异常情况检测。 |

有关 Azure 产品和服务的完整列表，请访问 [Azure 文档主页](/azure/?product=all)

### <a name="next-steps"></a>后续步骤

通过[创建 Azure 帐户](create-azure-account.md)开始配置 Azure 开发环境

---
title: 用于 .NET 的 Azure SDK 概述
description: 概述什么是用于 .NET 的 Azure SDK 以及在 .NET 应用程序中使用 SDK 的基本步骤
ms.date: 11/30/2020
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: b547e105b13d380ffae049ab55e76aa25abe8cc3
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98189195"
---
# <a name="azure-sdk-for-net-overview"></a>用于 .NET 的 Azure SDK 概述

## <a name="what-is-the-azure-sdk-for-net"></a>什么是用于 .NET 的 Azure SDK

用于 .NET 的 Azure SDK 旨在让用户能够轻松从 .NET 应用程序使用 Azure 服务。  无论是向 Blob 存储上传和下载文件、从 Azure Key Vault 检索应用程序机密，还是从 Azure 事件中心处理通知，用于 .NET 的 Azure SDK 都会提供一个一致且熟悉的界面来访问 Azure 服务。  

用于 .NET 的 Azure SDK 以一系列 NuGet 包的形式提供，可以在 .NET Core（2.1 及更高版本）和 .NET Framework（4.6.1 及更高版本）应用程序中使用。

![显示 .NET 应用程序如何使用 Azure SDK 访问 Azure 服务的示意图](./media/azure-sdk-for-dotnet-overview.png)

## <a name="use-the-azure-sdk-for-net-in-your-applications"></a>在应用程序中使用用于 .NET 的 Azure SDK

若要在某一款 .NET 应用程序中使用 Azure SDK 包，则需要按照以下步骤进行操作。

1. **找到相应的 SDK 包 -** 使用 [包列表](../packages.md)查找适合你正在使用的 Azure 服务的包。  请注意，大多数服务都具有用于处理服务的客户端包和用于创建和管理服务实例的管理包。  大多数情况下，你将需要客户端包。  使用 NuGet 在应用程序中安装此包。

2. **为应用程序设置身份验证 -** 若要访问 Azure 资源，应用程序将需要具有在 Azure 中分配的适当凭据和访问权限。  在[向 Azure 对 .NET 应用程序进行身份验证](../authentication.md)中了解如何配置身份验证。

3. **在应用程序中使用 SDK 编写代码 -** 使用 Azure 服务时，代码将首先创建一个客户端对象来处理服务，然后调用该客户端对象上的方法来与服务交互。  同时提供同步和异步方法。  Azure 文档中提供了有关使用每个 SDK 包的示例。

4. **为 SDK 配置日志记录（可选）-** 如果需要诊断应用程序与 Azure 之间的问题，则可以 [在用于 .NET 的 Azure SDK 中启用日志记录](../logging.md)。

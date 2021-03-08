---
title: 使用 Azure 开发 .NET 的配置清单
description: 提供有关已安装的所有工具的简短摘要，以便使用 Azure 进行 .NET 开发
ms.date: 1/1/2021
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 2f22f69ec99baf192d1cbdd28f884b7f47867389
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102257975"
---
# <a name="net-on-azure-development-environment-checklist"></a>使用 Azure 开发 .NET 的环境清单

提供此清单是为了帮助你确保正确配置开发环境以使用 Azure 进行 .NET 开发

## <a name="create-an-azure-account"></a>创建 Azure 帐户

要访问 Azure 服务或在 Azure 中运行应用程序，需要具备一个 Azure 帐户。

* 如果你是 Visual Studio 订阅者，每月都可使用[免费 Azure 额度](https://azure.microsoft.com/pricing/member-offers/credit-for-visual-studio-subscribers/)
* [创建免费的 Azure 帐户](https://azure.microsoft.com/free/dotnet/)即可获得 200 美元额度和精选服务（免费提供 12 个月）。
* 使用公司的 Azure 管理员分配给你的帐户

## <a name="configure-your-ide"></a>配置 IDE

常用工具（如 Visual Studio 和 Visual Studio Code）具有可用于通过 IDE 直接使用 Azure 的扩展。

* 使用 Azure [配置 Visual Studio](./configure-visual-studio.md) 以进行 .NET 开发
* 使用 Azure [配置 Visual Studio Code](./configure-vs-code.md) 以进行 .NET 开发

## <a name="install-the-azure-cli"></a>安装 Azure CLI

除使用 Azure 门户之外，你还需要安装 Azure CLI 来创建和管理 Azure 资源。

* [安装适用于 Windows 的 Azure CLI](/cli/azure/install-azure-cli-windows?tabs=azure-cli)
* [安装适用于 macOS 的 Azure CLI](/cli/azure/install-azure-cli-macos)
* [安装适用于 Linux 的 Azure CLI](/cli/azure/install-azure-cli-linux)

## <a name="install-additional-tools-and-utilities"></a>安装附加工具和实用程序

这些附加工具旨在帮助提高使用 Azure 时的工作效率。

* 如果计划使用 PowerShell 脚本创建和管理 Azure 资源，请[安装 Azure PowerShell](/powershell/azure/install-az-ps)
* 若要上传、下载和管理 Azure 存储资源数据（包括 blob、队列、表和 CosmosDB），请[安装 Azure 存储资源管理器](https://azure.microsoft.com/features/storage-explorer/)。
* 如果要使用 Azure SQL，请安装[Azure Data Studio](/sql/azure-data-studio/download-azure-data-studio)

## <a name="bookmark-the-following-sites"></a>在以下站点中添加书签

使用 Azure 进行开发时，将会频繁使用这些站点。  可为这些站点添加书签以供快速参考。

* Azure Portal - [https://portal.azure.com/](https://portal.azure.com/)
* Azure Cloud Shell - [https://shell.azure.com/](https://shell.azure.com/)

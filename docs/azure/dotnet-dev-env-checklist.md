---
title: 使用 Azure 开发 .NET 的配置清单
description: 提供有关已安装的所有工具的简短摘要，以便使用 Azure 进行 .NET 开发
ms.date: 1/1/2021
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: a2ff9bbf1e6a8790ddc161a1a1c8d14e8fab6e41
ms.sourcegitcommit: 5d9cee27d9ffe8f5670e5f663434511e81b8ac38
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "98027236"
---
# <a name="net-on-azure-development-environment-checklist"></a><span data-ttu-id="5493e-103">使用 Azure 开发 .NET 的环境清单</span><span class="sxs-lookup"><span data-stu-id="5493e-103">.NET on Azure development environment checklist</span></span>

<span data-ttu-id="5493e-104">提供此清单是为了帮助你确保正确配置开发环境以使用 Azure 进行 .NET 开发</span><span class="sxs-lookup"><span data-stu-id="5493e-104">This checklist is provided to help you make sure you have your development environment correctly configured for .NET development with Azure</span></span>

## <a name="create-an-azure-account"></a><span data-ttu-id="5493e-105">创建 Azure 帐户</span><span class="sxs-lookup"><span data-stu-id="5493e-105">Create an Azure account</span></span>

<span data-ttu-id="5493e-106">要访问 Azure 服务或在 Azure 中运行应用程序，需要具备一个 Azure 帐户。</span><span class="sxs-lookup"><span data-stu-id="5493e-106">To access Azure services or run applications in Azure, you need an Azure account.</span></span>

* <span data-ttu-id="5493e-107">如果你是 Visual Studio 订阅者，每月都可使用[免费 Azure 额度](https://azure.microsoft.com/pricing/member-offers/credit-for-visual-studio-subscribers/)</span><span class="sxs-lookup"><span data-stu-id="5493e-107">If you are a Visual Studio subscriber, you have monthly [free Azure credits](https://azure.microsoft.com/pricing/member-offers/credit-for-visual-studio-subscribers/) available to you every month</span></span>
* <span data-ttu-id="5493e-108">[创建免费的 Azure 帐户](https://azure.microsoft.com/free/dotnet/)即可获得 200 美元额度和精选服务（免费提供 12 个月）。</span><span class="sxs-lookup"><span data-stu-id="5493e-108">[Create a free Azure account](https://azure.microsoft.com/free/dotnet/) and receive $200 in credits and select services free for 12 months</span></span>
* <span data-ttu-id="5493e-109">使用公司的 Azure 管理员分配给你的帐户</span><span class="sxs-lookup"><span data-stu-id="5493e-109">Use an account assigned to you by your company's Azure administrator</span></span>

## <a name="configure-your-ide"></a><span data-ttu-id="5493e-110">配置 IDE</span><span class="sxs-lookup"><span data-stu-id="5493e-110">Configure your IDE</span></span>

<span data-ttu-id="5493e-111">常用工具（如 Visual Studio 和 Visual Studio Code）具有可用于通过 IDE 直接使用 Azure 的扩展。</span><span class="sxs-lookup"><span data-stu-id="5493e-111">Popular tools like Visual Studio and Visual Studio Code have extensions available to let you work with Azure right from your IDE.</span></span>

* <span data-ttu-id="5493e-112">使用 Azure [配置 Visual Studio](./configure-visual-studio.md) 以进行 .NET 开发</span><span class="sxs-lookup"><span data-stu-id="5493e-112">[Configure Visual Studio](./configure-visual-studio.md) for .NET development using Azure</span></span>
* <span data-ttu-id="5493e-113">使用 Azure [配置 Visual Studio Code](./configure-vs-code.md) 以进行 .NET 开发</span><span class="sxs-lookup"><span data-stu-id="5493e-113">[Configure Visual Studio Code](./configure-vs-code.md) for .NET Development using Azure</span></span>

## <a name="install-the-azure-cli"></a><span data-ttu-id="5493e-114">安装 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="5493e-114">Install the Azure CLI</span></span>

<span data-ttu-id="5493e-115">除使用 Azure 门户之外，你还需要安装 Azure CLI 来创建和管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="5493e-115">In addition to using the Azure portal, you will want to install the Azure CLI to create and manage Azure resources.</span></span>

* <span data-ttu-id="5493e-116">[安装适用于 Windows 的 Azure CLI](/cli/azure/install-azure-cli-windows?tabs=azure-cli)</span><span class="sxs-lookup"><span data-stu-id="5493e-116">[Install the Azure CLI for Windows](/cli/azure/install-azure-cli-windows?tabs=azure-cli))</span></span>
* [<span data-ttu-id="5493e-117">安装适用于 macOS 的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="5493e-117">Install the Azure CLI for macOS</span></span>](/cli/azure/install-azure-cli-macos)
* [<span data-ttu-id="5493e-118">安装适用于 Linux 的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="5493e-118">Install the Azure CLI for Linux</span></span>](/cli/azure/install-azure-cli-linux)

## <a name="install-additional-tools-and-utilities"></a><span data-ttu-id="5493e-119">安装附加工具和实用程序</span><span class="sxs-lookup"><span data-stu-id="5493e-119">Install additional tools and utilities</span></span>

<span data-ttu-id="5493e-120">这些附加工具旨在帮助提高使用 Azure 时的工作效率。</span><span class="sxs-lookup"><span data-stu-id="5493e-120">These additional tools are designed to make you more productive when working with Azure.</span></span>

* <span data-ttu-id="5493e-121">如果计划使用 PowerShell 脚本创建和管理 Azure 资源，请[安装 Azure PowerShell](/powershell/azure/install-az-ps)</span><span class="sxs-lookup"><span data-stu-id="5493e-121">[Install Azure PowerShell](/powershell/azure/install-az-ps) if you plan on using PowerShell scripts to create and manage Azure resources</span></span>
* <span data-ttu-id="5493e-122">若要上传、下载和管理 Azure 存储资源数据（包括 blob、队列、表和 CosmosDB），请[安装 Azure 存储资源管理器](https://azure.microsoft.com/features/storage-explorer/)。</span><span class="sxs-lookup"><span data-stu-id="5493e-122">[Install Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/) to upload, download, and manage data in Azure storage resources including blobs, queues, tables, and CosmosDB.</span></span>
* <span data-ttu-id="5493e-123">如果要使用 Azure SQL，请安装[Azure Data Studio](/sql/azure-data-studio/download-azure-data-studio)</span><span class="sxs-lookup"><span data-stu-id="5493e-123">[Install Azure Data Studio](/sql/azure-data-studio/download-azure-data-studio) if you are working with Azure SQL</span></span>

## <a name="bookmark-the-following-sites"></a><span data-ttu-id="5493e-124">在以下站点中添加书签</span><span class="sxs-lookup"><span data-stu-id="5493e-124">Bookmark the following sites</span></span>

<span data-ttu-id="5493e-125">使用 Azure 进行开发时，将会频繁使用这些站点。</span><span class="sxs-lookup"><span data-stu-id="5493e-125">You will use these sites frequently when doing Azure development.</span></span>  <span data-ttu-id="5493e-126">可为这些站点添加书签以供快速参考。</span><span class="sxs-lookup"><span data-stu-id="5493e-126">Bookmark them for quick reference.</span></span>

* <span data-ttu-id="5493e-127">Azure Portal - [https://portal.azure.com/](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="5493e-127">Azure Portal - [https://portal.azure.com/](https://portal.azure.com/)</span></span>
* <span data-ttu-id="5493e-128">Azure Cloud Shell - [https://shell.azure.com/](https://shell.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="5493e-128">Azure Cloud Shell - [https://shell.azure.com/](https://shell.azure.com/)</span></span>

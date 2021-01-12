---
title: 安装 Azure CLI
description: Azure 开发人员将需要安装 Azure CLI，因此本文介绍了需要 CLI 的原因以及从何处下载和安装 CLI。
ms.date: 11/30/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 43737aaf5dfd02b8c4ffa6c213d7221cfe38162f
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700897"
---
# <a name="install-the-azure-cli"></a><span data-ttu-id="eea98-103">安装 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="eea98-103">Install the Azure CLI</span></span>

<span data-ttu-id="eea98-104">除了 Azure 门户，Azure还提供 [Azure CLI](/cli/azure/) 作为命令行工具，以便创建和管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="eea98-104">In addition to the Azure Portal, Azure also offers the [Azure CLI](/cli/azure/) as a command-line tool to create and manage Azure resources.</span></span> <span data-ttu-id="eea98-105">Azure CLI 在效率、可重复性和可编写重复性任务脚本方面具有优势。</span><span class="sxs-lookup"><span data-stu-id="eea98-105">The Azure CLI offers the benefits of efficiency, repeatability, and the ability to script recurring tasks.</span></span>  

<span data-ttu-id="eea98-106">实际上，大多数开发人员同时使用 Azure 门户和 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="eea98-106">In practice, most developers use both the Azure Portal and the Azure CLI.</span></span> <span data-ttu-id="eea98-107">在探索新服务并大致了解 Azure 帐户中的所有资源时，尽管 Azure 门户非常有用，但大多数开发人员都发现 Azure CLI 速度更快且效率更高。</span><span class="sxs-lookup"><span data-stu-id="eea98-107">Where as the Azure Portal is useful when exploring new services and getting an overview of all of the resources in your Azure account, most developers find the Azure CLI to be faster and more efficient.</span></span>  <span data-ttu-id="eea98-108">Azure CLI 通常可在一个命令中完成 Azure 门户中需要执行多个步骤的内容。</span><span class="sxs-lookup"><span data-stu-id="eea98-108">The Azure CLI can often accomplish in a single command what takes multiple steps in the Azure Portal.</span></span>  <span data-ttu-id="eea98-109">此外，由于 Azure CLI 命令可以保存到文件中，因此开发人员可以确保重复性任务每次都以相同方式运行。</span><span class="sxs-lookup"><span data-stu-id="eea98-109">In addition, since Azure CLI commands can be saved to a file, developers can assure that recurrent tasks are run the same way each time.</span></span>

<span data-ttu-id="eea98-110">Azure CLI 适用于 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="eea98-110">The Azure CLI is available for Windows, macOS, and Linux.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="eea98-111">安装适用于 Windows 的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="eea98-111">Install the Azure CLI for Windows</span></span>](/cli/azure/install-azure-cli-windows?tabs=azure-cli)

> [!div class="nextstepaction"]
> [<span data-ttu-id="eea98-112">安装适用于 macOS 的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="eea98-112">Install the Azure CLI for macOS</span></span>](/cli/azure/install-azure-cli-macos)

> [!div class="nextstepaction"]
> [<span data-ttu-id="eea98-113">安装适用于 Linux 的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="eea98-113">Install the Azure CLI for Linux</span></span>](/cli/azure/install-azure-cli-linux)

### <a name="azure-cloud-shell"></a><span data-ttu-id="eea98-114">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="eea98-114">Azure Cloud Shell</span></span>

<span data-ttu-id="eea98-115">还可以通过以下链接在 Azure Cloud Shell 中使用 Azure CLI：[https://shell.azure.com](https://shell.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="eea98-115">You can also use the Azure CLI in the Azure Cloud Shell at [https://shell.azure.com](https://shell.azure.com).</span></span>  <span data-ttu-id="eea98-116">Azure Cloud Shell 是基于浏览器的功能齐全的 shell，用于管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="eea98-116">The Azure Cloud Shell is a fully functional, browser-based shell for managing Azure resources.</span></span>  <span data-ttu-id="eea98-117">当你需要命令行环境，而工作的设备无法安装 Azure CLI 时，Azure Cloud Shell 很有用。</span><span class="sxs-lookup"><span data-stu-id="eea98-117">The Azure Cloud Shell is useful when you need a command line environment but are working on a device where you are unable to install the Azure CLI.</span></span>

![在浏览器中运行的 Azure Cloud Shell 的屏幕截图](media/azure-cloud-shell.png)

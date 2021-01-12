---
title: 配置 Visual Studio Code，以使用 .NET 进行 Azure 开发
description: 本文可帮助你配置 Visual Studio Code，以进行 Azure 开发，包括在 VS Code 中安装和配置正确的插件
ms.date: 11/30/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 65ced99befe12d137062b4ea6a59a1ccd3099e0b
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700905"
---
# <a name="configure-visual-studio-code-for-azure-development"></a><span data-ttu-id="66571-103">配置 Visual Studio Code，以进行 Azure 开发</span><span class="sxs-lookup"><span data-stu-id="66571-103">Configure Visual Studio Code for Azure development</span></span>

<span data-ttu-id="66571-104">如果你使用的是 Visual Studio Code，则无论是进行 .NET 开发，使用框架（如 Angular、React 或 Vue）构建单页应用程序，还是使用其他语言（如 Python）编写应用程序，都需要配置 Visual Studio Code 才能进行 Azure 开发。</span><span class="sxs-lookup"><span data-stu-id="66571-104">If you are using Visual Studio Code, whether for .NET development, for building single page applications using frameworks like Angular, React or Vue, or for writing applications in another language like Python, you will want to configure Visual Studio Code for Azure development.</span></span>

### <a name="download-visual-studio-code"></a><span data-ttu-id="66571-105">下载 Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="66571-105">Download Visual Studio Code</span></span>

<span data-ttu-id="66571-106">如果已安装 Visual Studio Code，则可跳过此步骤</span><span class="sxs-lookup"><span data-stu-id="66571-106">If you already have Visual Studio Code installed, you can skip this step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="66571-107">下载 Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="66571-107">Download Visual Studio Code</span></span>](https://code.visualstudio.com/download)

### <a name="install-the-azure-tools-extension-pack"></a><span data-ttu-id="66571-108">安装 Azure Tools 扩展包</span><span class="sxs-lookup"><span data-stu-id="66571-108">Install the Azure Tools Extension Pack</span></span>

<span data-ttu-id="66571-109">[Azure Tools 扩展包](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack)包含适用于 Azure 应用服务、Azure Functions、Azure 存储、Cosmos DB 和 Azure 虚拟机的扩展，所有这些都位于一个方便的包中。</span><span class="sxs-lookup"><span data-stu-id="66571-109">The [Azure Tools Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack) contains extensions for working with Azure App Service, Azure Functions, Azure Storage, Cosmos DB, and Azure Virtual Machines all in one convenient package.</span></span>

<span data-ttu-id="66571-110">要从 Visual Studio Code 安装扩展，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="66571-110">To install the extension from Visual Studio Code:</span></span>

1. <span data-ttu-id="66571-111">按 <kbd>Ctrl+Shift+X</kbd> 打开“扩展”窗口。</span><span class="sxs-lookup"><span data-stu-id="66571-111">Press <kbd>Ctrl+Shift+X</kbd> to open the **Extensions** window.</span></span>
1. <span data-ttu-id="66571-112">搜索 Azure Tools 扩展。</span><span class="sxs-lookup"><span data-stu-id="66571-112">Search for the *Azure Tools* extension.</span></span>
1. <span data-ttu-id="66571-113">选择“安装”按钮  。</span><span class="sxs-lookup"><span data-stu-id="66571-113">Select the **Install** button.</span></span>

![Visual Studio Code 的屏幕截图，其中显示了正在搜索 Azure Tools 扩展包的扩展面板](./media/visual-studio-code-azure-tools.png)

<span data-ttu-id="66571-115">要详细了解如何在 Visual Studio Code 中安装扩展，请参阅 Visual Studio Code 网站上的[扩展市场](https://code.visualstudio.com/docs/editor/extension-gallery)文档。</span><span class="sxs-lookup"><span data-stu-id="66571-115">To learn more about installing extensions in Visual Studio Code, refer to the [Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery) document on the Visual Studio Code website.</span></span>

### <a name="sign-in-to-your-azure-account-with-azure-tools"></a><span data-ttu-id="66571-116">使用 Azure Tools 登录到 Azure 帐户</span><span class="sxs-lookup"><span data-stu-id="66571-116">Sign in to your Azure account with Azure Tools</span></span>

<span data-ttu-id="66571-117">在左侧面板上，将出现一个 Azure 图标。</span><span class="sxs-lookup"><span data-stu-id="66571-117">On the left hand panel, you'll see an Azure icon.</span></span> <span data-ttu-id="66571-118">选择此图标，此时将显示 Azure 服务的控制面板。</span><span class="sxs-lookup"><span data-stu-id="66571-118">Select this icon, and a control panel for Azure services will appear.</span></span> <span data-ttu-id="66571-119">在任何服务下选择“登录到 Azure…”，以在 Visual Studio Code 中完成 Azure Tools 的身份验证过程。</span><span class="sxs-lookup"><span data-stu-id="66571-119">Choose **Sign in to Azure...** under any service to complete the authentication process for the Azure tools in Visual Studio Code.</span></span>

![Visual Studio Code 的屏幕截图，其中显示了如何将 Azure Tools 登录到 Azure](./media/visual-studio-code-azure-login.png)

### <a name="next-steps"></a><span data-ttu-id="66571-121">后续步骤</span><span class="sxs-lookup"><span data-stu-id="66571-121">Next steps</span></span>

<span data-ttu-id="66571-122">接下来，在工作站上安装 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="66571-122">Next, you will want to install the Azure CLI on your workstation.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="66571-123">安装 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="66571-123">Install the Azure CLI</span></span>](./install-azure-cli.md)

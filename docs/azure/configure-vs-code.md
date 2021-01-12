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
# <a name="configure-visual-studio-code-for-azure-development"></a>配置 Visual Studio Code，以进行 Azure 开发

如果你使用的是 Visual Studio Code，则无论是进行 .NET 开发，使用框架（如 Angular、React 或 Vue）构建单页应用程序，还是使用其他语言（如 Python）编写应用程序，都需要配置 Visual Studio Code 才能进行 Azure 开发。

### <a name="download-visual-studio-code"></a>下载 Visual Studio Code

如果已安装 Visual Studio Code，则可跳过此步骤

> [!div class="nextstepaction"]
> [下载 Visual Studio Code](https://code.visualstudio.com/download)

### <a name="install-the-azure-tools-extension-pack"></a>安装 Azure Tools 扩展包

[Azure Tools 扩展包](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack)包含适用于 Azure 应用服务、Azure Functions、Azure 存储、Cosmos DB 和 Azure 虚拟机的扩展，所有这些都位于一个方便的包中。

要从 Visual Studio Code 安装扩展，请执行以下操作：

1. 按 <kbd>Ctrl+Shift+X</kbd> 打开“扩展”窗口。
1. 搜索 Azure Tools 扩展。
1. 选择“安装”按钮  。

![Visual Studio Code 的屏幕截图，其中显示了正在搜索 Azure Tools 扩展包的扩展面板](./media/visual-studio-code-azure-tools.png)

要详细了解如何在 Visual Studio Code 中安装扩展，请参阅 Visual Studio Code 网站上的[扩展市场](https://code.visualstudio.com/docs/editor/extension-gallery)文档。

### <a name="sign-in-to-your-azure-account-with-azure-tools"></a>使用 Azure Tools 登录到 Azure 帐户

在左侧面板上，将出现一个 Azure 图标。 选择此图标，此时将显示 Azure 服务的控制面板。 在任何服务下选择“登录到 Azure…”，以在 Visual Studio Code 中完成 Azure Tools 的身份验证过程。

![Visual Studio Code 的屏幕截图，其中显示了如何将 Azure Tools 登录到 Azure](./media/visual-studio-code-azure-login.png)

### <a name="next-steps"></a>后续步骤

接下来，在工作站上安装 Azure CLI。

> [!div class="nextstepaction"]
> [安装 Azure CLI](./install-azure-cli.md)

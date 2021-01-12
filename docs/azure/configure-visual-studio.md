---
title: 配置 Visual Studio，以使用 .NET 进行 Azure 开发
description: 本文可帮助你配置 Visual Studio，以进行 Azure 开发，包括安装正确的工作负载，以及将 Visual Studio 连接到 Azure 帐户
ms.date: 11/30/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.author: daberry
author: daberry
ms.openlocfilehash: 986469bd07657d968045465803047dc21d76dd62
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700908"
---
# <a name="configure-visual-studio-for-azure-development-with-net"></a>配置 Visual Studio，以使用 .NET 进行 Azure 开发

Visual Studio 包含有助于在 Azure 上开发和部署应用程序的工具。  本指南将帮助你确保正确配置 Visual Studio，以进行 Azure 开发。

### <a name="download-visual-studio-2019"></a>下载 Visual Studio 2019

如果已安装 Visual Studio 2019，则可跳过此步骤。

> [!div class="nextstepaction"]
> [下载 Visual Studio 2019](https://www.visualstudio.com/downloads/)

### <a name="install-azure-workloads"></a>安装 Azure 工作负载

启动 Visual Studio 安装程序并验证是否已安装 Azure 开发以及 ASP.NET 和 Web 开发工作负载  。  如果未安装其中任一工作负载，请选择相应工作负载进行安装。

![Visual Studio 安装程序的屏幕截图，其中显示了已选择 Azure 开发以及 ASP.NET 和 Web 开发工作负载](./media/visual-studio-installer-azure-development.png)

### <a name="authenticate-visual-studio-with-azure"></a>通过 Visual Studio 向 Azure 进行身份验证

通过 Visual Studio 调试应用时，Visual Studio 可以使用 Azure 帐户验证身份并访问 Azure 资源。  直接通过 Visual Studio 将应用发布到 Azure 时，也会用到此帐户。

若要在 Visual Studio 中对 Azure 帐户进行身份验证，请选择“工具” > “选项”菜单，以启动“选项”对话框  。 导航到 `Azure Service Authentication` 选项，并使用 Azure 帐户登录。

![Visual Studio“选项”对话框的屏幕截图，其中显示了 Azure 登录](./media/visual-studio-azure-login-dialog.png)

### <a name="next-steps"></a>后续步骤

如果还使用 [Visual Studio Code](https://code.visualstudio.com/) 以 .NET 或任何其他语言进行开发，则还应[配置 Visual Studio Code，以进行 Azure 开发](./configure-vs-code.md)。 否则，请继续[安装 Azure CLI](./install-azure-cli.md)。

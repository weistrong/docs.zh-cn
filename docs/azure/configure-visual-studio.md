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
# <a name="configure-visual-studio-for-azure-development-with-net"></a><span data-ttu-id="4f206-103">配置 Visual Studio，以使用 .NET 进行 Azure 开发</span><span class="sxs-lookup"><span data-stu-id="4f206-103">Configure Visual Studio for Azure development with .NET</span></span>

<span data-ttu-id="4f206-104">Visual Studio 包含有助于在 Azure 上开发和部署应用程序的工具。</span><span class="sxs-lookup"><span data-stu-id="4f206-104">Visual Studio includes tooling to help with the development and deployment of applications on Azure.</span></span>  <span data-ttu-id="4f206-105">本指南将帮助你确保正确配置 Visual Studio，以进行 Azure 开发。</span><span class="sxs-lookup"><span data-stu-id="4f206-105">This guide will help you make sure that you have Visual Studio properly configured for Azure development.</span></span>

### <a name="download-visual-studio-2019"></a><span data-ttu-id="4f206-106">下载 Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="4f206-106">Download Visual Studio 2019</span></span>

<span data-ttu-id="4f206-107">如果已安装 Visual Studio 2019，则可跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="4f206-107">If you already have Visual Studio 2019 installed, you can skip this step.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4f206-108">下载 Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="4f206-108">Download Visual Studio 2019</span></span>](https://www.visualstudio.com/downloads/)

### <a name="install-azure-workloads"></a><span data-ttu-id="4f206-109">安装 Azure 工作负载</span><span class="sxs-lookup"><span data-stu-id="4f206-109">Install Azure workloads</span></span>

<span data-ttu-id="4f206-110">启动 Visual Studio 安装程序并验证是否已安装 Azure 开发以及 ASP.NET 和 Web 开发工作负载  。</span><span class="sxs-lookup"><span data-stu-id="4f206-110">Launch the **Visual Studio Installer** and validate that you have the workloads **Azure development** and **ASP.NET and web development** are installed.</span></span>  <span data-ttu-id="4f206-111">如果未安装其中任一工作负载，请选择相应工作负载进行安装。</span><span class="sxs-lookup"><span data-stu-id="4f206-111">If either of these workloads is not installed, select these workloads to install them.</span></span>

![Visual Studio 安装程序的屏幕截图，其中显示了已选择 Azure 开发以及 ASP.NET 和 Web 开发工作负载](./media/visual-studio-installer-azure-development.png)

### <a name="authenticate-visual-studio-with-azure"></a><span data-ttu-id="4f206-113">通过 Visual Studio 向 Azure 进行身份验证</span><span class="sxs-lookup"><span data-stu-id="4f206-113">Authenticate Visual Studio with Azure</span></span>

<span data-ttu-id="4f206-114">通过 Visual Studio 调试应用时，Visual Studio 可以使用 Azure 帐户验证身份并访问 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="4f206-114">When debugging apps through Visual Studio, Visual Studio can use your Azure account to authenticate and access Azure Resources with.</span></span>  <span data-ttu-id="4f206-115">直接通过 Visual Studio 将应用发布到 Azure 时，也会用到此帐户。</span><span class="sxs-lookup"><span data-stu-id="4f206-115">This account is also used when you publish apps directly from Visual Studio to Azure.</span></span>

<span data-ttu-id="4f206-116">若要在 Visual Studio 中对 Azure 帐户进行身份验证，请选择“工具” > “选项”菜单，以启动“选项”对话框  。</span><span class="sxs-lookup"><span data-stu-id="4f206-116">To authenticate your Azure account from Visual Studio, select the **Tools** > **Options** menu to launch the **Options** dialog.</span></span> <span data-ttu-id="4f206-117">导航到 `Azure Service Authentication` 选项，并使用 Azure 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="4f206-117">Navigate to the `Azure Service Authentication` options and sign in using your Azure account.</span></span>

![Visual Studio“选项”对话框的屏幕截图，其中显示了 Azure 登录](./media/visual-studio-azure-login-dialog.png)

### <a name="next-steps"></a><span data-ttu-id="4f206-119">后续步骤</span><span class="sxs-lookup"><span data-stu-id="4f206-119">Next steps</span></span>

<span data-ttu-id="4f206-120">如果还使用 [Visual Studio Code](https://code.visualstudio.com/) 以 .NET 或任何其他语言进行开发，则还应[配置 Visual Studio Code，以进行 Azure 开发](./configure-vs-code.md)。</span><span class="sxs-lookup"><span data-stu-id="4f206-120">If you also use [Visual Studio Code](https://code.visualstudio.com/) for development in .NET or any other language, you should also [configure Visual Studio Code for Azure development](./configure-vs-code.md).</span></span> <span data-ttu-id="4f206-121">否则，请继续[安装 Azure CLI](./install-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="4f206-121">Otherwise, proceed to [Installing the Azure CLI](./install-azure-cli.md).</span></span>

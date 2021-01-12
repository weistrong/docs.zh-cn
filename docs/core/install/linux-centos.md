---
title: 在 CentOS 上安装 .NET - .NET
description: 演示在 CentOS 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 01/06/2021
ms.openlocfilehash: 7e73f90a1f1f7e11e592b1b074f243c9f5b32ced
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970858"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-centos"></a><span data-ttu-id="8af80-103">在 CentOS 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="8af80-103">Install the .NET SDK or the .NET Runtime on CentOS</span></span>

<span data-ttu-id="8af80-104">CentOS 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="8af80-104">.NET is supported on CentOS.</span></span> <span data-ttu-id="8af80-105">本文介绍如何在 CentOS 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="8af80-105">This article describes how to install .NET on CentOS.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="8af80-106">支持的分发</span><span class="sxs-lookup"><span data-stu-id="8af80-106">Supported distributions</span></span>

<span data-ttu-id="8af80-107">下表列出了 CentOS 7 和 CentOS 8 上当前受支持的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="8af80-107">The following table is a list of currently supported .NET releases on both CentOS 7 and CentOS 8.</span></span> <span data-ttu-id="8af80-108">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 CentOS 版本不再受支持之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="8af80-108">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of CentOS is no longer supported.</span></span>

- <span data-ttu-id="8af80-109">✔️ 指示 CentOS 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="8af80-109">A ✔️ indicates that the version of CentOS or .NET is still supported.</span></span>
- <span data-ttu-id="8af80-110">❌ 指示 CentOS 或 .NET 版本在该 CentOS 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="8af80-110">A ❌ indicates that the version of CentOS or .NET isn't supported on that CentOS release.</span></span>
- <span data-ttu-id="8af80-111">当 CentOS 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="8af80-111">When both a version of CentOS and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="8af80-112">CentOS</span><span class="sxs-lookup"><span data-stu-id="8af80-112">CentOS</span></span>                   | <span data-ttu-id="8af80-113">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="8af80-113">.NET Core 2.1</span></span> | <span data-ttu-id="8af80-114">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="8af80-114">.NET Core 3.1</span></span> | <span data-ttu-id="8af80-115">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="8af80-115">.NET 5.0</span></span> |
|--------------------------|---------------|---------------|----------------|
| <span data-ttu-id="8af80-116">✔️ [8](#centos-8-)</span><span class="sxs-lookup"><span data-stu-id="8af80-116">✔️ [8](#centos-8-)</span></span> | <span data-ttu-id="8af80-117">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="8af80-117">✔️ 2.1</span></span>        | <span data-ttu-id="8af80-118">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="8af80-118">✔️ 3.1</span></span>        | <span data-ttu-id="8af80-119">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="8af80-119">✔️ 5.0</span></span> |
| <span data-ttu-id="8af80-120">✔️ [7](#centos-7-)</span><span class="sxs-lookup"><span data-stu-id="8af80-120">✔️ [7](#centos-7-)</span></span> | <span data-ttu-id="8af80-121">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="8af80-121">✔️ 2.1</span></span>        | <span data-ttu-id="8af80-122">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="8af80-122">✔️ 3.1</span></span>        | <span data-ttu-id="8af80-123">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="8af80-123">✔️ 5.0</span></span> |

<span data-ttu-id="8af80-124">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="8af80-124">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="8af80-125">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="8af80-125">The downloads for these still remain published:</span></span>

- <span data-ttu-id="8af80-126">3.0</span><span class="sxs-lookup"><span data-stu-id="8af80-126">3.0</span></span>
- <span data-ttu-id="8af80-127">2.2</span><span class="sxs-lookup"><span data-stu-id="8af80-127">2.2</span></span>
- <span data-ttu-id="8af80-128">2.0</span><span class="sxs-lookup"><span data-stu-id="8af80-128">2.0</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="remove-preview-versions"></a><span data-ttu-id="8af80-129">删除预览版本</span><span class="sxs-lookup"><span data-stu-id="8af80-129">Remove preview versions</span></span>

[!INCLUDE [package-manager uninstall notice](./includes/linux-uninstall-preview-info.md)]

## <a name="centos-8-"></a><span data-ttu-id="8af80-130">CentOS 8 ✔️</span><span class="sxs-lookup"><span data-stu-id="8af80-130">CentOS 8 ✔️</span></span>

<span data-ttu-id="8af80-131">.NET 5.0 在 CentOS 8 的默认包存储库中提供。</span><span class="sxs-lookup"><span data-stu-id="8af80-131">.NET 5.0 is available in the default package repositories for CentOS 8.</span></span>

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="centos-7-"></a><span data-ttu-id="8af80-132">CentOS 7 ✔️</span><span class="sxs-lookup"><span data-stu-id="8af80-132">CentOS 7 ✔️</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
```

[!INCLUDE [linux-yum-install-50](includes/linux-install-50-yum.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="8af80-133">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="8af80-133">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="troubleshoot-the-package-manager"></a><span data-ttu-id="8af80-134">包管理器疑难解答</span><span class="sxs-lookup"><span data-stu-id="8af80-134">Troubleshoot the package manager</span></span>

<span data-ttu-id="8af80-135">本部分提供有关使用包管理器安装 .NET 时可能会遇到的常见错误的信息。</span><span class="sxs-lookup"><span data-stu-id="8af80-135">This section provides information on common errors you may get while using the package manager to install .NET.</span></span>

### <a name="unable-to-find-package"></a><span data-ttu-id="8af80-136">找不到包</span><span class="sxs-lookup"><span data-stu-id="8af80-136">Unable to find package</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

### <a name="failed-to-fetch"></a><span data-ttu-id="8af80-137">未能提取</span><span class="sxs-lookup"><span data-stu-id="8af80-137">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-rpm](includes/package-manager-failed-to-fetch-rpm.md)]

## <a name="dependencies"></a><span data-ttu-id="8af80-138">依赖项</span><span class="sxs-lookup"><span data-stu-id="8af80-138">Dependencies</span></span>

[!INCLUDE [linux-rpm-install-dependencies](includes/linux-rpm-install-dependencies.md)]

## <a name="next-steps"></a><span data-ttu-id="8af80-139">后续步骤</span><span class="sxs-lookup"><span data-stu-id="8af80-139">Next steps</span></span>

- [<span data-ttu-id="8af80-140">如何为 .NET CLI 启用 Tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="8af80-140">How to enable TAB completion for the .NET CLI</span></span>](../tools/enable-tab-autocomplete.md)
- [<span data-ttu-id="8af80-141">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="8af80-141">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)

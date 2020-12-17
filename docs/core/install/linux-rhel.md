---
title: 在 RHEL 上安装 .NET - .NET
description: 演示在 RHEL 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: 0b6138185bfd3e2f50c1b31e82779165715a5b6e
ms.sourcegitcommit: 45c7148f2483db2501c1aa696ab6ed2ed8cb71b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "96851635"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-rhel"></a><span data-ttu-id="d7cc3-103">在 RHEL 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="d7cc3-103">Install the .NET SDK or the .NET Runtime on RHEL</span></span>

<span data-ttu-id="d7cc3-104">RHEL 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-104">.NET is supported on RHEL.</span></span> <span data-ttu-id="d7cc3-105">本文介绍如何在 RHEL 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-105">This article describes how to install .NET on RHEL.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

## <a name="register-your-red-hat-subscription"></a><span data-ttu-id="d7cc3-106">注册 Red Hat 订阅</span><span class="sxs-lookup"><span data-stu-id="d7cc3-106">Register your Red Hat subscription</span></span>

<span data-ttu-id="d7cc3-107">若要在 RHEL 上从 Red Hat 安装 .NET，首先需要使用 Red Hat 订阅管理器进行注册。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-107">To install .NET from Red Hat on RHEL, you first need to register using the Red Hat Subscription Manager.</span></span> <span data-ttu-id="d7cc3-108">如果未在系统上完成此操作，或者不确定是否完成了此操作，请参阅[适用于 .NET 的 Red Hat 产品文档](https://access.redhat.com/documentation/net/5.0/)。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-108">If this hasn't been done on your system, or if you're unsure, see the [Red Hat Product Documentation for .NET](https://access.redhat.com/documentation/net/5.0/).</span></span>

## <a name="supported-distributions"></a><span data-ttu-id="d7cc3-109">支持的发行版</span><span class="sxs-lookup"><span data-stu-id="d7cc3-109">Supported distributions</span></span>

<span data-ttu-id="d7cc3-110">下表列出了 RHEL 7 和 RHEL 8 上当前受支持的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-110">The following table is a list of currently supported .NET releases on both RHEL 7 and RHEL 8.</span></span> <span data-ttu-id="d7cc3-111">这些版本在 [.NET 达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 RHEL 版本不再受到支持之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-111">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of RHEL is no longer supported.</span></span>

- <span data-ttu-id="d7cc3-112">✔️ 指示 RHEL 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-112">A ✔️ indicates that the version of RHEL or .NET is still supported.</span></span>
- <span data-ttu-id="d7cc3-113">❌ 指示 RHEL 或 .NET 版本在该 RHEL 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-113">A ❌ indicates that the version of RHEL or .NET isn't supported on that RHEL release.</span></span>
- <span data-ttu-id="d7cc3-114">当 RHEL 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-114">When both a version of RHEL and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="d7cc3-115">RHEL</span><span class="sxs-lookup"><span data-stu-id="d7cc3-115">RHEL</span></span>                     | <span data-ttu-id="d7cc3-116">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="d7cc3-116">.NET Core 2.1</span></span> | <span data-ttu-id="d7cc3-117">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="d7cc3-117">.NET Core 3.1</span></span> | <span data-ttu-id="d7cc3-118">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="d7cc3-118">.NET 5.0</span></span> |
|--------------------------|---------------|---------------|----------------|
| <span data-ttu-id="d7cc3-119">✔️ [8](#rhel-8-)</span><span class="sxs-lookup"><span data-stu-id="d7cc3-119">✔️ [8](#rhel-8-)</span></span>        | <span data-ttu-id="d7cc3-120">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="d7cc3-120">✔️ 2.1</span></span>        | <span data-ttu-id="d7cc3-121">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="d7cc3-121">✔️ 3.1</span></span>        | <span data-ttu-id="d7cc3-122">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="d7cc3-122">✔️ 5.0</span></span> |
| <span data-ttu-id="d7cc3-123">✔️ [7](#rhel-7--net-50)</span><span class="sxs-lookup"><span data-stu-id="d7cc3-123">✔️ [7](#rhel-7--net-50)</span></span> | <span data-ttu-id="d7cc3-124">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="d7cc3-124">✔️ 2.1</span></span>        | <span data-ttu-id="d7cc3-125">✔️ [3.1](#rhel-7--net-core-31)</span><span class="sxs-lookup"><span data-stu-id="d7cc3-125">✔️ [3.1](#rhel-7--net-core-31)</span></span>        | <span data-ttu-id="d7cc3-126">✔️ [5.0](#rhel-7--net-50)</span><span class="sxs-lookup"><span data-stu-id="d7cc3-126">✔️ [5.0](#rhel-7--net-50)</span></span> |

<span data-ttu-id="d7cc3-127">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-127">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="d7cc3-128">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="d7cc3-128">The downloads for these still remain published:</span></span>

- <span data-ttu-id="d7cc3-129">3.0</span><span class="sxs-lookup"><span data-stu-id="d7cc3-129">3.0</span></span>
- <span data-ttu-id="d7cc3-130">2.2</span><span class="sxs-lookup"><span data-stu-id="d7cc3-130">2.2</span></span>
- <span data-ttu-id="d7cc3-131">2.0</span><span class="sxs-lookup"><span data-stu-id="d7cc3-131">2.0</span></span>

## <a name="remove-preview-versions"></a><span data-ttu-id="d7cc3-132">删除预览版本</span><span class="sxs-lookup"><span data-stu-id="d7cc3-132">Remove preview versions</span></span>

[!INCLUDE [package-manager uninstall notice](./includes/linux-uninstall-preview-info.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="d7cc3-133">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="d7cc3-133">How to install other versions</span></span>

<span data-ttu-id="d7cc3-134">有关安装其他版本的 .NET 所需的步骤，请参阅[适用于 .NET 的 Red Hat 文档](https://access.redhat.com/documentation/net/5.0/)。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-134">Consult the [Red Hat documentation for .NET](https://access.redhat.com/documentation/net/5.0/) on the steps required to install other releases of .NET.</span></span>

## <a name="rhel-8-"></a><span data-ttu-id="d7cc3-135">RHEL 8 ✔️</span><span class="sxs-lookup"><span data-stu-id="d7cc3-135">RHEL 8 ✔️</span></span>

<span data-ttu-id="d7cc3-136">.NET 包含在 RHEL 8 的 AppStream 存储库中。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-136">.NET is included in the AppStream repositories for RHEL 8.</span></span>

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="rhel-7--net-50"></a><span data-ttu-id="d7cc3-137">RHEL 7 ✔️ .NET 5.0</span><span class="sxs-lookup"><span data-stu-id="d7cc3-137">RHEL 7 ✔️ .NET 5.0</span></span>

<span data-ttu-id="d7cc3-138">以下命令安装 `scl-utils` 包：</span><span class="sxs-lookup"><span data-stu-id="d7cc3-138">The following command installs the `scl-utils` package:</span></span>

```bash
sudo yum install scl-utils
```

### <a name="install-the-sdk"></a><span data-ttu-id="d7cc3-139">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="d7cc3-139">Install the SDK</span></span>

<span data-ttu-id="d7cc3-140">.NET SDK 使你可以通过 .NET 开发应用。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-140">The .NET SDK allows you to develop apps with .NET .</span></span> <span data-ttu-id="d7cc3-141">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-141">If you install the .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="d7cc3-142">若要安装 .NET SDK，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d7cc3-142">To install .NET SDK, run the following commands:</span></span>

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet50 -y
scl enable rh-dotnet50 bash
```

<span data-ttu-id="d7cc3-143">Red Hat 建议不要永久启用 `rh-dotnet50`，因为这可能会影响其他程序。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-143">Red Hat does not recommend permanently enabling `rh-dotnet50` because it may affect other programs.</span></span> <span data-ttu-id="d7cc3-144">如果要永久启用 `rh-dotnet`，请将以下行添加到 ~/.bashrc 文件中。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-144">If you want to enable `rh-dotnet` permanently, add the following line to your _~/.bashrc_ file.</span></span>

```bash
source scl_source enable rh-dotnet50
```

### <a name="install-the-runtime"></a><span data-ttu-id="d7cc3-145">安装运行时</span><span class="sxs-lookup"><span data-stu-id="d7cc3-145">Install the runtime</span></span>

<span data-ttu-id="d7cc3-146">通过 .NET 运行时，可以运行使用 .NET 开发且未包含运行时的应用。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-146">The .NET Runtime allows you to run apps that were made with .NET that didn't include the runtime.</span></span> <span data-ttu-id="d7cc3-147">以下命令安装 ASP.NET Core 运行时，这是与 .NET Core 最兼容的运行时。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-147">The commands below install the ASP.NET Core Runtime, which is the most compatible runtime for .NET Core.</span></span> <span data-ttu-id="d7cc3-148">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-148">In your terminal, run the following commands.</span></span>

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet50-aspnetcore-runtime-5.0 -y
scl enable rh-dotnet50 bash
```

<span data-ttu-id="d7cc3-149">Red Hat 建议不要永久启用 `rh-dotnet50`，因为这可能会影响其他程序。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-149">Red Hat does not recommend permanently enabling `rh-dotnet50` because it may affect other programs.</span></span> <span data-ttu-id="d7cc3-150">如果要永久启用 `rh-dotnet50`，请将以下行添加到 ~/.bashrc 文件中。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-150">If you want to enable `rh-dotnet50` permanently, add the following line to your _~/.bashrc_ file.</span></span>

```bash
source scl_source enable rh-dotnet50
```

<span data-ttu-id="d7cc3-151">作为 ASP.NET Core 运行时的一种替代方法，你可以安装不包含 ASP.NET Core 支持的 .NET 运行时：将上述命令中的 `rh-dotnet50-aspnetcore-runtime-5.0` 替换为 `rh-dotnet50-dotnet-runtime-5.0`。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-151">As an alternative to the ASP.NET Core Runtime, you can install the .NET Runtime that doesn't include ASP.NET Core support: replace `rh-dotnet50-aspnetcore-runtime-5.0` in the commands above with `rh-dotnet50-dotnet-runtime-5.0`.</span></span>

## <a name="rhel-7--net-core-31"></a><span data-ttu-id="d7cc3-152">RHEL 7 ✔️ .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="d7cc3-152">RHEL 7 ✔️ .NET Core 3.1</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

<span data-ttu-id="d7cc3-153">以下命令安装 `scl-utils` 包：</span><span class="sxs-lookup"><span data-stu-id="d7cc3-153">The following command installs the `scl-utils` package:</span></span>

```bash
sudo yum install scl-utils
```

### <a name="install-the-sdk"></a><span data-ttu-id="d7cc3-154">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="d7cc3-154">Install the SDK</span></span>

<span data-ttu-id="d7cc3-155">.NET Core SDK 使你可以通过 .NET Core 开发应用。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-155">.NET Core SDK allows you to develop apps with .NET Core.</span></span> <span data-ttu-id="d7cc3-156">如果安装 .NET Core SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-156">If you install .NET Core SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="d7cc3-157">若要安装 .NET Core SDK，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d7cc3-157">To install .NET Core SDK, run the following commands:</span></span>

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31 -y
scl enable rh-dotnet31 bash
```

<span data-ttu-id="d7cc3-158">Red Hat 建议不要永久启用 `rh-dotnet31`，因为这可能会影响其他程序。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-158">Red Hat does not recommend permanently enabling `rh-dotnet31` because it may affect other programs.</span></span> <span data-ttu-id="d7cc3-159">例如，`rh-dotnet31` 包括与基本 RHEL 版本不同的 `libcurl` 版本。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-159">For example, `rh-dotnet31` includes a version of `libcurl` that differs from the base RHEL version.</span></span> <span data-ttu-id="d7cc3-160">这可能会导致不需要不同版本的 `libcurl` 的程序出现问题。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-160">This may lead to issues in programs that do not expect a different version of `libcurl`.</span></span> <span data-ttu-id="d7cc3-161">如果要永久启用 `rh-dotnet`，请将以下行添加到 ~/.bashrc 文件中。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-161">If you want to enable `rh-dotnet` permanently, add the following line to your _~/.bashrc_ file.</span></span>

```bash
source scl_source enable rh-dotnet31
```

### <a name="install-the-runtime"></a><span data-ttu-id="d7cc3-162">安装运行时</span><span class="sxs-lookup"><span data-stu-id="d7cc3-162">Install the runtime</span></span>

<span data-ttu-id="d7cc3-163">.NET Core 运行时允许运行使用不随附运行时的 .NET Core 所开发的应用。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-163">The .NET Core Runtime allows you to run apps that were made with .NET Core that didn't include the runtime.</span></span> <span data-ttu-id="d7cc3-164">以下命令安装 ASP.NET Core 运行时，这是与 .NET Core 最兼容的运行时。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-164">The commands below install the ASP.NET Core Runtime, which is the most compatible runtime for .NET Core.</span></span> <span data-ttu-id="d7cc3-165">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-165">In your terminal, run the following commands.</span></span>

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31-aspnetcore-runtime-3.1 -y
scl enable rh-dotnet31 bash
```

<span data-ttu-id="d7cc3-166">Red Hat 建议不要永久启用 `rh-dotnet31`，因为这可能会影响其他程序。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-166">Red Hat does not recommend permanently enabling `rh-dotnet31` because it may affect other programs.</span></span> <span data-ttu-id="d7cc3-167">例如，`rh-dotnet31` 包括与基本 RHEL 版本不同的 `libcurl` 版本。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-167">For example, `rh-dotnet31` includes a version of `libcurl` that differs from the base RHEL version.</span></span> <span data-ttu-id="d7cc3-168">这可能会导致不需要不同版本的 `libcurl` 的程序出现问题。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-168">This may lead to issues in programs that do not expect a different version of `libcurl`.</span></span> <span data-ttu-id="d7cc3-169">如果要永久启用 `rh-dotnet31`，请将以下行添加到 ~/.bashrc 文件中。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-169">If you want to enable `rh-dotnet31` permanently, add the following line to your _~/.bashrc_ file.</span></span>

```bash
source scl_source enable rh-dotnet31
```

<span data-ttu-id="d7cc3-170">作为 ASP.NET Core 运行时的一种替代方法，你可以安装不包含 ASP.NET Core 支持的 .NET Core 运行时：将上述命令中的 `rh-dotnet31-aspnetcore-runtime-3.1` 替换为 `rh-dotnet31-dotnet-runtime-3.1`。</span><span class="sxs-lookup"><span data-stu-id="d7cc3-170">As an alternative to the ASP.NET Core Runtime, you can install the .NET Core Runtime that doesn't include ASP.NET Core support: replace `rh-dotnet31-aspnetcore-runtime-3.1` in the commands above with `rh-dotnet31-dotnet-runtime-3.1`.</span></span>

## <a name="snap"></a><span data-ttu-id="d7cc3-171">Snap</span><span class="sxs-lookup"><span data-stu-id="d7cc3-171">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="d7cc3-172">依赖项</span><span class="sxs-lookup"><span data-stu-id="d7cc3-172">Dependencies</span></span>

[!INCLUDE [linux-rpm-install-dependencies](includes/linux-rpm-install-dependencies.md)]

## <a name="scripted-install"></a><span data-ttu-id="d7cc3-173">脚本安装</span><span class="sxs-lookup"><span data-stu-id="d7cc3-173">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="d7cc3-174">手动安装</span><span class="sxs-lookup"><span data-stu-id="d7cc3-174">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="d7cc3-175">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d7cc3-175">Next steps</span></span>

- [<span data-ttu-id="d7cc3-176">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="d7cc3-176">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)

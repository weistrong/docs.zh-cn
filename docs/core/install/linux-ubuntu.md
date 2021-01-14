---
title: 在 Ubuntu 上安装 .NET - .NET
description: 演示在 Ubuntu 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 01/06/2021
ms.openlocfilehash: 14e5e9548d4aa09a586e2038f3e35a489ee65cd2
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970756"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-ubuntu"></a><span data-ttu-id="1af15-103">在 Ubuntu 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="1af15-103">Install the .NET SDK or the .NET Runtime on Ubuntu</span></span>

<span data-ttu-id="1af15-104">Ubuntu 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="1af15-104">.NET is supported on Ubuntu.</span></span> <span data-ttu-id="1af15-105">本文介绍如何在 Ubuntu 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="1af15-105">This article describes how to install .NET on Ubuntu.</span></span> <span data-ttu-id="1af15-106">如果 Ubuntu 版本不受支持，则该版本不再支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="1af15-106">When an Ubuntu version falls out of support, .NET is no longer supported with that version.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="1af15-107">支持的分发</span><span class="sxs-lookup"><span data-stu-id="1af15-107">Supported distributions</span></span>

<span data-ttu-id="1af15-108">下表列出了当前支持的 .NET 版本以及支持它们的 Ubuntu 版本。</span><span class="sxs-lookup"><span data-stu-id="1af15-108">The following table is a list of currently supported .NET releases and the versions of Ubuntu they're supported on.</span></span> <span data-ttu-id="1af15-109">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Ubuntu 的版本达到生命周期](https://wiki.ubuntu.com/Releases)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="1af15-109">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Ubuntu reaches end-of-life](https://wiki.ubuntu.com/Releases).</span></span>

- <span data-ttu-id="1af15-110">✔️ 指示 Ubuntu 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="1af15-110">A ✔️ indicates that the version of Ubuntu or .NET is still supported.</span></span>
- <span data-ttu-id="1af15-111">❌ 指示 Ubuntu 或 .NET 版本在该 Ubuntu 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="1af15-111">A ❌ indicates that the version of Ubuntu or .NET isn't supported on that Ubuntu release.</span></span>
- <span data-ttu-id="1af15-112">当 Ubuntu 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="1af15-112">When both a version of Ubuntu and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="1af15-113">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="1af15-113">Ubuntu</span></span>                   | <span data-ttu-id="1af15-114">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-114">.NET Core 2.1</span></span> | <span data-ttu-id="1af15-115">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-115">.NET Core 3.1</span></span> | <span data-ttu-id="1af15-116">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-116">.NET 5.0</span></span> |
|--------------------------|---------------|---------------|----------------|
| <span data-ttu-id="1af15-117">✔️ [20.10](#2010-)</span><span class="sxs-lookup"><span data-stu-id="1af15-117">✔️ [20.10](#2010-)</span></span>       | <span data-ttu-id="1af15-118">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-118">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-119">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-119">✔️ 3.1</span></span>        | <span data-ttu-id="1af15-120">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-120">✔️ 5.0</span></span> |
| <span data-ttu-id="1af15-121">✔️ [20.04 (LTS)](#2004-)</span><span class="sxs-lookup"><span data-stu-id="1af15-121">✔️ [20.04 (LTS)](#2004-)</span></span> | <span data-ttu-id="1af15-122">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-122">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-123">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-123">✔️ 3.1</span></span>        | <span data-ttu-id="1af15-124">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-124">✔️ 5.0</span></span> |
| <span data-ttu-id="1af15-125">❌ [19.10](#1910-)</span><span class="sxs-lookup"><span data-stu-id="1af15-125">❌ [19.10](#1910-)</span></span>       | <span data-ttu-id="1af15-126">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-126">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-127">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-127">✔️ 3.1</span></span>        | <span data-ttu-id="1af15-128">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-128">✔️ 5.0</span></span> |
| <span data-ttu-id="1af15-129">❌ [19.04](#1904-)</span><span class="sxs-lookup"><span data-stu-id="1af15-129">❌ [19.04](#1904-)</span></span>       | <span data-ttu-id="1af15-130">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-130">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-131">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-131">✔️ 3.1</span></span>        | <span data-ttu-id="1af15-132">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-132">❌ 5.0</span></span> |
| <span data-ttu-id="1af15-133">❌ [18.10](#1810-)</span><span class="sxs-lookup"><span data-stu-id="1af15-133">❌ [18.10](#1810-)</span></span>       | <span data-ttu-id="1af15-134">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-134">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-135">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-135">❌ 3.1</span></span>        | <span data-ttu-id="1af15-136">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-136">❌ 5.0</span></span> |
| <span data-ttu-id="1af15-137">✔️ [18.04 (LTS)](#1804-)</span><span class="sxs-lookup"><span data-stu-id="1af15-137">✔️ [18.04 (LTS)](#1804-)</span></span> | <span data-ttu-id="1af15-138">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-138">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-139">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-139">✔️ 3.1</span></span>        | <span data-ttu-id="1af15-140">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-140">✔️ 5.0</span></span> |
| <span data-ttu-id="1af15-141">❌ [17.10](#1710-)</span><span class="sxs-lookup"><span data-stu-id="1af15-141">❌ [17.10](#1710-)</span></span>       | <span data-ttu-id="1af15-142">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-142">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-143">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-143">❌ 3.1</span></span>        | <span data-ttu-id="1af15-144">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-144">❌ 5.0</span></span> |
| <span data-ttu-id="1af15-145">❌ [17.04](#1704-)</span><span class="sxs-lookup"><span data-stu-id="1af15-145">❌ [17.04](#1704-)</span></span>       | <span data-ttu-id="1af15-146">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-146">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-147">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-147">❌ 3.1</span></span>        | <span data-ttu-id="1af15-148">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-148">❌ 5.0</span></span> |
| <span data-ttu-id="1af15-149">❌ [16.10](#1610-)</span><span class="sxs-lookup"><span data-stu-id="1af15-149">❌ [16.10](#1610-)</span></span>       | <span data-ttu-id="1af15-150">❌ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-150">❌ 2.1</span></span>        | <span data-ttu-id="1af15-151">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-151">❌ 3.1</span></span>        | <span data-ttu-id="1af15-152">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-152">❌ 5.0</span></span> |
| <span data-ttu-id="1af15-153">✔️ [16.04 (LTS)](#1604-)</span><span class="sxs-lookup"><span data-stu-id="1af15-153">✔️ [16.04 (LTS)](#1604-)</span></span> | <span data-ttu-id="1af15-154">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="1af15-154">✔️ 2.1</span></span>        | <span data-ttu-id="1af15-155">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="1af15-155">✔️ 3.1</span></span>        | <span data-ttu-id="1af15-156">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="1af15-156">✔️ 5.0</span></span> |

<span data-ttu-id="1af15-157">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="1af15-157">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="1af15-158">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="1af15-158">The downloads for these still remain published:</span></span>

- <span data-ttu-id="1af15-159">3.0</span><span class="sxs-lookup"><span data-stu-id="1af15-159">3.0</span></span>
- <span data-ttu-id="1af15-160">2.2</span><span class="sxs-lookup"><span data-stu-id="1af15-160">2.2</span></span>
- <span data-ttu-id="1af15-161">2.0</span><span class="sxs-lookup"><span data-stu-id="1af15-161">2.0</span></span>

## <a name="remove-preview-versions"></a><span data-ttu-id="1af15-162">删除预览版本</span><span class="sxs-lookup"><span data-stu-id="1af15-162">Remove preview versions</span></span>

[!INCLUDE [package-manager uninstall notice](./includes/linux-uninstall-preview-info.md)]

## <a name="2010-"></a><span data-ttu-id="1af15-163">20.10 ✔️</span><span class="sxs-lookup"><span data-stu-id="1af15-163">20.10 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/20.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="2004-"></a><span data-ttu-id="1af15-164">20.04 ✔️</span><span class="sxs-lookup"><span data-stu-id="1af15-164">20.04 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="1910-"></a><span data-ttu-id="1af15-165">19.10 ❌</span><span class="sxs-lookup"><span data-stu-id="1af15-165">19.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/19.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-31](includes/linux-install-31-apt.md)]

## <a name="1904-"></a><span data-ttu-id="1af15-166">19.04 ❌</span><span class="sxs-lookup"><span data-stu-id="1af15-166">19.04 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/19.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-31](includes/linux-install-31-apt.md)]

## <a name="1810-"></a><span data-ttu-id="1af15-167">18.10 ❌</span><span class="sxs-lookup"><span data-stu-id="1af15-167">18.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/18.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1804-"></a><span data-ttu-id="1af15-168">18.04 ✔️</span><span class="sxs-lookup"><span data-stu-id="1af15-168">18.04 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="1710-"></a><span data-ttu-id="1af15-169">17.10 ❌</span><span class="sxs-lookup"><span data-stu-id="1af15-169">17.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/17.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1704-"></a><span data-ttu-id="1af15-170">17.04 ❌</span><span class="sxs-lookup"><span data-stu-id="1af15-170">17.04 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/17.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1610-"></a><span data-ttu-id="1af15-171">16.10 ❌</span><span class="sxs-lookup"><span data-stu-id="1af15-171">16.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/16.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1604-"></a><span data-ttu-id="1af15-172">16.04 ✔️</span><span class="sxs-lookup"><span data-stu-id="1af15-172">16.04 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="1af15-173">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="1af15-173">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="use-apt-to-update-net"></a><span data-ttu-id="1af15-174">使用 APT 更新 .NET</span><span class="sxs-lookup"><span data-stu-id="1af15-174">Use APT to update .NET</span></span>

<span data-ttu-id="1af15-175">当新的修补程序版本适用于 .NET 时，只需使用以下命令通过 APT 进行升级：</span><span class="sxs-lookup"><span data-stu-id="1af15-175">When a new patch release is available for .NET, you can simply upgrade it through APT with the following commands:</span></span>

```bash
sudo apt-get update
sudo apt-get upgrade
```

## <a name="apt-troubleshooting"></a><span data-ttu-id="1af15-176">APT 疑难解答</span><span class="sxs-lookup"><span data-stu-id="1af15-176">APT troubleshooting</span></span>

<span data-ttu-id="1af15-177">本部分提供有关使用 APT 安装 .NET 时可能会遇到的常见错误的信息。</span><span class="sxs-lookup"><span data-stu-id="1af15-177">This section provides information on common errors you may get while using APT to install .NET.</span></span>

### <a name="unable-to-find-package"></a><span data-ttu-id="1af15-178">找不到包</span><span class="sxs-lookup"><span data-stu-id="1af15-178">Unable to find package</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

### <a name="unable-to-locate--some-packages-could-not-be-installed"></a><span data-ttu-id="1af15-179">找不到 \\ 无法安装某些包</span><span class="sxs-lookup"><span data-stu-id="1af15-179">Unable to locate \\ Some packages could not be installed</span></span>

[!INCLUDE [package-manager-failed-to-find-deb](includes/package-manager-failed-to-find-deb.md)]

```bash
sudo apt-get install -y gpg
wget -O - https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor -o microsoft.asc.gpg
sudo mv microsoft.asc.gpg /etc/apt/trusted.gpg.d/
wget https://packages.microsoft.com/config/ubuntu/{os-version}/prod.list
sudo mv prod.list /etc/apt/sources.list.d/microsoft-prod.list
sudo chown root:root /etc/apt/trusted.gpg.d/microsoft.asc.gpg
sudo chown root:root /etc/apt/sources.list.d/microsoft-prod.list
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y {dotnet-package}
```

### <a name="failed-to-fetch"></a><span data-ttu-id="1af15-180">未能提取</span><span class="sxs-lookup"><span data-stu-id="1af15-180">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-deb](includes/package-manager-failed-to-fetch-deb.md)]

## <a name="dependencies"></a><span data-ttu-id="1af15-181">依赖项</span><span class="sxs-lookup"><span data-stu-id="1af15-181">Dependencies</span></span>

<span data-ttu-id="1af15-182">使用包管理器进行安装时，将为你安装这些库。</span><span class="sxs-lookup"><span data-stu-id="1af15-182">When you install with a package manager, these libraries are installed for you.</span></span> <span data-ttu-id="1af15-183">但是，如果手动安装 .NET 或发布自包含的应用，则需要确保已安装以下库：</span><span class="sxs-lookup"><span data-stu-id="1af15-183">But, if you manually install .NET or you publish a self-contained app, you'll need to make sure these libraries are installed:</span></span>

- <span data-ttu-id="1af15-184">libc6</span><span class="sxs-lookup"><span data-stu-id="1af15-184">libc6</span></span>
- <span data-ttu-id="1af15-185">libgcc1</span><span class="sxs-lookup"><span data-stu-id="1af15-185">libgcc1</span></span>
- <span data-ttu-id="1af15-186">libgssapi-krb5-2</span><span class="sxs-lookup"><span data-stu-id="1af15-186">libgssapi-krb5-2</span></span>
- <span data-ttu-id="1af15-187">libicu52（针对 14.x）</span><span class="sxs-lookup"><span data-stu-id="1af15-187">libicu52 (for 14.x)</span></span>
- <span data-ttu-id="1af15-188">libicu55（针对 16.x）</span><span class="sxs-lookup"><span data-stu-id="1af15-188">libicu55 (for 16.x)</span></span>
- <span data-ttu-id="1af15-189">libicu60（针对 18.x）</span><span class="sxs-lookup"><span data-stu-id="1af15-189">libicu60 (for 18.x)</span></span>
- <span data-ttu-id="1af15-190">libicu66（适用于 20. x）</span><span class="sxs-lookup"><span data-stu-id="1af15-190">libicu66 (for 20.x)</span></span>
- <span data-ttu-id="1af15-191">libssl1.0.0（适用于 14.x、16.x）</span><span class="sxs-lookup"><span data-stu-id="1af15-191">libssl1.0.0 (for 14.x, 16.x)</span></span>
- <span data-ttu-id="1af15-192">libssl1.1（适用于18.x、20.x）</span><span class="sxs-lookup"><span data-stu-id="1af15-192">libssl1.1 (for 18.x, 20.x)</span></span>
- <span data-ttu-id="1af15-193">libstdc++6</span><span class="sxs-lookup"><span data-stu-id="1af15-193">libstdc++6</span></span>
- <span data-ttu-id="1af15-194">zlib1g</span><span class="sxs-lookup"><span data-stu-id="1af15-194">zlib1g</span></span>

<span data-ttu-id="1af15-195">对于使用 System.Drawing.Common 程序集的 .NET 应用，还需要以下依赖项：</span><span class="sxs-lookup"><span data-stu-id="1af15-195">For .NET apps that use the *System.Drawing.Common* assembly, you also need the following dependency:</span></span>

- <span data-ttu-id="1af15-196">libgdiplus（版本 6.0.1 或更高版本）</span><span class="sxs-lookup"><span data-stu-id="1af15-196">libgdiplus (version 6.0.1 or later)</span></span>

  > [!WARNING]
  > <span data-ttu-id="1af15-197">可以通过将 Mono 存储库添加到系统来安装最新版 libgdiplus。</span><span class="sxs-lookup"><span data-stu-id="1af15-197">You can install a recent version of *libgdiplus* by adding the Mono repository to your system.</span></span> <span data-ttu-id="1af15-198">有关详细信息，请参阅 <https://www.mono-project.com/download/stable/>。</span><span class="sxs-lookup"><span data-stu-id="1af15-198">For more information, see <https://www.mono-project.com/download/stable/>.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1af15-199">后续步骤</span><span class="sxs-lookup"><span data-stu-id="1af15-199">Next steps</span></span>

- [<span data-ttu-id="1af15-200">如何为 .NET CLI 启用 Tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="1af15-200">How to enable TAB completion for the .NET CLI</span></span>](../tools/enable-tab-autocomplete.md)
- [<span data-ttu-id="1af15-201">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="1af15-201">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)

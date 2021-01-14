---
title: 在 Alpine 上安装 .NET - .NET
description: 演示在 Alpine 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 01/06/2021
ms.openlocfilehash: 6adaa905c400b45526ebbc3d8e2606522863eec3
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970845"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-alpine"></a><span data-ttu-id="11631-103">在 Alpine 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="11631-103">Install the .NET SDK or the .NET Runtime on Alpine</span></span>

<span data-ttu-id="11631-104">本文介绍如何在 Alpine 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="11631-104">This article describes how to install .NET on Alpine.</span></span> <span data-ttu-id="11631-105">如果 Alpine 版本不再受到支持，则该版本不再支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="11631-105">When an Alpine version falls out of support, .NET is no longer supported with that version.</span></span> <span data-ttu-id="11631-106">不过，可以按照这些说明在这些版本上运行 .NET，即使它不受支持。</span><span class="sxs-lookup"><span data-stu-id="11631-106">However, these instructions may help you to get .NET running on those versions, even though it isn't supported.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

## <a name="install"></a><span data-ttu-id="11631-107">安装</span><span class="sxs-lookup"><span data-stu-id="11631-107">Install</span></span>

<span data-ttu-id="11631-108">安装程序不可用于 Alpine Linux。</span><span class="sxs-lookup"><span data-stu-id="11631-108">Installers aren't available for Alpine Linux.</span></span> <span data-ttu-id="11631-109">必须使用以下方式之一安装 .NET：</span><span class="sxs-lookup"><span data-stu-id="11631-109">You must install .NET in one of the following ways:</span></span>

- [<span data-ttu-id="11631-110">Snap 包</span><span class="sxs-lookup"><span data-stu-id="11631-110">Snap package</span></span>](linux-snap.md)
- [<span data-ttu-id="11631-111">使用 install-dotnet.sh 脚本安装</span><span class="sxs-lookup"><span data-stu-id="11631-111">Scripted install with _install-dotnet.sh_</span></span>](linux-scripted-manual.md#scripted-install)
- [<span data-ttu-id="11631-112">手动提取二进制文件</span><span class="sxs-lookup"><span data-stu-id="11631-112">Manual binary extraction</span></span>](linux-scripted-manual.md#manual-install)

## <a name="supported-distributions"></a><span data-ttu-id="11631-113">支持的发行版</span><span class="sxs-lookup"><span data-stu-id="11631-113">Supported distributions</span></span>

<span data-ttu-id="11631-114">下表列出了当前支持的 .NET 版本以及支持它们的 Alpine 版本。</span><span class="sxs-lookup"><span data-stu-id="11631-114">The following table is a list of currently supported .NET releases and the versions of Alpine they're supported on.</span></span> <span data-ttu-id="11631-115">这些版本在 [.NET 到达支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Alpine 的版本到达有效期](https://wiki.alpinelinux.org/wiki/Alpine_Linux:Releases)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="11631-115">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Alpine reaches end-of-life](https://wiki.alpinelinux.org/wiki/Alpine_Linux:Releases).</span></span>

- <span data-ttu-id="11631-116">✔️ 指示 Alpine 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="11631-116">A ✔️ indicates that the version of Alpine or .NET is still supported.</span></span>
- <span data-ttu-id="11631-117">❌ 指示 Alpine 或 .NET 版本在该 Alpine 发行版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="11631-117">A ❌ indicates that the version of Alpine or .NET isn't supported on that Alpine release.</span></span>
- <span data-ttu-id="11631-118">当 Alpine 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="11631-118">When both a version of Alpine and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="11631-119">Alpine</span><span class="sxs-lookup"><span data-stu-id="11631-119">Alpine</span></span>  | <span data-ttu-id="11631-120">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="11631-120">.NET Core 2.1</span></span> | <span data-ttu-id="11631-121">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="11631-121">.NET Core 3.1</span></span> | <span data-ttu-id="11631-122">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="11631-122">.NET 5.0</span></span> |
|-------- |---------------|---------------|----------------|
| <span data-ttu-id="11631-123">✔️ 3.12</span><span class="sxs-lookup"><span data-stu-id="11631-123">✔️ 3.12</span></span> | <span data-ttu-id="11631-124">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="11631-124">✔️ 2.1</span></span>        | <span data-ttu-id="11631-125">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="11631-125">✔️ 3.1</span></span>        | <span data-ttu-id="11631-126">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="11631-126">✔️ 5.0</span></span> |
| <span data-ttu-id="11631-127">✔️ 3.11</span><span class="sxs-lookup"><span data-stu-id="11631-127">✔️ 3.11</span></span> | <span data-ttu-id="11631-128">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="11631-128">✔️ 2.1</span></span>        | <span data-ttu-id="11631-129">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="11631-129">✔️ 3.1</span></span>        | <span data-ttu-id="11631-130">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="11631-130">✔️ 5.0</span></span> |
| <span data-ttu-id="11631-131">✔️ 3.10</span><span class="sxs-lookup"><span data-stu-id="11631-131">✔️ 3.10</span></span> | <span data-ttu-id="11631-132">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="11631-132">✔️ 2.1</span></span>        | <span data-ttu-id="11631-133">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="11631-133">✔️ 3.1</span></span>        | <span data-ttu-id="11631-134">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="11631-134">❌ 5.0</span></span> |
| <span data-ttu-id="11631-135">❌ 3.9</span><span class="sxs-lookup"><span data-stu-id="11631-135">❌ 3.9</span></span>  | <span data-ttu-id="11631-136">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="11631-136">✔️ 2.1</span></span>        | <span data-ttu-id="11631-137">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="11631-137">✔️ 3.1</span></span>        | <span data-ttu-id="11631-138">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="11631-138">❌ 5.0</span></span> |
| <span data-ttu-id="11631-139">❌ 3.8</span><span class="sxs-lookup"><span data-stu-id="11631-139">❌ 3.8</span></span>  | <span data-ttu-id="11631-140">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="11631-140">✔️ 2.1</span></span>        | <span data-ttu-id="11631-141">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="11631-141">✔️ 3.1</span></span>        | <span data-ttu-id="11631-142">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="11631-142">❌ 5.0</span></span> |

<span data-ttu-id="11631-143">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="11631-143">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="11631-144">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="11631-144">The downloads for these still remain published:</span></span>

- <span data-ttu-id="11631-145">3.0</span><span class="sxs-lookup"><span data-stu-id="11631-145">3.0</span></span>
- <span data-ttu-id="11631-146">2.2</span><span class="sxs-lookup"><span data-stu-id="11631-146">2.2</span></span>
- <span data-ttu-id="11631-147">2.0</span><span class="sxs-lookup"><span data-stu-id="11631-147">2.0</span></span>

## <a name="dependencies"></a><span data-ttu-id="11631-148">依赖项</span><span class="sxs-lookup"><span data-stu-id="11631-148">Dependencies</span></span>

<span data-ttu-id="11631-149">Alpine Linux 上的 .NET 要求安装以下依赖项：</span><span class="sxs-lookup"><span data-stu-id="11631-149">.NET on Alpine Linux requires the following dependencies installed:</span></span>

- <span data-ttu-id="11631-150">icu-libs</span><span class="sxs-lookup"><span data-stu-id="11631-150">icu-libs</span></span>
- <span data-ttu-id="11631-151">krb5-libs</span><span class="sxs-lookup"><span data-stu-id="11631-151">krb5-libs</span></span>
- <span data-ttu-id="11631-152">libgcc</span><span class="sxs-lookup"><span data-stu-id="11631-152">libgcc</span></span>
- <span data-ttu-id="11631-153">libintl</span><span class="sxs-lookup"><span data-stu-id="11631-153">libintl</span></span>
- <span data-ttu-id="11631-154">libssl1.1（Alpine v3.9 或更高版本）</span><span class="sxs-lookup"><span data-stu-id="11631-154">libssl1.1 (Alpine v3.9 or greater)</span></span>
- <span data-ttu-id="11631-155">libssl1.0（Alpine v3.8 或更低版本）</span><span class="sxs-lookup"><span data-stu-id="11631-155">libssl1.0 (Alpine v3.8 or lower)</span></span>
- <span data-ttu-id="11631-156">libstdc++</span><span class="sxs-lookup"><span data-stu-id="11631-156">libstdc++</span></span>
- <span data-ttu-id="11631-157">zlib</span><span class="sxs-lookup"><span data-stu-id="11631-157">zlib</span></span>

## <a name="next-steps"></a><span data-ttu-id="11631-158">后续步骤</span><span class="sxs-lookup"><span data-stu-id="11631-158">Next steps</span></span>

- [<span data-ttu-id="11631-159">如何为 .NET CLI 启用 Tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="11631-159">How to enable TAB completion for the .NET CLI</span></span>](../tools/enable-tab-autocomplete.md)
- [<span data-ttu-id="11631-160">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="11631-160">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)

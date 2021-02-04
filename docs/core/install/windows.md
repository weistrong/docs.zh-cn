---
title: 在 Windows 上安装 .NET
description: 了解可在其上安装 .NET 的 Windows 版本。
author: adegeo
ms.author: adegeo
ms.date: 01/06/2021
ms.openlocfilehash: 33492cc6fa6c64ec3a1d745a4fa0c6cc418f87bd
ms.sourcegitcommit: 8299abfbd5c49b596d61f1e4d09bc6b8ba055b36
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "98898783"
---
# <a name="install-net-on-windows"></a><span data-ttu-id="a527f-103">在 Windows 上安装 .NET</span><span class="sxs-lookup"><span data-stu-id="a527f-103">Install .NET on Windows</span></span>

> [!div class="op_single_selector"]
>
> - [在 Windows 上安装](windows.md)
> - [在 macOS 上安装](macos.md)
> - [在 Linux 上安装](linux.md)

<span data-ttu-id="a527f-107">本文介绍如何在 Windows 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="a527f-107">In this article, you'll learn how to install .NET on Windows.</span></span> <span data-ttu-id="a527f-108">.NET 由运行时和 SDK 组成。</span><span class="sxs-lookup"><span data-stu-id="a527f-108">.NET is made up of the runtime and the SDK.</span></span> <span data-ttu-id="a527f-109">运行时用于运行 .NET 应用，应用可能包含也可能不包含它。</span><span class="sxs-lookup"><span data-stu-id="a527f-109">The runtime is used to run a .NET app and may or may not be included with the app.</span></span> <span data-ttu-id="a527f-110">SDK 用于创建 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="a527f-110">The SDK is used to create .NET apps and libraries.</span></span> <span data-ttu-id="a527f-111">.NET 运行时始终随 SDK 一起安装。</span><span class="sxs-lookup"><span data-stu-id="a527f-111">The .NET runtime is always installed with the SDK.</span></span>

<span data-ttu-id="a527f-112">最新版本的 .NET 是 5.0。</span><span class="sxs-lookup"><span data-stu-id="a527f-112">The latest version of .NET is 5.0.</span></span>

> [!div class="button"]
> [<span data-ttu-id="a527f-113">下载 .NET</span><span class="sxs-lookup"><span data-stu-id="a527f-113">Download .NET</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="supported-releases"></a><span data-ttu-id="a527f-114">支持的版本</span><span class="sxs-lookup"><span data-stu-id="a527f-114">Supported releases</span></span>

<span data-ttu-id="a527f-115">下表列出了当前支持的 .NET 版本以及支持它们的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-115">The following table is a list of currently supported .NET releases and the versions of Windows they're supported on.</span></span> <span data-ttu-id="a527f-116">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Windows 版本达到生命周期](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="a527f-116">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Windows reaches end-of-life](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

<span data-ttu-id="a527f-117">Windows 10 版本终止服务日期按版本分段。</span><span class="sxs-lookup"><span data-stu-id="a527f-117">Windows 10 versions end-of-service dates are segmented by edition.</span></span> <span data-ttu-id="a527f-118">下表中仅考虑家庭版、专业版、专业教育版和专业工作站版。   </span><span class="sxs-lookup"><span data-stu-id="a527f-118">Only **Home**, **Pro**, **Pro Education**, and **Pro for Workstations** editions are considered in the following table.</span></span> <span data-ttu-id="a527f-119">查看 [Windows 生命周期事实表单](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)，了解具体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a527f-119">Check the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet) for specific details.</span></span>

> [!TIP]
> <span data-ttu-id="a527f-120">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-120">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="a527f-121">操作系统</span><span class="sxs-lookup"><span data-stu-id="a527f-121">Operating System</span></span>            | <span data-ttu-id="a527f-122">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a527f-122">.NET Core 2.1</span></span> | <span data-ttu-id="a527f-123">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="a527f-123">.NET Core 3.1</span></span> | <span data-ttu-id="a527f-124">.NET 5</span><span class="sxs-lookup"><span data-stu-id="a527f-124">.NET 5</span></span> |
|-----------------------------|---------------|---------------|--------|
| <span data-ttu-id="a527f-125">Windows 10 版本 20H2</span><span class="sxs-lookup"><span data-stu-id="a527f-125">Windows 10, Version 20H2</span></span>    | <span data-ttu-id="a527f-126">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-126">✔️</span></span>           | <span data-ttu-id="a527f-127">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-127">✔️</span></span>            | <span data-ttu-id="a527f-128">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-128">✔️</span></span>    |
| <span data-ttu-id="a527f-129">Windows 10 版本 2004</span><span class="sxs-lookup"><span data-stu-id="a527f-129">Windows 10, Version 2004</span></span>    | <span data-ttu-id="a527f-130">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-130">✔️</span></span>           | <span data-ttu-id="a527f-131">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-131">✔️</span></span>            | <span data-ttu-id="a527f-132">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-132">✔️</span></span>    |
| <span data-ttu-id="a527f-133">Windows 10 版本 1909</span><span class="sxs-lookup"><span data-stu-id="a527f-133">Windows 10, Version 1909</span></span>    | <span data-ttu-id="a527f-134">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-134">✔️</span></span>           | <span data-ttu-id="a527f-135">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-135">✔️</span></span>            | <span data-ttu-id="a527f-136">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-136">✔️</span></span>    |
| <span data-ttu-id="a527f-137">Windows 10 版本 1903</span><span class="sxs-lookup"><span data-stu-id="a527f-137">Windows 10, Version 1903</span></span>    | <span data-ttu-id="a527f-138">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-138">✔️</span></span>           | <span data-ttu-id="a527f-139">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-139">✔️</span></span>            | <span data-ttu-id="a527f-140">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-140">✔️</span></span>    |
| <span data-ttu-id="a527f-141">Windows 10 版本 1809</span><span class="sxs-lookup"><span data-stu-id="a527f-141">Windows 10, Version 1809</span></span>    | <span data-ttu-id="a527f-142">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-142">✔️</span></span>           | <span data-ttu-id="a527f-143">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-143">✔️</span></span>            | <span data-ttu-id="a527f-144">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-144">✔️</span></span>    |
| <span data-ttu-id="a527f-145"> Windows 10 版本 1803</span><span class="sxs-lookup"><span data-stu-id="a527f-145">Windows 10, Version 1803</span></span>    | <span data-ttu-id="a527f-146">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-146">✔️</span></span>           | <span data-ttu-id="a527f-147">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-147">✔️</span></span>            | <span data-ttu-id="a527f-148">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-148">✔️</span></span>    |
| <span data-ttu-id="a527f-149"> Windows 10 版本 1709</span><span class="sxs-lookup"><span data-stu-id="a527f-149">Windows 10, Version 1709</span></span>    | <span data-ttu-id="a527f-150">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-150">✔️</span></span>           | <span data-ttu-id="a527f-151">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-151">✔️</span></span>            | <span data-ttu-id="a527f-152">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-152">✔️</span></span>    |
| <span data-ttu-id="a527f-153">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="a527f-153">Windows 10, Version 1607</span></span>    | <span data-ttu-id="a527f-154">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-154">✔️</span></span>           | <span data-ttu-id="a527f-155">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-155">✔️</span></span>            | <span data-ttu-id="a527f-156">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-156">✔️</span></span>    |
| <span data-ttu-id="a527f-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-157">Windows 8.1</span></span>                 | <span data-ttu-id="a527f-158">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-158">✔️</span></span>           | <span data-ttu-id="a527f-159">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-159">✔️</span></span>            | <span data-ttu-id="a527f-160">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-160">✔️</span></span>    |
| <span data-ttu-id="a527f-161">Windows 7 SP1 [ESU][esu]</span><span class="sxs-lookup"><span data-stu-id="a527f-161">Windows 7 SP1 [ESU][esu]</span></span>    | <span data-ttu-id="a527f-162">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-162">✔️</span></span>           | <span data-ttu-id="a527f-163">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-163">✔️</span></span>            | <span data-ttu-id="a527f-164">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-164">✔️</span></span>    |
| <span data-ttu-id="a527f-165">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="a527f-165">Windows 10, Version 1607</span></span>    | <span data-ttu-id="a527f-166">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-166">✔️</span></span>           | <span data-ttu-id="a527f-167">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-167">✔️</span></span>            | <span data-ttu-id="a527f-168">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-168">✔️</span></span>    |
| <span data-ttu-id="a527f-169">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="a527f-169">Windows 10, Version 1607</span></span>    | <span data-ttu-id="a527f-170">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-170">✔️</span></span>           | <span data-ttu-id="a527f-171">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-171">✔️</span></span>            | <span data-ttu-id="a527f-172">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-172">✔️</span></span>    |
| <span data-ttu-id="a527f-173">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a527f-173">Windows Server 2012 R2</span></span>      | <span data-ttu-id="a527f-174">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-174">✔️</span></span>           | <span data-ttu-id="a527f-175">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-175">✔️</span></span>            | <span data-ttu-id="a527f-176">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-176">✔️</span></span>    |
| <span data-ttu-id="a527f-177">Windows Server Core 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a527f-177">Windows Server Core 2012 R2</span></span> | <span data-ttu-id="a527f-178">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-178">✔️</span></span>           | <span data-ttu-id="a527f-179">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-179">✔️</span></span>            | <span data-ttu-id="a527f-180">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-180">✔️</span></span>    |
| <span data-ttu-id="a527f-181">Nano Server 版本 1809+</span><span class="sxs-lookup"><span data-stu-id="a527f-181">Nano Server, Version 1809+</span></span>  | <span data-ttu-id="a527f-182">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-182">✔️</span></span>           | <span data-ttu-id="a527f-183">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-183">✔️</span></span>            | <span data-ttu-id="a527f-184">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-184">✔️</span></span>    |
| <span data-ttu-id="a527f-185">Nano Server 版本 1803</span><span class="sxs-lookup"><span data-stu-id="a527f-185">Nano Server, Version 1803</span></span>   | <span data-ttu-id="a527f-186">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-186">✔️</span></span>           | <span data-ttu-id="a527f-187">✔️</span><span class="sxs-lookup"><span data-stu-id="a527f-187">✔️</span></span>            | ❌    |

## <a name="unsupported-releases"></a><span data-ttu-id="a527f-188">不支持的版本</span><span class="sxs-lookup"><span data-stu-id="a527f-188">Unsupported releases</span></span>

<span data-ttu-id="a527f-189">以下 .NET 版本 ❌ 不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="a527f-189">The following versions of .NET are ❌ no longer supported.</span></span> <span data-ttu-id="a527f-190">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="a527f-190">The downloads for these versions still remain published:</span></span>

- <span data-ttu-id="a527f-191">3.0</span><span class="sxs-lookup"><span data-stu-id="a527f-191">3.0</span></span>
- <span data-ttu-id="a527f-192">2.2</span><span class="sxs-lookup"><span data-stu-id="a527f-192">2.2</span></span>
- <span data-ttu-id="a527f-193">2.0</span><span class="sxs-lookup"><span data-stu-id="a527f-193">2.0</span></span>

## <a name="runtime-information"></a><span data-ttu-id="a527f-194">运行时信息</span><span class="sxs-lookup"><span data-stu-id="a527f-194">Runtime information</span></span>

<span data-ttu-id="a527f-195">运行时用于运行使用 .NET 创建的应用。</span><span class="sxs-lookup"><span data-stu-id="a527f-195">The runtime is used to run apps created with .NET.</span></span> <span data-ttu-id="a527f-196">应用作者发布应用时，可以在其应用中包含运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-196">When an app author publishes an app, they can include the runtime with their app.</span></span> <span data-ttu-id="a527f-197">如果作者未包含运行时，则由用户安装运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-197">If they don't include the runtime, it's up to the user to install the runtime.</span></span>

<span data-ttu-id="a527f-198">可以在 Windows 上安装三个不同的运行时：</span><span class="sxs-lookup"><span data-stu-id="a527f-198">There are three different runtimes you can install on Windows:</span></span>

<span data-ttu-id="a527f-199">*ASP.NET Core 运行时*</span><span class="sxs-lookup"><span data-stu-id="a527f-199">*ASP.NET Core runtime*</span></span>\
<span data-ttu-id="a527f-200">运行 ASP.NET Core 应用。</span><span class="sxs-lookup"><span data-stu-id="a527f-200">Runs ASP.NET Core apps.</span></span> <span data-ttu-id="a527f-201">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-201">Includes the .NET runtime.</span></span>

<span data-ttu-id="a527f-202">*桌面运行时*</span><span class="sxs-lookup"><span data-stu-id="a527f-202">*Desktop runtime*</span></span>\
<span data-ttu-id="a527f-203">运行适用于 Windows 的 .NET WPF 和 Windows 窗体桌面应用。</span><span class="sxs-lookup"><span data-stu-id="a527f-203">Runs .NET WPF and Windows Forms desktop apps for Windows.</span></span> <span data-ttu-id="a527f-204">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-204">Includes the .NET runtime.</span></span>

<span data-ttu-id="a527f-205">.NET 运行时</span><span class="sxs-lookup"><span data-stu-id="a527f-205">*.NET runtime*</span></span>\
<span data-ttu-id="a527f-206">此运行时是最简单的运行时，不包括任何其他运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-206">This runtime is the simplest runtime and doesn't include any other runtime.</span></span> <span data-ttu-id="a527f-207">强烈建议同时安装 ASP.NET Core 运行时和桌面运行时，以最大限度地提升与 .NET 应用的兼容性 。</span><span class="sxs-lookup"><span data-stu-id="a527f-207">It's highly recommended that you install both *ASP.NET Core runtime* and *Desktop runtime* for the best compatibility with .NET apps.</span></span>

> [!div class="button"]
> [<span data-ttu-id="a527f-208">下载 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="a527f-208">Download .NET Runtime</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="sdk-information"></a><span data-ttu-id="a527f-209">SDK 信息</span><span class="sxs-lookup"><span data-stu-id="a527f-209">SDK information</span></span>

<span data-ttu-id="a527f-210">SDK 用于生成和发布 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="a527f-210">The SDK is used to build and publish .NET apps and libraries.</span></span> <span data-ttu-id="a527f-211">安装 SDK 会包含三个[运行时](#runtime-information)：ASP.NET Core、桌面和 .NET。</span><span class="sxs-lookup"><span data-stu-id="a527f-211">Installing the SDK includes all three [runtimes](#runtime-information): ASP.NET Core, Desktop, and .NET.</span></span>

## <a name="dependencies"></a><span data-ttu-id="a527f-212">依赖项</span><span class="sxs-lookup"><span data-stu-id="a527f-212">Dependencies</span></span>

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD024 -->

# <a name="net-50"></a>[<span data-ttu-id="a527f-213">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="a527f-213">.NET 5.0</span></span>](#tab/net50)

<span data-ttu-id="a527f-214">.NET 5.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="a527f-214">The following Windows versions are supported with .NET 5.0:</span></span>

> [!NOTE]
> <span data-ttu-id="a527f-215">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-215">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="a527f-216">(OS)</span><span class="sxs-lookup"><span data-stu-id="a527f-216">OS</span></span>                  | <span data-ttu-id="a527f-217">Version</span><span class="sxs-lookup"><span data-stu-id="a527f-217">Version</span></span>       | <span data-ttu-id="a527f-218">体系结构</span><span class="sxs-lookup"><span data-stu-id="a527f-218">Architectures</span></span>   |
|---------------------|---------------|-----------------|
| <span data-ttu-id="a527f-219">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-219">Windows 10 Client</span></span>   | <span data-ttu-id="a527f-220">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="a527f-220">Version 1607+</span></span> | <span data-ttu-id="a527f-221">x64、x86、ARM64</span><span class="sxs-lookup"><span data-stu-id="a527f-221">x64, x86, ARM64</span></span> |
| <span data-ttu-id="a527f-222">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-222">Windows Client</span></span>      | <span data-ttu-id="a527f-223">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-223">7 SP1+, 8.1</span></span>   | <span data-ttu-id="a527f-224">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-224">x64, x86</span></span>        |
| <span data-ttu-id="a527f-225">Windows Server</span><span class="sxs-lookup"><span data-stu-id="a527f-225">Windows Server</span></span>      | <span data-ttu-id="a527f-226">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="a527f-226">2012 R2+</span></span>      | <span data-ttu-id="a527f-227">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-227">x64, x86</span></span>        |
| <span data-ttu-id="a527f-228">Windows Server 核心</span><span class="sxs-lookup"><span data-stu-id="a527f-228">Windows Server Core</span></span> | <span data-ttu-id="a527f-229">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="a527f-229">2012 R2+</span></span>      | <span data-ttu-id="a527f-230">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-230">x64, x86</span></span>        |
| <span data-ttu-id="a527f-231">Nano Server</span><span class="sxs-lookup"><span data-stu-id="a527f-231">Nano Server</span></span>         | <span data-ttu-id="a527f-232">版本 1809+</span><span class="sxs-lookup"><span data-stu-id="a527f-232">Version 1809+</span></span> | <span data-ttu-id="a527f-233">X64</span><span class="sxs-lookup"><span data-stu-id="a527f-233">x64</span></span>             |

<span data-ttu-id="a527f-234">有关 .NET 5.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET 5.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-234">For more information about .NET 5.0 supported operating systems, distributions, and lifecycle policy, see [.NET 5.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md).</span></span>

# <a name="net-core-31"></a>[<span data-ttu-id="a527f-235">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="a527f-235">.NET Core 3.1</span></span>](#tab/netcore31)

<span data-ttu-id="a527f-236">.NET Core 3.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="a527f-236">The following Windows versions are supported with .NET Core 3.1:</span></span>

> [!NOTE]
> <span data-ttu-id="a527f-237">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-237">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="a527f-238">(OS)</span><span class="sxs-lookup"><span data-stu-id="a527f-238">OS</span></span>                            | <span data-ttu-id="a527f-239">Version</span><span class="sxs-lookup"><span data-stu-id="a527f-239">Version</span></span>                        | <span data-ttu-id="a527f-240">体系结构</span><span class="sxs-lookup"><span data-stu-id="a527f-240">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="a527f-241">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-241">Windows Client</span></span>                | <span data-ttu-id="a527f-242">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-242">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="a527f-243">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-243">x64, x86</span></span>        |
| <span data-ttu-id="a527f-244">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-244">Windows 10 Client</span></span>             | <span data-ttu-id="a527f-245">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="a527f-245">Version 1607+</span></span>                  | <span data-ttu-id="a527f-246">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-246">x64, x86</span></span>        |
| <span data-ttu-id="a527f-247">Windows Server</span><span class="sxs-lookup"><span data-stu-id="a527f-247">Windows Server</span></span>                | <span data-ttu-id="a527f-248">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="a527f-248">2012 R2+</span></span>                       | <span data-ttu-id="a527f-249">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-249">x64, x86</span></span>        |
| <span data-ttu-id="a527f-250">Nano Server</span><span class="sxs-lookup"><span data-stu-id="a527f-250">Nano Server</span></span>                   | <span data-ttu-id="a527f-251">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="a527f-251">Version 1803+</span></span>                  | <span data-ttu-id="a527f-252">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="a527f-252">x64, ARM32</span></span>      |

<span data-ttu-id="a527f-253">有关 .NET Core 3.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-253">For more information about .NET Core 3.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md).</span></span>

# <a name="net-core-30"></a>[<span data-ttu-id="a527f-254">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="a527f-254">.NET Core 3.0</span></span>](#tab/netcore30)

<span data-ttu-id="a527f-255">目前不 ❌ 支持 .NET Core 3.0 *。* 有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="a527f-255">*.NET Core 3.0 is currently ❌ out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="a527f-256">.NET Core 3.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="a527f-256">The following Windows versions are supported with .NET Core 3.0:</span></span>

> [!NOTE]
> <span data-ttu-id="a527f-257">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-257">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="a527f-258">(OS)</span><span class="sxs-lookup"><span data-stu-id="a527f-258">OS</span></span>                            | <span data-ttu-id="a527f-259">Version</span><span class="sxs-lookup"><span data-stu-id="a527f-259">Version</span></span>                        | <span data-ttu-id="a527f-260">体系结构</span><span class="sxs-lookup"><span data-stu-id="a527f-260">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="a527f-261">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-261">Windows Client</span></span>                | <span data-ttu-id="a527f-262">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-262">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="a527f-263">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-263">x64, x86</span></span>        |
| <span data-ttu-id="a527f-264">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-264">Windows 10 Client</span></span>             | <span data-ttu-id="a527f-265">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="a527f-265">Version 1607+</span></span>                  | <span data-ttu-id="a527f-266">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-266">x64, x86</span></span>        |
| <span data-ttu-id="a527f-267">Windows Server</span><span class="sxs-lookup"><span data-stu-id="a527f-267">Windows Server</span></span>                | <span data-ttu-id="a527f-268">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="a527f-268">2012 R2+</span></span>                       | <span data-ttu-id="a527f-269">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-269">x64, x86</span></span>        |
| <span data-ttu-id="a527f-270">Nano Server</span><span class="sxs-lookup"><span data-stu-id="a527f-270">Nano Server</span></span>                   | <span data-ttu-id="a527f-271">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="a527f-271">Version 1803+</span></span>                  | <span data-ttu-id="a527f-272">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="a527f-272">x64, ARM32</span></span>      |

<span data-ttu-id="a527f-273">有关 .NET Core 3.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-273">For more information about .NET Core 3.0 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md).</span></span>

# <a name="net-core-22"></a>[<span data-ttu-id="a527f-274">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="a527f-274">.NET Core 2.2</span></span>](#tab/netcore22)

<span data-ttu-id="a527f-275">目前不 ❌ 支持 .NET Core 2.2。有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="a527f-275">*.NET Core 2.2 is currently ❌ out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="a527f-276">.NET Core 2.2 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="a527f-276">The following Windows versions are supported with .NET Core 2.2:</span></span>

> [!NOTE]
> <span data-ttu-id="a527f-277">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-277">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="a527f-278">(OS)</span><span class="sxs-lookup"><span data-stu-id="a527f-278">OS</span></span>                            | <span data-ttu-id="a527f-279">Version</span><span class="sxs-lookup"><span data-stu-id="a527f-279">Version</span></span>                        | <span data-ttu-id="a527f-280">体系结构</span><span class="sxs-lookup"><span data-stu-id="a527f-280">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="a527f-281">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-281">Windows Client</span></span>                | <span data-ttu-id="a527f-282">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-282">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="a527f-283">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-283">x64, x86</span></span>        |
| <span data-ttu-id="a527f-284">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-284">Windows 10 Client</span></span>             | <span data-ttu-id="a527f-285">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="a527f-285">Version 1607+</span></span>                  | <span data-ttu-id="a527f-286">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-286">x64, x86</span></span>        |
| <span data-ttu-id="a527f-287">Windows Server</span><span class="sxs-lookup"><span data-stu-id="a527f-287">Windows Server</span></span>                | <span data-ttu-id="a527f-288">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="a527f-288">2008 R2 SP1+</span></span>                   | <span data-ttu-id="a527f-289">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-289">x64, x86</span></span>        |
| <span data-ttu-id="a527f-290">Nano Server</span><span class="sxs-lookup"><span data-stu-id="a527f-290">Nano Server</span></span>                   | <span data-ttu-id="a527f-291">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="a527f-291">Version 1803+</span></span>                   | <span data-ttu-id="a527f-292">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="a527f-292">x64, ARM32</span></span>      |

<span data-ttu-id="a527f-293">有关 .NET Core 2.2 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.2 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-293">For more information about .NET Core 2.2 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.2 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md).</span></span>

# <a name="net-core-21"></a>[<span data-ttu-id="a527f-294">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a527f-294">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="a527f-295">.NET Core 2.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="a527f-295">The following Windows versions are supported with .NET Core 2.1:</span></span>

> [!NOTE]
> <span data-ttu-id="a527f-296">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-296">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="a527f-297">(OS)</span><span class="sxs-lookup"><span data-stu-id="a527f-297">OS</span></span>                            | <span data-ttu-id="a527f-298">Version</span><span class="sxs-lookup"><span data-stu-id="a527f-298">Version</span></span>                        | <span data-ttu-id="a527f-299">体系结构</span><span class="sxs-lookup"><span data-stu-id="a527f-299">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="a527f-300">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-300">Windows Client</span></span>                | <span data-ttu-id="a527f-301">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-301">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="a527f-302">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-302">x64, x86</span></span>        |
| <span data-ttu-id="a527f-303">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="a527f-303">Windows 10 Client</span></span>             | <span data-ttu-id="a527f-304">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="a527f-304">Version 1607+</span></span>                  | <span data-ttu-id="a527f-305">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-305">x64, x86</span></span>        |
| <span data-ttu-id="a527f-306">Windows Server</span><span class="sxs-lookup"><span data-stu-id="a527f-306">Windows Server</span></span>                | <span data-ttu-id="a527f-307">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="a527f-307">2008 R2 SP1+</span></span>                   | <span data-ttu-id="a527f-308">x64、x86</span><span class="sxs-lookup"><span data-stu-id="a527f-308">x64, x86</span></span>        |
| <span data-ttu-id="a527f-309">Nano Server</span><span class="sxs-lookup"><span data-stu-id="a527f-309">Nano Server</span></span>                   | <span data-ttu-id="a527f-310">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="a527f-310">Version 1803+</span></span>                  | <span data-ttu-id="a527f-311">x64</span><span class="sxs-lookup"><span data-stu-id="a527f-311">x64,</span></span>            |

<span data-ttu-id="a527f-312">有关 .NET Core 2.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-312">For more information about .NET Core 2.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md).</span></span>

### <a name="offline-install-for-windows-7"></a><span data-ttu-id="a527f-313">Windows 7 的脱机安装</span><span class="sxs-lookup"><span data-stu-id="a527f-313">Offline install for Windows 7</span></span>

<span data-ttu-id="a527f-314">在 Windows 7 上执行 .NET Core 2.1 的脱机安装时，首先需要确保目标计算机上已安装最新的 [Microsoft 根证书颁发机构 2011](https://www.microsoft.com/pkiops/Docs/Repository.htm)。</span><span class="sxs-lookup"><span data-stu-id="a527f-314">When doing an offline install for .NET Core 2.1 on Windows 7, you'll first need to make sure that the latest [Microsoft Root Certificate Authority 2011](https://www.microsoft.com/pkiops/Docs/Repository.htm) has been installed on the target machine.</span></span>

<span data-ttu-id="a527f-315">certmgr.exe 工具可以自动安装证书，并从 Visual Studio 或 Windows SDK 获取该证书。</span><span class="sxs-lookup"><span data-stu-id="a527f-315">The _certmgr.exe_ tool can automate installing a certificate and is obtained from Visual Studio or the Windows SDK.</span></span> <span data-ttu-id="a527f-316">以下命令用于在运行 .NET Core 2.1 安装程序之前安装证书：</span><span class="sxs-lookup"><span data-stu-id="a527f-316">The following command is used to install the certificate before running the .NET Core 2.1 installer:</span></span>

```console
certmgr.exe /add MicRooCerAut2011_2011_03_22.crt /s /r localMachine root
```

<span data-ttu-id="a527f-317">请务必查看[下面 Windows 7](#additional-deps) 所需的依赖项。</span><span class="sxs-lookup"><span data-stu-id="a527f-317">Be sure to review the dependencies required for [Windows 7 below](#additional-deps).</span></span>

---

<!-- markdownlint-disable MD001 -->

### <a name="windows-7--vista--81--server-2008-r2--server-2012-r2"></a><a name="additional-deps"></a> <span data-ttu-id="a527f-318">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a527f-318">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span></span>

<span data-ttu-id="a527f-319">如果要在以下 Windows 版本上安装 .NET SDK 或运行时，则需要其他依赖项：</span><span class="sxs-lookup"><span data-stu-id="a527f-319">More dependencies are required if you're installing the .NET SDK or runtime on the following Windows versions:</span></span>

| <span data-ttu-id="a527f-320">操作系统</span><span class="sxs-lookup"><span data-stu-id="a527f-320">Operating System</span></span>         | <span data-ttu-id="a527f-321">先决条件</span><span class="sxs-lookup"><span data-stu-id="a527f-321">Prerequisites</span></span>                                                                    |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a527f-322">Windows 7 SP1 [ESU][esu]</span><span class="sxs-lookup"><span data-stu-id="a527f-322">Windows 7 SP1 [ESU][esu]</span></span> | <span data-ttu-id="a527f-323">- Microsoft Visual C++ 2015-2019 Redistributable [64 位][vcc64] / [32 位][vcc32]</span><span class="sxs-lookup"><span data-stu-id="a527f-323">- Microsoft Visual C++ 2015-2019 Redistributable [64-bit][vcc64] / [32-bit][vcc32]</span></span> <br> <span data-ttu-id="a527f-324">- KB3063858 [64 位][kb64] / [32 位][kb32]</span><span class="sxs-lookup"><span data-stu-id="a527f-324">- KB3063858 [64-bit][kb64] / [32-bit][kb32]</span></span> <br> <span data-ttu-id="a527f-325">- [Microsoft 根证书颁发机构 2011](https://www.microsoft.com/pkiops/Docs/Repository.htm)（仅限 .NET Core 2.1 脱机安装程序）</span><span class="sxs-lookup"><span data-stu-id="a527f-325">- [Microsoft Root Certificate Authority 2011](https://www.microsoft.com/pkiops/Docs/Repository.htm) (.NET Core 2.1 offline installer only)</span></span> |
| <span data-ttu-id="a527f-326">Windows Vista SP 2</span><span class="sxs-lookup"><span data-stu-id="a527f-326">Windows Vista SP 2</span></span>       | <span data-ttu-id="a527f-327">Microsoft Visual C++ 2015-2019 Redistributable [64 位][vcc64] / [32 位][vcc32]</span><span class="sxs-lookup"><span data-stu-id="a527f-327">Microsoft Visual C++ 2015-2019 Redistributable [64-bit][vcc64] / [32-bit][vcc32]</span></span> |
| <span data-ttu-id="a527f-328">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a527f-328">Windows 8.1</span></span>              | <span data-ttu-id="a527f-329">Microsoft Visual C++ 2015-2019 Redistributable [64 位][vcc64] / [32 位][vcc32]</span><span class="sxs-lookup"><span data-stu-id="a527f-329">Microsoft Visual C++ 2015-2019 Redistributable [64-bit][vcc64] / [32-bit][vcc32]</span></span> |
| <span data-ttu-id="a527f-330">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a527f-330">Windows Server 2008 R2</span></span>   | <span data-ttu-id="a527f-331">Microsoft Visual C++ 2015-2019 Redistributable [64 位][vcc64] / [32 位][vcc32]</span><span class="sxs-lookup"><span data-stu-id="a527f-331">Microsoft Visual C++ 2015-2019 Redistributable [64-bit][vcc64] / [32-bit][vcc32]</span></span> |
| <span data-ttu-id="a527f-332">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a527f-332">Windows Server 2012 R2</span></span>   | <span data-ttu-id="a527f-333">Microsoft Visual C++ 2015-2019 Redistributable [64 位][vcc64] / [32 位][vcc32]</span><span class="sxs-lookup"><span data-stu-id="a527f-333">Microsoft Visual C++ 2015-2019 Redistributable [64-bit][vcc64] / [32-bit][vcc32]</span></span> |

<span data-ttu-id="a527f-334">如果收到与以下 dll 之一相关的错误，也需要满足上述要求：</span><span class="sxs-lookup"><span data-stu-id="a527f-334">The previous requirements are also required if you receive an error related to either of the following dlls:</span></span>

- <span data-ttu-id="a527f-335">api-ms-win-crt-runtime-l1-1-0.dll</span><span class="sxs-lookup"><span data-stu-id="a527f-335">*api-ms-win-crt-runtime-l1-1-0.dll*</span></span>
- <span data-ttu-id="a527f-336">api-ms-win-cor-timezone-l1-1-0.dll</span><span class="sxs-lookup"><span data-stu-id="a527f-336">*api-ms-win-cor-timezone-l1-1-0.dll*</span></span>
- <span data-ttu-id="a527f-337">hostfxr.dll</span><span class="sxs-lookup"><span data-stu-id="a527f-337">*hostfxr.dll*</span></span>

## <a name="install-with-powershell-automation"></a><span data-ttu-id="a527f-338">使用 PowerShell 自动化安装</span><span class="sxs-lookup"><span data-stu-id="a527f-338">Install with PowerShell automation</span></span>

<span data-ttu-id="a527f-339">[dotnet-install 脚本](../tools/dotnet-install-script.md)用于运行时的 CI 自动化和非管理员安装。</span><span class="sxs-lookup"><span data-stu-id="a527f-339">The [dotnet-install scripts](../tools/dotnet-install-script.md) are used for CI automation and non-admin installs of the runtime.</span></span> <span data-ttu-id="a527f-340">可从 [dotnet-install 脚本引用页](../tools/dotnet-install-script.md)下载该脚本。</span><span class="sxs-lookup"><span data-stu-id="a527f-340">You can download the script from the [dotnet-install script reference page](../tools/dotnet-install-script.md).</span></span>

<span data-ttu-id="a527f-341">此脚本默认安装最新的[长期支持 (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) 版本，即 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="a527f-341">The script defaults to installing the latest [long term support (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) version, which is .NET Core 3.1.</span></span> <span data-ttu-id="a527f-342">可通过指定 `Channel` 开关以选择特定版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-342">You can choose a specific release by specifying the `Channel` switch.</span></span> <span data-ttu-id="a527f-343">包括 `Runtime` 开关以安装运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-343">Include the `Runtime` switch to install a runtime.</span></span> <span data-ttu-id="a527f-344">否则，该脚本安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="a527f-344">Otherwise, the script installs the SDK.</span></span>

```powershell
dotnet-install.ps1 -Channel 5.0 -Runtime aspnetcore
```

<span data-ttu-id="a527f-345">通过省略 `-Runtime` 开关来安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="a527f-345">Install the SDK by omitting the `-Runtime` switch.</span></span> <span data-ttu-id="a527f-346">在此示例中将 `-Channel` 开关设置为 `Current`，这将安装受支持的最新版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-346">The `-Channel` switch is set in this example to `Current`, which installs the latest supported version.</span></span>

```powershell
dotnet-install.ps1 -Channel Current
```

## <a name="install-with-visual-studio"></a><span data-ttu-id="a527f-347">使用 Visual Studio 安装</span><span class="sxs-lookup"><span data-stu-id="a527f-347">Install with Visual Studio</span></span>

<span data-ttu-id="a527f-348">如果你要使用 Visual Studio 开发 .NET 应用，请参阅下表，了解不同目标 .NET SDK 版本所需的 Visual Studio 最低版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-348">If you're using Visual Studio to develop .NET apps, the following table describes the minimum required version of Visual Studio based on the target .NET SDK version.</span></span>

| <span data-ttu-id="a527f-349">.NET SDK 版本</span><span class="sxs-lookup"><span data-stu-id="a527f-349">.NET SDK version</span></span>      | <span data-ttu-id="a527f-350">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="a527f-350">Visual Studio version</span></span>                      |
| --------------------- | ------------------------------------------ |
| <span data-ttu-id="a527f-351">5.0</span><span class="sxs-lookup"><span data-stu-id="a527f-351">5.0</span></span>                   | <span data-ttu-id="a527f-352">Visual Studio 2019 版本 16.8 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-352">Visual Studio 2019 version 16.8 or higher.</span></span> |
| <span data-ttu-id="a527f-353">3.1</span><span class="sxs-lookup"><span data-stu-id="a527f-353">3.1</span></span>                   | <span data-ttu-id="a527f-354">Visual Studio 2019 版本 16.4 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-354">Visual Studio 2019 version 16.4 or higher.</span></span> |
| <span data-ttu-id="a527f-355">3.0</span><span class="sxs-lookup"><span data-stu-id="a527f-355">3.0</span></span>                   | <span data-ttu-id="a527f-356">Visual Studio 2019 版本 16.3 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-356">Visual Studio 2019 version 16.3 or higher.</span></span> |
| <span data-ttu-id="a527f-357">2.2</span><span class="sxs-lookup"><span data-stu-id="a527f-357">2.2</span></span>                   | <span data-ttu-id="a527f-358">Visual Studio 2017 版本 15.9 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-358">Visual Studio 2017 version 15.9 or higher.</span></span> |
| <span data-ttu-id="a527f-359">2.1</span><span class="sxs-lookup"><span data-stu-id="a527f-359">2.1</span></span>                   | <span data-ttu-id="a527f-360">Visual Studio 2017 版本 15.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-360">Visual Studio 2017 version 15.7 or higher.</span></span> |

<span data-ttu-id="a527f-361">如果你已安装 Visual Studio，则可以使用以下步骤检查你的版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-361">If you already have Visual Studio installed, you can check your version with the following steps.</span></span>

01. <span data-ttu-id="a527f-362">打开 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="a527f-362">Open Visual Studio.</span></span>
01. <span data-ttu-id="a527f-363">选择“帮助” > “Microsoft Visual Studio”。</span><span class="sxs-lookup"><span data-stu-id="a527f-363">Select **Help** > **About Microsoft Visual Studio**.</span></span>
01. <span data-ttu-id="a527f-364">从“关于”对话框中读取版本号。</span><span class="sxs-lookup"><span data-stu-id="a527f-364">Read the version number from the **About** dialog.</span></span>

<span data-ttu-id="a527f-365">Visual Studio 可安装最新的 .NET SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-365">Visual Studio can install the latest .NET SDK and runtime.</span></span>

> [!div class="button"]
> <span data-ttu-id="a527f-366">[下载 Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019)。</span><span class="sxs-lookup"><span data-stu-id="a527f-366">[Download Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019).</span></span>

### <a name="select-a-workload"></a><span data-ttu-id="a527f-367">选择工作负载</span><span class="sxs-lookup"><span data-stu-id="a527f-367">Select a workload</span></span>

<span data-ttu-id="a527f-368">安装或修改 Visual Studio 时，根据要生成的应用程序的类型，选择以下一个或多个工作负载：</span><span class="sxs-lookup"><span data-stu-id="a527f-368">When installing or modifying Visual Studio, select one or more of the following workloads, depending on the kind of application you're building:</span></span>

- <span data-ttu-id="a527f-369">“其他工具集”部分中的“.NET Core 跨平台开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="a527f-369">The **.NET Core cross-platform development** workload in the **Other Toolsets** section.</span></span>
- <span data-ttu-id="a527f-370">“Web 和云”部分中的“ASP.NET 和 Web 开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="a527f-370">The **ASP.NET and web development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="a527f-371">“Web 和云”部分中的“Azure 开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="a527f-371">The **Azure development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="a527f-372">“桌面和移动”部分中的“NET 桌面开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="a527f-372">The **.NET desktop development** workload in the **Desktop & Mobile** section.</span></span>

<span data-ttu-id="a527f-373">[![具有 .NET Core 工作负载的 Windows Visual Studio 2019](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a527f-373">[![Windows Visual Studio 2019 with .NET Core workload](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span></span>

## <a name="install-alongside-visual-studio-code"></a><span data-ttu-id="a527f-374">随 Visual Studio Code 一起安装</span><span class="sxs-lookup"><span data-stu-id="a527f-374">Install alongside Visual Studio Code</span></span>

<span data-ttu-id="a527f-375">Visual Studio Code 是一个功能强大的轻量级源代码编辑器，可在桌面上运行。</span><span class="sxs-lookup"><span data-stu-id="a527f-375">Visual Studio Code is a powerful and lightweight source code editor that runs on your desktop.</span></span> <span data-ttu-id="a527f-376">Visual Studio Code 适用于 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="a527f-376">Visual Studio Code is available for Windows, macOS, and Linux.</span></span>

<span data-ttu-id="a527f-377">虽然 Visual Studio Code 不像 Visual Studio 一样附带自动的 .NET Core 安装程序，但添加 .NET Core 支持非常简单。</span><span class="sxs-lookup"><span data-stu-id="a527f-377">While Visual Studio Code doesn't come with an automated .NET Core installer like Visual Studio does, adding .NET Core support is simple.</span></span>

01. <span data-ttu-id="a527f-378">[下载并安装 Visual Studio Code](https://code.visualstudio.com/Download)。</span><span class="sxs-lookup"><span data-stu-id="a527f-378">[Download and install Visual Studio Code](https://code.visualstudio.com/Download).</span></span>
01. <span data-ttu-id="a527f-379">[下载并安装 .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="a527f-379">[Download and install the .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core).</span></span>
01. <span data-ttu-id="a527f-380">[从 Visual Studio Code 市场安装 C# 扩展](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)。</span><span class="sxs-lookup"><span data-stu-id="a527f-380">[Install the C# extension from the Visual Studio Code marketplace](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="a527f-381">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a527f-381">Windows Installer</span></span>

<span data-ttu-id="a527f-382">适用于 .NET 的[下载页面](https://dotnet.microsoft.com/download/dotnet-core)提供了 Windows Installer 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="a527f-382">The [download page](https://dotnet.microsoft.com/download/dotnet-core) for .NET provides Windows Installer executables.</span></span>

<span data-ttu-id="a527f-383">使用 Windows 安装程序安装 .NET 时，可以通过设置 `DOTNETHOME_X64` 和 `DOTNETHOME_X86` 参数来自定义安装路径：</span><span class="sxs-lookup"><span data-stu-id="a527f-383">When you use the Windows installers to install .NET, you can customize the installation path by setting the `DOTNETHOME_X64` and `DOTNETHOME_X86` parameters:</span></span>

```console
dotnet-sdk-3.1.301-win-x64.exe DOTNETHOME_X64="F:\dotnet\x64" DOTNETHOME_X86="F:\dotnet\x86"
```

<span data-ttu-id="a527f-384">如果要以无提示方式安装 .NET（例如在生产环境中）或要支持持续集成，请使用以下开关：</span><span class="sxs-lookup"><span data-stu-id="a527f-384">If you want to install .NET silently, such as in a production environment or to support continuous integration, use the following switches:</span></span>

- `/install`\
<span data-ttu-id="a527f-385">安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="a527f-385">Installs .NET.</span></span>

- `/quiet`\
<span data-ttu-id="a527f-386">禁止显示任何 UI 和提示。</span><span class="sxs-lookup"><span data-stu-id="a527f-386">Prevents any UI and prompts from displaying.</span></span>

- `norestart`\
<span data-ttu-id="a527f-387">禁止任何重启尝试。</span><span class="sxs-lookup"><span data-stu-id="a527f-387">Suppresses any attempts to restart.</span></span>

```console
dotnet-sdk-3.1.301-win-x64.exe /install /quiet /norestart
```

<span data-ttu-id="a527f-388">有关详细信息，请参阅[标准安装程序命令行选项](/windows/win32/msi/standard-installer-command-line-options)。</span><span class="sxs-lookup"><span data-stu-id="a527f-388">For more information, see [Standard Installer Command-Line Options](/windows/win32/msi/standard-installer-command-line-options).</span></span>

> [!TIP]
> <span data-ttu-id="a527f-389">安装程序返回退出代码 0 以表示成功，返回退出代码 3010 以表示需要重启。</span><span class="sxs-lookup"><span data-stu-id="a527f-389">The installer returns an exit code of 0 for success and an exit code of 3010 to indicate that a restart is required.</span></span> <span data-ttu-id="a527f-390">任何其他值通常都是错误代码。</span><span class="sxs-lookup"><span data-stu-id="a527f-390">Any other value is generally an error code.</span></span>

## <a name="download-and-manually-install"></a><span data-ttu-id="a527f-391">下载并手动安装</span><span class="sxs-lookup"><span data-stu-id="a527f-391">Download and manually install</span></span>

<span data-ttu-id="a527f-392">除了使用适用于 .NET 的 Windows 安装程序，还可以下载并手动安装 SDK 或运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-392">As an alternative to the Windows installers for .NET, you can download and manually install the SDK or runtime.</span></span> <span data-ttu-id="a527f-393">手动安装通常作为持续集成测试的一部分执行。</span><span class="sxs-lookup"><span data-stu-id="a527f-393">Manual install is usually done as part of continuous integration testing.</span></span> <span data-ttu-id="a527f-394">对于开发人员或用户，一般使用[安装程序](https://dotnet.microsoft.com/download/dotnet-core)会更好。</span><span class="sxs-lookup"><span data-stu-id="a527f-394">For a developer or user, it's generally better to use an [installer](https://dotnet.microsoft.com/download/dotnet-core).</span></span>

<span data-ttu-id="a527f-395">在下载 .NET SDK 和 .NET 运行时后，可以手动安装它们。</span><span class="sxs-lookup"><span data-stu-id="a527f-395">Both .NET SDK and .NET Runtime can be manually installed after they've been downloaded.</span></span> <span data-ttu-id="a527f-396">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="a527f-396">If you install .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="a527f-397">首先，从以下站点之一下载 SDK 或运行时的二进制版本：</span><span class="sxs-lookup"><span data-stu-id="a527f-397">First, download a binary release for either the SDK or the runtime from one of the following sites:</span></span>

- [<span data-ttu-id="a527f-398">.NET 5.0 下载</span><span class="sxs-lookup"><span data-stu-id="a527f-398">.NET 5.0 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet/5.0)
- [<span data-ttu-id="a527f-399">.NET Core 3.1 下载</span><span class="sxs-lookup"><span data-stu-id="a527f-399">.NET Core 3.1 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [<span data-ttu-id="a527f-400">.NET Core 2.1 下载</span><span class="sxs-lookup"><span data-stu-id="a527f-400">.NET Core 2.1 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core/2.1)
- [<span data-ttu-id="a527f-401">所有 .NET Core 下载项</span><span class="sxs-lookup"><span data-stu-id="a527f-401">All .NET Core downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

<span data-ttu-id="a527f-402">创建要将 .NET 提取到的目录，例如 `%USERPROFILE%\dotnet`。</span><span class="sxs-lookup"><span data-stu-id="a527f-402">Create a directory to extract .NET to, for example `%USERPROFILE%\dotnet`.</span></span> <span data-ttu-id="a527f-403">然后，将下载的 zip 文件提取到该目录中。</span><span class="sxs-lookup"><span data-stu-id="a527f-403">Then, extract the downloaded zip file into that directory.</span></span>

<span data-ttu-id="a527f-404">默认情况下，.NET CLI 命令和应用不会使用通过这种方式安装的 .NET，并且你必须显式选择才能使用它。</span><span class="sxs-lookup"><span data-stu-id="a527f-404">By default, .NET CLI commands and apps won't use .NET installed in this way and you must explicitly choose to use it.</span></span> <span data-ttu-id="a527f-405">为此，请更改用于启动应用程序的环境变量：</span><span class="sxs-lookup"><span data-stu-id="a527f-405">To do so, change the environment variables with which an application is started:</span></span>

```console
set DOTNET_ROOT=%USERPROFILE%\dotnet
set PATH=%USERPROFILE%\dotnet;%PATH%
set DOTNET_MULTILEVEL_LOOKUP=0
```

<span data-ttu-id="a527f-406">使用此方法可以将多个版本安装到不同的位置，然后通过使用指向安装位置的环境变量运行应用程序来明确选择应用程序应使用哪个安装位置。</span><span class="sxs-lookup"><span data-stu-id="a527f-406">This approach lets you install multiple versions into separate locations, then explicitly choose which install location an application should use by running the application with environment variables pointing at that location.</span></span>

<span data-ttu-id="a527f-407">将 `DOTNET_MULTILEVEL_LOOKUP` 设置为 `0` 时，.NET 将忽略任何全局安装的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="a527f-407">When `DOTNET_MULTILEVEL_LOOKUP` is set to `0`, .NET ignores any globally installed .NET version.</span></span> <span data-ttu-id="a527f-408">删除环境设置，让 .NET 在选择用于运行应用程序的最佳框架时考虑默认的全局安装位置。</span><span class="sxs-lookup"><span data-stu-id="a527f-408">Remove that environment setting to let .NET consider the default global install location when selecting the best framework for running the application.</span></span> <span data-ttu-id="a527f-409">默认值通常为 `C:\Program Files\dotnet`，这是安装 .NET 的安装程序所在的位置。</span><span class="sxs-lookup"><span data-stu-id="a527f-409">The default is typically `C:\Program Files\dotnet`, which is where the installers install .NET.</span></span>

## <a name="docker"></a><span data-ttu-id="a527f-410">Docker</span><span class="sxs-lookup"><span data-stu-id="a527f-410">Docker</span></span>

<span data-ttu-id="a527f-411">容器提供了一种将应用程序与主机系统的其余部分隔离的轻量级方法。</span><span class="sxs-lookup"><span data-stu-id="a527f-411">Containers provide a lightweight way to isolate your application from the rest of the host system.</span></span> <span data-ttu-id="a527f-412">同一计算机上的容器只共享内核，并使用为应用程序提供的资源。</span><span class="sxs-lookup"><span data-stu-id="a527f-412">Containers on the same machine share just the kernel and use resources given to your application.</span></span>

<span data-ttu-id="a527f-413">.NET 可在 Docker 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="a527f-413">.NET can run in a Docker container.</span></span> <span data-ttu-id="a527f-414">官方 .NET Docker 映像发布到 Microsoft 容器注册表 (MCR)，用户可在 [Microsoft.NET Docker Hub 存储库](https://hub.docker.com/_/microsoft-dotnet)中找到这些映像。</span><span class="sxs-lookup"><span data-stu-id="a527f-414">Official .NET Docker images are published to the Microsoft Container Registry (MCR) and are discoverable at the [Microsoft .NET Docker Hub repository](https://hub.docker.com/_/microsoft-dotnet).</span></span> <span data-ttu-id="a527f-415">每个存储库包含 .NET（SDK 或运行时）和可以使用的操作系统的不同组合的映像。</span><span class="sxs-lookup"><span data-stu-id="a527f-415">Each repository contains images for different combinations of the .NET (SDK or Runtime) and OS that you can use.</span></span>

<span data-ttu-id="a527f-416">Microsoft 提供适合特定场景的映像。</span><span class="sxs-lookup"><span data-stu-id="a527f-416">Microsoft provides images that are tailored for specific scenarios.</span></span> <span data-ttu-id="a527f-417">例如，[ASP.NET Core 存储库](https://hub.docker.com/_/microsoft-dotnet-aspnet)提供针对在生产环境中运行 ASP.NET Core 应用生成的映像。</span><span class="sxs-lookup"><span data-stu-id="a527f-417">For example, the [ASP.NET Core repository](https://hub.docker.com/_/microsoft-dotnet-aspnet) provides images that are built for running ASP.NET Core apps in production.</span></span>

<span data-ttu-id="a527f-418">有关在 Docker 容器中使用 .NET 的详细信息，请参阅 [.NET 和 Docker 简介](../docker/introduction.md)和[示例](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-418">For more information about using .NET in a Docker container, see [Introduction to .NET and Docker](../docker/introduction.md) and [Samples](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a527f-419">后续步骤</span><span class="sxs-lookup"><span data-stu-id="a527f-419">Next steps</span></span>

- <span data-ttu-id="a527f-420">[如何检查是否已安装 .NET](how-to-detect-installed-versions.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="a527f-420">[How to check if .NET is already installed](how-to-detect-installed-versions.md?pivots=os-windows).</span></span>
- <span data-ttu-id="a527f-421">[教程：Hello World 教程](../tutorials/with-visual-studio.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-421">[Tutorial: Hello World tutorial](../tutorials/with-visual-studio.md).</span></span>
- <span data-ttu-id="a527f-422">[教程：使用 Visual Studio Code 创建一个新应用](../tutorials/with-visual-studio-code.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-422">[Tutorial: Create a new app with Visual Studio Code](../tutorials/with-visual-studio-code.md).</span></span>
- <span data-ttu-id="a527f-423">[教程：使 .NET Core 应用容器化](../docker/build-container.md)。</span><span class="sxs-lookup"><span data-stu-id="a527f-423">[Tutorial: Containerize a .NET Core app](../docker/build-container.md).</span></span>

[esu]: /troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq
[vcc64]: https://aka.ms/vs/16/release/vc_redist.x64.exe
[vcc32]: https://aka.ms/vs/16/release/vc_redist.x86.exe
[kb64]: https://www.microsoft.com/download/details.aspx?id=47442
[kb32]: https://www.microsoft.com/download/details.aspx?id=47409

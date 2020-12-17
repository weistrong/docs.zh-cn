---
title: 在 Windows 上安装 .NET
description: 了解可在其上安装 .NET 的 Windows 版本。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: b5c0949bbd591906536094a33d8583a265d8a4c8
ms.sourcegitcommit: 9b877e160c326577e8aa5ead22a937110d80fa44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97110229"
---
# <a name="install-net-on-windows"></a><span data-ttu-id="51a39-103">在 Windows 上安装 .NET</span><span class="sxs-lookup"><span data-stu-id="51a39-103">Install .NET on Windows</span></span>

> [!div class="op_single_selector"]
>
> - [在 Windows 上安装](windows.md)
> - [在 macOS 上安装](macos.md)
> - [在 Linux 上安装](linux.md)

<span data-ttu-id="51a39-107">本文介绍如何在 Windows 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="51a39-107">In this article, you'll learn how to install .NET on Windows.</span></span> <span data-ttu-id="51a39-108">.NET 由运行时和 SDK 组成。</span><span class="sxs-lookup"><span data-stu-id="51a39-108">.NET is made up of the runtime and the SDK.</span></span> <span data-ttu-id="51a39-109">运行时用于运行 .NET 应用，应用可能包含也可能不包含它。</span><span class="sxs-lookup"><span data-stu-id="51a39-109">The runtime is used to run a .NET app and may or may not be included with the app.</span></span> <span data-ttu-id="51a39-110">SDK 用于创建 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="51a39-110">The SDK is used to create .NET apps and libraries.</span></span> <span data-ttu-id="51a39-111">.NET 运行时始终随 SDK 一起安装。</span><span class="sxs-lookup"><span data-stu-id="51a39-111">The .NET runtime is always installed with the SDK.</span></span>

<span data-ttu-id="51a39-112">最新版本的 .NET 是 5.0。</span><span class="sxs-lookup"><span data-stu-id="51a39-112">The latest version of .NET is 5.0.</span></span>

> [!div class="button"]
> [<span data-ttu-id="51a39-113">下载 .NET</span><span class="sxs-lookup"><span data-stu-id="51a39-113">Download .NET</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="supported-releases"></a><span data-ttu-id="51a39-114">支持的版本</span><span class="sxs-lookup"><span data-stu-id="51a39-114">Supported releases</span></span>

<span data-ttu-id="51a39-115">下表列出了当前支持的 .NET 版本以及支持它们的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-115">The following table is a list of currently supported .NET releases and the versions of Windows they're supported on.</span></span> <span data-ttu-id="51a39-116">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Windows 版本达到生命周期](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="51a39-116">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Windows reaches end-of-life](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

<span data-ttu-id="51a39-117">Windows 10 版本终止服务日期按版本分段。</span><span class="sxs-lookup"><span data-stu-id="51a39-117">Windows 10 versions end-of-service dates are segmented by edition.</span></span> <span data-ttu-id="51a39-118">下表中仅考虑家庭版、专业版、专业教育版和专业工作站版。   </span><span class="sxs-lookup"><span data-stu-id="51a39-118">Only **Home**, **Pro**, **Pro Education**, and **Pro for Workstations** editions are considered in the following table.</span></span> <span data-ttu-id="51a39-119">查看 [Windows 生命周期事实表单](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)，了解具体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="51a39-119">Check the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet) for specific details.</span></span>

> [!TIP]
> <span data-ttu-id="51a39-120">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-120">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="51a39-121">操作系统</span><span class="sxs-lookup"><span data-stu-id="51a39-121">Operating System</span></span>            | <span data-ttu-id="51a39-122">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="51a39-122">.NET Core 2.1</span></span> | <span data-ttu-id="51a39-123">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="51a39-123">.NET Core 3.1</span></span> | <span data-ttu-id="51a39-124">.NET 5</span><span class="sxs-lookup"><span data-stu-id="51a39-124">.NET 5</span></span> |
|-----------------------------|---------------|---------------|--------|
| <span data-ttu-id="51a39-125">Windows 10 版本 20H2</span><span class="sxs-lookup"><span data-stu-id="51a39-125">Windows 10, Version 20H2</span></span>    | <span data-ttu-id="51a39-126">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-126">✔️</span></span>           | <span data-ttu-id="51a39-127">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-127">✔️</span></span>            | <span data-ttu-id="51a39-128">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-128">✔️</span></span>    |
| <span data-ttu-id="51a39-129">Windows 10 版本 2004</span><span class="sxs-lookup"><span data-stu-id="51a39-129">Windows 10, Version 2004</span></span>    | <span data-ttu-id="51a39-130">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-130">✔️</span></span>           | <span data-ttu-id="51a39-131">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-131">✔️</span></span>            | <span data-ttu-id="51a39-132">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-132">✔️</span></span>    |
| <span data-ttu-id="51a39-133">Windows 10 版本 1909</span><span class="sxs-lookup"><span data-stu-id="51a39-133">Windows 10, Version 1909</span></span>    | <span data-ttu-id="51a39-134">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-134">✔️</span></span>           | <span data-ttu-id="51a39-135">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-135">✔️</span></span>            | <span data-ttu-id="51a39-136">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-136">✔️</span></span>    |
| <span data-ttu-id="51a39-137">Windows 10 版本 1903</span><span class="sxs-lookup"><span data-stu-id="51a39-137">Windows 10, Version 1903</span></span>    | <span data-ttu-id="51a39-138">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-138">✔️</span></span>           | <span data-ttu-id="51a39-139">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-139">✔️</span></span>            | <span data-ttu-id="51a39-140">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-140">✔️</span></span>    |
| <span data-ttu-id="51a39-141">Windows 10 版本 1809</span><span class="sxs-lookup"><span data-stu-id="51a39-141">Windows 10, Version 1809</span></span>    | <span data-ttu-id="51a39-142">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-142">✔️</span></span>           | <span data-ttu-id="51a39-143">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-143">✔️</span></span>            | <span data-ttu-id="51a39-144">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-144">✔️</span></span>    |
| <span data-ttu-id="51a39-145"> Windows 10 版本 1803</span><span class="sxs-lookup"><span data-stu-id="51a39-145">Windows 10, Version 1803</span></span>    | <span data-ttu-id="51a39-146">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-146">✔️</span></span>           | <span data-ttu-id="51a39-147">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-147">✔️</span></span>            | <span data-ttu-id="51a39-148">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-148">✔️</span></span>    |
| <span data-ttu-id="51a39-149"> Windows 10 版本 1709</span><span class="sxs-lookup"><span data-stu-id="51a39-149">Windows 10, Version 1709</span></span>    | <span data-ttu-id="51a39-150">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-150">✔️</span></span>           | <span data-ttu-id="51a39-151">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-151">✔️</span></span>            | <span data-ttu-id="51a39-152">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-152">✔️</span></span>    |
| <span data-ttu-id="51a39-153">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="51a39-153">Windows 10, Version 1607</span></span>    | <span data-ttu-id="51a39-154">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-154">✔️</span></span>           | <span data-ttu-id="51a39-155">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-155">✔️</span></span>            | <span data-ttu-id="51a39-156">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-156">✔️</span></span>    |
| <span data-ttu-id="51a39-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-157">Windows 8.1</span></span>                 | <span data-ttu-id="51a39-158">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-158">✔️</span></span>           | <span data-ttu-id="51a39-159">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-159">✔️</span></span>            | <span data-ttu-id="51a39-160">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-160">✔️</span></span>    |
| <span data-ttu-id="51a39-161">Windows 7 SP1 [ESU][esu]</span><span class="sxs-lookup"><span data-stu-id="51a39-161">Windows 7 SP1 [ESU][esu]</span></span>    | <span data-ttu-id="51a39-162">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-162">✔️</span></span>           | <span data-ttu-id="51a39-163">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-163">✔️</span></span>            | <span data-ttu-id="51a39-164">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-164">✔️</span></span>    |
| <span data-ttu-id="51a39-165">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="51a39-165">Windows 10, Version 1607</span></span>    | <span data-ttu-id="51a39-166">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-166">✔️</span></span>           | <span data-ttu-id="51a39-167">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-167">✔️</span></span>            | <span data-ttu-id="51a39-168">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-168">✔️</span></span>    |
| <span data-ttu-id="51a39-169">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="51a39-169">Windows 10, Version 1607</span></span>    | <span data-ttu-id="51a39-170">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-170">✔️</span></span>           | <span data-ttu-id="51a39-171">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-171">✔️</span></span>            | <span data-ttu-id="51a39-172">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-172">✔️</span></span>    |
| <span data-ttu-id="51a39-173">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="51a39-173">Windows Server 2012 R2</span></span>      | <span data-ttu-id="51a39-174">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-174">✔️</span></span>           | <span data-ttu-id="51a39-175">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-175">✔️</span></span>            | <span data-ttu-id="51a39-176">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-176">✔️</span></span>    |
| <span data-ttu-id="51a39-177">Windows Server Core 2012 R2</span><span class="sxs-lookup"><span data-stu-id="51a39-177">Windows Server Core 2012 R2</span></span> | <span data-ttu-id="51a39-178">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-178">✔️</span></span>           | <span data-ttu-id="51a39-179">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-179">✔️</span></span>            | <span data-ttu-id="51a39-180">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-180">✔️</span></span>    |
| <span data-ttu-id="51a39-181">Nano Server 版本 1809+</span><span class="sxs-lookup"><span data-stu-id="51a39-181">Nano Server, Version 1809+</span></span>  | <span data-ttu-id="51a39-182">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-182">✔️</span></span>           | <span data-ttu-id="51a39-183">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-183">✔️</span></span>            | <span data-ttu-id="51a39-184">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-184">✔️</span></span>    |
| <span data-ttu-id="51a39-185">Nano Server 版本 1803</span><span class="sxs-lookup"><span data-stu-id="51a39-185">Nano Server, Version 1803</span></span>   | <span data-ttu-id="51a39-186">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-186">✔️</span></span>           | <span data-ttu-id="51a39-187">✔️</span><span class="sxs-lookup"><span data-stu-id="51a39-187">✔️</span></span>            | ❌    |

## <a name="unsupported-releases"></a><span data-ttu-id="51a39-188">不支持的版本</span><span class="sxs-lookup"><span data-stu-id="51a39-188">Unsupported releases</span></span>

<span data-ttu-id="51a39-189">以下 .NET 版本 ❌ 不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="51a39-189">The following versions of .NET are ❌ no longer supported.</span></span> <span data-ttu-id="51a39-190">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="51a39-190">The downloads for these still remain published:</span></span>

- <span data-ttu-id="51a39-191">3.0</span><span class="sxs-lookup"><span data-stu-id="51a39-191">3.0</span></span>
- <span data-ttu-id="51a39-192">2.2</span><span class="sxs-lookup"><span data-stu-id="51a39-192">2.2</span></span>
- <span data-ttu-id="51a39-193">2.0</span><span class="sxs-lookup"><span data-stu-id="51a39-193">2.0</span></span>

## <a name="runtime-information"></a><span data-ttu-id="51a39-194">运行时信息</span><span class="sxs-lookup"><span data-stu-id="51a39-194">Runtime information</span></span>

<span data-ttu-id="51a39-195">运行时用于运行使用 .NET 创建的应用。</span><span class="sxs-lookup"><span data-stu-id="51a39-195">The runtime is used to run apps created with .NET.</span></span> <span data-ttu-id="51a39-196">应用作者发布应用时，可以在其应用中包含运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-196">When an app author publishes an app, they can include the runtime with their app.</span></span> <span data-ttu-id="51a39-197">如果作者未包含运行时，则由用户安装运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-197">If they don't include the runtime, it's up to the user to install the runtime.</span></span>

<span data-ttu-id="51a39-198">可以在 Windows 上安装三个不同的运行时：</span><span class="sxs-lookup"><span data-stu-id="51a39-198">There are three different runtimes you can install on Windows:</span></span>

<span data-ttu-id="51a39-199">*ASP.NET Core 运行时*</span><span class="sxs-lookup"><span data-stu-id="51a39-199">*ASP.NET Core runtime*</span></span>\
<span data-ttu-id="51a39-200">运行 ASP.NET Core 应用。</span><span class="sxs-lookup"><span data-stu-id="51a39-200">Runs ASP.NET Core apps.</span></span> <span data-ttu-id="51a39-201">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-201">Includes the .NET runtime.</span></span>

<span data-ttu-id="51a39-202">*桌面运行时*</span><span class="sxs-lookup"><span data-stu-id="51a39-202">*Desktop runtime*</span></span>\
<span data-ttu-id="51a39-203">运行适用于 Windows 的 .NET WPF 和 Windows 窗体桌面应用。</span><span class="sxs-lookup"><span data-stu-id="51a39-203">Runs .NET WPF and Windows Forms desktop apps for Windows.</span></span> <span data-ttu-id="51a39-204">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-204">Includes the .NET runtime.</span></span>

<span data-ttu-id="51a39-205">.NET 运行时</span><span class="sxs-lookup"><span data-stu-id="51a39-205">*.NET runtime*</span></span>\
<span data-ttu-id="51a39-206">此运行时是最简单的运行时，不包括任何其他运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-206">This runtime is the simplest runtime and doesn't include any other runtime.</span></span> <span data-ttu-id="51a39-207">强烈建议同时安装 ASP.NET Core 运行时和桌面运行时，以最大限度地提升与 .NET 应用的兼容性 。</span><span class="sxs-lookup"><span data-stu-id="51a39-207">It's highly recommended that you install both *ASP.NET Core runtime* and *Desktop runtime* for the best compatibility with .NET apps.</span></span>

> [!div class="button"]
> [<span data-ttu-id="51a39-208">下载 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="51a39-208">Download .NET Runtime</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="sdk-information"></a><span data-ttu-id="51a39-209">SDK 信息</span><span class="sxs-lookup"><span data-stu-id="51a39-209">SDK information</span></span>

<span data-ttu-id="51a39-210">SDK 用于生成和发布 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="51a39-210">The SDK is used to build and publish .NET apps and libraries.</span></span> <span data-ttu-id="51a39-211">安装 SDK 会包含三个[运行时](#runtime-information)：ASP.NET Core、桌面和 .NET。</span><span class="sxs-lookup"><span data-stu-id="51a39-211">Installing the SDK includes all three [runtimes](#runtime-information): ASP.NET Core, Desktop, and .NET.</span></span>

## <a name="dependencies"></a><span data-ttu-id="51a39-212">依赖项</span><span class="sxs-lookup"><span data-stu-id="51a39-212">Dependencies</span></span>

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD024 -->

# <a name="net-50"></a>[<span data-ttu-id="51a39-213">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="51a39-213">.NET 5.0</span></span>](#tab/net50)

<span data-ttu-id="51a39-214">.NET 5.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="51a39-214">The following Windows versions are supported with .NET 5.0:</span></span>

> [!NOTE]
> <span data-ttu-id="51a39-215">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-215">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="51a39-216">(OS)</span><span class="sxs-lookup"><span data-stu-id="51a39-216">OS</span></span>                  | <span data-ttu-id="51a39-217">Version</span><span class="sxs-lookup"><span data-stu-id="51a39-217">Version</span></span>       | <span data-ttu-id="51a39-218">体系结构</span><span class="sxs-lookup"><span data-stu-id="51a39-218">Architectures</span></span>   |
|---------------------|---------------|-----------------|
| <span data-ttu-id="51a39-219">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-219">Windows 10 Client</span></span>   | <span data-ttu-id="51a39-220">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="51a39-220">Version 1607+</span></span> | <span data-ttu-id="51a39-221">x64、x86、ARM64</span><span class="sxs-lookup"><span data-stu-id="51a39-221">x64, x86, ARM64</span></span> |
| <span data-ttu-id="51a39-222">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-222">Windows Client</span></span>      | <span data-ttu-id="51a39-223">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-223">7 SP1+, 8.1</span></span>   | <span data-ttu-id="51a39-224">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-224">x64, x86</span></span>        |
| <span data-ttu-id="51a39-225">Windows Server</span><span class="sxs-lookup"><span data-stu-id="51a39-225">Windows Server</span></span>      | <span data-ttu-id="51a39-226">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="51a39-226">2012 R2+</span></span>      | <span data-ttu-id="51a39-227">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-227">x64, x86</span></span>        |
| <span data-ttu-id="51a39-228">Windows Server 核心</span><span class="sxs-lookup"><span data-stu-id="51a39-228">Windows Server Core</span></span> | <span data-ttu-id="51a39-229">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="51a39-229">2012 R2+</span></span>      | <span data-ttu-id="51a39-230">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-230">x64, x86</span></span>        |
| <span data-ttu-id="51a39-231">Nano Server</span><span class="sxs-lookup"><span data-stu-id="51a39-231">Nano Server</span></span>         | <span data-ttu-id="51a39-232">版本 1809+</span><span class="sxs-lookup"><span data-stu-id="51a39-232">Version 1809+</span></span> | <span data-ttu-id="51a39-233">X64</span><span class="sxs-lookup"><span data-stu-id="51a39-233">x64</span></span>             |

<span data-ttu-id="51a39-234">有关 .NET 5.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET 5.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-234">For more information about .NET 5.0 supported operating systems, distributions, and lifecycle policy, see [.NET 5.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md).</span></span>

# <a name="net-core-31"></a>[<span data-ttu-id="51a39-235">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="51a39-235">.NET Core 3.1</span></span>](#tab/netcore31)

<span data-ttu-id="51a39-236">.NET Core 3.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="51a39-236">The following Windows versions are supported with .NET Core 3.1:</span></span>

> [!NOTE]
> <span data-ttu-id="51a39-237">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-237">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="51a39-238">(OS)</span><span class="sxs-lookup"><span data-stu-id="51a39-238">OS</span></span>                            | <span data-ttu-id="51a39-239">Version</span><span class="sxs-lookup"><span data-stu-id="51a39-239">Version</span></span>                        | <span data-ttu-id="51a39-240">体系结构</span><span class="sxs-lookup"><span data-stu-id="51a39-240">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="51a39-241">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-241">Windows Client</span></span>                | <span data-ttu-id="51a39-242">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-242">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="51a39-243">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-243">x64, x86</span></span>        |
| <span data-ttu-id="51a39-244">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-244">Windows 10 Client</span></span>             | <span data-ttu-id="51a39-245">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="51a39-245">Version 1607+</span></span>                  | <span data-ttu-id="51a39-246">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-246">x64, x86</span></span>        |
| <span data-ttu-id="51a39-247">Windows Server</span><span class="sxs-lookup"><span data-stu-id="51a39-247">Windows Server</span></span>                | <span data-ttu-id="51a39-248">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="51a39-248">2012 R2+</span></span>                       | <span data-ttu-id="51a39-249">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-249">x64, x86</span></span>        |
| <span data-ttu-id="51a39-250">Nano Server</span><span class="sxs-lookup"><span data-stu-id="51a39-250">Nano Server</span></span>                   | <span data-ttu-id="51a39-251">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="51a39-251">Version 1803+</span></span>                  | <span data-ttu-id="51a39-252">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="51a39-252">x64, ARM32</span></span>      |

<span data-ttu-id="51a39-253">有关 .NET Core 3.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-253">For more information about .NET Core 3.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md).</span></span>

# <a name="net-core-30"></a>[<span data-ttu-id="51a39-254">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="51a39-254">.NET Core 3.0</span></span>](#tab/netcore30)

<span data-ttu-id="51a39-255">目前不 ❌ 支持 .NET Core 3.0 *。* 有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="51a39-255">*.NET Core 3.0 is currently ❌ out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="51a39-256">.NET Core 3.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="51a39-256">The following Windows versions are supported with .NET Core 3.0:</span></span>

> [!NOTE]
> <span data-ttu-id="51a39-257">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-257">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="51a39-258">(OS)</span><span class="sxs-lookup"><span data-stu-id="51a39-258">OS</span></span>                            | <span data-ttu-id="51a39-259">Version</span><span class="sxs-lookup"><span data-stu-id="51a39-259">Version</span></span>                        | <span data-ttu-id="51a39-260">体系结构</span><span class="sxs-lookup"><span data-stu-id="51a39-260">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="51a39-261">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-261">Windows Client</span></span>                | <span data-ttu-id="51a39-262">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-262">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="51a39-263">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-263">x64, x86</span></span>        |
| <span data-ttu-id="51a39-264">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-264">Windows 10 Client</span></span>             | <span data-ttu-id="51a39-265">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="51a39-265">Version 1607+</span></span>                  | <span data-ttu-id="51a39-266">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-266">x64, x86</span></span>        |
| <span data-ttu-id="51a39-267">Windows Server</span><span class="sxs-lookup"><span data-stu-id="51a39-267">Windows Server</span></span>                | <span data-ttu-id="51a39-268">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="51a39-268">2012 R2+</span></span>                       | <span data-ttu-id="51a39-269">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-269">x64, x86</span></span>        |
| <span data-ttu-id="51a39-270">Nano Server</span><span class="sxs-lookup"><span data-stu-id="51a39-270">Nano Server</span></span>                   | <span data-ttu-id="51a39-271">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="51a39-271">Version 1803+</span></span>                  | <span data-ttu-id="51a39-272">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="51a39-272">x64, ARM32</span></span>      |

<span data-ttu-id="51a39-273">有关 .NET Core 3.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-273">For more information about .NET Core 3.0 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md).</span></span>

# <a name="net-core-22"></a>[<span data-ttu-id="51a39-274">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="51a39-274">.NET Core 2.2</span></span>](#tab/netcore22)

<span data-ttu-id="51a39-275">目前不 ❌ 支持 .NET Core 2.2。有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="51a39-275">*.NET Core 2.2 is currently ❌ out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="51a39-276">.NET Core 2.2 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="51a39-276">The following Windows versions are supported with .NET Core 2.2:</span></span>

> [!NOTE]
> <span data-ttu-id="51a39-277">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-277">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="51a39-278">(OS)</span><span class="sxs-lookup"><span data-stu-id="51a39-278">OS</span></span>                            | <span data-ttu-id="51a39-279">Version</span><span class="sxs-lookup"><span data-stu-id="51a39-279">Version</span></span>                        | <span data-ttu-id="51a39-280">体系结构</span><span class="sxs-lookup"><span data-stu-id="51a39-280">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="51a39-281">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-281">Windows Client</span></span>                | <span data-ttu-id="51a39-282">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-282">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="51a39-283">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-283">x64, x86</span></span>        |
| <span data-ttu-id="51a39-284">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-284">Windows 10 Client</span></span>             | <span data-ttu-id="51a39-285">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="51a39-285">Version 1607+</span></span>                  | <span data-ttu-id="51a39-286">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-286">x64, x86</span></span>        |
| <span data-ttu-id="51a39-287">Windows Server</span><span class="sxs-lookup"><span data-stu-id="51a39-287">Windows Server</span></span>                | <span data-ttu-id="51a39-288">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="51a39-288">2008 R2 SP1+</span></span>                   | <span data-ttu-id="51a39-289">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-289">x64, x86</span></span>        |
| <span data-ttu-id="51a39-290">Nano Server</span><span class="sxs-lookup"><span data-stu-id="51a39-290">Nano Server</span></span>                   | <span data-ttu-id="51a39-291">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="51a39-291">Version 1803+</span></span>                   | <span data-ttu-id="51a39-292">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="51a39-292">x64, ARM32</span></span>      |

<span data-ttu-id="51a39-293">有关 .NET Core 2.2 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.2 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-293">For more information about .NET Core 2.2 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.2 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md).</span></span>

# <a name="net-core-21"></a>[<span data-ttu-id="51a39-294">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="51a39-294">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="51a39-295">.NET Core 2.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="51a39-295">The following Windows versions are supported with .NET Core 2.1:</span></span>

> [!NOTE]
> <span data-ttu-id="51a39-296">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-296">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="51a39-297">(OS)</span><span class="sxs-lookup"><span data-stu-id="51a39-297">OS</span></span>                            | <span data-ttu-id="51a39-298">Version</span><span class="sxs-lookup"><span data-stu-id="51a39-298">Version</span></span>                        | <span data-ttu-id="51a39-299">体系结构</span><span class="sxs-lookup"><span data-stu-id="51a39-299">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="51a39-300">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-300">Windows Client</span></span>                | <span data-ttu-id="51a39-301">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-301">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="51a39-302">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-302">x64, x86</span></span>        |
| <span data-ttu-id="51a39-303">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="51a39-303">Windows 10 Client</span></span>             | <span data-ttu-id="51a39-304">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="51a39-304">Version 1607+</span></span>                  | <span data-ttu-id="51a39-305">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-305">x64, x86</span></span>        |
| <span data-ttu-id="51a39-306">Windows Server</span><span class="sxs-lookup"><span data-stu-id="51a39-306">Windows Server</span></span>                | <span data-ttu-id="51a39-307">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="51a39-307">2008 R2 SP1+</span></span>                   | <span data-ttu-id="51a39-308">x64、x86</span><span class="sxs-lookup"><span data-stu-id="51a39-308">x64, x86</span></span>        |
| <span data-ttu-id="51a39-309">Nano Server</span><span class="sxs-lookup"><span data-stu-id="51a39-309">Nano Server</span></span>                   | <span data-ttu-id="51a39-310">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="51a39-310">Version 1803+</span></span>                  | <span data-ttu-id="51a39-311">x64</span><span class="sxs-lookup"><span data-stu-id="51a39-311">x64,</span></span>            |

<span data-ttu-id="51a39-312">有关 .NET Core 2.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-312">For more information about .NET Core 2.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md).</span></span>

---

<!-- markdownlint-disable MD001 -->

### <a name="windows-7--vista--81--server-2008-r2--server-2012-r2"></a><a name="additional-deps"></a> <span data-ttu-id="51a39-313">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="51a39-313">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span></span>

<span data-ttu-id="51a39-314">如果要在以下 Windows 版本上安装 .NET SDK 或运行时，则需要其他依赖项：</span><span class="sxs-lookup"><span data-stu-id="51a39-314">Additional dependencies are required if you're installing the .NET SDK or runtime on the following Windows versions:</span></span>

- <span data-ttu-id="51a39-315">Windows 7 SP1 [ESU][esu]</span><span class="sxs-lookup"><span data-stu-id="51a39-315">Windows 7 SP1 [ESU][esu]</span></span>
- <span data-ttu-id="51a39-316">Windows Vista SP 2</span><span class="sxs-lookup"><span data-stu-id="51a39-316">Windows Vista SP 2</span></span>
- <span data-ttu-id="51a39-317">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51a39-317">Windows 8.1</span></span>
- <span data-ttu-id="51a39-318">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51a39-318">Windows Server 2008 R2</span></span>
- <span data-ttu-id="51a39-319">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="51a39-319">Windows Server 2012 R2</span></span>

<span data-ttu-id="51a39-320">安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="51a39-320">Install the following:</span></span>

- <span data-ttu-id="51a39-321">[Microsoft Visual C++ 2015 Redistributable 更新 3](https://www.microsoft.com/download/details.aspx?id=52685)。</span><span class="sxs-lookup"><span data-stu-id="51a39-321">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685).</span></span>
- [<span data-ttu-id="51a39-322">KB2533623</span><span class="sxs-lookup"><span data-stu-id="51a39-322">KB2533623</span></span>](https://support.microsoft.com/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot)

<span data-ttu-id="51a39-323">如果遇到以下错误之一，也需要满足上述要求：</span><span class="sxs-lookup"><span data-stu-id="51a39-323">The previous requirements are also required if you come across one of the following errors:</span></span>

> <span data-ttu-id="51a39-324">此程序无法启动，因为计算机上缺少 api-ms-win-crt-runtime-l1-1-0.dll。</span><span class="sxs-lookup"><span data-stu-id="51a39-324">The program can't start because *api-ms-win-crt-runtime-l1-1-0.dll* is missing from your computer.</span></span> <span data-ttu-id="51a39-325">尝试重新安装该程序以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="51a39-325">Try reinstalling the program to fix this problem.</span></span>
>
> <span data-ttu-id="51a39-326">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="51a39-326">\- or -</span></span>
>
> <span data-ttu-id="51a39-327">此程序无法启动，因为计算机上缺少 api-ms-win-cor-timezone-l1-1-0.dll。</span><span class="sxs-lookup"><span data-stu-id="51a39-327">The program can't start because *api-ms-win-cor-timezone-l1-1-0.dll* is missing from your computer.</span></span> <span data-ttu-id="51a39-328">尝试重新安装该程序以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="51a39-328">Try reinstalling the program to fix this problem.</span></span>
>
> <span data-ttu-id="51a39-329">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="51a39-329">\- or -</span></span>
>
> <span data-ttu-id="51a39-330">已找到库 hostfxr.dll，但未能将其从 C:\\\<path_to_app>\\hostfxr.dll 中加载。</span><span class="sxs-lookup"><span data-stu-id="51a39-330">The library *hostfxr.dll* was found, but loading it from *C:\\\<path_to_app>\\hostfxr.dll* failed.</span></span>

## <a name="install-with-powershell-automation"></a><span data-ttu-id="51a39-331">使用 PowerShell 自动化安装</span><span class="sxs-lookup"><span data-stu-id="51a39-331">Install with PowerShell automation</span></span>

<span data-ttu-id="51a39-332">[dotnet-install 脚本](../tools/dotnet-install-script.md)用于运行时的 CI 自动化和非管理员安装。</span><span class="sxs-lookup"><span data-stu-id="51a39-332">The [dotnet-install scripts](../tools/dotnet-install-script.md) are used for CI automation and non-admin installs of the runtime.</span></span> <span data-ttu-id="51a39-333">可从 [dotnet-install 脚本引用页](../tools/dotnet-install-script.md)下载该脚本。</span><span class="sxs-lookup"><span data-stu-id="51a39-333">You can download the script from the [dotnet-install script reference page](../tools/dotnet-install-script.md).</span></span>

<span data-ttu-id="51a39-334">此脚本默认安装最新的[长期支持 (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) 版本，即 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="51a39-334">The script defaults to installing the latest [long term support (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) version, which is .NET Core 3.1.</span></span> <span data-ttu-id="51a39-335">可通过指定 `Channel` 开关以选择特定版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-335">You can choose a specific release by specifying the `Channel` switch.</span></span> <span data-ttu-id="51a39-336">包括 `Runtime` 开关以安装运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-336">Include the `Runtime` switch to install a runtime.</span></span> <span data-ttu-id="51a39-337">否则，该脚本安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="51a39-337">Otherwise, the script installs the SDK.</span></span>

```powershell
dotnet-install.ps1 -Channel 5.0 -Runtime aspnetcore
```

<span data-ttu-id="51a39-338">通过省略 `-Runtime` 开关来安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="51a39-338">Install the SDK by omitting the `-Runtime` switch.</span></span> <span data-ttu-id="51a39-339">在此示例中将 `-Channel` 开关设置为 `Current`，这将安装受支持的最新版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-339">The `-Channel` switch is set in this example to `Current`, which installs the latest supported version.</span></span>

```powershell
dotnet-install.ps1 -Channel Current
```

## <a name="install-with-visual-studio"></a><span data-ttu-id="51a39-340">使用 Visual Studio 安装</span><span class="sxs-lookup"><span data-stu-id="51a39-340">Install with Visual Studio</span></span>

<span data-ttu-id="51a39-341">如果你要使用 Visual Studio 开发 .NET 应用，请参阅下表，了解不同目标 .NET SDK 版本所需的 Visual Studio 最低版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-341">If you're using Visual Studio to develop .NET apps, the following table describes the minimum required version of Visual Studio based on the target .NET SDK version.</span></span>

| <span data-ttu-id="51a39-342">.NET SDK 版本</span><span class="sxs-lookup"><span data-stu-id="51a39-342">.NET SDK version</span></span>      | <span data-ttu-id="51a39-343">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="51a39-343">Visual Studio version</span></span>                      |
| --------------------- | ------------------------------------------ |
| <span data-ttu-id="51a39-344">5.0</span><span class="sxs-lookup"><span data-stu-id="51a39-344">5.0</span></span>                   | <span data-ttu-id="51a39-345">Visual Studio 2019 版本 16.8 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-345">Visual Studio 2019 version 16.8 or higher.</span></span> |
| <span data-ttu-id="51a39-346">3.1</span><span class="sxs-lookup"><span data-stu-id="51a39-346">3.1</span></span>                   | <span data-ttu-id="51a39-347">Visual Studio 2019 版本 16.4 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-347">Visual Studio 2019 version 16.4 or higher.</span></span> |
| <span data-ttu-id="51a39-348">3.0</span><span class="sxs-lookup"><span data-stu-id="51a39-348">3.0</span></span>                   | <span data-ttu-id="51a39-349">Visual Studio 2019 版本 16.3 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-349">Visual Studio 2019 version 16.3 or higher.</span></span> |
| <span data-ttu-id="51a39-350">2.2</span><span class="sxs-lookup"><span data-stu-id="51a39-350">2.2</span></span>                   | <span data-ttu-id="51a39-351">Visual Studio 2017 版本 15.9 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-351">Visual Studio 2017 version 15.9 or higher.</span></span> |
| <span data-ttu-id="51a39-352">2.1</span><span class="sxs-lookup"><span data-stu-id="51a39-352">2.1</span></span>                   | <span data-ttu-id="51a39-353">Visual Studio 2017 版本 15.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-353">Visual Studio 2017 version 15.7 or higher.</span></span> |

<span data-ttu-id="51a39-354">如果你已安装 Visual Studio，则可以使用以下步骤检查你的版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-354">If you already have Visual Studio installed, you can check your version with the following steps.</span></span>

01. <span data-ttu-id="51a39-355">打开 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="51a39-355">Open Visual Studio.</span></span>
01. <span data-ttu-id="51a39-356">选择“帮助” > “Microsoft Visual Studio”。</span><span class="sxs-lookup"><span data-stu-id="51a39-356">Select **Help** > **About Microsoft Visual Studio**.</span></span>
01. <span data-ttu-id="51a39-357">从“关于”对话框中读取版本号。</span><span class="sxs-lookup"><span data-stu-id="51a39-357">Read the version number from the **About** dialog.</span></span>

<span data-ttu-id="51a39-358">Visual Studio 可安装最新的 .NET SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-358">Visual Studio can install the latest .NET SDK and runtime.</span></span>

> [!div class="button"]
> <span data-ttu-id="51a39-359">[下载 Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019)。</span><span class="sxs-lookup"><span data-stu-id="51a39-359">[Download Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019).</span></span>

### <a name="select-a-workload"></a><span data-ttu-id="51a39-360">选择工作负载</span><span class="sxs-lookup"><span data-stu-id="51a39-360">Select a workload</span></span>

<span data-ttu-id="51a39-361">安装或修改 Visual Studio 时，根据要生成的应用程序的类型，选择以下一个或多个工作负载：</span><span class="sxs-lookup"><span data-stu-id="51a39-361">When installing or modifying Visual Studio, select one or more of the following workloads, depending on the kind of application you're building:</span></span>

- <span data-ttu-id="51a39-362">“其他工具集”部分中的“.NET Core 跨平台开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="51a39-362">The **.NET Core cross-platform development** workload in the **Other Toolsets** section.</span></span>
- <span data-ttu-id="51a39-363">“Web 和云”部分中的“ASP.NET 和 Web 开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="51a39-363">The **ASP.NET and web development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="51a39-364">“Web 和云”部分中的“Azure 开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="51a39-364">The **Azure development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="51a39-365">“桌面和移动”部分中的“NET 桌面开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="51a39-365">The **.NET desktop development** workload in the **Desktop & Mobile** section.</span></span>

<span data-ttu-id="51a39-366">[![具有 .NET Core 工作负载的 Windows Visual Studio 2019](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="51a39-366">[![Windows Visual Studio 2019 with .NET Core workload](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span></span>

## <a name="install-alongside-visual-studio-code"></a><span data-ttu-id="51a39-367">随 Visual Studio Code 一起安装</span><span class="sxs-lookup"><span data-stu-id="51a39-367">Install alongside Visual Studio Code</span></span>

<span data-ttu-id="51a39-368">Visual Studio Code 是一个功能强大的轻量级源代码编辑器，可在桌面上运行。</span><span class="sxs-lookup"><span data-stu-id="51a39-368">Visual Studio Code is a powerful and lightweight source code editor that runs on your desktop.</span></span> <span data-ttu-id="51a39-369">Visual Studio Code 适用于 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="51a39-369">Visual Studio Code is available for Windows, macOS, and Linux.</span></span>

<span data-ttu-id="51a39-370">虽然 Visual Studio Code 不像 Visual Studio 一样附带自动的 .NET Core 安装程序，但添加 .NET Core 支持非常简单。</span><span class="sxs-lookup"><span data-stu-id="51a39-370">While Visual Studio Code doesn't come with an automated .NET Core installer like Visual Studio does, adding .NET Core support is simple.</span></span>

01. <span data-ttu-id="51a39-371">[下载并安装 Visual Studio Code](https://code.visualstudio.com/Download)。</span><span class="sxs-lookup"><span data-stu-id="51a39-371">[Download and install Visual Studio Code](https://code.visualstudio.com/Download).</span></span>
01. <span data-ttu-id="51a39-372">[下载并安装 .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="51a39-372">[Download and install the .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core).</span></span>
01. <span data-ttu-id="51a39-373">[从 Visual Studio Code 市场安装 C# 扩展](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)。</span><span class="sxs-lookup"><span data-stu-id="51a39-373">[Install the C# extension from the Visual Studio Code marketplace](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="51a39-374">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="51a39-374">Windows Installer</span></span>

<span data-ttu-id="51a39-375">适用于 .NET 的[下载页面](https://dotnet.microsoft.com/download/dotnet-core)提供了 Windows Installer 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="51a39-375">The [download page](https://dotnet.microsoft.com/download/dotnet-core) for .NET provides Windows Installer executables.</span></span>

<span data-ttu-id="51a39-376">使用 MSI 文件安装 .NET< 时，可以通过设置 `DOTNETHOME_X64` 和 `DOTNETHOME_X86` 参数来自定义安装路径：</span><span class="sxs-lookup"><span data-stu-id="51a39-376">When you use the MSI files to install .NET< you can customize the installation path by setting the `DOTNETHOME_X64` and `DOTNETHOME_X86` parameters:</span></span>

```console
dotnet-sdk-3.1.301-win-x64.exe DOTNETHOME_X64="F:\dotnet\x64" DOTNETHOME_X86="F:\dotnet\x86"
```

## <a name="download-and-manually-install"></a><span data-ttu-id="51a39-377">下载并手动安装</span><span class="sxs-lookup"><span data-stu-id="51a39-377">Download and manually install</span></span>

<span data-ttu-id="51a39-378">除了使用适用于 .NET 的 Windows 安装程序，还可以下载并手动安装 SDK 或运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-378">As an alternative to the Windows installers for .NET, you can download and manually install the SDK or runtime.</span></span> <span data-ttu-id="51a39-379">手动安装通常作为持续集成测试的一部分执行。</span><span class="sxs-lookup"><span data-stu-id="51a39-379">Manual install is usually performed as part of continuous integration testing.</span></span> <span data-ttu-id="51a39-380">对于开发人员或用户，一般使用[安装程序](https://dotnet.microsoft.com/download/dotnet-core)会更好。</span><span class="sxs-lookup"><span data-stu-id="51a39-380">For a developer or user, it's generally better to use an [installer](https://dotnet.microsoft.com/download/dotnet-core).</span></span>

<span data-ttu-id="51a39-381">在下载 .NET SDK 和 .NET 运行时后，可以手动安装它们。</span><span class="sxs-lookup"><span data-stu-id="51a39-381">Both .NET SDK and .NET Runtime can be manually installed after they've been downloaded.</span></span> <span data-ttu-id="51a39-382">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="51a39-382">If you install .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="51a39-383">首先，从以下站点之一下载 SDK 或运行时的二进制版本：</span><span class="sxs-lookup"><span data-stu-id="51a39-383">First, download a binary release for either the SDK or the runtime from one of the following sites:</span></span>

- [<span data-ttu-id="51a39-384">.NET 5.0 下载</span><span class="sxs-lookup"><span data-stu-id="51a39-384">.NET 5.0 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet/5.0)
- [<span data-ttu-id="51a39-385">.NET Core 3.1 下载</span><span class="sxs-lookup"><span data-stu-id="51a39-385">.NET Core 3.1 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [<span data-ttu-id="51a39-386">.NET Core 2.1 下载</span><span class="sxs-lookup"><span data-stu-id="51a39-386">.NET Core 2.1 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core/2.1)
- [<span data-ttu-id="51a39-387">所有 .NET Core 下载项</span><span class="sxs-lookup"><span data-stu-id="51a39-387">All .NET Core downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

<span data-ttu-id="51a39-388">创建要将 .NET 提取到的目录，例如 `%USERPROFILE%\dotnet`。</span><span class="sxs-lookup"><span data-stu-id="51a39-388">Create a directory to extract .NET to, for example `%USERPROFILE%\dotnet`.</span></span> <span data-ttu-id="51a39-389">然后，将下载的 zip 文件提取到该目录中。</span><span class="sxs-lookup"><span data-stu-id="51a39-389">Then, extract the downloaded zip file into that directory.</span></span>

<span data-ttu-id="51a39-390">默认情况下，.NET CLI 命令和应用不会使用通过这种方式安装的 .NET，并且你必须显式选择才能使用它。</span><span class="sxs-lookup"><span data-stu-id="51a39-390">By default, .NET CLI commands and apps won't use .NET installed in this way and you must explicitly choose to use it.</span></span> <span data-ttu-id="51a39-391">为此，请更改用于启动应用程序的环境变量：</span><span class="sxs-lookup"><span data-stu-id="51a39-391">To do so, change the environment variables with which an application is started:</span></span>

```console
set DOTNET_ROOT=%USERPROFILE%\dotnet
set PATH=%USERPROFILE%\dotnet;%PATH%
set DOTNET_MULTILEVEL_LOOKUP=0
```

<span data-ttu-id="51a39-392">使用此方法可以将多个版本安装到不同的位置，然后通过使用指向安装位置的环境变量运行应用程序来明确选择应用程序应使用哪个安装位置。</span><span class="sxs-lookup"><span data-stu-id="51a39-392">This approach lets you install multiple versions into separate locations, then explicitly choose which install location an application should use by running the application with environment variables pointing at that location.</span></span>

<span data-ttu-id="51a39-393">将 `DOTNET_MULTILEVEL_LOOKUP` 设置为 `0` 时，.NET 将忽略任何全局安装的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="51a39-393">When `DOTNET_MULTILEVEL_LOOKUP` is set to `0`, .NET ignores any globally installed .NET version.</span></span> <span data-ttu-id="51a39-394">删除环境设置，让 .NET 在选择用于运行应用程序的最佳框架时考虑默认的全局安装位置。</span><span class="sxs-lookup"><span data-stu-id="51a39-394">Remove that environment setting to let .NET consider the default global install location when selecting the best framework for running the application.</span></span> <span data-ttu-id="51a39-395">默认值通常为 `C:\Program Files\dotnet`，这是安装 .NET 的安装程序所在的位置。</span><span class="sxs-lookup"><span data-stu-id="51a39-395">The default is typically `C:\Program Files\dotnet`, which is where the installers install .NET.</span></span>

## <a name="docker"></a><span data-ttu-id="51a39-396">Docker</span><span class="sxs-lookup"><span data-stu-id="51a39-396">Docker</span></span>

<span data-ttu-id="51a39-397">容器提供了一种将应用程序与主机系统的其余部分隔离的轻量级方法。</span><span class="sxs-lookup"><span data-stu-id="51a39-397">Containers provide a lightweight way to isolate your application from the rest of the host system.</span></span> <span data-ttu-id="51a39-398">同一计算机上的容器只共享内核，并使用为应用程序提供的资源。</span><span class="sxs-lookup"><span data-stu-id="51a39-398">Containers on the same machine share just the kernel and use resources given to your application.</span></span>

<span data-ttu-id="51a39-399">.NET 可在 Docker 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="51a39-399">.NET can run in a Docker container.</span></span> <span data-ttu-id="51a39-400">官方 .NET Docker 映像发布到 Microsoft 容器注册表 (MCR)，用户可在 [Microsoft.NET Docker Hub 存储库](https://hub.docker.com/_/microsoft-dotnet)中找到这些映像。</span><span class="sxs-lookup"><span data-stu-id="51a39-400">Official .NET Docker images are published to the Microsoft Container Registry (MCR) and are discoverable at the [Microsoft .NET Docker Hub repository](https://hub.docker.com/_/microsoft-dotnet).</span></span> <span data-ttu-id="51a39-401">每个存储库包含 .NET（SDK 或运行时）和可以使用的操作系统的不同组合的映像。</span><span class="sxs-lookup"><span data-stu-id="51a39-401">Each repository contains images for different combinations of the .NET (SDK or Runtime) and OS that you can use.</span></span>

<span data-ttu-id="51a39-402">Microsoft 提供适合特定场景的映像。</span><span class="sxs-lookup"><span data-stu-id="51a39-402">Microsoft provides images that are tailored for specific scenarios.</span></span> <span data-ttu-id="51a39-403">例如，[ASP.NET Core 存储库](https://hub.docker.com/_/microsoft-dotnet-aspnet)提供针对在生产环境中运行 ASP.NET Core 应用生成的映像。</span><span class="sxs-lookup"><span data-stu-id="51a39-403">For example, the [ASP.NET Core repository](https://hub.docker.com/_/microsoft-dotnet-aspnet) provides images that are built for running ASP.NET Core apps in production.</span></span>

<span data-ttu-id="51a39-404">有关在 Docker 容器中使用 .NET 的详细信息，请参阅 [.NET 和 Docker 简介](../docker/introduction.md)和[示例](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-404">For more information about using .NET in a Docker container, see [Introduction to .NET and Docker](../docker/introduction.md) and [Samples](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="51a39-405">后续步骤</span><span class="sxs-lookup"><span data-stu-id="51a39-405">Next steps</span></span>

- <span data-ttu-id="51a39-406">[如何检查是否已安装 .NET](how-to-detect-installed-versions.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="51a39-406">[How to check if .NET is already installed](how-to-detect-installed-versions.md?pivots=os-windows).</span></span>
- <span data-ttu-id="51a39-407">[教程：Hello World 教程](../tutorials/with-visual-studio.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-407">[Tutorial: Hello World tutorial](../tutorials/with-visual-studio.md).</span></span>
- <span data-ttu-id="51a39-408">[教程：使用 Visual Studio Code 创建一个新应用](../tutorials/with-visual-studio-code.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-408">[Tutorial: Create a new app with Visual Studio Code](../tutorials/with-visual-studio-code.md).</span></span>
- <span data-ttu-id="51a39-409">[教程：使 .NET Core 应用容器化](../docker/build-container.md)。</span><span class="sxs-lookup"><span data-stu-id="51a39-409">[Tutorial: Containerize a .NET Core app](../docker/build-container.md).</span></span>

[esu]: /troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq

---
title: SDK 样式项目中的目标框架 - .NET
description: 了解用于 .NET 应用和库的目标框架。
ms.date: 11/06/2020
ms.prod: dotnet
ms.custom: updateeachrelease
ms.technology: dotnet-standard
ms.openlocfilehash: 7a3dcd61c330607bacf0d05dbd775c62cfa15b37
ms.sourcegitcommit: c0b803bffaf101e12f071faf94ca21b46d04ff30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/24/2020
ms.locfileid: "97765054"
---
# <a name="target-frameworks-in-sdk-style-projects"></a><span data-ttu-id="f9b12-103">SDK 样式项目中的目标框架</span><span class="sxs-lookup"><span data-stu-id="f9b12-103">Target frameworks in SDK-style projects</span></span>

<span data-ttu-id="f9b12-104">以应用或库中的框架为目标时，需要指定想要向应用或库提供的 API 集。</span><span class="sxs-lookup"><span data-stu-id="f9b12-104">When you target a framework in an app or library, you're specifying the set of APIs that you'd like to make available to the app or library.</span></span> <span data-ttu-id="f9b12-105">使用目标框架名字对象 (TFM) 在项目文件中指定目标框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-105">You specify the target framework in your project file using a target framework moniker (TFM).</span></span>

<span data-ttu-id="f9b12-106">应用或库可以使用 [.NET Standard](net-standard.md) 版本作为目标。</span><span class="sxs-lookup"><span data-stu-id="f9b12-106">An app or library can target a version of [.NET Standard](net-standard.md).</span></span> <span data-ttu-id="f9b12-107">.NET Standard 版本表示所有 .NET 实现中的标准化 API 集。</span><span class="sxs-lookup"><span data-stu-id="f9b12-107">.NET Standard versions represent standardized sets of APIs across all .NET implementations.</span></span> <span data-ttu-id="f9b12-108">例如，库可以使用 .NET Standard 1.6 作为目标，并获得对可使用相同基本代码跨 .NET Core 和 .NET Framework 工作的 API 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f9b12-108">For example, a library can target .NET Standard 1.6 and gain access to APIs that function across .NET Core and .NET Framework using the same codebase.</span></span>

<span data-ttu-id="f9b12-109">应用或库还能以一个特定 .NET 实现为目标，获得特定于实现的 API 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f9b12-109">An app or library can also target a specific .NET implementation to gain access to implementation-specific APIs.</span></span> <span data-ttu-id="f9b12-110">例如，面向 Xamarin.iOS 的应用（如 `Xamarin.iOS10`）有权访问 Xamarin 提供的适用于 iOS 10 的 iOS API 包装器；面向通用 Windows 平台 (UWP) 的应用（如 `uap10.0`）有权访问为运行 Windows 10 的设备编译的 API。</span><span class="sxs-lookup"><span data-stu-id="f9b12-110">For example, an app that targets Xamarin.iOS (for example, `Xamarin.iOS10`) has access to Xamarin-provided iOS API wrappers for iOS 10, or an app that targets Universal Windows Platform (UWP, `uap10.0`) has access to APIs that compile for devices that run Windows 10.</span></span>

<span data-ttu-id="f9b12-111">对于某些目标框架（例如 .NET Framework），API 由框架在系统上安装的程序集定义，并且可能包括应用程序框架 API（例如 ASP.NET）。</span><span class="sxs-lookup"><span data-stu-id="f9b12-111">For some target frameworks, such as .NET Framework, the APIs are defined by the assemblies that the framework installs on a system and may include application framework APIs (for example, ASP.NET).</span></span>

<span data-ttu-id="f9b12-112">对于基于包的目标框架（例如 .NET 5、.NET Core 和 .NET Standard），API 由应用或库中包含的 NuGet 包定义。</span><span class="sxs-lookup"><span data-stu-id="f9b12-112">For package-based target frameworks (for example, .NET 5, .NET Core, and .NET Standard), the APIs are defined by the NuGet packages included in the app or library.</span></span>

## <a name="latest-versions"></a><span data-ttu-id="f9b12-113">最新版本</span><span class="sxs-lookup"><span data-stu-id="f9b12-113">Latest versions</span></span>

<span data-ttu-id="f9b12-114">下表定义了最常见的目标框架、如何引用这些框架，以及它们实现的 [.NET Standard](net-standard.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="f9b12-114">The following table defines the most common target frameworks, how they're referenced, and which version of [.NET Standard](net-standard.md) they implement.</span></span> <span data-ttu-id="f9b12-115">这些目标框架版本是最新的稳定版本。</span><span class="sxs-lookup"><span data-stu-id="f9b12-115">These target framework versions are the latest stable versions.</span></span> <span data-ttu-id="f9b12-116">预览版不会显示。</span><span class="sxs-lookup"><span data-stu-id="f9b12-116">Pre-release versions aren't shown.</span></span> <span data-ttu-id="f9b12-117">目标框架名字对象 (TFM) 是一个标准化令牌格式，用于指定 .NET 应用或库的目标框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-117">A target framework moniker (TFM) is a standardized token format for specifying the target framework of a .NET app or library.</span></span>

| <span data-ttu-id="f9b12-118">目标框架</span><span class="sxs-lookup"><span data-stu-id="f9b12-118">Target framework</span></span>      | <span data-ttu-id="f9b12-119">最新</span><span class="sxs-lookup"><span data-stu-id="f9b12-119">Latest</span></span> <br/> <span data-ttu-id="f9b12-120">稳定版本</span><span class="sxs-lookup"><span data-stu-id="f9b12-120">stable version</span></span> | <span data-ttu-id="f9b12-121">目标框架名字对象 (TFM)</span><span class="sxs-lookup"><span data-stu-id="f9b12-121">Target framework moniker (TFM)</span></span> | <span data-ttu-id="f9b12-122">已实现</span><span class="sxs-lookup"><span data-stu-id="f9b12-122">Implemented</span></span> <br/> <span data-ttu-id="f9b12-123">.NET Standard 版本</span><span class="sxs-lookup"><span data-stu-id="f9b12-123">.NET Standard version</span></span> |
| :-: | :-: | :-: | :-: |
| <span data-ttu-id="f9b12-124">.NET 5</span><span class="sxs-lookup"><span data-stu-id="f9b12-124">.NET 5</span></span>                | <span data-ttu-id="f9b12-125">5.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-125">5.0</span></span>                         | <span data-ttu-id="f9b12-126">net5.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-126">net5.0</span></span>                         | <span data-ttu-id="f9b12-127">空值</span><span class="sxs-lookup"><span data-stu-id="f9b12-127">N/A</span></span>                                     |
| <span data-ttu-id="f9b12-128">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="f9b12-128">.NET Standard</span></span>         | <span data-ttu-id="f9b12-129">2.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-129">2.1</span></span>                         | <span data-ttu-id="f9b12-130">netstandard2.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-130">netstandard2.1</span></span>                 | <span data-ttu-id="f9b12-131">空值</span><span class="sxs-lookup"><span data-stu-id="f9b12-131">N/A</span></span>                                     |
| <span data-ttu-id="f9b12-132">.NET Core</span><span class="sxs-lookup"><span data-stu-id="f9b12-132">.NET Core</span></span>             | <span data-ttu-id="f9b12-133">3.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-133">3.1</span></span>                         | <span data-ttu-id="f9b12-134">netcoreapp3.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-134">netcoreapp3.1</span></span>                  | <span data-ttu-id="f9b12-135">2.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-135">2.1</span></span>                                     |
| <span data-ttu-id="f9b12-136">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="f9b12-136">.NET Framework</span></span>        | <span data-ttu-id="f9b12-137">4.8</span><span class="sxs-lookup"><span data-stu-id="f9b12-137">4.8</span></span>                         | <span data-ttu-id="f9b12-138">net48</span><span class="sxs-lookup"><span data-stu-id="f9b12-138">net48</span></span>                          | <span data-ttu-id="f9b12-139">2.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-139">2.0</span></span>                                     |

## <a name="supported-target-frameworks"></a><span data-ttu-id="f9b12-140">支持的目标框架</span><span class="sxs-lookup"><span data-stu-id="f9b12-140">Supported target frameworks</span></span>

<span data-ttu-id="f9b12-141">目标框架通常由 TFM 引用。</span><span class="sxs-lookup"><span data-stu-id="f9b12-141">A target framework is typically referenced by a TFM.</span></span> <span data-ttu-id="f9b12-142">下表显示 .NET SDK 和 NuGet 客户端支持的目标框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-142">The following table shows the target frameworks supported by the .NET SDK and the NuGet client.</span></span> <span data-ttu-id="f9b12-143">等效项显示在括号内。</span><span class="sxs-lookup"><span data-stu-id="f9b12-143">Equivalents are shown within brackets.</span></span> <span data-ttu-id="f9b12-144">例如，`win81` 对于 `netcore451` 来说等效于 TFM。</span><span class="sxs-lookup"><span data-stu-id="f9b12-144">For example, `win81` is an equivalent TFM to `netcore451`.</span></span>

| <span data-ttu-id="f9b12-145">目标 Framework</span><span class="sxs-lookup"><span data-stu-id="f9b12-145">Target Framework</span></span>           | <span data-ttu-id="f9b12-146">TFM</span><span class="sxs-lookup"><span data-stu-id="f9b12-146">TFM</span></span> |
| -------------------------- | --- |
| <span data-ttu-id="f9b12-147">.NET 5（和 .NET Core）</span><span class="sxs-lookup"><span data-stu-id="f9b12-147">.NET 5 (and .NET Core)</span></span>     | <span data-ttu-id="f9b12-148">netcoreapp1.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-148">netcoreapp1.0</span></span><br><span data-ttu-id="f9b12-149">netcoreapp1.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-149">netcoreapp1.1</span></span><br><span data-ttu-id="f9b12-150">netcoreapp2.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-150">netcoreapp2.0</span></span><br><span data-ttu-id="f9b12-151">netcoreapp2.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-151">netcoreapp2.1</span></span><br><span data-ttu-id="f9b12-152">netcoreapp2.2</span><span class="sxs-lookup"><span data-stu-id="f9b12-152">netcoreapp2.2</span></span><br><span data-ttu-id="f9b12-153">netcoreapp3.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-153">netcoreapp3.0</span></span><br><span data-ttu-id="f9b12-154">netcoreapp3.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-154">netcoreapp3.1</span></span><br><span data-ttu-id="f9b12-155">net5.0\*</span><span class="sxs-lookup"><span data-stu-id="f9b12-155">net5.0\*</span></span> |
| <span data-ttu-id="f9b12-156">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="f9b12-156">.NET Standard</span></span>              | <span data-ttu-id="f9b12-157">netstandard1.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-157">netstandard1.0</span></span><br><span data-ttu-id="f9b12-158">netstandard1.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-158">netstandard1.1</span></span><br><span data-ttu-id="f9b12-159">netstandard1.2</span><span class="sxs-lookup"><span data-stu-id="f9b12-159">netstandard1.2</span></span><br><span data-ttu-id="f9b12-160">netstandard1.3</span><span class="sxs-lookup"><span data-stu-id="f9b12-160">netstandard1.3</span></span><br><span data-ttu-id="f9b12-161">netstandard1.4</span><span class="sxs-lookup"><span data-stu-id="f9b12-161">netstandard1.4</span></span><br><span data-ttu-id="f9b12-162">netstandard1.5</span><span class="sxs-lookup"><span data-stu-id="f9b12-162">netstandard1.5</span></span><br><span data-ttu-id="f9b12-163">netstandard1.6</span><span class="sxs-lookup"><span data-stu-id="f9b12-163">netstandard1.6</span></span><br><span data-ttu-id="f9b12-164">netstandard2.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-164">netstandard2.0</span></span><br><span data-ttu-id="f9b12-165">netstandard2.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-165">netstandard2.1</span></span> |
| <span data-ttu-id="f9b12-166">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="f9b12-166">.NET Framework</span></span>             | <span data-ttu-id="f9b12-167">net11</span><span class="sxs-lookup"><span data-stu-id="f9b12-167">net11</span></span><br><span data-ttu-id="f9b12-168">net20</span><span class="sxs-lookup"><span data-stu-id="f9b12-168">net20</span></span><br><span data-ttu-id="f9b12-169">net35</span><span class="sxs-lookup"><span data-stu-id="f9b12-169">net35</span></span><br><span data-ttu-id="f9b12-170">net40</span><span class="sxs-lookup"><span data-stu-id="f9b12-170">net40</span></span><br><span data-ttu-id="f9b12-171">net403</span><span class="sxs-lookup"><span data-stu-id="f9b12-171">net403</span></span><br><span data-ttu-id="f9b12-172">net45</span><span class="sxs-lookup"><span data-stu-id="f9b12-172">net45</span></span><br><span data-ttu-id="f9b12-173">net451</span><span class="sxs-lookup"><span data-stu-id="f9b12-173">net451</span></span><br><span data-ttu-id="f9b12-174">net452</span><span class="sxs-lookup"><span data-stu-id="f9b12-174">net452</span></span><br><span data-ttu-id="f9b12-175">net46</span><span class="sxs-lookup"><span data-stu-id="f9b12-175">net46</span></span><br><span data-ttu-id="f9b12-176">net461</span><span class="sxs-lookup"><span data-stu-id="f9b12-176">net461</span></span><br><span data-ttu-id="f9b12-177">net462</span><span class="sxs-lookup"><span data-stu-id="f9b12-177">net462</span></span><br><span data-ttu-id="f9b12-178">net47</span><span class="sxs-lookup"><span data-stu-id="f9b12-178">net47</span></span><br><span data-ttu-id="f9b12-179">net471</span><span class="sxs-lookup"><span data-stu-id="f9b12-179">net471</span></span><br><span data-ttu-id="f9b12-180">net472</span><span class="sxs-lookup"><span data-stu-id="f9b12-180">net472</span></span><br><span data-ttu-id="f9b12-181">net48</span><span class="sxs-lookup"><span data-stu-id="f9b12-181">net48</span></span> |
| <span data-ttu-id="f9b12-182">Windows 应用商店</span><span class="sxs-lookup"><span data-stu-id="f9b12-182">Windows Store</span></span>              | <span data-ttu-id="f9b12-183">netcore [netcore45]</span><span class="sxs-lookup"><span data-stu-id="f9b12-183">netcore [netcore45]</span></span><br><span data-ttu-id="f9b12-184">netcore45 [win] [win8]</span><span class="sxs-lookup"><span data-stu-id="f9b12-184">netcore45 [win] [win8]</span></span><br><span data-ttu-id="f9b12-185">netcore451 [win81]</span><span class="sxs-lookup"><span data-stu-id="f9b12-185">netcore451 [win81]</span></span> |
| <span data-ttu-id="f9b12-186">.NET Micro Framework</span><span class="sxs-lookup"><span data-stu-id="f9b12-186">.NET Micro Framework</span></span>       | <span data-ttu-id="f9b12-187">netmf</span><span class="sxs-lookup"><span data-stu-id="f9b12-187">netmf</span></span> |
| <span data-ttu-id="f9b12-188">Silverlight</span><span class="sxs-lookup"><span data-stu-id="f9b12-188">Silverlight</span></span>                | <span data-ttu-id="f9b12-189">sl4</span><span class="sxs-lookup"><span data-stu-id="f9b12-189">sl4</span></span><br><span data-ttu-id="f9b12-190">sl5</span><span class="sxs-lookup"><span data-stu-id="f9b12-190">sl5</span></span> |
| <span data-ttu-id="f9b12-191">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="f9b12-191">Windows Phone</span></span>              | <span data-ttu-id="f9b12-192">wp [wp7]</span><span class="sxs-lookup"><span data-stu-id="f9b12-192">wp [wp7]</span></span><br><span data-ttu-id="f9b12-193">wp7</span><span class="sxs-lookup"><span data-stu-id="f9b12-193">wp7</span></span><br><span data-ttu-id="f9b12-194">wp75</span><span class="sxs-lookup"><span data-stu-id="f9b12-194">wp75</span></span><br><span data-ttu-id="f9b12-195">wp8</span><span class="sxs-lookup"><span data-stu-id="f9b12-195">wp8</span></span><br><span data-ttu-id="f9b12-196">wp81</span><span class="sxs-lookup"><span data-stu-id="f9b12-196">wp81</span></span><br><span data-ttu-id="f9b12-197">wpa81</span><span class="sxs-lookup"><span data-stu-id="f9b12-197">wpa81</span></span> |
| <span data-ttu-id="f9b12-198">通用 Windows 平台</span><span class="sxs-lookup"><span data-stu-id="f9b12-198">Universal Windows Platform</span></span> | <span data-ttu-id="f9b12-199">uap [uap10.0]</span><span class="sxs-lookup"><span data-stu-id="f9b12-199">uap [uap10.0]</span></span><br><span data-ttu-id="f9b12-200">uap10.0 [win10] [netcore50]</span><span class="sxs-lookup"><span data-stu-id="f9b12-200">uap10.0 [win10] [netcore50]</span></span> |

<span data-ttu-id="f9b12-201">\* .NET 5.0 及更高版本的 TFM 包含特定于操作系统的变体。</span><span class="sxs-lookup"><span data-stu-id="f9b12-201">\* .NET 5.0 and later TFMs include operating system-specific variations.</span></span> <span data-ttu-id="f9b12-202">有关详细信息，请参阅下一节：[.NET 5 特定于 OS 的 TFM](#net-5-os-specific-tfms)。</span><span class="sxs-lookup"><span data-stu-id="f9b12-202">For more information, see the following section, [.NET 5 OS-specific TFMs](#net-5-os-specific-tfms).</span></span>

### <a name="net-5-os-specific-tfms"></a><span data-ttu-id="f9b12-203">.NET 5 特定于 OS 的 TFM</span><span class="sxs-lookup"><span data-stu-id="f9b12-203">.NET 5 OS-specific TFMs</span></span>

<span data-ttu-id="f9b12-204">对于每个 .NET 5.0 及更高版本的 TFM（例如 `net5.0`），都存在包含特定于 OS 的绑定的 TFM 变体。</span><span class="sxs-lookup"><span data-stu-id="f9b12-204">For each .NET 5.0 and later TFM, for example, `net5.0`, there are TFM variations that include OS-specific bindings.</span></span> <span data-ttu-id="f9b12-205">下表中显示了这些变体。</span><span class="sxs-lookup"><span data-stu-id="f9b12-205">These variations are shown in the following table.</span></span>

| <span data-ttu-id="f9b12-206">特定于 OS 的格式</span><span class="sxs-lookup"><span data-stu-id="f9b12-206">OS-specific format</span></span> | <span data-ttu-id="f9b12-207">示例</span><span class="sxs-lookup"><span data-stu-id="f9b12-207">Example</span></span>        |
|--------------------|----------------|
| <span data-ttu-id="f9b12-208">\<base-tfm>-android</span><span class="sxs-lookup"><span data-stu-id="f9b12-208">\<base-tfm>-android</span></span> | <span data-ttu-id="f9b12-209">net5.0-android</span><span class="sxs-lookup"><span data-stu-id="f9b12-209">net5.0-android</span></span> |
| <span data-ttu-id="f9b12-210">\<base-tfm>-ios</span><span class="sxs-lookup"><span data-stu-id="f9b12-210">\<base-tfm>-ios</span></span>     | <span data-ttu-id="f9b12-211">net5.0-ios</span><span class="sxs-lookup"><span data-stu-id="f9b12-211">net5.0-ios</span></span>     |
| <span data-ttu-id="f9b12-212">\<base-tfm>-macos</span><span class="sxs-lookup"><span data-stu-id="f9b12-212">\<base-tfm>-macos</span></span>   | <span data-ttu-id="f9b12-213">net5.0-macos</span><span class="sxs-lookup"><span data-stu-id="f9b12-213">net5.0-macos</span></span>   |
| <span data-ttu-id="f9b12-214">\<base-tfm>-tvos</span><span class="sxs-lookup"><span data-stu-id="f9b12-214">\<base-tfm>-tvos</span></span>    | <span data-ttu-id="f9b12-215">net5.0-tvos</span><span class="sxs-lookup"><span data-stu-id="f9b12-215">net5.0-tvos</span></span>    |
| <span data-ttu-id="f9b12-216">\<base-tfm>-watchos</span><span class="sxs-lookup"><span data-stu-id="f9b12-216">\<base-tfm>-watchos</span></span> | <span data-ttu-id="f9b12-217">net5.0-watchos</span><span class="sxs-lookup"><span data-stu-id="f9b12-217">net5.0-watchos</span></span> |
| <span data-ttu-id="f9b12-218">\<base-tfm>-windows</span><span class="sxs-lookup"><span data-stu-id="f9b12-218">\<base-tfm>-windows</span></span> | <span data-ttu-id="f9b12-219">net5.0-windows</span><span class="sxs-lookup"><span data-stu-id="f9b12-219">net5.0-windows</span></span> |

<span data-ttu-id="f9b12-220">`net5.0` TFM 仅包括跨平台工作的技术。</span><span class="sxs-lookup"><span data-stu-id="f9b12-220">The `net5.0` TFM only includes technologies that work cross-platform.</span></span> <span data-ttu-id="f9b12-221">指定特定于 OS 的 TFM 使特定于操作系统的 API 可供应用使用，例如 Windows 窗体或 iOS 绑定。</span><span class="sxs-lookup"><span data-stu-id="f9b12-221">Specifying an OS-specific TFM makes APIs that are specific to an operating system available to your app, for example, Windows Forms or iOS bindings.</span></span> <span data-ttu-id="f9b12-222">特定于 OS 的 TFM 还继承 `net5.0` TFM 可用的每个 API。</span><span class="sxs-lookup"><span data-stu-id="f9b12-222">OS-specific TFMs also inherit every API available to the `net5.0` TFM.</span></span>

<span data-ttu-id="f9b12-223">若要使应用可跨不同平台移植，你可以定位多个特定于 OS 的 TFM，并使用 `#if` 预处理器指令围绕特定于 OS 的 API 调用添加平台保护。</span><span class="sxs-lookup"><span data-stu-id="f9b12-223">To make your app portable across different platforms, you can target multiple OS-specific TFMs and add platform guards around OS-specific API calls using `#if` preprocessor directives.</span></span>

<span data-ttu-id="f9b12-224">下表显示了 .NET 5 TFM 与旧 .NET 版本的 TFM 的兼容性。</span><span class="sxs-lookup"><span data-stu-id="f9b12-224">The following table shows the compatibility of the .NET 5 TFMs with TFMs for previous .NET versions.</span></span>

| <span data-ttu-id="f9b12-225">TFM</span><span class="sxs-lookup"><span data-stu-id="f9b12-225">TFM</span></span>             | <span data-ttu-id="f9b12-226">可兼容对象</span><span class="sxs-lookup"><span data-stu-id="f9b12-226">Compatible with</span></span>                                            | <span data-ttu-id="f9b12-227">备注</span><span class="sxs-lookup"><span data-stu-id="f9b12-227">Notes</span></span> |
|-----------------|------------------------------------------------------------|-|
| <span data-ttu-id="f9b12-228">net5.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-228">net5.0</span></span>          | <span data-ttu-id="f9b12-229">net1..4（带有 NU1701 警告）</span><span class="sxs-lookup"><span data-stu-id="f9b12-229">net1..4 (with NU1701 warning)</span></span><br /><span data-ttu-id="f9b12-230">netcoreapp1..3.1 （引用 WinForms 或 WPF 时出现警告）</span><span class="sxs-lookup"><span data-stu-id="f9b12-230">netcoreapp1..3.1 (warning when WinForms or WPF is referenced)</span></span><br /><span data-ttu-id="f9b12-231">netstandard1..2.1</span><span class="sxs-lookup"><span data-stu-id="f9b12-231">netstandard1..2.1</span></span> | |
| <span data-ttu-id="f9b12-232">net5.0-android</span><span class="sxs-lookup"><span data-stu-id="f9b12-232">net5.0-android</span></span>  | <span data-ttu-id="f9b12-233">xamarin.android（以及从 `net5.0` 继承的所有其他内容）</span><span class="sxs-lookup"><span data-stu-id="f9b12-233">xamarin.android (plus everything else inherited from `net5.0`)</span></span> | |
| <span data-ttu-id="f9b12-234">net5.0-ios</span><span class="sxs-lookup"><span data-stu-id="f9b12-234">net5.0-ios</span></span>      | <span data-ttu-id="f9b12-235">xamarin.ios（以及从 `net5.0` 继承的所有其他内容）</span><span class="sxs-lookup"><span data-stu-id="f9b12-235">xamarin.ios (plus everything else inherited from `net5.0`)</span></span> | |
| <span data-ttu-id="f9b12-236">net5.0-macos</span><span class="sxs-lookup"><span data-stu-id="f9b12-236">net5.0-macos</span></span>    | <span data-ttu-id="f9b12-237">xamarin.mac（以及从 `net5.0` 继承的所有其他内容）</span><span class="sxs-lookup"><span data-stu-id="f9b12-237">xamarin.mac (plus everything else inherited from `net5.0`)</span></span> | |
| <span data-ttu-id="f9b12-238">net5.0-tvos</span><span class="sxs-lookup"><span data-stu-id="f9b12-238">net5.0-tvos</span></span>     | <span data-ttu-id="f9b12-239">xamarin.tvos（以及从 `net5.0` 继承的所有其他内容）</span><span class="sxs-lookup"><span data-stu-id="f9b12-239">xamarin.tvos (plus everything else inherited from `net5.0`)</span></span> | |
| <span data-ttu-id="f9b12-240">net5.0-watchos</span><span class="sxs-lookup"><span data-stu-id="f9b12-240">net5.0-watchos</span></span>  | <span data-ttu-id="f9b12-241">xamarin.watchos（以及从 `net5.0` 继承的所有其他内容）</span><span class="sxs-lookup"><span data-stu-id="f9b12-241">xamarin.watchos (plus everything else inherited from `net5.0`)</span></span> | |
| <span data-ttu-id="f9b12-242">net5.0-windows</span><span class="sxs-lookup"><span data-stu-id="f9b12-242">net5.0-windows</span></span>  | <span data-ttu-id="f9b12-243">netcoreapp1..3.1（以及从 `net5.0` 继承的所有其他内容）</span><span class="sxs-lookup"><span data-stu-id="f9b12-243">netcoreapp1..3.1 (plus everything else inherited from `net5.0`)</span></span> | <span data-ttu-id="f9b12-244">包括 WinForms、WPF 和 UWP API。</span><span class="sxs-lookup"><span data-stu-id="f9b12-244">Includes WinForms, WPF, and UWP APIs.</span></span><br /><span data-ttu-id="f9b12-245">有关信息，请参阅[在桌面应用中调用 Windows 运行时 API](/windows/apps/desktop/modernize/desktop-to-uwp-enhance)。</span><span class="sxs-lookup"><span data-stu-id="f9b12-245">For information, see [Call Windows Runtime APIs in desktop apps](/windows/apps/desktop/modernize/desktop-to-uwp-enhance).</span></span> |

#### <a name="suggested-targets"></a><span data-ttu-id="f9b12-246">建议的目标</span><span class="sxs-lookup"><span data-stu-id="f9b12-246">Suggested targets</span></span>

<span data-ttu-id="f9b12-247">使用以下准则确定在应用中使用哪种 TFM：</span><span class="sxs-lookup"><span data-stu-id="f9b12-247">Use these guidelines to determine which TFM to use in your app:</span></span>

- <span data-ttu-id="f9b12-248">可移植到多个平台的应用应面向 `net5.0`。</span><span class="sxs-lookup"><span data-stu-id="f9b12-248">Apps that are portable to multiple platforms should target `net5.0`.</span></span> <span data-ttu-id="f9b12-249">这包括大多数库，但也包含 ASP.NET Core 和实体框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-249">This includes most libraries but also ASP.NET Core and Entity Framework.</span></span>

- <span data-ttu-id="f9b12-250">特定于平台的库应面向特定于平台的风格。</span><span class="sxs-lookup"><span data-stu-id="f9b12-250">Platform-specific libraries should target platform-specific flavors.</span></span> <span data-ttu-id="f9b12-251">例如，WinForms 和 WPF 项目应面向 `net5.0-windows`。</span><span class="sxs-lookup"><span data-stu-id="f9b12-251">For example, WinForms and WPF projects should target `net5.0-windows`.</span></span>

- <span data-ttu-id="f9b12-252">跨平台应用程序模型（Xamarin Forms、ASP.NET Core）和网桥包 (Xamarin Essentials) 应至少面向 `net5.0`，但也可以面向其他特定于平台的风格来支持更多的 API 或功能。</span><span class="sxs-lookup"><span data-stu-id="f9b12-252">Cross-platform application models (Xamarin Forms, ASP.NET Core) and bridge packs (Xamarin Essentials) should at least target `net5.0`, but might also target additional platform-specific flavors to light-up more APIs or features.</span></span>

#### <a name="os-version-in-tfms"></a><span data-ttu-id="f9b12-253">TFM 中的 OS 版本</span><span class="sxs-lookup"><span data-stu-id="f9b12-253">OS version in TFMs</span></span>

<span data-ttu-id="f9b12-254">你还可以在 TFM 的末尾指定可选的 OS 版本，例如 `net5.0-ios13.0`，该版本指示应用可用的 API。</span><span class="sxs-lookup"><span data-stu-id="f9b12-254">You can also specify an optional OS version at the end of the TFM, for example, `net5.0-ios13.0`, which indicates what APIs are available to your app.</span></span> <span data-ttu-id="f9b12-255">（.NET 5 SDK 将更新，以在发布时包含对较新 OS 版本的支持。）若要访问新发布的 API，请增加 TFM 中的 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="f9b12-255">(The .NET 5 SDK will be updated to include support for newer OS versions as they are released.) To gain access to newly released APIs, increment the OS version in the TFM.</span></span> <span data-ttu-id="f9b12-256">通过将 `SupportedOSPlatformVersion` 元素添加到项目文件，仍可以使应用与旧 OS 版本兼容（并在调用更高版本的 API 时添加防护）。</span><span class="sxs-lookup"><span data-stu-id="f9b12-256">You can still make your app compatible with earlier OS versions (and add guards around calls to later-version APIs) by adding the `SupportedOSPlatformVersion` element to your project file.</span></span> <span data-ttu-id="f9b12-257">`SupportedOSPlatformVersion` 元素指示运行应用所需的最低 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="f9b12-257">The `SupportedOSPlatformVersion` element indicates the minimum OS version required to run your app.</span></span>

<span data-ttu-id="f9b12-258">例如，以下项目文件摘录指定 iOS 14 API 可用于应用，但它可以在 iOS 13 或更高版本的计算机上运行。</span><span class="sxs-lookup"><span data-stu-id="f9b12-258">For example, the following project file excerpt specifies that iOS 14 APIs are available to the app, but it can run on iOS 13 or later machines.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <TargetFramework>net5.0-ios14.0</TargetFramework>
    <SupportedOSPlatformVersion>13.0</SupportedOSPlatformVersion> (minimum os platform version)
  </PropertyGroup>

  ...

</Project>
```

## <a name="how-to-specify-a-target-framework"></a><span data-ttu-id="f9b12-259">如何指定目标框架</span><span class="sxs-lookup"><span data-stu-id="f9b12-259">How to specify a target framework</span></span>

<span data-ttu-id="f9b12-260">在项目文件中指定目标框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-260">Target frameworks are specified in a project file.</span></span> <span data-ttu-id="f9b12-261">指定单个目标框架时，使用 [TargetFramework 元素](../core/project-sdk/msbuild-props.md#targetframework)。</span><span class="sxs-lookup"><span data-stu-id="f9b12-261">When a single target framework is specified, use the [TargetFramework element](../core/project-sdk/msbuild-props.md#targetframework).</span></span> <span data-ttu-id="f9b12-262">以下控制台应用项目文件演示了如何面向 .NET 5.0：</span><span class="sxs-lookup"><span data-stu-id="f9b12-262">The following console app project file demonstrates how to target .NET 5.0:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net5.0</TargetFramework>
  </PropertyGroup>

</Project>
```

<span data-ttu-id="f9b12-263">指定多个目标框架时，可有条件地为每个目标框架引用程序集。</span><span class="sxs-lookup"><span data-stu-id="f9b12-263">When you specify multiple target frameworks, you may conditionally reference assemblies for each target framework.</span></span> <span data-ttu-id="f9b12-264">在代码中，可使用具有 -if-then-else  逻辑的预处理器符号，有条件地针对这些程序集进行编译。</span><span class="sxs-lookup"><span data-stu-id="f9b12-264">In your code, you can conditionally compile against those assemblies by using preprocessor symbols with *if-then-else* logic.</span></span>

<span data-ttu-id="f9b12-265">以下库项目面向 .NET Standard (`netstandard1.4`) 和 .NET Framework（`net40` 和 `net45`）的 API。</span><span class="sxs-lookup"><span data-stu-id="f9b12-265">The following library project targets APIs of .NET Standard (`netstandard1.4`) and .NET Framework (`net40` and `net45`).</span></span> <span data-ttu-id="f9b12-266">将复数形式的 [TargetFrameworks 元素](../core/project-sdk/msbuild-props.md#targetframeworks)与多个目标框架一起使用。</span><span class="sxs-lookup"><span data-stu-id="f9b12-266">Use the plural [TargetFrameworks element](../core/project-sdk/msbuild-props.md#targetframeworks) with multiple target frameworks.</span></span> <span data-ttu-id="f9b12-267">为两个 .NET Framework TFM 编译库时，`Condition` 属性包括特定于实现的包：</span><span class="sxs-lookup"><span data-stu-id="f9b12-267">The `Condition` attributes include implementation-specific packages when the library is compiled for the two .NET Framework TFMs:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <TargetFrameworks>netstandard1.4;net40;net45</TargetFrameworks>
  </PropertyGroup>

  <!-- Conditionally obtain references for the .NET Framework 4.0 target -->
  <ItemGroup Condition=" '$(TargetFramework)' == 'net40' ">
    <Reference Include="System.Net" />
  </ItemGroup>

  <!-- Conditionally obtain references for the .NET Framework 4.5 target -->
  <ItemGroup Condition=" '$(TargetFramework)' == 'net45' ">
    <Reference Include="System.Net.Http" />
    <Reference Include="System.Threading.Tasks" />
  </ItemGroup>

</Project>
```

<span data-ttu-id="f9b12-268">在库或应用中，使用[预处理器指令](../csharp/language-reference/preprocessor-directives/preprocessor-if.md)编写条件代码，针对每个目标框架进行编译：</span><span class="sxs-lookup"><span data-stu-id="f9b12-268">Within your library or app, you write conditional code using [preprocessor directives](../csharp/language-reference/preprocessor-directives/preprocessor-if.md) to compile for each target framework:</span></span>

```csharp
public class MyClass
{
    static void Main()
    {
#if NET40
        Console.WriteLine("Target framework: .NET Framework 4.0");
#elif NET45
        Console.WriteLine("Target framework: .NET Framework 4.5");
#else
        Console.WriteLine("Target framework: .NET Standard 1.4");
#endif
    }
}
```

<span data-ttu-id="f9b12-269">使用 SDK 样式项目时，生成系统可识别预处理器符号，这些符号表示[支持的目标框架版本](#supported-target-frameworks)表中所示的目标框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-269">The build system is aware of preprocessor symbols representing the target frameworks shown in the [Supported target framework versions](#supported-target-frameworks) table when you're using SDK-style projects.</span></span> <span data-ttu-id="f9b12-270">使用表示 .NET Standard、.NET Core 或 .NET 5 TFM 的符号时，请用下划线替换点和连字符，并将小写字母更改为大写字母（例如，`netstandard1.4` 的符号为 `NETSTANDARD1_4`）。</span><span class="sxs-lookup"><span data-stu-id="f9b12-270">When using a symbol that represents a .NET Standard, .NET Core, or .NET 5 TFM, replace dots and hyphens with an underscore and change lowercase letters to uppercase (for example, the symbol for `netstandard1.4` is `NETSTANDARD1_4`).</span></span>

<span data-ttu-id="f9b12-271">.NET 目标框架的预处理器符号的完整列表如下：</span><span class="sxs-lookup"><span data-stu-id="f9b12-271">The complete list of preprocessor symbols for .NET target frameworks is:</span></span>

[!INCLUDE [Preprocessor symbols](../../includes/preprocessor-symbols.md)]

## <a name="deprecated-target-frameworks"></a><span data-ttu-id="f9b12-272">已弃用的目标框架</span><span class="sxs-lookup"><span data-stu-id="f9b12-272">Deprecated target frameworks</span></span>

<span data-ttu-id="f9b12-273">以下目标框架已弃用。</span><span class="sxs-lookup"><span data-stu-id="f9b12-273">The following target frameworks are deprecated.</span></span> <span data-ttu-id="f9b12-274">面向这些目标框架的包应迁移到指定的替代框架。</span><span class="sxs-lookup"><span data-stu-id="f9b12-274">Packages that target these target frameworks should migrate to the indicated replacements.</span></span>

| <span data-ttu-id="f9b12-275">已弃用的 TFM</span><span class="sxs-lookup"><span data-stu-id="f9b12-275">Deprecated TFM</span></span>                                                                             | <span data-ttu-id="f9b12-276">Replacement</span><span class="sxs-lookup"><span data-stu-id="f9b12-276">Replacement</span></span> |
| ------------------------------------------------------------------------------------------ | ----------- |
| <span data-ttu-id="f9b12-277">aspnet50</span><span class="sxs-lookup"><span data-stu-id="f9b12-277">aspnet50</span></span><br><span data-ttu-id="f9b12-278">aspnetcore50</span><span class="sxs-lookup"><span data-stu-id="f9b12-278">aspnetcore50</span></span><br><span data-ttu-id="f9b12-279">dnxcore50</span><span class="sxs-lookup"><span data-stu-id="f9b12-279">dnxcore50</span></span><br><span data-ttu-id="f9b12-280">dnx</span><span class="sxs-lookup"><span data-stu-id="f9b12-280">dnx</span></span><br><span data-ttu-id="f9b12-281">dnx45</span><span class="sxs-lookup"><span data-stu-id="f9b12-281">dnx45</span></span><br><span data-ttu-id="f9b12-282">dnx451</span><span class="sxs-lookup"><span data-stu-id="f9b12-282">dnx451</span></span><br><span data-ttu-id="f9b12-283">dnx452</span><span class="sxs-lookup"><span data-stu-id="f9b12-283">dnx452</span></span>                  | <span data-ttu-id="f9b12-284">netcoreapp</span><span class="sxs-lookup"><span data-stu-id="f9b12-284">netcoreapp</span></span>  |
| <span data-ttu-id="f9b12-285">dotnet</span><span class="sxs-lookup"><span data-stu-id="f9b12-285">dotnet</span></span><br><span data-ttu-id="f9b12-286">dotnet50</span><span class="sxs-lookup"><span data-stu-id="f9b12-286">dotnet50</span></span><br><span data-ttu-id="f9b12-287">dotnet51</span><span class="sxs-lookup"><span data-stu-id="f9b12-287">dotnet51</span></span><br><span data-ttu-id="f9b12-288">dotnet52</span><span class="sxs-lookup"><span data-stu-id="f9b12-288">dotnet52</span></span><br><span data-ttu-id="f9b12-289">dotnet53</span><span class="sxs-lookup"><span data-stu-id="f9b12-289">dotnet53</span></span><br><span data-ttu-id="f9b12-290">dotnet54</span><span class="sxs-lookup"><span data-stu-id="f9b12-290">dotnet54</span></span><br><span data-ttu-id="f9b12-291">dotnet55</span><span class="sxs-lookup"><span data-stu-id="f9b12-291">dotnet55</span></span><br><span data-ttu-id="f9b12-292">dotnet56</span><span class="sxs-lookup"><span data-stu-id="f9b12-292">dotnet56</span></span> | <span data-ttu-id="f9b12-293">netstandard</span><span class="sxs-lookup"><span data-stu-id="f9b12-293">netstandard</span></span> |
| <span data-ttu-id="f9b12-294">netcore50</span><span class="sxs-lookup"><span data-stu-id="f9b12-294">netcore50</span></span>                                                                                  | <span data-ttu-id="f9b12-295">uap10.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-295">uap10.0</span></span>     |
| <span data-ttu-id="f9b12-296">win</span><span class="sxs-lookup"><span data-stu-id="f9b12-296">win</span></span>                                                                                        | <span data-ttu-id="f9b12-297">netcore45</span><span class="sxs-lookup"><span data-stu-id="f9b12-297">netcore45</span></span>   |
| <span data-ttu-id="f9b12-298">win8</span><span class="sxs-lookup"><span data-stu-id="f9b12-298">win8</span></span>                                                                                       | <span data-ttu-id="f9b12-299">netcore45</span><span class="sxs-lookup"><span data-stu-id="f9b12-299">netcore45</span></span>   |
| <span data-ttu-id="f9b12-300">win81</span><span class="sxs-lookup"><span data-stu-id="f9b12-300">win81</span></span>                                                                                      | <span data-ttu-id="f9b12-301">netcore451</span><span class="sxs-lookup"><span data-stu-id="f9b12-301">netcore451</span></span>  |
| <span data-ttu-id="f9b12-302">win10</span><span class="sxs-lookup"><span data-stu-id="f9b12-302">win10</span></span>                                                                                      | <span data-ttu-id="f9b12-303">uap10.0</span><span class="sxs-lookup"><span data-stu-id="f9b12-303">uap10.0</span></span>     |
| <span data-ttu-id="f9b12-304">winrt</span><span class="sxs-lookup"><span data-stu-id="f9b12-304">winrt</span></span>                                                                                      | <span data-ttu-id="f9b12-305">netcore45</span><span class="sxs-lookup"><span data-stu-id="f9b12-305">netcore45</span></span>   |

## <a name="see-also"></a><span data-ttu-id="f9b12-306">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f9b12-306">See also</span></span>

- [<span data-ttu-id="f9b12-307">.NET 5 中的目标框架名称</span><span class="sxs-lookup"><span data-stu-id="f9b12-307">Target framework names in .NET 5</span></span>](https://github.com/dotnet/designs/blob/master/accepted/2020/net5/net5.md)
- [<span data-ttu-id="f9b12-308">使用跨平台工具开发库</span><span class="sxs-lookup"><span data-stu-id="f9b12-308">Developing Libraries with Cross Platform Tools</span></span>](../core/tutorials/libraries.md)
- [<span data-ttu-id="f9b12-309">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="f9b12-309">.NET Standard</span></span>](net-standard.md)
- [<span data-ttu-id="f9b12-310">.NET Core 版本控制</span><span class="sxs-lookup"><span data-stu-id="f9b12-310">.NET Core Versioning</span></span>](../core/versions/index.md)
- [<span data-ttu-id="f9b12-311">dotnet/standard GitHub 存储库</span><span class="sxs-lookup"><span data-stu-id="f9b12-311">dotnet/standard GitHub repository</span></span>](https://github.com/dotnet/standard)
- [<span data-ttu-id="f9b12-312">NuGet 工具 GitHub 存储库</span><span class="sxs-lookup"><span data-stu-id="f9b12-312">NuGet Tools GitHub Repository</span></span>](https://github.com/joelverhagen/NuGetTools)
- [<span data-ttu-id="f9b12-313">.NET 中的框架配置文件</span><span class="sxs-lookup"><span data-stu-id="f9b12-313">Framework Profiles in .NET</span></span>](https://blog.stephencleary.com/2012/05/framework-profiles-in-net.html)
- [<span data-ttu-id="f9b12-314">平台兼容性分析器</span><span class="sxs-lookup"><span data-stu-id="f9b12-314">Platform compatibility analyzer</span></span>](analyzers/platform-compat-analyzer.md)

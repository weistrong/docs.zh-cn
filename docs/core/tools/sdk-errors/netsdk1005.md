---
title: NETSDK1005 和 NETSDK1047：资产文件缺少目标
description: 如何解决资产文件缺少目标的问题。
author: sfoslund
ms.topic: error-reference
ms.date: 12/17/2020
f1_keywords:
- NETSDK1005
- NETSDK1047
ms.openlocfilehash: e3e7389adf6a9a715d44661a5f7cbae5efe299e4
ms.sourcegitcommit: 4b79862c5b41fbd86cf38f926f6a49516059f6f2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2020
ms.locfileid: "97678173"
---
# <a name="netsdk1005-and-netsdk1047-asset-file-is-missing-target"></a><span data-ttu-id="450b7-103">NETSDK1005 和 NETSDK1047：资产文件缺少目标</span><span class="sxs-lookup"><span data-stu-id="450b7-103">NETSDK1005 and NETSDK1047: Asset file is missing target</span></span>

<span data-ttu-id="450b7-104">本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="450b7-104">**This article applies to:** ✔️ .NET Core 2.1.100 SDK and later versions</span></span>

<span data-ttu-id="450b7-105">当 .NET SDK 发出错误 NETSDK1005 或 NETSDK1047 时，项目的资产文件缺失某个目标框架的相关信息。</span><span class="sxs-lookup"><span data-stu-id="450b7-105">When the .NET SDK issues error NETSDK1005 or NETSDK1047, the project's assets file is missing information on one of your target frameworks.</span></span> <span data-ttu-id="450b7-106">NuGet 在“obj”文件夹中写入名为 project.assets.json 的文件，.NET SDK 使用该文件来获取有关要传递到编译器的包的信息 。</span><span class="sxs-lookup"><span data-stu-id="450b7-106">NuGet writes a file named *project.assets.json* in the *obj* folder, and the .NET SDK uses it to get information about packages to pass into the compiler.</span></span> <span data-ttu-id="450b7-107">在 .NET 5 中，NuGet 添加了名为 `TargetFrameworkAlias` 的新字段，以便早期版本的 MSBuild 或 NuGet 在没有新字段的情况下生成资产文件。</span><span class="sxs-lookup"><span data-stu-id="450b7-107">In .NET 5, NuGet added a new field named `TargetFrameworkAlias`, so earlier versions of MSBuild or NuGet generate an assets file without the new field.</span></span> <span data-ttu-id="450b7-108">有关详细信息，请参阅[错误 NETSDK1005](https://developercommunity.visualstudio.com/content/problem/1248649/error-netsdk1005-assets-file-projectassetsjson-doe.html)。</span><span class="sxs-lookup"><span data-stu-id="450b7-108">For more information, see [error NETSDK1005](https://developercommunity.visualstudio.com/content/problem/1248649/error-netsdk1005-assets-file-projectassetsjson-doe.html).</span></span>

<span data-ttu-id="450b7-109">可以采取下面的一些操作来解决错误：</span><span class="sxs-lookup"><span data-stu-id="450b7-109">Here are some actions you can take that may resolve the error:</span></span>

* <span data-ttu-id="450b7-110">确保使用的是 MSBuild 版本 16.8 或更高版本以及 NuGet 版本 5.8 或更高版本，并在更新工具后还原项目。</span><span class="sxs-lookup"><span data-stu-id="450b7-110">Make sure that you're using MSBuild version 16.8 or later and NuGet version 5.8 or later, and restore the project after updating your tools.</span></span> <span data-ttu-id="450b7-111">使用 NuGet 版本 5.8 或更高版本时，应使用 Visual Studio 2019 版本 16.8 或更高版本、MSBuild 版本 16.8 或更高版本以及 .NET 5.0 SDK 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="450b7-111">When you're using NuGet version 5.8 or later, you should be using Visual Studio 2019 version 16.8 or later, MSBuild version 16.8 or later, and .NET 5.0 SDK or later.</span></span>

* <span data-ttu-id="450b7-112">如果在安装版本 16.8 或在更改项目的目标框架后首次在 Visual Studio 2019 中生成项目时出现错误，请再次生成项目。</span><span class="sxs-lookup"><span data-stu-id="450b7-112">If you get the error while building a project in Visual Studio 2019 for the first time after installing version 16.8 or after changing the project's target framework, build the project a second time.</span></span>

* <span data-ttu-id="450b7-113">在生成项目之前删除“obj”文件夹。</span><span class="sxs-lookup"><span data-stu-id="450b7-113">Delete the *obj* folder before building the project.</span></span>

* <span data-ttu-id="450b7-114">请确保项目的 `TargetFrameworks` 属性中包含缺少的目标值。</span><span class="sxs-lookup"><span data-stu-id="450b7-114">Make sure that the missing target value is included in the `TargetFrameworks` property of your project.</span></span>

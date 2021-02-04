---
title: NETSDK1004：找不到资产文件
description: 了解在找不到 project.assets.json 文件时出现的 .NET SDK 错误 NETSDK1004。
ms.topic: error-reference
ms.date: 01/29/2021
f1_keywords:
- NETSDK1004
ms.openlocfilehash: 8416063fe318106cbcb4dbccacef3ecaaff5bba2
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99216430"
---
# <a name="netsdk1004-assets-file-not-found"></a><span data-ttu-id="57d22-103">NETSDK1004：找不到资产文件</span><span class="sxs-lookup"><span data-stu-id="57d22-103">NETSDK1004: Assets file not found</span></span>

<span data-ttu-id="57d22-104">本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="57d22-104">**This article applies to:** ✔️ .NET Core 2.1.100 SDK and later versions</span></span>

<span data-ttu-id="57d22-105">NuGet 在“obj”文件夹中写入名为 project.assets.json 的文件，.NET SDK 使用该文件来获取有关要传递到编译器的包的信息 。</span><span class="sxs-lookup"><span data-stu-id="57d22-105">NuGet writes a file named *project.assets.json* in the *obj* folder, and the .NET SDK uses it to get information about packages to pass into the compiler.</span></span> <span data-ttu-id="57d22-106">如果在生成过程中找不到资产文件 project.assets.json，则会发生此错误。</span><span class="sxs-lookup"><span data-stu-id="57d22-106">This error occurs when the assets file *project.assets.json* is not found during build.</span></span> <span data-ttu-id="57d22-107">完整的错误消息类似于以下示例：</span><span class="sxs-lookup"><span data-stu-id="57d22-107">The full error message is similar to the following example:</span></span>

<span data-ttu-id="57d22-108">**NETSDK1004：找不到资产文件“C:\path\to\project.assets.json”。运行 NuGet 包还原以生成此文件。**</span><span class="sxs-lookup"><span data-stu-id="57d22-108">**NETSDK1004: Assets file 'C:\path\to\project.assets.json' not found. Run a NuGet package restore to generate this file.**</span></span>

<span data-ttu-id="57d22-109">下面是一些可能导致此错误的原因：</span><span class="sxs-lookup"><span data-stu-id="57d22-109">Here are some possible causes of the error:</span></span>

* <span data-ttu-id="57d22-110">你正在从包含 `%` 字符的目录路径运行 `dotnet build` 命令。</span><span class="sxs-lookup"><span data-stu-id="57d22-110">You are running the `dotnet build` command from a directory path that contains a `%` character.</span></span> <span data-ttu-id="57d22-111">若要解决此错误，请从文件夹名称中删除 `%`，然后重新运行 `dotnet build`。</span><span class="sxs-lookup"><span data-stu-id="57d22-111">To resolve the error, remove the `%` from the folder name, and rerun `dotnet build`.</span></span>
* <span data-ttu-id="57d22-112">项目系统不会自动检测和还原对项目文件的更改。</span><span class="sxs-lookup"><span data-stu-id="57d22-112">A change to the project file wasn't automatically detected and restored by the project system.</span></span> <span data-ttu-id="57d22-113">若要解决此错误，请打开命令提示符并对项目运行 `dotnet restore`。</span><span class="sxs-lookup"><span data-stu-id="57d22-113">To resolve the error, open a command prompt and run `dotnet restore` on the project.</span></span>
* <span data-ttu-id="57d22-114">一个项目由更早版本的 Nuget.exe 单独还原。</span><span class="sxs-lookup"><span data-stu-id="57d22-114">A project was restored separately by an older version of Nuget.exe.</span></span> <span data-ttu-id="57d22-115">若要解决此错误，请打开命令提示符并对项目运行 `dotnet restore`。</span><span class="sxs-lookup"><span data-stu-id="57d22-115">To resolve the error, open a command prompt and run `dotnet restore` on the project.</span></span>
* <span data-ttu-id="57d22-116">之前的错误，如 NETSDK1045（正在使用的 SDK 版本不支持项目的目标框架），会阻止 NuGet 创建项目资产文件。</span><span class="sxs-lookup"><span data-stu-id="57d22-116">An earlier error, such as NETSDK1045 (the version of the SDK you're using doesn't support the project's target framework), prevented NuGet from creating the project assets file.</span></span> <span data-ttu-id="57d22-117">若要解决 NETSDK1004 错误，请解决以前的错误，然后对该项目运行 `dotnet restore`。</span><span class="sxs-lookup"><span data-stu-id="57d22-117">To resolve the NETSDK1004 error, resolve the earlier error, and then run `dotnet restore` on the project.</span></span>
* <span data-ttu-id="57d22-118">App Center CI 正在生成一个项目，该项目具有不在 NuGet 中的外部程序集。</span><span class="sxs-lookup"><span data-stu-id="57d22-118">App Center CI is building a project that has an external assembly that is not in NuGet.</span></span> <span data-ttu-id="57d22-119">若要解决此错误，请对程序集使用 NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="57d22-119">To resolve the error, use a NuGet package for the assembly.</span></span>

---
title: NETSDK1064：找不到包
description: 了解在找不到包时出现的 .NET SDK 错误 NETSDK1064。
ms.topic: error-reference
ms.date: 02/10/2021
f1_keywords:
- NETSDK1064
ms.openlocfilehash: 1a155db1aacbceb9878401dbcac61ece5f1f9824
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100488190"
---
# <a name="netsdk1064-package-not-found"></a><span data-ttu-id="232e9-103">NETSDK1064：找不到包</span><span class="sxs-lookup"><span data-stu-id="232e9-103">NETSDK1064: Package not found</span></span>

<span data-ttu-id="232e9-104">本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="232e9-104">**This article applies to:** ✔️ .NET Core 2.1.100 SDK and later versions</span></span>

<span data-ttu-id="232e9-105">当生成工具找不到生成项目所需的 NuGet 包时，会发生此错误。</span><span class="sxs-lookup"><span data-stu-id="232e9-105">This error occurs when the build tools can't find a NuGet package that's needed to build a project.</span></span> <span data-ttu-id="232e9-106">这通常是由于包还原问题导致的。</span><span class="sxs-lookup"><span data-stu-id="232e9-106">This is typically due to a package restore issue.</span></span> <span data-ttu-id="232e9-107">完整的错误消息类似于以下示例：</span><span class="sxs-lookup"><span data-stu-id="232e9-107">The full error message is similar to the following example:</span></span>

> <span data-ttu-id="232e9-108">NETSDK1064：找不到版本 x.x.x 的包“PackageName”。</span><span class="sxs-lookup"><span data-stu-id="232e9-108">NETSDK1064: Package 'PackageName', version x.x.x was not found.</span></span> <span data-ttu-id="232e9-109">自 NuGet 还原以来，它可能已被删除。</span><span class="sxs-lookup"><span data-stu-id="232e9-109">It might have been deleted since NuGet restore.</span></span> <span data-ttu-id="232e9-110">否则，NuGet 还原可能仅部分完成（可能由于最大路径长度限制所致）。</span><span class="sxs-lookup"><span data-stu-id="232e9-110">Otherwise, NuGet restore might have only partially completed, which might have been due to maximum path length restrictions.</span></span>

<span data-ttu-id="232e9-111">可以执行以下操作来解决此错误：</span><span class="sxs-lookup"><span data-stu-id="232e9-111">Here are some actions you can take to resolve this error:</span></span>

* <span data-ttu-id="232e9-112">将 `/restore` 选项添加到 MSBuild.exe 命令。</span><span class="sxs-lookup"><span data-stu-id="232e9-112">Add the `/restore` option to your *MSBuild.exe* command.</span></span> <span data-ttu-id="232e9-113">不要使用 `/t:Restore;Build`，因为这可能会导致难以察觉的 bug。</span><span class="sxs-lookup"><span data-stu-id="232e9-113">Don't use `/t:Restore;Build`, as that can result in subtle bugs.</span></span> <span data-ttu-id="232e9-114">一种替代方法是使用 `dotnet build` 命令，因为它会自动执行包还原。</span><span class="sxs-lookup"><span data-stu-id="232e9-114">An alternative is to use the `dotnet build` command, since it automatically does a package restore.</span></span>
* <span data-ttu-id="232e9-115">如果使用 Visual Studio 2019 或 MSBuild.exe 运行包还原，则该错误可能是由最大路径长度限制所导致的。</span><span class="sxs-lookup"><span data-stu-id="232e9-115">If you're running package restore by using Visual Studio 2019 or *MSBuild.exe*, the error may be caused by maximum path length restrictions.</span></span> <span data-ttu-id="232e9-116">有关详细信息，请参阅[长路径支持 (NuGet CLI)](/nuget/reference/cli-reference/cli-ref-long-path) 和 [NuGet/Home 问题 #3324](https://github.com/NuGet/Home/issues/3324)。</span><span class="sxs-lookup"><span data-stu-id="232e9-116">For more information, see [Long Path Support (NuGet CLI)](/nuget/reference/cli-reference/cli-ref-long-path) and [NuGet/Home issue #3324](https://github.com/NuGet/Home/issues/3324).</span></span>
* <span data-ttu-id="232e9-117">如果使用 x86 nuget.exe 进行还原，并使用 x64 MSBuild.exe 进行生成，则不匹配的位数可能会导致此错误。</span><span class="sxs-lookup"><span data-stu-id="232e9-117">If you're restoring with x86 *nuget.exe* and building with x64 *MSBuild.exe*, the mismatched bitness could cause this error.</span></span> <span data-ttu-id="232e9-118">该生成找不到还原过程声明它所获得的包，因为 project.assets.json 中的路径在不同位数的进程中无法起作用。</span><span class="sxs-lookup"><span data-stu-id="232e9-118">The build can't find the packages that the restore claims it acquired because the path in *project.assets.json* doesn't work in a process of different bitness.</span></span> <span data-ttu-id="232e9-119">若要解决此错误，请使用相同位数的工具进行还原和生成，或将 NuGet 配置为将包还原到未在 x86 和 x64 之间进行虚拟化的文件夹。</span><span class="sxs-lookup"><span data-stu-id="232e9-119">To resolve the error, use tools of the same bitness for restore and build, or configure NuGet to restore packages to a folder that doesn't virtualize between x86 and x64.</span></span> <span data-ttu-id="232e9-120">有关详细信息，请参阅 [dotnet/core 问题 #4332](https://github.com/dotnet/core/issues/4332)。</span><span class="sxs-lookup"><span data-stu-id="232e9-120">For more information, see [dotnet/core issue #4332](https://github.com/dotnet/core/issues/4332).</span></span>
* <span data-ttu-id="232e9-121">如果要生成 Docker 映像，请确保 .dockerginore 文件忽略 bin 和 obj 目录。</span><span class="sxs-lookup"><span data-stu-id="232e9-121">If you're building a Docker image, make sure the *.dockerignore* file ignores the *bin* and *obj* directories.</span></span> <span data-ttu-id="232e9-122">有关详细信息，请参阅 [NETSDK1064：找不到包 DnsClient 1.2.0](https://stackoverflow.com/questions/61167032/error-netsdk1064-package-dnsclient-1-2-0-was-not-found)。</span><span class="sxs-lookup"><span data-stu-id="232e9-122">For more information, see [NETSDK1064: Package DnsClient, 1.2.0 was not found](https://stackoverflow.com/questions/61167032/error-netsdk1064-package-dnsclient-1-2-0-was-not-found).</span></span>

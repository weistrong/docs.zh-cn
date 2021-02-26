---
title: C# 简介 - 熟悉开发工具
description: 本文介绍用于在计算机上开发 C# 和 .NET 应用程序的工具的基本知识。
ms.date: 02/02/2021
ms.openlocfilehash: 72116154126b0a97fffe417b2807576b1d9689df
ms.sourcegitcommit: f0fc5db7bcbf212e46933e9cf2d555bb82666141
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "100626599"
---
# <a name="set-up-your-local-environment"></a><span data-ttu-id="3cfe0-103">设置本地环境</span><span class="sxs-lookup"><span data-stu-id="3cfe0-103">Set up your local environment</span></span>

<span data-ttu-id="3cfe0-104">在计算机上演练教程的第一步是设置开发环境。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-104">The first step in running a tutorial on your machine is to set up a development environment.</span></span> <span data-ttu-id="3cfe0-105">选择以下备选方案之一：</span><span class="sxs-lookup"><span data-stu-id="3cfe0-105">Choose one of the following alternatives:</span></span>

* <span data-ttu-id="3cfe0-106">若要使用 .NET CLI 以及所选的文本或代码编辑器，请参阅 .NET 教程 [Hello World 10 分钟入门](https://dotnet.microsoft.com/learn/dotnet/hello-world-tutorial/intro)。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-106">To use the .NET CLI and your choice of text or code editor, see the .NET tutorial [Hello World in 10 minutes](https://dotnet.microsoft.com/learn/dotnet/hello-world-tutorial/intro).</span></span> <span data-ttu-id="3cfe0-107">本教程介绍了如何在 Windows、Linux 或 macOS 上创建开发环境。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-107">The tutorial has instructions for setting up a development environment on Windows, Linux, or macOS.</span></span>
* <span data-ttu-id="3cfe0-108">若要使用 .NET CLI 和 Visual Studio Code，请安装 [.NET SDK](https://dotnet.microsoft.com/download) 和 [Visual Studio Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-108">To use the .NET CLI and Visual Studio Code, install the [.NET SDK](https://dotnet.microsoft.com/download) and [Visual Studio Code](https://code.visualstudio.com/).</span></span>
* <span data-ttu-id="3cfe0-109">若要使用 Visual Studio 2019，请参阅[教程：在 Visual Studio 中创建简单的 C# 控制台应用](/visualstudio/get-started/csharp/tutorial-console)。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-109">To use Visual Studio 2019, see [Tutorial: Create a simple C# console app in Visual Studio](/visualstudio/get-started/csharp/tutorial-console).</span></span>

## <a name="basic-application-development-flow"></a><span data-ttu-id="3cfe0-110">基本的应用程序开发流</span><span class="sxs-lookup"><span data-stu-id="3cfe0-110">Basic application development flow</span></span>

<span data-ttu-id="3cfe0-111">若要更好地理解这些教程中的说明，请使用 .NET CLI 来创建、生成和运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-111">The instructions in these tutorials assume that you're using the .NET CLI to create, build, and run applications.</span></span> <span data-ttu-id="3cfe0-112">你将使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="3cfe0-112">You'll use the following commands:</span></span>

* <span data-ttu-id="3cfe0-113">[`dotnet new`](../../../core/tools/dotnet-new.md) 创建应用程序。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-113">[`dotnet new`](../../../core/tools/dotnet-new.md) creates an application.</span></span> <span data-ttu-id="3cfe0-114">此命令生成应用程序所需的文件和资产。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-114">This command generates the files and assets necessary for your application.</span></span> <span data-ttu-id="3cfe0-115">C# 简介的所有教程都使用 `console` 应用程序类型。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-115">The introduction to C# tutorials all use the `console` application type.</span></span> <span data-ttu-id="3cfe0-116">了解基础知识后，可以扩展到其他应用程序类型。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-116">Once you've got the basics, you can expand to other application types.</span></span>
* <span data-ttu-id="3cfe0-117">[`dotnet build`](../../../core/tools/dotnet-build.md) 生成可执行文件。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-117">[`dotnet build`](../../../core/tools/dotnet-build.md) builds the executable.</span></span>
* <span data-ttu-id="3cfe0-118">[`dotnet run`](../../../core/tools/dotnet-run.md) 运行可执行文件。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-118">[`dotnet run`](../../../core/tools/dotnet-run.md) runs the executable.</span></span>

<span data-ttu-id="3cfe0-119">如果你在这些教程中使用 Visual Studio 2019，则当教程指导你运行这些 CLI 命令之一时，你将选择一个 Visual Studio 菜单选项：</span><span class="sxs-lookup"><span data-stu-id="3cfe0-119">If you use Visual Studio 2019 for these tutorials, you'll choose a Visual Studio menu selection when a tutorial directs you to run one of these CLI commands:</span></span>

* <span data-ttu-id="3cfe0-120">“文件” > “新建” > “项目”：创建应用程序。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-120">**File** > **New** > **Project** creates an application.</span></span>
* <span data-ttu-id="3cfe0-121">“生成” >  “生成解决方案”：生成可执行文件。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-121">**Build** >  **Build Solution** builds the executable.</span></span>
* <span data-ttu-id="3cfe0-122">“调试” > “启动但不调试”：运行可执行文件。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-122">**Debug** > **Start Without Debugging** runs the executable.</span></span>

## <a name="pick-your-tutorial"></a><span data-ttu-id="3cfe0-123">选择教程</span><span class="sxs-lookup"><span data-stu-id="3cfe0-123">Pick your tutorial</span></span>

<span data-ttu-id="3cfe0-124">可以从下列任一教程入手：</span><span class="sxs-lookup"><span data-stu-id="3cfe0-124">You can start with any of the following tutorials:</span></span>

## <a name="numbers-in-c"></a><span data-ttu-id="3cfe0-125">C\# 中的数字</span><span class="sxs-lookup"><span data-stu-id="3cfe0-125">Numbers in C\#</span></span>

<span data-ttu-id="3cfe0-126">在 [C# 中的数字](numbers-in-csharp-local.md)教程中，将了解计算机如何存储数字，以及如何对不同类型的数字执行计算。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-126">In the [Numbers in C#](numbers-in-csharp-local.md) tutorial, you'll learn how computers store numbers and how to perform calculations with different numeric types.</span></span> <span data-ttu-id="3cfe0-127">读者将学习四舍五入的基础知识，以及如何使用 C# 执行数学运算。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-127">You'll learn the basics of rounding and how to perform mathematical calculations using C#.</span></span>

<span data-ttu-id="3cfe0-128">若要更好地学习本教程，需要已完成 [Hello world](hello-world.yml) 课程。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-128">This tutorial assumes that you have finished the [Hello world](hello-world.yml) lesson.</span></span>

## <a name="branches-and-loops"></a><span data-ttu-id="3cfe0-129">分支和循环</span><span class="sxs-lookup"><span data-stu-id="3cfe0-129">Branches and loops</span></span>

<span data-ttu-id="3cfe0-130">在[分支和循环](branches-and-loops-local.md)教程中，将了解根据变量中存储的值选择不同代码执行路径的基础知识。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-130">The [Branches and loops](branches-and-loops-local.md) tutorial teaches the basics of selecting different paths of code execution based on the values stored in variables.</span></span> <span data-ttu-id="3cfe0-131">读者将学习控制流的基础知识，这是程序决定选择不同操作的基本依据。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-131">You'll learn the basics of control flow, which is the basis of how programs make decisions and choose different actions.</span></span>

<span data-ttu-id="3cfe0-132">若要更好地学习本教程，需要先完成 [Hello World](hello-world.yml) 和 [C# 中的数字](numbers-in-csharp-local.md)课程。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-132">This tutorial assumes that you have finished the [Hello world](hello-world.yml) and [Numbers in C#](numbers-in-csharp-local.md) lessons.</span></span>

## <a name="list-collection"></a><span data-ttu-id="3cfe0-133">列表集合</span><span class="sxs-lookup"><span data-stu-id="3cfe0-133">List collection</span></span>

<span data-ttu-id="3cfe0-134">[列表集合](arrays-and-collections.md)课程将介绍存储一系列数据的列表集合类型。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-134">The [List collection](arrays-and-collections.md) lesson gives you a tour of the List collection type that stores sequences of data.</span></span> <span data-ttu-id="3cfe0-135">读者将学习如何添加和删除项、如何搜索项，以及如何对列表进行排序。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-135">You'll learn how to add and remove items, search for items, and sort the lists.</span></span> <span data-ttu-id="3cfe0-136">读者将探索各种列表。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-136">You'll explore different kinds of lists.</span></span>

<span data-ttu-id="3cfe0-137">若要更好地学习本教程，需要已完成上面列出的课程。</span><span class="sxs-lookup"><span data-stu-id="3cfe0-137">This tutorial assumes that you have finished the lessons listed above.</span></span>

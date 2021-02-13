---
title: C# 简介 - 熟悉开发工具
description: 本文介绍用于在计算机上开发 C# 和 .NET 应用程序的工具的基本知识。
ms.date: 02/02/2021
ms.openlocfilehash: d5fbd23679fc11f4e4c207c59858a71ab753c038
ms.sourcegitcommit: 65af0f0ad316858882845391d60ef7e303b756e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "99585320"
---
# <a name="set-up-your-local-environment"></a>设置本地环境

在计算机上演练教程的第一步是设置开发环境。 选择以下备选方案之一：

* 若要使用 .NET CLI 以及所选的文本或代码编辑器，请参阅 .NET 教程 [Hello World 10 分钟入门](https://dotnet.microsoft.com/learn/dotnet/hello-world-tutorial/intro)。 本教程介绍了如何在 Windows、Linux 或 macOS 上创建开发环境。
* 若要使用 .NET CLI 和 Visual Studio Code，请安装 [.NET SDK](https://dotnet.microsoft.com/download) 和 [Visual Studio Code](https://code.visualstudio.com/)。
* 若要在 Windows 上使用 Visual Studio 2019，请参阅[教程：在 Visual Studio 中创建简单的 C# 控制台应用](/visualstudio/get-started/csharp/tutorial-console)。

## <a name="basic-application-development-flow"></a>基本的应用程序开发流

若要更好地理解这些教程中的说明，请使用 .NET CLI 来创建、生成和运行应用程序。 你将使用以下命令：

* [`dotnet new`](../../../core/tools/dotnet-new.md) 创建应用程序。 此命令生成应用程序所需的文件和资产。 C# 简介的所有教程都使用 `console` 应用程序类型。 了解基础知识后，可以扩展到其他应用程序类型。
* [`dotnet build`](../../../core/tools/dotnet-build.md) 生成可执行文件。
* [`dotnet run`](../../../core/tools/dotnet-run.md) 运行可执行文件。

如果你在这些教程中使用 Visual Studio 2019，则当教程指导你运行这些 CLI 命令之一时，你将选择一个 Visual Studio 菜单选项：

* “文件” > “新建” > “项目”：创建应用程序。
* “生成” >  “生成解决方案”：生成可执行文件。
* “调试” > “启动但不调试”：运行可执行文件。

## <a name="pick-your-tutorial"></a>选择教程

可以从下列任一教程入手：

## <a name="numbers-in-c"></a>C\# 中的数字

在 [C# 中的数字](numbers-in-csharp-local.md)教程中，将了解计算机如何存储数字，以及如何对不同类型的数字执行计算。 读者将学习四舍五入的基础知识，以及如何使用 C# 执行数学运算。

若要更好地学习本教程，需要已完成 [Hello world](hello-world.yml) 课程。

## <a name="branches-and-loops"></a>分支和循环

在[分支和循环](branches-and-loops-local.md)教程中，将了解根据变量中存储的值选择不同代码执行路径的基础知识。 读者将学习控制流的基础知识，这是程序决定选择不同操作的基本依据。

若要更好地学习本教程，需要先完成 [Hello World](hello-world.yml) 和 [C# 中的数字](numbers-in-csharp-local.md)课程。

## <a name="list-collection"></a>列表集合

[列表集合](arrays-and-collections.md)课程将介绍存储一系列数据的列表集合类型。 读者将学习如何添加和删除项、如何搜索项，以及如何对列表进行排序。 读者将探索各种列表。

若要更好地学习本教程，需要已完成上面列出的课程。

## <a name="introduction-to-classes"></a>类简介

在[类简介](introduction-to-classes.md)中，你将生成一个控制台应用程序，并了解 C# 语言中的面向对象的基本功能。 这是最终的 C# 简介教程。 它只能在虚拟机上运行（使用你自己的本地开发环境和 .NET）。

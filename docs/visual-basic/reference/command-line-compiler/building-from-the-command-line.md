---
description: 详细了解：从命令行生成 (Visual Basic)
title: 从命令行生成
ms.date: 07/20/2015
helpviewer_keywords:
- builds [Visual Basic], command-line
- Visual Basic compiler, about Visual Basic compiler
- command line [Visual Basic], compilers
- command line [Visual Basic], building from
- command line [Visual Basic], builds
- compilers [Visual Basic], invoking from command line
- command-line builds
- compiling source code
- command-line compilers [Visual Basic], Visual Basic
- command line [Visual Basic], Visual Basic
ms.assetid: e61947e9-a42e-4717-a699-5f70a98cdd03
ms.openlocfilehash: 5f0f8dd61bd5b79987cc1e59dcf4bfd8071a925e
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100468260"
---
# <a name="building-from-the-command-line-visual-basic"></a><span data-ttu-id="66185-103">从命令行生成 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="66185-103">Building from the Command Line (Visual Basic)</span></span>

<span data-ttu-id="66185-104">Visual Basic 项目由一个或多个单独的源文件组成。</span><span class="sxs-lookup"><span data-stu-id="66185-104">A Visual Basic project is made up of one or more separate source files.</span></span> <span data-ttu-id="66185-105">在名为编译的过程中，这些文件会一起合并到一个包中，这是可作为应用程序运行的单个可执行文件。</span><span class="sxs-lookup"><span data-stu-id="66185-105">During the process known as compilation, these files are brought together into one package—a single executable file that can be run as an application.</span></span>

<span data-ttu-id="66185-106">Visual Basic 提供命令行编译器作为替代方法，用于在 Visual Studio 集成开发环境 (IDE) 中编译程序。</span><span class="sxs-lookup"><span data-stu-id="66185-106">Visual Basic provides a command-line compiler as an alternative to compiling programs from within the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="66185-107">命令行编译器旨在用于不需要 IDE 中的完整功能集的情况（例如，为系统内存或存储空间有限的计算机进行使用或编写）。</span><span class="sxs-lookup"><span data-stu-id="66185-107">The command-line compiler is designed for situations in which you do not require the full set of features in the IDE—for example, when you are using or writing for computers with limited system memory or storage space.</span></span>

<span data-ttu-id="66185-108">若要从 Visual Studio IDE 中编译源文件，请从“生成”  菜单中选择“生成”  命令。</span><span class="sxs-lookup"><span data-stu-id="66185-108">To compile source files from within the Visual Studio IDE, choose the **Build** command from the **Build** menu.</span></span>

> [!TIP]
> <span data-ttu-id="66185-109">使用 Visual Studio IDE 生成项目文件时，可以在输出窗口中显示有关关联 vbc  命令及其开关的信息。</span><span class="sxs-lookup"><span data-stu-id="66185-109">When you build project files by using the Visual Studio IDE, you can display information about the associated **vbc** command and its switches in the output window.</span></span> <span data-ttu-id="66185-110">若要显示此信息，请打开[“选项”对话框、“项目和解决方案”、“生成和运行”](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run)，然后将“MSBuild 项目生成输出详细信息”  设置为“普通”  或更高级别的详细程度。</span><span class="sxs-lookup"><span data-stu-id="66185-110">To display this information, open the [Options Dialog Box,  Projects and Solutions, Build and Run](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), and then set the **MSBuild project build output verbosity** to **Normal** or a higher level of verbosity.</span></span> <span data-ttu-id="66185-111">有关详细信息，请参阅[如何：查看、保存和配置生成日志文件](/visualstudio/ide/how-to-view-save-and-configure-build-log-files)。</span><span class="sxs-lookup"><span data-stu-id="66185-111">For more information, see [How to: View, Save, and Configure Build Log Files](/visualstudio/ide/how-to-view-save-and-configure-build-log-files).</span></span>

<span data-ttu-id="66185-112">可以使用 MSBuild 在命令提示符下编译项目 (.vbproj) 文件。</span><span class="sxs-lookup"><span data-stu-id="66185-112">You can compile project (.vbproj) files at a command prompt by using MSBuild.</span></span> <span data-ttu-id="66185-113">有关详细信息，请参阅[命令行参考](/visualstudio/msbuild/msbuild-command-line-reference)和[演练：使用 MSBuild](/visualstudio/msbuild/walkthrough-using-msbuild)。</span><span class="sxs-lookup"><span data-stu-id="66185-113">For more information, see [Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference) and [Walkthrough: Using MSBuild](/visualstudio/msbuild/walkthrough-using-msbuild).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66185-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="66185-114">In This Section</span></span>

<span data-ttu-id="66185-115">[如何：调用命令行编译器](how-to-invoke-the-command-line-compiler.md) </span><span class="sxs-lookup"><span data-stu-id="66185-115">[How to: Invoke the Command-Line Compiler](how-to-invoke-the-command-line-compiler.md) </span></span>\
<span data-ttu-id="66185-116">介绍如何在 MS-DOS 提示符下或从特定子目录调用命令行编译器。</span><span class="sxs-lookup"><span data-stu-id="66185-116">Describes how to invoke the command-line compiler at the MS-DOS prompt or from a specific subdirectory.</span></span>

<span data-ttu-id="66185-117">[示例编译命令行](sample-compilation-command-lines.md) </span><span class="sxs-lookup"><span data-stu-id="66185-117">[Sample Compilation Command Lines](sample-compilation-command-lines.md) </span></span>\
<span data-ttu-id="66185-118">提供可以进行修改以供自己使用的示例命令行的列表。</span><span class="sxs-lookup"><span data-stu-id="66185-118">Provides a list of sample command lines that you can modify for your own use.</span></span>

## <a name="related-sections"></a><span data-ttu-id="66185-119">相关章节</span><span class="sxs-lookup"><span data-stu-id="66185-119">Related Sections</span></span>

<span data-ttu-id="66185-120">[Visual Basic 命令行编译器](index.md) </span><span class="sxs-lookup"><span data-stu-id="66185-120">[Visual Basic Command-Line Compiler](index.md) </span></span>\
<span data-ttu-id="66185-121">提供按字母顺序或用途组织的编译器选项的列表。</span><span class="sxs-lookup"><span data-stu-id="66185-121">Provides lists of compiler options, organized alphabetically or by purpose.</span></span>

<span data-ttu-id="66185-122">[条件编译](../../programming-guide/program-structure/conditional-compilation.md) </span><span class="sxs-lookup"><span data-stu-id="66185-122">[Conditional Compilation](../../programming-guide/program-structure/conditional-compilation.md) </span></span>\
<span data-ttu-id="66185-123">介绍如何编译代码的特定部分。</span><span class="sxs-lookup"><span data-stu-id="66185-123">Describes how to compile particular sections of code.</span></span>

<span data-ttu-id="66185-124">[在 Visual Studio 中生成和清理项目和解决方案](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio) </span><span class="sxs-lookup"><span data-stu-id="66185-124">[Building and Cleaning Projects and Solutions in Visual Studio](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio) </span></span>\
<span data-ttu-id="66185-125">介绍如何组织将包含在不同生成中的内容、选择项目属性以及确保项目按正确顺序生成。</span><span class="sxs-lookup"><span data-stu-id="66185-125">Describes how to organize what will be included in different builds, choose project properties, and ensure that projects build in the correct order.</span></span>

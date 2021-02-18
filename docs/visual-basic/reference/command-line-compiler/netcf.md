---
description: 详细了解：-netcf
title: -netcf
ms.date: 03/13/2018
f1_keywords:
- /netcf
- -netcf
helpviewer_keywords:
- -netcf compiler option [Visual Basic]
- netcf compiler option [Visual Basic]
- /netcf compiler option [Visual Basic]
ms.assetid: db7cfa59-c315-401c-a59b-0daf355343d6
ms.openlocfilehash: 053e177d8d7008b10bfa552ee60cbbd2d5dda565
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434909"
---
# <a name="-netcf"></a><span data-ttu-id="c859c-103">-netcf</span><span class="sxs-lookup"><span data-stu-id="c859c-103">-netcf</span></span>

<span data-ttu-id="c859c-104">将编译器设置为以 .NET Compact Framework 为目标。</span><span class="sxs-lookup"><span data-stu-id="c859c-104">Sets the compiler to target the .NET Compact Framework.</span></span>

## <a name="syntax"></a><span data-ttu-id="c859c-105">语法</span><span class="sxs-lookup"><span data-stu-id="c859c-105">Syntax</span></span>

```console
-netcf
```

## <a name="remarks"></a><span data-ttu-id="c859c-106">备注</span><span class="sxs-lookup"><span data-stu-id="c859c-106">Remarks</span></span>

<span data-ttu-id="c859c-107">`-netcf` 选项使 Visual Basic 编译器将 .NET Compact Framework（而不是完整的 .NET Framework）作为目标。</span><span class="sxs-lookup"><span data-stu-id="c859c-107">The `-netcf` option causes the Visual Basic compiler to target the .NET Compact Framework rather than the full .NET Framework.</span></span> <span data-ttu-id="c859c-108">仅在完整的 .NET Framework 中存在的语言功能处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="c859c-108">Language functionality that is present only in the full .NET Framework is disabled.</span></span>

<span data-ttu-id="c859c-109">`-netcf` 选项专门与 [-sdkpath](sdkpath.md) 一起使用。</span><span class="sxs-lookup"><span data-stu-id="c859c-109">The `-netcf` option is designed to be used with [-sdkpath](sdkpath.md).</span></span> <span data-ttu-id="c859c-110">`-netcf` 禁用的语言功能与 `-sdkpath` 目标文件中不存在的语言功能相同。</span><span class="sxs-lookup"><span data-stu-id="c859c-110">The language features disabled by `-netcf` are the same language features not present in the files targeted with `-sdkpath`.</span></span>

> [!NOTE]
> <span data-ttu-id="c859c-111">`-netcf` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="c859c-111">The `-netcf` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span> <span data-ttu-id="c859c-112">加载 Visual Basic 设备项目时，将设置 `-netcf` 选项。</span><span class="sxs-lookup"><span data-stu-id="c859c-112">The `-netcf` option is set when a Visual Basic device project is loaded.</span></span>

<span data-ttu-id="c859c-113">`-netcf` 选项会更改以下语言功能：</span><span class="sxs-lookup"><span data-stu-id="c859c-113">The `-netcf` option changes the following language features:</span></span>

- <span data-ttu-id="c859c-114">禁用 [End \<keyword> Statement](../../language-reference/statements/end-keyword-statement.md) 关键字，该关键字可终止程序执行。</span><span class="sxs-lookup"><span data-stu-id="c859c-114">The [End \<keyword> Statement](../../language-reference/statements/end-keyword-statement.md) keyword, which terminates execution of a program, is disabled.</span></span> <span data-ttu-id="c859c-115">以下程序在没有 `-netcf` 的情况下进行编译和运行，但在通过 `-netcf` 进行编译时将失败。</span><span class="sxs-lookup"><span data-stu-id="c859c-115">The following program compiles and runs without `-netcf` but fails at compile time with `-netcf`.</span></span>

  [!code-vb[VbVbalrCompiler#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/netcf.vb#34)]

- <span data-ttu-id="c859c-116">在所有窗体中禁用后期绑定。</span><span class="sxs-lookup"><span data-stu-id="c859c-116">Late binding, in all forms, is disabled.</span></span> <span data-ttu-id="c859c-117">当遇到识别的后期绑定情况时，会产生编译时错误。</span><span class="sxs-lookup"><span data-stu-id="c859c-117">Compile-time errors are generated when recognized late-binding scenarios are encountered.</span></span> <span data-ttu-id="c859c-118">以下程序在没有 `-netcf` 的情况下进行编译和运行，但在通过 `-netcf` 进行编译时将失败。</span><span class="sxs-lookup"><span data-stu-id="c859c-118">The following program compiles and runs without `-netcf` but fails at compile time with `-netcf`.</span></span>

  [!code-vb[VbVbalrCompiler#35](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#35)]

- <span data-ttu-id="c859c-119">禁用 [Auto](../../language-reference/modifiers/auto.md)、[Ansi](../../language-reference/modifiers/ansi.md) 和[Unicode](../../language-reference/modifiers/unicode.md) 修饰符。</span><span class="sxs-lookup"><span data-stu-id="c859c-119">The [Auto](../../language-reference/modifiers/auto.md), [Ansi](../../language-reference/modifiers/ansi.md), and [Unicode](../../language-reference/modifiers/unicode.md) modifiers are disabled.</span></span> <span data-ttu-id="c859c-120">[Declare 语句](../../language-reference/statements/declare-statement.md)的语法也修改为 `Declare Sub|Function name Lib "library" [Alias "alias"] [([arglist])]`。</span><span class="sxs-lookup"><span data-stu-id="c859c-120">The syntax of the [Declare Statement](../../language-reference/statements/declare-statement.md) is also modified to `Declare Sub|Function name Lib "library" [Alias "alias"] [([arglist])]`.</span></span> <span data-ttu-id="c859c-121">以下代码显示 `-netcf` 对编译的影响。</span><span class="sxs-lookup"><span data-stu-id="c859c-121">The following code shows the effect of `-netcf` on a compilation.</span></span>

  [!code-vb[VbVbalrCompiler#36](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#36)]

- <span data-ttu-id="c859c-122">在使用 `-netcf` 时，使用从 Visual Basic 中删除的 Visual Basic 6.0 关键字会产生不同的错误。</span><span class="sxs-lookup"><span data-stu-id="c859c-122">Using Visual Basic 6.0 keywords that were removed from Visual Basic generates a different error when `-netcf` is used.</span></span> <span data-ttu-id="c859c-123">这会影响以下关键字的错误消息：</span><span class="sxs-lookup"><span data-stu-id="c859c-123">This affects the error messages for the following keywords:</span></span>

  - `Open`

  - `Close`

  - `Put`

  - `Print`

  - `Write`

  - `Input`

  - `Lock`

  - `Unlock`

  - `Seek`

  - `Width`

  - `Name`

  - `FreeFile`

  - `EOF`

  - `Loc`

  - `LOF`

  - `Line`

## <a name="example"></a><span data-ttu-id="c859c-124">示例</span><span class="sxs-lookup"><span data-stu-id="c859c-124">Example</span></span>

<span data-ttu-id="c859c-125">以下代码使用 C 盘上 .NET Compact Framework 的默认安装目录中的 mscorlib.dll 和 Microsoft.VisualBasic.dll 版本，通过 .NET Compact Framework 编译 `Myfile.vb`。</span><span class="sxs-lookup"><span data-stu-id="c859c-125">The following code compiles `Myfile.vb` with the .NET Compact Framework, using the versions of mscorlib.dll and Microsoft.VisualBasic.dll found in the default installation directory of the .NET Compact Framework on the C drive.</span></span> <span data-ttu-id="c859c-126">通常，会使用 .NET Compact Framework 的最新版本。</span><span class="sxs-lookup"><span data-stu-id="c859c-126">Typically, you would use the most recent version of the .NET Compact Framework.</span></span>

```console
vbc -netcf -sdkpath:"c:\Program Files\Microsoft Visual Studio .NET 2003\CompactFrameworkSDK\v1.0.5000\Windows CE " myfile.vb
```

## <a name="see-also"></a><span data-ttu-id="c859c-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="c859c-127">See also</span></span>

- [<span data-ttu-id="c859c-128">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="c859c-128">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="c859c-129">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="c859c-129">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="c859c-130">-sdkpath</span><span class="sxs-lookup"><span data-stu-id="c859c-130">-sdkpath</span></span>](sdkpath.md)

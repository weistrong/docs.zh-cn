---
description: 详细了解：-refonly (Visual Basic)
title: -refonly
ms.date: 03/16/2018
f1_keywords:
- -refonly
helpviewer_keywords:
- /refonly compiler option [Visual Basic]
- -refonly compiler option [Visual Basic]
- refonly compiler option [Visual Basic]
ms.openlocfilehash: 283aa75fceead38c62c4cf10c1ffe08151aeac9c
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474130"
---
# <a name="-refonly-visual-basic"></a><span data-ttu-id="56cc8-103">-refonly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56cc8-103">-refonly (Visual Basic)</span></span>

<span data-ttu-id="56cc8-104">-refonly  选项指示编译的主输出应为引用程序集（而不是实现程序集）。</span><span class="sxs-lookup"><span data-stu-id="56cc8-104">The **-refonly** option indicates that the primary output of the compilation should be a reference assembly instead of an implementation assembly.</span></span> <span data-ttu-id="56cc8-105">`-refonly` 参数以无提示方式禁用输出 PDB，因为无法执行引用程序集。</span><span class="sxs-lookup"><span data-stu-id="56cc8-105">The `-refonly` parameter silently disables outputting PDBs, as reference assemblies cannot be executed.</span></span>

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a><span data-ttu-id="56cc8-106">语法</span><span class="sxs-lookup"><span data-stu-id="56cc8-106">Syntax</span></span>

```console
-refonly
```

## <a name="remarks"></a><span data-ttu-id="56cc8-107">备注</span><span class="sxs-lookup"><span data-stu-id="56cc8-107">Remarks</span></span>

<span data-ttu-id="56cc8-108">从 15.3 版开始，Visual Basic 支持 `-refonly` 开关。</span><span class="sxs-lookup"><span data-stu-id="56cc8-108">Visual Basic supports the `-refonly` switch starting with version 15.3.</span></span>

<span data-ttu-id="56cc8-109">引用程序集是一种特殊类型的程序集，它只包含表示库的公共 API 外围应用所需的最少元数据量。</span><span class="sxs-lookup"><span data-stu-id="56cc8-109">Reference assemblies are a special type of assembly that contain only the minimum amount of metadata required to represent the library's public API surface.</span></span> <span data-ttu-id="56cc8-110">它们包括在生成工具中引用程序集时所需的所有成员的声明，但不包括所有成员实现以及对其 API 协定没有明显影响的私有成员的声明。</span><span class="sxs-lookup"><span data-stu-id="56cc8-110">They include declarations for all members that are significant when referencing an assembly in build tools, but exclude all member implementations and declarations of private members that have no observable impact on their API contract.</span></span> <span data-ttu-id="56cc8-111">有关详细信息，请参阅 .NET 指南中的[引用程序集](../../../standard/assembly/reference-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="56cc8-111">For more information, see [Reference assemblies](../../../standard/assembly/reference-assemblies.md) in .NET Guide.</span></span>

<span data-ttu-id="56cc8-112">`-refonly` 和 [`-refout`](refout-compiler-option.md) 选项互斥。</span><span class="sxs-lookup"><span data-stu-id="56cc8-112">The `-refonly` and [`-refout`](refout-compiler-option.md) options are mutually exclusive.</span></span>

## <a name="see-also"></a><span data-ttu-id="56cc8-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="56cc8-113">See also</span></span>

- [<span data-ttu-id="56cc8-114">/refout</span><span class="sxs-lookup"><span data-stu-id="56cc8-114">-refout</span></span>](refout-compiler-option.md)
- [<span data-ttu-id="56cc8-115">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="56cc8-115">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="56cc8-116">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="56cc8-116">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)

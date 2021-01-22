---
description: -deterministic（C# 编译器选项）
title: -deterministic（C# 编译器选项）
ms.date: 04/12/2018
f1_keywords:
- /deterministic
helpviewer_keywords:
- -deterministic compiler option [C#]
- deterministic compiler option [C#]
- /deterministic compiler option [C#]
ms.openlocfilehash: d64f4d4b0d4e9b5ed2cc1ee40662dc669fc6660d
ms.sourcegitcommit: 4f5f1855849cb02c3b610c7006ac21d7429f3348
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "98235321"
---
# <a name="-deterministic"></a><span data-ttu-id="c0158-103">-deterministic</span><span class="sxs-lookup"><span data-stu-id="c0158-103">-deterministic</span></span>

<span data-ttu-id="c0158-104">如果输入相同，则会导致编译器生成的程序集其逐字节输出在整个编译期间中相同。</span><span class="sxs-lookup"><span data-stu-id="c0158-104">Causes the compiler to produce an assembly whose byte-for-byte output is identical across compilations for identical inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0158-105">语法</span><span class="sxs-lookup"><span data-stu-id="c0158-105">Syntax</span></span>

```console
-deterministic
```

## <a name="remarks"></a><span data-ttu-id="c0158-106">备注</span><span class="sxs-lookup"><span data-stu-id="c0158-106">Remarks</span></span>

<span data-ttu-id="c0158-107">默认情况下，一组给定输入的编译器输出是唯一的，因为编译器会添加时间戳和随意数字生成的 MVID。</span><span class="sxs-lookup"><span data-stu-id="c0158-107">By default, compiler output from a given set of inputs is unique, since the compiler adds a timestamp and a MVID that is generated from random numbers.</span></span> <span data-ttu-id="c0158-108">使用 `-deterministic` 选项生成确定性的程序集，只要输入保持不变，该程序集的二进制内容在整个编译中都是相同的  。</span><span class="sxs-lookup"><span data-stu-id="c0158-108">You use the `-deterministic` option to produce a *deterministic assembly*, one whose binary content is identical across compilations as long as the input remains the same.</span></span> <span data-ttu-id="c0158-109">在此类生成中，时间戳和 MVID 字段会被替换为从所有编译输入的哈希派生的值。</span><span class="sxs-lookup"><span data-stu-id="c0158-109">In such a build, the timestamp and MVID fields will be replaced with values derived from a hash of all the compilation inputs.</span></span>

<span data-ttu-id="c0158-110">出于确定性目的，编译器会考虑以下输入：</span><span class="sxs-lookup"><span data-stu-id="c0158-110">The compiler considers the following inputs for the purpose of determinism:</span></span>

- <span data-ttu-id="c0158-111">命令行参数序列。</span><span class="sxs-lookup"><span data-stu-id="c0158-111">The sequence of command-line parameters.</span></span>
- <span data-ttu-id="c0158-112">编译器 .rsp 响应文件的内容。</span><span class="sxs-lookup"><span data-stu-id="c0158-112">The contents of the compiler's .rsp response file.</span></span>
- <span data-ttu-id="c0158-113">所用编译器的精确版本及其引用的程序集。</span><span class="sxs-lookup"><span data-stu-id="c0158-113">The precise version of the compiler used, and its referenced assemblies.</span></span>
- <span data-ttu-id="c0158-114">当前目录路径。</span><span class="sxs-lookup"><span data-stu-id="c0158-114">The current directory path.</span></span>
- <span data-ttu-id="c0158-115">直接或间接地显式传递到编译器的所有文件的二进制内容，包括：</span><span class="sxs-lookup"><span data-stu-id="c0158-115">The binary contents of all files explicitly passed to the compiler either directly or indirectly, including:</span></span>
  - <span data-ttu-id="c0158-116">源文件</span><span class="sxs-lookup"><span data-stu-id="c0158-116">Source files</span></span>
  - <span data-ttu-id="c0158-117">引用的程序集</span><span class="sxs-lookup"><span data-stu-id="c0158-117">Referenced assemblies</span></span>
  - <span data-ttu-id="c0158-118">引用的模块</span><span class="sxs-lookup"><span data-stu-id="c0158-118">Referenced modules</span></span>
  - <span data-ttu-id="c0158-119">资源</span><span class="sxs-lookup"><span data-stu-id="c0158-119">Resources</span></span>
  - <span data-ttu-id="c0158-120">强名称密钥文件</span><span class="sxs-lookup"><span data-stu-id="c0158-120">The strong name key file</span></span>
  - <span data-ttu-id="c0158-121">@ 响应文件</span><span class="sxs-lookup"><span data-stu-id="c0158-121">@ response files</span></span>
  - <span data-ttu-id="c0158-122">分析器</span><span class="sxs-lookup"><span data-stu-id="c0158-122">Analyzers</span></span>
  - <span data-ttu-id="c0158-123">规则集</span><span class="sxs-lookup"><span data-stu-id="c0158-123">Rulesets</span></span>
  - <span data-ttu-id="c0158-124">分析器可能使用的其他文件</span><span class="sxs-lookup"><span data-stu-id="c0158-124">Additional files that may be used by analyzers</span></span>
- <span data-ttu-id="c0158-125">当前区域性（针对生成诊断和异常消息的语言）。</span><span class="sxs-lookup"><span data-stu-id="c0158-125">The current culture (for the language in which diagnostics and exception messages are produced).</span></span>
- <span data-ttu-id="c0158-126">在未指定编码情况下使用的默认编码（或当前代码页）。</span><span class="sxs-lookup"><span data-stu-id="c0158-126">The default encoding (or the current code page) if the encoding is not specified.</span></span>
- <span data-ttu-id="c0158-127">编译器搜索路径（例如，由`-lib` 或 `-recurse` 指定）上文件是否存在及其内容。</span><span class="sxs-lookup"><span data-stu-id="c0158-127">The existence, non-existence, and contents of files on the compiler's search paths (specified, for example, by `-lib` or `-recurse`).</span></span>
- <span data-ttu-id="c0158-128">运行编译器的 CLR 平台。</span><span class="sxs-lookup"><span data-stu-id="c0158-128">The CLR platform on which the compiler is run.</span></span>
- <span data-ttu-id="c0158-129">`%LIBPATH%` 的值，该值会影响分析器的依赖项加载。</span><span class="sxs-lookup"><span data-stu-id="c0158-129">The value of `%LIBPATH%`, which can affect analyzer dependency loading.</span></span>

<span data-ttu-id="c0158-130">当源公开可用时，可使用确定性编译来确定是否从可信源编译二进制内容。</span><span class="sxs-lookup"><span data-stu-id="c0158-130">When sources are publicly available, deterministic compilation can be used for establishing whether a binary is compiled from a trusted source.</span></span> <span data-ttu-id="c0158-131">它还可有效用于连续生成系统，确定是否需要执行依赖于二进制内容更改的生成步骤。</span><span class="sxs-lookup"><span data-stu-id="c0158-131">It can also be useful in a continuous build system for determining whether build steps that are dependent on changes to a binary need to be executed.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0158-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0158-132">See also</span></span>

- [<span data-ttu-id="c0158-133">C# 编译器选项</span><span class="sxs-lookup"><span data-stu-id="c0158-133">C# Compiler Options</span></span>](./index.md)
- [<span data-ttu-id="c0158-134">管理项目和解决方案属性</span><span class="sxs-lookup"><span data-stu-id="c0158-134">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)

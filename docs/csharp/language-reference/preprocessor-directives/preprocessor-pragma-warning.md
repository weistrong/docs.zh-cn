---
description: '#pragma warning - C# 参考'
title: '#pragma warning - C# 参考'
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 16582a74bd34f2c0d89950280f1d5fde25435eea
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99215987"
---
# <a name="pragma-warning-c-reference"></a><span data-ttu-id="47051-103">#pragma warning（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="47051-103">#pragma warning (C# Reference)</span></span>

<span data-ttu-id="47051-104">`#pragma warning` 可以启用或禁用特定警告。</span><span class="sxs-lookup"><span data-stu-id="47051-104">`#pragma warning` can enable or disable certain warnings.</span></span>

## <a name="syntax"></a><span data-ttu-id="47051-105">语法</span><span class="sxs-lookup"><span data-stu-id="47051-105">Syntax</span></span>

```csharp
#pragma warning disable warning-list
#pragma warning restore warning-list
```

## <a name="parameters"></a><span data-ttu-id="47051-106">参数</span><span class="sxs-lookup"><span data-stu-id="47051-106">Parameters</span></span>

 <span data-ttu-id="47051-107">`warning-list` 以逗号分隔的警告编号的列表。</span><span class="sxs-lookup"><span data-stu-id="47051-107">`warning-list` A comma-separated list of warning numbers.</span></span> <span data-ttu-id="47051-108">“CS”前缀是可选的。</span><span class="sxs-lookup"><span data-stu-id="47051-108">The "CS" prefix is optional.</span></span>

 <span data-ttu-id="47051-109">未指定警告编号时，`disable` 会禁用所有警告，`restore` 会启用所有警告。</span><span class="sxs-lookup"><span data-stu-id="47051-109">When no warning numbers are specified, `disable` disables all warnings and `restore` enables all warnings.</span></span>

> [!NOTE]
> <span data-ttu-id="47051-110">若要在 Visual Studio 中查找警告编号，请生成项目，然后在“输出”窗口中查找警告编号。</span><span class="sxs-lookup"><span data-stu-id="47051-110">To find warning numbers in Visual Studio, build your project and then look for the warning numbers in the **Output** window.</span></span>

## <a name="example"></a><span data-ttu-id="47051-111">示例</span><span class="sxs-lookup"><span data-stu-id="47051-111">Example</span></span>

```csharp
// pragma_warning.cs
using System;

#pragma warning disable 414, CS3021
[CLSCompliant(false)]
public class C
{
    int i = 1;
    static void Main()
    {
    }
}
#pragma warning restore CS3021
[CLSCompliant(false)]  // CS3021
public class D
{
    int i = 1;
    public static void F()
    {
    }
}
```

## <a name="see-also"></a><span data-ttu-id="47051-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="47051-112">See also</span></span>

- [<span data-ttu-id="47051-113">C# 参考</span><span class="sxs-lookup"><span data-stu-id="47051-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="47051-114">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="47051-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="47051-115">C# 预处理器指令</span><span class="sxs-lookup"><span data-stu-id="47051-115">C# Preprocessor Directives</span></span>](./index.md)
- [<span data-ttu-id="47051-116">C# 编译器错误</span><span class="sxs-lookup"><span data-stu-id="47051-116">C# Compiler Errors</span></span>](../compiler-messages/index.md)
- [<span data-ttu-id="47051-117">如何禁止显示代码分析警告</span><span class="sxs-lookup"><span data-stu-id="47051-117">How to suppress code analysis warnings</span></span>](../../../fundamentals/code-analysis/suppress-warnings.md)

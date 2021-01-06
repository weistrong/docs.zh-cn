---
description: public 关键字 - C# 参考
title: public 关键字 - C# 参考
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 90c1d2a1d9efcdf57f914f4318bf7a743d3f37ec
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938463"
---
# <a name="public-c-reference"></a><span data-ttu-id="059ab-103">public（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="059ab-103">public (C# Reference)</span></span>

<span data-ttu-id="059ab-104">`public` 关键字是类型和类型成员的访问修饰符。</span><span class="sxs-lookup"><span data-stu-id="059ab-104">The `public` keyword is an access modifier for types and type members.</span></span> <span data-ttu-id="059ab-105">公共访问是允许的最高访问级别。</span><span class="sxs-lookup"><span data-stu-id="059ab-105">Public access is the most permissive access level.</span></span> <span data-ttu-id="059ab-106">对访问公共成员没有限制，如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="059ab-106">There are no restrictions on accessing public members, as in this example:</span></span>

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

<span data-ttu-id="059ab-107">有关详细信息，请参阅[访问修饰符](../../programming-guide/classes-and-structs/access-modifiers.md)和[可访问性级别](accessibility-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="059ab-107">See [Access Modifiers](../../programming-guide/classes-and-structs/access-modifiers.md) and [Accessibility Levels](accessibility-levels.md) for more information.</span></span>

## <a name="example"></a><span data-ttu-id="059ab-108">示例</span><span class="sxs-lookup"><span data-stu-id="059ab-108">Example</span></span>

<span data-ttu-id="059ab-109">在下面的示例中，声明了两个类：`PointTest` 和 `Program`。</span><span class="sxs-lookup"><span data-stu-id="059ab-109">In the following example, two classes are declared, `PointTest` and `Program`.</span></span> <span data-ttu-id="059ab-110">直接从 `Program` 访问 `PointTest` 的公共成员 `x` 和 `y`。</span><span class="sxs-lookup"><span data-stu-id="059ab-110">The public members `x` and `y` of `PointTest` are accessed directly from `Program`.</span></span>

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

<span data-ttu-id="059ab-111">如果将 `public` 访问级别更改为 [private](private.md) 或 [protected](protected.md)，则会收到错误消息：</span><span class="sxs-lookup"><span data-stu-id="059ab-111">If you change the `public` access level to [private](private.md) or [protected](protected.md), you will get the error message:</span></span>

<span data-ttu-id="059ab-112">“PointTest.y”不可访问，因为它受保护级别限制。</span><span class="sxs-lookup"><span data-stu-id="059ab-112">'PointTest.y' is inaccessible due to its protection level.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="059ab-113">C# 语言规范</span><span class="sxs-lookup"><span data-stu-id="059ab-113">C# language specification</span></span>  

<span data-ttu-id="059ab-114">有关详细信息，请参阅 [C# 语言规范](/dotnet/csharp/language-reference/language-specification/introduction)中的[声明的可访问性](~/_csharplang/spec/basic-concepts.md#declared-accessibility)。</span><span class="sxs-lookup"><span data-stu-id="059ab-114">For more information, see [Declared accessibility](~/_csharplang/spec/basic-concepts.md#declared-accessibility) in the [C# Language Specification](/dotnet/csharp/language-reference/language-specification/introduction).</span></span> <span data-ttu-id="059ab-115">该语言规范是 C# 语法和用法的权威资料。</span><span class="sxs-lookup"><span data-stu-id="059ab-115">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="059ab-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="059ab-116">See also</span></span>

- [<span data-ttu-id="059ab-117">C# 参考</span><span class="sxs-lookup"><span data-stu-id="059ab-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="059ab-118">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="059ab-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="059ab-119">访问修饰符</span><span class="sxs-lookup"><span data-stu-id="059ab-119">Access Modifiers</span></span>](../../programming-guide/classes-and-structs/access-modifiers.md)
- [<span data-ttu-id="059ab-120">C# 关键字</span><span class="sxs-lookup"><span data-stu-id="059ab-120">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="059ab-121">访问修饰符</span><span class="sxs-lookup"><span data-stu-id="059ab-121">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="059ab-122">可访问性级别</span><span class="sxs-lookup"><span data-stu-id="059ab-122">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="059ab-123">修饰符</span><span class="sxs-lookup"><span data-stu-id="059ab-123">Modifiers</span></span>](index.md)
- [<span data-ttu-id="059ab-124">private</span><span class="sxs-lookup"><span data-stu-id="059ab-124">private</span></span>](private.md)
- [<span data-ttu-id="059ab-125">受保护</span><span class="sxs-lookup"><span data-stu-id="059ab-125">protected</span></span>](protected.md)
- [<span data-ttu-id="059ab-126">internal</span><span class="sxs-lookup"><span data-stu-id="059ab-126">internal</span></span>](internal.md)

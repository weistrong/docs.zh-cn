---
title: 嵌套类型 - C# 编程指南
description: 在类、构造或接口中定义的类型称为 C# 中的嵌套类型。
ms.date: 02/08/2020
helpviewer_keywords:
- nested types [C#]
ms.assetid: f2e1b315-e3d1-48ce-977f-7bae0960ba99
ms.openlocfilehash: 0741ae88103b16ce34fd5a38b789beaf428e734a
ms.sourcegitcommit: 0014aa4d5cb2da56a70e03fc68f663d64df5247a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "96918575"
---
# <a name="nested-types-c-programming-guide"></a><span data-ttu-id="1883d-103">嵌套类型（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="1883d-103">Nested Types (C# Programming Guide)</span></span>

<span data-ttu-id="1883d-104">在[类](../../language-reference/keywords/class.md)、[构造](../../language-reference/builtin-types/struct.md)、[委托](../../language-reference/builtin-types/reference-types.md#the-delegate-type)或[接口](../../language-reference/keywords/interface.md)中定义的类型称为嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="1883d-104">A type defined within a [class](../../language-reference/keywords/class.md), [struct](../../language-reference/builtin-types/struct.md), [delegate](../../language-reference/builtin-types/reference-types.md#the-delegate-type) or [interface](../../language-reference/keywords/interface.md) is called a nested type.</span></span> <span data-ttu-id="1883d-105">例如</span><span class="sxs-lookup"><span data-stu-id="1883d-105">For example</span></span>

[!code-csharp[DeclareNestedClass](~/samples/snippets/csharp/objectoriented/nestedtypes.cs#DeclareNestedClass)]

<span data-ttu-id="1883d-106">不论外部类型是类、接口还是构造，嵌套类型均默认为 [private](../../language-reference/keywords/private.md)；仅可从其包含类型中进行访问。</span><span class="sxs-lookup"><span data-stu-id="1883d-106">Regardless of whether the outer type is a class, interface, or struct, nested types default to [private](../../language-reference/keywords/private.md); they are accessible only from their containing type.</span></span> <span data-ttu-id="1883d-107">在上一个示例中，`Nested` 类无法访问外部类型。</span><span class="sxs-lookup"><span data-stu-id="1883d-107">In the previous example, the `Nested` class is inaccessible to external types.</span></span>

<span data-ttu-id="1883d-108">还可指定[访问修饰符](../../language-reference/keywords/access-modifiers.md)来定义嵌套类型的可访问性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1883d-108">You can also specify an [access modifier](../../language-reference/keywords/access-modifiers.md) to define the accessibility of a nested type, as follows:</span></span>

- <span data-ttu-id="1883d-109">“类”的嵌套类型可以是 [public](../../language-reference/keywords/public.md)、[protected](../../language-reference/keywords/protected.md)、[internal](../../language-reference/keywords/internal.md)、[protected internal](../../language-reference/keywords/protected-internal.md)、[private](../../language-reference/keywords/private.md) 或 [private protected](../../language-reference/keywords/private-protected.md)。</span><span class="sxs-lookup"><span data-stu-id="1883d-109">Nested types of a **class** can be [public](../../language-reference/keywords/public.md), [protected](../../language-reference/keywords/protected.md), [internal](../../language-reference/keywords/internal.md), [protected internal](../../language-reference/keywords/protected-internal.md), [private](../../language-reference/keywords/private.md) or [private protected](../../language-reference/keywords/private-protected.md).</span></span>

   <span data-ttu-id="1883d-110">但是，在[密封类](../../language-reference/keywords/sealed.md)中定义 `protected`、`protected internal` 或 `private protected` 嵌套类将产生编译器警告 [CS0628](../../misc/cs0628.md)“封闭类汇中声明了新的受保护成员”。</span><span class="sxs-lookup"><span data-stu-id="1883d-110">However, defining a `protected`, `protected internal` or `private protected` nested class inside a [sealed class](../../language-reference/keywords/sealed.md) generates compiler warning [CS0628](../../misc/cs0628.md), "new protected member declared in sealed class."</span></span>
  
- <span data-ttu-id="1883d-111">构造的嵌套类型可以是 [public](../../language-reference/keywords/public.md)、[internal](../../language-reference/keywords/internal.md) 或 [private](../../language-reference/keywords/private.md)。</span><span class="sxs-lookup"><span data-stu-id="1883d-111">Nested types of a **struct** can be [public](../../language-reference/keywords/public.md), [internal](../../language-reference/keywords/internal.md), or [private](../../language-reference/keywords/private.md).</span></span>

<span data-ttu-id="1883d-112">以下示例使 `Nested` 类为 public：</span><span class="sxs-lookup"><span data-stu-id="1883d-112">The following example makes the `Nested` class public:</span></span>

[!code-csharp[PublicNestedClass](~/samples/snippets/csharp/objectoriented/nestedtypes.cs#PublicNestedClass)]

<span data-ttu-id="1883d-113">嵌套类型（或内部类型）可访问包含类型（或外部类型）。</span><span class="sxs-lookup"><span data-stu-id="1883d-113">The nested, or inner, type can access the containing, or outer, type.</span></span> <span data-ttu-id="1883d-114">若要访问包含类型，请将其作为参数传递给嵌套类型的构造函数。</span><span class="sxs-lookup"><span data-stu-id="1883d-114">To access the containing type, pass it as an argument to the constructor of the nested type.</span></span> <span data-ttu-id="1883d-115">例如：</span><span class="sxs-lookup"><span data-stu-id="1883d-115">For example:</span></span>

[!code-csharp[DeclareNestedInstance](~/samples/snippets/csharp/objectoriented/nestedtypes.cs#DeclareNestedInstance)]

<span data-ttu-id="1883d-116">嵌套类型可以访问其包含类型可以访问的所有成员。</span><span class="sxs-lookup"><span data-stu-id="1883d-116">A nested type has access to all of the members that are accessible to its containing type.</span></span> <span data-ttu-id="1883d-117">它可以访问包含类型的私有成员和受保护成员（包括所有继承的受保护成员）。</span><span class="sxs-lookup"><span data-stu-id="1883d-117">It can access private and protected members of the containing type, including any inherited protected members.</span></span>

<span data-ttu-id="1883d-118">在前面的声明中，类 `Nested` 的完整名称为 `Container.Nested`。</span><span class="sxs-lookup"><span data-stu-id="1883d-118">In the previous declaration, the full name of class `Nested` is `Container.Nested`.</span></span> <span data-ttu-id="1883d-119">这是用来创建嵌套类新实例的名称，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1883d-119">This is the name used to create a new instance of the nested class, as follows:</span></span>

[!code-csharp[UseNestedInstance](~/samples/snippets/csharp/objectoriented/nestedtypes.cs#UseNestedInstance)]

## <a name="see-also"></a><span data-ttu-id="1883d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="1883d-120">See also</span></span>

- [<span data-ttu-id="1883d-121">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="1883d-121">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="1883d-122">类和结构</span><span class="sxs-lookup"><span data-stu-id="1883d-122">Classes and Structs</span></span>](./index.md)
- [<span data-ttu-id="1883d-123">访问修饰符</span><span class="sxs-lookup"><span data-stu-id="1883d-123">Access Modifiers</span></span>](./access-modifiers.md)
- [<span data-ttu-id="1883d-124">构造函数</span><span class="sxs-lookup"><span data-stu-id="1883d-124">Constructors</span></span>](./constructors.md)

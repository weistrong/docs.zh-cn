---
description: '了解详细信息： Out (泛型修饰符)  (的 Visual Basic) '
title: Out（泛型修饰符）
ms.date: 07/20/2015
f1_keywords:
- vb.VarianceOut
helpviewer_keywords:
- Out keyword [Visual Basic]
- covariance, Out keyword [Visual Basic]
ms.assetid: c4418369-1518-4a46-9a1e-054c61038eca
ms.openlocfilehash: cdf80439fbae0d2411eecff1c7e8438534fcfdc1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730533"
---
# <a name="out-generic-modifier-visual-basic"></a><span data-ttu-id="58a36-103">Out（泛型修饰符）(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="58a36-103">Out (Generic Modifier) (Visual Basic)</span></span>

<span data-ttu-id="58a36-104">对于泛型类型参数， `Out` 关键字指定该类型是协变的。</span><span class="sxs-lookup"><span data-stu-id="58a36-104">For generic type parameters, the `Out` keyword specifies that the type is covariant.</span></span>

## <a name="remarks"></a><span data-ttu-id="58a36-105">备注</span><span class="sxs-lookup"><span data-stu-id="58a36-105">Remarks</span></span>

<span data-ttu-id="58a36-106">协变使你使用的类型可以比泛型参数指定的类型派生程度更大。</span><span class="sxs-lookup"><span data-stu-id="58a36-106">Covariance enables you to use a more derived type than that specified by the generic parameter.</span></span> <span data-ttu-id="58a36-107">这样可以隐式转换实现变体接口的类以及隐式转换委托类型。</span><span class="sxs-lookup"><span data-stu-id="58a36-107">This allows for implicit conversion of classes that implement variant interfaces and implicit conversion of delegate types.</span></span>

<span data-ttu-id="58a36-108">有关详细信息，请参阅[协变和逆变](../../programming-guide/concepts/covariance-contravariance/index.md)。</span><span class="sxs-lookup"><span data-stu-id="58a36-108">For more information, see [Covariance and Contravariance](../../programming-guide/concepts/covariance-contravariance/index.md).</span></span>

## <a name="rules"></a><span data-ttu-id="58a36-109">规则</span><span class="sxs-lookup"><span data-stu-id="58a36-109">Rules</span></span>

<span data-ttu-id="58a36-110">可以在泛型接口和委托中使用 `Out` 关键字。</span><span class="sxs-lookup"><span data-stu-id="58a36-110">You can use the `Out` keyword in generic interfaces and delegates.</span></span>

<span data-ttu-id="58a36-111">在泛型接口中，如果类型参数满足以下条件，则可以声明为协变：</span><span class="sxs-lookup"><span data-stu-id="58a36-111">In a generic interface, a type parameter can be declared covariant if it satisfies the following conditions:</span></span>

- <span data-ttu-id="58a36-112">类型参数只用作接口方法的返回类型，而不用作方法参数的类型。</span><span class="sxs-lookup"><span data-stu-id="58a36-112">The type parameter is used only as a return type of interface methods and not used as a type of method arguments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58a36-113">此规则有一个例外。</span><span class="sxs-lookup"><span data-stu-id="58a36-113">There is one exception to this rule.</span></span> <span data-ttu-id="58a36-114">如果在协变接口中将逆变泛型委托用作方法参数，则可以将协变类型用作此委托的泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="58a36-114">If in a covariant interface you have a contravariant generic delegate as a method parameter, you can use the covariant type as a generic type parameter for this delegate.</span></span> <span data-ttu-id="58a36-115">有关协变和逆变泛型委托的详细信息，请参阅[委托中的变体](../../programming-guide/concepts/covariance-contravariance/variance-in-delegates.md)和[对 Func 和 Action 泛型委托使用变体](../../programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md)。</span><span class="sxs-lookup"><span data-stu-id="58a36-115">For more information about covariant and contravariant generic delegates, see [Variance in Delegates](../../programming-guide/concepts/covariance-contravariance/variance-in-delegates.md) and [Using Variance for Func and Action Generic Delegates](../../programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md).</span></span>

- <span data-ttu-id="58a36-116">类型参数不用作接口方法的泛型约束。</span><span class="sxs-lookup"><span data-stu-id="58a36-116">The type parameter is not used as a generic constraint for the interface methods.</span></span>

<span data-ttu-id="58a36-117">在泛型委托中，如果类型参数仅用作方法返回类型并且不用于方法参数，则可以声明为协变。</span><span class="sxs-lookup"><span data-stu-id="58a36-117">In a generic delegate, a type parameter can be declared covariant if it is used only as a method return type and not used for method arguments.</span></span>

<span data-ttu-id="58a36-118">引用类型支持协变和逆变，但值类型不支持它们。</span><span class="sxs-lookup"><span data-stu-id="58a36-118">Covariance and contravariance are supported for reference types, but they are not supported for value types.</span></span>

<span data-ttu-id="58a36-119">在 Visual Basic 中，如果不指定委托类型，则不能在协变接口中声明事件。</span><span class="sxs-lookup"><span data-stu-id="58a36-119">In Visual Basic, you cannot declare events in covariant interfaces without specifying the delegate type.</span></span> <span data-ttu-id="58a36-120">此外，协变接口不能具有嵌套的类、枚举或结构，但它们可以具有嵌套接口。</span><span class="sxs-lookup"><span data-stu-id="58a36-120">Also, covariant interfaces cannot have nested classes, enums, or structures, but they can have nested interfaces.</span></span>

## <a name="behavior"></a><span data-ttu-id="58a36-121">行为</span><span class="sxs-lookup"><span data-stu-id="58a36-121">Behavior</span></span>

<span data-ttu-id="58a36-122">具有协变类型参数的接口使其方法返回的类型可以比类型参数指定的类型派生程度更大。</span><span class="sxs-lookup"><span data-stu-id="58a36-122">An interface that has a covariant type parameter enables its methods to return more derived types than those specified by the type parameter.</span></span> <span data-ttu-id="58a36-123">例如，因为在 .NET Framework 4 的 <xref:System.Collections.Generic.IEnumerable%601> 中，类型 T 是协变的，所以可以将 `IEnumerable(Of String)` 类型的对象分配给 `IEnumerable(Of Object)` 类型的对象，而无需使用任何特殊转换方法。</span><span class="sxs-lookup"><span data-stu-id="58a36-123">For example, because in .NET Framework 4, in <xref:System.Collections.Generic.IEnumerable%601>, type T is covariant, you can assign an object of the `IEnumerable(Of String)` type to an object of the `IEnumerable(Of Object)` type without using any special conversion methods.</span></span>

<span data-ttu-id="58a36-124">可以向协变委托分配相同类型的其他委托，不过要使用派生程度更大的泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="58a36-124">A covariant delegate can be assigned another delegate of the same type, but with a more derived generic type parameter.</span></span>

## <a name="example"></a><span data-ttu-id="58a36-125">示例</span><span class="sxs-lookup"><span data-stu-id="58a36-125">Example</span></span>

<span data-ttu-id="58a36-126">下面的示例演示如何声明、扩展和实现协变泛型接口。</span><span class="sxs-lookup"><span data-stu-id="58a36-126">The following example shows how to declare, extend, and implement a covariant generic interface.</span></span> <span data-ttu-id="58a36-127">它还演示如何对实现协变接口的类使用隐式转换。</span><span class="sxs-lookup"><span data-stu-id="58a36-127">It also shows how to use implicit conversion for classes that implement a covariant interface.</span></span>

[!code-vb[vbVarianceKeywords#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvariancekeywords/vb/module1.vb#3)]

## <a name="example"></a><span data-ttu-id="58a36-128">示例</span><span class="sxs-lookup"><span data-stu-id="58a36-128">Example</span></span>

<span data-ttu-id="58a36-129">以下示例演示如何声明、实例化和调用协变泛型委托。</span><span class="sxs-lookup"><span data-stu-id="58a36-129">The following example shows how to declare, instantiate, and invoke a covariant generic delegate.</span></span> <span data-ttu-id="58a36-130">它还演示了如何对委托类型使用隐式转换。</span><span class="sxs-lookup"><span data-stu-id="58a36-130">It also shows how you can use implicit conversion for delegate types.</span></span>

[!code-vb[vbVarianceKeywords#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvariancekeywords/vb/module1.vb#4)]

## <a name="see-also"></a><span data-ttu-id="58a36-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="58a36-131">See also</span></span>

- [<span data-ttu-id="58a36-132">泛型接口中的变体</span><span class="sxs-lookup"><span data-stu-id="58a36-132">Variance in Generic Interfaces</span></span>](../../programming-guide/concepts/covariance-contravariance/variance-in-generic-interfaces.md)
- [<span data-ttu-id="58a36-133">位于</span><span class="sxs-lookup"><span data-stu-id="58a36-133">In</span></span>](in-generic-modifier.md)

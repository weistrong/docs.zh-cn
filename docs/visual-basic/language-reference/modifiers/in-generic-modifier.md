---
description: '详细了解：在 (泛型修饰符中)  (Visual Basic) '
title: 在 (泛型修饰符) -Visual Basic
ms.date: 07/20/2015
f1_keywords:
- vb.VarianceIn
helpviewer_keywords:
- contravariance, In keyword [Visual Basic]
- In keyword [Visual Basic]
ms.assetid: 59bb13c5-fe96-42b8-8286-86293d1661c5
ms.openlocfilehash: e6ac95a77253b28e45a4be8a29623bdd76a231f1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774533"
---
# <a name="in-generic-modifier-visual-basic"></a><span data-ttu-id="9dc87-103">In（泛型修饰符）(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9dc87-103">In (Generic Modifier) (Visual Basic)</span></span>

<span data-ttu-id="9dc87-104">对于泛型类型参数，`In` 关键字可指定类型参数是逆变的。</span><span class="sxs-lookup"><span data-stu-id="9dc87-104">For generic type parameters, the `In` keyword specifies that the type parameter is contravariant.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc87-105">备注</span><span class="sxs-lookup"><span data-stu-id="9dc87-105">Remarks</span></span>

<span data-ttu-id="9dc87-106">逆变使你使用的类型可以比泛型参数指定的类型派生程度更小。</span><span class="sxs-lookup"><span data-stu-id="9dc87-106">Contravariance enables you to use a less derived type than that specified by the generic parameter.</span></span> <span data-ttu-id="9dc87-107">这样可以隐式转换实现变体接口的类以及隐式转换委托类型。</span><span class="sxs-lookup"><span data-stu-id="9dc87-107">This allows for implicit conversion of classes that implement variant interfaces and implicit conversion of delegate types.</span></span>

<span data-ttu-id="9dc87-108">有关详细信息，请参阅[协变和逆变](../../programming-guide/concepts/covariance-contravariance/index.md)。</span><span class="sxs-lookup"><span data-stu-id="9dc87-108">For more information, see [Covariance and Contravariance](../../programming-guide/concepts/covariance-contravariance/index.md).</span></span>

## <a name="rules"></a><span data-ttu-id="9dc87-109">规则</span><span class="sxs-lookup"><span data-stu-id="9dc87-109">Rules</span></span>

<span data-ttu-id="9dc87-110">可以在泛型接口和委托中使用 `In` 关键字。</span><span class="sxs-lookup"><span data-stu-id="9dc87-110">You can use the `In` keyword in generic interfaces and delegates.</span></span>
  
<span data-ttu-id="9dc87-111">如果类型参数仅用作方法参数的类型并且不用作方法返回类型，则可以在泛型接口或委托中声明为逆变。</span><span class="sxs-lookup"><span data-stu-id="9dc87-111">A type parameter can be declared contravariant in a generic interface or delegate if it is used only as a type of method arguments and not used as a method return type.</span></span> <span data-ttu-id="9dc87-112">`ByRef` 参数不能是协变或逆变。</span><span class="sxs-lookup"><span data-stu-id="9dc87-112">`ByRef` parameters cannot be covariant or contravariant.</span></span>

<span data-ttu-id="9dc87-113">引用类型支持协变和逆变，但值类型不支持协变和逆变。</span><span class="sxs-lookup"><span data-stu-id="9dc87-113">Covariance and contravariance are supported for reference types and not supported for value types.</span></span>

<span data-ttu-id="9dc87-114">在 Visual Basic 中，不能声明逆变接口中的事件，而无需指定委托类型。</span><span class="sxs-lookup"><span data-stu-id="9dc87-114">In Visual Basic, you cannot declare events in contravariant interfaces without specifying the delegate type.</span></span> <span data-ttu-id="9dc87-115">此外，逆变接口不能有嵌套的类、枚举或结构，但它们可以有嵌套的接口。</span><span class="sxs-lookup"><span data-stu-id="9dc87-115">Also, contravariant interfaces cannot have nested classes, enums, or structures, but they can have nested interfaces.</span></span>

## <a name="behavior"></a><span data-ttu-id="9dc87-116">行为</span><span class="sxs-lookup"><span data-stu-id="9dc87-116">Behavior</span></span>

<span data-ttu-id="9dc87-117">具有逆变类型参数的接口使其方法接受的参数的类型可以比接口类型参数指定的类型派生程度更小。</span><span class="sxs-lookup"><span data-stu-id="9dc87-117">An interface that has a contravariant type parameter allows its methods to accept arguments of less derived types than those specified by the interface type parameter.</span></span> <span data-ttu-id="9dc87-118">例如，因为在 .NET Framework 4 的接口中， <xref:System.Collections.Generic.IComparer%601> 类型 T 是逆变的，所以可以将类型的对象分配 `IComparer(Of Person)` 给类型的对象， `IComparer(Of Employee)` 而无需使用任何特殊转换方法（如果 `Employee` 从继承） `Person` 。</span><span class="sxs-lookup"><span data-stu-id="9dc87-118">For example, because in .NET Framework 4, in the <xref:System.Collections.Generic.IComparer%601> interface, type T is contravariant, you can assign an object of the `IComparer(Of Person)` type to an object of the `IComparer(Of Employee)` type without using any special conversion methods if `Employee` inherits from `Person`.</span></span>

<span data-ttu-id="9dc87-119">可以向逆变委托分配相同类型的其他委托，不过要使用派生程度更小的泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="9dc87-119">A contravariant delegate can be assigned another delegate of the same type, but with a less derived generic type parameter.</span></span>

## <a name="example---contravariant-generic-interface"></a><span data-ttu-id="9dc87-120">示例-逆变泛型接口</span><span class="sxs-lookup"><span data-stu-id="9dc87-120">Example - contravariant generic interface</span></span>

<span data-ttu-id="9dc87-121">下面的示例演示如何声明、扩展和实现逆变泛型接口。</span><span class="sxs-lookup"><span data-stu-id="9dc87-121">The following example shows how to declare, extend, and implement a contravariant generic interface.</span></span> <span data-ttu-id="9dc87-122">它还演示如何对实现此接口的类使用隐式转换。</span><span class="sxs-lookup"><span data-stu-id="9dc87-122">It also shows how you can use implicit conversion for classes that implement this interface.</span></span>

[!code-vb[vbVarianceKeywords#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvariancekeywords/vb/module1.vb#1)]

## <a name="example---contravariant-generic-delegate"></a><span data-ttu-id="9dc87-123">示例-逆变泛型委托</span><span class="sxs-lookup"><span data-stu-id="9dc87-123">Example - contravariant generic delegate</span></span>

<span data-ttu-id="9dc87-124">以下示例演示如何声明、实例化和调用逆变泛型委托。</span><span class="sxs-lookup"><span data-stu-id="9dc87-124">The following example shows how to declare, instantiate, and invoke a contravariant generic delegate.</span></span> <span data-ttu-id="9dc87-125">它还演示如何隐式转换委托类型。</span><span class="sxs-lookup"><span data-stu-id="9dc87-125">It also shows how you can implicitly convert a delegate type.</span></span>

[!code-vb[vbVarianceKeywords#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvariancekeywords/vb/module1.vb#2)]

## <a name="see-also"></a><span data-ttu-id="9dc87-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="9dc87-126">See also</span></span>

- [<span data-ttu-id="9dc87-127">泛型接口中的变体</span><span class="sxs-lookup"><span data-stu-id="9dc87-127">Variance in Generic Interfaces</span></span>](../../programming-guide/concepts/covariance-contravariance/variance-in-generic-interfaces.md)
- [<span data-ttu-id="9dc87-128">Out</span><span class="sxs-lookup"><span data-stu-id="9dc87-128">Out</span></span>](out-generic-modifier.md)

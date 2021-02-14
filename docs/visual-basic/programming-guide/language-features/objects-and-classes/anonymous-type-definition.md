---
description: '了解详细信息：匿名类型定义 (Visual Basic) '
title: 匿名类型定义
ms.date: 07/20/2015
helpviewer_keywords:
- anonymous types [Visual Basic], type definition
ms.assetid: 7a8a0ddc-55ba-4d67-869e-87a84d938bac
ms.openlocfilehash: 2e3f847f5f844e3ed6e036c26efc330a237d193f
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100436911"
---
# <a name="anonymous-type-definition-visual-basic"></a><span data-ttu-id="559a3-103">匿名类型定义 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="559a3-103">Anonymous Type Definition (Visual Basic)</span></span>

<span data-ttu-id="559a3-104">为了响应匿名类型的实例的声明，编译器会创建一个新的类定义，其中包含类型的指定属性。</span><span class="sxs-lookup"><span data-stu-id="559a3-104">In response to the declaration of an instance of an anonymous type, the compiler creates a new class definition that contains the specified properties for the type.</span></span>

## <a name="compiler-generated-code"></a><span data-ttu-id="559a3-105">Compiler-Generated 代码</span><span class="sxs-lookup"><span data-stu-id="559a3-105">Compiler-Generated Code</span></span>

<span data-ttu-id="559a3-106">对于的以下定义 `product` ，编译器将创建包含属性、和的新类定义 `Name` `Price` `OnHand` 。</span><span class="sxs-lookup"><span data-stu-id="559a3-106">For the following definition of `product`, the compiler creates a new class definition that contains properties `Name`, `Price`, and `OnHand`.</span></span>

[!code-vb[VbVbalrAnonymousTypes#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#25)]

<span data-ttu-id="559a3-107">类定义包含如下所示的属性定义。</span><span class="sxs-lookup"><span data-stu-id="559a3-107">The class definition contains property definitions similar to the following.</span></span> <span data-ttu-id="559a3-108">请注意，没有 `Set` 用于键属性的方法。</span><span class="sxs-lookup"><span data-stu-id="559a3-108">Notice that there is no `Set` method for the key properties.</span></span> <span data-ttu-id="559a3-109">键属性的值是只读的。</span><span class="sxs-lookup"><span data-stu-id="559a3-109">The values of key properties are read-only.</span></span>

```vb
Public Class $Anonymous1
    Private _name As String
    Private _price As Double
    Private _onHand As Integer
     Public ReadOnly Property Name() As String
        Get
            Return _name
        End Get
    End Property

    Public ReadOnly Property Price() As Double
        Get
            Return _price
        End Get
    End Property

    Public Property OnHand() As Integer
        Get
            Return _onHand
        End Get
        Set(ByVal Value As Integer)
            _onHand = Value
        End Set
    End Property

End Class
```

<span data-ttu-id="559a3-110">此外，匿名类型定义包含一个无参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="559a3-110">In addition, anonymous type definitions contain a parameterless constructor.</span></span> <span data-ttu-id="559a3-111">不允许使用需要参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="559a3-111">Constructors that require parameters are not permitted.</span></span>

<span data-ttu-id="559a3-112">如果匿名类型声明至少包含一个键属性，则类型定义将重写继承自的三个成员 <xref:System.Object> ： <xref:System.Object.Equals%2A> 、 <xref:System.Object.GetHashCode%2A> 和 <xref:System.Object.ToString%2A> 。</span><span class="sxs-lookup"><span data-stu-id="559a3-112">If an anonymous type declaration contains at least one key property, the type definition overrides three members inherited from <xref:System.Object>: <xref:System.Object.Equals%2A>, <xref:System.Object.GetHashCode%2A>, and <xref:System.Object.ToString%2A>.</span></span> <span data-ttu-id="559a3-113">如果未声明键属性，则只 <xref:System.Object.ToString%2A> 会重写。</span><span class="sxs-lookup"><span data-stu-id="559a3-113">If no key properties are declared, only <xref:System.Object.ToString%2A> is overridden.</span></span> <span data-ttu-id="559a3-114">替代提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="559a3-114">The overrides provide the following functionality:</span></span>

- <span data-ttu-id="559a3-115">`Equals``True`如果两个匿名类型实例为同一实例，则返回; 如果满足以下条件，则返回：</span><span class="sxs-lookup"><span data-stu-id="559a3-115">`Equals` returns `True` if two anonymous type instances are the same instance, or if they meet the following conditions:</span></span>

  - <span data-ttu-id="559a3-116">它们具有相同数量的属性。</span><span class="sxs-lookup"><span data-stu-id="559a3-116">They have the same number of properties.</span></span>

  - <span data-ttu-id="559a3-117">属性以相同顺序声明，具有相同的名称和相同的推断类型。</span><span class="sxs-lookup"><span data-stu-id="559a3-117">The properties are declared in the same order, with the same names and the same inferred types.</span></span> <span data-ttu-id="559a3-118">名称比较不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="559a3-118">Name comparisons are not case-sensitive.</span></span>

  - <span data-ttu-id="559a3-119">至少一个属性是键属性，并且 `Key` 关键字应用于相同的属性。</span><span class="sxs-lookup"><span data-stu-id="559a3-119">At least one of the properties is a key property, and the `Key` keyword is applied to the same properties.</span></span>

  - <span data-ttu-id="559a3-120">每个对应的键属性对的比较都将返回 `True` 。</span><span class="sxs-lookup"><span data-stu-id="559a3-120">Comparison of each corresponding pair of key properties returns `True`.</span></span>

    <span data-ttu-id="559a3-121">例如，在下面的示例中， `Equals` `True` 仅为 `employee01` 和返回 `employee08` 。</span><span class="sxs-lookup"><span data-stu-id="559a3-121">For example, in the following examples, `Equals` returns `True` only for `employee01` and `employee08`.</span></span> <span data-ttu-id="559a3-122">每行前的注释指定新实例不匹配的原因 `employee01` 。</span><span class="sxs-lookup"><span data-stu-id="559a3-122">The comment before each line specifies the reason why the new instance does not match `employee01`.</span></span>

    [!code-vb[VbVbalrAnonymousTypes#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#24)]

- <span data-ttu-id="559a3-123">`GetHashcode` 提供适当唯一的 GetHashCode 算法。</span><span class="sxs-lookup"><span data-stu-id="559a3-123">`GetHashcode` provides an appropriately unique GetHashCode algorithm.</span></span> <span data-ttu-id="559a3-124">算法只使用键属性来计算哈希代码。</span><span class="sxs-lookup"><span data-stu-id="559a3-124">The algorithm uses only the key properties to compute the hash code.</span></span>

- <span data-ttu-id="559a3-125">`ToString` 返回连接的属性值的字符串，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="559a3-125">`ToString` returns a string of concatenated property values, as shown in the following example.</span></span> <span data-ttu-id="559a3-126">同时包含键属性和非键属性。</span><span class="sxs-lookup"><span data-stu-id="559a3-126">Both key and non-key properties are included.</span></span>

  [!code-vb[VbVbalrAnonymousTypes#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#29)]

<span data-ttu-id="559a3-127">匿名类型的显式命名属性不能与这些生成的方法冲突。</span><span class="sxs-lookup"><span data-stu-id="559a3-127">Explicitly named properties of an anonymous type cannot conflict with these generated methods.</span></span> <span data-ttu-id="559a3-128">也就是说，不能使用 `.Equals` 、 `.GetHashCode` 或 `.ToString` 对属性命名。</span><span class="sxs-lookup"><span data-stu-id="559a3-128">That is, you cannot use `.Equals`, `.GetHashCode`, or `.ToString` to name a property.</span></span>

<span data-ttu-id="559a3-129">包含至少一个键属性的匿名类型定义还实现 <xref:System.IEquatable%601?displayProperty=nameWithType> 接口，其中 `T` 是匿名类型的类型。</span><span class="sxs-lookup"><span data-stu-id="559a3-129">Anonymous type definitions that include at least one key property also implement the <xref:System.IEquatable%601?displayProperty=nameWithType> interface, where `T` is the type of the anonymous type.</span></span>

> [!NOTE]
> <span data-ttu-id="559a3-130">仅当匿名类型声明出现在同一程序集中时，才创建相同的匿名类型，其属性具有相同的名称和相同的推断类型，属性以相同顺序声明，相同的属性被标记为键属性。</span><span class="sxs-lookup"><span data-stu-id="559a3-130">Anonymous type declarations create the same anonymous type only if they occur in the same assembly, their properties have the same names and the same inferred types, the properties are declared in the same order, and the same properties are marked as key properties.</span></span>

## <a name="see-also"></a><span data-ttu-id="559a3-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="559a3-131">See also</span></span>

- [<span data-ttu-id="559a3-132">匿名类型</span><span class="sxs-lookup"><span data-stu-id="559a3-132">Anonymous Types</span></span>](anonymous-types.md)
- [<span data-ttu-id="559a3-133">如何：推断匿名类型声明中的属性名和类型</span><span class="sxs-lookup"><span data-stu-id="559a3-133">How to: Infer Property Names and Types in Anonymous Type Declarations</span></span>](how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)

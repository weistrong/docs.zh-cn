---
description: '详细了解： of 子句 (Visual Basic) '
title: Of 子句
ms.date: 07/20/2015
f1_keywords:
- Of
- vb.Of
- vb.of
helpviewer_keywords:
- Of keyword [Visual Basic]
- arguments [Visual Basic], data types
- constraints, Visual Basic generic types
- generic parameters
- generics [Visual Basic], constraints
- parameters [Visual Basic], type
- types [Visual Basic], generic
- parameters [Visual Basic], generic
- type parameters
- data type arguments
ms.assetid: 0db8f65c-65af-4089-ab7f-6fcfecb60444
ms.openlocfilehash: d6002041a2fe8db5b07e12e9e396a65fde30b716
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768839"
---
# <a name="of-clause-visual-basic"></a><span data-ttu-id="89714-103">Of 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="89714-103">Of Clause (Visual Basic)</span></span>

<span data-ttu-id="89714-104">引入一个 `Of` 子句，该子句标识 *泛型* 类、结构、接口、委托或过程中的 *类型参数*。</span><span class="sxs-lookup"><span data-stu-id="89714-104">Introduces an `Of` clause, which identifies a *type parameter* on a *generic* class, structure, interface, delegate, or procedure.</span></span> <span data-ttu-id="89714-105">有关泛型类型的信息，请参阅 [Visual Basic 中的泛型类型](../../programming-guide/language-features/data-types/generic-types.md)。</span><span class="sxs-lookup"><span data-stu-id="89714-105">For information on generic types, see [Generic Types in Visual Basic](../../programming-guide/language-features/data-types/generic-types.md).</span></span>  
  
## <a name="using-the-of-keyword"></a><span data-ttu-id="89714-106">使用关键字 of</span><span class="sxs-lookup"><span data-stu-id="89714-106">Using the Of Keyword</span></span>  

 <span data-ttu-id="89714-107">下面的代码示例使用 `Of` 关键字定义带有两个类型参数的类的轮廓。</span><span class="sxs-lookup"><span data-stu-id="89714-107">The following code example uses the `Of` keyword to define the outline of a class that takes two type parameters.</span></span> <span data-ttu-id="89714-108">它 `keyType` 通过接口约束参数 <xref:System.IComparable> ，这意味着使用的代码必须提供实现的类型参数 <xref:System.IComparable> 。</span><span class="sxs-lookup"><span data-stu-id="89714-108">It *constrains* the `keyType` parameter by the <xref:System.IComparable> interface, which means the consuming code must supply a type argument that implements <xref:System.IComparable>.</span></span> <span data-ttu-id="89714-109">这是必需的，以便 `add` 过程可以调用 <xref:System.IComparable.CompareTo%2A?displayProperty=nameWithType> 方法。</span><span class="sxs-lookup"><span data-stu-id="89714-109">This is necessary so that the `add` procedure can call the <xref:System.IComparable.CompareTo%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="89714-110">有关约束的详细信息，请参阅 [Type List](type-list.md)。</span><span class="sxs-lookup"><span data-stu-id="89714-110">For more information on constraints, see [Type List](type-list.md).</span></span>  
  
```vb  
Public Class Dictionary(Of entryType, keyType As IComparable)  
    Public Sub add(ByVal e As entryType, ByVal k As keyType)  
        Dim dk As keyType  
        If k.CompareTo(dk) = 0 Then  
        End If  
    End Sub  
    Public Function find(ByVal k As keyType) As entryType  
    End Function  
End Class  
```  
  
 <span data-ttu-id="89714-111">如果你完成了前面的类定义，则可以构造其中的各种 `dictionary` 类。</span><span class="sxs-lookup"><span data-stu-id="89714-111">If you complete the preceding class definition, you can construct a variety of `dictionary` classes from it.</span></span> <span data-ttu-id="89714-112">提供给的类型， `entryType` 并 `keyType` 确定类包含的项的类型以及它与每个项关联的键的类型。</span><span class="sxs-lookup"><span data-stu-id="89714-112">The types you supply to `entryType` and `keyType` determine what type of entry the class holds and what type of key it associates with each entry.</span></span> <span data-ttu-id="89714-113">由于约束的原因，您必须提供 `keyType` 实现的类型 <xref:System.IComparable> 。</span><span class="sxs-lookup"><span data-stu-id="89714-113">Because of the constraint, you must supply to `keyType` a type that implements <xref:System.IComparable>.</span></span>  
  
 <span data-ttu-id="89714-114">下面的代码示例创建一个对象，该对象保存 `String` 项并将 `Integer` 键与每个项关联。</span><span class="sxs-lookup"><span data-stu-id="89714-114">The following code example creates an object that holds `String` entries and associates an `Integer` key with each one.</span></span> <span data-ttu-id="89714-115">`Integer` 实现 <xref:System.IComparable> 并因此满足上的约束 `keyType` 。</span><span class="sxs-lookup"><span data-stu-id="89714-115">`Integer` implements <xref:System.IComparable> and therefore satisfies the constraint on `keyType`.</span></span>  
  
```vb  
Dim d As New dictionary(Of String, Integer)  
```  
  
 <span data-ttu-id="89714-116">`Of` 关键字可用于以下上下文中：</span><span class="sxs-lookup"><span data-stu-id="89714-116">The `Of` keyword can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="89714-117">Class 语句</span><span class="sxs-lookup"><span data-stu-id="89714-117">Class Statement</span></span>](class-statement.md)  
  
 [<span data-ttu-id="89714-118">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="89714-118">Delegate Statement</span></span>](delegate-statement.md)  
  
 [<span data-ttu-id="89714-119">Function 语句</span><span class="sxs-lookup"><span data-stu-id="89714-119">Function Statement</span></span>](function-statement.md)  
  
 [<span data-ttu-id="89714-120">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="89714-120">Interface Statement</span></span>](interface-statement.md)  
  
 [<span data-ttu-id="89714-121">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="89714-121">Structure Statement</span></span>](structure-statement.md)  
  
 [<span data-ttu-id="89714-122">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="89714-122">Sub Statement</span></span>](sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="89714-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="89714-123">See also</span></span>

- <xref:System.IComparable>
- [<span data-ttu-id="89714-124">Type List</span><span class="sxs-lookup"><span data-stu-id="89714-124">Type List</span></span>](type-list.md)
- [<span data-ttu-id="89714-125">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="89714-125">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="89714-126">位于</span><span class="sxs-lookup"><span data-stu-id="89714-126">In</span></span>](../modifiers/in-generic-modifier.md)
- [<span data-ttu-id="89714-127">Out</span><span class="sxs-lookup"><span data-stu-id="89714-127">Out</span></span>](../modifiers/out-generic-modifier.md)

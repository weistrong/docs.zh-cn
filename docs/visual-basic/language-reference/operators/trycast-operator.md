---
description: '详细了解： TryCast Operator (Visual Basic) '
title: TryCast 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.trycast
- trycast
helpviewer_keywords:
- TryCast keyword [Visual Basic]
ms.assetid: d1ef5d47-fef4-491e-b014-1d910628f65c
ms.openlocfilehash: 5b941ec40c4ba0198fced64d0ef039605efad472
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795243"
---
# <a name="trycast-operator-visual-basic"></a><span data-ttu-id="d8fec-103">TryCast 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8fec-103">TryCast Operator (Visual Basic)</span></span>

<span data-ttu-id="d8fec-104">引入不引发异常的类型转换操作。</span><span class="sxs-lookup"><span data-stu-id="d8fec-104">Introduces a type conversion operation that does not throw an exception.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d8fec-105">备注</span><span class="sxs-lookup"><span data-stu-id="d8fec-105">Remarks</span></span>  

 <span data-ttu-id="d8fec-106">如果尝试的转换失败，则会 `CType` `DirectCast` 引发 <xref:System.InvalidCastException> 错误。</span><span class="sxs-lookup"><span data-stu-id="d8fec-106">If an attempted conversion fails, `CType` and `DirectCast` both throw an <xref:System.InvalidCastException> error.</span></span> <span data-ttu-id="d8fec-107">这会对应用程序的性能产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="d8fec-107">This can adversely affect the performance of your application.</span></span> <span data-ttu-id="d8fec-108">`TryCast` 不返回 [任何内容](../nothing.md)，因此只需测试返回的结果，而无需处理可能出现的异常 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="d8fec-108">`TryCast` returns [Nothing](../nothing.md), so that instead of having to handle a possible exception, you need only test the returned result against `Nothing`.</span></span>  
  
 <span data-ttu-id="d8fec-109">`TryCast`关键字的使用方式与使用[CType 函数](../functions/ctype-function.md)和[DirectCast 运算符](directcast-operator.md)关键字相同。</span><span class="sxs-lookup"><span data-stu-id="d8fec-109">You use the `TryCast` keyword the same way you use the [CType Function](../functions/ctype-function.md) and the [DirectCast Operator](directcast-operator.md) keyword.</span></span> <span data-ttu-id="d8fec-110">提供表达式作为第一个参数，并提供一个类型以将其转换为第二个参数。</span><span class="sxs-lookup"><span data-stu-id="d8fec-110">You supply an expression as the first argument and a type to convert it to as the second argument.</span></span> <span data-ttu-id="d8fec-111">`TryCast` 仅对引用类型（如类和接口）进行操作。</span><span class="sxs-lookup"><span data-stu-id="d8fec-111">`TryCast` operates only on reference types, such as classes and interfaces.</span></span> <span data-ttu-id="d8fec-112">它需要这两个类型之间的继承关系或实现关系。</span><span class="sxs-lookup"><span data-stu-id="d8fec-112">It requires an inheritance or implementation relationship between the two types.</span></span> <span data-ttu-id="d8fec-113">这意味着一个类型必须从继承或实现另一个类型。</span><span class="sxs-lookup"><span data-stu-id="d8fec-113">This means that one type must inherit from or implement the other.</span></span>  
  
## <a name="errors-and-failures"></a><span data-ttu-id="d8fec-114">错误和失败</span><span class="sxs-lookup"><span data-stu-id="d8fec-114">Errors and Failures</span></span>  

 <span data-ttu-id="d8fec-115">`TryCast` 如果检测到不存在继承或实现关系，则会生成编译器错误。</span><span class="sxs-lookup"><span data-stu-id="d8fec-115">`TryCast` generates a compiler error if it detects that no inheritance or implementation relationship exists.</span></span> <span data-ttu-id="d8fec-116">但缺少编译器错误并不能保证成功转换。</span><span class="sxs-lookup"><span data-stu-id="d8fec-116">But the lack of a compiler error does not guarantee a successful conversion.</span></span> <span data-ttu-id="d8fec-117">如果所需的转换是收缩转换，则可能会在运行时失败。</span><span class="sxs-lookup"><span data-stu-id="d8fec-117">If the desired conversion is narrowing, it could fail at run time.</span></span> <span data-ttu-id="d8fec-118">如果发生这种情况，则不 `TryCast` 返回 [任何内容](../nothing.md)。</span><span class="sxs-lookup"><span data-stu-id="d8fec-118">If this happens, `TryCast` returns [Nothing](../nothing.md).</span></span>  
  
## <a name="conversion-keywords"></a><span data-ttu-id="d8fec-119">转换关键字</span><span class="sxs-lookup"><span data-stu-id="d8fec-119">Conversion Keywords</span></span>  

 <span data-ttu-id="d8fec-120">下面是类型转换关键字的比较。</span><span class="sxs-lookup"><span data-stu-id="d8fec-120">A comparison of the type conversion keywords is as follows.</span></span>  
  
|<span data-ttu-id="d8fec-121">关键字</span><span class="sxs-lookup"><span data-stu-id="d8fec-121">Keyword</span></span>|<span data-ttu-id="d8fec-122">数据类型</span><span class="sxs-lookup"><span data-stu-id="d8fec-122">Data types</span></span>|<span data-ttu-id="d8fec-123">参数关系</span><span class="sxs-lookup"><span data-stu-id="d8fec-123">Argument relationship</span></span>|<span data-ttu-id="d8fec-124">运行时失败</span><span class="sxs-lookup"><span data-stu-id="d8fec-124">Run-time failure</span></span>|  
|---|---|---|---|  
|[<span data-ttu-id="d8fec-125">CType Function</span><span class="sxs-lookup"><span data-stu-id="d8fec-125">CType Function</span></span>](../functions/ctype-function.md)|<span data-ttu-id="d8fec-126">任何数据类型</span><span class="sxs-lookup"><span data-stu-id="d8fec-126">Any data types</span></span>|<span data-ttu-id="d8fec-127">必须在这两种数据类型之间定义扩大转换或收缩转换</span><span class="sxs-lookup"><span data-stu-id="d8fec-127">Widening or narrowing conversion must be defined between the two data types</span></span>|<span data-ttu-id="d8fec-128">却 <xref:System.InvalidCastException></span><span class="sxs-lookup"><span data-stu-id="d8fec-128">Throws <xref:System.InvalidCastException></span></span>|  
|[<span data-ttu-id="d8fec-129">DirectCast 运算符</span><span class="sxs-lookup"><span data-stu-id="d8fec-129">DirectCast Operator</span></span>](directcast-operator.md)|<span data-ttu-id="d8fec-130">任何数据类型</span><span class="sxs-lookup"><span data-stu-id="d8fec-130">Any data types</span></span>|<span data-ttu-id="d8fec-131">一个类型必须继承自或实现另一个类型</span><span class="sxs-lookup"><span data-stu-id="d8fec-131">One type must inherit from or implement the other type</span></span>|<span data-ttu-id="d8fec-132">却 <xref:System.InvalidCastException></span><span class="sxs-lookup"><span data-stu-id="d8fec-132">Throws <xref:System.InvalidCastException></span></span>|  
|`TryCast`|<span data-ttu-id="d8fec-133">仅引用类型</span><span class="sxs-lookup"><span data-stu-id="d8fec-133">Reference types only</span></span>|<span data-ttu-id="d8fec-134">一个类型必须继承自或实现另一个类型</span><span class="sxs-lookup"><span data-stu-id="d8fec-134">One type must inherit from or implement the other type</span></span>|<span data-ttu-id="d8fec-135">不返回 [任何内容](../nothing.md)</span><span class="sxs-lookup"><span data-stu-id="d8fec-135">Returns [Nothing](../nothing.md)</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d8fec-136">示例</span><span class="sxs-lookup"><span data-stu-id="d8fec-136">Example</span></span>  

 <span data-ttu-id="d8fec-137">下面的示例说明如何使用 `TryCast`。</span><span class="sxs-lookup"><span data-stu-id="d8fec-137">The following example shows how to use `TryCast`.</span></span>  
  
 [!code-vb[VbVbalrKeywords#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="d8fec-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8fec-138">See also</span></span>

- [<span data-ttu-id="d8fec-139">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="d8fec-139">Widening and Narrowing Conversions</span></span>](../../programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="d8fec-140">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="d8fec-140">Implicit and Explicit Conversions</span></span>](../../programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)

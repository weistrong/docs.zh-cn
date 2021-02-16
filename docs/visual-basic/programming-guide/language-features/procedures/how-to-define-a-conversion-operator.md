---
description: '了解有关详细信息，请参阅如何：定义转换运算符 (Visual Basic) '
title: 如何：定义转换运算符
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
ms.openlocfilehash: c090e183e809974163625c4bfcf33536b1082b66
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481982"
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a><span data-ttu-id="c3dfa-103">如何：定义转换运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c3dfa-103">How to: Define a Conversion Operator (Visual Basic)</span></span>

<span data-ttu-id="c3dfa-104">如果已定义类或结构，则可以在类或结构的类型与另一种数据类型 (如 `Integer` 、或) 之间定义类型转换运算符 `Double` `String` 。</span><span class="sxs-lookup"><span data-stu-id="c3dfa-104">If you have defined a class or structure, you can define a type conversion operator between the type of your class or structure and another data type (such as `Integer`, `Double`, or `String`).</span></span>  
  
 <span data-ttu-id="c3dfa-105">将类型转换定义为类或结构中的 [CType 函数](../../../language-reference/functions/ctype-function.md) 过程。</span><span class="sxs-lookup"><span data-stu-id="c3dfa-105">Define the type conversion as a [CType Function](../../../language-reference/functions/ctype-function.md) procedure within the class or structure.</span></span> <span data-ttu-id="c3dfa-106">所有转换过程必须是 `Public Shared` ，并且每个转换过程必须指定 [扩大](../../../language-reference/modifiers/widening.md) 或 [收缩](../../../language-reference/modifiers/narrowing.md)。</span><span class="sxs-lookup"><span data-stu-id="c3dfa-106">All conversion procedures must be `Public Shared`, and each one must specify either [Widening](../../../language-reference/modifiers/widening.md) or [Narrowing](../../../language-reference/modifiers/narrowing.md).</span></span>  
  
 <span data-ttu-id="c3dfa-107">在类或结构上定义运算符也称为 *重载* 运算符。</span><span class="sxs-lookup"><span data-stu-id="c3dfa-107">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c3dfa-108">示例</span><span class="sxs-lookup"><span data-stu-id="c3dfa-108">Example</span></span>  

 <span data-ttu-id="c3dfa-109">下面的示例定义了名为和的结构之间的转换运算符 `digit` `Byte` 。</span><span class="sxs-lookup"><span data-stu-id="c3dfa-109">The following example defines conversion operators between a structure called `digit` and a `Byte`.</span></span>  
  
 [!code-vb[VbVbcnProcedures#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#27)]  
  
 <span data-ttu-id="c3dfa-110">可以 `digit` 通过以下代码测试结构。</span><span class="sxs-lookup"><span data-stu-id="c3dfa-110">You can test the structure `digit` with the following code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#28)]  
  
## <a name="see-also"></a><span data-ttu-id="c3dfa-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="c3dfa-111">See also</span></span>

- [<span data-ttu-id="c3dfa-112">运算符过程</span><span class="sxs-lookup"><span data-stu-id="c3dfa-112">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="c3dfa-113">如何：定义运算符</span><span class="sxs-lookup"><span data-stu-id="c3dfa-113">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)
- [<span data-ttu-id="c3dfa-114">如何：调用运算符过程</span><span class="sxs-lookup"><span data-stu-id="c3dfa-114">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)
- [<span data-ttu-id="c3dfa-115">如何：使用定义运算符的类</span><span class="sxs-lookup"><span data-stu-id="c3dfa-115">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)
- [<span data-ttu-id="c3dfa-116">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="c3dfa-116">Operator Statement</span></span>](../../../language-reference/statements/operator-statement.md)
- [<span data-ttu-id="c3dfa-117">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="c3dfa-117">Structure Statement</span></span>](../../../language-reference/statements/structure-statement.md)
- [<span data-ttu-id="c3dfa-118">如何：声明结构</span><span class="sxs-lookup"><span data-stu-id="c3dfa-118">How to: Declare a Structure</span></span>](../data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="c3dfa-119">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="c3dfa-119">Implicit and Explicit Conversions</span></span>](../data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="c3dfa-120">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="c3dfa-120">Widening and Narrowing Conversions</span></span>](../data-types/widening-and-narrowing-conversions.md)

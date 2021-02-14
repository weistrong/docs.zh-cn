---
description: '了解有关详细信息，请参阅如何：定义操作员 (Visual Basic) '
title: 如何：定义运算符
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- Visual Basic code, operators
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- operator procedures [Visual Basic], about operator procedures
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: d4b0e253-092a-4e6e-9fe2-01f562140a29
ms.openlocfilehash: ead96a302426c6f5b1667bb030aab56afe3284c8
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100462706"
---
# <a name="how-to-define-an-operator-visual-basic"></a><span data-ttu-id="d98f3-103">如何：定义运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d98f3-103">How to: Define an Operator (Visual Basic)</span></span>

<span data-ttu-id="d98f3-104">如果已定义类或结构，则可在 `*` `<>` `And` 一个或两个操作数为类或结构的类型时定义标准运算符 (如、或) 的行为。</span><span class="sxs-lookup"><span data-stu-id="d98f3-104">If you have defined a class or structure, you can define the behavior of a standard operator (such as `*`, `<>`, or `And`) when one or both of the operands is of the type of your class or structure.</span></span>  
  
 <span data-ttu-id="d98f3-105">将标准运算符定义为类或结构中的运算符过程。</span><span class="sxs-lookup"><span data-stu-id="d98f3-105">Define the standard operator as an operator procedure within the class or structure.</span></span> <span data-ttu-id="d98f3-106">所有运算符过程必须是 `Public` `Shared` 。</span><span class="sxs-lookup"><span data-stu-id="d98f3-106">All operator procedures must be `Public` `Shared`.</span></span>  
  
 <span data-ttu-id="d98f3-107">在类或结构上定义运算符也称为 *重载* 运算符。</span><span class="sxs-lookup"><span data-stu-id="d98f3-107">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d98f3-108">示例</span><span class="sxs-lookup"><span data-stu-id="d98f3-108">Example</span></span>  

 <span data-ttu-id="d98f3-109">下面的示例 `+` 为一个名为的结构定义运算符 `height` 。</span><span class="sxs-lookup"><span data-stu-id="d98f3-109">The following example defines the `+` operator for a structure called `height`.</span></span> <span data-ttu-id="d98f3-110">结构使用以英尺和英寸为单位的高度。</span><span class="sxs-lookup"><span data-stu-id="d98f3-110">The structure uses heights measured in feet and inches.</span></span> <span data-ttu-id="d98f3-111">一 *英寸* 为2.54 厘米，1 *英尺* 为12英寸。</span><span class="sxs-lookup"><span data-stu-id="d98f3-111">One *inch* is 2.54 centimeters, and one *foot* is 12 inches.</span></span> <span data-ttu-id="d98f3-112">若要确保标准化的值 (英寸 < 12.0) ，则构造函数执行第 12 *模* 运算。</span><span class="sxs-lookup"><span data-stu-id="d98f3-112">To ensure normalized values (inches < 12.0), the constructor performs *modulo* 12 arithmetic.</span></span> <span data-ttu-id="d98f3-113">`+`运算符使用构造函数生成规范化值。</span><span class="sxs-lookup"><span data-stu-id="d98f3-113">The `+` operator uses the constructor to generate normalized values.</span></span>  
  
 [!code-vb[VbVbcnProcedures#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#25)]  
  
 <span data-ttu-id="d98f3-114">可以 `height` 通过以下代码测试结构。</span><span class="sxs-lookup"><span data-stu-id="d98f3-114">You can test the structure `height` with the following code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#26)]  

## <a name="see-also"></a><span data-ttu-id="d98f3-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d98f3-115">See also</span></span>

- [<span data-ttu-id="d98f3-116">运算符过程</span><span class="sxs-lookup"><span data-stu-id="d98f3-116">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="d98f3-117">如何：定义转换运算符</span><span class="sxs-lookup"><span data-stu-id="d98f3-117">How to: Define a Conversion Operator</span></span>](./how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="d98f3-118">如何：调用运算符过程</span><span class="sxs-lookup"><span data-stu-id="d98f3-118">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)
- [<span data-ttu-id="d98f3-119">如何：使用定义运算符的类</span><span class="sxs-lookup"><span data-stu-id="d98f3-119">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)
- [<span data-ttu-id="d98f3-120">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="d98f3-120">Operator Statement</span></span>](../../../language-reference/statements/operator-statement.md)
- [<span data-ttu-id="d98f3-121">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="d98f3-121">Structure Statement</span></span>](../../../language-reference/statements/structure-statement.md)
- [<span data-ttu-id="d98f3-122">如何：声明结构</span><span class="sxs-lookup"><span data-stu-id="d98f3-122">How to: Declare a Structure</span></span>](../data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="d98f3-123">Mod 运算符</span><span class="sxs-lookup"><span data-stu-id="d98f3-123">Mod Operator</span></span>](../../../language-reference/operators/mod-operator.md)

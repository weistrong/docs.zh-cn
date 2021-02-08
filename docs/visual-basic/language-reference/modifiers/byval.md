---
description: '详细了解： ByVal (Visual Basic) '
title: ByVal
ms.date: 07/20/2015
f1_keywords:
- vb.ByVal
- ByVal
helpviewer_keywords:
- ByVal keyword [Visual Basic], contexts
- ByVal keyword [Visual Basic]
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
ms.openlocfilehash: cd7116c0bcc3d263cc2bb6a9b95e46e8ff0cc116
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774611"
---
# <a name="byval-visual-basic"></a><span data-ttu-id="8323e-103">ByVal (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8323e-103">ByVal (Visual Basic)</span></span>

<span data-ttu-id="8323e-104">指定参数 [按值](../../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)传递，因此被调用的过程或属性无法更改调用代码中参数的基础变量的值。</span><span class="sxs-lookup"><span data-stu-id="8323e-104">Specifies that an argument is passed [by value](../../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md), so that the called procedure or property cannot change the value of a variable underlying the argument in the calling code.</span></span> <span data-ttu-id="8323e-105">如果未指定修饰符，则 ByVal 为默认值。</span><span class="sxs-lookup"><span data-stu-id="8323e-105">If no modifier is specified, ByVal is the default.</span></span>

> [!NOTE]
> <span data-ttu-id="8323e-106">由于它是默认值，因此不必 `ByVal` 在方法签名中显式指定关键字。</span><span class="sxs-lookup"><span data-stu-id="8323e-106">Because it is the default, you do not have to explicitly specify the `ByVal` keyword in method signatures.</span></span> <span data-ttu-id="8323e-107">它往往会产生干扰代码，并经常导致非默认 `ByRef` 关键字被忽略。</span><span class="sxs-lookup"><span data-stu-id="8323e-107">It tends to produce noisy code and often leads to the non-default `ByRef` keyword being overlooked.</span></span>

## <a name="remarks"></a><span data-ttu-id="8323e-108">备注</span><span class="sxs-lookup"><span data-stu-id="8323e-108">Remarks</span></span>

 <span data-ttu-id="8323e-109">`ByVal` 修饰符可用于下面的上下文中：</span><span class="sxs-lookup"><span data-stu-id="8323e-109">The `ByVal` modifier can be used in these contexts:</span></span>

 [<span data-ttu-id="8323e-110">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="8323e-110">Declare Statement</span></span>](../statements/declare-statement.md)

 [<span data-ttu-id="8323e-111">Function 语句</span><span class="sxs-lookup"><span data-stu-id="8323e-111">Function Statement</span></span>](../statements/function-statement.md)
  
 [<span data-ttu-id="8323e-112">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="8323e-112">Operator Statement</span></span>](../statements/operator-statement.md)
  
 [<span data-ttu-id="8323e-113">Property Statement</span><span class="sxs-lookup"><span data-stu-id="8323e-113">Property Statement</span></span>](../statements/property-statement.md)
  
 [<span data-ttu-id="8323e-114">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="8323e-114">Sub Statement</span></span>](../statements/sub-statement.md)

## <a name="example"></a><span data-ttu-id="8323e-115">示例</span><span class="sxs-lookup"><span data-stu-id="8323e-115">Example</span></span>

 <span data-ttu-id="8323e-116">下面的示例演示如何将 `ByVal` 参数传递机制与引用类型参数一起使用。</span><span class="sxs-lookup"><span data-stu-id="8323e-116">The following example demonstrates the use of the `ByVal` parameter passing mechanism with a reference type argument.</span></span> <span data-ttu-id="8323e-117">在此示例中，自变量是 `c1` 类的实例 `Class1` 。</span><span class="sxs-lookup"><span data-stu-id="8323e-117">In the example, the argument is `c1`, an instance of class `Class1`.</span></span> <span data-ttu-id="8323e-118">`ByVal` 阻止过程中的代码更改 reference 参数的基础值，但不保护的 `c1` 可访问字段和属性 `c1` 。</span><span class="sxs-lookup"><span data-stu-id="8323e-118">`ByVal` prevents the code in the procedures from changing the underlying value of the reference argument, `c1`, but does not protect the accessible fields and properties of `c1`.</span></span>

 [!code-vb[VbVbalrKeywords#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class5.vb#10)]

## <a name="see-also"></a><span data-ttu-id="8323e-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8323e-119">See also</span></span>

- [<span data-ttu-id="8323e-120">关键字</span><span class="sxs-lookup"><span data-stu-id="8323e-120">Keywords</span></span>](../keywords/index.md)
- [<span data-ttu-id="8323e-121">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="8323e-121">Passing Arguments by Value and by Reference</span></span>](../../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)

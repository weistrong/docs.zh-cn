---
description: '详细了解： Call 语句 (Visual Basic) '
title: Call 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Call
helpviewer_keywords:
- procedures [Visual Basic], Call statement
- Call statement [Visual Basic]
- procedures [Visual Basic], calling
ms.assetid: e5b31571-6867-406f-b8e7-a3f9aae4723a
ms.openlocfilehash: 70e6c109621c3710ad9476a952e9c384a142ba3d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674007"
---
# <a name="call-statement-visual-basic"></a><span data-ttu-id="5390e-103">Call 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5390e-103">Call Statement (Visual Basic)</span></span>

<span data-ttu-id="5390e-104">将控制转移到 `Function` 、 `Sub` 或动态链接库 (DLL) 过程。</span><span class="sxs-lookup"><span data-stu-id="5390e-104">Transfers control to a `Function`, `Sub`, or dynamic-link library (DLL) procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5390e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5390e-105">Syntax</span></span>  
  
```vb  
[ Call ] procedureName [ (argumentList) ]  
```  
  
## <a name="parts"></a><span data-ttu-id="5390e-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="5390e-106">Parts</span></span>  

|||
|---|---|
|`procedureName`|<span data-ttu-id="5390e-107">必需。</span><span class="sxs-lookup"><span data-stu-id="5390e-107">Required.</span></span> <span data-ttu-id="5390e-108">要调用的过程的名称。</span><span class="sxs-lookup"><span data-stu-id="5390e-108">Name of the procedure to call.</span></span>|
|`argumentList`|<span data-ttu-id="5390e-109">可选。</span><span class="sxs-lookup"><span data-stu-id="5390e-109">Optional.</span></span> <span data-ttu-id="5390e-110">表示在调用过程时传递给过程的参数的变量或表达式列表。</span><span class="sxs-lookup"><span data-stu-id="5390e-110">List of variables or expressions representing arguments that are passed to the procedure when it is called.</span></span> <span data-ttu-id="5390e-111">多个参数之间用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="5390e-111">Multiple arguments are separated by commas.</span></span> <span data-ttu-id="5390e-112">如果包含 `argumentList` ，则必须将其括在括号中。</span><span class="sxs-lookup"><span data-stu-id="5390e-112">If you include `argumentList`, you must enclose it in parentheses.</span></span>|
|||
  
## <a name="remarks"></a><span data-ttu-id="5390e-113">备注</span><span class="sxs-lookup"><span data-stu-id="5390e-113">Remarks</span></span>

 <span data-ttu-id="5390e-114">`Call`您可以在调用过程时使用关键字。</span><span class="sxs-lookup"><span data-stu-id="5390e-114">You can use the `Call` keyword when you call a procedure.</span></span> <span data-ttu-id="5390e-115">对于大多数过程调用，不需要使用此关键字。</span><span class="sxs-lookup"><span data-stu-id="5390e-115">For most procedure calls, you aren’t required to use this  keyword.</span></span>

 <span data-ttu-id="5390e-116">`Call`当被调用的表达式不是以标识符开头时，通常使用关键字。</span><span class="sxs-lookup"><span data-stu-id="5390e-116">You typically use the `Call` keyword when the called expression doesn’t start with an identifier.</span></span> <span data-ttu-id="5390e-117">`Call`不建议对其他用法使用关键字。</span><span class="sxs-lookup"><span data-stu-id="5390e-117">Use of the `Call` keyword for other uses isn't recommended.</span></span>

 <span data-ttu-id="5390e-118">如果过程返回值，则 `Call` 语句会将其丢弃。</span><span class="sxs-lookup"><span data-stu-id="5390e-118">If the procedure returns a value, the `Call` statement discards it.</span></span>

## <a name="example"></a><span data-ttu-id="5390e-119">示例</span><span class="sxs-lookup"><span data-stu-id="5390e-119">Example</span></span>

 <span data-ttu-id="5390e-120">下面的代码演示了两个示例，其中， `Call` 关键字是调用过程所必需的。</span><span class="sxs-lookup"><span data-stu-id="5390e-120">The following code shows two examples where the `Call` keyword is necessary to call a procedure.</span></span> <span data-ttu-id="5390e-121">在这两个示例中，调用的表达式不以标识符开头。</span><span class="sxs-lookup"><span data-stu-id="5390e-121">In both examples, the called expression doesn't start with an identifier.</span></span>

 [!code-vb[VbVbalrStatements#97](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#97)]  
  
## <a name="see-also"></a><span data-ttu-id="5390e-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="5390e-122">See also</span></span>

- [<span data-ttu-id="5390e-123">Function 语句</span><span class="sxs-lookup"><span data-stu-id="5390e-123">Function Statement</span></span>](function-statement.md)
- [<span data-ttu-id="5390e-124">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="5390e-124">Sub Statement</span></span>](sub-statement.md)
- [<span data-ttu-id="5390e-125">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="5390e-125">Declare Statement</span></span>](declare-statement.md)
- [<span data-ttu-id="5390e-126">Lambda 表达式</span><span class="sxs-lookup"><span data-stu-id="5390e-126">Lambda Expressions</span></span>](../../programming-guide/language-features/procedures/lambda-expressions.md)

---
description: '了解详细信息： AddressOf Operator (Visual Basic) '
title: AddressOf 运算符
ms.date: 07/20/2015
f1_keywords:
- AddressOf
- vb.AddressOf
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- addresses, passing to API procedures
ms.assetid: 8105a59d-60d8-4ab5-b221-5899cdfacbf4
ms.openlocfilehash: 2aba8c26aa9581fe1070574b8c408e09bf063d1f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774377"
---
# <a name="addressof-operator-visual-basic"></a><span data-ttu-id="892f6-103">AddressOf 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="892f6-103">AddressOf Operator (Visual Basic)</span></span>

<span data-ttu-id="892f6-104">创建引用特定过程的委托实例。</span><span class="sxs-lookup"><span data-stu-id="892f6-104">Creates a delegate instance that references the specific procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="892f6-105">语法</span><span class="sxs-lookup"><span data-stu-id="892f6-105">Syntax</span></span>  
  
```vb  
AddressOf procedurename  
```  
  
## <a name="parts"></a><span data-ttu-id="892f6-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="892f6-106">Parts</span></span>  

 `procedurename`  
 <span data-ttu-id="892f6-107">必需。</span><span class="sxs-lookup"><span data-stu-id="892f6-107">Required.</span></span> <span data-ttu-id="892f6-108">指定新创建的委托所引用的过程。</span><span class="sxs-lookup"><span data-stu-id="892f6-108">Specifies the procedure to be referenced by the newly created delegate.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="892f6-109">备注</span><span class="sxs-lookup"><span data-stu-id="892f6-109">Remarks</span></span>  

 <span data-ttu-id="892f6-110">`AddressOf`运算符创建指向由指定的 sub 或函数的委托 `procedurename` 。</span><span class="sxs-lookup"><span data-stu-id="892f6-110">The `AddressOf` operator creates a delegate that points to the sub or function specified by `procedurename`.</span></span> <span data-ttu-id="892f6-111">如果指定的过程是实例方法，则委托同时引用实例和方法。</span><span class="sxs-lookup"><span data-stu-id="892f6-111">When the specified procedure is an instance method then the delegate refers to both the instance and the method.</span></span> <span data-ttu-id="892f6-112">然后，在调用委托时，将调用指定实例的指定方法。</span><span class="sxs-lookup"><span data-stu-id="892f6-112">Then, when the  delegate is invoked the specified method of the specified instance is called.</span></span>  
  
 <span data-ttu-id="892f6-113">`AddressOf`运算符可用作委托构造函数的操作数，或可用于可由编译器确定委托的类型的上下文中。</span><span class="sxs-lookup"><span data-stu-id="892f6-113">The `AddressOf` operator can be used as the operand of a delegate constructor or it can be used in a context in which the type of the delegate can be determined by the compiler.</span></span>  
  
## <a name="example"></a><span data-ttu-id="892f6-114">示例</span><span class="sxs-lookup"><span data-stu-id="892f6-114">Example</span></span>  

 <span data-ttu-id="892f6-115">此示例使用 `AddressOf` 运算符来指定用于处理 `Click` 按钮事件的委托。</span><span class="sxs-lookup"><span data-stu-id="892f6-115">This example uses the `AddressOf` operator to designate a delegate to handle the `Click` event of a button.</span></span>  
  
 [!code-vb[VbVbalrDelegates#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#8)]  
  
## <a name="example"></a><span data-ttu-id="892f6-116">示例</span><span class="sxs-lookup"><span data-stu-id="892f6-116">Example</span></span>  

 <span data-ttu-id="892f6-117">下面的示例使用 `AddressOf` 运算符来指定线程的启动函数。</span><span class="sxs-lookup"><span data-stu-id="892f6-117">The following example uses the `AddressOf` operator to designate the startup function for a thread.</span></span>  
  
 [!code-vb[VbVbalrDelegates#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#9)]  
  
## <a name="see-also"></a><span data-ttu-id="892f6-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="892f6-118">See also</span></span>

- [<span data-ttu-id="892f6-119">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="892f6-119">Declare Statement</span></span>](../statements/declare-statement.md)
- [<span data-ttu-id="892f6-120">Function 语句</span><span class="sxs-lookup"><span data-stu-id="892f6-120">Function Statement</span></span>](../statements/function-statement.md)
- [<span data-ttu-id="892f6-121">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="892f6-121">Sub Statement</span></span>](../statements/sub-statement.md)
- [<span data-ttu-id="892f6-122">委托</span><span class="sxs-lookup"><span data-stu-id="892f6-122">Delegates</span></span>](../../programming-guide/language-features/delegates/index.md)

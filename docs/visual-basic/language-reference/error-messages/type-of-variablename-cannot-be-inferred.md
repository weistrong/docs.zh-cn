---
description: 了解有关以下内容的详细信息： BC30982： <variablename> 无法推断 "" 的类型，因为循环边界和步骤变量未扩大到同一类型
title: 无法推断“<variablename>”的类型，因为循环边界和步骤变量未扩大到同一类型
ms.date: 07/20/2015
f1_keywords:
- bc30982
- vbc30982
helpviewer_keywords:
- BC30982
ms.assetid: 741e85d9-a747-42ad-a1e1-a3f1928aaff5
ms.openlocfilehash: 399e021500813127df6ecede2534783df09ac8dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641156"
---
# <a name="bc30982-type-of-variablename-cannot-be-inferred-because-the-loop-bounds-and-the-step-variable-do-not-widen-to-the-same-type"></a><span data-ttu-id="4fd3c-103">BC30982：无法推断 "" 的类型， \<variablename> 因为循环边界和步骤变量未扩大到同一类型</span><span class="sxs-lookup"><span data-stu-id="4fd3c-103">BC30982: Type of '\<variablename>' cannot be inferred because the loop bounds and the step variable do not widen to the same type</span></span>

<span data-ttu-id="4fd3c-104">你编写了一个 `For...Next` 循环，该循环中编译器无法推断循环控制变量的数据类型，因为满足以下条件：</span><span class="sxs-lookup"><span data-stu-id="4fd3c-104">You have written a `For...Next` loop in which the compiler cannot infer a data type for the loop control variable because the following conditions are true:</span></span>

- <span data-ttu-id="4fd3c-105">未在 `As` 子句中指定循环控制变量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-105">The data type of the loop control variable is not specified with an `As` clause.</span></span>

- <span data-ttu-id="4fd3c-106">循环边界和步骤变量包含至少两种数据类型。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-106">The loop bounds and step variable contain at least two data types.</span></span>

- <span data-ttu-id="4fd3c-107">数据类型之间不存在标准转换。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-107">No standard conversions exist between the data types.</span></span>

 <span data-ttu-id="4fd3c-108">因此，编译器无法推断循环控制变量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-108">Therefore, the compiler cannot infer the data type of a loop's control variable.</span></span>

 <span data-ttu-id="4fd3c-109">在下面的示例中，步骤变量是一个字符，并且循环边界都是整数。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-109">In the following example, the step variable is a character and the loop bounds are both integers.</span></span> <span data-ttu-id="4fd3c-110">由于字符和整数之间没有标准转换，因此将报告此错误。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-110">Because there is no standard conversion between characters and integers, this error is reported.</span></span>

```vb
Dim stepVar = "1"c
Dim m = 0
Dim n = 20

' Not valid.
' For i = 1 To 10 Step stepVar
    ' Loop processing
' Next
```

<span data-ttu-id="4fd3c-111">**错误 ID：** BC30982</span><span class="sxs-lookup"><span data-stu-id="4fd3c-111">**Error ID:** BC30982</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4fd3c-112">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4fd3c-112">To correct this error</span></span>

- <span data-ttu-id="4fd3c-113">根据需要更改循环边界和步骤变量的类型，以使其中至少有一个类型为其他类型。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-113">Change the types of the loop bounds and step variable as necessary so that at least one of them is a type that the others widen to.</span></span> <span data-ttu-id="4fd3c-114">在前面的示例中，将的类型更改 `stepVar` 为 `Integer` 。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-114">In the preceding example, change the type of `stepVar` to `Integer`.</span></span>

  ```vb
  Dim stepVar = 1
  ```

  <span data-ttu-id="4fd3c-115">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="4fd3c-115">-or-</span></span>

  ```vb
  Dim stepVar As Integer = 1
  ```

- <span data-ttu-id="4fd3c-116">使用显式转换函数将循环边界和步骤变量转换为适当的类型。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-116">Use explicit conversion functions to convert the loop bounds and step variable to the appropriate types.</span></span> <span data-ttu-id="4fd3c-117">在前面的示例中，将 `Val` 函数应用于 `stepVar` 。</span><span class="sxs-lookup"><span data-stu-id="4fd3c-117">In the preceding example, apply the `Val` function to `stepVar`.</span></span>

  ```vb
  For i = 1 To 10 Step Val(stepVar)
      ' Loop processing
  Next
  ```

## <a name="see-also"></a><span data-ttu-id="4fd3c-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="4fd3c-118">See also</span></span>

- <xref:Microsoft.VisualBasic.Conversion.Val%2A>
- [<span data-ttu-id="4fd3c-119">For...Next 语句</span><span class="sxs-lookup"><span data-stu-id="4fd3c-119">For...Next Statement</span></span>](../statements/for-next-statement.md)
- [<span data-ttu-id="4fd3c-120">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="4fd3c-120">Implicit and Explicit Conversions</span></span>](../../programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="4fd3c-121">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="4fd3c-121">Local Type Inference</span></span>](../../programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="4fd3c-122">Option Infer 语句</span><span class="sxs-lookup"><span data-stu-id="4fd3c-122">Option Infer Statement</span></span>](../statements/option-infer-statement.md)
- [<span data-ttu-id="4fd3c-123">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="4fd3c-123">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="4fd3c-124">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="4fd3c-124">Widening and Narrowing Conversions</span></span>](../../programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)

---
description: 了解更多相关信息： BC30020： "Is" 需要具有引用类型的操作数，但此操作数的值类型为 " <typename> "
title: “Is”要求具有引用类型的操作数，但此操作数的值类型为“<typename>”。
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: f05040c6174f4b1edd006d1302f0d94b871d1cd9
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100427539"
---
# <a name="bc30020-is-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-typename"></a><span data-ttu-id="caeb2-103">BC30020： "Is" 需要具有引用类型的操作数，但此操作数的值类型为 " \<typename> "</span><span class="sxs-lookup"><span data-stu-id="caeb2-103">BC30020: 'Is' requires operands that have reference types, but this operand has the value type '\<typename>'</span></span>

<span data-ttu-id="caeb2-104">`Is`比较运算符确定两个对象变量是否引用相同的实例。</span><span class="sxs-lookup"><span data-stu-id="caeb2-104">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="caeb2-105">没有为值类型定义此比较。</span><span class="sxs-lookup"><span data-stu-id="caeb2-105">This comparison is not defined for value types.</span></span>

 <span data-ttu-id="caeb2-106">**错误 ID：** BC30020</span><span class="sxs-lookup"><span data-stu-id="caeb2-106">**Error ID:** BC30020</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="caeb2-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="caeb2-107">To correct this error</span></span>

- <span data-ttu-id="caeb2-108">使用适当的算术比较运算符或 `Like` 运算符比较两个值类型。</span><span class="sxs-lookup"><span data-stu-id="caeb2-108">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>

## <a name="see-also"></a><span data-ttu-id="caeb2-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="caeb2-109">See also</span></span>

- [<span data-ttu-id="caeb2-110">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="caeb2-110">Is Operator</span></span>](../operators/is-operator.md)
- [<span data-ttu-id="caeb2-111">Like 运算符</span><span class="sxs-lookup"><span data-stu-id="caeb2-111">Like Operator</span></span>](../operators/like-operator.md)
- [<span data-ttu-id="caeb2-112">比较运算符</span><span class="sxs-lookup"><span data-stu-id="caeb2-112">Comparison Operators</span></span>](../operators/comparison-operators.md)

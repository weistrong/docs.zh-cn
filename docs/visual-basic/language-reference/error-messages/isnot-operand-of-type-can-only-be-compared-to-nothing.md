---
description: 了解有关以下内容的详细信息： BC32128：类型 "typename" 的 "IsNot" 操作数只能与 "Nothing" 比较，因为 "typename" 是一个可以为 null 的类型
title: 类型“typename”的操作数“IsNot”只能与“Nothing”比较，因为“typename”是一个可以为 null 的类型
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: 732c8bee2ae352824c7d50bba8b2b35598d6f53b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795984"
---
# <a name="bc32128-isnot-operand-of-type-typename-can-only-be-compared-to-nothing-because-typename-is-a-nullable-type"></a><span data-ttu-id="cdb8c-103">BC32128：类型 "typename" 的 "IsNot" 操作数只能与 "Nothing" 比较，因为 "typename" 是一个可以为 null 的类型</span><span class="sxs-lookup"><span data-stu-id="cdb8c-103">BC32128: 'IsNot' operand of type 'typename' can only be compared to 'Nothing', because 'typename' is a nullable type</span></span>

<span data-ttu-id="cdb8c-104">已将声明为可以为 null 的值类型的变量与使用运算符之外的表达式进行比较 `Nothing` `IsNot` 。</span><span class="sxs-lookup"><span data-stu-id="cdb8c-104">A variable declared as a nullable value type has been compared to an expression other than `Nothing` using the `IsNot` operator.</span></span>

<span data-ttu-id="cdb8c-105">**错误 ID：** BC32128</span><span class="sxs-lookup"><span data-stu-id="cdb8c-105">**Error ID:** BC32128</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="cdb8c-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="cdb8c-106">To correct this error</span></span>

<span data-ttu-id="cdb8c-107">要将可以为 null 的类型和表达式进行比较（而不是使用 `Nothing` 运算符比较 `IsNot` ），请调用可以为 null 的类型中的 `GetType` 方法并将结果与表达式进行比较，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="cdb8c-107">To compare a nullable type to an expression other than `Nothing` by using the `IsNot` operator, call the `GetType` method on the nullable type and compare the result to the expression, as shown in the following example.</span></span>

```vb
Dim number? As Integer = 5

If number IsNot Nothing Then
  If number.GetType() IsNot Type.GetType("System.Int32") Then

  End If
End If
```

## <a name="see-also"></a><span data-ttu-id="cdb8c-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="cdb8c-108">See also</span></span>

- [<span data-ttu-id="cdb8c-109">可以为 null 的值类型</span><span class="sxs-lookup"><span data-stu-id="cdb8c-109">Nullable Value Types</span></span>](../../programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="cdb8c-110">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="cdb8c-110">IsNot Operator</span></span>](../operators/isnot-operator.md)

---
description: '了解详细信息： Is operator (Visual Basic) '
title: Is 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.is
helpviewer_keywords:
- comparison operators [Visual Basic]
- equivalent objects
- TypeOf...Is expression
- Is operator [Visual Basic]
ms.assetid: 8045a6c8-2a83-45b6-ad47-d09a704c656d
ms.openlocfilehash: 0912ebd9bc9c33149568c6cea0197ef24c305ff2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665679"
---
# <a name="is-operator-visual-basic"></a><span data-ttu-id="395bb-103">Is 运算符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="395bb-103">Is operator (Visual Basic)</span></span>

<span data-ttu-id="395bb-104">比较两个对象引用变量。</span><span class="sxs-lookup"><span data-stu-id="395bb-104">Compares two object reference variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="395bb-105">语法</span><span class="sxs-lookup"><span data-stu-id="395bb-105">Syntax</span></span>

```vb
result = object1 Is object2
```

## <a name="parts"></a><span data-ttu-id="395bb-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="395bb-106">Parts</span></span>

 `result`  
 <span data-ttu-id="395bb-107">必需。</span><span class="sxs-lookup"><span data-stu-id="395bb-107">Required.</span></span> <span data-ttu-id="395bb-108">任何 `Boolean` 值。</span><span class="sxs-lookup"><span data-stu-id="395bb-108">Any `Boolean` value.</span></span>  
  
 `object1`  
 <span data-ttu-id="395bb-109">必需。</span><span class="sxs-lookup"><span data-stu-id="395bb-109">Required.</span></span> <span data-ttu-id="395bb-110">任意 `Object` 名称。</span><span class="sxs-lookup"><span data-stu-id="395bb-110">Any `Object` name.</span></span>  
  
 `object2`  
 <span data-ttu-id="395bb-111">必需。</span><span class="sxs-lookup"><span data-stu-id="395bb-111">Required.</span></span> <span data-ttu-id="395bb-112">任意 `Object` 名称。</span><span class="sxs-lookup"><span data-stu-id="395bb-112">Any `Object` name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="395bb-113">备注</span><span class="sxs-lookup"><span data-stu-id="395bb-113">Remarks</span></span>

<span data-ttu-id="395bb-114">`Is`运算符确定两个对象引用是否引用同一对象。</span><span class="sxs-lookup"><span data-stu-id="395bb-114">The `Is` operator determines if two object references refer to the same object.</span></span> <span data-ttu-id="395bb-115">但是，它不会执行值比较。</span><span class="sxs-lookup"><span data-stu-id="395bb-115">However, it does not perform value comparisons.</span></span> <span data-ttu-id="395bb-116">如果 `object1` 和 `object2` 都引用完全相同的对象实例，则 `result` 为 `True` ; 如果不是，则为; 如果不是，则 `result` 为 `False` 。</span><span class="sxs-lookup"><span data-stu-id="395bb-116">If `object1` and `object2` both refer to the exact same object instance, `result` is `True`; if they do not, `result` is `False`.</span></span>

> [!NOTE]
> <span data-ttu-id="395bb-117">`Is`关键字还用于[Select .。。Case 语句](../statements/select-case-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="395bb-117">The `Is` keyword is also used in the [Select...Case Statement](../statements/select-case-statement.md).</span></span>
  
## <a name="example"></a><span data-ttu-id="395bb-118">示例</span><span class="sxs-lookup"><span data-stu-id="395bb-118">Example</span></span>

<span data-ttu-id="395bb-119">下面的示例使用 `Is` 运算符比较对象引用对。</span><span class="sxs-lookup"><span data-stu-id="395bb-119">The following example uses the `Is` operator to compare pairs of object references.</span></span> <span data-ttu-id="395bb-120">将结果分配给一个 `Boolean` 值，该值表示两个对象是否相同。</span><span class="sxs-lookup"><span data-stu-id="395bb-120">The results are assigned to a `Boolean` value representing whether the two objects are identical.</span></span>

[!code-vb[VbVbalrOperators#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#27)]

<span data-ttu-id="395bb-121">如前面的示例所示，可以使用 `Is` 运算符来测试早期绑定和晚期绑定对象。</span><span class="sxs-lookup"><span data-stu-id="395bb-121">As the preceding example demonstrates, you can use the `Is` operator to test both early bound and late bound objects.</span></span>

## <a name="use-typeof-operator-with-is-operator"></a><span data-ttu-id="395bb-122">对 Is 运算符使用 TypeOf 运算符</span><span class="sxs-lookup"><span data-stu-id="395bb-122">Use TypeOf operator with Is operator</span></span>

<span data-ttu-id="395bb-123">`Is` 运算符还可与关键字一起使用 `TypeOf` ，以生成 `TypeOf` ... `Is` 表达式，该表达式测试对象变量是否与数据类型兼容。</span><span class="sxs-lookup"><span data-stu-id="395bb-123">`Is` operator can also be used with the `TypeOf` keyword to make a `TypeOf`...`Is` expression, which tests whether an object variable is compatible with a data type.</span></span> <span data-ttu-id="395bb-124">例如：</span><span class="sxs-lookup"><span data-stu-id="395bb-124">For example:</span></span>

```vb
If TypeOf sender Is Button Then
```

## <a name="see-also"></a><span data-ttu-id="395bb-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="395bb-125">See also</span></span>

- [<span data-ttu-id="395bb-126">TypeOf 运算符</span><span class="sxs-lookup"><span data-stu-id="395bb-126">TypeOf Operator</span></span>](typeof-operator.md)
- [<span data-ttu-id="395bb-127">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="395bb-127">IsNot Operator</span></span>](isnot-operator.md)
- [<span data-ttu-id="395bb-128">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="395bb-128">Comparison Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [<span data-ttu-id="395bb-129">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="395bb-129">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="395bb-130">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="395bb-130">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="395bb-131">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="395bb-131">Operators and Expressions</span></span>](../../programming-guide/language-features/operators-and-expressions/index.md)

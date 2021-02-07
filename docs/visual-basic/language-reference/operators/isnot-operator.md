---
description: '了解详细信息： IsNot Operator (Visual Basic) '
title: IsNot 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.isnot
helpviewer_keywords:
- comparison operators [Visual Basic]
- TypeOf...IsNot expression
- IsNot operator [Visual Basic]
ms.assetid: 8dd2bcdb-0166-48a2-9094-60dfb448f36c
ms.openlocfilehash: ac3e127676dfa57d14e07838152022de62fc336b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665661"
---
# <a name="isnot-operator-visual-basic"></a><span data-ttu-id="270bc-103">IsNot 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="270bc-103">IsNot Operator (Visual Basic)</span></span>

<span data-ttu-id="270bc-104">比较两个对象引用变量。</span><span class="sxs-lookup"><span data-stu-id="270bc-104">Compares two object reference variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="270bc-105">语法</span><span class="sxs-lookup"><span data-stu-id="270bc-105">Syntax</span></span>

```vb
result = object1 IsNot object2
```

## <a name="parts"></a><span data-ttu-id="270bc-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="270bc-106">Parts</span></span>

- `result`

  <span data-ttu-id="270bc-107">必需。</span><span class="sxs-lookup"><span data-stu-id="270bc-107">Required.</span></span> <span data-ttu-id="270bc-108">一个 `Boolean` 值。</span><span class="sxs-lookup"><span data-stu-id="270bc-108">A `Boolean` value.</span></span>

- `object1`

  <span data-ttu-id="270bc-109">必需。</span><span class="sxs-lookup"><span data-stu-id="270bc-109">Required.</span></span> <span data-ttu-id="270bc-110">任何 `Object` 变量或表达式。</span><span class="sxs-lookup"><span data-stu-id="270bc-110">Any `Object` variable or expression.</span></span>

- `object2`

  <span data-ttu-id="270bc-111">必需。</span><span class="sxs-lookup"><span data-stu-id="270bc-111">Required.</span></span> <span data-ttu-id="270bc-112">任何 `Object` 变量或表达式。</span><span class="sxs-lookup"><span data-stu-id="270bc-112">Any `Object` variable or expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="270bc-113">备注</span><span class="sxs-lookup"><span data-stu-id="270bc-113">Remarks</span></span>

<span data-ttu-id="270bc-114">`IsNot`运算符确定两个对象引用是否引用不同的对象。</span><span class="sxs-lookup"><span data-stu-id="270bc-114">The `IsNot` operator determines if two object references refer to different objects.</span></span> <span data-ttu-id="270bc-115">但是，它不会执行值比较。</span><span class="sxs-lookup"><span data-stu-id="270bc-115">However, it doesn't perform value comparisons.</span></span> <span data-ttu-id="270bc-116">如果 `object1` 和 `object2` 都引用完全相同的对象实例，则 `result` 为 `False` ; 如果不是，则为; 如果不是， `result` 则为 `True` 。</span><span class="sxs-lookup"><span data-stu-id="270bc-116">If `object1` and `object2` both refer to the exact same object instance, `result` is `False`; if they don't, `result` is `True`.</span></span>

<span data-ttu-id="270bc-117">`IsNot` 与 `Is` 运算符相反。</span><span class="sxs-lookup"><span data-stu-id="270bc-117">`IsNot` is the opposite of the `Is` operator.</span></span> <span data-ttu-id="270bc-118">的优点 `IsNot` 是，您可以避免使用 `Not` 和 `Is` 难以理解语法，这会很难阅读。</span><span class="sxs-lookup"><span data-stu-id="270bc-118">The advantage of `IsNot` is that you can avoid awkward syntax with `Not` and `Is`, which can be difficult to read.</span></span>

 <span data-ttu-id="270bc-119">您可以使用 `Is` 和 `IsNot` 运算符来测试早期绑定对象和后期绑定对象。</span><span class="sxs-lookup"><span data-stu-id="270bc-119">You can use the `Is` and `IsNot` operators to test both early-bound and late-bound objects.</span></span>

## <a name="example"></a><span data-ttu-id="270bc-120">示例</span><span class="sxs-lookup"><span data-stu-id="270bc-120">Example</span></span>

<span data-ttu-id="270bc-121">下面的代码示例使用 `Is` 运算符和 `IsNot` 运算符来完成相同的比较。</span><span class="sxs-lookup"><span data-stu-id="270bc-121">The following code example uses both the `Is` operator and the `IsNot` operator to accomplish the same comparison.</span></span>

[!code-vb[VbVbalrOperators#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#29)]

## <a name="use-typeof-operator-with-isnot-operator"></a><span data-ttu-id="270bc-122">对 IsNot 运算符使用 TypeOf 运算符</span><span class="sxs-lookup"><span data-stu-id="270bc-122">Use TypeOf operator with IsNot operator</span></span>

<span data-ttu-id="270bc-123">从 Visual Basic 14 开始，可以将 `TypeOf` 运算符与运算符一起使用， `IsNot` 以测试对象是否与数据类型 *不* 兼容。</span><span class="sxs-lookup"><span data-stu-id="270bc-123">Starting with Visual Basic 14, you can use the `TypeOf` operator with the `IsNot` operator to test whether an object is *not* compatible with a data type.</span></span> <span data-ttu-id="270bc-124">例如：</span><span class="sxs-lookup"><span data-stu-id="270bc-124">For example:</span></span>

```vb
If TypeOf sender IsNot Button Then
```

## <a name="see-also"></a><span data-ttu-id="270bc-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="270bc-125">See also</span></span>

- [<span data-ttu-id="270bc-126">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="270bc-126">Is Operator</span></span>](is-operator.md)
- [<span data-ttu-id="270bc-127">TypeOf 运算符</span><span class="sxs-lookup"><span data-stu-id="270bc-127">TypeOf Operator</span></span>](typeof-operator.md)
- [<span data-ttu-id="270bc-128">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="270bc-128">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="270bc-129">如何：测试两个对象是否相同</span><span class="sxs-lookup"><span data-stu-id="270bc-129">How to: Test Whether Two Objects Are the Same</span></span>](../../programming-guide/language-features/operators-and-expressions/how-to-test-whether-two-objects-are-the-same.md)

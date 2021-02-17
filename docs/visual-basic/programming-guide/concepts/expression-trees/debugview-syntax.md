---
title: DebugView 属性使用的语法
description: 描述 DebugView 属性使用的特殊语法以生成表达式数的字符串表示形式
author: zspitz
ms.author: wiwagn
ms.date: 14/02/2021
ms.topic: reference
helpviewer_keywords:
- expression trees
- debugview
ms.openlocfilehash: 8a4feac72c2cd79485f5733b16d65b52cc50ee6c
ms.sourcegitcommit: f0fc5db7bcbf212e46933e9cf2d555bb82666141
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "100584891"
---
# <a name="debugview-syntax"></a><span data-ttu-id="c123f-103">**DebugView** 语法</span><span class="sxs-lookup"><span data-stu-id="c123f-103">**DebugView** syntax</span></span>

<span data-ttu-id="c123f-104">仅当调试) 提供表达式树的字符串呈现时， **DebugView** 属性才可用 (。</span><span class="sxs-lookup"><span data-stu-id="c123f-104">The **DebugView** property (available only when debugging) provides a string rendering of expression trees.</span></span> <span data-ttu-id="c123f-105">大部分语法都相当容易理解；特殊情况将在以下部分中介绍。</span><span class="sxs-lookup"><span data-stu-id="c123f-105">Most of the syntax is fairly straightforward to understand; the special cases are described in the following sections.</span></span>

<span data-ttu-id="c123f-106">每个示例后跟包含 **DebugView** 的注释块。</span><span class="sxs-lookup"><span data-stu-id="c123f-106">Each example is followed by a comment block containing the **DebugView**.</span></span>

## <a name="parameterexpression"></a><span data-ttu-id="c123f-107">ParameterExpression</span><span class="sxs-lookup"><span data-stu-id="c123f-107">ParameterExpression</span></span>

<span data-ttu-id="c123f-108"><xref:System.Linq.Expressions.ParameterExpression> 变量名称的开头显示有“$”符号。</span><span class="sxs-lookup"><span data-stu-id="c123f-108"><xref:System.Linq.Expressions.ParameterExpression> variable names are displayed with a "$" symbol at the beginning.</span></span>

<span data-ttu-id="c123f-109">如果参数没有名称，则会为其分配一个自动生成的名称，例如 `$var1` 或 `$var2`。</span><span class="sxs-lookup"><span data-stu-id="c123f-109">If a parameter does not have a name, it is assigned an automatically generated name, such as `$var1` or `$var2`.</span></span>

### <a name="examples"></a><span data-ttu-id="c123f-110">示例</span><span class="sxs-lookup"><span data-stu-id="c123f-110">Examples</span></span>

```vb
Dim numParam As ParameterExpression = Expression.Parameter(GetType(Integer), "num")
'
'    $num
'

Dim numParam As ParameterExpression = Expression.Parameter(GetType(Integer))
'
'    $var1
'
```

## <a name="constantexpressions"></a><span data-ttu-id="c123f-111">ConstantExpressions</span><span class="sxs-lookup"><span data-stu-id="c123f-111">ConstantExpressions</span></span>

<span data-ttu-id="c123f-112">对于表示整数值、字符串和 `null` 的 <xref:System.Linq.Expressions.ConstantExpression> 对象，将显示常数的值。</span><span class="sxs-lookup"><span data-stu-id="c123f-112">For <xref:System.Linq.Expressions.ConstantExpression> objects that represent integer values, strings, and `null`, the value of the constant is displayed.</span></span>

<span data-ttu-id="c123f-113">对于某些数值类型，会将一个后缀添加到值：</span><span class="sxs-lookup"><span data-stu-id="c123f-113">For some numeric types, a suffix is added to the value:</span></span>

| <span data-ttu-id="c123f-114">类型</span><span class="sxs-lookup"><span data-stu-id="c123f-114">Type</span></span> | <span data-ttu-id="c123f-115">关键字</span><span class="sxs-lookup"><span data-stu-id="c123f-115">Keyword</span></span> | <span data-ttu-id="c123f-116">Suffix</span><span class="sxs-lookup"><span data-stu-id="c123f-116">Suffix</span></span> |
|--|--|--|
| <xref:System.UInt32?displayProperty=nameWithType> | [<span data-ttu-id="c123f-117">UInteger</span><span class="sxs-lookup"><span data-stu-id="c123f-117">UInteger</span></span>](../../../language-reference/data-types/uinteger-data-type.md) | <span data-ttu-id="c123f-118">U</span><span class="sxs-lookup"><span data-stu-id="c123f-118">U</span></span> |
| <xref:System.Int64?displayProperty=nameWithType> | [<span data-ttu-id="c123f-119">Long</span><span class="sxs-lookup"><span data-stu-id="c123f-119">Long</span></span>](../../../language-reference/data-types/long-data-type.md) | <span data-ttu-id="c123f-120">L</span><span class="sxs-lookup"><span data-stu-id="c123f-120">L</span></span> |
| <xref:System.UInt64?displayProperty=nameWithType> | [<span data-ttu-id="c123f-121">ULong</span><span class="sxs-lookup"><span data-stu-id="c123f-121">ULong</span></span>](../../../language-reference/data-types/ulong-data-type.md) | <span data-ttu-id="c123f-122">UL</span><span class="sxs-lookup"><span data-stu-id="c123f-122">UL</span></span> |
| <xref:System.Double?displayProperty=nameWithType> | [<span data-ttu-id="c123f-123">双精度</span><span class="sxs-lookup"><span data-stu-id="c123f-123">Double</span></span>](../../../language-reference/data-types/double-data-type.md) | <span data-ttu-id="c123f-124">D</span><span class="sxs-lookup"><span data-stu-id="c123f-124">D</span></span> |
| <xref:System.Single?displayProperty=nameWithType> | [<span data-ttu-id="c123f-125">单精度</span><span class="sxs-lookup"><span data-stu-id="c123f-125">Single</span></span>](../../../language-reference/data-types/single-data-type.md) | <span data-ttu-id="c123f-126">F</span><span class="sxs-lookup"><span data-stu-id="c123f-126">F</span></span> |
| <xref:System.Decimal?displayProperty=nameWithType> | <span data-ttu-id="c123f-127">十进制 </span><span class="sxs-lookup"><span data-stu-id="c123f-127">[Decimal](../../../language-reference/data-types/decimal-data-type.md)</span></span> | <span data-ttu-id="c123f-128">M</span><span class="sxs-lookup"><span data-stu-id="c123f-128">M</span></span> |

### <a name="examples"></a><span data-ttu-id="c123f-129">示例</span><span class="sxs-lookup"><span data-stu-id="c123f-129">Examples</span></span>

```vb
Dim num as Integer = 10
Dim expr As ConstantExpression = Expression.Constant(num)
'
'    10
'

Dim num As Double = 10
Dim expr As ConstantExpression = Expression.Constant(num)
'
'    10D
'
```

## <a name="blockexpression"></a><span data-ttu-id="c123f-130">BlockExpression</span><span class="sxs-lookup"><span data-stu-id="c123f-130">BlockExpression</span></span>

<span data-ttu-id="c123f-131">如果 <xref:System.Linq.Expressions.BlockExpression> 对象的类型与块中最后一个表达式的类型不同，则该类型将显示在尖括号（`<` 和 `>`）内。</span><span class="sxs-lookup"><span data-stu-id="c123f-131">If the type of a <xref:System.Linq.Expressions.BlockExpression> object differs from the type of the last expression in the block, the type is displayed within angle brackets (`<` and `>`).</span></span> <span data-ttu-id="c123f-132">否则，将不显示 <xref:System.Linq.Expressions.BlockExpression> 对象的类型。</span><span class="sxs-lookup"><span data-stu-id="c123f-132">Otherwise, the type of the <xref:System.Linq.Expressions.BlockExpression> object is not displayed.</span></span>

### <a name="examples"></a><span data-ttu-id="c123f-133">示例</span><span class="sxs-lookup"><span data-stu-id="c123f-133">Examples</span></span>

```vb
Dim block As BlockExpression = Expression.Block(Expression.Constant("test"))
'
'    .Block() {
'        "test"
'    }
'

Dim block As BlockExpression = Expression.Block(
    GetType(Object),
    Expression.Constant("test")
)
'
'    .Block<System.Object>() {
'        "test"
'    }
'
```

## <a name="lambdaexpression"></a><span data-ttu-id="c123f-134">LambdaExpression</span><span class="sxs-lookup"><span data-stu-id="c123f-134">LambdaExpression</span></span>

<span data-ttu-id="c123f-135">显示 <xref:System.Linq.Expressions.LambdaExpression> 对象及其委托类型。</span><span class="sxs-lookup"><span data-stu-id="c123f-135"><xref:System.Linq.Expressions.LambdaExpression> objects are displayed together with their delegate types.</span></span>

<span data-ttu-id="c123f-136">如果 lambda 表达式没有名称，则会为其分配一个自动生成的名称，例如 `#Lambda1` 或 `#Lambda2`。</span><span class="sxs-lookup"><span data-stu-id="c123f-136">If a lambda expression does not have a name, it is assigned an automatically generated name, such as `#Lambda1` or `#Lambda2`.</span></span>

### <a name="examples"></a><span data-ttu-id="c123f-137">示例</span><span class="sxs-lookup"><span data-stu-id="c123f-137">Examples</span></span>

```vb
Dim lambda As LambdaExpression = Expression.Lambda(Of Func(Of Integer))(
    Expression.Constant(1)
)
'
'    .Lambda #Lambda1<System.Func'1[System.Int32]>() {
'        1
'    }
'

Dim lambda As LambdaExpression = Expression.Lambda(Of Func(Of Integer))(
    Expression.Constant(1),
    "SampleLambda",
    Nothing
)
'
'    .Lambda #SampleLambda<System.Func'1[System.Int32]>() {
'        1
'    }
'
```

## <a name="labelexpression"></a><span data-ttu-id="c123f-138">LabelExpression</span><span class="sxs-lookup"><span data-stu-id="c123f-138">LabelExpression</span></span>

<span data-ttu-id="c123f-139">如果指定 <xref:System.Linq.Expressions.LabelExpression> 对象的默认值，则在 <xref:System.Linq.Expressions.LabelTarget> 对象之前显示此值。</span><span class="sxs-lookup"><span data-stu-id="c123f-139">If you specify a default value for the <xref:System.Linq.Expressions.LabelExpression> object, this value is displayed before the <xref:System.Linq.Expressions.LabelTarget> object.</span></span>

<span data-ttu-id="c123f-140">`.Label` 令牌指示标签的开头。</span><span class="sxs-lookup"><span data-stu-id="c123f-140">The `.Label` token indicates the start of the label.</span></span> <span data-ttu-id="c123f-141">`.LabelTarget` 令牌指示要跳转到的目标的目的地。</span><span class="sxs-lookup"><span data-stu-id="c123f-141">The `.LabelTarget` token indicates the destination of the target to jump to.</span></span>

<span data-ttu-id="c123f-142">如果标签没有名称，则会为其分配一个自动生成的名称，例如 `#Label1` 或 `#Label2`。</span><span class="sxs-lookup"><span data-stu-id="c123f-142">If a label does not have a name, it is assigned an automatically generated name, such as `#Label1` or `#Label2`.</span></span>

### <a name="examples"></a><span data-ttu-id="c123f-143">示例</span><span class="sxs-lookup"><span data-stu-id="c123f-143">Examples</span></span>

```vb
Dim target As LabelTarget = Expression.Label(GetType(Integer), "SampleLabel")
Dim label1 As BlockExpression = Expression.Block(
    Expression.Goto(target, Expression.Constant(0)),
    Expression.Label(target, Expression.Constant(-1))
)
'
'    .Block() {
'        .Goto SampleLabel { 0 };
'        .Label
'            -1
'        .LabelTarget SampleLabel:
'    }
'

Dim target As LabelTarget = Expression.Label()
Dim block As BlockExpression = Expression.Block(
    Expression.Goto(target),
    Expression.Label(target)
)
'
'    .Block() {
'        .Goto #Label1 { };
'        .Label
'        .LabelTarget #Label1:
'    }
'
```

## <a name="checked-operators"></a><span data-ttu-id="c123f-144">Checked 运算符</span><span class="sxs-lookup"><span data-stu-id="c123f-144">Checked Operators</span></span>

<span data-ttu-id="c123f-145">Checked 运算符在运算符前面显示 `#` 符号。</span><span class="sxs-lookup"><span data-stu-id="c123f-145">Checked operators are displayed with the `#` symbol in front of the operator.</span></span> <span data-ttu-id="c123f-146">例如，checked 加号显示为 `#+`。</span><span class="sxs-lookup"><span data-stu-id="c123f-146">For example, the checked addition operator is displayed as `#+`.</span></span>

### <a name="examples"></a><span data-ttu-id="c123f-147">示例</span><span class="sxs-lookup"><span data-stu-id="c123f-147">Examples</span></span>

```vb
Dim expr As Expression = Expression.AddChecked(
    Expression.Constant(1),
    Expression.Constant(2)
)
'
'     1 #+ 2
'

Dim expr As Expression = Expression.ConvertChecked(
    Expression.Constant(10.0),
    GetType(Integer)
)
'
'    #(System.Int32)10D
'
```

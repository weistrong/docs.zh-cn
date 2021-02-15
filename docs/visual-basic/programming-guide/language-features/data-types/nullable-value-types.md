---
description: '了解有关以下内容的详细信息：可为 Null 的值类型 (Visual Basic) '
title: 可以为 null 的值类型
ms.date: 07/20/2015
f1_keywords:
- vb.Nullable
helpviewer_keywords:
- nullable types [Visual Basic]
- '? [Visual Basic]'
- types [Visual Basic], nullable
- nullable types [Visual Basic]
- data types [Visual Basic], nullable
ms.assetid: 9ac3b602-6f96-4e6d-96f7-cd4e81c468a6
ms.openlocfilehash: acc91d98a3ed288a9bf0bcf6abbd3d8a516bd699
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100483880"
---
# <a name="nullable-value-types-visual-basic"></a><span data-ttu-id="7dbe8-103">可以为 Null 的值类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7dbe8-103">Nullable Value Types (Visual Basic)</span></span>

<span data-ttu-id="7dbe8-104">有时，您在某些情况下使用的值类型不具有定义的值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-104">Sometimes you work with a value type that does not have a defined value in certain circumstances.</span></span> <span data-ttu-id="7dbe8-105">例如，数据库中的字段可能必须区分分配的值是否有意义，并且没有分配值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-105">For example, a field in a database might have to distinguish between having an assigned value that is meaningful and not having an assigned value.</span></span> <span data-ttu-id="7dbe8-106">可以对值类型进行扩展，使其使用普通值或 null 值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-106">Value types can be extended to take either their normal values or a null value.</span></span> <span data-ttu-id="7dbe8-107">此类扩展称为 *可以为 null 的类型*。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-107">Such an extension is called a *nullable type*.</span></span>

<span data-ttu-id="7dbe8-108">每个可以为 null 的值类型都是从泛型结构构造的 <xref:System.Nullable%601> 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-108">Each nullable value type is constructed from the generic <xref:System.Nullable%601> structure.</span></span> <span data-ttu-id="7dbe8-109">考虑使用跟踪工作相关活动的数据库。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-109">Consider a database that tracks work-related activities.</span></span> <span data-ttu-id="7dbe8-110">下面的示例构造一个可以为 null 的 `Boolean` 类型，并声明该类型的变量。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-110">The following example constructs a nullable `Boolean` type and declares a variable of that type.</span></span> <span data-ttu-id="7dbe8-111">可以通过三种方式编写声明：</span><span class="sxs-lookup"><span data-stu-id="7dbe8-111">You can write the declaration in three ways:</span></span>

[!code-vb[VbVbalrNullableValue#1](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#1)]

<span data-ttu-id="7dbe8-112">变量 `ridesBusToWork` 可以包含值 `True` 、值 `False` 或根本不包含值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-112">The variable `ridesBusToWork` can hold a value of `True`, a value of `False`, or no value at all.</span></span> <span data-ttu-id="7dbe8-113">默认情况下，它的初始默认值为 "无" 值，在这种情况下，这可能意味着尚未获取此人的信息。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-113">Its initial default value is no value at all, which in this case could mean that the information has not yet been obtained for this person.</span></span> <span data-ttu-id="7dbe8-114">与此相反， `False` 可能表示信息已获得，并且用户不能使用该总线。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-114">In contrast, `False` could mean that the information has been obtained and the person does not ride the bus to work.</span></span>

<span data-ttu-id="7dbe8-115">可以声明具有可以为 null 的值类型的变量和属性，并且可以使用可以为 null 的值类型的元素声明数组。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-115">You can declare variables and properties with nullable value types, and you can declare an array with elements of a nullable value type.</span></span> <span data-ttu-id="7dbe8-116">您可以使用可以为 null 的值类型作为参数来声明过程，并且可以从过程中返回可以为 null 的值类型 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-116">You can declare procedures with nullable value types as parameters, and you can return a nullable value type from a `Function` procedure.</span></span>

<span data-ttu-id="7dbe8-117">不能对引用类型（如数组、或类）构造可以为 null 的类型 `String` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-117">You cannot construct a nullable type on a reference type such as an array, a `String`, or a class.</span></span> <span data-ttu-id="7dbe8-118">基础类型必须为值类型。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-118">The underlying type must be a value type.</span></span> <span data-ttu-id="7dbe8-119">有关详细信息，请参阅 [值类型和引用类型](value-types-and-reference-types.md)。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-119">For more information, see [Value Types and Reference Types](value-types-and-reference-types.md).</span></span>

## <a name="using-a-nullable-type-variable"></a><span data-ttu-id="7dbe8-120">使用可以为 Null 的类型变量</span><span class="sxs-lookup"><span data-stu-id="7dbe8-120">Using a Nullable Type Variable</span></span>

<span data-ttu-id="7dbe8-121">可以为 null 的值类型的最重要成员是其 <xref:System.Nullable%601.HasValue%2A> 和 <xref:System.Nullable%601.Value%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-121">The most important members of a nullable value type are its <xref:System.Nullable%601.HasValue%2A> and <xref:System.Nullable%601.Value%2A> properties.</span></span> <span data-ttu-id="7dbe8-122">对于可以为 null 的值类型的变量， <xref:System.Nullable%601.HasValue%2A> 会告诉您变量是否包含定义的值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-122">For a variable of a nullable value type, <xref:System.Nullable%601.HasValue%2A> tells you whether the variable contains a defined value.</span></span> <span data-ttu-id="7dbe8-123">如果 <xref:System.Nullable%601.HasValue%2A> 为 `True` ，则可以从中读取值 <xref:System.Nullable%601.Value%2A> 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-123">If <xref:System.Nullable%601.HasValue%2A> is `True`, you can read the value from <xref:System.Nullable%601.Value%2A>.</span></span> <span data-ttu-id="7dbe8-124">请注意， <xref:System.Nullable%601.HasValue%2A> 和 <xref:System.Nullable%601.Value%2A> 都是 `ReadOnly` 属性。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-124">Note that both <xref:System.Nullable%601.HasValue%2A> and <xref:System.Nullable%601.Value%2A> are `ReadOnly` properties.</span></span>

### <a name="default-values"></a><span data-ttu-id="7dbe8-125">默认值</span><span class="sxs-lookup"><span data-stu-id="7dbe8-125">Default Values</span></span>

<span data-ttu-id="7dbe8-126">当你使用可以为 null 的值类型声明变量时，其 <xref:System.Nullable%601.HasValue%2A> 属性的默认值为 `False` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-126">When you declare a variable with a nullable value type, its <xref:System.Nullable%601.HasValue%2A> property has a default value of `False`.</span></span> <span data-ttu-id="7dbe8-127">这意味着，默认情况下，该变量没有定义的值，而不是其基础值类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-127">This means that by default the variable has no defined value, instead of the default value of its underlying value type.</span></span> <span data-ttu-id="7dbe8-128">在下面的示例中，变量 `numberOfChildren` 最初没有定义的值，即使该类型的默认值 `Integer` 为0。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-128">In the following example, the variable `numberOfChildren` initially has no defined value, even though the default value of the `Integer` type is 0.</span></span>

[!code-vb[VbVbalrNullableValue#2](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#2)]

<span data-ttu-id="7dbe8-129">空值有助于指示未定义或未知的值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-129">A null value is useful to indicate an undefined or unknown value.</span></span> <span data-ttu-id="7dbe8-130">如果 `numberOfChildren` 已将声明为 `Integer` ，则不会有任何值表明信息当前不可用。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-130">If `numberOfChildren` had been declared as `Integer`, there would be no value that could indicate that the information is not currently available.</span></span>

### <a name="storing-values"></a><span data-ttu-id="7dbe8-131">存储值</span><span class="sxs-lookup"><span data-stu-id="7dbe8-131">Storing Values</span></span>

<span data-ttu-id="7dbe8-132">以典型方式将值存储在可以为 null 的值类型的变量或属性中。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-132">You store a value in a variable or property of a nullable value type in the typical way.</span></span> <span data-ttu-id="7dbe8-133">下面的示例将值赋给 `numberOfChildren` 在上一个示例中声明的变量。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-133">The following example assigns a value to the variable `numberOfChildren` declared in the previous example.</span></span>

[!code-vb[VbVbalrNullableValue#3](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#3)]

<span data-ttu-id="7dbe8-134">如果可以为 null 的值类型的变量或属性包含定义的值，则可以使其恢复到未分配值的初始状态。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-134">If a variable or property of a nullable value type contains a defined value, you can cause it to revert to its initial state of not having a value assigned.</span></span> <span data-ttu-id="7dbe8-135">为此，可将变量或属性设置为 `Nothing` ，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-135">You do this by setting the variable or property to `Nothing`, as the following example shows.</span></span>

[!code-vb[VbVbalrNullableValue#4](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#4)]

> [!NOTE]
> <span data-ttu-id="7dbe8-136">虽然可以将分配 `Nothing` 给可以为 null 的值类型的变量，但不能 `Nothing` 使用等号对其进行测试。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-136">Although you can assign `Nothing` to a variable of a nullable value type, you cannot test it for `Nothing` by using the equal sign.</span></span> <span data-ttu-id="7dbe8-137">使用等号的比较的 `someVar = Nothing` 计算结果始终为 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-137">Comparison that uses the equal sign, `someVar = Nothing`, always evaluates to `Nothing`.</span></span> <span data-ttu-id="7dbe8-138">可以测试变量的 <xref:System.Nullable%601.HasValue%2A> 属性 `False` ，或使用 `Is` or `IsNot` 运算符测试。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-138">You can test the variable's <xref:System.Nullable%601.HasValue%2A> property for `False`, or test by using the `Is` or `IsNot` operator.</span></span>

### <a name="retrieving-values"></a><span data-ttu-id="7dbe8-139">检索值</span><span class="sxs-lookup"><span data-stu-id="7dbe8-139">Retrieving Values</span></span>

<span data-ttu-id="7dbe8-140">若要检索可为 null 的值类型的变量的值，您应该首先测试其 <xref:System.Nullable%601.HasValue%2A> 属性以确认它具有值。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-140">To retrieve the value of a variable of a nullable value type, you should first test its <xref:System.Nullable%601.HasValue%2A> property to confirm that it has a value.</span></span> <span data-ttu-id="7dbe8-141">如果在为时尝试读取值 <xref:System.Nullable%601.HasValue%2A> `False` ，Visual Basic 会引发 <xref:System.InvalidOperationException> 异常。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-141">If you try to read the value when <xref:System.Nullable%601.HasValue%2A> is `False`, Visual Basic throws an <xref:System.InvalidOperationException> exception.</span></span> <span data-ttu-id="7dbe8-142">下面的示例演示了读取前面示例的变量的建议方法 `numberOfChildren` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-142">The following example shows the recommended way to read the variable `numberOfChildren` of the previous examples.</span></span>

[!code-vb[VbVbalrNullableValue#5](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#5)]

## <a name="comparing-nullable-types"></a><span data-ttu-id="7dbe8-143">比较可以为 Null 的类型</span><span class="sxs-lookup"><span data-stu-id="7dbe8-143">Comparing Nullable Types</span></span>

<span data-ttu-id="7dbe8-144">在 `Boolean` 布尔表达式中使用可以为 null 的变量时，结果可以是 `True` 、 `False` 或 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-144">When nullable `Boolean` variables are used in Boolean expressions, the result can be `True`, `False`, or `Nothing`.</span></span> <span data-ttu-id="7dbe8-145">下面是和的事实数据表 `And` `Or` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-145">The following is the truth table for `And` and `Or`.</span></span> <span data-ttu-id="7dbe8-146">由于 `b1` 和 `b2` 现在具有三个可能的值，因此有九个计算组合。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-146">Because `b1` and `b2` now have three possible values, there are nine combinations to evaluate.</span></span>

|<span data-ttu-id="7dbe8-147">b1</span><span class="sxs-lookup"><span data-stu-id="7dbe8-147">b1</span></span>|<span data-ttu-id="7dbe8-148">b2</span><span class="sxs-lookup"><span data-stu-id="7dbe8-148">b2</span></span>|<span data-ttu-id="7dbe8-149">b1 和 b2</span><span class="sxs-lookup"><span data-stu-id="7dbe8-149">b1 And b2</span></span>|<span data-ttu-id="7dbe8-150">b1 或 b2</span><span class="sxs-lookup"><span data-stu-id="7dbe8-150">b1 Or b2</span></span>|
|--------|--------|---------------|--------------|
|`Nothing`|`Nothing`|`Nothing`|`Nothing`|
|`Nothing`|`True`|`Nothing`|`True`|
|`Nothing`|`False`|`False`|`Nothing`|
|`True`|`Nothing`|`Nothing`|`True`|
|`True`|`True`|`True`|`True`|
|`True`|`False`|`False`|`True`|
|`False`|`Nothing`|`False`|`Nothing`|
|`False`|`True`|`False`|`True`|
|`False`|`False`|`False`|`False`|

<span data-ttu-id="7dbe8-151">当布尔变量或表达式的值为时 `Nothing` ，它既不是 `true` 也不是 `false` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-151">When the value of a Boolean variable or expression is `Nothing`, it is neither `true` nor `false`.</span></span> <span data-ttu-id="7dbe8-152">请看下面的示例。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-152">Consider the following example.</span></span>

[!code-vb[VbVbalrNullableValue#6](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#6)]

<span data-ttu-id="7dbe8-153">在此示例中， `b1 And b2` 计算结果为 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-153">In this example, `b1 And b2` evaluates to `Nothing`.</span></span> <span data-ttu-id="7dbe8-154">因此， `Else` 子句是在每个语句中执行的 `If` ，输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="7dbe8-154">As a result, the `Else` clause is executed in each `If` statement, and the output is as follows:</span></span>

`Expression is not true`

`Expression is not false`

> [!NOTE]
> <span data-ttu-id="7dbe8-155">`AndAlso``OrElse`如果和使用短路计算，则必须在第一个计算结果为时计算其第二个操作数 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-155">`AndAlso` and `OrElse`, which use short-circuit evaluation, must evaluate their second operands when the first evaluates to `Nothing`.</span></span>

## <a name="propagation"></a><span data-ttu-id="7dbe8-156">传播</span><span class="sxs-lookup"><span data-stu-id="7dbe8-156">Propagation</span></span>

<span data-ttu-id="7dbe8-157">如果算术、比较、移位或类型运算的一个或两个操作数是可以为 null 的值类型，则运算的结果也是可以为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-157">If one or both of the operands of an arithmetic, comparison, shift, or type operation is a nullable value type, the result of the operation is also a nullable value type.</span></span> <span data-ttu-id="7dbe8-158">如果两个操作数的值都不是，则对 `Nothing` 操作数的基础值执行运算，就像两者都不是可以为 null 的值类型一样。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-158">If both operands have values that are not `Nothing`, the operation is performed on the underlying values of the operands, as if neither were a nullable value type.</span></span> <span data-ttu-id="7dbe8-159">在下面的示例中，变量 `compare1` 和 `sum1` 是隐式类型。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-159">In the following example, variables `compare1` and `sum1` are implicitly typed.</span></span> <span data-ttu-id="7dbe8-160">如果将鼠标指针停留在其上，则会看到编译器将为这两个值推断出可为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-160">If you rest the mouse pointer over them, you will see that the compiler infers nullable value types for both of them.</span></span>

[!code-vb[VbVbalrNullableValue#7](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#7)]

<span data-ttu-id="7dbe8-161">如果一个或两个操作数的值都为 `Nothing` ，则结果将为 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-161">If one or both operands have a value of `Nothing`, the result will be `Nothing`.</span></span>

[!code-vb[VbVbalrNullableValue#8](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#8)]

## <a name="using-nullable-types-with-data"></a><span data-ttu-id="7dbe8-162">对数据使用可以为 Null 的类型</span><span class="sxs-lookup"><span data-stu-id="7dbe8-162">Using Nullable Types with Data</span></span>

<span data-ttu-id="7dbe8-163">数据库是使用可以为 null 的值类型的最重要的地方之一。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-163">A database is one of the most important places to use nullable value types.</span></span> <span data-ttu-id="7dbe8-164">并非所有数据库对象当前都支持可以为 null 的值类型，而是由设计器生成的表适配器。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-164">Not all database objects currently support nullable value types, but the designer-generated table adapters do.</span></span> <span data-ttu-id="7dbe8-165">请参阅 [对可以为 null 的类型的 TableAdapter 支持](/visualstudio/data-tools/fill-datasets-by-using-tableadapters#tableadapter-support-for-nullable-types)。</span><span class="sxs-lookup"><span data-stu-id="7dbe8-165">See [TableAdapter support for nullable types](/visualstudio/data-tools/fill-datasets-by-using-tableadapters#tableadapter-support-for-nullable-types).</span></span>

## <a name="see-also"></a><span data-ttu-id="7dbe8-166">请参阅</span><span class="sxs-lookup"><span data-stu-id="7dbe8-166">See also</span></span>

- <xref:System.InvalidOperationException>
- <xref:System.Nullable%601.HasValue%2A>
- [<span data-ttu-id="7dbe8-167">数据类型</span><span class="sxs-lookup"><span data-stu-id="7dbe8-167">Data Types</span></span>](index.md)
- [<span data-ttu-id="7dbe8-168">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="7dbe8-168">Value Types and Reference Types</span></span>](value-types-and-reference-types.md)
- [<span data-ttu-id="7dbe8-169">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="7dbe8-169">Troubleshooting Data Types</span></span>](troubleshooting-data-types.md)
- [<span data-ttu-id="7dbe8-170">使用 Tableadapter 填充数据集</span><span class="sxs-lookup"><span data-stu-id="7dbe8-170">Fill datasets by using TableAdapters</span></span>](/visualstudio/data-tools/fill-datasets-by-using-tableadapters)
- [<span data-ttu-id="7dbe8-171">If 运算符</span><span class="sxs-lookup"><span data-stu-id="7dbe8-171">If Operator</span></span>](../../../language-reference/operators/if-operator.md)
- [<span data-ttu-id="7dbe8-172">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="7dbe8-172">Local Type Inference</span></span>](../variables/local-type-inference.md)
- [<span data-ttu-id="7dbe8-173">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="7dbe8-173">Is Operator</span></span>](../../../language-reference/operators/is-operator.md)
- [<span data-ttu-id="7dbe8-174">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="7dbe8-174">IsNot Operator</span></span>](../../../language-reference/operators/isnot-operator.md)
- [<span data-ttu-id="7dbe8-175">C # (可以为 null 的值类型 ) </span><span class="sxs-lookup"><span data-stu-id="7dbe8-175">Nullable Value Types (C#)</span></span>](../../../../csharp/language-reference/builtin-types/nullable-value-types.md)

---
description: '了解详细信息：比较运算符 (Visual Basic) '
title: 比较运算符
ms.date: 07/20/2015
f1_keywords:
- vb.<>
- vb.>=
- vb.<=
- vb.>
- vb.<
helpviewer_keywords:
- greater than or equal to operator [Visual Basic]
- '>= operator [Visual Basic]'
- = operator [Visual Basic]
- < operator [Visual Basic]
- less than operator [Visual Basic]
- relational operators [Visual Basic], syntax
- Like operator [Visual Basic]
- <> operator [Visual Basic]
- '> operator [Visual Basic]'
- equal operator [Visual Basic]
- less than or equal to operator [Visual Basic]
- symbols, operators
- greater than operator [Visual Basic]
- comparing values [Visual Basic]
- operators [Visual Basic], relational
- string comparison [Visual Basic]
- not equal to comparison operator [Visual Basic]
- <= operator [Visual Basic]
- operators [Visual Basic], comparison
- Is operator [Visual Basic]
- comparison operators [Visual Basic], Visual Basic
ms.assetid: d6cb12a8-e52e-46a7-8aaf-f804d634a825
ms.openlocfilehash: 28eded0cfae54ec83ad9546b801243e4de0e45fc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774104"
---
# <a name="comparison-operators-visual-basic"></a><span data-ttu-id="db9b9-103">比较运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="db9b9-103">Comparison Operators (Visual Basic)</span></span>

<span data-ttu-id="db9b9-104">下面是 Visual Basic 中定义的比较运算符。</span><span class="sxs-lookup"><span data-stu-id="db9b9-104">The following are the comparison operators defined in Visual Basic.</span></span>

 <span data-ttu-id="db9b9-105">`<` 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-105">`<` operator</span></span>

 <span data-ttu-id="db9b9-106">`<=` 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-106">`<=` operator</span></span>

 <span data-ttu-id="db9b9-107">`>` 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-107">`>` operator</span></span>

 <span data-ttu-id="db9b9-108">`>=` 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-108">`>=` operator</span></span>

 <span data-ttu-id="db9b9-109">`=` 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-109">`=` operator</span></span>

 <span data-ttu-id="db9b9-110">`<>` 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-110">`<>` operator</span></span>

 [<span data-ttu-id="db9b9-111">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-111">Is Operator</span></span>](is-operator.md)

 [<span data-ttu-id="db9b9-112">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-112">IsNot Operator</span></span>](isnot-operator.md)

 [<span data-ttu-id="db9b9-113">Like 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-113">Like Operator</span></span>](like-operator.md)

 <span data-ttu-id="db9b9-114">这些运算符比较两个表达式以确定它们是否相等，如果不相等，则确定它们之间的差异。</span><span class="sxs-lookup"><span data-stu-id="db9b9-114">These operators compare two expressions to determine whether or not they are equal, and if not, how they differ.</span></span> <span data-ttu-id="db9b9-115">`Is``IsNot` `Like` 在单独的帮助页上详细讨论了、和。</span><span class="sxs-lookup"><span data-stu-id="db9b9-115">`Is`, `IsNot`, and `Like` are discussed in detail on separate Help pages.</span></span> <span data-ttu-id="db9b9-116">此页上详细讨论了关系比较运算符。</span><span class="sxs-lookup"><span data-stu-id="db9b9-116">The relational comparison operators are discussed in detail on this page.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9b9-117">语法</span><span class="sxs-lookup"><span data-stu-id="db9b9-117">Syntax</span></span>
  
```vb
result = expression1 comparisonoperator expression2  
result = object1 [Is | IsNot] object2  
result = string Like pattern  
```  
  
## <a name="parts"></a><span data-ttu-id="db9b9-118">组成部分</span><span class="sxs-lookup"><span data-stu-id="db9b9-118">Parts</span></span>

 `result`  
 <span data-ttu-id="db9b9-119">必需。</span><span class="sxs-lookup"><span data-stu-id="db9b9-119">Required.</span></span> <span data-ttu-id="db9b9-120">一个 `Boolean` 值，该值表示比较的结果。</span><span class="sxs-lookup"><span data-stu-id="db9b9-120">A `Boolean` value representing the result of the comparison.</span></span>

 <span data-ttu-id="db9b9-121">`expression1`, `expression2`</span><span class="sxs-lookup"><span data-stu-id="db9b9-121">`expression1`, `expression2`</span></span>  
 <span data-ttu-id="db9b9-122">必需。</span><span class="sxs-lookup"><span data-stu-id="db9b9-122">Required.</span></span> <span data-ttu-id="db9b9-123">任何表达式。</span><span class="sxs-lookup"><span data-stu-id="db9b9-123">Any expression.</span></span>

 `comparisonoperator`  
 <span data-ttu-id="db9b9-124">必需。</span><span class="sxs-lookup"><span data-stu-id="db9b9-124">Required.</span></span> <span data-ttu-id="db9b9-125">任何关系比较运算符。</span><span class="sxs-lookup"><span data-stu-id="db9b9-125">Any relational comparison operator.</span></span>

 <span data-ttu-id="db9b9-126">`object1`, `object2`</span><span class="sxs-lookup"><span data-stu-id="db9b9-126">`object1`, `object2`</span></span>  
 <span data-ttu-id="db9b9-127">必需。</span><span class="sxs-lookup"><span data-stu-id="db9b9-127">Required.</span></span> <span data-ttu-id="db9b9-128">任何引用对象的名称。</span><span class="sxs-lookup"><span data-stu-id="db9b9-128">Any reference object names.</span></span>

 `string`  
 <span data-ttu-id="db9b9-129">必需。</span><span class="sxs-lookup"><span data-stu-id="db9b9-129">Required.</span></span> <span data-ttu-id="db9b9-130">任何 `String` 表达式。</span><span class="sxs-lookup"><span data-stu-id="db9b9-130">Any `String` expression.</span></span>

 `pattern`  
 <span data-ttu-id="db9b9-131">必需。</span><span class="sxs-lookup"><span data-stu-id="db9b9-131">Required.</span></span> <span data-ttu-id="db9b9-132">任何 `String` 表达式或字符范围。</span><span class="sxs-lookup"><span data-stu-id="db9b9-132">Any `String` expression or range of characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9b9-133">备注</span><span class="sxs-lookup"><span data-stu-id="db9b9-133">Remarks</span></span>

 <span data-ttu-id="db9b9-134">下表包含关系比较运算符和确定是还是的条件的列表 `result` `True` `False` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-134">The following table contains a list of the relational comparison operators and the conditions that determine whether `result` is `True` or `False`.</span></span>

|<span data-ttu-id="db9b9-135">操作员</span><span class="sxs-lookup"><span data-stu-id="db9b9-135">Operator</span></span>|<span data-ttu-id="db9b9-136">`True` 是否</span><span class="sxs-lookup"><span data-stu-id="db9b9-136">`True` if</span></span>|<span data-ttu-id="db9b9-137">`False` 是否</span><span class="sxs-lookup"><span data-stu-id="db9b9-137">`False` if</span></span>|
|--------------|---------------|----------------|
|<span data-ttu-id="db9b9-138">`<` (小于) </span><span class="sxs-lookup"><span data-stu-id="db9b9-138">`<` (Less than)</span></span>|`expression1` < `expression2`|`expression1` >= `expression2`|
|<span data-ttu-id="db9b9-139">`<=` (小于或等于) </span><span class="sxs-lookup"><span data-stu-id="db9b9-139">`<=` (Less than or equal to)</span></span>|`expression1` <= `expression2`|`expression1` > `expression2`|
|<span data-ttu-id="db9b9-140">`>` (大于) </span><span class="sxs-lookup"><span data-stu-id="db9b9-140">`>` (Greater than)</span></span>|`expression1` > `expression2`|`expression1` <= `expression2`|
|<span data-ttu-id="db9b9-141">`>=` (大于或等于) </span><span class="sxs-lookup"><span data-stu-id="db9b9-141">`>=` (Greater than or equal to)</span></span>|`expression1` >= `expression2`|`expression1` < `expression2`|
|<span data-ttu-id="db9b9-142">`=` (等于) </span><span class="sxs-lookup"><span data-stu-id="db9b9-142">`=` (Equal to)</span></span>|`expression1` = `expression2`|`expression1` <> `expression2`|
|<span data-ttu-id="db9b9-143">`<>` (不等于) </span><span class="sxs-lookup"><span data-stu-id="db9b9-143">`<>` (Not equal to)</span></span>|`expression1` <> `expression2`|`expression1` = `expression2`|

> [!NOTE]
> <span data-ttu-id="db9b9-144">[= 运算符](assignment-operator.md)也用作赋值运算符。</span><span class="sxs-lookup"><span data-stu-id="db9b9-144">The [= Operator](assignment-operator.md) is also used as an assignment operator.</span></span>

 <span data-ttu-id="db9b9-145">`Is`运算符、运算符 `IsNot` 和 `Like` 运算符具有特定的比较功能，这些功能不同于上表中的运算符。</span><span class="sxs-lookup"><span data-stu-id="db9b9-145">The `Is` operator, the `IsNot` operator, and the `Like` operator have specific comparison functionalities that differ from the operators in the preceding table.</span></span>

## <a name="comparing-numbers"></a><span data-ttu-id="db9b9-146">比较数字</span><span class="sxs-lookup"><span data-stu-id="db9b9-146">Comparing Numbers</span></span>

 <span data-ttu-id="db9b9-147">将类型的表达式与类型的表达式进行比较时 `Single` `Double` ， `Single` 表达式将转换为 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-147">When you compare an expression of type `Single` to one of type `Double`, the `Single` expression is converted to `Double`.</span></span> <span data-ttu-id="db9b9-148">此行为与 Visual Basic 6 中的行为相反。</span><span class="sxs-lookup"><span data-stu-id="db9b9-148">This behavior is opposite to the behavior found in Visual Basic 6.</span></span>

 <span data-ttu-id="db9b9-149">同样，将类型的表达式与 `Decimal` 或类型的表达式进行比较时 `Single` `Double` ， `Decimal` 表达式将转换为 `Single` 或 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-149">Similarly, when you compare an expression of type `Decimal` to an expression of type `Single` or `Double`, the `Decimal` expression is converted to `Single` or `Double`.</span></span> <span data-ttu-id="db9b9-150">对于 `Decimal` 表达式，小于 1e-28 的任何小数值都可能会丢失。</span><span class="sxs-lookup"><span data-stu-id="db9b9-150">For `Decimal` expressions, any fractional value less than 1E-28 might be lost.</span></span> <span data-ttu-id="db9b9-151">此类小数值损失可能导致两个值在不时比较为相等。</span><span class="sxs-lookup"><span data-stu-id="db9b9-151">Such fractional value loss may cause two values to compare as equal when they are not.</span></span> <span data-ttu-id="db9b9-152">出于此原因，在使用相等 (`=`) 比较两个浮点变量时，应格外小心。</span><span class="sxs-lookup"><span data-stu-id="db9b9-152">For this reason, you should take care when using equality (`=`) to compare two floating-point variables.</span></span> <span data-ttu-id="db9b9-153">更安全的做法是测试两个数字之差的绝对值是否小于可接受的小容差。</span><span class="sxs-lookup"><span data-stu-id="db9b9-153">It is safer to test whether the absolute value of the difference between the two numbers is less than a small acceptable tolerance.</span></span>

### <a name="floating-point-imprecision"></a><span data-ttu-id="db9b9-154">浮点不精确性</span><span class="sxs-lookup"><span data-stu-id="db9b9-154">Floating-point Imprecision</span></span>

 <span data-ttu-id="db9b9-155">使用浮点数时，请记住，它们在内存中不一定有精确的表示形式。</span><span class="sxs-lookup"><span data-stu-id="db9b9-155">When you work with floating-point numbers, keep in mind that they do not always have a precise representation in memory.</span></span> <span data-ttu-id="db9b9-156">这可能会导致某些操作产生意外结果，如值比较和 [Mod 运算符](mod-operator.md)。</span><span class="sxs-lookup"><span data-stu-id="db9b9-156">This could lead to unexpected results from certain operations, such as value comparison and the [Mod Operator](mod-operator.md).</span></span> <span data-ttu-id="db9b9-157">有关详细信息，请参阅 [数据类型疑难解答](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="db9b9-157">For more information, see [Troubleshooting Data Types](../../programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>

## <a name="comparing-strings"></a><span data-ttu-id="db9b9-158">比较字符串</span><span class="sxs-lookup"><span data-stu-id="db9b9-158">Comparing Strings</span></span>

 <span data-ttu-id="db9b9-159">在比较字符串时，将根据设置的字母顺序对字符串表达式进行计算 `Option Compare` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-159">When you compare strings, the string expressions are evaluated based on their alphabetical sort order, which depends on the `Option Compare` setting.</span></span>

 <span data-ttu-id="db9b9-160">`Option Compare Binary` 对从字符的内部二进制表示形式派生的排序顺序进行字符串比较。</span><span class="sxs-lookup"><span data-stu-id="db9b9-160">`Option Compare Binary` bases string comparisons on a sort order derived from the internal binary representations of the characters.</span></span> <span data-ttu-id="db9b9-161">排序顺序由代码页确定。</span><span class="sxs-lookup"><span data-stu-id="db9b9-161">The sort order is determined by the code page.</span></span> <span data-ttu-id="db9b9-162">下面的示例显示了一个典型的二进制排序顺序。</span><span class="sxs-lookup"><span data-stu-id="db9b9-162">The following example shows a typical binary sort order.</span></span>

 `A < B < E < Z < a < b < e < z < À < Ê < Ø < à < ê < ø`

 <span data-ttu-id="db9b9-163">`Option Compare Text` 基于不区分大小写的文本排序顺序对应用程序的区域设置进行字符串比较。</span><span class="sxs-lookup"><span data-stu-id="db9b9-163">`Option Compare Text` bases string comparisons on a case-insensitive, textual sort order determined by your application's locale.</span></span> <span data-ttu-id="db9b9-164">设置 `Option Compare Text` 和排序前面的示例中的字符时，将应用以下文本排序顺序：</span><span class="sxs-lookup"><span data-stu-id="db9b9-164">When you set `Option Compare Text` and sort the characters in the preceding example, the following text sort order applies:</span></span>

 `(A=a) < (À= à) < (B=b) < (E=e) < (Ê= ê) < (Ø = ø) < (Z=z)`

### <a name="locale-dependence"></a><span data-ttu-id="db9b9-165">区域设置依赖关系</span><span class="sxs-lookup"><span data-stu-id="db9b9-165">Locale Dependence</span></span>

 <span data-ttu-id="db9b9-166">设置时 `Option Compare Text` ，字符串比较的结果可能取决于应用程序运行所在的区域设置。</span><span class="sxs-lookup"><span data-stu-id="db9b9-166">When you set `Option Compare Text`, the result of a string comparison can depend on the locale in which the application is running.</span></span> <span data-ttu-id="db9b9-167">在一个区域设置中，两个字符的比较结果可能不相同，而在另一个区域中</span><span class="sxs-lookup"><span data-stu-id="db9b9-167">Two characters might compare as equal in one locale but not in another.</span></span> <span data-ttu-id="db9b9-168">如果使用字符串比较来做出重要决策（例如是否接受登录尝试），则应注意区域设置的敏感性。</span><span class="sxs-lookup"><span data-stu-id="db9b9-168">If you are using a string comparison to make important decisions, such as whether to accept an attempt to log on, you should be alert to locale sensitivity.</span></span> <span data-ttu-id="db9b9-169">请考虑设置 `Option Compare Binary` 或调用 <xref:Microsoft.VisualBasic.Strings.StrComp%2A> ，这会使区域设置生效。</span><span class="sxs-lookup"><span data-stu-id="db9b9-169">Consider either setting `Option Compare Binary` or calling the <xref:Microsoft.VisualBasic.Strings.StrComp%2A>, which takes the locale into account.</span></span>

## <a name="typeless-programming-with-relational-comparison-operators"></a><span data-ttu-id="db9b9-170">用关系比较运算符进行无方式编程</span><span class="sxs-lookup"><span data-stu-id="db9b9-170">Typeless Programming with Relational Comparison Operators</span></span>

 <span data-ttu-id="db9b9-171">不允许在下使用带有表达式的关系比较运算符 `Object` `Option Strict On` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-171">The use of relational comparison operators with `Object` expressions is not allowed under `Option Strict On`.</span></span> <span data-ttu-id="db9b9-172">如果 `Option Strict` 为 `Off` ，并且 `expression1` 或 `expression2` 是 `Object` 表达式，则运行时类型确定如何比较它们。</span><span class="sxs-lookup"><span data-stu-id="db9b9-172">When `Option Strict` is `Off`, and either `expression1` or `expression2` is an `Object` expression, the run-time types determine how they are compared.</span></span> <span data-ttu-id="db9b9-173">下表显示了如何比较表达式和比较的结果，具体取决于操作数的运行时类型。</span><span class="sxs-lookup"><span data-stu-id="db9b9-173">The following table shows how the expressions are compared and the result from the comparison, depending on the runtime type of the operands.</span></span>

|<span data-ttu-id="db9b9-174">如果操作数为</span><span class="sxs-lookup"><span data-stu-id="db9b9-174">If operands are</span></span>|<span data-ttu-id="db9b9-175">比较是</span><span class="sxs-lookup"><span data-stu-id="db9b9-175">Comparison is</span></span>|
|---------------------|-------------------|
|<span data-ttu-id="db9b9-176">全部 `String`</span><span class="sxs-lookup"><span data-stu-id="db9b9-176">Both `String`</span></span>|<span data-ttu-id="db9b9-177">基于字符串排序特性的排序比较。</span><span class="sxs-lookup"><span data-stu-id="db9b9-177">Sort comparison based on string sorting characteristics.</span></span>|
|<span data-ttu-id="db9b9-178">均为数值</span><span class="sxs-lookup"><span data-stu-id="db9b9-178">Both numeric</span></span>|<span data-ttu-id="db9b9-179">转换为 `Double` 数值比较的对象。</span><span class="sxs-lookup"><span data-stu-id="db9b9-179">Objects converted to `Double`, numeric comparison.</span></span>|
|<span data-ttu-id="db9b9-180">一个数字和一个 `String`</span><span class="sxs-lookup"><span data-stu-id="db9b9-180">One numeric and one `String`</span></span>|<span data-ttu-id="db9b9-181">`String`转换为 `Double` 并执行数值比较。</span><span class="sxs-lookup"><span data-stu-id="db9b9-181">The `String` is converted to a `Double` and numeric comparison is performed.</span></span> <span data-ttu-id="db9b9-182">如果 `String` 无法转换为 `Double` ， <xref:System.InvalidCastException> 则会引发。</span><span class="sxs-lookup"><span data-stu-id="db9b9-182">If the `String` cannot be converted to `Double`, an <xref:System.InvalidCastException> is thrown.</span></span>|
|<span data-ttu-id="db9b9-183">其中一个或两个都是引用类型，而不是 `String`</span><span class="sxs-lookup"><span data-stu-id="db9b9-183">Either or both are reference types other than `String`</span></span>|<span data-ttu-id="db9b9-184">引发 <xref:System.InvalidCastException>。</span><span class="sxs-lookup"><span data-stu-id="db9b9-184">An <xref:System.InvalidCastException> is thrown.</span></span>|

 <span data-ttu-id="db9b9-185">数值比较视为 `Nothing` 0。</span><span class="sxs-lookup"><span data-stu-id="db9b9-185">Numeric comparisons treat `Nothing` as 0.</span></span> <span data-ttu-id="db9b9-186">字符串比较视为 `Nothing` `""` (空字符串) 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-186">String comparisons treat `Nothing` as `""` (an empty string).</span></span>

## <a name="overloading"></a><span data-ttu-id="db9b9-187">重载</span><span class="sxs-lookup"><span data-stu-id="db9b9-187">Overloading</span></span>

 <span data-ttu-id="db9b9-188">关系比较运算符 (`<` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-188">The relational comparison operators (`<`.</span></span> <span data-ttu-id="db9b9-189">`<=`、 `>` 、 `>=` 、 `=` 、 `<>`) 可以进行 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义它们的行为。</span><span class="sxs-lookup"><span data-stu-id="db9b9-189">`<=`, `>`, `>=`, `=`, `<>`) can be *overloaded*, which means that a class or structure can redefine their behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="db9b9-190">如果你的代码在此类或结构上使用这些运算符中的任何一种，请确保了解重定义的行为。</span><span class="sxs-lookup"><span data-stu-id="db9b9-190">If your code uses any of these operators on such a class or structure, be sure you understand the redefined behavior.</span></span> <span data-ttu-id="db9b9-191">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="db9b9-191">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>

 <span data-ttu-id="db9b9-192">请注意， [= 运算符](assignment-operator.md) 只能作为关系比较运算符重载，而不能作为赋值运算符重载。</span><span class="sxs-lookup"><span data-stu-id="db9b9-192">Notice that the [= Operator](assignment-operator.md) can be overloaded only as a relational comparison operator, not as an assignment operator.</span></span>

## <a name="example"></a><span data-ttu-id="db9b9-193">示例</span><span class="sxs-lookup"><span data-stu-id="db9b9-193">Example</span></span>

 <span data-ttu-id="db9b9-194">下面的示例演示了用于比较表达式的关系比较运算符的各种用法。</span><span class="sxs-lookup"><span data-stu-id="db9b9-194">The following example shows various uses of relational comparison operators, which you use to compare expressions.</span></span> <span data-ttu-id="db9b9-195">关系比较运算符返回一个 `Boolean` 结果，该结果表示指定表达式的计算结果是否为 `True` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-195">Relational comparison operators return a `Boolean` result that represents whether or not the stated expression evaluates to `True`.</span></span> <span data-ttu-id="db9b9-196">将 `>` and `<` 运算符应用到字符串时，将使用标准的按字母顺序排序的字符串进行比较。</span><span class="sxs-lookup"><span data-stu-id="db9b9-196">When you apply the `>` and `<` operators to strings, the comparison is made using the normal alphabetical sorting order of the strings.</span></span> <span data-ttu-id="db9b9-197">此顺序可能取决于区域设置。</span><span class="sxs-lookup"><span data-stu-id="db9b9-197">This order can be dependent on your locale setting.</span></span> <span data-ttu-id="db9b9-198">排序是否区分大小写取决于 " [选项比较](../statements/option-compare-statement.md) " 设置。</span><span class="sxs-lookup"><span data-stu-id="db9b9-198">Whether the sort is case-sensitive or not depends on the [Option Compare](../statements/option-compare-statement.md) setting.</span></span>

 [!code-vb[VbVbalrOperators#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#1)]

 <span data-ttu-id="db9b9-199">在前面的示例中，第一个比较返回， `False` 其余比较返回 `True` 。</span><span class="sxs-lookup"><span data-stu-id="db9b9-199">In the preceding example, the first comparison returns `False` and the remaining comparisons return `True`.</span></span>

## <a name="see-also"></a><span data-ttu-id="db9b9-200">请参阅</span><span class="sxs-lookup"><span data-stu-id="db9b9-200">See also</span></span>

- <xref:System.InvalidCastException>
- [<span data-ttu-id="db9b9-201">= 运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-201">= Operator</span></span>](assignment-operator.md)
- [<span data-ttu-id="db9b9-202">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="db9b9-202">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="db9b9-203">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="db9b9-203">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="db9b9-204">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="db9b9-204">Troubleshooting Data Types</span></span>](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="db9b9-205">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="db9b9-205">Comparison Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/comparison-operators.md)

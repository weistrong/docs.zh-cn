---
title: '基于运行时状态的查询 (Visual Basic) '
description: 描述您的代码可用于根据运行时状态进行动态查询的各种技术，方法是改变 LINQ 方法调用或传入这些方法的表达式树。
ms.date: 02/14/2021
ms.assetid: 16278787-7532-4b65-98b2-7a412406c4ee
ms.openlocfilehash: c9f57950b2c26c0cca798ab632da90bf9f6c519a
ms.sourcegitcommit: f0fc5db7bcbf212e46933e9cf2d555bb82666141
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "100584850"
---
# <a name="querying-based-on-runtime-state-visual-basic"></a>基于运行时状态的查询 (Visual Basic) 

考虑 <xref:System.Linq.IQueryable> 针对数据源定义 [T) 的或 IQueryable (的 ](<xref:System.Linq.IQueryable%601>) 代码：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Initialize":::

每次运行此代码时，都将执行相同的查询。 这通常不是很有用，因为你可能希望代码根据运行时的条件执行不同的查询。 本文介绍如何根据运行时状态执行不同的查询。

## <a name="iqueryable--iqueryableof-t-and-expression-trees"></a>T) 和表达式树的 IQueryable/IQueryable (

基本上， <xref:System.Linq.IQueryable> 有两个组件：

* <xref:System.Linq.IQueryable.Expression>&mdash;当前查询的组件的与语言和数据源无关的表示形式，以表达式树的形式表示。
* <xref:System.Linq.IQueryable.Provider>&mdash;LINQ 提供程序的实例，它知道如何将当前查询具体化为一个值或一组值。

在动态查询上下文中，提供程序通常会保持不变;查询的表达式树将不同于查询的表达式树。

表达式树是不可变的;如果需要不同的表达式树 &mdash; ，因而需要不同的查询 &mdash; ，则需要将现有表达式树转换为新的表达式树，从而将其转换为新的 <xref:System.Linq.IQueryable> 。

以下各节介绍了不同的查询方法，以响应运行时状态：

- 使用表达式树中的运行时状态
- 调用其他 LINQ 方法
- 改变传入 LINQ 方法的表达式树
- 使用工厂方法在 TDelegate) 表达式树构造[表达式 (](xref:System.Linq.Expressions.Expression%601)<xref:System.Linq.Expressions.Expression>
- 将方法调用节点添加到 <xref:System.Linq.IQueryable> 的表达式树
- 构造字符串，并使用 [动态 LINQ 库](https://dynamic-linq.net/)

## <a name="use-runtime-state-from-within-the-expression-tree"></a>使用表达式树中的运行时状态

假设 LINQ 提供程序支持，最简单的查询方式是通过关闭的变量直接在查询中引用运行时状态，如 `length` 以下代码示例中所示：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Runtime_state_from_within_expression_tree":::

内部表达式树 &mdash; ，因此未修改查询 &mdash; ; 查询只返回不同的值，因为的值已 `length` 更改。

## <a name="call-additional-linq-methods"></a>调用其他 LINQ 方法

通常， [中的内置 LINQ 方法](https://github.com/dotnet/runtime/blob/master/src/libraries/System.Linq.Queryable/src/System/Linq/Queryable.cs) <xref:System.Linq.Queryable> 执行两个步骤：

* 在表示方法调用的中包装当前的表达式树 <xref:System.Linq.Expressions.MethodCallExpression> 。
* 将包装的表达式树传递回提供程序，以便通过提供程序的方法返回值 <xref:System.Linq.IQueryProvider.Execute%2A?displayProperty=nameWithType> ; 或通过方法返回翻译的查询对象 <xref:System.Linq.IQueryProvider.CreateQuery%2A?displayProperty=nameWithType> 。

可以将原始查询替换为返回 T) 方法的 [IQueryable (的 ](xref:System.Linq.IQueryable%601)结果，以获取新的查询。 您可以根据运行时状态执行此操作，如以下示例中所示：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Added_method_calls":::

## <a name="vary-the-expression-tree-passed-into-the-linq-methods"></a>改变传入 LINQ 方法的表达式树

可以将不同的表达式传入 LINQ 方法，具体取决于运行时状态：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Varying_expressions":::

你可能还希望使用第三方库（如 [LinqKit](http://www.albahari.com/nutshell/linqkit.aspx)的 [PredicateBuilder](http://www.albahari.com/nutshell/predicatebuilder.aspx)）来编写各种子表达式：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Compose_expression":::

## <a name="construct-expression-trees-and-queries-using-factory-methods"></a>使用工厂方法构造表达式树和查询

在所有示例中，在此之前，我们在编译时已知元素类型， &mdash; `String` &mdash; 因此是查询的类型 &mdash; `IQueryable(Of String)` 。 可能需要将组件添加到任何元素类型的查询中，或者根据元素类型添加不同的组件。 您可以使用中的工厂方法从头开始创建表达式树，从而在 <xref:System.Linq.Expressions.Expression?displayProperty=fullName> 运行时将表达式定制为特定的元素类型。

### <a name="constructing-an-expressionof-tdelegate"></a>构造 [TDelegate 的表达式 () ](xref:System.Linq.Expressions.Expression%601)

当构造要传入其中一个 LINQ 方法的表达式时，实际上就是构造一个 [ (为 TDelegate) 的表达式 ](xref:System.Linq.Expressions.Expression%601)实例，其中 `TDelegate` 是某个委托类型，如 `Func(Of String, Boolean)` 、 `Action` 或自定义委托类型。

[TDelegate) ) 的 Expression (](xref:System.Linq.Expressions.Expression%601) 继承自 <xref:System.Linq.Expressions.LambdaExpression> ，这表示完整的 lambda 表达式，如下所示：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Compiler_generated":::

<xref:System.Linq.Expressions.LambdaExpression>具有两个组件：

* &mdash; `(x As String)` &mdash; 由属性表示的 <xref:System.Linq.Expressions.LambdaExpression.Parameters> 参数列表
* &mdash; `x.StartsWith("a")` &mdash; 由属性表示的正文 <xref:System.Linq.Expressions.LambdaExpression.Body> 。

构造 [表达式 (TDelegate) ](xref:System.Linq.Expressions.Expression%601) 的基本步骤如下所示：

* <xref:System.Linq.Expressions.ParameterExpression>使用工厂方法为每个参数定义对象， (如果 lambda 表达式中有任何) <xref:System.Linq.Expressions.Expression.Parameter%2A> 。

    :::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Factory_method_parameter":::

* <xref:System.Linq.Expressions.LambdaExpression> <xref:System.Linq.Expressions.ParameterExpression> (使用你定义的) 和中的工厂方法构造的正文 <xref:System.Linq.Expressions.Expression> 。 例如， `x.StartsWith("a")` 可以如下所示构造表示的表达式：

    :::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Factory_method_body":::

* 使用适当的工厂方法重载，在 [TDelegate) ](xref:System.Linq.Expressions.Expression%601)的编译时类型化表达式中包装参数和正文 (<xref:System.Linq.Expressions.Expression.Lambda%2A> ：

    :::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Factory_method_lambda":::

以下各节介绍了一种方案，在该方案中，你可能想要构造 [TDelegate) 的表达式 (](xref:System.Linq.Expressions.Expression%601) 以传入 LINQ 方法，并提供有关如何使用工厂方法执行此操作的完整示例。

### <a name="scenario"></a>方案

假设您有多个实体类型：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Entities.vb":::

对于这些实体类型中的任何一种，你都需要仅筛选和返回在其中一个字段内具有给定文本的实体 `string` 。 对于 `Person` ，你需要搜索 `FirstName` 和 `LastName` 属性：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="PersonsQry":::

但对于 `Car` ，只需搜索 `Model` 属性：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="CarsQry":::

尽管可以为编写一个自定义函数， `IQueryable(Of Person)` 而另一个用于 `IQueryable(Of Car)` ，但以下函数会将此筛选添加到任何现有查询，而不考虑特定的元素类型。

### <a name="example"></a>示例

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Factory_methods_expression_of_tdelegate":::

由于 `TextFilter` 函数采用并返回 [T) 的 IQueryable (](xref:System.Linq.IQueryable%601) (而不只是 <xref:System.Linq.IQueryable>) ，因此您可以在文本筛选器后添加更多的编译时类型的查询元素。

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Factory_methods_expression_of_tdelegate_usage":::

## <a name="add-method-call-nodes-to-the-xrefsystemlinqiqueryables-expression-tree"></a>向的表达式树中添加方法调用节点 <xref:System.Linq.IQueryable>

如果有 <xref:System.Linq.IQueryable> 而不是 [ (T) 的 IQueryable ](xref:System.Linq.IQueryable%601)，则不能直接调用泛型 LINQ 方法。 一种替代方法是生成上面的内部表达式树，并使用反射来调用适当的 LINQ 方法，同时在表达式树中传递。

还可以通过在中包装整个树（ <xref:System.Linq.Expressions.MethodCallExpression> 表示对 LINQ 方法的调用）来复制 linq 方法的功能：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Factory_methods_lambdaexpression":::

请注意，在这种情况下，你没有编译时 `T` 泛型占位符，因此你将使用 <xref:System.Linq.Expressions.Expression.Lambda%2A> 不需要编译时类型信息的重载，这将生成 <xref:System.Linq.Expressions.LambdaExpression> 而不是 [表达式 (TDelegate) ](xref:System.Linq.Expressions.Expression%601)。

## <a name="the-dynamic-linq-library"></a>动态 LINQ 库

使用工厂方法构造表达式树比较复杂;编写字符串更为容易。 [动态 linq 库](https://dynamic-linq.net/)公开了一组扩展方法，这些方法与中 <xref:System.Linq.IQueryable> 的标准 LINQ 方法相对应 <xref:System.Linq.Queryable> ，后者接受[特殊语法](https://dynamic-linq.net/expression-language)而不是表达式树中的字符串。 库从字符串生成相应的表达式树，并可返回转换后的结果 <xref:System.Linq.IQueryable> 。

例如，前面的示例 (包括表达式树构造) 可以重写，如下所示：

:::code language="vb" source="../../../../../samples/snippets/visualbasic/programming-guide/dynamic-linq-expression-trees/Program.vb" id="Dynamic_linq":::

## <a name="see-also"></a>另请参阅

- [表达式树 (Visual Basic)](index.md)
- [如何：执行表达式树 (Visual Basic)](how-to-execute-expression-trees.md)

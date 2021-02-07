---
description: '了解详细信息： Where 子句 (Visual Basic) '
title: Where 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryWhere
helpviewer_keywords:
- Where statement [Visual Basic]
- queries [Visual Basic], Where
- Where clause [Visual Basic]
ms.assetid: 48b5c2c5-3181-429c-8545-894296798c89
ms.openlocfilehash: 11f9a7e586a1fdea826df4fb34a7227747c8cebd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730312"
---
# <a name="where-clause-visual-basic"></a><span data-ttu-id="c8900-103">Where 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c8900-103">Where Clause (Visual Basic)</span></span>

<span data-ttu-id="c8900-104">指定查询的筛选条件。</span><span class="sxs-lookup"><span data-stu-id="c8900-104">Specifies the filtering condition for a query.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8900-105">语法</span><span class="sxs-lookup"><span data-stu-id="c8900-105">Syntax</span></span>  
  
```vb  
Where condition  
```  
  
## <a name="parts"></a><span data-ttu-id="c8900-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="c8900-106">Parts</span></span>  

 `condition`  
 <span data-ttu-id="c8900-107">必需。</span><span class="sxs-lookup"><span data-stu-id="c8900-107">Required.</span></span> <span data-ttu-id="c8900-108">确定集合中当前项的值是否包含在输出集合中的表达式。</span><span class="sxs-lookup"><span data-stu-id="c8900-108">An expression that determines whether the values for the current item in the collection are included in the output collection.</span></span> <span data-ttu-id="c8900-109">表达式的计算结果必须是值 `Boolean` 或值的等效值 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="c8900-109">The expression must evaluate to a `Boolean` value or the equivalent of a `Boolean` value.</span></span> <span data-ttu-id="c8900-110">如果条件的计算结果为 `True` ，则元素将包含在查询结果中; 否则，将从查询结果中排除元素。</span><span class="sxs-lookup"><span data-stu-id="c8900-110">If the condition evaluates to `True`, the element is included in the query result; otherwise, the element is excluded from the query result.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c8900-111">备注</span><span class="sxs-lookup"><span data-stu-id="c8900-111">Remarks</span></span>  

 <span data-ttu-id="c8900-112">使用 `Where` 子句可以通过仅选择符合特定条件的元素来筛选查询数据。</span><span class="sxs-lookup"><span data-stu-id="c8900-112">The `Where` clause enables you to filter query data by selecting only elements that meet certain criteria.</span></span> <span data-ttu-id="c8900-113">其值导致 `Where` 子句计算结果的元素 `True` 包含在查询结果中，其他元素将被排除。</span><span class="sxs-lookup"><span data-stu-id="c8900-113">Elements whose values cause the `Where` clause to evaluate to `True` are included in the query result; other elements are excluded.</span></span> <span data-ttu-id="c8900-114">子句中使用的表达式的 `Where` 计算结果必须为或的 `Boolean` 等效项 `Boolean` ，例如， `False` 如果其值为零，则计算结果为。</span><span class="sxs-lookup"><span data-stu-id="c8900-114">The expression that is used in a `Where` clause must evaluate to a `Boolean` or the equivalent of a `Boolean`, such as an Integer that evaluates to `False` when its value is zero.</span></span> <span data-ttu-id="c8900-115">您可以 `Where` 通过使用逻辑运算符（例如、、、 `And` `Or` `AndAlso` `OrElse` 、 `Is` 和 `IsNot` ）组合子句中的多个表达式。</span><span class="sxs-lookup"><span data-stu-id="c8900-115">You can combine multiple expressions in a `Where` clause by using logical operators such as `And`, `Or`, `AndAlso`, `OrElse`, `Is`, and `IsNot`.</span></span>  
  
 <span data-ttu-id="c8900-116">默认情况下，在访问查询表达式之前，不会对其进行计算（例如，当它们在循环中进行数据绑定或循环访问时） `For` 。</span><span class="sxs-lookup"><span data-stu-id="c8900-116">By default, query expressions are not evaluated until they are accessed—for example, when they are data-bound or iterated through in a `For` loop.</span></span> <span data-ttu-id="c8900-117">因此，在 `Where` 访问查询之前，不会计算子句的值。</span><span class="sxs-lookup"><span data-stu-id="c8900-117">As a result, the `Where` clause is not evaluated until the query is accessed.</span></span> <span data-ttu-id="c8900-118">如果在子句中使用的查询外部存在值 `Where` ，请确保在执行查询时在子句中使用相应的值 `Where` 。</span><span class="sxs-lookup"><span data-stu-id="c8900-118">If you have values external to the query that are used in the `Where` clause, ensure that the appropriate value is used in the `Where` clause at the time the query is executed.</span></span> <span data-ttu-id="c8900-119">有关查询执行的详细信息，请参阅 [编写第一个 LINQ 查询](../../programming-guide/concepts/linq/writing-your-first-linq-query.md)。</span><span class="sxs-lookup"><span data-stu-id="c8900-119">For more information about query execution, see [Writing Your First LINQ Query](../../programming-guide/concepts/linq/writing-your-first-linq-query.md).</span></span>  
  
 <span data-ttu-id="c8900-120">可以在子句中调用函数 `Where` ，以对集合中的当前元素中的值执行计算或运算。</span><span class="sxs-lookup"><span data-stu-id="c8900-120">You can call functions within a `Where` clause to perform a calculation or operation on a value from the current element in the collection.</span></span> <span data-ttu-id="c8900-121">如果在子句中调用函数，则 `Where` 可能会导致查询在定义时立即执行，而不是在访问时执行。</span><span class="sxs-lookup"><span data-stu-id="c8900-121">Calling a function in a `Where` clause can cause the query to be executed immediately when it is defined instead of when it is accessed.</span></span> <span data-ttu-id="c8900-122">有关查询执行的详细信息，请参阅 [编写第一个 LINQ 查询](../../programming-guide/concepts/linq/writing-your-first-linq-query.md)。</span><span class="sxs-lookup"><span data-stu-id="c8900-122">For more information about query execution, see [Writing Your First LINQ Query](../../programming-guide/concepts/linq/writing-your-first-linq-query.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c8900-123">示例</span><span class="sxs-lookup"><span data-stu-id="c8900-123">Example</span></span>  

 <span data-ttu-id="c8900-124">下面的查询表达式使用 `From` 子句为 `cust` 集合中的每个对象声明一个范围变量 `Customer` `customers` 。</span><span class="sxs-lookup"><span data-stu-id="c8900-124">The following query expression uses a `From` clause to declare a range variable `cust` for each `Customer` object in the `customers` collection.</span></span> <span data-ttu-id="c8900-125">`Where`子句使用范围变量将输出限制为指定区域的客户。</span><span class="sxs-lookup"><span data-stu-id="c8900-125">The `Where` clause uses the range variable to restrict the output to customers from the specified region.</span></span> <span data-ttu-id="c8900-126">该 `For Each` 循环将在查询结果中显示每个客户的公司名称。</span><span class="sxs-lookup"><span data-stu-id="c8900-126">The `For Each` loop displays the company name for each customer in the query result.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#23)]  
  
## <a name="example"></a><span data-ttu-id="c8900-127">示例</span><span class="sxs-lookup"><span data-stu-id="c8900-127">Example</span></span>  

 <span data-ttu-id="c8900-128">下面的示例 `And` `Or` 在子句中使用和逻辑运算符 `Where` 。</span><span class="sxs-lookup"><span data-stu-id="c8900-128">The following example uses `And` and `Or` logical operators in the `Where` clause.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#31)]  
  
## <a name="see-also"></a><span data-ttu-id="c8900-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="c8900-129">See also</span></span>

- [<span data-ttu-id="c8900-130">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="c8900-130">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="c8900-131">查询</span><span class="sxs-lookup"><span data-stu-id="c8900-131">Queries</span></span>](index.md)
- [<span data-ttu-id="c8900-132">From 子句</span><span class="sxs-lookup"><span data-stu-id="c8900-132">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="c8900-133">Select 子句</span><span class="sxs-lookup"><span data-stu-id="c8900-133">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="c8900-134">For Each...Next 语句</span><span class="sxs-lookup"><span data-stu-id="c8900-134">For Each...Next Statement</span></span>](../statements/for-each-next-statement.md)

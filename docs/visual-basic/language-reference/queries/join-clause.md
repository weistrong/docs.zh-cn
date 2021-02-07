---
description: '详细了解： Join 子句 (Visual Basic) '
title: Join 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryJoinIn
- vb.QueryJoin
- vb.QueryJoinOn
helpviewer_keywords:
- queries [Visual Basic], Join
- Join statement [Visual Basic]
- Join clause [Visual Basic]
ms.assetid: 6dd37936-b27c-4e00-98ad-154b23f4de64
ms.openlocfilehash: 69d808e68a32b3f8799dabbbc8abc53acae42b57
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700437"
---
# <a name="join-clause-visual-basic"></a><span data-ttu-id="acd1c-103">Join 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="acd1c-103">Join Clause (Visual Basic)</span></span>

<span data-ttu-id="acd1c-104">将两个集合合并为单个集合。</span><span class="sxs-lookup"><span data-stu-id="acd1c-104">Combines two collections into a single collection.</span></span> <span data-ttu-id="acd1c-105">联接运算基于匹配键，并使用 `Equals` 运算符。</span><span class="sxs-lookup"><span data-stu-id="acd1c-105">The join operation is based on matching keys and uses the `Equals` operator.</span></span>

## <a name="syntax"></a><span data-ttu-id="acd1c-106">语法</span><span class="sxs-lookup"><span data-stu-id="acd1c-106">Syntax</span></span>

```vb
Join element In collection _
  [ joinClause _ ]
  [ groupJoinClause ... _ ]
On key1 Equals key2 [ And key3 Equals key4 [... ]
```

## <a name="parts"></a><span data-ttu-id="acd1c-107">组成部分</span><span class="sxs-lookup"><span data-stu-id="acd1c-107">Parts</span></span>

<span data-ttu-id="acd1c-108">`element`（必需）。</span><span class="sxs-lookup"><span data-stu-id="acd1c-108">`element` Required.</span></span> <span data-ttu-id="acd1c-109">要联接的集合的控件变量。</span><span class="sxs-lookup"><span data-stu-id="acd1c-109">The control variable for the collection being joined.</span></span>

`collection`  
<span data-ttu-id="acd1c-110">必需。</span><span class="sxs-lookup"><span data-stu-id="acd1c-110">Required.</span></span> <span data-ttu-id="acd1c-111">要与运算符左侧标识的集合组合的集合 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="acd1c-111">The collection to combine with the collection identified on the left side of the `Join` operator.</span></span> <span data-ttu-id="acd1c-112">`Join`子句可以嵌套在另一个 `Join` 子句或 `Group Join` 子句中。</span><span class="sxs-lookup"><span data-stu-id="acd1c-112">A `Join` clause can be nested in another `Join` clause, or in a `Group Join` clause.</span></span>

`joinClause`  
<span data-ttu-id="acd1c-113">可选。</span><span class="sxs-lookup"><span data-stu-id="acd1c-113">Optional.</span></span> <span data-ttu-id="acd1c-114">`Join`用于进一步优化查询的一个或多个其他子句。</span><span class="sxs-lookup"><span data-stu-id="acd1c-114">One or more additional `Join` clauses to further refine the query.</span></span>

`groupJoinClause`  
<span data-ttu-id="acd1c-115">可选。</span><span class="sxs-lookup"><span data-stu-id="acd1c-115">Optional.</span></span> <span data-ttu-id="acd1c-116">`Group Join`用于进一步优化查询的一个或多个其他子句。</span><span class="sxs-lookup"><span data-stu-id="acd1c-116">One or more additional `Group Join` clauses to further refine the query.</span></span>

<span data-ttu-id="acd1c-117">`key1` `Equals` `key2`</span><span class="sxs-lookup"><span data-stu-id="acd1c-117">`key1` `Equals` `key2`</span></span>  
<span data-ttu-id="acd1c-118">必需。</span><span class="sxs-lookup"><span data-stu-id="acd1c-118">Required.</span></span> <span data-ttu-id="acd1c-119">标识要联接的集合的键。</span><span class="sxs-lookup"><span data-stu-id="acd1c-119">Identifies keys for the collections being joined.</span></span> <span data-ttu-id="acd1c-120">必须使用 `Equals` 运算符来比较要联接的集合中的键。</span><span class="sxs-lookup"><span data-stu-id="acd1c-120">You must use the `Equals` operator to compare keys from the collections being joined.</span></span> <span data-ttu-id="acd1c-121">可以通过使用 `And` 运算符来标识多个键，从而组合联接条件。</span><span class="sxs-lookup"><span data-stu-id="acd1c-121">You can combine join conditions by using the `And` operator to identify multiple keys.</span></span> <span data-ttu-id="acd1c-122">`key1` 必须是位于运算符左侧的集合中 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="acd1c-122">`key1` must be from the collection on the left side of the `Join` operator.</span></span> <span data-ttu-id="acd1c-123">`key2` 必须来自运算符右侧的集合 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="acd1c-123">`key2` must be from the collection on the right side of the `Join` operator.</span></span>

<span data-ttu-id="acd1c-124">联接条件中使用的键可以是包含集合中多个项的表达式。</span><span class="sxs-lookup"><span data-stu-id="acd1c-124">The keys used in the join condition can be expressions that include more than one item from the collection.</span></span> <span data-ttu-id="acd1c-125">但是，每个键表达式只能包含其各自集合中的项。</span><span class="sxs-lookup"><span data-stu-id="acd1c-125">However, each key expression can contain only items from its respective collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="acd1c-126">备注</span><span class="sxs-lookup"><span data-stu-id="acd1c-126">Remarks</span></span>

<span data-ttu-id="acd1c-127">`Join`子句组合了两个集合，这些集合基于要联接的集合中的匹配键值。</span><span class="sxs-lookup"><span data-stu-id="acd1c-127">The `Join` clause combines two collections based on matching key values from the collections being joined.</span></span> <span data-ttu-id="acd1c-128">生成的集合可以包含运算符左侧标识的集合中的任何值组合 `Join` 和子句中标识的集合 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="acd1c-128">The resulting collection can contain any combination of values from the collection identified on the left side of the `Join` operator and the collection identified in the `Join` clause.</span></span> <span data-ttu-id="acd1c-129">查询将只返回满足运算符指定的条件的结果 `Equals` 。</span><span class="sxs-lookup"><span data-stu-id="acd1c-129">The query will return only results for which the condition specified by the `Equals` operator is met.</span></span> <span data-ttu-id="acd1c-130">这等效于 `INNER JOIN` SQL 中的。</span><span class="sxs-lookup"><span data-stu-id="acd1c-130">This is equivalent to an `INNER JOIN` in SQL.</span></span>

<span data-ttu-id="acd1c-131">您可以 `Join` 在查询中使用多个子句，以将两个或多个集合联接到一个集合中。</span><span class="sxs-lookup"><span data-stu-id="acd1c-131">You can use multiple `Join` clauses in a query to join two or more collections into a single collection.</span></span>

<span data-ttu-id="acd1c-132">您可以执行隐式联接以组合集合，而不使用 `Join` 子句。</span><span class="sxs-lookup"><span data-stu-id="acd1c-132">You can perform an implicit join to combine collections without the `Join` clause.</span></span> <span data-ttu-id="acd1c-133">为此，请 `In` 在子句中包含多个子句， `From` 并指定一个用于 `Where` 标识要用于联接的键的子句。</span><span class="sxs-lookup"><span data-stu-id="acd1c-133">To do this, include multiple `In` clauses in your `From` clause and specify a `Where` clause that identifies the keys that you want to use for the join.</span></span>

<span data-ttu-id="acd1c-134">可以使用子句将 `Group Join` 集合合并为单个分层集合。</span><span class="sxs-lookup"><span data-stu-id="acd1c-134">You can use the `Group Join` clause to combine collections into a single hierarchical collection.</span></span> <span data-ttu-id="acd1c-135">这类似于 `LEFT OUTER JOIN` SQL 中的。</span><span class="sxs-lookup"><span data-stu-id="acd1c-135">This is like a `LEFT OUTER JOIN` in SQL.</span></span>

## <a name="example"></a><span data-ttu-id="acd1c-136">示例</span><span class="sxs-lookup"><span data-stu-id="acd1c-136">Example</span></span>

<span data-ttu-id="acd1c-137">下面的代码示例将执行隐式联接，以将客户列表与订单组合在一起。</span><span class="sxs-lookup"><span data-stu-id="acd1c-137">The following code example performs an implicit join to combine a list of customers with their orders.</span></span>

[!code-vb[VbSimpleQuerySamples#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#13)]

## <a name="example"></a><span data-ttu-id="acd1c-138">示例</span><span class="sxs-lookup"><span data-stu-id="acd1c-138">Example</span></span>

<span data-ttu-id="acd1c-139">下面的代码示例使用子句联接两个集合 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="acd1c-139">The following code example joins two collections by using the `Join` clause.</span></span>

[!code-vb[VbSimpleQuerySamples#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples2.vb#12)]

<span data-ttu-id="acd1c-140">此示例将生成与下面类似的输出：</span><span class="sxs-lookup"><span data-stu-id="acd1c-140">This example will produce output similar to the following:</span></span>

`winlogon (968), Windows Logon`

`explorer (2424), File Explorer`

`cmd (5136), Command Window`

## <a name="example"></a><span data-ttu-id="acd1c-141">示例</span><span class="sxs-lookup"><span data-stu-id="acd1c-141">Example</span></span>

<span data-ttu-id="acd1c-142">下面的代码示例通过使用 `Join` 具有两个键列的子句来联接两个集合。</span><span class="sxs-lookup"><span data-stu-id="acd1c-142">The following code example joins two collections by using the `Join` clause with two key columns.</span></span>

[!code-vb[VbSimpleQuerySamples#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples3.vb#17)]

<span data-ttu-id="acd1c-143">该示例将生成类似于以下内容的输出：</span><span class="sxs-lookup"><span data-stu-id="acd1c-143">The example will produce output similar to the following:</span></span>

`winlogon (968), Windows Logon, Priority = 13`

`cmd (700), Command Window, Priority = 8`

`explorer (2424), File Explorer, Priority = 8`

## <a name="see-also"></a><span data-ttu-id="acd1c-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="acd1c-144">See also</span></span>

- [<span data-ttu-id="acd1c-145">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="acd1c-145">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="acd1c-146">查询</span><span class="sxs-lookup"><span data-stu-id="acd1c-146">Queries</span></span>](index.md)
- [<span data-ttu-id="acd1c-147">Select 子句</span><span class="sxs-lookup"><span data-stu-id="acd1c-147">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="acd1c-148">From 子句</span><span class="sxs-lookup"><span data-stu-id="acd1c-148">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="acd1c-149">Group Join 子句</span><span class="sxs-lookup"><span data-stu-id="acd1c-149">Group Join Clause</span></span>](group-join-clause.md)
- [<span data-ttu-id="acd1c-150">Where 子句</span><span class="sxs-lookup"><span data-stu-id="acd1c-150">Where Clause</span></span>](where-clause.md)

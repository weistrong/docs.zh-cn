---
description: '了解更多相关信息：将数据类型转换 (Visual Basic) '
title: 转换数据类型
ms.date: 07/20/2015
ms.assetid: 9b0cf1ab-de48-4c6e-9f00-05b40fade46e
ms.openlocfilehash: 7650f5d5d6f727b7815b9dd2de8a565e27fa18d9
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100428709"
---
# <a name="converting-data-types-visual-basic"></a><span data-ttu-id="59719-103">将数据类型转换 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="59719-103">Converting Data Types (Visual Basic)</span></span>

<span data-ttu-id="59719-104">转换方法可更改输入对象的类型。</span><span class="sxs-lookup"><span data-stu-id="59719-104">Conversion methods change the type of input objects.</span></span>

 <span data-ttu-id="59719-105">LINQ 查询中的转换运算可用于各种应用程序。</span><span class="sxs-lookup"><span data-stu-id="59719-105">Conversion operations in LINQ queries are useful in a variety of applications.</span></span> <span data-ttu-id="59719-106">下面是一些示例：</span><span class="sxs-lookup"><span data-stu-id="59719-106">The following are some examples:</span></span>

- <span data-ttu-id="59719-107"><xref:System.Linq.Enumerable.AsEnumerable%2A?displayProperty=nameWithType> 方法可用于隐藏类型的标准查询运算符自定义实现。</span><span class="sxs-lookup"><span data-stu-id="59719-107">The <xref:System.Linq.Enumerable.AsEnumerable%2A?displayProperty=nameWithType> method can be used to hide a type's custom implementation of a standard query operator.</span></span>

- <span data-ttu-id="59719-108"><xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType> 方法可用于为 LINQ 查询启用非参数化集合。</span><span class="sxs-lookup"><span data-stu-id="59719-108">The <xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType> method can be used to enable non-parameterized collections for LINQ querying.</span></span>

- <span data-ttu-id="59719-109"><xref:System.Linq.Enumerable.ToArray%2A?displayProperty=nameWithType>、<xref:System.Linq.Enumerable.ToDictionary%2A?displayProperty=nameWithType>、<xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType> 和 <xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType> 方法可用于强制执行即时的查询，而不是将其推迟到枚举该查询时。</span><span class="sxs-lookup"><span data-stu-id="59719-109">The <xref:System.Linq.Enumerable.ToArray%2A?displayProperty=nameWithType>, <xref:System.Linq.Enumerable.ToDictionary%2A?displayProperty=nameWithType>, <xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType>, and <xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType> methods can be used to force immediate query execution instead of deferring it until the query is enumerated.</span></span>

## <a name="methods"></a><span data-ttu-id="59719-110">方法</span><span class="sxs-lookup"><span data-stu-id="59719-110">Methods</span></span>

<span data-ttu-id="59719-111">下表列出了执行数据类型转换的标准查询运算符方法。</span><span class="sxs-lookup"><span data-stu-id="59719-111">The following table lists the standard query operator methods that perform data-type conversions.</span></span>

<span data-ttu-id="59719-112">本表中名称以“As”开头的转换方法可更改源集合的静态类型，但不对其进行枚举。</span><span class="sxs-lookup"><span data-stu-id="59719-112">The conversion methods in this table whose names start with "As" change the static type of the source collection but do not enumerate it.</span></span> <span data-ttu-id="59719-113">名称以“To”开头的方法可枚举源集合，并将项放入相应的集合类型。</span><span class="sxs-lookup"><span data-stu-id="59719-113">The methods whose names start with "To" enumerate the source collection and put the items into the corresponding collection type.</span></span>

|<span data-ttu-id="59719-114">方法名</span><span class="sxs-lookup"><span data-stu-id="59719-114">Method Name</span></span>|<span data-ttu-id="59719-115">描述</span><span class="sxs-lookup"><span data-stu-id="59719-115">Description</span></span>|<span data-ttu-id="59719-116">Visual Basic 查询表达式语法</span><span class="sxs-lookup"><span data-stu-id="59719-116">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="59719-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="59719-117">More Information</span></span>|
|-----------------|-----------------|------------------------------------------|----------------------|
|<span data-ttu-id="59719-118">AsEnumerable</span><span class="sxs-lookup"><span data-stu-id="59719-118">AsEnumerable</span></span>|<span data-ttu-id="59719-119">返回类型化为 <xref:System.Collections.Generic.IEnumerable%601> 的输入。</span><span class="sxs-lookup"><span data-stu-id="59719-119">Returns the input typed as <xref:System.Collections.Generic.IEnumerable%601>.</span></span>|<span data-ttu-id="59719-120">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-120">Not applicable.</span></span>|<xref:System.Linq.Enumerable.AsEnumerable%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-121">AsQueryable</span><span class="sxs-lookup"><span data-stu-id="59719-121">AsQueryable</span></span>|<span data-ttu-id="59719-122">将（泛型）<xref:System.Collections.IEnumerable> 转换为（泛型）<xref:System.Linq.IQueryable>。</span><span class="sxs-lookup"><span data-stu-id="59719-122">Converts a (generic) <xref:System.Collections.IEnumerable> to a (generic) <xref:System.Linq.IQueryable>.</span></span>|<span data-ttu-id="59719-123">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-123">Not applicable.</span></span>|<xref:System.Linq.Queryable.AsQueryable%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-124">Cast</span><span class="sxs-lookup"><span data-stu-id="59719-124">Cast</span></span>|<span data-ttu-id="59719-125">将集合中的元素转换为指定类型。</span><span class="sxs-lookup"><span data-stu-id="59719-125">Casts the elements of a collection to a specified type.</span></span>|`From … As …`|<xref:System.Linq.Enumerable.Cast%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Cast%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-126">OfType</span><span class="sxs-lookup"><span data-stu-id="59719-126">OfType</span></span>|<span data-ttu-id="59719-127">根据其转换为指定类型的能力筛选值。</span><span class="sxs-lookup"><span data-stu-id="59719-127">Filters values, depending on their ability to be cast to a specified type.</span></span>|<span data-ttu-id="59719-128">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-128">Not applicable.</span></span>|<xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.OfType%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-129">ToArray</span><span class="sxs-lookup"><span data-stu-id="59719-129">ToArray</span></span>|<span data-ttu-id="59719-130">将集合转换为数组。</span><span class="sxs-lookup"><span data-stu-id="59719-130">Converts a collection to an array.</span></span> <span data-ttu-id="59719-131">此方法强制执行查询。</span><span class="sxs-lookup"><span data-stu-id="59719-131">This method forces query execution.</span></span>|<span data-ttu-id="59719-132">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-132">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToArray%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-133">ToDictionary</span><span class="sxs-lookup"><span data-stu-id="59719-133">ToDictionary</span></span>|<span data-ttu-id="59719-134">根据键选择器函数将元素放入 <xref:System.Collections.Generic.Dictionary%602>。</span><span class="sxs-lookup"><span data-stu-id="59719-134">Puts elements into a <xref:System.Collections.Generic.Dictionary%602> based on a key selector function.</span></span> <span data-ttu-id="59719-135">此方法强制执行查询。</span><span class="sxs-lookup"><span data-stu-id="59719-135">This method forces query execution.</span></span>|<span data-ttu-id="59719-136">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-136">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToDictionary%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-137">ToList</span><span class="sxs-lookup"><span data-stu-id="59719-137">ToList</span></span>|<span data-ttu-id="59719-138">将集合转换为 <xref:System.Collections.Generic.List%601>。</span><span class="sxs-lookup"><span data-stu-id="59719-138">Converts a collection to a <xref:System.Collections.Generic.List%601>.</span></span> <span data-ttu-id="59719-139">此方法强制执行查询。</span><span class="sxs-lookup"><span data-stu-id="59719-139">This method forces query execution.</span></span>|<span data-ttu-id="59719-140">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-140">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType>|
|<span data-ttu-id="59719-141">ToLookup</span><span class="sxs-lookup"><span data-stu-id="59719-141">ToLookup</span></span>|<span data-ttu-id="59719-142">根据键选择器函数将元素放入 <xref:System.Linq.Lookup%602>（一对多字典）。</span><span class="sxs-lookup"><span data-stu-id="59719-142">Puts elements into a <xref:System.Linq.Lookup%602> (a one-to-many dictionary) based on a key selector function.</span></span> <span data-ttu-id="59719-143">此方法强制执行查询。</span><span class="sxs-lookup"><span data-stu-id="59719-143">This method forces query execution.</span></span>|<span data-ttu-id="59719-144">不适用。</span><span class="sxs-lookup"><span data-stu-id="59719-144">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType>|

## <a name="query-expression-syntax-example"></a><span data-ttu-id="59719-145">查询表达式语法示例</span><span class="sxs-lookup"><span data-stu-id="59719-145">Query Expression Syntax Example</span></span>

<span data-ttu-id="59719-146">下面的代码示例使用 `From As` 子句将类型转换为子类型，然后访问仅在子类型上可用的成员。</span><span class="sxs-lookup"><span data-stu-id="59719-146">The following code example uses the `From As` clause to cast a type to a subtype before accessing a member that is available only on the subtype.</span></span>

```vb
Class Plant
    Public Property Name As String
End Class

Class CarnivorousPlant
    Inherits Plant
    Public Property TrapType As String
End Class

Sub Cast()

    Dim plants() As Plant = {
        New CarnivorousPlant With {.Name = "Venus Fly Trap", .TrapType = "Snap Trap"},
        New CarnivorousPlant With {.Name = "Pitcher Plant", .TrapType = "Pitfall Trap"},
        New CarnivorousPlant With {.Name = "Sundew", .TrapType = "Flypaper Trap"},
        New CarnivorousPlant With {.Name = "Waterwheel Plant", .TrapType = "Snap Trap"}}

    Dim query = From plant As CarnivorousPlant In plants
                Where plant.TrapType = "Snap Trap"
                Select plant

    Dim sb As New System.Text.StringBuilder()
    For Each plant In query
        sb.AppendLine(plant.Name)
    Next

    ' Display the results.
    MsgBox(sb.ToString())

    ' This code produces the following output:

    ' Venus Fly Trap
    ' Waterwheel Plant

End Sub
```

## <a name="see-also"></a><span data-ttu-id="59719-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="59719-147">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="59719-148">标准查询运算符概述 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="59719-148">Standard Query Operators Overview (Visual Basic)</span></span>](standard-query-operators-overview.md)
- [<span data-ttu-id="59719-149">From 子句</span><span class="sxs-lookup"><span data-stu-id="59719-149">From Clause</span></span>](../../../language-reference/queries/from-clause.md)
- [<span data-ttu-id="59719-150">如何：使用 LINQ (Visual Basic 查询 ArrayList) </span><span class="sxs-lookup"><span data-stu-id="59719-150">How to: Query an ArrayList with LINQ (Visual Basic)</span></span>](how-to-query-an-arraylist-with-linq.md)

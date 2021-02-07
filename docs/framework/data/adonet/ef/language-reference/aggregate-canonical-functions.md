---
description: 了解更多：聚合规范函数
title: 聚合规范函数
ms.date: 03/30/2017
ms.assetid: 3bcff826-ca90-41b3-a791-04d6ff0e5085
ms.openlocfilehash: e26888ac15553a592f7d2cb9b1a0941161115615
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697291"
---
# <a name="aggregate-canonical-functions"></a><span data-ttu-id="96d0a-103">聚合规范函数</span><span class="sxs-lookup"><span data-stu-id="96d0a-103">Aggregate Canonical Functions</span></span>

<span data-ttu-id="96d0a-104">聚合是缩减一系列输入值（例如，缩减为单个值）的表达式。</span><span class="sxs-lookup"><span data-stu-id="96d0a-104">Aggregates are expressions that reduce a series of input values into, for example, a single value.</span></span> <span data-ttu-id="96d0a-105">聚合通常与 SELECT 表达式的 GROUP BY 子句一起使用，对于可以使用聚合的位置存在一些约束。</span><span class="sxs-lookup"><span data-stu-id="96d0a-105">Aggregates are normally used in conjunction with the GROUP BY clause of the SELECT expression, and there are constraints on where they can be used.</span></span>

## <a name="aggregate-entity-sql-canonical-functions"></a><span data-ttu-id="96d0a-106">聚合实体 SQL 规范函数</span><span class="sxs-lookup"><span data-stu-id="96d0a-106">Aggregate Entity SQL canonical functions</span></span>

<span data-ttu-id="96d0a-107">下面是聚合实体 SQL 规范函数。</span><span class="sxs-lookup"><span data-stu-id="96d0a-107">The following are the aggregate Entity SQL canonical functions.</span></span>

### <a name="avgexpression"></a><span data-ttu-id="96d0a-108">Avg(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-108">Avg(expression)</span></span>

<span data-ttu-id="96d0a-109">返回非 null 值的平均值。</span><span class="sxs-lookup"><span data-stu-id="96d0a-109">Returns the average of the non-null values.</span></span>

<span data-ttu-id="96d0a-110">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-110">**Arguments**</span></span>

<span data-ttu-id="96d0a-111">`Int32`、、 `Int64` `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-111">An `Int32`, `Int64`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="96d0a-112">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-112">**Return Value**</span></span>

<span data-ttu-id="96d0a-113">的类型 `expression` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-113">The type of `expression`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-114">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-114">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_AVG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_avg)]
[!code-sql[DP EntityServices Concepts#EDM_AVG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_avg)]

### <a name="bigcountexpression"></a><span data-ttu-id="96d0a-115">BigCount(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-115">BigCount(expression)</span></span>

<span data-ttu-id="96d0a-116">返回包含 null 值和重复值的聚合的大小。</span><span class="sxs-lookup"><span data-stu-id="96d0a-116">Returns the size of the aggregate including null and duplicate values.</span></span>

<span data-ttu-id="96d0a-117">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-117">**Arguments**</span></span>

<span data-ttu-id="96d0a-118">任何类型。</span><span class="sxs-lookup"><span data-stu-id="96d0a-118">Any type.</span></span>

<span data-ttu-id="96d0a-119">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-119">**Return Value**</span></span>

<span data-ttu-id="96d0a-120">`Int64`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-120">An `Int64`.</span></span>

<span data-ttu-id="96d0a-121">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-121">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_BIGCOUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_bigcount)]
[!code-sql[DP EntityServices Concepts#EDM_BIGCOUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_bigcount)]

### <a name="countexpression"></a><span data-ttu-id="96d0a-122">Count(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-122">Count(expression)</span></span>

<span data-ttu-id="96d0a-123">返回包含 null 值和重复值的聚合的大小。</span><span class="sxs-lookup"><span data-stu-id="96d0a-123">Returns the size of the aggregate including null and duplicate values.</span></span>

<span data-ttu-id="96d0a-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-124">**Arguments**</span></span>

<span data-ttu-id="96d0a-125">任何类型。</span><span class="sxs-lookup"><span data-stu-id="96d0a-125">Any type.</span></span>

<span data-ttu-id="96d0a-126">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-126">**Return Value**</span></span>

<span data-ttu-id="96d0a-127">`Int32`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-127">An `Int32`.</span></span>

<span data-ttu-id="96d0a-128">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-128">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_COUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_count)]
[!code-sql[DP EntityServices Concepts#EDM_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_count)]

### <a name="maxexpression"></a><span data-ttu-id="96d0a-129">Max(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-129">Max(expression)</span></span>

<span data-ttu-id="96d0a-130">返回非 null 值的最大值。</span><span class="sxs-lookup"><span data-stu-id="96d0a-130">Returns the maximum of the non-null values.</span></span>

<span data-ttu-id="96d0a-131">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-131">**Arguments**</span></span>

<span data-ttu-id="96d0a-132">`Byte`、`Int16`、`Int32`、`Int64`、`Byte`、`Single`、`Double`、`Decimal`、`DateTime`、`DateTimeOffset`、`Time`、`String`、`Binary`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-132">A `Byte`, `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, `Decimal`, `DateTime`, `DateTimeOffset`, `Time`, `String`, `Binary`.</span></span>

<span data-ttu-id="96d0a-133">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-133">**Return Value**</span></span>

<span data-ttu-id="96d0a-134">的类型 `expression` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-134">The type of `expression`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-135">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-135">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_MAX](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_max)]
[!code-sql[DP EntityServices Concepts#EDM_MAX](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_max)]

### <a name="minexpression"></a><span data-ttu-id="96d0a-136">Min(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-136">Min(expression)</span></span>

<span data-ttu-id="96d0a-137">返回非 null 值的最小值。</span><span class="sxs-lookup"><span data-stu-id="96d0a-137">Returns the minimum of the non-null values.</span></span>

<span data-ttu-id="96d0a-138">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-138">**Arguments**</span></span>

<span data-ttu-id="96d0a-139">`Byte`、`Int16`、`Int32`、`Int64`、`Byte`、`Single`、`Double`、`Decimal`、`DateTime`、`DateTimeOffset`、`Time`、`String`、`Binary`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-139">A `Byte`, `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, `Decimal`, `DateTime`, `DateTimeOffset`, `Time`, `String`, `Binary`.</span></span>

<span data-ttu-id="96d0a-140">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-140">**Return Value**</span></span>

<span data-ttu-id="96d0a-141">的类型 `expression` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-141">The type of `expression`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-142">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-142">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_MIN](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_min)]
[!code-sql[DP EntityServices Concepts#EDM_MIN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_min)]

### <a name="stdevexpression"></a><span data-ttu-id="96d0a-143">StDev(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-143">StDev(expression)</span></span>

<span data-ttu-id="96d0a-144">返回非 null 值的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="96d0a-144">Returns the standard deviation of the non-null values.</span></span>

<span data-ttu-id="96d0a-145">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-145">**Arguments**</span></span>

<span data-ttu-id="96d0a-146">`Int32`、`Int64`、`Double`、`Decimal`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-146">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="96d0a-147">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-147">**Return Value**</span></span>

<span data-ttu-id="96d0a-148">`Double`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-148">A `Double`.</span></span> <span data-ttu-id="96d0a-149">如果所有输入值均为 `Null` 值，则为 `null`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-149">`Null`, if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-150">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-150">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_STDEV](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_stdev)]
[!code-sql[DP EntityServices Concepts#EDM_STDEV](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_stdev)]

### <a name="stdevpexpression"></a><span data-ttu-id="96d0a-151">StDevP(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-151">StDevP(expression)</span></span>

<span data-ttu-id="96d0a-152">返回所有值的总体标准偏差。</span><span class="sxs-lookup"><span data-stu-id="96d0a-152">Returns the standard deviation for the population of all values.</span></span>

<span data-ttu-id="96d0a-153">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-153">**Arguments**</span></span>

<span data-ttu-id="96d0a-154">`Int32`、`Int64`、`Double`、`Decimal`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-154">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="96d0a-155">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-155">**Return Value**</span></span>

<span data-ttu-id="96d0a-156">一个 `Double` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-156">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-157">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-157">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_STDEVP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_stdevp)]
[!code-sql[DP EntityServices Concepts#EDM_STDEVP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_stdevp)]

### <a name="sumexpression"></a><span data-ttu-id="96d0a-158">Sum(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-158">Sum(expression)</span></span>

<span data-ttu-id="96d0a-159">返回非 null 值的总和。</span><span class="sxs-lookup"><span data-stu-id="96d0a-159">Returns the sum of the non-null values.</span></span>

<span data-ttu-id="96d0a-160">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-160">**Arguments**</span></span>

<span data-ttu-id="96d0a-161">`Int32`、`Int64`、`Double`、`Decimal`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-161">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="96d0a-162">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-162">**Return Value**</span></span>

<span data-ttu-id="96d0a-163">一个 `Double` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-163">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-164">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-164">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_SUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_sum)]
[!code-sql[DP EntityServices Concepts#EDM_SUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_sum)]

### <a name="varexpression"></a><span data-ttu-id="96d0a-165">Var(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-165">Var(expression)</span></span>

<span data-ttu-id="96d0a-166">返回所有非 Null 值的方差。</span><span class="sxs-lookup"><span data-stu-id="96d0a-166">Returns the variance of all non-null values.</span></span>

<span data-ttu-id="96d0a-167">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-167">**Arguments**</span></span>

<span data-ttu-id="96d0a-168">`Int32`、`Int64`、`Double`、`Decimal`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-168">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="96d0a-169">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-169">**Return Value**</span></span>

<span data-ttu-id="96d0a-170">一个 `Double` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-170">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-171">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-171">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_VAR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_var)]
[!code-sql[DP EntityServices Concepts#EDM_VAR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_var)]

### <a name="varpexpression"></a><span data-ttu-id="96d0a-172">VarP(expression)</span><span class="sxs-lookup"><span data-stu-id="96d0a-172">VarP(expression)</span></span>

<span data-ttu-id="96d0a-173">返回所有非 Null 值的总体方差。</span><span class="sxs-lookup"><span data-stu-id="96d0a-173">Returns the variance for the population of all non-null values.</span></span>

<span data-ttu-id="96d0a-174">**参数**</span><span class="sxs-lookup"><span data-stu-id="96d0a-174">**Arguments**</span></span>

<span data-ttu-id="96d0a-175">`Int32`、`Int64`、`Double`、`Decimal`。</span><span class="sxs-lookup"><span data-stu-id="96d0a-175">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="96d0a-176">**返回值**</span><span class="sxs-lookup"><span data-stu-id="96d0a-176">**Return Value**</span></span>

<span data-ttu-id="96d0a-177">一个 `Double` ， `null` 如果所有输入值都是值，则为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="96d0a-177">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="96d0a-178">**示例**</span><span class="sxs-lookup"><span data-stu-id="96d0a-178">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_VARP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_varp)]
[!code-sql[DP EntityServices Concepts#EDM_VARP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_varp)]

<span data-ttu-id="96d0a-179">Microsoft SQL 客户端托管提供程序中提供了等效功能。</span><span class="sxs-lookup"><span data-stu-id="96d0a-179">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="96d0a-180">有关详细信息，请参阅 [SqlClient for 实体框架函数](../sqlclient-for-ef-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="96d0a-180">For more information, see [SqlClient for Entity Framework Functions](../sqlclient-for-ef-functions.md).</span></span>

## <a name="collection-based-aggregates"></a><span data-ttu-id="96d0a-181">基于集合的聚合</span><span class="sxs-lookup"><span data-stu-id="96d0a-181">Collection-based aggregates</span></span>

<span data-ttu-id="96d0a-182">基于集合的聚合（集合函数）针对集合而运行并返回值。</span><span class="sxs-lookup"><span data-stu-id="96d0a-182">Collection-based aggregates (collection functions) operate on collections and return a value.</span></span> <span data-ttu-id="96d0a-183">例如，如果 ORDERS 是所有订单的集合，则可以使用以下表达式计算最早的发货日期：</span><span class="sxs-lookup"><span data-stu-id="96d0a-183">For example if ORDERS is a collection of all orders, you can calculate the earliest ship date with the following expression:</span></span>

```sql
min(select value o.ShipDate from LOB.Orders as o)
```

<span data-ttu-id="96d0a-184">将在当前环境名称解析范围内计算基于集合的聚合内的表达式。</span><span class="sxs-lookup"><span data-stu-id="96d0a-184">Expressions inside collection-based aggregates are evaluated within the current ambient name-resolution scope.</span></span>

## <a name="group-based-aggregates"></a><span data-ttu-id="96d0a-185">基于组的聚合</span><span class="sxs-lookup"><span data-stu-id="96d0a-185">Group-based aggregates</span></span>

<span data-ttu-id="96d0a-186">基于组的聚合将按照 GROUP BY 子句定义的方式对组进行计算。</span><span class="sxs-lookup"><span data-stu-id="96d0a-186">Group-based aggregates are calculated over a group as defined by the GROUP BY clause.</span></span> <span data-ttu-id="96d0a-187">对于结果中的每个组，将使用每个组中的元素作为聚合计算的输入来计算单独的聚合。</span><span class="sxs-lookup"><span data-stu-id="96d0a-187">For each group in the result, a separate aggregate is calculated by using the elements in each group as input to the aggregate calculation.</span></span> <span data-ttu-id="96d0a-188">当在 select 表达式中使用 group-by 子句时，在投影或 order-by 子句中只存在分组表达式名称、聚合或常量表达式。</span><span class="sxs-lookup"><span data-stu-id="96d0a-188">When a group-by clause is used in a select expression, only grouping expression names, aggregates, or constant expressions can be present in the projection or order-by clause.</span></span>

<span data-ttu-id="96d0a-189">以下示例计算每种产品的平均订购数量：</span><span class="sxs-lookup"><span data-stu-id="96d0a-189">The following example calculates the average quantity ordered for each product:</span></span>

```sql
select p, avg(ol.Quantity) from LOB.OrderLines as ol
  group by ol.Product as p
```

<span data-ttu-id="96d0a-190">在 SELECT 表达式中，可以有一个基于组的聚合，无需使用显式分组依据子句。</span><span class="sxs-lookup"><span data-stu-id="96d0a-190">It's possible to have a group-based aggregate without an explicit group-by clause in the SELECT expression.</span></span> <span data-ttu-id="96d0a-191">在这种情况下，所有元素都被视为单个组。</span><span class="sxs-lookup"><span data-stu-id="96d0a-191">In this case, all elements are treated as a single group.</span></span> <span data-ttu-id="96d0a-192">这等效于指定基于常量的分组。</span><span class="sxs-lookup"><span data-stu-id="96d0a-192">This is equivalent of specifying a grouping based on a constant.</span></span> <span data-ttu-id="96d0a-193">例如，请看下面的表达式：</span><span class="sxs-lookup"><span data-stu-id="96d0a-193">Take, for example, the following expression:</span></span>

```sql
select avg(ol.Quantity) from LOB.OrderLines as ol
```

<span data-ttu-id="96d0a-194">此表达式等效于以下表达式：</span><span class="sxs-lookup"><span data-stu-id="96d0a-194">This is equivalent to the following:</span></span>

```sql
select avg(ol.Quantity) from LOB.OrderLines as ol group by 1
```

<span data-ttu-id="96d0a-195">将在 WHERE 子句表达式可见的名称解析范围内计算基于组的聚合中的表达式。</span><span class="sxs-lookup"><span data-stu-id="96d0a-195">Expressions inside the group-based aggregate are evaluated within the name-resolution scope that would be visible to the WHERE clause expression.</span></span>

<span data-ttu-id="96d0a-196">在 Transact-sql 中，基于组的聚合还可以指定 ALL 或 DISTINCT 修饰符。</span><span class="sxs-lookup"><span data-stu-id="96d0a-196">As in Transact-SQL, group-based aggregates can also specify an ALL or DISTINCT modifier.</span></span> <span data-ttu-id="96d0a-197">如果指定 DISTINCT 修饰符，则将从聚合输入集合中消除重复项，然后计算聚合。</span><span class="sxs-lookup"><span data-stu-id="96d0a-197">If the DISTINCT modifier is specified, duplicates are eliminated from the aggregate input collection, before the aggregate is computed.</span></span> <span data-ttu-id="96d0a-198">如果指定 ALL 修饰符（或者未指定修饰符），则不执行重复项消除。</span><span class="sxs-lookup"><span data-stu-id="96d0a-198">If the ALL modifier is specified (or if no modifier is specified), no duplicate elimination is performed.</span></span>

## <a name="see-also"></a><span data-ttu-id="96d0a-199">请参阅</span><span class="sxs-lookup"><span data-stu-id="96d0a-199">See also</span></span>

- [<span data-ttu-id="96d0a-200">规范函数</span><span class="sxs-lookup"><span data-stu-id="96d0a-200">Canonical Functions</span></span>](canonical-functions.md)

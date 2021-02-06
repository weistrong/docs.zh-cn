---
description: '了解详细信息：聚合函数 (SqlClient for 实体框架) '
title: 聚合函数（用于实体框架的 SqlClient）
ms.date: 03/30/2017
ms.assetid: 03303f01-b591-4efc-9875-f9c608edff0b
ms.openlocfilehash: b9f1ff8c75fc09de7532b459090b0b5cd1d47262
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651075"
---
# <a name="aggregate-functions-sqlclient-for-entity-framework"></a><span data-ttu-id="b58ed-103">聚合函数（用于实体框架的 SqlClient）</span><span class="sxs-lookup"><span data-stu-id="b58ed-103">Aggregate Functions (SqlClient for Entity Framework)</span></span>

<span data-ttu-id="b58ed-104">SQL Server .NET Framework 数据提供程序 (SqlClient) 提供聚合函数。</span><span class="sxs-lookup"><span data-stu-id="b58ed-104">The .NET Framework Data Provider for SQL Server (SqlClient) provides aggregate functions.</span></span> <span data-ttu-id="b58ed-105">聚合函数对一组输入值执行计算并返回一个值。</span><span class="sxs-lookup"><span data-stu-id="b58ed-105">Aggregate functions perform calculations on a set of input values and return a value.</span></span> <span data-ttu-id="b58ed-106">这些函数位于 SqlServer 命名空间中，该命名空间在您使用 SqlClient 时可用。</span><span class="sxs-lookup"><span data-stu-id="b58ed-106">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="b58ed-107">提供程序的命名空间属性使实体框架可以确定此提供程序对特定构造（如类型和函数）使用哪个前缀。</span><span class="sxs-lookup"><span data-stu-id="b58ed-107">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span>  
  
 <span data-ttu-id="b58ed-108">下面是 SqlClient 聚合函数。</span><span class="sxs-lookup"><span data-stu-id="b58ed-108">The following are the SqlClient aggregate functions.</span></span>  

## <a name="avgexpression"></a><span data-ttu-id="b58ed-109">AVG (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-109">AVG(expression)</span></span>

<span data-ttu-id="b58ed-110">返回集合中各值的平均值。</span><span class="sxs-lookup"><span data-stu-id="b58ed-110">Returns the average of the values in a collection.</span></span> <span data-ttu-id="b58ed-111">Null 值会被忽略。</span><span class="sxs-lookup"><span data-stu-id="b58ed-111">Null values are ignored.</span></span>

<span data-ttu-id="b58ed-112">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-112">**Arguments**</span></span>

<span data-ttu-id="b58ed-113">`Int32`、、 `Int64` `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-113">An `Int32`, `Int64`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="b58ed-114">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-114">**Return Value**</span></span>

<span data-ttu-id="b58ed-115">`expression` 的类型。</span><span class="sxs-lookup"><span data-stu-id="b58ed-115">The type of `expression`.</span></span>

<span data-ttu-id="b58ed-116">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-116">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_avg)]

## <a name="checksum_aggcollection"></a><span data-ttu-id="b58ed-117">CHECKSUM_AGG (集合) </span><span class="sxs-lookup"><span data-stu-id="b58ed-117">CHECKSUM_AGG(collection)</span></span>

 <span data-ttu-id="b58ed-118">返回集合中各值的校验和。</span><span class="sxs-lookup"><span data-stu-id="b58ed-118">Returns the checksum of the values in a collection.</span></span> <span data-ttu-id="b58ed-119">Null 值会被忽略。</span><span class="sxs-lookup"><span data-stu-id="b58ed-119">Null values are ignored.</span></span>

 <span data-ttu-id="b58ed-120">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-120">**Arguments**</span></span>

 <span data-ttu-id="b58ed-121">)  (集合 `Int32` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-121">A Collection(`Int32`).</span></span>

 <span data-ttu-id="b58ed-122">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-122">**Return Value**</span></span>

 <span data-ttu-id="b58ed-123">`Int32`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-123">An `Int32`.</span></span>

 <span data-ttu-id="b58ed-124">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-124">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_checksum)]

## <a name="countexpression"></a><span data-ttu-id="b58ed-125">计数 (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-125">COUNT(expression)</span></span>

<span data-ttu-id="b58ed-126">以 `Int32` 形式返回集合中的项数。</span><span class="sxs-lookup"><span data-stu-id="b58ed-126">Returns the number of items in a collection as an `Int32`.</span></span>

<span data-ttu-id="b58ed-127">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-127">**Arguments**</span></span>

<span data-ttu-id="b58ed-128">一个集合 \<T> ，其中 T 为以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="b58ed-128">A Collection\<T>, where T is one of the following types:</span></span>

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|<span data-ttu-id="b58ed-129">`Guid` SQL Server 2000 中未返回 () </span><span class="sxs-lookup"><span data-stu-id="b58ed-129">`Guid` (not returned in SQL Server 2000)</span></span>|

<span data-ttu-id="b58ed-130">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-130">**Return Value**</span></span>

<span data-ttu-id="b58ed-131">`Int32`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-131">An `Int32`.</span></span>

<span data-ttu-id="b58ed-132">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-132">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_count)]

## <a name="count_bigexpression"></a><span data-ttu-id="b58ed-133"> (表达式的 COUNT_BIG) </span><span class="sxs-lookup"><span data-stu-id="b58ed-133">COUNT_BIG(expression)</span></span>

<span data-ttu-id="b58ed-134">以 `bigint` 形式返回集合中的项数。</span><span class="sxs-lookup"><span data-stu-id="b58ed-134">Returns the number of items in a collection as a `bigint`.</span></span>

 <span data-ttu-id="b58ed-135">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-135">**Arguments**</span></span>

 <span data-ttu-id="b58ed-136">集合 (T) ，其中 T 为以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="b58ed-136">A Collection(T), where T is one of the following types:</span></span>

 |   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|<span data-ttu-id="b58ed-137">`Guid` SQL Server 2000 中未返回 () </span><span class="sxs-lookup"><span data-stu-id="b58ed-137">`Guid` (not returned in SQL Server 2000)</span></span>|

<span data-ttu-id="b58ed-138">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-138">**Return Value**</span></span>

<span data-ttu-id="b58ed-139">`Int64`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-139">An `Int64`.</span></span>

<span data-ttu-id="b58ed-140">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-140">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_countbig)]

## <a name="maxexpression"></a><span data-ttu-id="b58ed-141">MAX (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-141">MAX(expression)</span></span>

<span data-ttu-id="b58ed-142">返回集合中的最大值。</span><span class="sxs-lookup"><span data-stu-id="b58ed-142">Returns the maximum value the collection.</span></span>

<span data-ttu-id="b58ed-143">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-143">**Arguments**</span></span>

<span data-ttu-id="b58ed-144">集合 (T) ，其中 T 为以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="b58ed-144">A Collection(T), where T is one of the following types:</span></span>

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

<span data-ttu-id="b58ed-145">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-145">**Return Value**</span></span>

<span data-ttu-id="b58ed-146">`expression` 的类型。</span><span class="sxs-lookup"><span data-stu-id="b58ed-146">The type of `expression`.</span></span>

<span data-ttu-id="b58ed-147">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-147">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_max)]

## <a name="minexpression"></a><span data-ttu-id="b58ed-148">MIN (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-148">MIN(expression)</span></span>

<span data-ttu-id="b58ed-149">返回集合中的最小值。</span><span class="sxs-lookup"><span data-stu-id="b58ed-149">Returns the minimum value in a collection.</span></span>

<span data-ttu-id="b58ed-150">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-150">**Arguments**</span></span>

<span data-ttu-id="b58ed-151">集合 (T) ，其中 T 为以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="b58ed-151">A Collection(T), where T is one of the following types:</span></span>

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

<span data-ttu-id="b58ed-152">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-152">**Return Value**</span></span>

<span data-ttu-id="b58ed-153">`expression` 的类型。</span><span class="sxs-lookup"><span data-stu-id="b58ed-153">The type of `expression`.</span></span>

<span data-ttu-id="b58ed-154">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-154">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_min)]

## <a name="stdevexpression"></a><span data-ttu-id="b58ed-155">STDEV (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-155">STDEV(expression)</span></span>

<span data-ttu-id="b58ed-156">返回指定表达式中所有值的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="b58ed-156">Returns the statistical standard deviation of all values in the specified expression.</span></span>

<span data-ttu-id="b58ed-157">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-157">**Arguments**</span></span>

<span data-ttu-id="b58ed-158">)  (集合 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-158">A Collection(`Double`).</span></span>

<span data-ttu-id="b58ed-159">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-159">**Return Value**</span></span>

<span data-ttu-id="b58ed-160">`Double`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-160">A `Double`.</span></span>

<span data-ttu-id="b58ed-161">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-161">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdev)]

## <a name="stdevpexpression"></a><span data-ttu-id="b58ed-162">STDEVP (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-162">STDEVP(expression)</span></span>

<span data-ttu-id="b58ed-163">返回指定表达式中所有值的总体标准偏差。</span><span class="sxs-lookup"><span data-stu-id="b58ed-163">Returns the statistical standard deviation for the population for all values in the specified expression.</span></span>

<span data-ttu-id="b58ed-164">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-164">**Arguments**</span></span>

<span data-ttu-id="b58ed-165">)  (集合 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-165">A Collection(`Double`).</span></span>

<span data-ttu-id="b58ed-166">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-166">**Return Value**</span></span>

<span data-ttu-id="b58ed-167">`Double`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-167">A `Double`.</span></span>

<span data-ttu-id="b58ed-168">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-168">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdevp)]

## <a name="sumexpression"></a><span data-ttu-id="b58ed-169">SUM (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-169">SUM(expression)</span></span>

<span data-ttu-id="b58ed-170">返回集合中所有值的总和。</span><span class="sxs-lookup"><span data-stu-id="b58ed-170">Returns the sum of all the values in the collection.</span></span>

<span data-ttu-id="b58ed-171">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-171">**Arguments**</span></span>

<span data-ttu-id="b58ed-172">集合 (T) 其中 T 为以下类型之一： `Int32` 、 `Int64` 、 `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-172">A Collection(T) where T is one of the following types: `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="b58ed-173">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-173">**Return Value**</span></span>

<span data-ttu-id="b58ed-174">`expression` 的类型。</span><span class="sxs-lookup"><span data-stu-id="b58ed-174">The type of `expression`.</span></span>

<span data-ttu-id="b58ed-175">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-175">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_sum)]

## <a name="varexpression"></a><span data-ttu-id="b58ed-176">VAR (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-176">VAR(expression)</span></span>

<span data-ttu-id="b58ed-177">返回指定表达式中所有值的方差。</span><span class="sxs-lookup"><span data-stu-id="b58ed-177">Returns the statistical variance of all values in the specified expression.</span></span>

<span data-ttu-id="b58ed-178">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-178">**Arguments**</span></span>

<span data-ttu-id="b58ed-179">)  (集合 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-179">A Collection(`Double`).</span></span>

<span data-ttu-id="b58ed-180">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-180">**Return Value**</span></span>

<span data-ttu-id="b58ed-181">`Double`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-181">A `Double`.</span></span>

<span data-ttu-id="b58ed-182">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-182">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_var)]

## <a name="varpexpression"></a><span data-ttu-id="b58ed-183">VARP (表达式) </span><span class="sxs-lookup"><span data-stu-id="b58ed-183">VARP(expression)</span></span>

<span data-ttu-id="b58ed-184">返回指定表达式中所有值的总体统计方差。</span><span class="sxs-lookup"><span data-stu-id="b58ed-184">Returns the statistical variance for the population for all values in the specified expression.</span></span>

<span data-ttu-id="b58ed-185">**参数**</span><span class="sxs-lookup"><span data-stu-id="b58ed-185">**Arguments**</span></span>

<span data-ttu-id="b58ed-186">)  (集合 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="b58ed-186">A Collection(`Double`).</span></span>

<span data-ttu-id="b58ed-187">**返回值**</span><span class="sxs-lookup"><span data-stu-id="b58ed-187">**Return Value**</span></span>

<span data-ttu-id="b58ed-188">`Double`。</span><span class="sxs-lookup"><span data-stu-id="b58ed-188">A `Double`.</span></span>

<span data-ttu-id="b58ed-189">**示例**</span><span class="sxs-lookup"><span data-stu-id="b58ed-189">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_varp)]
  
## <a name="see-also"></a><span data-ttu-id="b58ed-190">请参阅</span><span class="sxs-lookup"><span data-stu-id="b58ed-190">See also</span></span>

- [<span data-ttu-id="b58ed-191">聚合函数 (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="b58ed-191">Aggregate Functions (Transact-SQL)</span></span>](/sql/t-sql/functions/aggregate-functions-transact-sql)
- [<span data-ttu-id="b58ed-192">Entity SQL 语言</span><span class="sxs-lookup"><span data-stu-id="b58ed-192">Entity SQL Language</span></span>](./language-reference/entity-sql-language.md)
- [<span data-ttu-id="b58ed-193">聚合规范函数</span><span class="sxs-lookup"><span data-stu-id="b58ed-193">Aggregate Canonical Functions</span></span>](./language-reference/aggregate-canonical-functions.md)

---
description: 了解详细信息：数学函数
title: 数学函数
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: 6bf1f116d6d88a8a188dc31cab91fbf26bdaea36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795022"
---
# <a name="mathematical-functions"></a><span data-ttu-id="d7d25-103">数学函数</span><span class="sxs-lookup"><span data-stu-id="d7d25-103">Mathematical Functions</span></span>

<span data-ttu-id="d7d25-104">SQL Server .NET Framework 数据提供程序 (SqlClient) 提供了各种数学函数，这些函数针对作为自变量提供的输入值执行计算并返回数值结果。</span><span class="sxs-lookup"><span data-stu-id="d7d25-104">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="d7d25-105">这些函数位于 SqlServer 命名空间中，该命名空间在您使用 SqlClient 时可用。</span><span class="sxs-lookup"><span data-stu-id="d7d25-105">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="d7d25-106">提供程序的命名空间属性使实体框架可以确定此提供程序对特定构造（如类型和函数）使用哪个前缀。</span><span class="sxs-lookup"><span data-stu-id="d7d25-106">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="d7d25-107">下表介绍了 SqlClient 数学函数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-107">The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="d7d25-108">ABS (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-108">ABS(expression)</span></span>

<span data-ttu-id="d7d25-109">执行绝对值函数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-109">Performs the absolute value function.</span></span>

<span data-ttu-id="d7d25-110">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-110">**Arguments**</span></span>

<span data-ttu-id="d7d25-111">`expression`：`Int32`、`Int64`、`Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-111">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-112">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-112">**Return Value**</span></span>

<span data-ttu-id="d7d25-113">指定表达式的绝对值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-113">The absolute value of the specified expression.</span></span>

<span data-ttu-id="d7d25-114">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-114">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="d7d25-115">ACOS (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-115">ACOS(expression)</span></span>

<span data-ttu-id="d7d25-116">返回指定表达式的反余弦值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-116">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="d7d25-117">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-117">**Arguments**</span></span>

<span data-ttu-id="d7d25-118">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-118">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-119">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-119">**Return Value**</span></span>

<span data-ttu-id="d7d25-120">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-120">A `Double`.</span></span>

<span data-ttu-id="d7d25-121">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-121">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="d7d25-122">ASIN (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-122">ASIN(expression)</span></span>

<span data-ttu-id="d7d25-123">返回指定表达式的反正弦值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-123">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="d7d25-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-124">**Arguments**</span></span>

<span data-ttu-id="d7d25-125">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-125">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-126">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-126">**Return Value**</span></span>

<span data-ttu-id="d7d25-127">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-127">A `Double`.</span></span>

<span data-ttu-id="d7d25-128">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-128">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="d7d25-129">ATAN (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-129">ATAN(expression)</span></span>

<span data-ttu-id="d7d25-130">返回指定数值表达式的反正切值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-130">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="d7d25-131">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-131">**Arguments**</span></span>

<span data-ttu-id="d7d25-132">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-132">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-133">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-133">**Return Value**</span></span>

<span data-ttu-id="d7d25-134">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-134">A `Double`.</span></span>

<span data-ttu-id="d7d25-135">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-135">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="d7d25-136">ATN2 (expression，expression) </span><span class="sxs-lookup"><span data-stu-id="d7d25-136">ATN2(expression, expression)</span></span>

<span data-ttu-id="d7d25-137">返回以弧度表示的角度，其正切介于两个指定的数值表达式之间。</span><span class="sxs-lookup"><span data-stu-id="d7d25-137">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="d7d25-138">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-138">**Arguments**</span></span>

<span data-ttu-id="d7d25-139">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-139">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-140">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-140">**Return Value**</span></span>

<span data-ttu-id="d7d25-141">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-141">A `Double`.</span></span>

<span data-ttu-id="d7d25-142">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-142">**Example**</span></span>

`SqlServer.ATN2(9, 8)`

## <a name="ceilingexpression"></a><span data-ttu-id="d7d25-143">天花板 (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-143">CEILING(expression)</span></span>

<span data-ttu-id="d7d25-144">将指定表达式转换为大于或等于该表达式的最小整数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-144">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="d7d25-145">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-145">**Arguments**</span></span>

<span data-ttu-id="d7d25-146">`expression`：`Int32`、`Int64`、`Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-146">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-147">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-147">**Return Value**</span></span>

<span data-ttu-id="d7d25-148">`Int32`、、 `Int64` `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-148">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-149">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-149">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="d7d25-150">COS (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-150">COS(expression)</span></span>

<span data-ttu-id="d7d25-151">计算以弧度表示的指定角度的三角余弦。</span><span class="sxs-lookup"><span data-stu-id="d7d25-151">Calculates the trigonometric cosine of the specified angle in radians.</span></span>

<span data-ttu-id="d7d25-152">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-152">**Arguments**</span></span>

<span data-ttu-id="d7d25-153">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-153">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-154">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-154">**Return Value**</span></span>

<span data-ttu-id="d7d25-155">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-155">A `Double`.</span></span>

<span data-ttu-id="d7d25-156">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-156">**Example**</span></span>

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="d7d25-157">COT (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-157">COT(expression)</span></span>

<span data-ttu-id="d7d25-158">计算以弧度表示的指定角度的三角余切。</span><span class="sxs-lookup"><span data-stu-id="d7d25-158">Calculates the trigonometric cotangent of the specified angle in radians.</span></span>

<span data-ttu-id="d7d25-159">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-159">**Arguments**</span></span>

<span data-ttu-id="d7d25-160">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-160">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-161">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-161">**Return Value**</span></span>

<span data-ttu-id="d7d25-162">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-162">A `Double`.</span></span>

<span data-ttu-id="d7d25-163">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-163">**Example**</span></span>

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="d7d25-164">度 (弧度) </span><span class="sxs-lookup"><span data-stu-id="d7d25-164">DEGREES(radians)</span></span>

<span data-ttu-id="d7d25-165">返回以度为单位的对应角度。</span><span class="sxs-lookup"><span data-stu-id="d7d25-165">Returns the corresponding angle in degrees.</span></span>

<span data-ttu-id="d7d25-166">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-166">**Arguments**</span></span>

<span data-ttu-id="d7d25-167">`expression`：`Int32`、`Int64`、`Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-167">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-168">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-168">**Return Value**</span></span>

<span data-ttu-id="d7d25-169">`Int32`、、 `Int64` `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-169">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-170">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-170">**Example**</span></span>

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="d7d25-171">EXP (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-171">EXP(expression)</span></span>

<span data-ttu-id="d7d25-172">计算指定数值表达式的指数值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-172">Calculates the exponential value of a specified numeric expression.</span></span>

<span data-ttu-id="d7d25-173">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-173">**Arguments**</span></span>

<span data-ttu-id="d7d25-174">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-174">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-175">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-175">**Return Value**</span></span>

<span data-ttu-id="d7d25-176">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-176">A `Double`.</span></span>

<span data-ttu-id="d7d25-177">**示例** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="d7d25-177">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="d7d25-178">楼层 (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-178">FLOOR(expression)</span></span>

<span data-ttu-id="d7d25-179">将指定表达式转换为小于或等于该表达式的最大整数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-179">Converts the specified expression to the largest integer less than or equal to it.</span></span>

<span data-ttu-id="d7d25-180">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-180">**Arguments**</span></span>

<span data-ttu-id="d7d25-181">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-181">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-182">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-182">**Return Value**</span></span>

<span data-ttu-id="d7d25-183">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-183">A `Double`.</span></span>

<span data-ttu-id="d7d25-184">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-184">**Example**</span></span>

[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="d7d25-185">日志 (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-185">LOG(expression)</span></span>

<span data-ttu-id="d7d25-186">计算指定 `float` 表达式的自然对数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-186">Calculates the natural logarithm of the specified `float` expression.</span></span>

<span data-ttu-id="d7d25-187">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-187">**Arguments**</span></span>

<span data-ttu-id="d7d25-188">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-188">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-189">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-189">**Return Value**</span></span>

<span data-ttu-id="d7d25-190">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-190">A `Double`.</span></span>

<span data-ttu-id="d7d25-191">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-191">**Example**</span></span>

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="d7d25-192">LOG10 (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-192">LOG10(expression)</span></span>

<span data-ttu-id="d7d25-193">返回指定 `Double` 表达式的以 10 为底的对数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-193">Returns the base-10 logarithm of the specified `Double` expression.</span></span>

<span data-ttu-id="d7d25-194">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-194">**Arguments**</span></span>

<span data-ttu-id="d7d25-195">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-195">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-196">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-196">**Return Value**</span></span>

<span data-ttu-id="d7d25-197">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-197">A `Double`.</span></span>

<span data-ttu-id="d7d25-198">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-198">**Example**</span></span>

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="d7d25-199">PI ( # A1</span><span class="sxs-lookup"><span data-stu-id="d7d25-199">PI()</span></span>

<span data-ttu-id="d7d25-200">以 `Double` 格式返回 pi 的常量值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-200">Returns the constant value of pi as a `Double`.</span></span>

<span data-ttu-id="d7d25-201">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-201">**Return Value**</span></span>

<span data-ttu-id="d7d25-202">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-202">A `Double`.</span></span>

<span data-ttu-id="d7d25-203">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-203">**Example**</span></span>

`SqlServer.PI()`

## <a name="powernumeric_expression-power_expression"></a><span data-ttu-id="d7d25-204">POWER (numeric_expression，power_expression) </span><span class="sxs-lookup"><span data-stu-id="d7d25-204">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="d7d25-205">计算指定表达式的指定幂的值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-205">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="d7d25-206">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-206">**Arguments**</span></span>

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="d7d25-207">`Int32`、、 `Int64` `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-207">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="d7d25-208">`Double`，表示对 `numeric_expression` 进行幂运算的幂值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-208">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>|

<span data-ttu-id="d7d25-209">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-209">**Return Value**</span></span>

<span data-ttu-id="d7d25-210">指定 `numeric_expression` 的指定 `power_expression` 次幂的值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-210">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="d7d25-211">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-211">**Example**</span></span>

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="d7d25-212">RADIANS (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-212">RADIANS(expression)</span></span>

<span data-ttu-id="d7d25-213">将度转换为弧度。</span><span class="sxs-lookup"><span data-stu-id="d7d25-213">Converts degrees to radians.</span></span>

<span data-ttu-id="d7d25-214">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-214">**Arguments**</span></span>

<span data-ttu-id="d7d25-215">`expression`：`Int32`、`Int64`、`Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-215">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-216">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-216">**Return Value**</span></span>

<span data-ttu-id="d7d25-217">`Int32`、、 `Int64` `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-217">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-218">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-218">**Example**</span></span>

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="d7d25-219">RAND ( [seed] ) </span><span class="sxs-lookup"><span data-stu-id="d7d25-219">RAND([seed])</span></span>

<span data-ttu-id="d7d25-220">返回介于 0 和 1 之间的随机值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-220">Returns a random value from 0 through 1.</span></span>

<span data-ttu-id="d7d25-221">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-221">**Arguments**</span></span>

<span data-ttu-id="d7d25-222">形式的种子值 `Int32` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-222">The seed value as an `Int32`.</span></span> <span data-ttu-id="d7d25-223">如果未指定种子，则 SQL Server 数据库引擎将随机分配种子值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-223">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="d7d25-224">对于指定的种子值，返回的结果始终相同。</span><span class="sxs-lookup"><span data-stu-id="d7d25-224">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="d7d25-225">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-225">**Return Value**</span></span>

<span data-ttu-id="d7d25-226">介于 0 和 1 之间的随机 `Double` 值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-226">A random `Double` value from 0 through 1.</span></span>

<span data-ttu-id="d7d25-227">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-227">**Example**</span></span>

`SqlServer.RAND()`
  
## <a name="roundnumeric_expression-lengthfunction"></a><span data-ttu-id="d7d25-228">舍入 (numeric_expression，length [，function] ) </span><span class="sxs-lookup"><span data-stu-id="d7d25-228">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="d7d25-229">返回一个舍入到指定长度或精度的数值表达式。</span><span class="sxs-lookup"><span data-stu-id="d7d25-229">Returns a numeric expression, rounded to the specified length or precision.</span></span>

<span data-ttu-id="d7d25-230">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-230">**Arguments**</span></span>

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="d7d25-231">`Int32`、、 `Int64` `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-231">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>
|`length`| <span data-ttu-id="d7d25-232">表示 `Int32` 要舍入到的精度的 `numeric_expression`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-232">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="d7d25-233">如果 `length` 为正数，则将 `numeric_expression` 舍入到 `length` 指定的小数位数。</span><span class="sxs-lookup"><span data-stu-id="d7d25-233">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="d7d25-234">如果 `length` 为负数，则将 `numeric_expression` 向小数点左边舍入 `length` 指定的长度。</span><span class="sxs-lookup"><span data-stu-id="d7d25-234">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="d7d25-235">可选。</span><span class="sxs-lookup"><span data-stu-id="d7d25-235">Optional.</span></span> <span data-ttu-id="d7d25-236">一个 `Int32` ，表示要执行的操作的类型。</span><span class="sxs-lookup"><span data-stu-id="d7d25-236">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="d7d25-237">如果省略函数或其值为 0 (默认值) ， `numeric_expression` 则将舍入。</span><span class="sxs-lookup"><span data-stu-id="d7d25-237">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="d7d25-238">如果指定了 0 以外的值，则将截断 `numeric_expression`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-238">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="d7d25-239">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-239">**Return Value**</span></span>

<span data-ttu-id="d7d25-240">指定 `numeric_expression` 的指定 `power_expression` 次幂的值。</span><span class="sxs-lookup"><span data-stu-id="d7d25-240">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="d7d25-241">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-241">**Example**</span></span>

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="d7d25-242">SIGN (expression) </span><span class="sxs-lookup"><span data-stu-id="d7d25-242">SIGN(expression)</span></span>

<span data-ttu-id="d7d25-243">返回指定表达式的正号 (+1)、零 (0) 或负号 (-1)。</span><span class="sxs-lookup"><span data-stu-id="d7d25-243">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span>

<span data-ttu-id="d7d25-244">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-244">**Arguments**</span></span>

<span data-ttu-id="d7d25-245">`expression`：`Int32`、`Int64`、`Double` 或 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="d7d25-245">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span>

<span data-ttu-id="d7d25-246">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-246">**Return Value**</span></span>

<span data-ttu-id="d7d25-247">`Int32`、、 `Int64` `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="d7d25-247">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d7d25-248">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-248">**Example**</span></span>

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="d7d25-249">SIN (expression) </span><span class="sxs-lookup"><span data-stu-id="d7d25-249">SIN(expression)</span></span>

<span data-ttu-id="d7d25-250">计算以弧度表示的指定角度的三角正弦并返回 `Double` 表达式。</span><span class="sxs-lookup"><span data-stu-id="d7d25-250">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span>

<span data-ttu-id="d7d25-251">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-251">**Arguments**</span></span>

<span data-ttu-id="d7d25-252">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-252">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-253">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-253">**Return Value**</span></span>

<span data-ttu-id="d7d25-254">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-254">A `Double`.</span></span>

<span data-ttu-id="d7d25-255">**示例** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="d7d25-255">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="d7d25-256">SQRT (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-256">SQRT(expression)</span></span>

<span data-ttu-id="d7d25-257">返回指定表达式的平方根。</span><span class="sxs-lookup"><span data-stu-id="d7d25-257">Returns the square root of the specified expression.</span></span>

<span data-ttu-id="d7d25-258">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-258">**Arguments**</span></span>

<span data-ttu-id="d7d25-259">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-259">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-260">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-260">**Return Value**</span></span>

<span data-ttu-id="d7d25-261">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-261">A `Double`.</span></span>

<span data-ttu-id="d7d25-262">**示例** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="d7d25-262">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="d7d25-263">方形 (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-263">SQUARE(expression)</span></span>

<span data-ttu-id="d7d25-264">返回指定表达式的平方。</span><span class="sxs-lookup"><span data-stu-id="d7d25-264">Returns the square of the specified expression.</span></span>

<span data-ttu-id="d7d25-265">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-265">**Arguments**</span></span>

<span data-ttu-id="d7d25-266">`expression`：`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-266">`expression`: A `Double`.</span></span>

<span data-ttu-id="d7d25-267">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-267">**Return Value**</span></span>

<span data-ttu-id="d7d25-268">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d7d25-268">A `Double`.</span></span>

<span data-ttu-id="d7d25-269">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-269">**Example**</span></span>

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="d7d25-270">TAN (表达式) </span><span class="sxs-lookup"><span data-stu-id="d7d25-270">TAN(expression)</span></span>

<span data-ttu-id="d7d25-271">计算指定表达式的正切。</span><span class="sxs-lookup"><span data-stu-id="d7d25-271">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="d7d25-272">**参数**</span><span class="sxs-lookup"><span data-stu-id="d7d25-272">**Arguments**</span></span>

<span data-ttu-id="d7d25-273">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="d7d25-273">`expression`: `Double`</span></span>

<span data-ttu-id="d7d25-274">**返回值**</span><span class="sxs-lookup"><span data-stu-id="d7d25-274">**Return Value**</span></span>

`Double`

<span data-ttu-id="d7d25-275">**示例**</span><span class="sxs-lookup"><span data-stu-id="d7d25-275">**Example**</span></span>

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="d7d25-276">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7d25-276">See also</span></span>

- [<span data-ttu-id="d7d25-277">数学函数 (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="d7d25-277">Mathematical Functions (Transact-SQL)</span></span>](/sql/t-sql/functions/mathematical-functions-transact-sql)
- [<span data-ttu-id="d7d25-278">用于实体框架函数的 SqlClient</span><span class="sxs-lookup"><span data-stu-id="d7d25-278">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)

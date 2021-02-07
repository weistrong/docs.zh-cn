---
description: 详细了解：数学规范函数
title: 数学规范函数
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: 55072099f5766d48ea3067a2e9eaa187a8b3f111
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739360"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="e7187-103">数学规范函数</span><span class="sxs-lookup"><span data-stu-id="e7187-103">Math Canonical Functions</span></span>

<span data-ttu-id="e7187-104">实体 SQL 包括以下数学规范函数：</span><span class="sxs-lookup"><span data-stu-id="e7187-104">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="e7187-105">Abs(value)</span><span class="sxs-lookup"><span data-stu-id="e7187-105">Abs(value)</span></span>

<span data-ttu-id="e7187-106">返回 `value` 的绝对值。</span><span class="sxs-lookup"><span data-stu-id="e7187-106">Returns the absolute value of `value`.</span></span>

<span data-ttu-id="e7187-107">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-107">**Arguments**</span></span>

<span data-ttu-id="e7187-108">、、、 `Int16` `Int32` 、、 `Int64` `Byte` `Single` `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="e7187-108">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="e7187-109">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-109">**Return Value**</span></span>

<span data-ttu-id="e7187-110">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-110">The type of `value`.</span></span>

<span data-ttu-id="e7187-111">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-111">**Example**</span></span>

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="e7187-112">Ceiling(value)</span><span class="sxs-lookup"><span data-stu-id="e7187-112">Ceiling(value)</span></span>

<span data-ttu-id="e7187-113">返回不小于 `value` 的最小整数。</span><span class="sxs-lookup"><span data-stu-id="e7187-113">Returns the smallest integer that is not less than `value`.</span></span>

<span data-ttu-id="e7187-114">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-114">**Arguments**</span></span>

<span data-ttu-id="e7187-115">`Single`、 `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="e7187-115">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="e7187-116">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-116">**Return Value**</span></span>

<span data-ttu-id="e7187-117">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-117">The type of `value`.</span></span>

<span data-ttu-id="e7187-118">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-118">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="e7187-119">Floor(value)</span><span class="sxs-lookup"><span data-stu-id="e7187-119">Floor(value)</span></span>

<span data-ttu-id="e7187-120">返回不大于 `value` 的最大整数。</span><span class="sxs-lookup"><span data-stu-id="e7187-120">Returns the largest integer that is not greater than `value`.</span></span>

<span data-ttu-id="e7187-121">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-121">**Arguments**</span></span>

<span data-ttu-id="e7187-122">`Single`、 `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="e7187-122">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="e7187-123">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-123">**Return Value**</span></span>

<span data-ttu-id="e7187-124">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-124">The type of `value`.</span></span>

<span data-ttu-id="e7187-125">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-125">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="e7187-126">Power(值, 指数)</span><span class="sxs-lookup"><span data-stu-id="e7187-126">Power(value, exponent)</span></span>

<span data-ttu-id="e7187-127">返回对指定的 `value` 求指定的 `exponent` 幂次所得的结果。</span><span class="sxs-lookup"><span data-stu-id="e7187-127">Returns the result of the specified `value` to the specified `exponent`.</span></span>

<span data-ttu-id="e7187-128">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-128">**Arguments**</span></span>

|  |  |
|--|--|
|`value` | <span data-ttu-id="e7187-129">`Int32, Int64, Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="e7187-129">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="e7187-130">`Int64`、 `Double` 或 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="e7187-130">An `Int64`, `Double`, or `Decimal`.</span></span> |

<span data-ttu-id="e7187-131">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-131">**Return Value**</span></span>

<span data-ttu-id="e7187-132">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-132">The type of `value`.</span></span>

<span data-ttu-id="e7187-133">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-133">**Example**</span></span>

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="e7187-134">Round(value)</span><span class="sxs-lookup"><span data-stu-id="e7187-134">Round(value)</span></span>

<span data-ttu-id="e7187-135">返回 `value` 的整数部分，舍入到最近的整数。</span><span class="sxs-lookup"><span data-stu-id="e7187-135">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

<span data-ttu-id="e7187-136">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-136">**Arguments**</span></span>

<span data-ttu-id="e7187-137">`Single`、 `Double` 和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="e7187-137">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="e7187-138">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-138">**Return Value**</span></span>

<span data-ttu-id="e7187-139">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-139">The type of `value`.</span></span>

<span data-ttu-id="e7187-140">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-140">**Example**</span></span>

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="e7187-141">Round(值, 位数)</span><span class="sxs-lookup"><span data-stu-id="e7187-141">Round(value, digits)</span></span>

<span data-ttu-id="e7187-142">返回 `value`，舍入到最近的指定 `digits`。</span><span class="sxs-lookup"><span data-stu-id="e7187-142">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

<span data-ttu-id="e7187-143">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-143">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="e7187-144">`Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="e7187-144">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="e7187-145">`Int16` 或 `Int32`。</span><span class="sxs-lookup"><span data-stu-id="e7187-145">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="e7187-146">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-146">**Return Value**</span></span>

<span data-ttu-id="e7187-147">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-147">The type of `value`.</span></span>

<span data-ttu-id="e7187-148">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-148">**Example**</span></span>

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="e7187-149">Truncate(值, 位数)</span><span class="sxs-lookup"><span data-stu-id="e7187-149">Truncate(value, digits)</span></span>

<span data-ttu-id="e7187-150">返回 `value`，截断至最近的指定 `digits`。</span><span class="sxs-lookup"><span data-stu-id="e7187-150">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

<span data-ttu-id="e7187-151">**参数**</span><span class="sxs-lookup"><span data-stu-id="e7187-151">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="e7187-152">`Double` 或 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="e7187-152">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="e7187-153">`Int16` 或 `Int32`。</span><span class="sxs-lookup"><span data-stu-id="e7187-153">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="e7187-154">**返回值**</span><span class="sxs-lookup"><span data-stu-id="e7187-154">**Return Value**</span></span>

<span data-ttu-id="e7187-155">`value` 的类型。</span><span class="sxs-lookup"><span data-stu-id="e7187-155">The type of `value`.</span></span>

<span data-ttu-id="e7187-156">**示例**</span><span class="sxs-lookup"><span data-stu-id="e7187-156">**Example**</span></span>

`Truncate(748.58,1)`  
  
 <span data-ttu-id="e7187-157">如果提供 `null` 输入，则这些函数返回 `null`。</span><span class="sxs-lookup"><span data-stu-id="e7187-157">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="e7187-158">Microsoft SQL 客户端托管提供程序中提供了等效功能。</span><span class="sxs-lookup"><span data-stu-id="e7187-158">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="e7187-159">有关详细信息，请参阅 [SqlClient for 实体框架函数](../sqlclient-for-ef-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="e7187-159">For more information, see [SqlClient for Entity Framework Functions](../sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7187-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="e7187-160">See also</span></span>

- [<span data-ttu-id="e7187-161">规范函数</span><span class="sxs-lookup"><span data-stu-id="e7187-161">Canonical Functions</span></span>](canonical-functions.md)

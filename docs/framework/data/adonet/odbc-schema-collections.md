---
description: 了解有关以下内容的详细信息： ODBC 架构集合
title: ODBC 架构集合
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: ceac67e49914db7010e315a2dfcdb630bea1e29f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786194"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="5ae7f-103">ODBC 架构集合</span><span class="sxs-lookup"><span data-stu-id="5ae7f-103">ODBC Schema Collections</span></span>

<span data-ttu-id="5ae7f-104">本节讨论对适用于 Microsoft SQL Server、Oracle 和 Microsoft Jet 的 ODBC 驱动程序的架构集合支持。</span><span class="sxs-lookup"><span data-stu-id="5ae7f-104">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>

## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="5ae7f-105">Microsoft SQL Server ODBC 驱动程序</span><span class="sxs-lookup"><span data-stu-id="5ae7f-105">Microsoft SQL Server ODBC Driver</span></span>

<span data-ttu-id="5ae7f-106">除了通用架构集合之外，Microsoft SQL Server ODBC 驱动程序还支持下列特定的架构集合：</span><span class="sxs-lookup"><span data-stu-id="5ae7f-106">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="5ae7f-107">表</span><span class="sxs-lookup"><span data-stu-id="5ae7f-107">Tables</span></span>

- <span data-ttu-id="5ae7f-108">索引</span><span class="sxs-lookup"><span data-stu-id="5ae7f-108">Indexes</span></span>

- <span data-ttu-id="5ae7f-109">列</span><span class="sxs-lookup"><span data-stu-id="5ae7f-109">Columns</span></span>

- <span data-ttu-id="5ae7f-110">过程</span><span class="sxs-lookup"><span data-stu-id="5ae7f-110">Procedures</span></span>

- <span data-ttu-id="5ae7f-111">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5ae7f-111">ProcedureColumns</span></span>

- <span data-ttu-id="5ae7f-112">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5ae7f-112">ProcedureParameters</span></span>

- <span data-ttu-id="5ae7f-113">视图</span><span class="sxs-lookup"><span data-stu-id="5ae7f-113">Views</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="5ae7f-114">表和视图</span><span class="sxs-lookup"><span data-stu-id="5ae7f-114">Tables and Views</span></span>

|<span data-ttu-id="5ae7f-115">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-115">ColumnName</span></span>|<span data-ttu-id="5ae7f-116">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-116">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-117">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-117">TABLE_CAT</span></span>|<span data-ttu-id="5ae7f-118">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-118">String</span></span>|
|<span data-ttu-id="5ae7f-119">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-119">TABLE_SCHEM</span></span>|<span data-ttu-id="5ae7f-120">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-120">String</span></span>|
|<span data-ttu-id="5ae7f-121">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-121">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-122">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-122">String</span></span>|
|<span data-ttu-id="5ae7f-123">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-123">TABLE_TYPE</span></span>|<span data-ttu-id="5ae7f-124">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-124">String</span></span>|
|<span data-ttu-id="5ae7f-125">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-125">REMARKS</span></span>|<span data-ttu-id="5ae7f-126">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-126">String</span></span>|

### <a name="indexes"></a><span data-ttu-id="5ae7f-127">索引</span><span class="sxs-lookup"><span data-stu-id="5ae7f-127">Indexes</span></span>

|<span data-ttu-id="5ae7f-128">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-128">ColumnName</span></span>|<span data-ttu-id="5ae7f-129">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-129">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-130">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-130">TABLE_CAT</span></span>|<span data-ttu-id="5ae7f-131">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-131">String</span></span>|
|<span data-ttu-id="5ae7f-132">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-132">TABLE_SCHEM</span></span>|<span data-ttu-id="5ae7f-133">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-133">String</span></span>|
|<span data-ttu-id="5ae7f-134">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-134">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-135">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-135">String</span></span>|
|<span data-ttu-id="5ae7f-136">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-136">NON_UNIQUE</span></span>|<span data-ttu-id="5ae7f-137">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-137">Int16</span></span>|
|<span data-ttu-id="5ae7f-138">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-138">INDEX_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-139">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-139">String</span></span>|
|<span data-ttu-id="5ae7f-140">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-140">INDEX_NAME</span></span>|<span data-ttu-id="5ae7f-141">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-141">String</span></span>|
|<span data-ttu-id="5ae7f-142">TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-142">TYPE</span></span>|<span data-ttu-id="5ae7f-143">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-143">Int16</span></span>|
|<span data-ttu-id="5ae7f-144">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-144">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-145">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-145">Int16</span></span>|
|<span data-ttu-id="5ae7f-146">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-146">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-147">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-147">String</span></span>|
|<span data-ttu-id="5ae7f-148">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="5ae7f-148">ASC_OR_DESC</span></span>|<span data-ttu-id="5ae7f-149">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-149">String</span></span>|
|<span data-ttu-id="5ae7f-150">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="5ae7f-150">CARDINALITY</span></span>|<span data-ttu-id="5ae7f-151">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-151">Int32</span></span>|
|<span data-ttu-id="5ae7f-152">PAGES</span><span class="sxs-lookup"><span data-stu-id="5ae7f-152">PAGES</span></span>|<span data-ttu-id="5ae7f-153">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-153">Int32</span></span>|
|<span data-ttu-id="5ae7f-154">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-154">FILTER_CONDITION</span></span>|<span data-ttu-id="5ae7f-155">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-155">String</span></span>|
|<span data-ttu-id="5ae7f-156">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ae7f-156">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5ae7f-157">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-157">String</span></span>|
|<span data-ttu-id="5ae7f-158">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-158">SS_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-159">Byte</span><span class="sxs-lookup"><span data-stu-id="5ae7f-159">Byte</span></span>|

### <a name="columns"></a><span data-ttu-id="5ae7f-160">列</span><span class="sxs-lookup"><span data-stu-id="5ae7f-160">Columns</span></span>

|<span data-ttu-id="5ae7f-161">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-161">ColumnName</span></span>|<span data-ttu-id="5ae7f-162">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-162">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-163">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-163">TABLE_CAT</span></span>|<span data-ttu-id="5ae7f-164">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-164">String</span></span>|
|<span data-ttu-id="5ae7f-165">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-165">TABLE_SCHEM</span></span>|<span data-ttu-id="5ae7f-166">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-166">String</span></span>|
|<span data-ttu-id="5ae7f-167">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-167">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-168">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-168">String</span></span>|
|<span data-ttu-id="5ae7f-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-169">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-170">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-170">String</span></span>|
|<span data-ttu-id="5ae7f-171">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-171">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-172">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-172">Int16</span></span>|
|<span data-ttu-id="5ae7f-173">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-173">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-174">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-174">String</span></span>|
|<span data-ttu-id="5ae7f-175">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-175">COLUMN_SIZE</span></span>|<span data-ttu-id="5ae7f-176">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-176">Int32</span></span>|
|<span data-ttu-id="5ae7f-177">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-177">BUFFER_LENGTH</span></span>|<span data-ttu-id="5ae7f-178">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-178">Int32</span></span>|
|<span data-ttu-id="5ae7f-179">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-179">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5ae7f-180">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-180">Int16</span></span>|
|<span data-ttu-id="5ae7f-181">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-181">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5ae7f-182">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-182">Int16</span></span>|
|<span data-ttu-id="5ae7f-183">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-183">NULLABLE</span></span>|<span data-ttu-id="5ae7f-184">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-184">Int16</span></span>|
|<span data-ttu-id="5ae7f-185">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-185">REMARKS</span></span>|<span data-ttu-id="5ae7f-186">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-186">String</span></span>|
|<span data-ttu-id="5ae7f-187">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5ae7f-187">COLUMN_DEF</span></span>|<span data-ttu-id="5ae7f-188">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-188">String</span></span>|
|<span data-ttu-id="5ae7f-189">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-189">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-190">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-190">Int16</span></span>|
|<span data-ttu-id="5ae7f-191">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5ae7f-191">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5ae7f-192">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-192">Int16</span></span>|
|<span data-ttu-id="5ae7f-193">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-193">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5ae7f-194">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-194">Int32</span></span>|
|<span data-ttu-id="5ae7f-195">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-195">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-196">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-196">Int32</span></span>|
|<span data-ttu-id="5ae7f-197">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-197">IS_NULLABLE</span></span>|<span data-ttu-id="5ae7f-198">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-198">String</span></span>|
|<span data-ttu-id="5ae7f-199">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ae7f-199">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="5ae7f-200">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-200">String</span></span>|
|<span data-ttu-id="5ae7f-201">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ae7f-201">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5ae7f-202">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-202">String</span></span>|
|<span data-ttu-id="5ae7f-203">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-203">SS_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-204">Byte</span><span class="sxs-lookup"><span data-stu-id="5ae7f-204">Byte</span></span>|

### <a name="procedures"></a><span data-ttu-id="5ae7f-205">过程</span><span class="sxs-lookup"><span data-stu-id="5ae7f-205">Procedures</span></span>

|<span data-ttu-id="5ae7f-206">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-206">ColumnName</span></span>|<span data-ttu-id="5ae7f-207">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-207">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-208">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-208">PROCEDURE_CAT</span></span>|<span data-ttu-id="5ae7f-209">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-209">String</span></span>|
|<span data-ttu-id="5ae7f-210">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-210">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5ae7f-211">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-211">String</span></span>|
|<span data-ttu-id="5ae7f-212">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-212">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-213">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-213">String</span></span>|
|<span data-ttu-id="5ae7f-214">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-214">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="5ae7f-215">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-215">Int32</span></span>|
|<span data-ttu-id="5ae7f-216">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-216">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="5ae7f-217">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-217">Int32</span></span>|
|<span data-ttu-id="5ae7f-218">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-218">NUM_RESULT_SETS</span></span>|<span data-ttu-id="5ae7f-219">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-219">Int32</span></span>|
|<span data-ttu-id="5ae7f-220">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-220">REMARKS</span></span>|<span data-ttu-id="5ae7f-221">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-221">String</span></span>|
|<span data-ttu-id="5ae7f-222">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-222">PROCEDURE_TYPE</span></span>|<span data-ttu-id="5ae7f-223">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-223">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="5ae7f-224">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5ae7f-224">ProcedureColumns</span></span>

|<span data-ttu-id="5ae7f-225">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-225">ColumnName</span></span>|<span data-ttu-id="5ae7f-226">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-226">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-227">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-227">PROCEDURE_CAT</span></span>|<span data-ttu-id="5ae7f-228">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-228">String</span></span>|
|<span data-ttu-id="5ae7f-229">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-229">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5ae7f-230">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-230">String</span></span>|
|<span data-ttu-id="5ae7f-231">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-231">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-232">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-232">String</span></span>|
|<span data-ttu-id="5ae7f-233">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-233">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-234">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-234">String</span></span>|
|<span data-ttu-id="5ae7f-235">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-235">COLUMN_TYPE</span></span>|<span data-ttu-id="5ae7f-236">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-236">Int16</span></span>|
|<span data-ttu-id="5ae7f-237">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-237">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-238">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-238">Int16</span></span>|
|<span data-ttu-id="5ae7f-239">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-239">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-240">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-240">String</span></span>|
|<span data-ttu-id="5ae7f-241">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-241">COLUMN_SIZE</span></span>|<span data-ttu-id="5ae7f-242">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-242">Int32</span></span>|
|<span data-ttu-id="5ae7f-243">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-243">BUFFER_LENGTH</span></span>|<span data-ttu-id="5ae7f-244">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-244">Int32</span></span>|
|<span data-ttu-id="5ae7f-245">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-245">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5ae7f-246">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-246">Int16</span></span>|
|<span data-ttu-id="5ae7f-247">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-247">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5ae7f-248">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-248">Int16</span></span>|
|<span data-ttu-id="5ae7f-249">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-249">NULLABLE</span></span>|<span data-ttu-id="5ae7f-250">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-250">Int16</span></span>|
|<span data-ttu-id="5ae7f-251">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-251">REMARKS</span></span>|<span data-ttu-id="5ae7f-252">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-252">String</span></span>|
|<span data-ttu-id="5ae7f-253">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5ae7f-253">COLUMN_DEF</span></span>|<span data-ttu-id="5ae7f-254">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-254">String</span></span>|
|<span data-ttu-id="5ae7f-255">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-255">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-256">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-256">Int16</span></span>|
|<span data-ttu-id="5ae7f-257">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5ae7f-257">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5ae7f-258">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-258">Int16</span></span>|
|<span data-ttu-id="5ae7f-259">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-259">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5ae7f-260">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-260">Int32</span></span>|
|<span data-ttu-id="5ae7f-261">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-261">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-262">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-262">Int32</span></span>|
|<span data-ttu-id="5ae7f-263">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-263">IS_NULLABLE</span></span>|<span data-ttu-id="5ae7f-264">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-264">String</span></span>|
|<span data-ttu-id="5ae7f-265">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ae7f-265">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="5ae7f-266">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-266">String</span></span>|
|<span data-ttu-id="5ae7f-267">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ae7f-267">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5ae7f-268">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-268">String</span></span>|
|<span data-ttu-id="5ae7f-269">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-269">SS_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-270">Byte</span><span class="sxs-lookup"><span data-stu-id="5ae7f-270">Byte</span></span>|

### <a name="procedureparameters"></a><span data-ttu-id="5ae7f-271">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5ae7f-271">ProcedureParameters</span></span>

|<span data-ttu-id="5ae7f-272">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-272">ColumnName</span></span>|<span data-ttu-id="5ae7f-273">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-273">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-274">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-274">PROCEDURE_CAT</span></span>|<span data-ttu-id="5ae7f-275">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-275">String</span></span>|
|<span data-ttu-id="5ae7f-276">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-276">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5ae7f-277">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-277">String</span></span>|
|<span data-ttu-id="5ae7f-278">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-278">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-279">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-279">String</span></span>|
|<span data-ttu-id="5ae7f-280">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-280">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-281">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-281">String</span></span>|
|<span data-ttu-id="5ae7f-282">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-282">COLUMN_TYPE</span></span>|<span data-ttu-id="5ae7f-283">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-283">Int16</span></span>|
|<span data-ttu-id="5ae7f-284">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-284">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-285">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-285">Int16</span></span>|
|<span data-ttu-id="5ae7f-286">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-286">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-287">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-287">String</span></span>|
|<span data-ttu-id="5ae7f-288">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-288">COLUMN_SIZE</span></span>|<span data-ttu-id="5ae7f-289">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-289">Int32</span></span>|
|<span data-ttu-id="5ae7f-290">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-290">BUFFER_LENGTH</span></span>|<span data-ttu-id="5ae7f-291">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-291">Int32</span></span>|
|<span data-ttu-id="5ae7f-292">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-292">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5ae7f-293">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-293">Int16</span></span>|
|<span data-ttu-id="5ae7f-294">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-294">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5ae7f-295">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-295">Int16</span></span>|
|<span data-ttu-id="5ae7f-296">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-296">NULLABLE</span></span>|<span data-ttu-id="5ae7f-297">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-297">Int16</span></span>|
|<span data-ttu-id="5ae7f-298">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-298">REMARKS</span></span>|<span data-ttu-id="5ae7f-299">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-299">String</span></span>|
|<span data-ttu-id="5ae7f-300">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5ae7f-300">COLUMN_DEF</span></span>|<span data-ttu-id="5ae7f-301">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-301">String</span></span>|
|<span data-ttu-id="5ae7f-302">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-302">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-303">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-303">Int16</span></span>|
|<span data-ttu-id="5ae7f-304">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5ae7f-304">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5ae7f-305">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-305">Int16</span></span>|
|<span data-ttu-id="5ae7f-306">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-306">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5ae7f-307">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-307">Int32</span></span>|
|<span data-ttu-id="5ae7f-308">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-308">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-309">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-309">Int32</span></span>|
|<span data-ttu-id="5ae7f-310">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-310">IS_NULLABLE</span></span>|<span data-ttu-id="5ae7f-311">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-311">String</span></span>|
|<span data-ttu-id="5ae7f-312">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ae7f-312">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="5ae7f-313">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-313">String</span></span>|
|<span data-ttu-id="5ae7f-314">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ae7f-314">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5ae7f-315">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-315">String</span></span>|
|<span data-ttu-id="5ae7f-316">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-316">SS_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-317">Byte</span><span class="sxs-lookup"><span data-stu-id="5ae7f-317">Byte</span></span>|

## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="5ae7f-318">Microsoft Oracle ODBC 驱动程序</span><span class="sxs-lookup"><span data-stu-id="5ae7f-318">Microsoft Oracle ODBC Driver</span></span>

<span data-ttu-id="5ae7f-319">除了通用架构集合之外，Microsoft SQL Server Oracle ODBC 驱动程序还支持下列特定的架构集合：</span><span class="sxs-lookup"><span data-stu-id="5ae7f-319">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="5ae7f-320">表</span><span class="sxs-lookup"><span data-stu-id="5ae7f-320">Tables</span></span>

- <span data-ttu-id="5ae7f-321">列</span><span class="sxs-lookup"><span data-stu-id="5ae7f-321">Columns</span></span>

- <span data-ttu-id="5ae7f-322">过程</span><span class="sxs-lookup"><span data-stu-id="5ae7f-322">Procedures</span></span>

- <span data-ttu-id="5ae7f-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5ae7f-323">ProcedureColumns</span></span>

- <span data-ttu-id="5ae7f-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5ae7f-324">ProcedureParameters</span></span>

- <span data-ttu-id="5ae7f-325">视图</span><span class="sxs-lookup"><span data-stu-id="5ae7f-325">Views</span></span>

- <span data-ttu-id="5ae7f-326">索引</span><span class="sxs-lookup"><span data-stu-id="5ae7f-326">Indexes</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="5ae7f-327">表和视图</span><span class="sxs-lookup"><span data-stu-id="5ae7f-327">Tables and Views</span></span>

|<span data-ttu-id="5ae7f-328">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-328">ColumnName</span></span>|<span data-ttu-id="5ae7f-329">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-329">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-330">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-330">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-331">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-331">String</span></span>|
|<span data-ttu-id="5ae7f-332">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-332">TABLE_OWNER</span></span>|<span data-ttu-id="5ae7f-333">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-333">String</span></span>|
|<span data-ttu-id="5ae7f-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-334">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-335">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-335">String</span></span>|
|<span data-ttu-id="5ae7f-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-336">TABLE_TYPE</span></span>|<span data-ttu-id="5ae7f-337">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-337">String</span></span>|
|<span data-ttu-id="5ae7f-338">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-338">REMARKS</span></span>|<span data-ttu-id="5ae7f-339">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-339">String</span></span>|

### <a name="columns"></a><span data-ttu-id="5ae7f-340">列</span><span class="sxs-lookup"><span data-stu-id="5ae7f-340">Columns</span></span>

|<span data-ttu-id="5ae7f-341">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-341">ColumnName</span></span>|<span data-ttu-id="5ae7f-342">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-342">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-343">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-343">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-344">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-344">String</span></span>|
|<span data-ttu-id="5ae7f-345">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-345">TABLE_OWNER</span></span>|<span data-ttu-id="5ae7f-346">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-346">String</span></span>|
|<span data-ttu-id="5ae7f-347">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-347">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-348">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-348">String</span></span>|
|<span data-ttu-id="5ae7f-349">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-349">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-350">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-350">String</span></span>|
|<span data-ttu-id="5ae7f-351">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-351">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-352">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-352">Int16</span></span>|
|<span data-ttu-id="5ae7f-353">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-353">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-354">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-354">String</span></span>|
|<span data-ttu-id="5ae7f-355">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-355">PRECISION</span></span>|<span data-ttu-id="5ae7f-356">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-356">Int32</span></span>|
|<span data-ttu-id="5ae7f-357">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-357">LENGTH</span></span>|<span data-ttu-id="5ae7f-358">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-358">Int32</span></span>|
|<span data-ttu-id="5ae7f-359">SCALE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-359">SCALE</span></span>|<span data-ttu-id="5ae7f-360">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-360">Int16</span></span>|
|<span data-ttu-id="5ae7f-361">RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-361">RADIX</span></span>|<span data-ttu-id="5ae7f-362">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-362">Int16</span></span>|
|<span data-ttu-id="5ae7f-363">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-363">NULLABLE</span></span>|<span data-ttu-id="5ae7f-364">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-364">Int16</span></span>|
|<span data-ttu-id="5ae7f-365">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-365">REMARKS</span></span>|<span data-ttu-id="5ae7f-366">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-366">String</span></span>|
|<span data-ttu-id="5ae7f-367">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-367">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-368">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-368">Int32</span></span>|

### <a name="procedures"></a><span data-ttu-id="5ae7f-369">过程</span><span class="sxs-lookup"><span data-stu-id="5ae7f-369">Procedures</span></span>

|<span data-ttu-id="5ae7f-370">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-370">ColumnName</span></span>|<span data-ttu-id="5ae7f-371">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-371">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-372">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-372">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-373">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-373">String</span></span>|
|<span data-ttu-id="5ae7f-374">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-374">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5ae7f-375">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-375">String</span></span>|
|<span data-ttu-id="5ae7f-376">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-376">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-377">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-377">String</span></span>|
|<span data-ttu-id="5ae7f-378">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-378">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="5ae7f-379">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-379">Int16</span></span>|
|<span data-ttu-id="5ae7f-380">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-380">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="5ae7f-381">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-381">Int16</span></span>|
|<span data-ttu-id="5ae7f-382">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-382">NUM_RESULT_SETS</span></span>|<span data-ttu-id="5ae7f-383">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-383">Int16</span></span>|
|<span data-ttu-id="5ae7f-384">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-384">REMARKS</span></span>|<span data-ttu-id="5ae7f-385">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-385">String</span></span>|
|<span data-ttu-id="5ae7f-386">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-386">PROCEDURE_TYPE</span></span>|<span data-ttu-id="5ae7f-387">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-387">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="5ae7f-388">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5ae7f-388">ProcedureColumns</span></span>

|<span data-ttu-id="5ae7f-389">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-389">ColumnName</span></span>|<span data-ttu-id="5ae7f-390">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-390">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-391">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-391">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-392">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-392">String</span></span>|
|<span data-ttu-id="5ae7f-393">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-393">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5ae7f-394">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-394">String</span></span>|
|<span data-ttu-id="5ae7f-395">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-395">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-396">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-396">String</span></span>|
|<span data-ttu-id="5ae7f-397">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-397">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-398">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-398">String</span></span>|
|<span data-ttu-id="5ae7f-399">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-399">COLUMN_TYPE</span></span>|<span data-ttu-id="5ae7f-400">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-400">Int16</span></span>|
|<span data-ttu-id="5ae7f-401">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-401">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-402">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-402">Int16</span></span>|
|<span data-ttu-id="5ae7f-403">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-403">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-404">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-404">String</span></span>|
|<span data-ttu-id="5ae7f-405">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-405">PRECISION</span></span>|<span data-ttu-id="5ae7f-406">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-406">Int32</span></span>|
|<span data-ttu-id="5ae7f-407">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-407">LENGTH</span></span>|<span data-ttu-id="5ae7f-408">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-408">Int32</span></span>|
|<span data-ttu-id="5ae7f-409">SCALE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-409">SCALE</span></span>|<span data-ttu-id="5ae7f-410">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-410">Int16</span></span>|
|<span data-ttu-id="5ae7f-411">RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-411">RADIX</span></span>|<span data-ttu-id="5ae7f-412">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-412">Int16</span></span>|
|<span data-ttu-id="5ae7f-413">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-413">NULLABLE</span></span>|<span data-ttu-id="5ae7f-414">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-414">Int16</span></span>|
|<span data-ttu-id="5ae7f-415">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-415">REMARKS</span></span>|<span data-ttu-id="5ae7f-416">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-416">String</span></span>|
|<span data-ttu-id="5ae7f-417">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="5ae7f-417">OVERLOAD</span></span>|<span data-ttu-id="5ae7f-418">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-418">Int32</span></span>|
|<span data-ttu-id="5ae7f-419">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-419">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-420">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-420">Int32</span></span>|

## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="5ae7f-421">Microsoft Jet ODBC 驱动程序</span><span class="sxs-lookup"><span data-stu-id="5ae7f-421">Microsoft Jet ODBC Driver</span></span>

<span data-ttu-id="5ae7f-422">除了通用架构集合之外，Microsoft Jet ODBC 驱动程序还支持下列特定的架构集合：</span><span class="sxs-lookup"><span data-stu-id="5ae7f-422">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="5ae7f-423">表</span><span class="sxs-lookup"><span data-stu-id="5ae7f-423">Tables</span></span>

- <span data-ttu-id="5ae7f-424">索引</span><span class="sxs-lookup"><span data-stu-id="5ae7f-424">Indexes</span></span>

- <span data-ttu-id="5ae7f-425">列</span><span class="sxs-lookup"><span data-stu-id="5ae7f-425">Columns</span></span>

- <span data-ttu-id="5ae7f-426">过程</span><span class="sxs-lookup"><span data-stu-id="5ae7f-426">Procedures</span></span>

- <span data-ttu-id="5ae7f-427">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5ae7f-427">ProcedureColumns</span></span>

- <span data-ttu-id="5ae7f-428">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5ae7f-428">ProcedureParameters</span></span>

- <span data-ttu-id="5ae7f-429">视图</span><span class="sxs-lookup"><span data-stu-id="5ae7f-429">Views</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="5ae7f-430">表和视图</span><span class="sxs-lookup"><span data-stu-id="5ae7f-430">Tables and Views</span></span>

|<span data-ttu-id="5ae7f-431">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-431">ColumnName</span></span>|<span data-ttu-id="5ae7f-432">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-432">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-433">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-433">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-434">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-434">String</span></span>|
|<span data-ttu-id="5ae7f-435">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-435">TABLE_OWNER</span></span>|<span data-ttu-id="5ae7f-436">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-436">String</span></span>|
|<span data-ttu-id="5ae7f-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-437">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-438">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-438">String</span></span>|
|<span data-ttu-id="5ae7f-439">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-439">TABLE_TYPE</span></span>|<span data-ttu-id="5ae7f-440">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-440">String</span></span>|
|<span data-ttu-id="5ae7f-441">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-441">REMARKS</span></span>|<span data-ttu-id="5ae7f-442">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-442">String</span></span>|

### <a name="columns"></a><span data-ttu-id="5ae7f-443">列</span><span class="sxs-lookup"><span data-stu-id="5ae7f-443">Columns</span></span>

|<span data-ttu-id="5ae7f-444">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-444">ColumnName</span></span>|<span data-ttu-id="5ae7f-445">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-445">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-446">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-446">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-447">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-447">String</span></span>|
|<span data-ttu-id="5ae7f-448">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-448">TABLE_OWNER</span></span>|<span data-ttu-id="5ae7f-449">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-449">String</span></span>|
|<span data-ttu-id="5ae7f-450">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-450">TABLE_NAME</span></span>|<span data-ttu-id="5ae7f-451">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-451">String</span></span>|
|<span data-ttu-id="5ae7f-452">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-452">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-453">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-453">String</span></span>|
|<span data-ttu-id="5ae7f-454">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-454">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-455">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-455">Int16</span></span>|
|<span data-ttu-id="5ae7f-456">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-456">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-457">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-457">String</span></span>|
|<span data-ttu-id="5ae7f-458">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-458">PRECISION</span></span>|<span data-ttu-id="5ae7f-459">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-459">Int32</span></span>|
|<span data-ttu-id="5ae7f-460">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-460">LENGTH</span></span>|<span data-ttu-id="5ae7f-461">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-461">Int32</span></span>|
|<span data-ttu-id="5ae7f-462">SCALE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-462">SCALE</span></span>|<span data-ttu-id="5ae7f-463">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-463">Int16</span></span>|
|<span data-ttu-id="5ae7f-464">RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-464">RADIX</span></span>|<span data-ttu-id="5ae7f-465">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-465">Int16</span></span>|
|<span data-ttu-id="5ae7f-466">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-466">NULLABLE</span></span>|<span data-ttu-id="5ae7f-467">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-467">Int16</span></span>|
|<span data-ttu-id="5ae7f-468">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-468">REMARKS</span></span>|<span data-ttu-id="5ae7f-469">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-469">String</span></span>|
|<span data-ttu-id="5ae7f-470">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-470">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-471">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-471">Int32</span></span>|

### <a name="procedures"></a><span data-ttu-id="5ae7f-472">过程</span><span class="sxs-lookup"><span data-stu-id="5ae7f-472">Procedures</span></span>

|<span data-ttu-id="5ae7f-473">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-473">ColumnName</span></span>|<span data-ttu-id="5ae7f-474">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-474">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-475">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-475">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-476">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-476">String</span></span>|
|<span data-ttu-id="5ae7f-477">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-477">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5ae7f-478">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-478">String</span></span>|
|<span data-ttu-id="5ae7f-479">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-479">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-480">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-480">String</span></span>|
|<span data-ttu-id="5ae7f-481">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-481">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="5ae7f-482">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-482">Int16</span></span>|
|<span data-ttu-id="5ae7f-483">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-483">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="5ae7f-484">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-484">Int16</span></span>|
|<span data-ttu-id="5ae7f-485">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-485">NUM_RESULT_SETS</span></span>|<span data-ttu-id="5ae7f-486">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-486">Int16</span></span>|
|<span data-ttu-id="5ae7f-487">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-487">REMARKS</span></span>|<span data-ttu-id="5ae7f-488">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-488">String</span></span>|
|<span data-ttu-id="5ae7f-489">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-489">PROCEDURE_TYPE</span></span>|<span data-ttu-id="5ae7f-490">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-490">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="5ae7f-491">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5ae7f-491">ProcedureColumns</span></span>

|<span data-ttu-id="5ae7f-492">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-492">ColumnName</span></span>|<span data-ttu-id="5ae7f-493">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-493">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-494">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-494">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5ae7f-495">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-495">String</span></span>|
|<span data-ttu-id="5ae7f-496">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ae7f-496">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5ae7f-497">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-497">String</span></span>|
|<span data-ttu-id="5ae7f-498">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-498">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-499">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-499">String</span></span>|
|<span data-ttu-id="5ae7f-500">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-500">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-501">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-501">String</span></span>|
|<span data-ttu-id="5ae7f-502">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-502">COLUMN_TYPE</span></span>|<span data-ttu-id="5ae7f-503">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-503">Int16</span></span>|
|<span data-ttu-id="5ae7f-504">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-504">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-505">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-505">Int16</span></span>|
|<span data-ttu-id="5ae7f-506">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-506">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-507">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-507">String</span></span>|
|<span data-ttu-id="5ae7f-508">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-508">PRECISION</span></span>|<span data-ttu-id="5ae7f-509">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-509">Int32</span></span>|
|<span data-ttu-id="5ae7f-510">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-510">LENGTH</span></span>|<span data-ttu-id="5ae7f-511">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-511">Int32</span></span>|
|<span data-ttu-id="5ae7f-512">SCALE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-512">SCALE</span></span>|<span data-ttu-id="5ae7f-513">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-513">Int16</span></span>|
|<span data-ttu-id="5ae7f-514">RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-514">RADIX</span></span>|<span data-ttu-id="5ae7f-515">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-515">Int16</span></span>|
|<span data-ttu-id="5ae7f-516">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-516">NULLABLE</span></span>|<span data-ttu-id="5ae7f-517">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-517">Int16</span></span>|
|<span data-ttu-id="5ae7f-518">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-518">REMARKS</span></span>|<span data-ttu-id="5ae7f-519">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-519">String</span></span>|
|<span data-ttu-id="5ae7f-520">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="5ae7f-520">OVERLOAD</span></span>|<span data-ttu-id="5ae7f-521">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-521">Int32</span></span>|
|<span data-ttu-id="5ae7f-522">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-522">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-523">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-523">Int32</span></span>|

### <a name="procedureparameters"></a><span data-ttu-id="5ae7f-524">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5ae7f-524">ProcedureParameters</span></span>

|<span data-ttu-id="5ae7f-525">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5ae7f-525">ColumnName</span></span>|<span data-ttu-id="5ae7f-526">数据类型</span><span class="sxs-lookup"><span data-stu-id="5ae7f-526">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="5ae7f-527">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5ae7f-527">PROCEDURE_CAT</span></span>|<span data-ttu-id="5ae7f-528">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-528">String</span></span>|
|<span data-ttu-id="5ae7f-529">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5ae7f-529">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5ae7f-530">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-530">String</span></span>|
|<span data-ttu-id="5ae7f-531">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-531">PROCEDURE_NAME</span></span>|<span data-ttu-id="5ae7f-532">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-532">String</span></span>|
|<span data-ttu-id="5ae7f-533">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-533">COLUMN_NAME</span></span>|<span data-ttu-id="5ae7f-534">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-534">String</span></span>|
|<span data-ttu-id="5ae7f-535">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-535">COLUMN_TYPE</span></span>|<span data-ttu-id="5ae7f-536">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-536">Int16</span></span>|
|<span data-ttu-id="5ae7f-537">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-537">DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-538">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-538">Int16</span></span>|
|<span data-ttu-id="5ae7f-539">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ae7f-539">TYPE_NAME</span></span>|<span data-ttu-id="5ae7f-540">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-540">String</span></span>|
|<span data-ttu-id="5ae7f-541">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-541">COLUMN_SIZE</span></span>|<span data-ttu-id="5ae7f-542">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-542">Int32</span></span>|
|<span data-ttu-id="5ae7f-543">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-543">BUFFER_LENGTH</span></span>|<span data-ttu-id="5ae7f-544">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-544">Int32</span></span>|
|<span data-ttu-id="5ae7f-545">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-545">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5ae7f-546">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-546">Int16</span></span>|
|<span data-ttu-id="5ae7f-547">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5ae7f-547">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5ae7f-548">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-548">Int16</span></span>|
|<span data-ttu-id="5ae7f-549">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-549">NULLABLE</span></span>|<span data-ttu-id="5ae7f-550">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-550">Int16</span></span>|
|<span data-ttu-id="5ae7f-551">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5ae7f-551">REMARKS</span></span>|<span data-ttu-id="5ae7f-552">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-552">String</span></span>|
|<span data-ttu-id="5ae7f-553">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5ae7f-553">COLUMN_DEF</span></span>|<span data-ttu-id="5ae7f-554">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-554">String</span></span>|
|<span data-ttu-id="5ae7f-555">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-555">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5ae7f-556">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-556">Int16</span></span>|
|<span data-ttu-id="5ae7f-557">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5ae7f-557">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5ae7f-558">Int16</span><span class="sxs-lookup"><span data-stu-id="5ae7f-558">Int16</span></span>|
|<span data-ttu-id="5ae7f-559">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5ae7f-559">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5ae7f-560">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-560">Int32</span></span>|
|<span data-ttu-id="5ae7f-561">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5ae7f-561">ORDINAL_POSITION</span></span>|<span data-ttu-id="5ae7f-562">Int32</span><span class="sxs-lookup"><span data-stu-id="5ae7f-562">Int32</span></span>|
|<span data-ttu-id="5ae7f-563">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5ae7f-563">IS_NULLABLE</span></span>|<span data-ttu-id="5ae7f-564">字符串</span><span class="sxs-lookup"><span data-stu-id="5ae7f-564">String</span></span>|

## <a name="see-also"></a><span data-ttu-id="5ae7f-565">请参阅</span><span class="sxs-lookup"><span data-stu-id="5ae7f-565">See also</span></span>

- [<span data-ttu-id="5ae7f-566">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="5ae7f-566">ADO.NET Overview</span></span>](ado-net-overview.md)

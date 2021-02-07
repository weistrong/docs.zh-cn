---
description: 了解详细信息： OLE DB 架构集合
title: OLE DB 架构集合
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: d4d4bae5387575bdaeaf013ed690e95aa3259068
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672616"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="3165a-103">OLE DB 架构集合</span><span class="sxs-lookup"><span data-stu-id="3165a-103">OLE DB Schema Collections</span></span>

<span data-ttu-id="3165a-104">本节讨论对适用于 Microsoft SQL Server、Oracle 和 Microsoft Jet 的 OLE DB 提供程序的架构集合支持</span><span class="sxs-lookup"><span data-stu-id="3165a-104">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="3165a-105">Microsoft SQL Server OLE DB 提供程序</span><span class="sxs-lookup"><span data-stu-id="3165a-105">Microsoft SQL Server OLE DB Provider</span></span>  

 <span data-ttu-id="3165a-106">除了通用架构集合之外，Microsoft SQL Server OLE DB 驱动程序还支持下列特定的架构集合：</span><span class="sxs-lookup"><span data-stu-id="3165a-106">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
- <span data-ttu-id="3165a-107">表</span><span class="sxs-lookup"><span data-stu-id="3165a-107">Tables</span></span>  
  
- <span data-ttu-id="3165a-108">列</span><span class="sxs-lookup"><span data-stu-id="3165a-108">Columns</span></span>  
  
- <span data-ttu-id="3165a-109">过程</span><span class="sxs-lookup"><span data-stu-id="3165a-109">Procedures</span></span>  
  
- <span data-ttu-id="3165a-110">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3165a-110">ProcedureParameters</span></span>  
  
- <span data-ttu-id="3165a-111">目录</span><span class="sxs-lookup"><span data-stu-id="3165a-111">Catalog</span></span>  
  
- <span data-ttu-id="3165a-112">索引</span><span class="sxs-lookup"><span data-stu-id="3165a-112">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="3165a-113">表</span><span class="sxs-lookup"><span data-stu-id="3165a-113">Tables</span></span>  
  
|<span data-ttu-id="3165a-114">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-114">ColumnName</span></span>|<span data-ttu-id="3165a-115">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-116">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-116">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-117">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-117">String</span></span>|  
|<span data-ttu-id="3165a-118">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-118">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-119">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-119">String</span></span>|  
|<span data-ttu-id="3165a-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-120">TABLE_NAME</span></span>|<span data-ttu-id="3165a-121">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-121">String</span></span>|  
|<span data-ttu-id="3165a-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-122">TABLE_TYPE</span></span>|<span data-ttu-id="3165a-123">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-123">String</span></span>|  
|<span data-ttu-id="3165a-124">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-124">TABLE_GUID</span></span>|<span data-ttu-id="3165a-125">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-125">Guid</span></span>|  
|<span data-ttu-id="3165a-126">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-126">DESCRIPTION</span></span>|<span data-ttu-id="3165a-127">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-127">String</span></span>|  
|<span data-ttu-id="3165a-128">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-128">TABLE_PROPID</span></span>|<span data-ttu-id="3165a-129">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-129">Int64</span></span>|  
|<span data-ttu-id="3165a-130">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-130">DATE_CREATED</span></span>|<span data-ttu-id="3165a-131">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-131">DateTime</span></span>|  
|<span data-ttu-id="3165a-132">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-132">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-133">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-133">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="3165a-134">列</span><span class="sxs-lookup"><span data-stu-id="3165a-134">Columns</span></span>  
  
|<span data-ttu-id="3165a-135">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-135">ColumnName</span></span>|<span data-ttu-id="3165a-136">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-136">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-137">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-137">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-138">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-138">String</span></span>|  
|<span data-ttu-id="3165a-139">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-139">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-140">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-140">String</span></span>|  
|<span data-ttu-id="3165a-141">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-141">TABLE_NAME</span></span>|<span data-ttu-id="3165a-142">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-142">String</span></span>|  
|<span data-ttu-id="3165a-143">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-143">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-144">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-144">String</span></span>|  
|<span data-ttu-id="3165a-145">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-145">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-146">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-146">Guid</span></span>|  
|<span data-ttu-id="3165a-147">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-147">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-148">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-148">Int64</span></span>|  
|<span data-ttu-id="3165a-149">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-149">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-150">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-150">Int64</span></span>|  
|<span data-ttu-id="3165a-151">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-151">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="3165a-152">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-152">Boolean</span></span>|  
|<span data-ttu-id="3165a-153">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-153">COLUMN_DEFAULT</span></span>|<span data-ttu-id="3165a-154">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-154">String</span></span>|  
|<span data-ttu-id="3165a-155">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3165a-155">COLUMN_FLAGS</span></span>|<span data-ttu-id="3165a-156">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-156">Int64</span></span>|  
|<span data-ttu-id="3165a-157">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-157">IS_NULLABLE</span></span>|<span data-ttu-id="3165a-158">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-158">Boolean</span></span>|  
|<span data-ttu-id="3165a-159">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-159">DATA_TYPE</span></span>|<span data-ttu-id="3165a-160">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-160">Int32</span></span>|  
|<span data-ttu-id="3165a-161">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-161">TYPE_GUID</span></span>|<span data-ttu-id="3165a-162">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-162">Guid</span></span>|  
|<span data-ttu-id="3165a-163">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-163">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="3165a-164">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-164">Int64</span></span>|  
|<span data-ttu-id="3165a-165">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-165">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="3165a-166">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-166">Int64</span></span>|  
|<span data-ttu-id="3165a-167">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-167">NUMERIC_PRECISION</span></span>|<span data-ttu-id="3165a-168">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-168">Int32</span></span>|  
|<span data-ttu-id="3165a-169">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="3165a-169">NUMERIC_SCALE</span></span>|<span data-ttu-id="3165a-170">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-170">Int16</span></span>|  
|<span data-ttu-id="3165a-171">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-171">DATETIME_PRECISION</span></span>|<span data-ttu-id="3165a-172">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-172">Int64</span></span>|  
|<span data-ttu-id="3165a-173">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-173">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="3165a-174">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-174">String</span></span>|  
|<span data-ttu-id="3165a-175">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-175">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="3165a-176">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-176">String</span></span>|  
|<span data-ttu-id="3165a-177">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-177">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="3165a-178">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-178">String</span></span>|  
|<span data-ttu-id="3165a-179">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-179">COLLATION_CATALOG</span></span>|<span data-ttu-id="3165a-180">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-180">String</span></span>|  
|<span data-ttu-id="3165a-181">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-181">COLLATION_SCHEMA</span></span>|<span data-ttu-id="3165a-182">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-182">String</span></span>|  
|<span data-ttu-id="3165a-183">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-183">COLLATION_NAME</span></span>|<span data-ttu-id="3165a-184">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-184">String</span></span>|  
|<span data-ttu-id="3165a-185">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-185">DOMAIN_CATALOG</span></span>|<span data-ttu-id="3165a-186">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-186">String</span></span>|  
|<span data-ttu-id="3165a-187">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-187">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="3165a-188">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-188">String</span></span>|  
|<span data-ttu-id="3165a-189">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-189">DOMAIN_NAME</span></span>|<span data-ttu-id="3165a-190">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-190">String</span></span>|  
|<span data-ttu-id="3165a-191">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-191">DESCRIPTION</span></span>|<span data-ttu-id="3165a-192">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-192">String</span></span>|  
|<span data-ttu-id="3165a-193">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="3165a-193">COLUMN_LCID</span></span>|<span data-ttu-id="3165a-194">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-194">Int32</span></span>|  
|<span data-ttu-id="3165a-195">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="3165a-195">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="3165a-196">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-196">Int32</span></span>|  
|<span data-ttu-id="3165a-197">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="3165a-197">COLUMN_SORTID</span></span>|<span data-ttu-id="3165a-198">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-198">Int32</span></span>|  
|<span data-ttu-id="3165a-199">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-199">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="3165a-200">Byte[]</span><span class="sxs-lookup"><span data-stu-id="3165a-200">Byte[]</span></span>|  
|<span data-ttu-id="3165a-201">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="3165a-201">IS_COMPUTED</span></span>|<span data-ttu-id="3165a-202">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-202">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="3165a-203">过程</span><span class="sxs-lookup"><span data-stu-id="3165a-203">Procedures</span></span>  
  
|<span data-ttu-id="3165a-204">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-204">ColumnName</span></span>|<span data-ttu-id="3165a-205">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-205">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-206">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-206">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="3165a-207">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-207">String</span></span>|  
|<span data-ttu-id="3165a-208">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-208">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="3165a-209">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-209">String</span></span>|  
|<span data-ttu-id="3165a-210">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-210">PROCEDURE_NAME</span></span>|<span data-ttu-id="3165a-211">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-211">String</span></span>|  
|<span data-ttu-id="3165a-212">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-212">PROCEDURE_TYPE</span></span>|<span data-ttu-id="3165a-213">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-213">Int16</span></span>|  
|<span data-ttu-id="3165a-214">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="3165a-214">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="3165a-215">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-215">String</span></span>|  
|<span data-ttu-id="3165a-216">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-216">DESCRIPTION</span></span>|<span data-ttu-id="3165a-217">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-217">String</span></span>|  
|<span data-ttu-id="3165a-218">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-218">DATE_CREATED</span></span>|<span data-ttu-id="3165a-219">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-219">DateTime</span></span>|  
|<span data-ttu-id="3165a-220">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-220">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-221">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-221">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="3165a-222">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3165a-222">ProcedureParameters</span></span>  
  
|<span data-ttu-id="3165a-223">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-223">ColumnName</span></span>|<span data-ttu-id="3165a-224">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-224">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-225">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-225">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="3165a-226">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-226">String</span></span>|  
|<span data-ttu-id="3165a-227">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-227">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="3165a-228">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-228">String</span></span>|  
|<span data-ttu-id="3165a-229">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-229">PROCEDURE_NAME</span></span>|<span data-ttu-id="3165a-230">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-230">String</span></span>|  
|<span data-ttu-id="3165a-231">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-231">PARAMETER_NAME</span></span>|<span data-ttu-id="3165a-232">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-232">String</span></span>|  
|<span data-ttu-id="3165a-233">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-233">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-234">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-234">Int32</span></span>|  
|<span data-ttu-id="3165a-235">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-235">PARAMETER_TYPE</span></span>|<span data-ttu-id="3165a-236">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-236">Int32</span></span>|  
|<span data-ttu-id="3165a-237">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-237">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="3165a-238">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-238">Boolean</span></span>|  
|<span data-ttu-id="3165a-239">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-239">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="3165a-240">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-240">String</span></span>|  
|<span data-ttu-id="3165a-241">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-241">IS_NULLABLE</span></span>|<span data-ttu-id="3165a-242">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-242">Boolean</span></span>|  
|<span data-ttu-id="3165a-243">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-243">DATA_TYPE</span></span>|<span data-ttu-id="3165a-244">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-244">Int32</span></span>|  
|<span data-ttu-id="3165a-245">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-245">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="3165a-246">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-246">Int64</span></span>|  
|<span data-ttu-id="3165a-247">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-247">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="3165a-248">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-248">Int64</span></span>|  
|<span data-ttu-id="3165a-249">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-249">NUMERIC_PRECISION</span></span>|<span data-ttu-id="3165a-250">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-250">Int32</span></span>|  
|<span data-ttu-id="3165a-251">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="3165a-251">NUMERIC_SCALE</span></span>|<span data-ttu-id="3165a-252">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-252">Int16</span></span>|  
|<span data-ttu-id="3165a-253">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-253">DESCRIPTION</span></span>|<span data-ttu-id="3165a-254">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-254">String</span></span>|  
|<span data-ttu-id="3165a-255">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-255">TYPE_NAME</span></span>|<span data-ttu-id="3165a-256">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-256">String</span></span>|  
|<span data-ttu-id="3165a-257">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-257">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="3165a-258">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-258">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="3165a-259">目录</span><span class="sxs-lookup"><span data-stu-id="3165a-259">Catalog</span></span>  
  
|<span data-ttu-id="3165a-260">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-260">ColumnName</span></span>|<span data-ttu-id="3165a-261">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-261">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-262">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-262">CATALOG_NAME</span></span>|<span data-ttu-id="3165a-263">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-263">String</span></span>|  
|<span data-ttu-id="3165a-264">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-264">DESCRIPTION</span></span>|<span data-ttu-id="3165a-265">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-265">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="3165a-266">索引</span><span class="sxs-lookup"><span data-stu-id="3165a-266">Indexes</span></span>  
  
|<span data-ttu-id="3165a-267">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-267">ColumnName</span></span>|<span data-ttu-id="3165a-268">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-268">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-269">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-269">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-270">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-270">String</span></span>|  
|<span data-ttu-id="3165a-271">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-271">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-272">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-272">String</span></span>|  
|<span data-ttu-id="3165a-273">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-273">TABLE_NAME</span></span>|<span data-ttu-id="3165a-274">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-274">String</span></span>|  
|<span data-ttu-id="3165a-275">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-275">INDEX_CATALOG</span></span>|<span data-ttu-id="3165a-276">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-276">String</span></span>|  
|<span data-ttu-id="3165a-277">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-277">INDEX_SCHEMA</span></span>|<span data-ttu-id="3165a-278">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-278">String</span></span>|  
|<span data-ttu-id="3165a-279">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-279">INDEX_NAME</span></span>|<span data-ttu-id="3165a-280">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-280">String</span></span>|  
|<span data-ttu-id="3165a-281">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="3165a-281">PRIMARY_KEY</span></span>|<span data-ttu-id="3165a-282">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-282">Boolean</span></span>|  
|<span data-ttu-id="3165a-283">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="3165a-283">UNIQUE</span></span>|<span data-ttu-id="3165a-284">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-284">Boolean</span></span>|  
|<span data-ttu-id="3165a-285">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="3165a-285">CLUSTERED</span></span>|<span data-ttu-id="3165a-286">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-286">Boolean</span></span>|  
|<span data-ttu-id="3165a-287">TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-287">TYPE</span></span>|<span data-ttu-id="3165a-288">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-288">Int32</span></span>|  
|<span data-ttu-id="3165a-289">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="3165a-289">FILL_FACTOR</span></span>|<span data-ttu-id="3165a-290">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-290">Int32</span></span>|  
|<span data-ttu-id="3165a-291">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="3165a-291">INITIAL_SIZE</span></span>|<span data-ttu-id="3165a-292">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-292">Int32</span></span>|  
|<span data-ttu-id="3165a-293">NULLS</span><span class="sxs-lookup"><span data-stu-id="3165a-293">NULLS</span></span>|<span data-ttu-id="3165a-294">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-294">Int32</span></span>|  
|<span data-ttu-id="3165a-295">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3165a-295">SORT_BOOKMARKS</span></span>|<span data-ttu-id="3165a-296">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-296">Boolean</span></span>|  
|<span data-ttu-id="3165a-297">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="3165a-297">AUTO_UPDATE</span></span>|<span data-ttu-id="3165a-298">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-298">Boolean</span></span>|  
|<span data-ttu-id="3165a-299">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-299">NULL_COLLATION</span></span>|<span data-ttu-id="3165a-300">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-300">Int32</span></span>|  
|<span data-ttu-id="3165a-301">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-301">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-302">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-302">Int64</span></span>|  
|<span data-ttu-id="3165a-303">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-303">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-304">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-304">String</span></span>|  
|<span data-ttu-id="3165a-305">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-305">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-306">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-306">Guid</span></span>|  
|<span data-ttu-id="3165a-307">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-307">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-308">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-308">Int64</span></span>|  
|<span data-ttu-id="3165a-309">COLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-309">COLLATION</span></span>|<span data-ttu-id="3165a-310">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-310">Int16</span></span>|  
|<span data-ttu-id="3165a-311">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="3165a-311">CARDINALITY</span></span>|<span data-ttu-id="3165a-312">小数</span><span class="sxs-lookup"><span data-stu-id="3165a-312">Decimal</span></span>|  
|<span data-ttu-id="3165a-313">PAGES</span><span class="sxs-lookup"><span data-stu-id="3165a-313">PAGES</span></span>|<span data-ttu-id="3165a-314">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-314">Int32</span></span>|  
|<span data-ttu-id="3165a-315">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="3165a-315">FILTER_CONDITION</span></span>|<span data-ttu-id="3165a-316">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-316">String</span></span>|  
|<span data-ttu-id="3165a-317">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="3165a-317">INTEGRATED</span></span>|<span data-ttu-id="3165a-318">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-318">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="3165a-319">Microsoft Oracle OLE DB 提供程序</span><span class="sxs-lookup"><span data-stu-id="3165a-319">Microsoft Oracle OLE DB Provider</span></span>  

 <span data-ttu-id="3165a-320">除了通用架构集合之外，Microsoft Oracle OLE DB 驱动程序还支持下列特定的架构集合：</span><span class="sxs-lookup"><span data-stu-id="3165a-320">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
- <span data-ttu-id="3165a-321">表</span><span class="sxs-lookup"><span data-stu-id="3165a-321">Tables</span></span>  
  
- <span data-ttu-id="3165a-322">列</span><span class="sxs-lookup"><span data-stu-id="3165a-322">Columns</span></span>  
  
- <span data-ttu-id="3165a-323">过程</span><span class="sxs-lookup"><span data-stu-id="3165a-323">Procedures</span></span>  
  
- <span data-ttu-id="3165a-324">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3165a-324">ProcedureColumns</span></span>  
  
- <span data-ttu-id="3165a-325">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3165a-325">ProcedureParameters</span></span>  
  
- <span data-ttu-id="3165a-326">视图</span><span class="sxs-lookup"><span data-stu-id="3165a-326">Views</span></span>  
  
- <span data-ttu-id="3165a-327">索引</span><span class="sxs-lookup"><span data-stu-id="3165a-327">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="3165a-328">表</span><span class="sxs-lookup"><span data-stu-id="3165a-328">Tables</span></span>  
  
|<span data-ttu-id="3165a-329">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-329">ColumnName</span></span>|<span data-ttu-id="3165a-330">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-330">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-331">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-331">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-332">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-332">String</span></span>|  
|<span data-ttu-id="3165a-333">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-333">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-334">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-334">String</span></span>|  
|<span data-ttu-id="3165a-335">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-335">TABLE_NAME</span></span>|<span data-ttu-id="3165a-336">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-336">String</span></span>|  
|<span data-ttu-id="3165a-337">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-337">TABLE_TYPE</span></span>|<span data-ttu-id="3165a-338">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-338">String</span></span>|  
|<span data-ttu-id="3165a-339">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-339">TABLE_GUID</span></span>|<span data-ttu-id="3165a-340">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-340">Guid</span></span>|  
|<span data-ttu-id="3165a-341">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-341">DESCRIPTION</span></span>|<span data-ttu-id="3165a-342">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-342">String</span></span>|  
|<span data-ttu-id="3165a-343">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-343">TABLE_PROPID</span></span>|<span data-ttu-id="3165a-344">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-344">Int64</span></span>|  
|<span data-ttu-id="3165a-345">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-345">DATE_CREATED</span></span>|<span data-ttu-id="3165a-346">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-346">DateTime</span></span>|  
|<span data-ttu-id="3165a-347">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-347">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-348">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-348">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="3165a-349">列</span><span class="sxs-lookup"><span data-stu-id="3165a-349">Columns</span></span>  
  
|<span data-ttu-id="3165a-350">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-350">ColumnName</span></span>|<span data-ttu-id="3165a-351">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-351">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-352">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-352">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-353">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-353">String</span></span>|  
|<span data-ttu-id="3165a-354">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-354">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-355">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-355">String</span></span>|  
|<span data-ttu-id="3165a-356">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-356">TABLE_NAME</span></span>|<span data-ttu-id="3165a-357">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-357">String</span></span>|  
|<span data-ttu-id="3165a-358">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-358">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-359">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-359">String</span></span>|  
|<span data-ttu-id="3165a-360">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-360">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-361">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-361">Guid</span></span>|  
|<span data-ttu-id="3165a-362">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-362">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-363">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-363">Int64</span></span>|  
|<span data-ttu-id="3165a-364">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-364">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-365">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-365">Int64</span></span>|  
|<span data-ttu-id="3165a-366">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-366">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="3165a-367">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-367">Boolean</span></span>|  
|<span data-ttu-id="3165a-368">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-368">COLUMN_DEFAULT</span></span>|<span data-ttu-id="3165a-369">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-369">String</span></span>|  
|<span data-ttu-id="3165a-370">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3165a-370">COLUMN_FLAGS</span></span>|<span data-ttu-id="3165a-371">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-371">Int64</span></span>|  
|<span data-ttu-id="3165a-372">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-372">IS_NULLABLE</span></span>|<span data-ttu-id="3165a-373">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-373">Boolean</span></span>|  
|<span data-ttu-id="3165a-374">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-374">DATA_TYPE</span></span>|<span data-ttu-id="3165a-375">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-375">Int32</span></span>|  
|<span data-ttu-id="3165a-376">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-376">TYPE_GUID</span></span>|<span data-ttu-id="3165a-377">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-377">Guid</span></span>|  
|<span data-ttu-id="3165a-378">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-378">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="3165a-379">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-379">Int64</span></span>|  
|<span data-ttu-id="3165a-380">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-380">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="3165a-381">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-381">Int64</span></span>|  
|<span data-ttu-id="3165a-382">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-382">NUMERIC_PRECISION</span></span>|<span data-ttu-id="3165a-383">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-383">Int32</span></span>|  
|<span data-ttu-id="3165a-384">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="3165a-384">NUMERIC_SCALE</span></span>|<span data-ttu-id="3165a-385">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-385">Int16</span></span>|  
|<span data-ttu-id="3165a-386">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-386">DATETIME_PRECISION</span></span>|<span data-ttu-id="3165a-387">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-387">Int64</span></span>|  
|<span data-ttu-id="3165a-388">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-388">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="3165a-389">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-389">String</span></span>|  
|<span data-ttu-id="3165a-390">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-390">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="3165a-391">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-391">String</span></span>|  
|<span data-ttu-id="3165a-392">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-392">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="3165a-393">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-393">String</span></span>|  
|<span data-ttu-id="3165a-394">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-394">COLLATION_CATALOG</span></span>|<span data-ttu-id="3165a-395">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-395">String</span></span>|  
|<span data-ttu-id="3165a-396">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-396">COLLATION_SCHEMA</span></span>|<span data-ttu-id="3165a-397">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-397">String</span></span>|  
|<span data-ttu-id="3165a-398">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-398">COLLATION_NAME</span></span>|<span data-ttu-id="3165a-399">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-399">String</span></span>|  
|<span data-ttu-id="3165a-400">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-400">DOMAIN_CATALOG</span></span>|<span data-ttu-id="3165a-401">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-401">String</span></span>|  
|<span data-ttu-id="3165a-402">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-402">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="3165a-403">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-403">String</span></span>|  
|<span data-ttu-id="3165a-404">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-404">DOMAIN_NAME</span></span>|<span data-ttu-id="3165a-405">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-405">String</span></span>|  
|<span data-ttu-id="3165a-406">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-406">DESCRIPTION</span></span>|<span data-ttu-id="3165a-407">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-407">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="3165a-408">过程</span><span class="sxs-lookup"><span data-stu-id="3165a-408">Procedures</span></span>  
  
|<span data-ttu-id="3165a-409">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-409">ColumnName</span></span>|<span data-ttu-id="3165a-410">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-410">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-411">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-411">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="3165a-412">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-412">String</span></span>|  
|<span data-ttu-id="3165a-413">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-413">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="3165a-414">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-414">String</span></span>|  
|<span data-ttu-id="3165a-415">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-415">PROCEDURE_NAME</span></span>|<span data-ttu-id="3165a-416">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-416">String</span></span>|  
|<span data-ttu-id="3165a-417">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-417">PROCEDURE_TYPE</span></span>|<span data-ttu-id="3165a-418">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-418">Int16</span></span>|  
|<span data-ttu-id="3165a-419">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="3165a-419">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="3165a-420">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-420">String</span></span>|  
|<span data-ttu-id="3165a-421">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-421">DESCRIPTION</span></span>|<span data-ttu-id="3165a-422">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-422">String</span></span>|  
|<span data-ttu-id="3165a-423">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-423">DATE_CREATED</span></span>|<span data-ttu-id="3165a-424">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-424">DateTime</span></span>|  
|<span data-ttu-id="3165a-425">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-425">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-426">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-426">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="3165a-427">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3165a-427">ProcedureColumns</span></span>  
  
|<span data-ttu-id="3165a-428">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-428">ColumnName</span></span>|<span data-ttu-id="3165a-429">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-429">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-430">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-430">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="3165a-431">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-431">String</span></span>|  
|<span data-ttu-id="3165a-432">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-432">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="3165a-433">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-433">String</span></span>|  
|<span data-ttu-id="3165a-434">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-434">PROCEDURE_NAME</span></span>|<span data-ttu-id="3165a-435">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-435">String</span></span>|  
|<span data-ttu-id="3165a-436">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-436">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-437">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-437">String</span></span>|  
|<span data-ttu-id="3165a-438">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-438">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-439">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-439">Guid</span></span>|  
|<span data-ttu-id="3165a-440">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-440">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-441">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-441">Int64</span></span>|  
|<span data-ttu-id="3165a-442">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="3165a-442">ROWSET_NUMBER</span></span>|<span data-ttu-id="3165a-443">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-443">Int64</span></span>|  
|<span data-ttu-id="3165a-444">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-444">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-445">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-445">Int64</span></span>|  
|<span data-ttu-id="3165a-446">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-446">IS_NULLABLE</span></span>|<span data-ttu-id="3165a-447">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-447">Boolean</span></span>|  
|<span data-ttu-id="3165a-448">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-448">DATA_TYPE</span></span>|<span data-ttu-id="3165a-449">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-449">Int32</span></span>|  
|<span data-ttu-id="3165a-450">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-450">TYPE_GUID</span></span>|<span data-ttu-id="3165a-451">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-451">Guid</span></span>|  
|<span data-ttu-id="3165a-452">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-452">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="3165a-453">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-453">Int64</span></span>|  
|<span data-ttu-id="3165a-454">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-454">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="3165a-455">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-455">Int64</span></span>|  
|<span data-ttu-id="3165a-456">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-456">NUMERIC_PRECISION</span></span>|<span data-ttu-id="3165a-457">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-457">Int32</span></span>|  
|<span data-ttu-id="3165a-458">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="3165a-458">NUMERIC_SCALE</span></span>|<span data-ttu-id="3165a-459">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-459">Int16</span></span>|  
|<span data-ttu-id="3165a-460">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-460">DESCRIPTION</span></span>|<span data-ttu-id="3165a-461">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-461">String</span></span>|  
|<span data-ttu-id="3165a-462">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="3165a-462">OVERLOAD</span></span>|<span data-ttu-id="3165a-463">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-463">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="3165a-464">视图</span><span class="sxs-lookup"><span data-stu-id="3165a-464">Views</span></span>  
  
|<span data-ttu-id="3165a-465">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-465">ColumnName</span></span>|<span data-ttu-id="3165a-466">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-466">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-467">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-467">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-468">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-468">String</span></span>|  
|<span data-ttu-id="3165a-469">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-469">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-470">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-470">String</span></span>|  
|<span data-ttu-id="3165a-471">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-471">TABLE_NAME</span></span>|<span data-ttu-id="3165a-472">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-472">String</span></span>|  
|<span data-ttu-id="3165a-473">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="3165a-473">VIEW_DEFINITION</span></span>|<span data-ttu-id="3165a-474">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-474">String</span></span>|  
|<span data-ttu-id="3165a-475">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-475">CHECK_OPTION</span></span>|<span data-ttu-id="3165a-476">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-476">Boolean</span></span>|  
|<span data-ttu-id="3165a-477">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-477">IS_UPDATABLE</span></span>|<span data-ttu-id="3165a-478">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-478">Boolean</span></span>|  
|<span data-ttu-id="3165a-479">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-479">DESCRIPTION</span></span>|<span data-ttu-id="3165a-480">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-480">String</span></span>|  
|<span data-ttu-id="3165a-481">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-481">DATE_CREATED</span></span>|<span data-ttu-id="3165a-482">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-482">DateTime</span></span>|  
|<span data-ttu-id="3165a-483">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-483">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-484">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-484">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="3165a-485">索引</span><span class="sxs-lookup"><span data-stu-id="3165a-485">Indexes</span></span>  
  
|<span data-ttu-id="3165a-486">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-486">ColumnName</span></span>|<span data-ttu-id="3165a-487">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-487">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-488">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-488">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-489">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-489">String</span></span>|  
|<span data-ttu-id="3165a-490">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-490">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-491">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-491">String</span></span>|  
|<span data-ttu-id="3165a-492">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-492">TABLE_NAME</span></span>|<span data-ttu-id="3165a-493">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-493">String</span></span>|  
|<span data-ttu-id="3165a-494">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-494">INDEX_CATALOG</span></span>|<span data-ttu-id="3165a-495">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-495">String</span></span>|  
|<span data-ttu-id="3165a-496">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-496">INDEX_SCHEMA</span></span>|<span data-ttu-id="3165a-497">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-497">String</span></span>|  
|<span data-ttu-id="3165a-498">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-498">INDEX_NAME</span></span>|<span data-ttu-id="3165a-499">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-499">String</span></span>|  
|<span data-ttu-id="3165a-500">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="3165a-500">PRIMARY_KEY</span></span>|<span data-ttu-id="3165a-501">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-501">Boolean</span></span>|  
|<span data-ttu-id="3165a-502">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="3165a-502">UNIQUE</span></span>|<span data-ttu-id="3165a-503">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-503">Boolean</span></span>|  
|<span data-ttu-id="3165a-504">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="3165a-504">CLUSTERED</span></span>|<span data-ttu-id="3165a-505">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-505">Boolean</span></span>|  
|<span data-ttu-id="3165a-506">TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-506">TYPE</span></span>|<span data-ttu-id="3165a-507">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-507">Int32</span></span>|  
|<span data-ttu-id="3165a-508">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="3165a-508">FILL_FACTOR</span></span>|<span data-ttu-id="3165a-509">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-509">Int32</span></span>|  
|<span data-ttu-id="3165a-510">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="3165a-510">INITIAL_SIZE</span></span>|<span data-ttu-id="3165a-511">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-511">Int32</span></span>|  
|<span data-ttu-id="3165a-512">NULLS</span><span class="sxs-lookup"><span data-stu-id="3165a-512">NULLS</span></span>|<span data-ttu-id="3165a-513">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-513">Int32</span></span>|  
|<span data-ttu-id="3165a-514">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3165a-514">SORT_BOOKMARKS</span></span>|<span data-ttu-id="3165a-515">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-515">Boolean</span></span>|  
|<span data-ttu-id="3165a-516">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="3165a-516">AUTO_UPDATE</span></span>|<span data-ttu-id="3165a-517">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-517">Boolean</span></span>|  
|<span data-ttu-id="3165a-518">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-518">NULL_COLLATION</span></span>|<span data-ttu-id="3165a-519">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-519">Int32</span></span>|  
|<span data-ttu-id="3165a-520">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-520">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-521">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-521">Int64</span></span>|  
|<span data-ttu-id="3165a-522">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-522">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-523">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-523">String</span></span>|  
|<span data-ttu-id="3165a-524">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-524">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-525">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-525">Guid</span></span>|  
|<span data-ttu-id="3165a-526">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-526">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-527">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-527">Int64</span></span>|  
|<span data-ttu-id="3165a-528">COLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-528">COLLATION</span></span>|<span data-ttu-id="3165a-529">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-529">Int16</span></span>|  
|<span data-ttu-id="3165a-530">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="3165a-530">CARDINALITY</span></span>|<span data-ttu-id="3165a-531">小数</span><span class="sxs-lookup"><span data-stu-id="3165a-531">Decimal</span></span>|  
|<span data-ttu-id="3165a-532">PAGES</span><span class="sxs-lookup"><span data-stu-id="3165a-532">PAGES</span></span>|<span data-ttu-id="3165a-533">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-533">Int32</span></span>|  
|<span data-ttu-id="3165a-534">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="3165a-534">FILTER_CONDITION</span></span>|<span data-ttu-id="3165a-535">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-535">String</span></span>|  
|<span data-ttu-id="3165a-536">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="3165a-536">INTEGRATED</span></span>|<span data-ttu-id="3165a-537">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-537">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="3165a-538">Microsoft Jet OLE DB     </span><span class="sxs-lookup"><span data-stu-id="3165a-538">Microsoft Jet OLE DB Provider</span></span>  

 <span data-ttu-id="3165a-539">除了通用架构集合之外，Microsoft Jet OLE DB 驱动程序还支持下列特定的架构集合：</span><span class="sxs-lookup"><span data-stu-id="3165a-539">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
- <span data-ttu-id="3165a-540">表</span><span class="sxs-lookup"><span data-stu-id="3165a-540">Tables</span></span>  
  
- <span data-ttu-id="3165a-541">列</span><span class="sxs-lookup"><span data-stu-id="3165a-541">Columns</span></span>  
  
- <span data-ttu-id="3165a-542">过程</span><span class="sxs-lookup"><span data-stu-id="3165a-542">Procedures</span></span>  
  
- <span data-ttu-id="3165a-543">视图</span><span class="sxs-lookup"><span data-stu-id="3165a-543">Views</span></span>  
  
- <span data-ttu-id="3165a-544">索引</span><span class="sxs-lookup"><span data-stu-id="3165a-544">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="3165a-545">表</span><span class="sxs-lookup"><span data-stu-id="3165a-545">Tables</span></span>  
  
|<span data-ttu-id="3165a-546">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-546">ColumnName</span></span>|<span data-ttu-id="3165a-547">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-547">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-548">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-548">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-549">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-549">String</span></span>|  
|<span data-ttu-id="3165a-550">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-550">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-551">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-551">String</span></span>|  
|<span data-ttu-id="3165a-552">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-552">TABLE_NAME</span></span>|<span data-ttu-id="3165a-553">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-553">String</span></span>|  
|<span data-ttu-id="3165a-554">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-554">TABLE_TYPE</span></span>|<span data-ttu-id="3165a-555">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-555">String</span></span>|  
|<span data-ttu-id="3165a-556">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-556">TABLE_GUID</span></span>|<span data-ttu-id="3165a-557">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-557">Guid</span></span>|  
|<span data-ttu-id="3165a-558">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-558">DESCRIPTION</span></span>|<span data-ttu-id="3165a-559">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-559">String</span></span>|  
|<span data-ttu-id="3165a-560">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-560">TABLE_PROPID</span></span>|<span data-ttu-id="3165a-561">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-561">Int64</span></span>|  
|<span data-ttu-id="3165a-562">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-562">DATE_CREATED</span></span>|<span data-ttu-id="3165a-563">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-563">DateTime</span></span>|  
|<span data-ttu-id="3165a-564">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-564">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-565">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-565">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="3165a-566">列</span><span class="sxs-lookup"><span data-stu-id="3165a-566">Columns</span></span>  
  
|<span data-ttu-id="3165a-567">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-567">ColumnName</span></span>|<span data-ttu-id="3165a-568">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-568">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-569">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-569">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-570">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-570">String</span></span>|  
|<span data-ttu-id="3165a-571">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-571">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-572">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-572">String</span></span>|  
|<span data-ttu-id="3165a-573">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-573">TABLE_NAME</span></span>|<span data-ttu-id="3165a-574">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-574">String</span></span>|  
|<span data-ttu-id="3165a-575">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-575">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-576">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-576">String</span></span>|  
|<span data-ttu-id="3165a-577">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-577">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-578">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-578">Guid</span></span>|  
|<span data-ttu-id="3165a-579">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-579">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-580">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-580">Int64</span></span>|  
|<span data-ttu-id="3165a-581">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-581">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-582">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-582">Int64</span></span>|  
|<span data-ttu-id="3165a-583">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-583">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="3165a-584">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-584">Boolean</span></span>|  
|<span data-ttu-id="3165a-585">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3165a-585">COLUMN_DEFAULT</span></span>|<span data-ttu-id="3165a-586">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-586">String</span></span>|  
|<span data-ttu-id="3165a-587">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3165a-587">COLUMN_FLAGS</span></span>|<span data-ttu-id="3165a-588">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-588">Int64</span></span>|  
|<span data-ttu-id="3165a-589">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-589">IS_NULLABLE</span></span>|<span data-ttu-id="3165a-590">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-590">Boolean</span></span>|  
|<span data-ttu-id="3165a-591">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-591">DATA_TYPE</span></span>|<span data-ttu-id="3165a-592">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-592">Int32</span></span>|  
|<span data-ttu-id="3165a-593">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-593">TYPE_GUID</span></span>|<span data-ttu-id="3165a-594">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-594">Guid</span></span>|  
|<span data-ttu-id="3165a-595">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-595">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="3165a-596">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-596">Int64</span></span>|  
|<span data-ttu-id="3165a-597">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3165a-597">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="3165a-598">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-598">Int64</span></span>|  
|<span data-ttu-id="3165a-599">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-599">NUMERIC_PRECISION</span></span>|<span data-ttu-id="3165a-600">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-600">Int32</span></span>|  
|<span data-ttu-id="3165a-601">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="3165a-601">NUMERIC_SCALE</span></span>|<span data-ttu-id="3165a-602">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-602">Int16</span></span>|  
|<span data-ttu-id="3165a-603">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="3165a-603">DATETIME_PRECISION</span></span>|<span data-ttu-id="3165a-604">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-604">Int64</span></span>|  
|<span data-ttu-id="3165a-605">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-605">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="3165a-606">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-606">String</span></span>|  
|<span data-ttu-id="3165a-607">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-607">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="3165a-608">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-608">String</span></span>|  
|<span data-ttu-id="3165a-609">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-609">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="3165a-610">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-610">String</span></span>|  
|<span data-ttu-id="3165a-611">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-611">COLLATION_CATALOG</span></span>|<span data-ttu-id="3165a-612">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-612">String</span></span>|  
|<span data-ttu-id="3165a-613">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-613">COLLATION_SCHEMA</span></span>|<span data-ttu-id="3165a-614">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-614">String</span></span>|  
|<span data-ttu-id="3165a-615">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-615">COLLATION_NAME</span></span>|<span data-ttu-id="3165a-616">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-616">String</span></span>|  
|<span data-ttu-id="3165a-617">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-617">DOMAIN_CATALOG</span></span>|<span data-ttu-id="3165a-618">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-618">String</span></span>|  
|<span data-ttu-id="3165a-619">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-619">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="3165a-620">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-620">String</span></span>|  
|<span data-ttu-id="3165a-621">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-621">DOMAIN_NAME</span></span>|<span data-ttu-id="3165a-622">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-622">String</span></span>|  
|<span data-ttu-id="3165a-623">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-623">DESCRIPTION</span></span>|<span data-ttu-id="3165a-624">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-624">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="3165a-625">过程</span><span class="sxs-lookup"><span data-stu-id="3165a-625">Procedures</span></span>  
  
|<span data-ttu-id="3165a-626">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-626">ColumnName</span></span>|<span data-ttu-id="3165a-627">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-627">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-628">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-628">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="3165a-629">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-629">String</span></span>|  
|<span data-ttu-id="3165a-630">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-630">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="3165a-631">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-631">String</span></span>|  
|<span data-ttu-id="3165a-632">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-632">PROCEDURE_NAME</span></span>|<span data-ttu-id="3165a-633">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-633">String</span></span>|  
|<span data-ttu-id="3165a-634">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-634">PROCEDURE_TYPE</span></span>|<span data-ttu-id="3165a-635">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-635">Int16</span></span>|  
|<span data-ttu-id="3165a-636">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="3165a-636">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="3165a-637">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-637">String</span></span>|  
|<span data-ttu-id="3165a-638">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-638">DESCRIPTION</span></span>|<span data-ttu-id="3165a-639">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-639">String</span></span>|  
|<span data-ttu-id="3165a-640">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-640">DATE_CREATED</span></span>|<span data-ttu-id="3165a-641">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-641">DateTime</span></span>|  
|<span data-ttu-id="3165a-642">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-642">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-643">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-643">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="3165a-644">视图</span><span class="sxs-lookup"><span data-stu-id="3165a-644">Views</span></span>  
  
|<span data-ttu-id="3165a-645">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-645">ColumnName</span></span>|<span data-ttu-id="3165a-646">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-646">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-647">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-647">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-648">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-648">String</span></span>|  
|<span data-ttu-id="3165a-649">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-649">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-650">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-650">String</span></span>|  
|<span data-ttu-id="3165a-651">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-651">TABLE_NAME</span></span>|<span data-ttu-id="3165a-652">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-652">String</span></span>|  
|<span data-ttu-id="3165a-653">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="3165a-653">VIEW_DEFINITION</span></span>|<span data-ttu-id="3165a-654">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-654">String</span></span>|  
|<span data-ttu-id="3165a-655">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-655">CHECK_OPTION</span></span>|<span data-ttu-id="3165a-656">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-656">Boolean</span></span>|  
|<span data-ttu-id="3165a-657">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="3165a-657">IS_UPDATABLE</span></span>|<span data-ttu-id="3165a-658">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-658">Boolean</span></span>|  
|<span data-ttu-id="3165a-659">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3165a-659">DESCRIPTION</span></span>|<span data-ttu-id="3165a-660">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-660">String</span></span>|  
|<span data-ttu-id="3165a-661">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="3165a-661">DATE_CREATED</span></span>|<span data-ttu-id="3165a-662">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-662">DateTime</span></span>|  
|<span data-ttu-id="3165a-663">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3165a-663">DATE_MODIFIED</span></span>|<span data-ttu-id="3165a-664">DateTime</span><span class="sxs-lookup"><span data-stu-id="3165a-664">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="3165a-665">索引</span><span class="sxs-lookup"><span data-stu-id="3165a-665">Indexes</span></span>  
  
|<span data-ttu-id="3165a-666">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3165a-666">ColumnName</span></span>|<span data-ttu-id="3165a-667">数据类型</span><span class="sxs-lookup"><span data-stu-id="3165a-667">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3165a-668">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-668">TABLE_CATALOG</span></span>|<span data-ttu-id="3165a-669">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-669">String</span></span>|  
|<span data-ttu-id="3165a-670">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-670">TABLE_SCHEMA</span></span>|<span data-ttu-id="3165a-671">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-671">String</span></span>|  
|<span data-ttu-id="3165a-672">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-672">TABLE_NAME</span></span>|<span data-ttu-id="3165a-673">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-673">String</span></span>|  
|<span data-ttu-id="3165a-674">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3165a-674">INDEX_CATALOG</span></span>|<span data-ttu-id="3165a-675">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-675">String</span></span>|  
|<span data-ttu-id="3165a-676">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3165a-676">INDEX_SCHEMA</span></span>|<span data-ttu-id="3165a-677">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-677">String</span></span>|  
|<span data-ttu-id="3165a-678">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-678">INDEX_NAME</span></span>|<span data-ttu-id="3165a-679">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-679">String</span></span>|  
|<span data-ttu-id="3165a-680">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="3165a-680">PRIMARY_KEY</span></span>|<span data-ttu-id="3165a-681">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-681">Boolean</span></span>|  
|<span data-ttu-id="3165a-682">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="3165a-682">UNIQUE</span></span>|<span data-ttu-id="3165a-683">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-683">Boolean</span></span>|  
|<span data-ttu-id="3165a-684">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="3165a-684">CLUSTERED</span></span>|<span data-ttu-id="3165a-685">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-685">Boolean</span></span>|  
|<span data-ttu-id="3165a-686">TYPE</span><span class="sxs-lookup"><span data-stu-id="3165a-686">TYPE</span></span>|<span data-ttu-id="3165a-687">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-687">Int32</span></span>|  
|<span data-ttu-id="3165a-688">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="3165a-688">FILL_FACTOR</span></span>|<span data-ttu-id="3165a-689">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-689">Int32</span></span>|  
|<span data-ttu-id="3165a-690">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="3165a-690">INITIAL_SIZE</span></span>|<span data-ttu-id="3165a-691">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-691">Int32</span></span>|  
|<span data-ttu-id="3165a-692">NULLS</span><span class="sxs-lookup"><span data-stu-id="3165a-692">NULLS</span></span>|<span data-ttu-id="3165a-693">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-693">Int32</span></span>|  
|<span data-ttu-id="3165a-694">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3165a-694">SORT_BOOKMARKS</span></span>|<span data-ttu-id="3165a-695">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-695">Boolean</span></span>|  
|<span data-ttu-id="3165a-696">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="3165a-696">AUTO_UPDATE</span></span>|<span data-ttu-id="3165a-697">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-697">Boolean</span></span>|  
|<span data-ttu-id="3165a-698">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-698">NULL_COLLATION</span></span>|<span data-ttu-id="3165a-699">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-699">Int32</span></span>|  
|<span data-ttu-id="3165a-700">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3165a-700">ORDINAL_POSITION</span></span>|<span data-ttu-id="3165a-701">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-701">Int64</span></span>|  
|<span data-ttu-id="3165a-702">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3165a-702">COLUMN_NAME</span></span>|<span data-ttu-id="3165a-703">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-703">String</span></span>|  
|<span data-ttu-id="3165a-704">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="3165a-704">COLUMN_GUID</span></span>|<span data-ttu-id="3165a-705">Guid</span><span class="sxs-lookup"><span data-stu-id="3165a-705">Guid</span></span>|  
|<span data-ttu-id="3165a-706">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="3165a-706">COLUMN_PROPID</span></span>|<span data-ttu-id="3165a-707">Int64</span><span class="sxs-lookup"><span data-stu-id="3165a-707">Int64</span></span>|  
|<span data-ttu-id="3165a-708">COLLATION</span><span class="sxs-lookup"><span data-stu-id="3165a-708">COLLATION</span></span>|<span data-ttu-id="3165a-709">Int16</span><span class="sxs-lookup"><span data-stu-id="3165a-709">Int16</span></span>|  
|<span data-ttu-id="3165a-710">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="3165a-710">CARDINALITY</span></span>|<span data-ttu-id="3165a-711">小数</span><span class="sxs-lookup"><span data-stu-id="3165a-711">Decimal</span></span>|  
|<span data-ttu-id="3165a-712">PAGES</span><span class="sxs-lookup"><span data-stu-id="3165a-712">PAGES</span></span>|<span data-ttu-id="3165a-713">Int32</span><span class="sxs-lookup"><span data-stu-id="3165a-713">Int32</span></span>|  
|<span data-ttu-id="3165a-714">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="3165a-714">FILTER_CONDITION</span></span>|<span data-ttu-id="3165a-715">字符串</span><span class="sxs-lookup"><span data-stu-id="3165a-715">String</span></span>|  
|<span data-ttu-id="3165a-716">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="3165a-716">INTEGRATED</span></span>|<span data-ttu-id="3165a-717">布尔</span><span class="sxs-lookup"><span data-stu-id="3165a-717">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3165a-718">请参阅</span><span class="sxs-lookup"><span data-stu-id="3165a-718">See also</span></span>

- [<span data-ttu-id="3165a-719">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="3165a-719">ADO.NET Overview</span></span>](ado-net-overview.md)

---
description: 了解详细信息：实体 SQL 快速参考
title: Entity SQL 快速参考
ms.date: 03/30/2017
ms.assetid: e53dad9e-5e83-426e-abb4-be3e78e3d6dc
ms.openlocfilehash: ddac48bece1f0e9df737db295d4d028529ea290f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724552"
---
# <a name="entity-sql-quick-reference"></a><span data-ttu-id="7855d-103">Entity SQL 快速参考</span><span class="sxs-lookup"><span data-stu-id="7855d-103">Entity SQL Quick Reference</span></span>

<span data-ttu-id="7855d-104">本主题提供 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询的快速参考。</span><span class="sxs-lookup"><span data-stu-id="7855d-104">This topic provides a quick reference to [!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries.</span></span> <span data-ttu-id="7855d-105">本主题中的查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="7855d-105">The queries in this topic are based on the AdventureWorks Sales model.</span></span>  
  
## <a name="literals"></a><span data-ttu-id="7855d-106">文本</span><span class="sxs-lookup"><span data-stu-id="7855d-106">Literals</span></span>  
  
### <a name="string"></a><span data-ttu-id="7855d-107">字符串</span><span class="sxs-lookup"><span data-stu-id="7855d-107">String</span></span>  

 <span data-ttu-id="7855d-108">字符串分为 Unicode 字符串和非 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="7855d-108">There are Unicode and non-Unicode character string literals.</span></span> <span data-ttu-id="7855d-109">Unicode 字符串前面附有 N。例如， `N'hello'` 。</span><span class="sxs-lookup"><span data-stu-id="7855d-109">Unicode strings are prepended with N. For example, `N'hello'`.</span></span>  
  
 <span data-ttu-id="7855d-110">下面是非 Unicode 字符串的示例：</span><span class="sxs-lookup"><span data-stu-id="7855d-110">The following is an example of a Non-Unicode string literal:</span></span>  
  
```sql  
'hello'  
--same as  
"hello"  
```  
  
 <span data-ttu-id="7855d-111">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-111">Output:</span></span>  
  
|<span data-ttu-id="7855d-112">值</span><span class="sxs-lookup"><span data-stu-id="7855d-112">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-113">hello</span><span class="sxs-lookup"><span data-stu-id="7855d-113">hello</span></span>|  
  
### <a name="datetime"></a><span data-ttu-id="7855d-114">DateTime</span><span class="sxs-lookup"><span data-stu-id="7855d-114">DateTime</span></span>  

 <span data-ttu-id="7855d-115">在日期时间文本中，日期部分和时间部分是必须存在的。</span><span class="sxs-lookup"><span data-stu-id="7855d-115">In DateTime literals, both date and time parts are mandatory.</span></span> <span data-ttu-id="7855d-116">这里没有默认值。</span><span class="sxs-lookup"><span data-stu-id="7855d-116">There are no default values.</span></span>  
  
 <span data-ttu-id="7855d-117">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-117">Example:</span></span>  
  
```sql  
DATETIME '2006-12-25 01:01:00.000'
--same as  
DATETIME '2006-12-25 01:01'  
```  
  
 <span data-ttu-id="7855d-118">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-118">Output:</span></span>  
  
|<span data-ttu-id="7855d-119">值</span><span class="sxs-lookup"><span data-stu-id="7855d-119">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-120">12/25/2006 1:01:00 AM</span><span class="sxs-lookup"><span data-stu-id="7855d-120">12/25/2006 1:01:00 AM</span></span>|  
  
### <a name="integer"></a><span data-ttu-id="7855d-121">Integer</span><span class="sxs-lookup"><span data-stu-id="7855d-121">Integer</span></span>  

 <span data-ttu-id="7855d-122">整数文本可以为 Int32 (123)、UInt32 (123U)、Int64 (123L) 和 UInt64 (123UL) 类型。</span><span class="sxs-lookup"><span data-stu-id="7855d-122">Integer literals can be of type Int32 (123), UInt32 (123U), Int64 (123L), and UInt64 (123UL).</span></span>  
  
 <span data-ttu-id="7855d-123">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-123">Example:</span></span>  
  
```sql  
--a collection of integers  
{1, 2, 3}  
```  
  
 <span data-ttu-id="7855d-124">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-124">Output:</span></span>  
  
|<span data-ttu-id="7855d-125">值</span><span class="sxs-lookup"><span data-stu-id="7855d-125">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-126">1</span><span class="sxs-lookup"><span data-stu-id="7855d-126">1</span></span>|  
|<span data-ttu-id="7855d-127">2</span><span class="sxs-lookup"><span data-stu-id="7855d-127">2</span></span>|  
|<span data-ttu-id="7855d-128">3</span><span class="sxs-lookup"><span data-stu-id="7855d-128">3</span></span>|  
  
### <a name="other"></a><span data-ttu-id="7855d-129">其他</span><span class="sxs-lookup"><span data-stu-id="7855d-129">Other</span></span>  

 <span data-ttu-id="7855d-130">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 支持的其他文字为、Guid、二进制、浮点/双精度型、十进制和 `null`。</span><span class="sxs-lookup"><span data-stu-id="7855d-130">Other literals supported by [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are Guid, Binary, Float/Double, Decimal, and `null`.</span></span> <span data-ttu-id="7855d-131">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的 null 文本视为与概念模型中的每一种其他类型兼容。</span><span class="sxs-lookup"><span data-stu-id="7855d-131">Null literals in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are considered to be compatible with every other type in the conceptual model.</span></span>  
  
## <a name="type-constructors"></a><span data-ttu-id="7855d-132">类型构造函数</span><span class="sxs-lookup"><span data-stu-id="7855d-132">Type Constructors</span></span>  
  
### <a name="row"></a><span data-ttu-id="7855d-133">ROW</span><span class="sxs-lookup"><span data-stu-id="7855d-133">ROW</span></span>  

 <span data-ttu-id="7855d-134">[ROW](row-entity-sql.md) 构造一个匿名的结构化类型 (记录) 值，如下所示： `ROW(1 AS myNumber, ‘Name’ AS myName).`</span><span class="sxs-lookup"><span data-stu-id="7855d-134">[ROW](row-entity-sql.md) constructs an anonymous, structurally-typed (record) value as in: `ROW(1 AS myNumber, ‘Name’ AS myName).`</span></span>  
  
 <span data-ttu-id="7855d-135">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-135">Example:</span></span>  
  
```sql  
SELECT VALUE row (product.ProductID AS ProductID, product.Name
    AS ProductName) FROM AdventureWorksEntities.Product AS product
```  
  
 <span data-ttu-id="7855d-136">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-136">Output:</span></span>  
  
|<span data-ttu-id="7855d-137">ProductID</span><span class="sxs-lookup"><span data-stu-id="7855d-137">ProductID</span></span>|<span data-ttu-id="7855d-138">名称</span><span class="sxs-lookup"><span data-stu-id="7855d-138">Name</span></span>|  
|---------------|----------|  
|<span data-ttu-id="7855d-139">1</span><span class="sxs-lookup"><span data-stu-id="7855d-139">1</span></span>|<span data-ttu-id="7855d-140">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="7855d-140">Adjustable Race</span></span>|  
|<span data-ttu-id="7855d-141">879</span><span class="sxs-lookup"><span data-stu-id="7855d-141">879</span></span>|<span data-ttu-id="7855d-142">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="7855d-142">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="7855d-143">712</span><span class="sxs-lookup"><span data-stu-id="7855d-143">712</span></span>|<span data-ttu-id="7855d-144">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="7855d-144">AWC Logo Cap</span></span>|  
|<span data-ttu-id="7855d-145">...</span><span class="sxs-lookup"><span data-stu-id="7855d-145">...</span></span>|<span data-ttu-id="7855d-146">...</span><span class="sxs-lookup"><span data-stu-id="7855d-146">...</span></span>|  
  
### <a name="multiset"></a><span data-ttu-id="7855d-147">MULTISET</span><span class="sxs-lookup"><span data-stu-id="7855d-147">MULTISET</span></span>  

 <span data-ttu-id="7855d-148">[多重集](multiset-entity-sql.md) 构造集合，例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-148">[MULTISET](multiset-entity-sql.md) constructs collections, such as:</span></span>  
  
 <span data-ttu-id="7855d-149">`MULTISET(1,2,2,3)` `--same as`-`{1,2,2,3}.`</span><span class="sxs-lookup"><span data-stu-id="7855d-149">`MULTISET(1,2,2,3)` `--same as`-`{1,2,2,3}.`</span></span>  
  
 <span data-ttu-id="7855d-150">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-150">Example:</span></span>  
  
```sql  
SELECT VALUE product FROM AdventureWorksEntities.Product AS product WHERE product.ListPrice IN MultiSet (125, 300)  
```  
  
 <span data-ttu-id="7855d-151">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-151">Output:</span></span>  
  
|<span data-ttu-id="7855d-152">ProductID</span><span class="sxs-lookup"><span data-stu-id="7855d-152">ProductID</span></span>|<span data-ttu-id="7855d-153">名称</span><span class="sxs-lookup"><span data-stu-id="7855d-153">Name</span></span>|<span data-ttu-id="7855d-154">ProductNumber</span><span class="sxs-lookup"><span data-stu-id="7855d-154">ProductNumber</span></span>|<span data-ttu-id="7855d-155">…</span><span class="sxs-lookup"><span data-stu-id="7855d-155">…</span></span>|  
|---------------|----------|-------------------|-------|  
|<span data-ttu-id="7855d-156">842</span><span class="sxs-lookup"><span data-stu-id="7855d-156">842</span></span>|<span data-ttu-id="7855d-157">Touring-Panniers, Large</span><span class="sxs-lookup"><span data-stu-id="7855d-157">Touring-Panniers, Large</span></span>|<span data-ttu-id="7855d-158">PA-T100</span><span class="sxs-lookup"><span data-stu-id="7855d-158">PA-T100</span></span>|<span data-ttu-id="7855d-159">…</span><span class="sxs-lookup"><span data-stu-id="7855d-159">…</span></span>|  
  
### <a name="object"></a><span data-ttu-id="7855d-160">对象</span><span class="sxs-lookup"><span data-stu-id="7855d-160">Object</span></span>  

 <span data-ttu-id="7855d-161">[命名类型构造函数](named-type-constructor-entity-sql.md) 构造 (名) 用户定义对象，例如 `person("abc", 12)` 。</span><span class="sxs-lookup"><span data-stu-id="7855d-161">[Named Type Constructor](named-type-constructor-entity-sql.md) constructs (named) user-defined objects, such as `person("abc", 12)`.</span></span>  
  
 <span data-ttu-id="7855d-162">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-162">Example:</span></span>  
  
```sql  
SELECT VALUE AdventureWorksModel.SalesOrderDetail (o.SalesOrderDetailID, o.CarrierTrackingNumber, o.OrderQty,
o.ProductID, o.SpecialOfferID, o.UnitPrice, o.UnitPriceDiscount,
o.rowguid, o.ModifiedDate) FROM AdventureWorksEntities.SalesOrderDetail
AS o  
```  
  
 <span data-ttu-id="7855d-163">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-163">Output:</span></span>  
  
|<span data-ttu-id="7855d-164">SalesOrderDetailID</span><span class="sxs-lookup"><span data-stu-id="7855d-164">SalesOrderDetailID</span></span>|<span data-ttu-id="7855d-165">CarrierTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="7855d-165">CarrierTrackingNumber</span></span>|<span data-ttu-id="7855d-166">OrderQty</span><span class="sxs-lookup"><span data-stu-id="7855d-166">OrderQty</span></span>|<span data-ttu-id="7855d-167">ProductID</span><span class="sxs-lookup"><span data-stu-id="7855d-167">ProductID</span></span>|<span data-ttu-id="7855d-168">...</span><span class="sxs-lookup"><span data-stu-id="7855d-168">...</span></span>|  
|------------------------|---------------------------|--------------|---------------|---------|  
|<span data-ttu-id="7855d-169">1</span><span class="sxs-lookup"><span data-stu-id="7855d-169">1</span></span>|<span data-ttu-id="7855d-170">4911-403C-98</span><span class="sxs-lookup"><span data-stu-id="7855d-170">4911-403C-98</span></span>|<span data-ttu-id="7855d-171">1</span><span class="sxs-lookup"><span data-stu-id="7855d-171">1</span></span>|<span data-ttu-id="7855d-172">776</span><span class="sxs-lookup"><span data-stu-id="7855d-172">776</span></span>|<span data-ttu-id="7855d-173">...</span><span class="sxs-lookup"><span data-stu-id="7855d-173">...</span></span>|  
|<span data-ttu-id="7855d-174">2</span><span class="sxs-lookup"><span data-stu-id="7855d-174">2</span></span>|<span data-ttu-id="7855d-175">4911-403C-98</span><span class="sxs-lookup"><span data-stu-id="7855d-175">4911-403C-98</span></span>|<span data-ttu-id="7855d-176">3</span><span class="sxs-lookup"><span data-stu-id="7855d-176">3</span></span>|<span data-ttu-id="7855d-177">777</span><span class="sxs-lookup"><span data-stu-id="7855d-177">777</span></span>|<span data-ttu-id="7855d-178">...</span><span class="sxs-lookup"><span data-stu-id="7855d-178">...</span></span>|  
|<span data-ttu-id="7855d-179">...</span><span class="sxs-lookup"><span data-stu-id="7855d-179">...</span></span>|<span data-ttu-id="7855d-180">...</span><span class="sxs-lookup"><span data-stu-id="7855d-180">...</span></span>|<span data-ttu-id="7855d-181">...</span><span class="sxs-lookup"><span data-stu-id="7855d-181">...</span></span>|<span data-ttu-id="7855d-182">...</span><span class="sxs-lookup"><span data-stu-id="7855d-182">...</span></span>|<span data-ttu-id="7855d-183">...</span><span class="sxs-lookup"><span data-stu-id="7855d-183">...</span></span>|  
  
## <a name="references"></a><span data-ttu-id="7855d-184">参考</span><span class="sxs-lookup"><span data-stu-id="7855d-184">References</span></span>  
  
### <a name="ref"></a><span data-ttu-id="7855d-185">REF</span><span class="sxs-lookup"><span data-stu-id="7855d-185">REF</span></span>  

 <span data-ttu-id="7855d-186">[REF](ref-entity-sql.md) 创建对实体类型实例的引用。</span><span class="sxs-lookup"><span data-stu-id="7855d-186">[REF](ref-entity-sql.md) creates a reference to an entity type instance.</span></span> <span data-ttu-id="7855d-187">例如，下面的查询返回对 Orders 实体集中每一个 Order 实体的引用：</span><span class="sxs-lookup"><span data-stu-id="7855d-187">For example, the following query returns references to each Order entity in the Orders entity set:</span></span>  
  
```sql  
SELECT REF(o) AS OrderID FROM Orders AS o  
```  
  
 <span data-ttu-id="7855d-188">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-188">Output:</span></span>  
  
|<span data-ttu-id="7855d-189">值</span><span class="sxs-lookup"><span data-stu-id="7855d-189">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-190">1</span><span class="sxs-lookup"><span data-stu-id="7855d-190">1</span></span>|  
|<span data-ttu-id="7855d-191">2</span><span class="sxs-lookup"><span data-stu-id="7855d-191">2</span></span>|  
|<span data-ttu-id="7855d-192">3</span><span class="sxs-lookup"><span data-stu-id="7855d-192">3</span></span>|  
|<span data-ttu-id="7855d-193">...</span><span class="sxs-lookup"><span data-stu-id="7855d-193">...</span></span>|  
  
 <span data-ttu-id="7855d-194">下面的示例使用属性提取运算符 (.) 访问实体的属性。</span><span class="sxs-lookup"><span data-stu-id="7855d-194">The following example uses the property extraction operator (.) to access a property of an entity.</span></span> <span data-ttu-id="7855d-195">在使用属性提取运算符时，引用将自动被反引用。</span><span class="sxs-lookup"><span data-stu-id="7855d-195">When the property extraction operator is used, the reference is automatically dereferenced.</span></span>  
  
 <span data-ttu-id="7855d-196">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-196">Example:</span></span>  
  
```sql  
SELECT VALUE REF(p).Name FROM
    AdventureWorksEntities.Product AS p
```  
  
 <span data-ttu-id="7855d-197">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-197">Output:</span></span>  
  
|<span data-ttu-id="7855d-198">值</span><span class="sxs-lookup"><span data-stu-id="7855d-198">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-199">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="7855d-199">Adjustable Race</span></span>|  
|<span data-ttu-id="7855d-200">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="7855d-200">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="7855d-201">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="7855d-201">AWC Logo Cap</span></span>|  
|<span data-ttu-id="7855d-202">...</span><span class="sxs-lookup"><span data-stu-id="7855d-202">...</span></span>|  
  
### <a name="deref"></a><span data-ttu-id="7855d-203">DEREF</span><span class="sxs-lookup"><span data-stu-id="7855d-203">DEREF</span></span>  

 <span data-ttu-id="7855d-204">[DEREF](deref-entity-sql.md) 取消引用一个引用值，并生成该取消引用的结果。</span><span class="sxs-lookup"><span data-stu-id="7855d-204">[DEREF](deref-entity-sql.md) dereferences a reference value and produces the result of that dereference.</span></span> <span data-ttu-id="7855d-205">例如，下面的查询生成 Orders 实体集中每一个 Order 的 Order 实体：`SELECT DEREF(o2.r) FROM (SELECT REF(o) AS r FROM LOB.Orders AS o) AS o2`。</span><span class="sxs-lookup"><span data-stu-id="7855d-205">For example, the following query produces the Order entities for each Order in the Orders entity set: `SELECT DEREF(o2.r) FROM (SELECT REF(o) AS r FROM LOB.Orders AS o) AS o2`..</span></span>  
  
 <span data-ttu-id="7855d-206">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-206">Example:</span></span>  
  
```sql  
SELECT VALUE DEREF(REF(p)).Name FROM
    AdventureWorksEntities.Product AS p
```  
  
 <span data-ttu-id="7855d-207">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-207">Output:</span></span>  
  
|<span data-ttu-id="7855d-208">值</span><span class="sxs-lookup"><span data-stu-id="7855d-208">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-209">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="7855d-209">Adjustable Race</span></span>|  
|<span data-ttu-id="7855d-210">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="7855d-210">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="7855d-211">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="7855d-211">AWC Logo Cap</span></span>|  
|<span data-ttu-id="7855d-212">...</span><span class="sxs-lookup"><span data-stu-id="7855d-212">...</span></span>|  
  
### <a name="createref-and-key"></a><span data-ttu-id="7855d-213">CREATEREF 和 KEY</span><span class="sxs-lookup"><span data-stu-id="7855d-213">CREATEREF AND KEY</span></span>  

 <span data-ttu-id="7855d-214">[CREATEREF](createref-entity-sql.md) 创建一个传递密钥的引用。</span><span class="sxs-lookup"><span data-stu-id="7855d-214">[CREATEREF](createref-entity-sql.md) creates a reference passing a key.</span></span> <span data-ttu-id="7855d-215">[KEY](key-entity-sql.md) 提取具有类型引用的表达式的键部分。</span><span class="sxs-lookup"><span data-stu-id="7855d-215">[KEY](key-entity-sql.md) extracts the key portion of an expression with type reference.</span></span>  
  
 <span data-ttu-id="7855d-216">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-216">Example:</span></span>  
  
```sql  
SELECT VALUE Key(CreateRef(AdventureWorksEntities.Product, row(p.ProductID)))
    FROM AdventureWorksEntities.Product AS p
```  
  
 <span data-ttu-id="7855d-217">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-217">Output:</span></span>  
  
|<span data-ttu-id="7855d-218">ProductID</span><span class="sxs-lookup"><span data-stu-id="7855d-218">ProductID</span></span>|  
|---------------|  
|<span data-ttu-id="7855d-219">980</span><span class="sxs-lookup"><span data-stu-id="7855d-219">980</span></span>|  
|<span data-ttu-id="7855d-220">365</span><span class="sxs-lookup"><span data-stu-id="7855d-220">365</span></span>|  
|<span data-ttu-id="7855d-221">771</span><span class="sxs-lookup"><span data-stu-id="7855d-221">771</span></span>|  
|<span data-ttu-id="7855d-222">...</span><span class="sxs-lookup"><span data-stu-id="7855d-222">...</span></span>|  
  
## <a name="functions"></a><span data-ttu-id="7855d-223">函数</span><span class="sxs-lookup"><span data-stu-id="7855d-223">Functions</span></span>  
  
### <a name="canonical"></a><span data-ttu-id="7855d-224">Canonical</span><span class="sxs-lookup"><span data-stu-id="7855d-224">Canonical</span></span>  

 <span data-ttu-id="7855d-225">[规范函数](canonical-functions.md)的命名空间为 Edm，如中所示 `Edm.Length("string")` 。</span><span class="sxs-lookup"><span data-stu-id="7855d-225">The namespace for [canonical functions](canonical-functions.md) is Edm, as in `Edm.Length("string")`.</span></span> <span data-ttu-id="7855d-226">您无需指定命名空间，除非导入的另一个命名空间中包含与规范函数同名的函数。</span><span class="sxs-lookup"><span data-stu-id="7855d-226">You do not have to specify the namespace unless another namespace is imported that contains a function with the same name as a canonical function.</span></span> <span data-ttu-id="7855d-227">如果两个命名空间有相同的函数，用户应指定完整名称。</span><span class="sxs-lookup"><span data-stu-id="7855d-227">If two namespaces have the same function, the user should specific the full name.</span></span>  
  
 <span data-ttu-id="7855d-228">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-228">Example:</span></span>  
  
```sql  
SELECT Length(c. FirstName) AS NameLen FROM
    AdventureWorksEntities.Contact AS c
    WHERE c.ContactID BETWEEN 10 AND 12  
```  
  
 <span data-ttu-id="7855d-229">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-229">Output:</span></span>  
  
|<span data-ttu-id="7855d-230">NameLen</span><span class="sxs-lookup"><span data-stu-id="7855d-230">NameLen</span></span>|  
|-------------|  
|<span data-ttu-id="7855d-231">6</span><span class="sxs-lookup"><span data-stu-id="7855d-231">6</span></span>|  
|<span data-ttu-id="7855d-232">6</span><span class="sxs-lookup"><span data-stu-id="7855d-232">6</span></span>|  
|<span data-ttu-id="7855d-233">5</span><span class="sxs-lookup"><span data-stu-id="7855d-233">5</span></span>|  
  
### <a name="microsoft-provider-specific"></a><span data-ttu-id="7855d-234">特定于 Microsoft 提供程序</span><span class="sxs-lookup"><span data-stu-id="7855d-234">Microsoft Provider-Specific</span></span>  

 <span data-ttu-id="7855d-235">命名空间中有[特定于 Microsoft 提供程序的函数](../sqlclient-for-ef-functions.md) `SqlServer` 。</span><span class="sxs-lookup"><span data-stu-id="7855d-235">[Microsoft provider-specific functions](../sqlclient-for-ef-functions.md) are in the `SqlServer` namespace.</span></span>  
  
 <span data-ttu-id="7855d-236">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-236">Example:</span></span>  
  
```sql  
SELECT SqlServer.LEN(c.EmailAddress) AS EmailLen FROM
    AdventureWorksEntities.Contact AS c WHERE
    c.ContactID BETWEEN 10 AND 12  
```  
  
 <span data-ttu-id="7855d-237">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-237">Output:</span></span>  
  
|<span data-ttu-id="7855d-238">EmailLen</span><span class="sxs-lookup"><span data-stu-id="7855d-238">EmailLen</span></span>|  
|--------------|  
|<span data-ttu-id="7855d-239">27</span><span class="sxs-lookup"><span data-stu-id="7855d-239">27</span></span>|  
|<span data-ttu-id="7855d-240">27</span><span class="sxs-lookup"><span data-stu-id="7855d-240">27</span></span>|  
|<span data-ttu-id="7855d-241">26</span><span class="sxs-lookup"><span data-stu-id="7855d-241">26</span></span>|  
  
## <a name="namespaces"></a><span data-ttu-id="7855d-242">命名空间</span><span class="sxs-lookup"><span data-stu-id="7855d-242">Namespaces</span></span>  

 <span data-ttu-id="7855d-243">[USING](using-entity-sql.md) 指定查询表达式中使用的命名空间。</span><span class="sxs-lookup"><span data-stu-id="7855d-243">[USING](using-entity-sql.md) specifies namespaces used in a query expression.</span></span>  
  
 <span data-ttu-id="7855d-244">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-244">Example:</span></span>  
  
```sql  
using SqlServer; LOWER('AA');  
```  
  
 <span data-ttu-id="7855d-245">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-245">Output:</span></span>  
  
|<span data-ttu-id="7855d-246">值</span><span class="sxs-lookup"><span data-stu-id="7855d-246">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-247">aa</span><span class="sxs-lookup"><span data-stu-id="7855d-247">aa</span></span>|  
  
## <a name="paging"></a><span data-ttu-id="7855d-248">Paging</span><span class="sxs-lookup"><span data-stu-id="7855d-248">Paging</span></span>  

 <span data-ttu-id="7855d-249">可以通过在[ORDER by](order-by-entity-sql.md)子句中声明[SKIP](skip-entity-sql.md)和[LIMIT](limit-entity-sql.md)子子句来表示分页。</span><span class="sxs-lookup"><span data-stu-id="7855d-249">Paging can be expressed by declaring a [SKIP](skip-entity-sql.md) and [LIMIT](limit-entity-sql.md) sub-clauses to the [ORDER BY](order-by-entity-sql.md) clause.</span></span>  
  
 <span data-ttu-id="7855d-250">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-250">Example:</span></span>  
  
```sql  
SELECT c.ContactID as ID, c.LastName AS Name FROM
    AdventureWorks.Contact AS c ORDER BY c.ContactID SKIP 9 LIMIT 3;  
```  
  
 <span data-ttu-id="7855d-251">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-251">Output:</span></span>  
  
|<span data-ttu-id="7855d-252">ID</span><span class="sxs-lookup"><span data-stu-id="7855d-252">ID</span></span>|<span data-ttu-id="7855d-253">名称</span><span class="sxs-lookup"><span data-stu-id="7855d-253">Name</span></span>|  
|--------|----------|  
|<span data-ttu-id="7855d-254">10</span><span class="sxs-lookup"><span data-stu-id="7855d-254">10</span></span>|<span data-ttu-id="7855d-255">Adina</span><span class="sxs-lookup"><span data-stu-id="7855d-255">Adina</span></span>|  
|<span data-ttu-id="7855d-256">11</span><span class="sxs-lookup"><span data-stu-id="7855d-256">11</span></span>|<span data-ttu-id="7855d-257">Agcaoili</span><span class="sxs-lookup"><span data-stu-id="7855d-257">Agcaoili</span></span>|  
|<span data-ttu-id="7855d-258">12</span><span class="sxs-lookup"><span data-stu-id="7855d-258">12</span></span>|<span data-ttu-id="7855d-259">Aguilar</span><span class="sxs-lookup"><span data-stu-id="7855d-259">Aguilar</span></span>|  
  
## <a name="grouping"></a><span data-ttu-id="7855d-260">分组</span><span class="sxs-lookup"><span data-stu-id="7855d-260">Grouping</span></span>  

 <span data-ttu-id="7855d-261">[分组依据](group-by-entity-sql.md) 指定由查询返回的对象 ([选择](select-entity-sql.md) 要放置) 表达式的组。</span><span class="sxs-lookup"><span data-stu-id="7855d-261">[GROUPING BY](group-by-entity-sql.md) specifies groups into which objects returned by a query ([SELECT](select-entity-sql.md)) expression are to be placed.</span></span>  
  
 <span data-ttu-id="7855d-262">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-262">Example:</span></span>  
  
```sql  
SELECT VALUE name FROM AdventureWorksEntities.Product AS P
    GROUP BY P.Name HAVING MAX(P.ListPrice) > 5  
```  
  
 <span data-ttu-id="7855d-263">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-263">Output:</span></span>  
  
|<span data-ttu-id="7855d-264">name</span><span class="sxs-lookup"><span data-stu-id="7855d-264">name</span></span>|  
|----------|  
|<span data-ttu-id="7855d-265">LL Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="7855d-265">LL Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="7855d-266">ML Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="7855d-266">ML Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="7855d-267">HL Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="7855d-267">HL Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="7855d-268">...</span><span class="sxs-lookup"><span data-stu-id="7855d-268">...</span></span>|  
  
## <a name="navigation"></a><span data-ttu-id="7855d-269">导航</span><span class="sxs-lookup"><span data-stu-id="7855d-269">Navigation</span></span>  

 <span data-ttu-id="7855d-270">关系导航运算符用于导航从一个实体（起始端）到另一个实体（结束端）的关系。</span><span class="sxs-lookup"><span data-stu-id="7855d-270">The relationship navigation operator allows you to navigate over the relationship from one entity (from end) to another (to end).</span></span> <span data-ttu-id="7855d-271">[导航](navigate-entity-sql.md)采用 \<namespace> 限定为的关系类型。 \<relationship type name></span><span class="sxs-lookup"><span data-stu-id="7855d-271">[NAVIGATE](navigate-entity-sql.md) takes the relationship type qualified as \<namespace>.\<relationship type name>.</span></span> <span data-ttu-id="7855d-272">\<T>如果结束端的基数为1，则导航返回 Ref。</span><span class="sxs-lookup"><span data-stu-id="7855d-272">Navigate returns Ref\<T> if the cardinality of the to end is 1.</span></span> <span data-ttu-id="7855d-273">如果结束端的基数为 n，将返回<引用> 的集合 \<T> 。</span><span class="sxs-lookup"><span data-stu-id="7855d-273">If the cardinality of the to end is n, the Collection<Ref\<T>> will be returned.</span></span>  
  
 <span data-ttu-id="7855d-274">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-274">Example:</span></span>  
  
```sql  
SELECT a.AddressID, (SELECT VALUE DEREF(v) FROM
    NAVIGATE(a, AdventureWorksModel.FK_SalesOrderHeader_Address_BillToAddressID) AS v)
    FROM AdventureWorksEntities.Address AS a  
```  
  
 <span data-ttu-id="7855d-275">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-275">Output:</span></span>  
  
|<span data-ttu-id="7855d-276">AddressID</span><span class="sxs-lookup"><span data-stu-id="7855d-276">AddressID</span></span>|  
|---------------|  
|<span data-ttu-id="7855d-277">1</span><span class="sxs-lookup"><span data-stu-id="7855d-277">1</span></span>|  
|<span data-ttu-id="7855d-278">2</span><span class="sxs-lookup"><span data-stu-id="7855d-278">2</span></span>|  
|<span data-ttu-id="7855d-279">3</span><span class="sxs-lookup"><span data-stu-id="7855d-279">3</span></span>|  
|<span data-ttu-id="7855d-280">...</span><span class="sxs-lookup"><span data-stu-id="7855d-280">...</span></span>|  
  
## <a name="select-value-and-select"></a><span data-ttu-id="7855d-281">SELECT VALUE 和 SELECT</span><span class="sxs-lookup"><span data-stu-id="7855d-281">SELECT VALUE AND SELECT</span></span>  
  
### <a name="select-value"></a><span data-ttu-id="7855d-282">SELECT VALUE</span><span class="sxs-lookup"><span data-stu-id="7855d-282">SELECT VALUE</span></span>  

 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="7855d-283">提供了 SELECT VALUE 子句以跳过隐式行构造。</span><span class="sxs-lookup"><span data-stu-id="7855d-283">provides the SELECT VALUE clause to skip the implicit row construction.</span></span> <span data-ttu-id="7855d-284">SELECT VALUE 子句中只能指定一项。</span><span class="sxs-lookup"><span data-stu-id="7855d-284">Only one item can be specified in a SELECT VALUE clause.</span></span> <span data-ttu-id="7855d-285">使用此类子句时，将不会围绕 SELECT 子句中的项构造行包装器，并且可生成所需形状的集合，例如： `SELECT VALUE a` 。</span><span class="sxs-lookup"><span data-stu-id="7855d-285">When such a clause is used, no row wrapper is constructed around the items in the SELECT clause, and a collection of the desired shape can be produced, for example: `SELECT VALUE a`.</span></span>  
  
 <span data-ttu-id="7855d-286">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-286">Example:</span></span>  
  
```sql  
SELECT VALUE p.Name FROM AdventureWorksEntities.Product AS p
```  
  
 <span data-ttu-id="7855d-287">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-287">Output:</span></span>  
  
|<span data-ttu-id="7855d-288">名称</span><span class="sxs-lookup"><span data-stu-id="7855d-288">Name</span></span>|  
|----------|  
|<span data-ttu-id="7855d-289">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="7855d-289">Adjustable Race</span></span>|  
|<span data-ttu-id="7855d-290">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="7855d-290">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="7855d-291">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="7855d-291">AWC Logo Cap</span></span>|  
|<span data-ttu-id="7855d-292">...</span><span class="sxs-lookup"><span data-stu-id="7855d-292">...</span></span>|  
  
### <a name="select"></a><span data-ttu-id="7855d-293">SELECT</span><span class="sxs-lookup"><span data-stu-id="7855d-293">SELECT</span></span>  

 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="7855d-294">还提供了用于构造任意行的行构造函数。</span><span class="sxs-lookup"><span data-stu-id="7855d-294">also provides the row constructor to construct arbitrary rows.</span></span> <span data-ttu-id="7855d-295">SELECT 接受投影中的一个或多个元素，并生成含有字段的数据记录，例如：`SELECT a, b, c`。</span><span class="sxs-lookup"><span data-stu-id="7855d-295">SELECT takes one or more elements in the projection and results in a data record with fields, for example: `SELECT a, b, c`.</span></span>  
  
 <span data-ttu-id="7855d-296">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-296">Example:</span></span>  
  
 <span data-ttu-id="7855d-297">SELECT p.Name, p.ProductID FROM AdventureWorksEntities.Product as p Output:</span><span class="sxs-lookup"><span data-stu-id="7855d-297">SELECT p.Name, p.ProductID FROM AdventureWorksEntities.Product as p Output:</span></span>  
  
|<span data-ttu-id="7855d-298">名称</span><span class="sxs-lookup"><span data-stu-id="7855d-298">Name</span></span>|<span data-ttu-id="7855d-299">ProductID</span><span class="sxs-lookup"><span data-stu-id="7855d-299">ProductID</span></span>|  
|----------|---------------|  
|<span data-ttu-id="7855d-300">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="7855d-300">Adjustable Race</span></span>|<span data-ttu-id="7855d-301">1</span><span class="sxs-lookup"><span data-stu-id="7855d-301">1</span></span>|  
|<span data-ttu-id="7855d-302">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="7855d-302">All-Purpose Bike Stand</span></span>|<span data-ttu-id="7855d-303">879</span><span class="sxs-lookup"><span data-stu-id="7855d-303">879</span></span>|  
|<span data-ttu-id="7855d-304">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="7855d-304">AWC Logo Cap</span></span>|<span data-ttu-id="7855d-305">712</span><span class="sxs-lookup"><span data-stu-id="7855d-305">712</span></span>|  
|<span data-ttu-id="7855d-306">...</span><span class="sxs-lookup"><span data-stu-id="7855d-306">...</span></span>|<span data-ttu-id="7855d-307">...</span><span class="sxs-lookup"><span data-stu-id="7855d-307">...</span></span>|  
  
## <a name="case-expression"></a><span data-ttu-id="7855d-308">CASE 表达式</span><span class="sxs-lookup"><span data-stu-id="7855d-308">CASE EXPRESSION</span></span>  

 <span data-ttu-id="7855d-309">[Case 表达式](case-entity-sql.md)计算一组布尔表达式的值以确定结果。</span><span class="sxs-lookup"><span data-stu-id="7855d-309">The [case expression](case-entity-sql.md) evaluates a set of Boolean expressions to determine the result.</span></span>  
  
 <span data-ttu-id="7855d-310">例如：</span><span class="sxs-lookup"><span data-stu-id="7855d-310">Example:</span></span>  
  
```sql  
CASE WHEN AVG({25,12,11}) < 100 THEN TRUE ELSE FALSE END  
```  
  
 <span data-ttu-id="7855d-311">输出：</span><span class="sxs-lookup"><span data-stu-id="7855d-311">Output:</span></span>  
  
|<span data-ttu-id="7855d-312">值</span><span class="sxs-lookup"><span data-stu-id="7855d-312">Value</span></span>|  
|-----------|  
|<span data-ttu-id="7855d-313">true</span><span class="sxs-lookup"><span data-stu-id="7855d-313">TRUE</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7855d-314">请参阅</span><span class="sxs-lookup"><span data-stu-id="7855d-314">See also</span></span>

- [<span data-ttu-id="7855d-315">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="7855d-315">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="7855d-316">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="7855d-316">Entity SQL Overview</span></span>](entity-sql-overview.md)

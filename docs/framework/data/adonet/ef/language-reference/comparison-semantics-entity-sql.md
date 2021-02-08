---
description: '了解详细信息：比较语义 (实体 SQL) '
title: 比较语义 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: b36ce28a-2fe4-4236-b782-e5f7c054deae
ms.openlocfilehash: b1c832cb6f2903073b1c6be806c73823b1f4a220
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786428"
---
# <a name="comparison-semantics-entity-sql"></a><span data-ttu-id="b2ab3-103">比较语义 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="b2ab3-103">Comparison Semantics (Entity SQL)</span></span>

<span data-ttu-id="b2ab3-104">执行下列任一 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 运算符时都涉及类型实例的比较：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-104">Performing any of the following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] operators involves comparison of type instances:</span></span>  
  
## <a name="explicit-comparison"></a><span data-ttu-id="b2ab3-105">显式比较</span><span class="sxs-lookup"><span data-stu-id="b2ab3-105">Explicit comparison</span></span>  

 <span data-ttu-id="b2ab3-106">相等运算：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-106">Equality operations:</span></span>  
  
- =  
  
- <span data-ttu-id="b2ab3-107">!=</span><span class="sxs-lookup"><span data-stu-id="b2ab3-107">!=</span></span>  
  
 <span data-ttu-id="b2ab3-108">排序运算：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-108">Ordering operations:</span></span>  
  
- <  
  
- \<=  
  
- \>  
  
- \>=  
  
 <span data-ttu-id="b2ab3-109">判断是否可为 Null 的运算：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-109">Nullability operations:</span></span>  
  
- <span data-ttu-id="b2ab3-110">为 NULL</span><span class="sxs-lookup"><span data-stu-id="b2ab3-110">IS NULL</span></span>  
  
- <span data-ttu-id="b2ab3-111">IS NOT NULL</span><span class="sxs-lookup"><span data-stu-id="b2ab3-111">IS NOT NULL</span></span>  
  
## <a name="explicit-distinction"></a><span data-ttu-id="b2ab3-112">显式区别</span><span class="sxs-lookup"><span data-stu-id="b2ab3-112">Explicit distinction</span></span>  

 <span data-ttu-id="b2ab3-113">相等区别：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-113">Equality distinction:</span></span>  
  
- <span data-ttu-id="b2ab3-114">DISTINCT</span><span class="sxs-lookup"><span data-stu-id="b2ab3-114">DISTINCT</span></span>  
  
- <span data-ttu-id="b2ab3-115">GROUP BY</span><span class="sxs-lookup"><span data-stu-id="b2ab3-115">GROUP BY</span></span>  
  
 <span data-ttu-id="b2ab3-116">排序区别：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-116">Ordering distinction:</span></span>  
  
- <span data-ttu-id="b2ab3-117">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="b2ab3-117">ORDER BY</span></span>  
  
## <a name="implicit-distinction"></a><span data-ttu-id="b2ab3-118">隐式区别</span><span class="sxs-lookup"><span data-stu-id="b2ab3-118">Implicit distinction</span></span>  

 <span data-ttu-id="b2ab3-119">集运算和谓词（相等）：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-119">Set operations and predicates (equality):</span></span>  
  
- <span data-ttu-id="b2ab3-120">UNION</span><span class="sxs-lookup"><span data-stu-id="b2ab3-120">UNION</span></span>  
  
- <span data-ttu-id="b2ab3-121">INTERSECT</span><span class="sxs-lookup"><span data-stu-id="b2ab3-121">INTERSECT</span></span>  
  
- <span data-ttu-id="b2ab3-122">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="b2ab3-122">EXCEPT</span></span>  
  
- <span data-ttu-id="b2ab3-123">SET</span><span class="sxs-lookup"><span data-stu-id="b2ab3-123">SET</span></span>  
  
- <span data-ttu-id="b2ab3-124">OVERLAPS</span><span class="sxs-lookup"><span data-stu-id="b2ab3-124">OVERLAPS</span></span>  
  
 <span data-ttu-id="b2ab3-125">项谓词（相等）：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-125">Item predicates (equality):</span></span>  
  
- <span data-ttu-id="b2ab3-126">IN</span><span class="sxs-lookup"><span data-stu-id="b2ab3-126">IN</span></span>  
  
## <a name="supported-combinations"></a><span data-ttu-id="b2ab3-127">支持的组合</span><span class="sxs-lookup"><span data-stu-id="b2ab3-127">Supported Combinations</span></span>  

 <span data-ttu-id="b2ab3-128">下表说明了每种类型的比较运算符的所有受支持的组合：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-128">The following table shows all the supported combinations of comparison operators for each kind of type:</span></span>  
  
|<span data-ttu-id="b2ab3-129">**类型**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-129">**Type**</span></span>|**=**<br /><br /> <span data-ttu-id="b2ab3-130">**!=**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-130">**!=**</span></span>|<span data-ttu-id="b2ab3-131">**GROUP BY**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-131">**GROUP BY**</span></span><br /><br /> <span data-ttu-id="b2ab3-132">**DISTINCT**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-132">**DISTINCT**</span></span>|<span data-ttu-id="b2ab3-133">**UNION**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-133">**UNION**</span></span><br /><br /> <span data-ttu-id="b2ab3-134">**INTERSECT**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-134">**INTERSECT**</span></span><br /><br /> <span data-ttu-id="b2ab3-135">**EXCEPT**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-135">**EXCEPT**</span></span><br /><br /> <span data-ttu-id="b2ab3-136">**SET**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-136">**SET**</span></span><br /><br /> <span data-ttu-id="b2ab3-137">**OVERLAPS**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-137">**OVERLAPS**</span></span>|<span data-ttu-id="b2ab3-138">**IN**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-138">**IN**</span></span>|<span data-ttu-id="b2ab3-139">**<   <=**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-139">**<   <=**</span></span><br /><br /> <span data-ttu-id="b2ab3-140">**>   >=**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-140">**>   >=**</span></span>|<span data-ttu-id="b2ab3-141">**ORDER BY**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-141">**ORDER BY**</span></span>|<span data-ttu-id="b2ab3-142">**为 NULL**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-142">**IS NULL**</span></span><br /><br /> <span data-ttu-id="b2ab3-143">**不为 NULL**</span><span class="sxs-lookup"><span data-stu-id="b2ab3-143">**IS NOT NULL**</span></span>|  
|-|-|-|-|-|-|-|-|  
|<span data-ttu-id="b2ab3-144">实体类型</span><span class="sxs-lookup"><span data-stu-id="b2ab3-144">Entity type</span></span>|<span data-ttu-id="b2ab3-145">Ref<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-145">Ref<sup>1</sup></span></span>|<span data-ttu-id="b2ab3-146">所有属性<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-146">All properties<sup>2</sup></span></span>|<span data-ttu-id="b2ab3-147">所有属性<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-147">All properties<sup>2</sup></span></span>|<span data-ttu-id="b2ab3-148">所有属性<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-148">All properties<sup>2</sup></span></span>|<span data-ttu-id="b2ab3-149">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-149">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-150">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-150">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-151">Ref<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-151">Ref<sup>1</sup></span></span>|  
|<span data-ttu-id="b2ab3-152">复杂类型</span><span class="sxs-lookup"><span data-stu-id="b2ab3-152">Complex type</span></span>|<span data-ttu-id="b2ab3-153">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-153">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-154">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-154">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-155">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-155">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-156">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-156">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-157">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-157">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-158">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-158">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-159">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-159">Throw<sup>3</sup></span></span>|  
|<span data-ttu-id="b2ab3-160">行</span><span class="sxs-lookup"><span data-stu-id="b2ab3-160">Row</span></span>|<span data-ttu-id="b2ab3-161">所有属性<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-161">All properties<sup>4</sup></span></span>|<span data-ttu-id="b2ab3-162">所有属性<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-162">All properties<sup>4</sup></span></span>|<span data-ttu-id="b2ab3-163">所有属性<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-163">All properties<sup>4</sup></span></span>|<span data-ttu-id="b2ab3-164">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-164">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-165">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-165">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-166">所有属性<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-166">All properties<sup>4</sup></span></span>|<span data-ttu-id="b2ab3-167">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-167">Throw<sup>3</sup></span></span>|  
|<span data-ttu-id="b2ab3-168">基元类型</span><span class="sxs-lookup"><span data-stu-id="b2ab3-168">Primitive type</span></span>|<span data-ttu-id="b2ab3-169">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-169">Provider-specific</span></span>|<span data-ttu-id="b2ab3-170">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-170">Provider-specific</span></span>|<span data-ttu-id="b2ab3-171">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-171">Provider-specific</span></span>|<span data-ttu-id="b2ab3-172">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-172">Provider-specific</span></span>|<span data-ttu-id="b2ab3-173">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-173">Provider-specific</span></span>|<span data-ttu-id="b2ab3-174">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-174">Provider-specific</span></span>|<span data-ttu-id="b2ab3-175">特定于提供程序</span><span class="sxs-lookup"><span data-stu-id="b2ab3-175">Provider-specific</span></span>|  
|<span data-ttu-id="b2ab3-176">多集</span><span class="sxs-lookup"><span data-stu-id="b2ab3-176">Multiset</span></span>|<span data-ttu-id="b2ab3-177">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-177">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-178">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-178">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-179">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-179">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-180">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-180">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-181">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-181">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-182">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-182">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-183">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-183">Throw<sup>3</sup></span></span>|  
|<span data-ttu-id="b2ab3-184">引用</span><span class="sxs-lookup"><span data-stu-id="b2ab3-184">Ref</span></span>|<span data-ttu-id="b2ab3-185">是<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-185">Yes<sup>5</sup></span></span>|<span data-ttu-id="b2ab3-186">是<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-186">Yes<sup>5</sup></span></span>|<span data-ttu-id="b2ab3-187">是<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-187">Yes<sup>5</sup></span></span>|<span data-ttu-id="b2ab3-188">是<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-188">Yes<sup>5</sup></span></span>|<span data-ttu-id="b2ab3-189">Throw</span><span class="sxs-lookup"><span data-stu-id="b2ab3-189">Throw</span></span>|<span data-ttu-id="b2ab3-190">Throw</span><span class="sxs-lookup"><span data-stu-id="b2ab3-190">Throw</span></span>|<span data-ttu-id="b2ab3-191">是<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-191">Yes<sup>5</sup></span></span>|  
|<span data-ttu-id="b2ab3-192">关联</span><span class="sxs-lookup"><span data-stu-id="b2ab3-192">Association</span></span><br /><br /> <span data-ttu-id="b2ab3-193">type</span><span class="sxs-lookup"><span data-stu-id="b2ab3-193">type</span></span>|<span data-ttu-id="b2ab3-194">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-194">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-195">Throw</span><span class="sxs-lookup"><span data-stu-id="b2ab3-195">Throw</span></span>|<span data-ttu-id="b2ab3-196">Throw</span><span class="sxs-lookup"><span data-stu-id="b2ab3-196">Throw</span></span>|<span data-ttu-id="b2ab3-197">Throw</span><span class="sxs-lookup"><span data-stu-id="b2ab3-197">Throw</span></span>|<span data-ttu-id="b2ab3-198">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-198">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-199">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-199">Throw<sup>3</sup></span></span>|<span data-ttu-id="b2ab3-200">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-200">Throw<sup>3</sup></span></span>|  
  
 <span data-ttu-id="b2ab3-201"><sup>1</sup>给定实体类型实例的引用将被隐式比较，如下面的示例中所示：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-201"><sup>1</sup>The references of the given entity type instances are implicitly compared, as shown in the following example:</span></span>  
  
```sql  
SELECT p1, p2
FROM AdventureWorksEntities.Product AS p1
     JOIN AdventureWorksEntities.Product AS p2
WHERE p1 != p2 OR p1 IS NULL  
```  
  
 <span data-ttu-id="b2ab3-202">不能将实体实例与显式引用进行比较。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-202">An entity instance cannot be compared to an explicit reference.</span></span> <span data-ttu-id="b2ab3-203">如果试图这么做，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-203">If this is attempted, an exception is thrown.</span></span> <span data-ttu-id="b2ab3-204">例如，以下查询将引发异常：</span><span class="sxs-lookup"><span data-stu-id="b2ab3-204">For example, the following query will throw an exception:</span></span>  
  
```sql  
SELECT p1, p2
FROM AdventureWorksEntities.Product AS p1
     JOIN AdventureWorksEntities.Product AS p2
WHERE p1 != REF(p2)  
```  
  
 <span data-ttu-id="b2ab3-205"><sup>2</sup>在将复杂类型发送到存储区之前，会将其属性展开，因此只要它们的所有属性都是可比较的) ，它们就会变得可比较 (。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-205"><sup>2</sup>Properties of complex types are flattened out before being sent to the store, so they become comparable (as long as all their properties are comparable).</span></span> <span data-ttu-id="b2ab3-206">另请参阅 <sup>4。</sup></span><span class="sxs-lookup"><span data-stu-id="b2ab3-206">Also see <sup>4.</sup></span></span>  
  
 <span data-ttu-id="b2ab3-207"><sup>3</sup>实体框架运行时检测不受支持的情况，并引发有意义的异常，而不参与提供程序/存储。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-207"><sup>3</sup>The Entity Framework runtime detects the unsupported case and throws a meaningful exception without engaging the provider/store.</span></span>  
  
 <span data-ttu-id="b2ab3-208"><sup>4</sup>尝试比较所有属性。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-208"><sup>4</sup>An attempt is made to compare all properties.</span></span> <span data-ttu-id="b2ab3-209">如果某个属性的类型不可比较，例如 text、ntext 或 image，则可能引发服务器异常。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-209">If there is a property that is of a non-comparable type, such as text, ntext, or image, a server exception might be thrown.</span></span>  
  
 <span data-ttu-id="b2ab3-210"><sup>5</sup>将对引用的所有单个元素进行比较 (这包括实体类型的实体集名称和) 的所有键属性。</span><span class="sxs-lookup"><span data-stu-id="b2ab3-210"><sup>5</sup>All individual elements of the references are compared (this includes the entity set name and all the key properties of the entity type).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2ab3-211">请参阅</span><span class="sxs-lookup"><span data-stu-id="b2ab3-211">See also</span></span>

- [<span data-ttu-id="b2ab3-212">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="b2ab3-212">Entity SQL Overview</span></span>](entity-sql-overview.md)

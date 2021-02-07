---
description: '了解详细信息： CREATEREF (实体 SQL) '
title: CREATEREF (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 489828cf-a335-4449-9360-b0d92eec5481
ms.openlocfilehash: c4e96f97bd3587e50b34f6cbd63c5ae9ed8d94ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724773"
---
# <a name="createref-entity-sql"></a><span data-ttu-id="f550a-103">CREATEREF (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="f550a-103">CREATEREF (Entity SQL)</span></span>

<span data-ttu-id="f550a-104">创建对实体集中的实体的引用。</span><span class="sxs-lookup"><span data-stu-id="f550a-104">Fabricates references to an entity in an entityset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f550a-105">语法</span><span class="sxs-lookup"><span data-stu-id="f550a-105">Syntax</span></span>  
  
```sql  
CreateRef(entityset_identifier, row_typed_expression)  
```  
  
## <a name="arguments"></a><span data-ttu-id="f550a-106">参数</span><span class="sxs-lookup"><span data-stu-id="f550a-106">Arguments</span></span>  

 `entityset_identifier`  
 <span data-ttu-id="f550a-107">实体集标识符，不是字符串文本。</span><span class="sxs-lookup"><span data-stu-id="f550a-107">The entityset identifier, not a string literal.</span></span>  
  
 `row_typed_expression`  
 <span data-ttu-id="f550a-108">对应于实体类型的键属性的行类型化表达式。</span><span class="sxs-lookup"><span data-stu-id="f550a-108">A row-typed expression that corresponds to the key properties of the entity type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f550a-109">备注</span><span class="sxs-lookup"><span data-stu-id="f550a-109">Remarks</span></span>  

 <span data-ttu-id="f550a-110">`row_typed_expression` 必须在结构上等效于实体的键类型。</span><span class="sxs-lookup"><span data-stu-id="f550a-110">`row_typed_expression` must be structurally equivalent to the key type for the entity.</span></span> <span data-ttu-id="f550a-111">即，其字段的数目和类型以及顺序必须与实体键相同。</span><span class="sxs-lookup"><span data-stu-id="f550a-111">That is, it must have the same number and types of fields in the same order as the entity keys.</span></span>  
  
 <span data-ttu-id="f550a-112">在下面的示例中，Orders 和 BadOrders 都是类型 Order 的实体集，而假定 Id 为 Order 的单个键属性。</span><span class="sxs-lookup"><span data-stu-id="f550a-112">In the example below, Orders and BadOrders are both entitysets of type Order, and Id is assumed to be the single key property of Order.</span></span> <span data-ttu-id="f550a-113">该示例演示如何生成对 BadOrders 中的实体的引用。</span><span class="sxs-lookup"><span data-stu-id="f550a-113">The example illustrates how we may produce a reference to an entity in BadOrders.</span></span> <span data-ttu-id="f550a-114">请注意，该引用可以是无关联引用。</span><span class="sxs-lookup"><span data-stu-id="f550a-114">Note that the reference may be dangling.</span></span>  <span data-ttu-id="f550a-115">即，该引用可以不真正标识特定实体。</span><span class="sxs-lookup"><span data-stu-id="f550a-115">That is, the reference may not actually identify a specific entity.</span></span> <span data-ttu-id="f550a-116">在这种情况下，对该引用的 `DEREF` 操作会返回 Null。</span><span class="sxs-lookup"><span data-stu-id="f550a-116">In those cases, a `DEREF` operation on that reference returns a null.</span></span>  
  
```sql  
SELECT CreateRef(LOB.BadOrders, row(o.Id))
FROM LOB.Orders AS o
```  
  
## <a name="example"></a><span data-ttu-id="f550a-117">示例</span><span class="sxs-lookup"><span data-stu-id="f550a-117">Example</span></span>  

 <span data-ttu-id="f550a-118">下面的 Entity SQL 查询使用 CREATEREF 运算符创建对实体集中的实体的引用。</span><span class="sxs-lookup"><span data-stu-id="f550a-118">The following Entity SQL query uses the CREATEREF operator to fabricate references to an entity in an entity set.</span></span> <span data-ttu-id="f550a-119">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="f550a-119">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="f550a-120">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="f550a-120">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="f550a-121">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="f550a-121">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="f550a-122">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="f550a-122">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#CREATEREF](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#createref)]  
  
## <a name="see-also"></a><span data-ttu-id="f550a-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f550a-123">See also</span></span>

- [<span data-ttu-id="f550a-124">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="f550a-124">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="f550a-125">DEREF</span><span class="sxs-lookup"><span data-stu-id="f550a-125">DEREF</span></span>](deref-entity-sql.md)
- [<span data-ttu-id="f550a-126">KEY</span><span class="sxs-lookup"><span data-stu-id="f550a-126">KEY</span></span>](key-entity-sql.md)
- [<span data-ttu-id="f550a-127">REF</span><span class="sxs-lookup"><span data-stu-id="f550a-127">REF</span></span>](ref-entity-sql.md)

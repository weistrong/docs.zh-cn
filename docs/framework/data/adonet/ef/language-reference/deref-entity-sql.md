---
description: '了解详细信息： DEREF (实体 SQL) '
title: DEREF (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4c78e833-b260-453d-9bf4-eb39857dd0fa
ms.openlocfilehash: 9d0f29123c1459c6eab21ea9cd860b5c9e77f591
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724721"
---
# <a name="deref-entity-sql"></a><span data-ttu-id="d971e-103">DEREF (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="d971e-103">DEREF (Entity SQL)</span></span>

<span data-ttu-id="d971e-104">取消引用一个引用值，并生成该取消引用的结果。</span><span class="sxs-lookup"><span data-stu-id="d971e-104">Dereferences a reference value and produces the result of that dereference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d971e-105">语法</span><span class="sxs-lookup"><span data-stu-id="d971e-105">Syntax</span></span>  
  
```sql  
SELECT DEREF ( o.expression ) FROM Table AS o;
```  
  
## <a name="arguments"></a><span data-ttu-id="d971e-106">参数</span><span class="sxs-lookup"><span data-stu-id="d971e-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="d971e-107">任何返回集合的有效查询表达式。</span><span class="sxs-lookup"><span data-stu-id="d971e-107">Any valid query expression that returns a collection.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d971e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d971e-108">Return Value</span></span>  

 <span data-ttu-id="d971e-109">引用的实体的值。</span><span class="sxs-lookup"><span data-stu-id="d971e-109">The value of the entity that is referenced.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d971e-110">备注</span><span class="sxs-lookup"><span data-stu-id="d971e-110">Remarks</span></span>  

 <span data-ttu-id="d971e-111">DEREF 运算符取消引用一个引用值，并生成该取消引用的结果。</span><span class="sxs-lookup"><span data-stu-id="d971e-111">The DEREF operator dereferences a reference value and produces the result of that dereference.</span></span> <span data-ttu-id="d971e-112">例如，如果 `r` 是 ref 类型的引用 \<T> ， `Deref(r)` 则是类型的表达式， `T` 该表达式生成由引用的实体 `r` 。</span><span class="sxs-lookup"><span data-stu-id="d971e-112">For example, if `r` is a reference of type ref\<T>, `Deref(r)` is an expression of type `T` that yields the entity referenced by `r`.</span></span> <span data-ttu-id="d971e-113">如果引用值为 Null，或无关联（即，引用的目标不存在），则 DEREF 运算符的结果为 Null。</span><span class="sxs-lookup"><span data-stu-id="d971e-113">If the reference value is null, or is dangling (that is, the target of the reference does not exist), the result of the DEREF operator is null.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d971e-114">示例</span><span class="sxs-lookup"><span data-stu-id="d971e-114">Example</span></span>  

 <span data-ttu-id="d971e-115">下面的 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询使用 DEREF 运算符取消引用一个引用值，并生成该取消引用的结果。</span><span class="sxs-lookup"><span data-stu-id="d971e-115">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the DEREF operator to dereference a reference value and produce the result of that dereference.</span></span> <span data-ttu-id="d971e-116">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="d971e-116">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="d971e-117">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="d971e-117">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="d971e-118">按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。</span><span class="sxs-lookup"><span data-stu-id="d971e-118">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2. <span data-ttu-id="d971e-119">将以下查询作为参数传递给 ExecutePrimitiveTypeQuery 方法：</span><span class="sxs-lookup"><span data-stu-id="d971e-119">Pass the following query as an argument to the ExecutePrimitiveTypeQuery method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#DEREF](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#deref)]  
  
## <a name="see-also"></a><span data-ttu-id="d971e-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="d971e-120">See also</span></span>

- [<span data-ttu-id="d971e-121">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="d971e-121">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="d971e-122">REF</span><span class="sxs-lookup"><span data-stu-id="d971e-122">REF</span></span>](ref-entity-sql.md)
- [<span data-ttu-id="d971e-123">CREATEREF</span><span class="sxs-lookup"><span data-stu-id="d971e-123">CREATEREF</span></span>](createref-entity-sql.md)
- [<span data-ttu-id="d971e-124">KEY</span><span class="sxs-lookup"><span data-stu-id="d971e-124">KEY</span></span>](key-entity-sql.md)
- [<span data-ttu-id="d971e-125">可以为 NULL 的结构化类型</span><span class="sxs-lookup"><span data-stu-id="d971e-125">Nullable Structured Types</span></span>](nullable-structured-types-entity-sql.md)

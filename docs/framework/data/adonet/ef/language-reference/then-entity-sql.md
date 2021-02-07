---
description: '详细了解：然后 (实体 SQL) '
title: THEN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 54222642-23c6-4f61-9861-67caca53ac5f
ms.openlocfilehash: e1f0657cfef3786832f489434fd8fc0342e8687b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673461"
---
# <a name="then-entity-sql"></a><span data-ttu-id="8ca8b-103">THEN (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="8ca8b-103">THEN (Entity SQL)</span></span>

<span data-ttu-id="8ca8b-104">当 WHEN 子句取值为 `true`时的结果。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-104">The result of a WHEN clause when it evaluates to `true`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ca8b-105">语法</span><span class="sxs-lookup"><span data-stu-id="8ca8b-105">Syntax</span></span>  
  
```sql  
WHEN when_expression THEN then_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="8ca8b-106">参数</span><span class="sxs-lookup"><span data-stu-id="8ca8b-106">Arguments</span></span>  

 `when_expression`  
 <span data-ttu-id="8ca8b-107">任何有效的 Boolean 表达式。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-107">Any valid Boolean expression.</span></span>  
  
 `then_expression`  
 <span data-ttu-id="8ca8b-108">任何返回集合的有效查询表达式。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-108">Any valid query expression that returns a collection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8ca8b-109">备注</span><span class="sxs-lookup"><span data-stu-id="8ca8b-109">Remarks</span></span>  

 <span data-ttu-id="8ca8b-110">如果 `when_expression` 取值为 `true`，则结果为对应的 `then-expression`。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-110">If `when_expression` evaluates to the value `true`, the result is the corresponding `then-expression`.</span></span> <span data-ttu-id="8ca8b-111">如果任何 WHEN 条件均未得以满足，将求出 `else-expression` 的值。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-111">If none of the WHEN conditions are satisfied, the `else-expression` is evaluated.</span></span> <span data-ttu-id="8ca8b-112">然而，如果没有 `else-expression`，则结果为空值。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-112">However, if there is no `else-expression`, the result is null.</span></span>  
  
 <span data-ttu-id="8ca8b-113">有关示例，请参阅 [CASE](case-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-113">For an example, see [CASE](case-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8ca8b-114">示例</span><span class="sxs-lookup"><span data-stu-id="8ca8b-114">Example</span></span>  

 <span data-ttu-id="8ca8b-115">以下 Entity SQL 查询使用 CASE 表达式计算一组 `Boolean` 表达式的值。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-115">The following Entity SQL query uses the CASE expression to evaluate a set of `Boolean` expressions.</span></span> <span data-ttu-id="8ca8b-116">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-116">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="8ca8b-117">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="8ca8b-117">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="8ca8b-118">按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。</span><span class="sxs-lookup"><span data-stu-id="8ca8b-118">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2. <span data-ttu-id="8ca8b-119">将以下查询作为参数传递给 `ExecutePrimitiveTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="8ca8b-119">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#CASE_WHEN_THEN_ELSE](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#case_when_then_else)]  
  
## <a name="see-also"></a><span data-ttu-id="8ca8b-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ca8b-120">See also</span></span>

- [<span data-ttu-id="8ca8b-121">CASE</span><span class="sxs-lookup"><span data-stu-id="8ca8b-121">CASE</span></span>](case-entity-sql.md)
- [<span data-ttu-id="8ca8b-122">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="8ca8b-122">Entity SQL Reference</span></span>](entity-sql-reference.md)

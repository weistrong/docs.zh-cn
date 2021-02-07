---
description: '详细了解：在 (实体 SQL) '
title: IN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 51662950-ee01-4857-b7b9-311dd8515966
ms.openlocfilehash: 234ed15430e44d12d4ca7c98fcb4a7bc03d117f9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748591"
---
# <a name="in-entity-sql"></a><span data-ttu-id="3214f-103">IN (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="3214f-103">IN (Entity SQL)</span></span>

<span data-ttu-id="3214f-104">确定某个值是否与某个集合中的任何值匹配。</span><span class="sxs-lookup"><span data-stu-id="3214f-104">Determines whether a value matches any value in a collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3214f-105">语法</span><span class="sxs-lookup"><span data-stu-id="3214f-105">Syntax</span></span>  
  
```sql  
value [ NOT ] IN expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="3214f-106">参数</span><span class="sxs-lookup"><span data-stu-id="3214f-106">Arguments</span></span>  

 `value`  
 <span data-ttu-id="3214f-107">返回匹配值的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="3214f-107">Any valid expression that returns the value to match.</span></span>  
  
 <span data-ttu-id="3214f-108">[ NOT ]</span><span class="sxs-lookup"><span data-stu-id="3214f-108">[ NOT ]</span></span>  
 <span data-ttu-id="3214f-109">指定对 IN 的 `Boolean` 结果取反。</span><span class="sxs-lookup"><span data-stu-id="3214f-109">Specifies that the `Boolean` result of IN be negated.</span></span>  
  
 `expression`  
 <span data-ttu-id="3214f-110">返回集合以测试是否具有匹配的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="3214f-110">Any valid expression that returns the collection to test for a match.</span></span> <span data-ttu-id="3214f-111">所有表达式都必须与 `value`一样属于同一类型或属于公共基类型或派生类型。</span><span class="sxs-lookup"><span data-stu-id="3214f-111">All expressions must be of the same type or of a common base or derived type as `value`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3214f-112">返回值</span><span class="sxs-lookup"><span data-stu-id="3214f-112">Return Value</span></span>  

 <span data-ttu-id="3214f-113">如果在集合中找到此值，则为 `true`；如果值为空或集合为空，则为空；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="3214f-113">`true` if the value is found in the collection; null if the value is null or the collection is null; otherwise, `false`.</span></span> <span data-ttu-id="3214f-114">使用 NOT IN 可对 IN 的结果取反。</span><span class="sxs-lookup"><span data-stu-id="3214f-114">Using NOT IN negates the results of IN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3214f-115">示例</span><span class="sxs-lookup"><span data-stu-id="3214f-115">Example</span></span>  

 <span data-ttu-id="3214f-116">以下 Entity SQL 查询使用 IN 运算符以确定某个值是否与集合中的任何值匹配。</span><span class="sxs-lookup"><span data-stu-id="3214f-116">The following Entity SQL query uses the IN operator to determine whether a value matches any value in a collection.</span></span> <span data-ttu-id="3214f-117">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="3214f-117">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="3214f-118">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="3214f-118">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="3214f-119">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="3214f-119">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="3214f-120">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="3214f-120">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#IN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#in)]  
  
## <a name="see-also"></a><span data-ttu-id="3214f-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="3214f-121">See also</span></span>

- [<span data-ttu-id="3214f-122">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="3214f-122">Entity SQL Reference</span></span>](entity-sql-reference.md)

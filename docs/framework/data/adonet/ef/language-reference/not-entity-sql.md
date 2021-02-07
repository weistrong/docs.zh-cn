---
description: 详细了解：！ (NOT) (Entity SQL)
title: '! (NOT) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: a1447a34-df06-4393-93c3-0612ebd41abc
ms.openlocfilehash: 648cc4ff73769ae280570b2d42934b2001fa5182
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696446"
---
# <a name="-not-entity-sql"></a><span data-ttu-id="ab9d3-105">!</span><span class="sxs-lookup"><span data-stu-id="ab9d3-105">!</span></span> <span data-ttu-id="ab9d3-106">(NOT) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="ab9d3-106">(NOT) (Entity SQL)</span></span>

<span data-ttu-id="ab9d3-107">对 `Boolean` 表达式求反。</span><span class="sxs-lookup"><span data-stu-id="ab9d3-107">Negates a `Boolean` expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab9d3-108">语法</span><span class="sxs-lookup"><span data-stu-id="ab9d3-108">Syntax</span></span>  
  
```sql  
NOT boolean_expression  
-- or  
! boolean_expression  
```
  
## <a name="arguments"></a><span data-ttu-id="ab9d3-109">参数</span><span class="sxs-lookup"><span data-stu-id="ab9d3-109">Arguments</span></span>  

 `boolean_expression`  
 <span data-ttu-id="ab9d3-110">返回 Boolean 的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="ab9d3-110">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ab9d3-111">备注</span><span class="sxs-lookup"><span data-stu-id="ab9d3-111">Remarks</span></span>  

 <span data-ttu-id="ab9d3-112">惊叹号 (!) 与 NOT 运算符具有相同的功能。</span><span class="sxs-lookup"><span data-stu-id="ab9d3-112">The exclamation point (!) has the same functionality as the NOT operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ab9d3-113">示例</span><span class="sxs-lookup"><span data-stu-id="ab9d3-113">Example</span></span>  

 <span data-ttu-id="ab9d3-114">以下 Entity SQL 查询使用 NOT 运算符以对 `Boolean` 表达式求反。</span><span class="sxs-lookup"><span data-stu-id="ab9d3-114">The following Entity SQL query uses the NOT operator to negates a `Boolean` expression.</span></span> <span data-ttu-id="ab9d3-115">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="ab9d3-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="ab9d3-116">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="ab9d3-116">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="ab9d3-117">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="ab9d3-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="ab9d3-118">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="ab9d3-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#NOT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#not)]  
  
## <a name="see-also"></a><span data-ttu-id="ab9d3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab9d3-119">See also</span></span>

- [<span data-ttu-id="ab9d3-120">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="ab9d3-120">Entity SQL Reference</span></span>](entity-sql-reference.md)

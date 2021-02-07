---
description: '了解详细信息：限制 (实体 SQL) '
title: LIMIT (Entity SQL)
ms.date: 03/30/2017
ms.assetid: c22ffede-0a52-44d1-99b9-4a91e651e1b9
ms.openlocfilehash: 873f3fd5ed83d04313aff92bf1f97e07001c3f08
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748201"
---
# <a name="limit-entity-sql"></a><span data-ttu-id="444f2-103">LIMIT (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="444f2-103">LIMIT (Entity SQL)</span></span>

<span data-ttu-id="444f2-104">在 ORDER BY 子句中使用 LIMIT 子子句可执行物理分页。</span><span class="sxs-lookup"><span data-stu-id="444f2-104">Physical paging can be performed by using LIMIT sub-clause in ORDER BY clause.</span></span> <span data-ttu-id="444f2-105">LIMIT 不能脱离 ORDER BY 子句单独使用。</span><span class="sxs-lookup"><span data-stu-id="444f2-105">LIMIT can not be used separately from ORDER BY clause.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="444f2-106">语法</span><span class="sxs-lookup"><span data-stu-id="444f2-106">Syntax</span></span>  
  
```sql  
[ LIMIT n ]  
```  
  
## <a name="arguments"></a><span data-ttu-id="444f2-107">参数</span><span class="sxs-lookup"><span data-stu-id="444f2-107">Arguments</span></span>  

 `n`  
 <span data-ttu-id="444f2-108">将选择的项的数量。</span><span class="sxs-lookup"><span data-stu-id="444f2-108">The number of items that will be selected.</span></span>  
  
 <span data-ttu-id="444f2-109">如果 ORDER BY 子句中存在 LIMIT 表达式子子句，则将根据排序规范对查询排序，并且结果行数将受到 LIMIT 表达式限制。</span><span class="sxs-lookup"><span data-stu-id="444f2-109">If a LIMIT expression sub-clause is present in an ORDER BY clause, the query will be sorted according to the sort specification and the resulting number of rows will be restricted by the LIMIT expression.</span></span> <span data-ttu-id="444f2-110">例如，LIMIT 5 将结果集限制为 5 个实例或行。</span><span class="sxs-lookup"><span data-stu-id="444f2-110">For instance, LIMIT 5 will restrict the result set to 5 instances or rows.</span></span> <span data-ttu-id="444f2-111">LIMIT 的功能与 TOP 相当，区别之处是 LIMIT 要求 ORDER BY 子句存在。</span><span class="sxs-lookup"><span data-stu-id="444f2-111">LIMIT is functionally equivalent to TOP with the exception that LIMIT requires ORDER BY clause to be present.</span></span> <span data-ttu-id="444f2-112">SKIP 和 LIMIT 可独立与 ORDER BY 子句一起使用。</span><span class="sxs-lookup"><span data-stu-id="444f2-112">SKIP and LIMIT can be used independently along with ORDER BY clause.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="444f2-113">如果 TOP 修饰符和 SKIP 子子句出现在同一个查询表达式中，Entity SQL 查询将被视为无效。</span><span class="sxs-lookup"><span data-stu-id="444f2-113">An Entity Sql query will be considered invalid if TOP modifier and SKIP sub-clause is present in the same query expression.</span></span> <span data-ttu-id="444f2-114">应重写查询，将 TOP 表达式更改为 LIMIT 表达式。</span><span class="sxs-lookup"><span data-stu-id="444f2-114">The query should be rewritten by changing TOP expression to LIMIT expression.</span></span>  
  
## <a name="example"></a><span data-ttu-id="444f2-115">示例</span><span class="sxs-lookup"><span data-stu-id="444f2-115">Example</span></span>  

 <span data-ttu-id="444f2-116">下面的 Entity SQL 查询将 LIMIT 和 ORDER BY 运算符结合使用来指定用于 SELECT 语句所返回的对象的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="444f2-116">The following Entity SQL query uses the ORDER BY operator with LIMIT to specify the sort order used on objects returned in a SELECT statement.</span></span> <span data-ttu-id="444f2-117">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="444f2-117">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="444f2-118">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="444f2-118">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="444f2-119">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="444f2-119">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="444f2-120">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="444f2-120">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#LIMIT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#limit)]  
  
## <a name="see-also"></a><span data-ttu-id="444f2-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="444f2-121">See also</span></span>

- [<span data-ttu-id="444f2-122">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="444f2-122">ORDER BY</span></span>](order-by-entity-sql.md)
- <span data-ttu-id="444f2-123">[如何：按页查看查询结果](/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="444f2-123">[How to: Page Through Query Results](/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))</span></span>
- [<span data-ttu-id="444f2-124">分页</span><span class="sxs-lookup"><span data-stu-id="444f2-124">Paging</span></span>](paging-entity-sql.md)
- [<span data-ttu-id="444f2-125">TOP</span><span class="sxs-lookup"><span data-stu-id="444f2-125">TOP</span></span>](top-entity-sql.md)

---
description: '了解详细信息：拥有 (实体 SQL) '
title: HAVING (Entity SQL)
ms.date: 03/30/2017
ms.assetid: b5d52d97-8372-4335-beac-2d0b79dc3707
ms.openlocfilehash: 70ace20d67e93aa051873d2b32a49f560902e63d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696875"
---
# <a name="having-entity-sql"></a><span data-ttu-id="3efa6-103">HAVING (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="3efa6-103">HAVING (Entity SQL)</span></span>

<span data-ttu-id="3efa6-104">指定组或聚合的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="3efa6-104">Specifies a search condition for a group or an aggregate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3efa6-105">语法</span><span class="sxs-lookup"><span data-stu-id="3efa6-105">Syntax</span></span>  
  
```sql  
[ HAVING search_condition ]  
```  
  
## <a name="arguments"></a><span data-ttu-id="3efa6-106">参数</span><span class="sxs-lookup"><span data-stu-id="3efa6-106">Arguments</span></span>  

 `search_condition`  
 <span data-ttu-id="3efa6-107">指定组或聚合应满足的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="3efa6-107">Specifies the search condition for the group or the aggregate to meet.</span></span> <span data-ttu-id="3efa6-108">当 HAVING 与 GROUP BY ALL 一起使用时，HAVING 子句优先于 ALL。</span><span class="sxs-lookup"><span data-stu-id="3efa6-108">When HAVING is used with GROUP BY ALL, the HAVING clause overrides ALL.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3efa6-109">备注</span><span class="sxs-lookup"><span data-stu-id="3efa6-109">Remarks</span></span>  

 <span data-ttu-id="3efa6-110">HAVING 子句用于对分组结果指定附加筛选条件。</span><span class="sxs-lookup"><span data-stu-id="3efa6-110">The HAVING clause is used to specify an additional filtering condition on the result of a grouping.</span></span> <span data-ttu-id="3efa6-111">如果在查询表达式中未指定 GROUP BY 子句，则将使用隐式单集组。</span><span class="sxs-lookup"><span data-stu-id="3efa6-111">If no GROUP BY clause is specified in the query expression, an implicit single-set group is assumed.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3efa6-112">HAVING 只能与 [SELECT](select-entity-sql.md) 语句一起使用。</span><span class="sxs-lookup"><span data-stu-id="3efa6-112">HAVING can be used only with the [SELECT](select-entity-sql.md) statement.</span></span> <span data-ttu-id="3efa6-113">如果不使用 [GROUP BY](group-by-entity-sql.md) ，则其行为与 WHERE 子句类似。</span><span class="sxs-lookup"><span data-stu-id="3efa6-113">When [GROUP BY](group-by-entity-sql.md) is not used, HAVING behaves like a WHERE clause.</span></span>  
  
<span data-ttu-id="3efa6-114">HAVING 子句与 WHERE 子句的工作方式类似，只是它应用在 GROUP BY 操作之后。</span><span class="sxs-lookup"><span data-stu-id="3efa6-114">The HAVING clause works like the WHERE clause except that it is applied after the GROUP BY operation.</span></span> <span data-ttu-id="3efa6-115">这意味着 HAVING 子句只能引用分组别名和聚合，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="3efa6-115">This means that the HAVING clause can only make references to grouping aliases and aggregates, as illustrated in the following example:</span></span>
  
```sql  
SELECT Name, SUM(o.Price * o.Quantity) AS Total FROM orderLines AS o GROUP BY o.Product AS Name  
HAVING SUM(o.Quantity) > 1  
```  
  
 <span data-ttu-id="3efa6-116">上例将组限定为只包含多个产品的组。</span><span class="sxs-lookup"><span data-stu-id="3efa6-116">The previous restricts the groups to only those that include more than one product.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3efa6-117">示例</span><span class="sxs-lookup"><span data-stu-id="3efa6-117">Example</span></span>  

 <span data-ttu-id="3efa6-118">下面的 Entity SQL 查询使用 HAVING 和 GROUP BY 运算符指定组或聚合的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="3efa6-118">The following Entity SQL query uses the HAVING and GROUP BY operators to specify a search condition for a group or an aggregate.</span></span> <span data-ttu-id="3efa6-119">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="3efa6-119">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="3efa6-120">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="3efa6-120">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="3efa6-121">按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。</span><span class="sxs-lookup"><span data-stu-id="3efa6-121">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2. <span data-ttu-id="3efa6-122">将以下查询作为参数传递给 `ExecutePrimitiveTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="3efa6-122">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#HAVING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#having)]  
  
## <a name="see-also"></a><span data-ttu-id="3efa6-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="3efa6-123">See also</span></span>

- [<span data-ttu-id="3efa6-124">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="3efa6-124">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="3efa6-125">查询表达式</span><span class="sxs-lookup"><span data-stu-id="3efa6-125">Query Expressions</span></span>](query-expressions-entity-sql.md)

---
description: '了解详细信息： GROUPPARTITION (实体 SQL) '
title: GROUPPARTITION (Entity SQL)
ms.date: 03/30/2017
ms.assetid: d0482e9b-086c-451c-9dfa-ccb024a9efb6
ms.openlocfilehash: 18fdb655f62f54d59c03c0a34f6f77c5ca26729e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696901"
---
# <a name="grouppartition-entity-sql"></a><span data-ttu-id="79585-103">GROUPPARTITION (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="79585-103">GROUPPARTITION (Entity SQL)</span></span>

<span data-ttu-id="79585-104">返回从聚合与之相关的当前组分区提取的参数值集合。</span><span class="sxs-lookup"><span data-stu-id="79585-104">Returns a collection of argument values that are projected off the current group partition to which the aggregate is related.</span></span> <span data-ttu-id="79585-105">`GroupPartition` 聚合是基于组的聚合，没有基于集合的形式。</span><span class="sxs-lookup"><span data-stu-id="79585-105">The `GroupPartition` aggregate is a group-based aggregate and has no collection-based form.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79585-106">语法</span><span class="sxs-lookup"><span data-stu-id="79585-106">Syntax</span></span>  
  
```sql  
GROUPPARTITION( [ALL|DISTINCT] expression )  
```  
  
## <a name="arguments"></a><span data-ttu-id="79585-107">参数</span><span class="sxs-lookup"><span data-stu-id="79585-107">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="79585-108">任何 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 表达式。</span><span class="sxs-lookup"><span data-stu-id="79585-108">Any [!INCLUDE[esql](../../../../../../includes/esql-md.md)] expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79585-109">备注</span><span class="sxs-lookup"><span data-stu-id="79585-109">Remarks</span></span>  

 <span data-ttu-id="79585-110">以下查询生成产品列表以及每个产品的订单行数量的集合。</span><span class="sxs-lookup"><span data-stu-id="79585-110">The following query produces a list of products and a collection of order line quantities per each product:</span></span>  
  
```sql  
SELECT p, GroupPartition(ol.Quantity) FROM LOB.OrderLines AS ol
  GROUP BY ol.Product AS p
```  
  
 <span data-ttu-id="79585-111">以下两个查询在语义上是相同的：</span><span class="sxs-lookup"><span data-stu-id="79585-111">The following two queries are semantically equal:</span></span>  
  
```sql  
SELECT p, Sum(GroupPartition(ol.Quantity)) FROM LOB.OrderLines AS ol
  GROUP BY ol.Product AS p
SELET p, Sum(ol.Quantity) FROM LOB.OrderLines AS ol
  group by ol.Product as p  
```  
  
 <span data-ttu-id="79585-112">`GROUPPARTITION` 运算符可以与用户定义的聚合函数结合使用。</span><span class="sxs-lookup"><span data-stu-id="79585-112">The `GROUPPARTITION` operator can be used in conjunction with user-defined aggregate functions.</span></span>  
  
<span data-ttu-id="79585-113">`GROUPPARTITION` 是一个特殊的聚合运算符，它保留对于分组的输入集的引用。</span><span class="sxs-lookup"><span data-stu-id="79585-113">`GROUPPARTITION` is a special aggregate operator that holds a reference to the grouped input set.</span></span> <span data-ttu-id="79585-114">此引用可以用在 GROUP BY 处于作用域内的查询中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="79585-114">This reference can be used anywhere in the query where GROUP BY is in scope.</span></span> <span data-ttu-id="79585-115">例如：</span><span class="sxs-lookup"><span data-stu-id="79585-115">For example:</span></span>
  
```sql  
SELECT p, GroupPartition(ol.Quantity) FROM LOB.OrderLines AS ol GROUP BY ol.Product AS p
```  
  
 <span data-ttu-id="79585-116">对于常规 `GROUP BY` ，将隐藏分组的结果。</span><span class="sxs-lookup"><span data-stu-id="79585-116">With a regular `GROUP BY`, the results of the grouping are hidden.</span></span> <span data-ttu-id="79585-117">您只能在聚合函数中使用结果。</span><span class="sxs-lookup"><span data-stu-id="79585-117">You can only use the results in an aggregate function.</span></span> <span data-ttu-id="79585-118">为了能够看到分组的结果，必须使用子查询使分组的结果与输入集相关。</span><span class="sxs-lookup"><span data-stu-id="79585-118">In order to see the results of the grouping, you have to correlate the results of the grouping and the input set by using a subquery.</span></span> <span data-ttu-id="79585-119">下面两个查询是等效的：</span><span class="sxs-lookup"><span data-stu-id="79585-119">The following two queries are equivalent:</span></span>  
  
```sql  
SELET p, (SELECT q FROM GroupPartition(ol.Quantity) AS q) FROM LOB.OrderLines AS ol GROUP BY ol.Product AS p
SELECT p, (SELECT ol.Quantity AS q FROM LOB.OrderLines AS ol2 WHERE ol2.Product = p) FROM LOB.OrderLines AS ol GROUP BY ol.Product AS p
```  
  
 <span data-ttu-id="79585-120">如示例中所示，通过 GROUPPARTITION 聚合运算符，可以在分组后更轻松地获得对输入集的引用。</span><span class="sxs-lookup"><span data-stu-id="79585-120">As seen from the example, the GROUPPARTITION aggregate operator makes it easier to get a reference to the input set after the grouping.</span></span>  
  
 <span data-ttu-id="79585-121">当您使用 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 参数时，GROUPPARTITION 运算符可以在运算符输入中指定任何 `expression` 表达式。</span><span class="sxs-lookup"><span data-stu-id="79585-121">The GROUPPARTITION operator can specify any [!INCLUDE[esql](../../../../../../includes/esql-md.md)] expression in the operator input when you use the `expression` parameter.</span></span>  
  
 <span data-ttu-id="79585-122">例如，下面针对组分区的所有输入表达式都是有效的：</span><span class="sxs-lookup"><span data-stu-id="79585-122">For instance all of the following input expressions to the group partition are valid:</span></span>  
  
```sql  
SELECT groupkey, GroupPartition(b) FROM {1,2,3} AS a INNER JOIN {4,5,6} AS b ON true GROUP BY a AS groupkey
SELECT groupkey, GroupPartition(1) FROM {1,2,3} AS a INNER JOIN {4,5,6} AS b ON true GROUP BY a AS groupkey
SELECT groupkey, GroupPartition(a + b) FROM {1,2,3} AS a INNER JOIN {4,5,6} AS b ON true GROUP BY a AS groupkey
SELECT groupkey, GroupPartition({a + b}) FROM {1,2,3} AS a INNER JOIN {4,5,6} AS b ON true GROUP BY a AS groupkey  
SELECT groupkey, GroupPartition({42}) FROM {1,2,3} AS a INNER JOIN {4,5,6} AS b ON true GROUP BY a AS groupkey  
SELECT groupkey, GroupPartition(b > a) FROM {1,2,3} AS a INNER JOIN {4,5,6} AS b ON true GROUP BY a AS groupkey  
```  
  
## <a name="example"></a><span data-ttu-id="79585-123">示例</span><span class="sxs-lookup"><span data-stu-id="79585-123">Example</span></span>  

 <span data-ttu-id="79585-124">下面的示例演示如何将 GROUPPARTITION 子句与 GROUP BY 子句一起使用。</span><span class="sxs-lookup"><span data-stu-id="79585-124">The following example shows how to use the GROUPPARTITION clause with the GROUP BY clause.</span></span> <span data-ttu-id="79585-125">GROUP BY 子句按照 `SalesOrderHeader` 实体的 `Contact`对这些实体进行分组。</span><span class="sxs-lookup"><span data-stu-id="79585-125">The GROUP BY clause groups `SalesOrderHeader` entities by their `Contact`.</span></span> <span data-ttu-id="79585-126">然后，GROUPPARTITION 子句投影每个组的 `TotalDue` 属性，而生成一个十进制值集合。</span><span class="sxs-lookup"><span data-stu-id="79585-126">The GROUPPARTITION clause then projects the `TotalDue` property for each group, resulting in a collection of decimals.</span></span>  
  
 [!code-sql[DP EntityServices Concepts#Collection_GroupPartition](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#collection_grouppartition)]

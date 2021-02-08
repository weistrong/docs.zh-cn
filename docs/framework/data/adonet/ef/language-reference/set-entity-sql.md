---
description: '了解详细信息：设置 (实体 SQL) '
title: SET (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 28b4deac-c7e4-4f09-b428-4d352ef2dc94
ms.openlocfilehash: 80be5b76e654c39776d97413c4ece5a8f3df8d2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768020"
---
# <a name="set-entity-sql"></a><span data-ttu-id="25d22-103">SET (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="25d22-103">SET (Entity SQL)</span></span>

<span data-ttu-id="25d22-104">SET 表达式用于通过生成一个新集合（其中移除了所有重复元素）将对象集合转换为一个集。</span><span class="sxs-lookup"><span data-stu-id="25d22-104">The SET expression is used to convert a collection of objects into a set by yielding a new collection with all duplicate elements removed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25d22-105">语法</span><span class="sxs-lookup"><span data-stu-id="25d22-105">Syntax</span></span>  
  
```sql  
SET ( expression )  
```  
  
## <a name="arguments"></a><span data-ttu-id="25d22-106">参数</span><span class="sxs-lookup"><span data-stu-id="25d22-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="25d22-107">任何返回集合的有效查询表达式。</span><span class="sxs-lookup"><span data-stu-id="25d22-107">Any valid query expression that returns a collection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="25d22-108">备注</span><span class="sxs-lookup"><span data-stu-id="25d22-108">Remarks</span></span>  

 <span data-ttu-id="25d22-109">SET 表达式 `SET(c)` 在逻辑上等效于以下 select 语句：</span><span class="sxs-lookup"><span data-stu-id="25d22-109">The set expression `SET(c)` is logically equivalent to the following select statement:</span></span>  
  
```sql  
SELECT VALUE DISTINCT c FROM c  
```  
  
 <span data-ttu-id="25d22-110">`SET` 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。</span><span class="sxs-lookup"><span data-stu-id="25d22-110">`SET` is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="25d22-111">所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。</span><span class="sxs-lookup"><span data-stu-id="25d22-111">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="25d22-112">有关集运算符 [的优先级信息，请参阅](except-entity-sql.md) [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="25d22-112">See [EXCEPT](except-entity-sql.md) for precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="25d22-113">示例</span><span class="sxs-lookup"><span data-stu-id="25d22-113">Example</span></span>  

 <span data-ttu-id="25d22-114">以下 Entity SQL 查询使用 SET 表达式将一个对象集合转换为一个集。</span><span class="sxs-lookup"><span data-stu-id="25d22-114">The following Entity SQL query uses the SET expression to convert a collection of objects into a set.</span></span> <span data-ttu-id="25d22-115">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="25d22-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="25d22-116">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="25d22-116">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="25d22-117">按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。</span><span class="sxs-lookup"><span data-stu-id="25d22-117">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2. <span data-ttu-id="25d22-118">将以下查询作为参数传递给 `ExecutePrimitiveTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="25d22-118">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#SET](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#set)]  
  
## <a name="see-also"></a><span data-ttu-id="25d22-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="25d22-119">See also</span></span>

- [<span data-ttu-id="25d22-120">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="25d22-120">Entity SQL Reference</span></span>](entity-sql-reference.md)

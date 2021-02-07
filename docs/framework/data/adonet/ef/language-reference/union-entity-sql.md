---
description: '详细了解：联合 (实体 SQL) '
title: UNION (Entity SQL)
ms.date: 03/30/2017
ms.assetid: df98a4db-b00d-4c8b-bd74-0d285f27e1df
ms.openlocfilehash: f02b3d76d8c21848b7a1b7ef5e7bbf749aea5c0f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673305"
---
# <a name="union-entity-sql"></a><span data-ttu-id="df494-103">UNION (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="df494-103">UNION (Entity SQL)</span></span>

<span data-ttu-id="df494-104">将两个或更多查询的结果组合成单个集合。</span><span class="sxs-lookup"><span data-stu-id="df494-104">Combines the results of two or more queries into a single collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df494-105">语法</span><span class="sxs-lookup"><span data-stu-id="df494-105">Syntax</span></span>  
  
```sql  
expression  
UNION [ ALL ]  
expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="df494-106">参数</span><span class="sxs-lookup"><span data-stu-id="df494-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="df494-107">返回一个集合以与该集合进行组合的任何有效查询表达式。所有表达式都必须与 `expression`一样属于同一类型或属于公共基类型或派生类型。</span><span class="sxs-lookup"><span data-stu-id="df494-107">Any valid query expression that returns a collection to combine with the collection All expressions must be of the same type or of a common base or derived type as `expression`.</span></span>  
  
 <span data-ttu-id="df494-108">UNION</span><span class="sxs-lookup"><span data-stu-id="df494-108">UNION</span></span>  
 <span data-ttu-id="df494-109">指定组合多个集合并将其作为单个集合返回。</span><span class="sxs-lookup"><span data-stu-id="df494-109">Specifies that multiple collections are to be combined and returned as a single collection.</span></span>  
  
 <span data-ttu-id="df494-110">ALL</span><span class="sxs-lookup"><span data-stu-id="df494-110">ALL</span></span>  
 <span data-ttu-id="df494-111">指定组合多个集合并将其作为单个集合返回（包括重复项）。</span><span class="sxs-lookup"><span data-stu-id="df494-111">Specifies that multiple collections are to be combined and returned as a single collection, including duplicates.</span></span> <span data-ttu-id="df494-112">如果未指定，则从结果集合中删除重复项。</span><span class="sxs-lookup"><span data-stu-id="df494-112">If not specified, duplicates are removed from the result collection.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="df494-113">返回值</span><span class="sxs-lookup"><span data-stu-id="df494-113">Return Value</span></span>  

 <span data-ttu-id="df494-114">与 `expression`具有相同类型或属于公共基类型或派生类型的一个集合。</span><span class="sxs-lookup"><span data-stu-id="df494-114">A collection of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="df494-115">备注</span><span class="sxs-lookup"><span data-stu-id="df494-115">Remarks</span></span>  

 <span data-ttu-id="df494-116">UNION 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。</span><span class="sxs-lookup"><span data-stu-id="df494-116">UNION is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="df494-117">所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。</span><span class="sxs-lookup"><span data-stu-id="df494-117">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="df494-118">有关集运算符的优先级信息 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ，请参阅 [EXCEPT](except-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="df494-118">For precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators, see [EXCEPT](except-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="df494-119">示例</span><span class="sxs-lookup"><span data-stu-id="df494-119">Example</span></span>  

 <span data-ttu-id="df494-120">以下 Entity SQL 查询使用 UNION ALL 运算符以将两个查询的结果组合成单个集合。</span><span class="sxs-lookup"><span data-stu-id="df494-120">The following Entity SQL query uses the UNION ALL operator to combine the results of two queries into a single collection.</span></span> <span data-ttu-id="df494-121">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="df494-121">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="df494-122">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="df494-122">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="df494-123">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="df494-123">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="df494-124">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="df494-124">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#UNION](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#union)]  
  
## <a name="see-also"></a><span data-ttu-id="df494-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="df494-125">See also</span></span>

- [<span data-ttu-id="df494-126">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="df494-126">Entity SQL Reference</span></span>](entity-sql-reference.md)

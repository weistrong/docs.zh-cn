---
description: '了解有关以下内容的详细信息： (实体 SQL 除外) '
title: EXCEPT (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 69cc23e5-3f8f-4b49-b20e-2f84ff11c80d
ms.openlocfilehash: fd66d8dc6e22a73afbfd27e6eb1fd6c8bb9d3475
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786389"
---
# <a name="except-entity-sql"></a><span data-ttu-id="6eb6e-103">EXCEPT (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="6eb6e-103">EXCEPT (Entity SQL)</span></span>

<span data-ttu-id="6eb6e-104">返回由 EXCEPT 操作数左侧的查询表达式返回而不由 EXCEPT 操作数右侧的查询表达式返回的任何非重复值的集合。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-104">Returns a collection of any distinct values from the query expression to the left of the EXCEPT operand that are not also returned from the query expression to the right of the EXCEPT operand.</span></span> <span data-ttu-id="6eb6e-105">所有表达式都必须与 `expression`一样属于同一类型或属于公共基类型或派生类型。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-105">All expressions must be of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6eb6e-106">语法</span><span class="sxs-lookup"><span data-stu-id="6eb6e-106">Syntax</span></span>  
  
```sql  
expression EXCEPT expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="6eb6e-107">参数</span><span class="sxs-lookup"><span data-stu-id="6eb6e-107">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="6eb6e-108">返回一个集合以与从其他查询表达式返回的集合进行比较的任何有效查询表达式。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-108">Any valid query expression that returns a collection to compare with the collection returned from another query expression.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6eb6e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="6eb6e-109">Return Value</span></span>  

 <span data-ttu-id="6eb6e-110">与 `expression`具有相同类型或属于公共基类型或派生类型的一个集合。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-110">A collection of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6eb6e-111">备注</span><span class="sxs-lookup"><span data-stu-id="6eb6e-111">Remarks</span></span>  

 <span data-ttu-id="6eb6e-112">EXCEPT 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-112">EXCEPT is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="6eb6e-113">所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-113">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="6eb6e-114">下表显示 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符的优先级。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-114">The following table shows the precedence of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span>  
  
|<span data-ttu-id="6eb6e-115">优先级</span><span class="sxs-lookup"><span data-stu-id="6eb6e-115">Precedence</span></span>|<span data-ttu-id="6eb6e-116">运算符</span><span class="sxs-lookup"><span data-stu-id="6eb6e-116">Operators</span></span>|  
|----------------|---------------|  
|<span data-ttu-id="6eb6e-117">最高</span><span class="sxs-lookup"><span data-stu-id="6eb6e-117">Highest</span></span>|<span data-ttu-id="6eb6e-118">INTERSECT</span><span class="sxs-lookup"><span data-stu-id="6eb6e-118">INTERSECT</span></span>|  
||<span data-ttu-id="6eb6e-119">UNION</span><span class="sxs-lookup"><span data-stu-id="6eb6e-119">UNION</span></span><br /><br /> <span data-ttu-id="6eb6e-120">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="6eb6e-120">UNION ALL</span></span>|  
||<span data-ttu-id="6eb6e-121">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="6eb6e-121">EXCEPT</span></span>|  
|<span data-ttu-id="6eb6e-122">最低</span><span class="sxs-lookup"><span data-stu-id="6eb6e-122">Lowest</span></span>|<span data-ttu-id="6eb6e-123">EXISTS</span><span class="sxs-lookup"><span data-stu-id="6eb6e-123">EXISTS</span></span><br /><br /> <span data-ttu-id="6eb6e-124">OVERLAPS</span><span class="sxs-lookup"><span data-stu-id="6eb6e-124">OVERLAPS</span></span><br /><br /> <span data-ttu-id="6eb6e-125">FLATTEN</span><span class="sxs-lookup"><span data-stu-id="6eb6e-125">FLATTEN</span></span><br /><br /> <span data-ttu-id="6eb6e-126">SET</span><span class="sxs-lookup"><span data-stu-id="6eb6e-126">SET</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6eb6e-127">示例</span><span class="sxs-lookup"><span data-stu-id="6eb6e-127">Example</span></span>  

 <span data-ttu-id="6eb6e-128">以下 Entity SQL 查询使用 EXCEPT 运算符以返回从两个查询表达式返回的任何非重复值的集合。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-128">The following Entity SQL query uses the EXCEPT operator to return a collection of any distinct values from two query expressions.</span></span> <span data-ttu-id="6eb6e-129">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-129">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="6eb6e-130">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="6eb6e-130">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="6eb6e-131">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="6eb6e-131">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="6eb6e-132">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="6eb6e-132">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#EXCEPT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#except)]  
  
## <a name="see-also"></a><span data-ttu-id="6eb6e-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="6eb6e-133">See also</span></span>

- [<span data-ttu-id="6eb6e-134">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="6eb6e-134">Entity SQL Reference</span></span>](entity-sql-reference.md)

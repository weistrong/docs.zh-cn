---
description: '了解详细信息：存在 (实体 SQL) '
title: EXISTS (Entity SQL)
ms.date: 03/30/2017
ms.assetid: d28ead43-4afb-4bdc-af64-efd2e05005d7
ms.openlocfilehash: c6c5b86616d63b9cc3389365a96c382101463732
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786376"
---
# <a name="exists-entity-sql"></a><span data-ttu-id="4e455-103">EXISTS (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="4e455-103">EXISTS (Entity SQL)</span></span>

<span data-ttu-id="4e455-104">确定集合是否为空。</span><span class="sxs-lookup"><span data-stu-id="4e455-104">Determines if a collection is empty.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e455-105">语法</span><span class="sxs-lookup"><span data-stu-id="4e455-105">Syntax</span></span>  
  
```sql  
[NOT] EXISTS ( expression )  
```  
  
## <a name="arguments"></a><span data-ttu-id="4e455-106">参数</span><span class="sxs-lookup"><span data-stu-id="4e455-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="4e455-107">返回集合的任何有效的表达式。</span><span class="sxs-lookup"><span data-stu-id="4e455-107">Any valid expression that returns a collection.</span></span>  
  
 <span data-ttu-id="4e455-108">NOT</span><span class="sxs-lookup"><span data-stu-id="4e455-108">NOT</span></span>  
 <span data-ttu-id="4e455-109">指定对 EXISTS 的结果取反。</span><span class="sxs-lookup"><span data-stu-id="4e455-109">Specifies that the result of EXISTS be negated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4e455-110">返回值</span><span class="sxs-lookup"><span data-stu-id="4e455-110">Return Value</span></span>  

 <span data-ttu-id="4e455-111">如果集合不为空，则为 `true`；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="4e455-111">`true` if the collection is not empty; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4e455-112">备注</span><span class="sxs-lookup"><span data-stu-id="4e455-112">Remarks</span></span>  

 <span data-ttu-id="4e455-113">EXISTS 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。</span><span class="sxs-lookup"><span data-stu-id="4e455-113">EXISTS is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="4e455-114">所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。</span><span class="sxs-lookup"><span data-stu-id="4e455-114">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="4e455-115">有关集运算符的优先级信息 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ，请参阅 [EXCEPT](except-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="4e455-115">For precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators, see [EXCEPT](except-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="4e455-116">示例</span><span class="sxs-lookup"><span data-stu-id="4e455-116">Example</span></span>  

 <span data-ttu-id="4e455-117">以下 Entity SQL 查询使用 EXISTS 运算符以确定集合是否为空。</span><span class="sxs-lookup"><span data-stu-id="4e455-117">The following Entity SQL query uses the EXISTS operator to determine whether the collection is empty.</span></span> <span data-ttu-id="4e455-118">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="4e455-118">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="4e455-119">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="4e455-119">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="4e455-120">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="4e455-120">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="4e455-121">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="4e455-121">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#EXISTS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#exists)]  
  
## <a name="see-also"></a><span data-ttu-id="4e455-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="4e455-122">See also</span></span>

- [<span data-ttu-id="4e455-123">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="4e455-123">Entity SQL Reference</span></span>](entity-sql-reference.md)

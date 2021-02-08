---
description: '了解详细信息： (实体 SQL 重叠) '
title: OVERLAPS (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
ms.openlocfilehash: dd2f4a0925c57edcc3dd2d1264d00921b092525a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791902"
---
# <a name="overlaps-entity-sql"></a><span data-ttu-id="fec3a-103">OVERLAPS (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="fec3a-103">OVERLAPS (Entity SQL)</span></span>

<span data-ttu-id="fec3a-104">确定两个集合是否具有公共元素。</span><span class="sxs-lookup"><span data-stu-id="fec3a-104">Determines whether two collections have common elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fec3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="fec3a-105">Syntax</span></span>  
  
```sql  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="fec3a-106">参数</span><span class="sxs-lookup"><span data-stu-id="fec3a-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="fec3a-107">返回一个集合以与从其他查询表达式返回的集合进行比较的任何有效查询表达式。</span><span class="sxs-lookup"><span data-stu-id="fec3a-107">Any valid query expression that returns a collection to compare with the collection returned from another query expression.</span></span> <span data-ttu-id="fec3a-108">所有表达式都必须与 `expression`一样属于同一类型或属于公共基类型或派生类型。</span><span class="sxs-lookup"><span data-stu-id="fec3a-108">All expressions must be of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fec3a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="fec3a-109">Return Value</span></span>  

 <span data-ttu-id="fec3a-110">如果两个集合具有公共元素，则为`true` ；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="fec3a-110">`true` if the two collections have common elements; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fec3a-111">备注</span><span class="sxs-lookup"><span data-stu-id="fec3a-111">Remarks</span></span>  

 <span data-ttu-id="fec3a-112">重叠提供的功能等效于以下形式：</span><span class="sxs-lookup"><span data-stu-id="fec3a-112">OVERLAPS provides functionally equivalent to the following:</span></span>  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 <span data-ttu-id="fec3a-113">OVERLAPS 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。</span><span class="sxs-lookup"><span data-stu-id="fec3a-113">OVERLAPS is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="fec3a-114">所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。</span><span class="sxs-lookup"><span data-stu-id="fec3a-114">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="fec3a-115">有关集运算符的优先级信息 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ，请参阅 [EXCEPT](except-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="fec3a-115">For precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators, see [EXCEPT](except-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="fec3a-116">示例</span><span class="sxs-lookup"><span data-stu-id="fec3a-116">Example</span></span>  

 <span data-ttu-id="fec3a-117">以下 Entity SQL 查询使用 OVERLAPS 运算符以确定两个集合是否具有公共值。</span><span class="sxs-lookup"><span data-stu-id="fec3a-117">The following Entity SQL query uses the OVERLAPS operator to determines whether two collections have a common value.</span></span> <span data-ttu-id="fec3a-118">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="fec3a-118">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="fec3a-119">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="fec3a-119">To compile and run this, follow these steps:</span></span>  
  
1. <span data-ttu-id="fec3a-120">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="fec3a-120">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="fec3a-121">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="fec3a-121">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#OVERLAPS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#overlaps)]  
  
## <a name="see-also"></a><span data-ttu-id="fec3a-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fec3a-122">See also</span></span>

- [<span data-ttu-id="fec3a-123">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="fec3a-123">Entity SQL Reference</span></span>](entity-sql-reference.md)

---
description: '了解详细信息： (实体 SQL) '
title: WHERE (Entity SQL)
ms.date: 03/30/2017
ms.assetid: a8e1061e-0028-4a6f-8f19-b9f48e96c4b8
ms.openlocfilehash: e094a93927f6ac77aef772654f1d8d4fcf999cbd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712865"
---
# <a name="where-entity-sql"></a><span data-ttu-id="0e985-103">WHERE (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="0e985-103">WHERE (Entity SQL)</span></span>

<span data-ttu-id="0e985-104">WHERE 子句直接应用于 [from](from-entity-sql.md) 子句之后。</span><span class="sxs-lookup"><span data-stu-id="0e985-104">The WHERE clause is applied directly after the [FROM](from-entity-sql.md) clause.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e985-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e985-105">Syntax</span></span>  
  
```sql  
[ WHERE expression ]  
```  
  
## <a name="arguments"></a><span data-ttu-id="0e985-106">参数</span><span class="sxs-lookup"><span data-stu-id="0e985-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="0e985-107">Boolean 类型。</span><span class="sxs-lookup"><span data-stu-id="0e985-107">A Boolean type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0e985-108">备注</span><span class="sxs-lookup"><span data-stu-id="0e985-108">Remarks</span></span>  

 <span data-ttu-id="0e985-109">WHERE 子句具有与 Transact-sql 所述相同的语义。</span><span class="sxs-lookup"><span data-stu-id="0e985-109">The WHERE clause has the same semantics as described for Transact-SQL.</span></span> <span data-ttu-id="0e985-110">它将源集合的元素限定为传递条件的元素，以此限制查询表达式所生成的对象。</span><span class="sxs-lookup"><span data-stu-id="0e985-110">It restricts the objects produced by the query expression by limiting the elements of the source collections to those that pass the condition.</span></span>  
  
```sql  
select c from cs as c where e  
```  
  
 <span data-ttu-id="0e985-111">表达式 `e` 必须为 Boolean 类型。</span><span class="sxs-lookup"><span data-stu-id="0e985-111">The expression `e` must have the type Boolean.</span></span>  
  
 <span data-ttu-id="0e985-112">WHERE 子句直接应用在 FROM 子句之后，任何分组、排序或投影操作之前。</span><span class="sxs-lookup"><span data-stu-id="0e985-112">The WHERE clause is applied directly after the FROM clause and before any grouping, ordering, or projection takes place.</span></span> <span data-ttu-id="0e985-113">FROM 子句中定义的所有元素名称对 WHERE 子句的表达式都是可见的。</span><span class="sxs-lookup"><span data-stu-id="0e985-113">All element names defined in the FROM clause are visible to the expression of the WHERE clause.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e985-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="0e985-114">See also</span></span>

- [<span data-ttu-id="0e985-115">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="0e985-115">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="0e985-116">查询表达式</span><span class="sxs-lookup"><span data-stu-id="0e985-116">Query Expressions</span></span>](query-expressions-entity-sql.md)

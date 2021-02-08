---
description: '详细了解： = (等于)  (实体 SQL) '
title: =（等于）(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 948eb588-7080-4046-bb48-633b007393bf
ms.openlocfilehash: 500c3fdde2377b3b5160436f23d051c2bcd0ee62
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786402"
---
# <a name="-equals-entity-sql"></a><span data-ttu-id="a8bf3-103">=（等于）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="a8bf3-103">= (Equals) (Entity SQL)</span></span>

<span data-ttu-id="a8bf3-104">比较两个表达式是否相等。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-104">Compares the equality of two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8bf3-105">语法</span><span class="sxs-lookup"><span data-stu-id="a8bf3-105">Syntax</span></span>  
  
```sql  
expression = expression  
-- or
expression == expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="a8bf3-106">参数</span><span class="sxs-lookup"><span data-stu-id="a8bf3-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="a8bf3-107">任何有效的表达式。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-107">Any valid expression.</span></span> <span data-ttu-id="a8bf3-108">两个表达式都必须包含可隐式转换的数据类型。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-108">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="a8bf3-109">结果类型</span><span class="sxs-lookup"><span data-stu-id="a8bf3-109">Result Types</span></span>  

 <span data-ttu-id="a8bf3-110">如果左侧表达式等于右侧表达式，则为`true` ；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-110">`true` if the left expression is equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a8bf3-111">备注</span><span class="sxs-lookup"><span data-stu-id="a8bf3-111">Remarks</span></span>  

 <span data-ttu-id="a8bf3-112">== 运算符等效于 =。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-112">The == operator is equivalent to =.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8bf3-113">示例</span><span class="sxs-lookup"><span data-stu-id="a8bf3-113">Example</span></span>  

 <span data-ttu-id="a8bf3-114">下面的 Entity SQL 查询使用 = 比较运算符比较两个表达式是否相等。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-114">The following Entity SQL query uses = comparison operator to compare the equality of two expressions.</span></span> <span data-ttu-id="a8bf3-115">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="a8bf3-116">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="a8bf3-116">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="a8bf3-117">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="a8bf3-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="a8bf3-118">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="a8bf3-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#EQUALS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#equals)]  
  
## <a name="see-also"></a><span data-ttu-id="a8bf3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="a8bf3-119">See also</span></span>

- [<span data-ttu-id="a8bf3-120">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="a8bf3-120">Entity SQL Reference</span></span>](entity-sql-reference.md)

---
description: '了解详细信息： <= (小于或等于)  (实体 SQL) '
title: '<= (小于或等于)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: 7c46da5c-fa09-4d90-adcc-c7e1b769d8e6
ms.openlocfilehash: f720c4ef87cdd0cceea175b1ea70caf5ac6e1deb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748253"
---
# <a name="-less-than-or-equal-to-entity-sql"></a><span data-ttu-id="b0e83-103">\<=（小于或等于）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="b0e83-103">\<= (Less Than or Equal To) (Entity SQL)</span></span>

<span data-ttu-id="b0e83-104">比较两个表达式以确定左侧表达式的值是否小于或等于右侧表达式的值。</span><span class="sxs-lookup"><span data-stu-id="b0e83-104">Compares two expressions to determine whether the left expression has a value less than or equal to the right expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0e83-105">语法</span><span class="sxs-lookup"><span data-stu-id="b0e83-105">Syntax</span></span>  
  
```sql  
expression <= expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="b0e83-106">参数</span><span class="sxs-lookup"><span data-stu-id="b0e83-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="b0e83-107">任何有效的表达式。</span><span class="sxs-lookup"><span data-stu-id="b0e83-107">Any valid expression.</span></span> <span data-ttu-id="b0e83-108">两个表达式都必须包含可隐式转换的数据类型。</span><span class="sxs-lookup"><span data-stu-id="b0e83-108">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="b0e83-109">结果类型</span><span class="sxs-lookup"><span data-stu-id="b0e83-109">Result Types</span></span>  

 <span data-ttu-id="b0e83-110">如果左侧表达式的值小于或等于右侧表达式的值，则为`true` ；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="b0e83-110">`true` if the left expression has a value less than or equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b0e83-111">示例</span><span class="sxs-lookup"><span data-stu-id="b0e83-111">Example</span></span>  

 <span data-ttu-id="b0e83-112">下面的 Entity SQL 查询使用 <= 比较运算符比较两个表达式，以确定左侧表达式的值是否小于或等于右侧表达式的值。</span><span class="sxs-lookup"><span data-stu-id="b0e83-112">The following Entity SQL query uses <= comparison operator to compare two expressions to determine whether the left expression has a value less than or equal to the right expression.</span></span> <span data-ttu-id="b0e83-113">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="b0e83-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="b0e83-114">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="b0e83-114">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="b0e83-115">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="b0e83-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="b0e83-116">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="b0e83-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#LESS_OR_EQUALS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#less_or_equals)]  
  
## <a name="see-also"></a><span data-ttu-id="b0e83-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b0e83-117">See also</span></span>

- [<span data-ttu-id="b0e83-118">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="b0e83-118">Entity SQL Reference</span></span>](entity-sql-reference.md)

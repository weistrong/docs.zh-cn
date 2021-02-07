---
description: '详细了解： * (乘法)  (实体 SQL) '
title: '*  (乘)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: 508ce246-4e86-47dd-a605-4af4bebb9891
ms.openlocfilehash: 92606e5f9e4646ab651d0e07095e6f419401188f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696615"
---
# <a name="-multiply-entity-sql"></a><span data-ttu-id="8df59-103">\*（乘）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="8df59-103">\* (Multiply) (Entity SQL)</span></span>

<span data-ttu-id="8df59-104">将两个表达式相乘。</span><span class="sxs-lookup"><span data-stu-id="8df59-104">Multiplies two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8df59-105">语法</span><span class="sxs-lookup"><span data-stu-id="8df59-105">Syntax</span></span>  
  
```sql  
expression * expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="8df59-106">参数</span><span class="sxs-lookup"><span data-stu-id="8df59-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="8df59-107">任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="8df59-107">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="8df59-108">结果类型</span><span class="sxs-lookup"><span data-stu-id="8df59-108">Result Types</span></span>  

 <span data-ttu-id="8df59-109">对这两个参数进行隐式类型提升而产生的数据类型。</span><span class="sxs-lookup"><span data-stu-id="8df59-109">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="8df59-110">有关隐式类型升级的详细信息，请参阅 [类型系统](type-system-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="8df59-110">For more information about implicit type promotion, see [Type System](type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8df59-111">示例</span><span class="sxs-lookup"><span data-stu-id="8df59-111">Example</span></span>  

 <span data-ttu-id="8df59-112">以下 Entity SQL 查询使用 \* 算术运算符将两个数字相乘。</span><span class="sxs-lookup"><span data-stu-id="8df59-112">The following Entity SQL query uses the \* arithmetic operator to multiply two numbers.</span></span> <span data-ttu-id="8df59-113">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="8df59-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="8df59-114">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="8df59-114">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="8df59-115">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="8df59-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="8df59-116">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="8df59-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#MULTIPLY](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#multiply)]  
  
## <a name="see-also"></a><span data-ttu-id="8df59-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="8df59-117">See also</span></span>

- [<span data-ttu-id="8df59-118">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="8df59-118">Entity SQL Reference</span></span>](entity-sql-reference.md)

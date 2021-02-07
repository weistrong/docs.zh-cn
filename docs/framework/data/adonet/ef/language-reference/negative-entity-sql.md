---
description: '了解有关以下内容的详细信息：- (消极)  (实体 SQL) '
title: '-  (负)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: 208e54ef-4741-4ec5-89d6-6ff700863cb0
ms.openlocfilehash: f3d30ce36b95e44755d148dc06279f67f15b0664
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712878"
---
# <a name="--negative-entity-sql"></a><span data-ttu-id="8117e-103">-（负号）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="8117e-103">- (Negative) (Entity SQL)</span></span>

<span data-ttu-id="8117e-104">返回数值表达式的值的负值。</span><span class="sxs-lookup"><span data-stu-id="8117e-104">Returns the negative of the value of a numeric expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8117e-105">语法</span><span class="sxs-lookup"><span data-stu-id="8117e-105">Syntax</span></span>  
  
```sql  
- expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="8117e-106">参数</span><span class="sxs-lookup"><span data-stu-id="8117e-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="8117e-107">任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="8117e-107">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="8117e-108">结果类型</span><span class="sxs-lookup"><span data-stu-id="8117e-108">Result Types</span></span>  

 <span data-ttu-id="8117e-109">`expression` 的数据类型。</span><span class="sxs-lookup"><span data-stu-id="8117e-109">The data type of `expression`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8117e-110">备注</span><span class="sxs-lookup"><span data-stu-id="8117e-110">Remarks</span></span>  

 <span data-ttu-id="8117e-111">如果 `expression` 为无符号类型，则结果类型将是与 `expression`的类型相关性最密切的有符号类型。</span><span class="sxs-lookup"><span data-stu-id="8117e-111">If `expression` is an unsigned type, the result type will be the signed type that most closely relates to the type of `expression`.</span></span> <span data-ttu-id="8117e-112">例如，如果 `expression` 属于 Byte 类型，则将返回类型为 Int16 的值。</span><span class="sxs-lookup"><span data-stu-id="8117e-112">For example, if `expression` is of type Byte, a value of type Int16 will be returned.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8117e-113">示例</span><span class="sxs-lookup"><span data-stu-id="8117e-113">Example</span></span>  

 <span data-ttu-id="8117e-114">以下 Entity SQL 查询使用 - 算数运算符以返回数值表达式的值的负值。</span><span class="sxs-lookup"><span data-stu-id="8117e-114">The following Entity SQL query uses the - arithmetic operator to return the negative of the value of a numeric expression.</span></span> <span data-ttu-id="8117e-115">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="8117e-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="8117e-116">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="8117e-116">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="8117e-117">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="8117e-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="8117e-118">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="8117e-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#NEGATIVE](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#negative)]  
  
## <a name="see-also"></a><span data-ttu-id="8117e-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8117e-119">See also</span></span>

- [<span data-ttu-id="8117e-120">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="8117e-120">Entity SQL Reference</span></span>](entity-sql-reference.md)

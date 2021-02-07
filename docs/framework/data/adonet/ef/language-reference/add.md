---
description: '详细了解： + (Add) '
title: + （加）
ms.date: 03/30/2017
ms.assetid: 51769b02-a8f7-4177-9e99-bbd10e77092c
ms.openlocfilehash: b8ec9f50b349fe971513f399b7e9984e9044cf58
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697304"
---
# <a name="-add"></a><span data-ttu-id="d1ed0-103">+（添加）</span><span class="sxs-lookup"><span data-stu-id="d1ed0-103">+ (Add)</span></span>

<span data-ttu-id="d1ed0-104">两个数相加。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-104">Adds two numbers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1ed0-105">语法</span><span class="sxs-lookup"><span data-stu-id="d1ed0-105">Syntax</span></span>  
  
```csharp  
expression + expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="d1ed0-106">参数</span><span class="sxs-lookup"><span data-stu-id="d1ed0-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="d1ed0-107">任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-107">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="d1ed0-108">结果类型</span><span class="sxs-lookup"><span data-stu-id="d1ed0-108">Result Types</span></span>  

 <span data-ttu-id="d1ed0-109">对这两个参数进行隐式类型提升而产生的数据类型。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-109">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="d1ed0-110">有关隐式类型升级的详细信息，请参阅 [类型系统](type-system-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-110">For more information about implicit type promotion, see [Type System](type-system-entity-sql.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d1ed0-111">备注</span><span class="sxs-lookup"><span data-stu-id="d1ed0-111">Remarks</span></span>  

 <span data-ttu-id="d1ed0-112">对于 EDM.String 类型，加法指的是串联。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-112">For EDM.String types, addition is concatenation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1ed0-113">示例</span><span class="sxs-lookup"><span data-stu-id="d1ed0-113">Example</span></span>  

 <span data-ttu-id="d1ed0-114">以下 Entity SQL 查询使用 + 算术运算符将两个数值相加。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-114">The following Entity SQL query uses the + arithmetic operator to add two numbers.</span></span> <span data-ttu-id="d1ed0-115">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="d1ed0-116">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="d1ed0-116">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="d1ed0-117">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="d1ed0-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="d1ed0-118">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="d1ed0-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#ADD](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#add)]  
  
## <a name="see-also"></a><span data-ttu-id="d1ed0-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1ed0-119">See also</span></span>

- [<span data-ttu-id="d1ed0-120">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="d1ed0-120">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="d1ed0-121">概念模型类型 (CSDL)</span><span class="sxs-lookup"><span data-stu-id="d1ed0-121">Conceptual Model Types (CSDL)</span></span>](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#conceptual-model-types-csdl)

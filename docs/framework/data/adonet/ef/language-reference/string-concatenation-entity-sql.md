---
description: '详细了解： + (字符串串联)  (实体 SQL) '
title: '+  () 实体 SQL (字符串串联) '
ms.date: 03/30/2017
ms.assetid: 580130fa-6c7c-4f76-a47d-d22c27ccadf6
ms.openlocfilehash: 7b6aac5b865e2127bb23446248e20d83ea3c7ea3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791837"
---
# <a name="-string-concatenation-entity-sql"></a><span data-ttu-id="07292-103">+（字符串串联）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="07292-103">+ (String Concatenation) (Entity SQL)</span></span>

<span data-ttu-id="07292-104">串联两个字符串。</span><span class="sxs-lookup"><span data-stu-id="07292-104">Concatenates two strings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07292-105">语法</span><span class="sxs-lookup"><span data-stu-id="07292-105">Syntax</span></span>  
  
```sql  
expression + expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="07292-106">参数</span><span class="sxs-lookup"><span data-stu-id="07292-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="07292-107">EDM.String 数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="07292-107">Any valid expression of the EDM.String data types.</span></span> <span data-ttu-id="07292-108">两个表达式必须具有相同的数据类型，或者其中一个表达式必须能够隐式转换为另一个表达式的数据类型。</span><span class="sxs-lookup"><span data-stu-id="07292-108">Both expressions must be of the same data type, or one expression must be able to be implicitly converted to the data type of the other expression.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="07292-109">结果类型</span><span class="sxs-lookup"><span data-stu-id="07292-109">Result Types</span></span>  

 <span data-ttu-id="07292-110">对这两个参数进行隐式类型提升而产生的数据类型。</span><span class="sxs-lookup"><span data-stu-id="07292-110">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="07292-111">有关隐式类型升级的详细信息，请参阅 [类型系统](type-system-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="07292-111">For more information about implicit type promotion, see [Type System](type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="07292-112">示例</span><span class="sxs-lookup"><span data-stu-id="07292-112">Example</span></span>  

 <span data-ttu-id="07292-113">以下 Entity SQL 查询使用 + 运算符以串联两个字符串。</span><span class="sxs-lookup"><span data-stu-id="07292-113">The following Entity SQL query uses the + operator to concatenates two strings.</span></span> <span data-ttu-id="07292-114">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="07292-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="07292-115">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="07292-115">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="07292-116">按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。</span><span class="sxs-lookup"><span data-stu-id="07292-116">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2. <span data-ttu-id="07292-117">将以下查询作为参数传递给 `ExecutePrimitiveTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="07292-117">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#CONCAT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#concat)]  
  
## <a name="see-also"></a><span data-ttu-id="07292-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="07292-118">See also</span></span>

- [<span data-ttu-id="07292-119">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="07292-119">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="07292-120">概念模型类型 (CSDL)</span><span class="sxs-lookup"><span data-stu-id="07292-120">Conceptual Model Types (CSDL)</span></span>](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#conceptual-model-types-csdl)

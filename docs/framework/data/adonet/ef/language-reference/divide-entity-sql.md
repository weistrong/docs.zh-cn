---
description: '详细了解：/ (除以)  (实体 SQL) '
title: '-  (除以)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: ef48c368-f3ed-4275-8ada-4e9649781262
ms.openlocfilehash: 4ac487c636c460401eeb147dc7ce1a8d8ba7f7ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724630"
---
# <a name="-divide-entity-sql"></a><span data-ttu-id="3e4ab-103">/（除）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="3e4ab-103">/ (Divide) (Entity SQL)</span></span>

<span data-ttu-id="3e4ab-104">用一个数除以另一个数。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-104">Divides one number by another.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e4ab-105">语法</span><span class="sxs-lookup"><span data-stu-id="3e4ab-105">Syntax</span></span>  
  
```sql  
dividend / divisor  
```  
  
## <a name="arguments"></a><span data-ttu-id="3e4ab-106">参数</span><span class="sxs-lookup"><span data-stu-id="3e4ab-106">Arguments</span></span>  

 `dividend`  
 <span data-ttu-id="3e4ab-107">被除数的数值表达式。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-107">The numeric expression to divide.</span></span> <span data-ttu-id="3e4ab-108">`dividend` 为任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-108">`dividend` is any valid expression of any one of the numeric data types.</span></span>  
  
 `divisor`  
 <span data-ttu-id="3e4ab-109">除数的数值表达式。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-109">The numeric expression to divide the dividend by.</span></span> <span data-ttu-id="3e4ab-110">`divisor` 为任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-110">`divisor` is any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="3e4ab-111">结果类型</span><span class="sxs-lookup"><span data-stu-id="3e4ab-111">Result Types</span></span>  

 <span data-ttu-id="3e4ab-112">对这两个参数进行隐式类型提升而产生的数据类型。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-112">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="3e4ab-113">有关隐式类型升级的详细信息，请参阅 [类型系统](type-system-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-113">For more information about implicit type promotion, see [Type System](type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3e4ab-114">示例</span><span class="sxs-lookup"><span data-stu-id="3e4ab-114">Example</span></span>  

 <span data-ttu-id="3e4ab-115">以下实体 SQL 查询使用/算术运算符将一个数除以另一个数。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-115">The following Entity SQL query uses the / arithmetic operator to divide one number by another.</span></span> <span data-ttu-id="3e4ab-116">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-116">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="3e4ab-117">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="3e4ab-117">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="3e4ab-118">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="3e4ab-118">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="3e4ab-119">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="3e4ab-119">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#DIVIDE](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#divide)]  
  
## <a name="see-also"></a><span data-ttu-id="3e4ab-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="3e4ab-120">See also</span></span>

- [<span data-ttu-id="3e4ab-121">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="3e4ab-121">Entity SQL Reference</span></span>](entity-sql-reference.md)

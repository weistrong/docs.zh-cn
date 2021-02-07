---
description: '了解详细信息： (取模)  (实体 SQL) '
title: （取模）（实体 SQL）
ms.date: 03/30/2017
ms.assetid: 243ddc4f-3c4e-41e1-a3ef-4ed39e36248b
ms.openlocfilehash: 8ac9bf2fa9dbee843215dcfeed13fefc7bd54796
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696628"
---
# <a name="modulo-entity-sql"></a><span data-ttu-id="09762-103">（取模）（实体 SQL）</span><span class="sxs-lookup"><span data-stu-id="09762-103">(Modulo) (Entity SQL)</span></span>

<span data-ttu-id="09762-104">返回两个表达式相除后的余数。</span><span class="sxs-lookup"><span data-stu-id="09762-104">Returns the remainder of one expression divided by another.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09762-105">语法</span><span class="sxs-lookup"><span data-stu-id="09762-105">Syntax</span></span>  
  
```sql  
dividend % divisor  
```  
  
## <a name="arguments"></a><span data-ttu-id="09762-106">参数</span><span class="sxs-lookup"><span data-stu-id="09762-106">Arguments</span></span>  

 `dividend`  
 <span data-ttu-id="09762-107">被除数的数值表达式。</span><span class="sxs-lookup"><span data-stu-id="09762-107">The numeric expression to divide.</span></span> <span data-ttu-id="09762-108">`dividend` 为任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="09762-108">`dividend` is any valid expression of any one of the numeric data types.</span></span>  
  
 `divisor`  
 <span data-ttu-id="09762-109">除数的数值表达式。</span><span class="sxs-lookup"><span data-stu-id="09762-109">The numeric expression to divide the dividend by.</span></span> <span data-ttu-id="09762-110">`divisor` 为任何一种数值数据类型的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="09762-110">`divisor` is any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="09762-111">结果类型</span><span class="sxs-lookup"><span data-stu-id="09762-111">Result Types</span></span>  

 <span data-ttu-id="09762-112">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="09762-112">Edm.Int32</span></span>  
  
## <a name="example"></a><span data-ttu-id="09762-113">示例</span><span class="sxs-lookup"><span data-stu-id="09762-113">Example</span></span>  

 <span data-ttu-id="09762-114">以下 Entity SQL 查询使用 % 算数运算符以返回两个表达式相除后的余数。</span><span class="sxs-lookup"><span data-stu-id="09762-114">The following Entity SQL query uses the % arithmetic operator to return the remainder of one expression divided by another.</span></span> <span data-ttu-id="09762-115">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="09762-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="09762-116">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="09762-116">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="09762-117">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="09762-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="09762-118">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="09762-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#MODULO](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#modulo)]  
  
## <a name="see-also"></a><span data-ttu-id="09762-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="09762-119">See also</span></span>

- [<span data-ttu-id="09762-120">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="09762-120">Entity SQL Reference</span></span>](entity-sql-reference.md)

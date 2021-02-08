---
description: '了解详细信息： > (大于)  (实体 SQL) '
title: '> （大于）(Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 4cea865c-677c-4b06-99a1-010f2ae2394a
ms.openlocfilehash: e14470d477336fd719bb419657af3fdadcd54d98
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786285"
---
# <a name="-greater-than-entity-sql"></a><span data-ttu-id="9e436-103">> (大于)  (实体 SQL) </span><span class="sxs-lookup"><span data-stu-id="9e436-103">> (Greater Than) (Entity SQL)</span></span>

<span data-ttu-id="9e436-104">比较两个表达式以确定左侧表达式的值是否大于右侧表达式的值。</span><span class="sxs-lookup"><span data-stu-id="9e436-104">Compares two expressions to determine whether the left expression has a value greater than the right expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e436-105">语法</span><span class="sxs-lookup"><span data-stu-id="9e436-105">Syntax</span></span>  
  
```sql  
expression > expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="9e436-106">参数</span><span class="sxs-lookup"><span data-stu-id="9e436-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="9e436-107">任何有效的表达式。</span><span class="sxs-lookup"><span data-stu-id="9e436-107">Any valid expression.</span></span> <span data-ttu-id="9e436-108">两个表达式都必须包含可隐式转换的数据类型。</span><span class="sxs-lookup"><span data-stu-id="9e436-108">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="9e436-109">结果类型</span><span class="sxs-lookup"><span data-stu-id="9e436-109">Result Types</span></span>  

 <span data-ttu-id="9e436-110">如果左侧表达式的值大于右侧表达式的值，则为`true` ；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="9e436-110">`true` if the left expression has a value greater than the right expression; otherwise, `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9e436-111">示例</span><span class="sxs-lookup"><span data-stu-id="9e436-111">Example</span></span>  

 <span data-ttu-id="9e436-112">下面的 Entity SQL 查询使用 > 比较运算符比较两个表达式，以确定左侧表达式的值是否大于右侧表达式的值。</span><span class="sxs-lookup"><span data-stu-id="9e436-112">The following Entity SQL query uses > comparison operator to compare two expressions to determine whether the left expression has a value greater than the right expression.</span></span> <span data-ttu-id="9e436-113">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="9e436-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="9e436-114">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="9e436-114">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="9e436-115">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="9e436-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="9e436-116">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="9e436-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#GREATER](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#greater)]  
  
## <a name="see-also"></a><span data-ttu-id="9e436-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9e436-117">See also</span></span>

- [<span data-ttu-id="9e436-118">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="9e436-118">Entity SQL Reference</span></span>](entity-sql-reference.md)

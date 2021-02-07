---
description: '了解详细信息： < (小于)  (实体 SQL) '
title: '< (小于)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: 1fc2a039-3ad6-4b3c-b41d-09932e803f86
ms.openlocfilehash: 523defa6c19ca43a5827258277bbe3f489b9b8c2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748279"
---
# <a name="-less-than-entity-sql"></a><span data-ttu-id="c1bcf-103">\<（小于）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c1bcf-103">\< (Less Than) (Entity SQL)</span></span>

<span data-ttu-id="c1bcf-104">比较两个表达式以确定左侧表达式的值是否小于右侧表达式的值。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-104">Compares two expressions to determine whether the left expression has a value less than the right expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1bcf-105">语法</span><span class="sxs-lookup"><span data-stu-id="c1bcf-105">Syntax</span></span>  
  
```sql  
expression < expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="c1bcf-106">参数</span><span class="sxs-lookup"><span data-stu-id="c1bcf-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="c1bcf-107">任何有效的表达式。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-107">Any valid expression.</span></span> <span data-ttu-id="c1bcf-108">两个表达式都必须包含可隐式转换的数据类型。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-108">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="c1bcf-109">结果类型</span><span class="sxs-lookup"><span data-stu-id="c1bcf-109">Result Types</span></span>  

 <span data-ttu-id="c1bcf-110">如果左侧表达式的值小于右侧表达式的值，则为`true` ；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-110">`true` if the left expression has a value less than the right expression; otherwise, `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1bcf-111">示例</span><span class="sxs-lookup"><span data-stu-id="c1bcf-111">Example</span></span>  

 <span data-ttu-id="c1bcf-112">下面的 Entity SQL 查询使用 < 比较运算符比较两个表达式，以确定左侧表达式的值是否小于右侧表达式的值。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-112">The following Entity SQL query uses < comparison operator to compare two expressions to determine whether the left expression has a value less than the right expression.</span></span> <span data-ttu-id="c1bcf-113">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="c1bcf-114">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="c1bcf-114">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="c1bcf-115">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="c1bcf-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="c1bcf-116">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="c1bcf-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#LESS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#less)]  
  
## <a name="see-also"></a><span data-ttu-id="c1bcf-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1bcf-117">See also</span></span>

- [<span data-ttu-id="c1bcf-118">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="c1bcf-118">Entity SQL Reference</span></span>](entity-sql-reference.md)

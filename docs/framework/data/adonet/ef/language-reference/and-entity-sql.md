---
description: '了解详细信息： &amp; &amp; (和)  (实体 SQL) '
title: '&amp;&amp; (和)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: e7d24213-471d-4807-b85e-570375df89b5
ms.openlocfilehash: 14fc6bc3f58ac78cb9806a7f421db87bbad048ae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697174"
---
# <a name="ampamp-and-entity-sql"></a><span data-ttu-id="3cff2-103">&amp;&amp; (和)  (实体 SQL) </span><span class="sxs-lookup"><span data-stu-id="3cff2-103">&amp;&amp; (AND) (Entity SQL)</span></span>

<span data-ttu-id="3cff2-104">如果两个表达式均为 `true` ，则返回 `true`；否则，返回 `false` 或 `NULL`。</span><span class="sxs-lookup"><span data-stu-id="3cff2-104">Returns `true` if both expressions are `true`; otherwise, `false` or `NULL`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cff2-105">语法</span><span class="sxs-lookup"><span data-stu-id="3cff2-105">Syntax</span></span>  
  
```csharp  
boolean_expression AND boolean_expression
```

<span data-ttu-id="3cff2-106">or</span><span class="sxs-lookup"><span data-stu-id="3cff2-106">or</span></span>  

```csharp
boolean_expression && boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="3cff2-107">自变量</span><span class="sxs-lookup"><span data-stu-id="3cff2-107">Arguments</span></span>  

 `boolean_expression`  
 <span data-ttu-id="3cff2-108">返回 Boolean 的任何有效表达式。</span><span class="sxs-lookup"><span data-stu-id="3cff2-108">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3cff2-109">备注</span><span class="sxs-lookup"><span data-stu-id="3cff2-109">Remarks</span></span>  

 <span data-ttu-id="3cff2-110">双“与”符号 (&&) 与 AND 运算符具有相同的功能。</span><span class="sxs-lookup"><span data-stu-id="3cff2-110">Double ampersands (&&) have the same functionality as the AND operator.</span></span>  
  
 <span data-ttu-id="3cff2-111">下表显示可能的输入值和返回类型。</span><span class="sxs-lookup"><span data-stu-id="3cff2-111">The following table shows possible input values and return types.</span></span>  
  
||`TRUE`|`FALSE`|`NULL`|  
|-|------------|-------------|------------|  
|`TRUE`|<span data-ttu-id="3cff2-112">true</span><span class="sxs-lookup"><span data-stu-id="3cff2-112">TRUE</span></span>|<span data-ttu-id="3cff2-113">false</span><span class="sxs-lookup"><span data-stu-id="3cff2-113">FALSE</span></span>|<span data-ttu-id="3cff2-114">Null</span><span class="sxs-lookup"><span data-stu-id="3cff2-114">NULL</span></span>|  
|`FALSE`|<span data-ttu-id="3cff2-115">false</span><span class="sxs-lookup"><span data-stu-id="3cff2-115">FALSE</span></span>|<span data-ttu-id="3cff2-116">false</span><span class="sxs-lookup"><span data-stu-id="3cff2-116">FALSE</span></span>|<span data-ttu-id="3cff2-117">false</span><span class="sxs-lookup"><span data-stu-id="3cff2-117">FALSE</span></span>|  
|`NULL`|<span data-ttu-id="3cff2-118">Null</span><span class="sxs-lookup"><span data-stu-id="3cff2-118">NULL</span></span>|<span data-ttu-id="3cff2-119">false</span><span class="sxs-lookup"><span data-stu-id="3cff2-119">FALSE</span></span>|<span data-ttu-id="3cff2-120">Null</span><span class="sxs-lookup"><span data-stu-id="3cff2-120">NULL</span></span>|  
  
## <a name="example"></a><span data-ttu-id="3cff2-121">示例</span><span class="sxs-lookup"><span data-stu-id="3cff2-121">Example</span></span>  

 <span data-ttu-id="3cff2-122">以下 Entity SQL 查询演示如何使用 AND 运算符。</span><span class="sxs-lookup"><span data-stu-id="3cff2-122">The following Entity SQL query demonstrates how to use the AND operator.</span></span> <span data-ttu-id="3cff2-123">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="3cff2-123">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="3cff2-124">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="3cff2-124">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="3cff2-125">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="3cff2-125">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="3cff2-126">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="3cff2-126">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#AND](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#and)]  
  
## <a name="see-also"></a><span data-ttu-id="3cff2-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="3cff2-127">See also</span></span>

- [<span data-ttu-id="3cff2-128">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="3cff2-128">Entity SQL Reference</span></span>](entity-sql-reference.md)

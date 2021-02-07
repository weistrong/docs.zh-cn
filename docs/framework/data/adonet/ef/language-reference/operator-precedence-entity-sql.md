---
description: '了解详细信息：运算符优先级 (实体 SQL) '
title: 运算符优先级 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: e92e4ca5-2889-4266-9625-47f0eb01a948
ms.openlocfilehash: 72cfdecf7dfe4ce590d99e866429e771f9ede231
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739321"
---
# <a name="operator-precedence-entity-sql"></a><span data-ttu-id="94f73-103">运算符优先级 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="94f73-103">Operator Precedence (Entity SQL)</span></span>

<span data-ttu-id="94f73-104">当 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询具有多个运算符时，运算符优先级确定执行操作的顺序。</span><span class="sxs-lookup"><span data-stu-id="94f73-104">When an [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query has multiple operators, operator precedence determines the sequence in which the operations are performed.</span></span> <span data-ttu-id="94f73-105">执行顺序可能对查询结果有明显的影响。</span><span class="sxs-lookup"><span data-stu-id="94f73-105">The order of execution can significantly affect the query result.</span></span>  
  
 <span data-ttu-id="94f73-106">运算符的优先级别如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="94f73-106">Operators have the precedence levels shown in the following table.</span></span> <span data-ttu-id="94f73-107">在较低级别的运算符之前先对较高级别的运算符进行求值。</span><span class="sxs-lookup"><span data-stu-id="94f73-107">An operator with a higher level is evaluated before an operator with a lower level.</span></span>  
  
|<span data-ttu-id="94f73-108">级别</span><span class="sxs-lookup"><span data-stu-id="94f73-108">Level</span></span>|<span data-ttu-id="94f73-109">操作类型</span><span class="sxs-lookup"><span data-stu-id="94f73-109">Operation type</span></span>|<span data-ttu-id="94f73-110">操作员</span><span class="sxs-lookup"><span data-stu-id="94f73-110">Operator</span></span>|  
|-----------|--------------------|--------------|  
|<span data-ttu-id="94f73-111">1</span><span class="sxs-lookup"><span data-stu-id="94f73-111">1</span></span>|<span data-ttu-id="94f73-112">主要</span><span class="sxs-lookup"><span data-stu-id="94f73-112">Primary</span></span>|`. , [] ()`|  
|<span data-ttu-id="94f73-113">2</span><span class="sxs-lookup"><span data-stu-id="94f73-113">2</span></span>|<span data-ttu-id="94f73-114">一元</span><span class="sxs-lookup"><span data-stu-id="94f73-114">Unary</span></span>|`! not`|  
|<span data-ttu-id="94f73-115">3</span><span class="sxs-lookup"><span data-stu-id="94f73-115">3</span></span>|<span data-ttu-id="94f73-116">乘法</span><span class="sxs-lookup"><span data-stu-id="94f73-116">Multiplicative</span></span>|`* / %`|  
|<span data-ttu-id="94f73-117">4</span><span class="sxs-lookup"><span data-stu-id="94f73-117">4</span></span>|<span data-ttu-id="94f73-118">加法</span><span class="sxs-lookup"><span data-stu-id="94f73-118">Additive</span></span>|`+ -`|  
|<span data-ttu-id="94f73-119">5</span><span class="sxs-lookup"><span data-stu-id="94f73-119">5</span></span>|<span data-ttu-id="94f73-120">中间件排序</span><span class="sxs-lookup"><span data-stu-id="94f73-120">Ordering</span></span>|`< > <= >=`|  
|<span data-ttu-id="94f73-121">6</span><span class="sxs-lookup"><span data-stu-id="94f73-121">6</span></span>|<span data-ttu-id="94f73-122">相等</span><span class="sxs-lookup"><span data-stu-id="94f73-122">Equality</span></span>|`= != <>`|  
|<span data-ttu-id="94f73-123">7</span><span class="sxs-lookup"><span data-stu-id="94f73-123">7</span></span>|<span data-ttu-id="94f73-124">条件“与”</span><span class="sxs-lookup"><span data-stu-id="94f73-124">Conditional AND</span></span>|`and &&`|  
|<span data-ttu-id="94f73-125">8</span><span class="sxs-lookup"><span data-stu-id="94f73-125">8</span></span>|<span data-ttu-id="94f73-126">条件“或”</span><span class="sxs-lookup"><span data-stu-id="94f73-126">Conditional OR</span></span>|`or &#124;&#124;`|  
  
 <span data-ttu-id="94f73-127">当一个表达式中的两个运算符有相同的运算符优先级别时，将按照它们在查询中的位置对其从左到右进行求值。</span><span class="sxs-lookup"><span data-stu-id="94f73-127">When two operators in an expression have the same operator precedence level, they are evaluated left to right, based on their position in the query.</span></span> <span data-ttu-id="94f73-128">例如，`x+y-z` 将计算为 `(x+y)-z`。</span><span class="sxs-lookup"><span data-stu-id="94f73-128">For example, `x+y-z` is evaluated as `(x+y)-z`.</span></span>  
  
 <span data-ttu-id="94f73-129">在查询中可以使用括号替代所定义的运算符的优先级。</span><span class="sxs-lookup"><span data-stu-id="94f73-129">You can use parentheses to override the defined precedence of the operators in a query.</span></span> <span data-ttu-id="94f73-130">首先对括号中的内容进行求值，从而产生一个结果，然后括号外的运算符才可以使用这个结果。</span><span class="sxs-lookup"><span data-stu-id="94f73-130">Everything within parentheses is evaluated first to yield a single result before that result can be used by any operator outside the parentheses.</span></span> <span data-ttu-id="94f73-131">例如，将 `x+y*z` 乘以 `y` ， `z` 然后添加 `x` ，但 `(x+y)*z` 将添加 `x` 到，然后将结果与 `y` 相乘 `z` 。</span><span class="sxs-lookup"><span data-stu-id="94f73-131">For example, `x+y*z` multiplies `y` by `z` and then adds `x`, but `(x+y)*z` adds `x` to `y` and then multiplies the result by `z`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94f73-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="94f73-132">See also</span></span>

- [<span data-ttu-id="94f73-133">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="94f73-133">Entity SQL Overview</span></span>](entity-sql-overview.md)

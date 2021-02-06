---
description: '详细了解： Let 子句 (Visual Basic) '
title: Let 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryLet
helpviewer_keywords:
- queries [Visual Basic], Let
- Let clause [Visual Basic]
- Let statement [Visual Basic]
ms.assetid: 981aa516-16eb-4c53-b1f1-5aa3e82f316e
ms.openlocfilehash: 88a7d96bb790a1e6ec5adfa4337c51f807930168
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99653636"
---
# <a name="let-clause-visual-basic"></a><span data-ttu-id="8be70-103">Let 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8be70-103">Let Clause (Visual Basic)</span></span>

<span data-ttu-id="8be70-104">计算值并将其分配给查询中的新变量。</span><span class="sxs-lookup"><span data-stu-id="8be70-104">Computes a value and assigns it to a new variable within the query.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8be70-105">语法</span><span class="sxs-lookup"><span data-stu-id="8be70-105">Syntax</span></span>  
  
```vb  
Let variable = expression [, ...]  
```  
  
## <a name="parts"></a><span data-ttu-id="8be70-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="8be70-106">Parts</span></span>  
  
|<span data-ttu-id="8be70-107">术语</span><span class="sxs-lookup"><span data-stu-id="8be70-107">Term</span></span>|<span data-ttu-id="8be70-108">定义</span><span class="sxs-lookup"><span data-stu-id="8be70-108">Definition</span></span>|  
|---|---|  
|`variable`|<span data-ttu-id="8be70-109">必需。</span><span class="sxs-lookup"><span data-stu-id="8be70-109">Required.</span></span> <span data-ttu-id="8be70-110">可用于引用所提供表达式的结果的别名。</span><span class="sxs-lookup"><span data-stu-id="8be70-110">An alias that can be used to reference the results of the supplied expression.</span></span>|  
|`expression`|<span data-ttu-id="8be70-111">必需。</span><span class="sxs-lookup"><span data-stu-id="8be70-111">Required.</span></span> <span data-ttu-id="8be70-112">将进行计算并分配给指定变量的表达式。</span><span class="sxs-lookup"><span data-stu-id="8be70-112">An expression that will be evaluated and assigned to the specified variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8be70-113">备注</span><span class="sxs-lookup"><span data-stu-id="8be70-113">Remarks</span></span>  

 <span data-ttu-id="8be70-114">`Let`使用子句可以计算每个查询结果的值，并使用别名引用这些值。</span><span class="sxs-lookup"><span data-stu-id="8be70-114">The `Let` clause enables you to compute values for each query result and reference them by using an alias.</span></span> <span data-ttu-id="8be70-115">别名可用于其他子句，如 `Where` 子句。</span><span class="sxs-lookup"><span data-stu-id="8be70-115">The alias can be used in other clauses, such as the `Where` clause.</span></span> <span data-ttu-id="8be70-116">`Let`使用子句可以创建更易于阅读的查询语句，因为您可以为查询中包括的 expression 子句指定一个别名，并在每次使用 expression 子句时替换该别名。</span><span class="sxs-lookup"><span data-stu-id="8be70-116">The `Let` clause enables you to create a query statement that is easier to read because you can specify an alias for an expression clause included in the query and substitute the alias each time the expression clause is used.</span></span>  
  
 <span data-ttu-id="8be70-117">可以在子句中包含任意数量的 `variable` 和 `expression` 赋值 `Let` 。</span><span class="sxs-lookup"><span data-stu-id="8be70-117">You can include any number of `variable` and `expression` assignments in the `Let` clause.</span></span> <span data-ttu-id="8be70-118">用逗号分隔每个分配 (，) 。</span><span class="sxs-lookup"><span data-stu-id="8be70-118">Separate each assignment with a comma (,).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8be70-119">示例</span><span class="sxs-lookup"><span data-stu-id="8be70-119">Example</span></span>  

 <span data-ttu-id="8be70-120">下面的代码示例使用 `Let` 子句来计算产品10% 的折扣。</span><span class="sxs-lookup"><span data-stu-id="8be70-120">The following code example uses the `Let` clause to compute a 10 percent discount on products.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#16)]  
  
## <a name="see-also"></a><span data-ttu-id="8be70-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="8be70-121">See also</span></span>

- [<span data-ttu-id="8be70-122">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="8be70-122">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="8be70-123">查询</span><span class="sxs-lookup"><span data-stu-id="8be70-123">Queries</span></span>](index.md)
- [<span data-ttu-id="8be70-124">Select 子句</span><span class="sxs-lookup"><span data-stu-id="8be70-124">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="8be70-125">From 子句</span><span class="sxs-lookup"><span data-stu-id="8be70-125">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="8be70-126">Where 子句</span><span class="sxs-lookup"><span data-stu-id="8be70-126">Where Clause</span></span>](where-clause.md)

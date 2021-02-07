---
description: '了解有关详细信息，请参阅 Take While 子句 (Visual Basic) '
title: Take While 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTakeWhile
helpviewer_keywords:
- queries [Visual Basic], Take While
- Take While clause [Visual Basic]
- Take While statement [Visual Basic]
ms.assetid: db8f9f2f-fc9f-4a6c-b0b8-1bf048147e11
ms.openlocfilehash: a413223d4a85670c66f71e24addb92ae4d38a4a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719703"
---
# <a name="take-while-clause-visual-basic"></a><span data-ttu-id="dcba4-103">Take While 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dcba4-103">Take While Clause (Visual Basic)</span></span>

<span data-ttu-id="dcba4-104">包括集合中指定条件为 `true` 的任何元素，并绕过剩余元素。</span><span class="sxs-lookup"><span data-stu-id="dcba4-104">Includes elements in a collection as long as a specified condition is `true` and bypasses the remaining elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcba4-105">语法</span><span class="sxs-lookup"><span data-stu-id="dcba4-105">Syntax</span></span>  
  
```vb  
Take While expression  
```  
  
## <a name="parts"></a><span data-ttu-id="dcba4-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="dcba4-106">Parts</span></span>  
  
|<span data-ttu-id="dcba4-107">术语</span><span class="sxs-lookup"><span data-stu-id="dcba4-107">Term</span></span>|<span data-ttu-id="dcba4-108">定义</span><span class="sxs-lookup"><span data-stu-id="dcba4-108">Definition</span></span>|  
|---|---|  
|`expression`|<span data-ttu-id="dcba4-109">必需。</span><span class="sxs-lookup"><span data-stu-id="dcba4-109">Required.</span></span> <span data-ttu-id="dcba4-110">表示要为其测试元素的条件的表达式。</span><span class="sxs-lookup"><span data-stu-id="dcba4-110">An expression that represents a condition to test elements for.</span></span> <span data-ttu-id="dcba4-111">表达式必须返回一个 `Boolean` 值或函数等效项，如 `Integer` 要计算为的 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="dcba4-111">The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dcba4-112">备注</span><span class="sxs-lookup"><span data-stu-id="dcba4-112">Remarks</span></span>  

 <span data-ttu-id="dcba4-113">`Take While`子句包括从查询结果的开头开始直到提供的返回的元素 `expression` `false` 。</span><span class="sxs-lookup"><span data-stu-id="dcba4-113">The `Take While` clause includes elements from the start of a query result until the supplied `expression` returns `false`.</span></span> <span data-ttu-id="dcba4-114">返回后 `expression` `false` ，查询将跳过所有剩余的元素。</span><span class="sxs-lookup"><span data-stu-id="dcba4-114">After the `expression` returns `false`, the query will bypass all remaining elements.</span></span> <span data-ttu-id="dcba4-115">`expression`对于剩余的结果，将忽略。</span><span class="sxs-lookup"><span data-stu-id="dcba4-115">The `expression` is ignored for the remaining results.</span></span>  
  
 <span data-ttu-id="dcba4-116">`Take While`子句与子句的不同之处 `Where` 在于， `Where` 子句可用于包括查询中满足特定条件的所有元素。</span><span class="sxs-lookup"><span data-stu-id="dcba4-116">The `Take While` clause differs from the `Where` clause in that the `Where` clause can be used to include all elements from a query that meet a particular condition.</span></span> <span data-ttu-id="dcba4-117">`Take While`子句仅包含元素，直到第一次未满足条件。</span><span class="sxs-lookup"><span data-stu-id="dcba4-117">The `Take While` clause includes elements only until the first time that the condition is not satisfied.</span></span> <span data-ttu-id="dcba4-118">`Take While`当使用排序的查询结果时，子句最有用。</span><span class="sxs-lookup"><span data-stu-id="dcba4-118">The `Take While` clause is most useful when you are working with an ordered query result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dcba4-119">示例</span><span class="sxs-lookup"><span data-stu-id="dcba4-119">Example</span></span>  

 <span data-ttu-id="dcba4-120">下面的代码示例使用 `Take While` 子句检索结果，直到找到第一个不含任何订单的客户。</span><span class="sxs-lookup"><span data-stu-id="dcba4-120">The following code example uses the `Take While` clause to retrieve results until the first customer without any orders is found.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="dcba4-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="dcba4-121">See also</span></span>

- [<span data-ttu-id="dcba4-122">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="dcba4-122">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="dcba4-123">查询</span><span class="sxs-lookup"><span data-stu-id="dcba4-123">Queries</span></span>](index.md)
- [<span data-ttu-id="dcba4-124">Select 子句</span><span class="sxs-lookup"><span data-stu-id="dcba4-124">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="dcba4-125">From 子句</span><span class="sxs-lookup"><span data-stu-id="dcba4-125">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="dcba4-126">Take 子句</span><span class="sxs-lookup"><span data-stu-id="dcba4-126">Take Clause</span></span>](take-clause.md)
- [<span data-ttu-id="dcba4-127">Skip While 子句</span><span class="sxs-lookup"><span data-stu-id="dcba4-127">Skip While Clause</span></span>](skip-while-clause.md)
- [<span data-ttu-id="dcba4-128">Where 子句</span><span class="sxs-lookup"><span data-stu-id="dcba4-128">Where Clause</span></span>](where-clause.md)

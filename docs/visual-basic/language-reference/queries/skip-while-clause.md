---
description: '了解详细信息： Skip While 子句 (Visual Basic) '
title: Skip While 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkipWhile
helpviewer_keywords:
- Skip While statement [Visual Basic]
- Skip While clause [Visual Basic]
- queries [Visual Basic], Skip While
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
ms.openlocfilehash: 6f2785fde1a62c10c914904ccba51510dbb1a041
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773844"
---
# <a name="skip-while-clause-visual-basic"></a><span data-ttu-id="18357-103">Skip While 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="18357-103">Skip While Clause (Visual Basic)</span></span>

<span data-ttu-id="18357-104">跳过集合中指定条件为 `true` 的任何元素，然后返回剩余元素。</span><span class="sxs-lookup"><span data-stu-id="18357-104">Bypasses elements in a collection as long as a specified condition is `true` and then returns the remaining elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18357-105">语法</span><span class="sxs-lookup"><span data-stu-id="18357-105">Syntax</span></span>  
  
```vb  
Skip While expression  
```  
  
## <a name="parts"></a><span data-ttu-id="18357-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="18357-106">Parts</span></span>  
  
|<span data-ttu-id="18357-107">术语</span><span class="sxs-lookup"><span data-stu-id="18357-107">Term</span></span>|<span data-ttu-id="18357-108">定义</span><span class="sxs-lookup"><span data-stu-id="18357-108">Definition</span></span>|  
|---|---|  
|`expression`|<span data-ttu-id="18357-109">必需。</span><span class="sxs-lookup"><span data-stu-id="18357-109">Required.</span></span> <span data-ttu-id="18357-110">表示要为其测试元素的条件的表达式。</span><span class="sxs-lookup"><span data-stu-id="18357-110">An expression that represents a condition to test elements for.</span></span> <span data-ttu-id="18357-111">表达式必须返回一个 `Boolean` 值或函数等效项，如 `Integer` 要计算为的 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="18357-111">The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="18357-112">备注</span><span class="sxs-lookup"><span data-stu-id="18357-112">Remarks</span></span>  

 <span data-ttu-id="18357-113">`Skip While`子句会绕过查询结果开头的元素，直到提供的 `expression` 返回 `false` 。</span><span class="sxs-lookup"><span data-stu-id="18357-113">The `Skip While` clause bypasses elements from the beginning of a query result until the supplied `expression` returns `false`.</span></span> <span data-ttu-id="18357-114">`expression`返回后 `false` ，该查询将返回所有剩余元素。</span><span class="sxs-lookup"><span data-stu-id="18357-114">After `expression` returns `false`, the query returns all the remaining elements.</span></span> <span data-ttu-id="18357-115">`expression`对于剩余的结果，将忽略。</span><span class="sxs-lookup"><span data-stu-id="18357-115">The `expression` is ignored for the remaining results.</span></span>  
  
 <span data-ttu-id="18357-116">`Skip While`子句与子句的不同之处 `Where` 在于， `Where` 子句可用于从查询中排除不满足特定条件的所有元素。</span><span class="sxs-lookup"><span data-stu-id="18357-116">The `Skip While` clause differs from the `Where` clause in that the `Where` clause can be used to exclude all elements from a query that do not meet a particular condition.</span></span> <span data-ttu-id="18357-117">`Skip While`子句仅排除元素，直到第一次未满足条件。</span><span class="sxs-lookup"><span data-stu-id="18357-117">The `Skip While` clause excludes elements only until the first time that the condition is not satisfied.</span></span> <span data-ttu-id="18357-118">`Skip While`当使用排序的查询结果时，子句最有用。</span><span class="sxs-lookup"><span data-stu-id="18357-118">The `Skip While` clause is most useful when you are working with an ordered query result.</span></span>  
  
 <span data-ttu-id="18357-119">您可以使用子句从查询结果的开头跳过特定数目的结果 `Skip` 。</span><span class="sxs-lookup"><span data-stu-id="18357-119">You can bypass a specific number of results from the beginning of a query result by using the `Skip` clause.</span></span>  
  
## <a name="example"></a><span data-ttu-id="18357-120">示例</span><span class="sxs-lookup"><span data-stu-id="18357-120">Example</span></span>  

 <span data-ttu-id="18357-121">下面的代码示例使用 `Skip While` 子句跳过结果，直到找到美国中的第一个客户。</span><span class="sxs-lookup"><span data-stu-id="18357-121">The following code example uses the `Skip While` clause to bypass results until the first customer from the United States is found.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="18357-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="18357-122">See also</span></span>

- [<span data-ttu-id="18357-123">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="18357-123">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="18357-124">查询</span><span class="sxs-lookup"><span data-stu-id="18357-124">Queries</span></span>](index.md)
- [<span data-ttu-id="18357-125">Select 子句</span><span class="sxs-lookup"><span data-stu-id="18357-125">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="18357-126">From 子句</span><span class="sxs-lookup"><span data-stu-id="18357-126">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="18357-127">Skip 子句</span><span class="sxs-lookup"><span data-stu-id="18357-127">Skip Clause</span></span>](skip-clause.md)
- [<span data-ttu-id="18357-128">Take While 子句</span><span class="sxs-lookup"><span data-stu-id="18357-128">Take While Clause</span></span>](take-while-clause.md)
- [<span data-ttu-id="18357-129">Where 子句</span><span class="sxs-lookup"><span data-stu-id="18357-129">Where Clause</span></span>](where-clause.md)

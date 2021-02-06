---
description: '了解有关详细信息，请参阅 Take 子句 (Visual Basic) '
title: Take 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTake
helpviewer_keywords:
- Take statement [Visual Basic]
- queries [Visual Basic], Take
- Take clause [Visual Basic]
ms.assetid: 77bf87b2-1476-4456-957f-fee922fbad8c
ms.openlocfilehash: 6542d262490d9d4acff893b2a99ffb60dd1446a2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99653532"
---
# <a name="take-clause-visual-basic"></a><span data-ttu-id="4f4ed-103">Take 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4f4ed-103">Take Clause (Visual Basic)</span></span>

<span data-ttu-id="4f4ed-104">从集合的开头返回指定数量的连续元素。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-104">Returns a specified number of contiguous elements from the start of a collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f4ed-105">语法</span><span class="sxs-lookup"><span data-stu-id="4f4ed-105">Syntax</span></span>  
  
```vb  
Take count  
```  
  
## <a name="parts"></a><span data-ttu-id="4f4ed-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="4f4ed-106">Parts</span></span>  

 `count`  
 <span data-ttu-id="4f4ed-107">必需。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-107">Required.</span></span> <span data-ttu-id="4f4ed-108">值或计算结果为要返回的序列的元素数的表达式。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-108">A value or an expression that evaluates to the number of elements of the sequence to return.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4f4ed-109">备注</span><span class="sxs-lookup"><span data-stu-id="4f4ed-109">Remarks</span></span>  

 <span data-ttu-id="4f4ed-110">`Take`子句使查询包括从结果列表的开头开始的指定数量的连续元素。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-110">The `Take` clause causes a query to include a specified number of contiguous elements from the start of a results list.</span></span> <span data-ttu-id="4f4ed-111">要包括的元素数是由参数指定的 `count` 。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-111">The number of elements to include is specified by the `count` parameter.</span></span>  
  
 <span data-ttu-id="4f4ed-112">可以将 `Take` 子句与子句结合使用， `Skip` 以便从查询的任何段返回数据范围。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-112">You can use the `Take` clause with the `Skip` clause to return a range of data from any segment of a query.</span></span> <span data-ttu-id="4f4ed-113">为此，请将范围中第一个元素的索引传递给 `Skip` 子句，并将范围的大小传递到 `Take` 子句。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-113">To do this, pass the index of the first element of the range to the `Skip` clause and the size of the range to the `Take` clause.</span></span> <span data-ttu-id="4f4ed-114">在这种情况下， `Take` 子句必须在子句之后指定 `Skip` 。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-114">In this case, the `Take` clause must be specified after the `Skip` clause.</span></span>  
  
 <span data-ttu-id="4f4ed-115">在 `Take` 查询中使用子句时，您可能还需要确保按使 `Take` 子句包含预期结果的顺序返回结果。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-115">When you use the `Take` clause in a query, you may also need to ensure that the results are returned in an order that will enable the `Take` clause to include the intended results.</span></span> <span data-ttu-id="4f4ed-116">有关对查询结果进行排序的详细信息，请参阅 [Order By 子句](order-by-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-116">For more information about ordering query results, see [Order By Clause](order-by-clause.md).</span></span>  
  
 <span data-ttu-id="4f4ed-117">您可以使用 `TakeWhile` 子句指定仅返回某些元素，具体取决于所提供的条件。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-117">You can use the `TakeWhile` clause to specify that only certain elements be returned, depending on a supplied condition.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f4ed-118">示例</span><span class="sxs-lookup"><span data-stu-id="4f4ed-118">Example</span></span>  

 <span data-ttu-id="4f4ed-119">下面的代码示例将 `Take` 子句与子句一起使用 `Skip` ，以从页的查询返回数据。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-119">The following code example uses the `Take` clause together with the `Skip` clause to return data from a query in pages.</span></span> <span data-ttu-id="4f4ed-120">GetCustomers 函数使用 `Skip` 子句跳过列表中的客户，直至提供的起始索引值，并使用 `Take` 子句返回从该索引值开始的客户页面。</span><span class="sxs-lookup"><span data-stu-id="4f4ed-120">The GetCustomers function uses the `Skip` clause to bypass the customers in the list until the supplied starting index value, and uses the `Take` clause to return a page of customers starting from that index value.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="4f4ed-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="4f4ed-121">See also</span></span>

- [<span data-ttu-id="4f4ed-122">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="4f4ed-122">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="4f4ed-123">查询</span><span class="sxs-lookup"><span data-stu-id="4f4ed-123">Queries</span></span>](index.md)
- [<span data-ttu-id="4f4ed-124">Select 子句</span><span class="sxs-lookup"><span data-stu-id="4f4ed-124">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="4f4ed-125">From 子句</span><span class="sxs-lookup"><span data-stu-id="4f4ed-125">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="4f4ed-126">Order By 子句</span><span class="sxs-lookup"><span data-stu-id="4f4ed-126">Order By Clause</span></span>](order-by-clause.md)
- [<span data-ttu-id="4f4ed-127">Take While 子句</span><span class="sxs-lookup"><span data-stu-id="4f4ed-127">Take While Clause</span></span>](take-while-clause.md)
- [<span data-ttu-id="4f4ed-128">Skip 子句</span><span class="sxs-lookup"><span data-stu-id="4f4ed-128">Skip Clause</span></span>](skip-clause.md)

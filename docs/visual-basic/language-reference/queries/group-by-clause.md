---
description: '了解详细信息： Group By 子句 (Visual Basic) '
title: Group By 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryGroupByInto
- vb.QueryGroupBy
- vb.QueryGroupRef
- vb.QueryGroupInto
- vb.QueryGroup
helpviewer_keywords:
- queries [Visual Basic], Group By
- Group By statement [Visual Basic]
- Group By clause [Visual Basic]
ms.assetid: b1b5dcea-6654-473b-a2db-01f7e4c265d7
ms.openlocfilehash: f5cfb76b0f4b1d191f959ae1812140c6872e93bb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700502"
---
# <a name="group-by-clause-visual-basic"></a><span data-ttu-id="982b2-103">Group By 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="982b2-103">Group By Clause (Visual Basic)</span></span>

<span data-ttu-id="982b2-104">对查询结果的元素进行分组。</span><span class="sxs-lookup"><span data-stu-id="982b2-104">Groups the elements of a query result.</span></span> <span data-ttu-id="982b2-105">也可用于将聚合函数应用于每个组。</span><span class="sxs-lookup"><span data-stu-id="982b2-105">Can also be used to apply aggregate functions to each group.</span></span> <span data-ttu-id="982b2-106">分组运算基于一个或多个键。</span><span class="sxs-lookup"><span data-stu-id="982b2-106">The grouping operation is based on one or more keys.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="982b2-107">语法</span><span class="sxs-lookup"><span data-stu-id="982b2-107">Syntax</span></span>  
  
```vb  
Group [ listField1 [, listField2 [...] ] By keyExp1 [, keyExp2 [...] ]  
  Into aggregateList  
```  
  
## <a name="parts"></a><span data-ttu-id="982b2-108">组成部分</span><span class="sxs-lookup"><span data-stu-id="982b2-108">Parts</span></span>  
  
- <span data-ttu-id="982b2-109">`listField1`, `listField2`</span><span class="sxs-lookup"><span data-stu-id="982b2-109">`listField1`, `listField2`</span></span>  
  
     <span data-ttu-id="982b2-110">可选。</span><span class="sxs-lookup"><span data-stu-id="982b2-110">Optional.</span></span> <span data-ttu-id="982b2-111">分组结果中将包括一个或多个显式标识字段的查询变量的一个或多个字段。</span><span class="sxs-lookup"><span data-stu-id="982b2-111">One or more fields of the query variable or variables that explicitly identify the fields to be included in the grouped result.</span></span> <span data-ttu-id="982b2-112">如果未指定字段，则分组结果中将包括一个或多个查询变量的所有字段。</span><span class="sxs-lookup"><span data-stu-id="982b2-112">If no fields are specified, all fields of the query variable or variables are included in the grouped result.</span></span>  
  
- `keyExp1`  
  
     <span data-ttu-id="982b2-113">必需。</span><span class="sxs-lookup"><span data-stu-id="982b2-113">Required.</span></span> <span data-ttu-id="982b2-114">标识键以用于确定元素所在的组的表达式。</span><span class="sxs-lookup"><span data-stu-id="982b2-114">An expression that identifies the key to use to determine the groups of elements.</span></span> <span data-ttu-id="982b2-115">可以指定多个键以形成组合键。</span><span class="sxs-lookup"><span data-stu-id="982b2-115">You can specify more than one key to specify a composite key.</span></span>  
  
- `keyExp2`  
  
     <span data-ttu-id="982b2-116">可选。</span><span class="sxs-lookup"><span data-stu-id="982b2-116">Optional.</span></span> <span data-ttu-id="982b2-117">与 `keyExp1` 结合以形成组合键的一个或多个其他键。</span><span class="sxs-lookup"><span data-stu-id="982b2-117">One or more additional keys that are combined with `keyExp1` to create a composite key.</span></span>  
  
- `aggregateList`  
  
     <span data-ttu-id="982b2-118">必需。</span><span class="sxs-lookup"><span data-stu-id="982b2-118">Required.</span></span> <span data-ttu-id="982b2-119">标识如何对组进行聚合的一个或多个表达式。</span><span class="sxs-lookup"><span data-stu-id="982b2-119">One or more expressions that identify how the groups are aggregated.</span></span> <span data-ttu-id="982b2-120">若要标识分组结果的成员名称，请使用 `Group` 关键字，它可以采用以下任意一种形式：</span><span class="sxs-lookup"><span data-stu-id="982b2-120">To identify a member name for the grouped results, use the `Group` keyword, which can be in either of the following forms:</span></span>  
  
    ```vb  
    Into Group  
    ```  
  
     <span data-ttu-id="982b2-121">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="982b2-121">-or-</span></span>  
  
    ```vb  
    Into <alias> = Group  
    ```  
  
     <span data-ttu-id="982b2-122">还可以包含聚合函数以将其应用于该组。</span><span class="sxs-lookup"><span data-stu-id="982b2-122">You can also include aggregate functions to apply to the group.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="982b2-123">备注</span><span class="sxs-lookup"><span data-stu-id="982b2-123">Remarks</span></span>  

 <span data-ttu-id="982b2-124">可以使用 `Group By` 子句来将查询的结果分解为组。</span><span class="sxs-lookup"><span data-stu-id="982b2-124">You can use the `Group By` clause to break the results of a query into groups.</span></span> <span data-ttu-id="982b2-125">分组基于某个键或包含多个键的组合键。</span><span class="sxs-lookup"><span data-stu-id="982b2-125">The grouping is based on a key or a composite key consisting of multiple keys.</span></span> <span data-ttu-id="982b2-126">与匹配的键值相关联的元素包括在同一组中。</span><span class="sxs-lookup"><span data-stu-id="982b2-126">Elements that are associated with matching key values are included in the same group.</span></span>  
  
 <span data-ttu-id="982b2-127">使用 `aggregateList` 子句的 `Into` 参数和 `Group` 关键字来标识用于引用该组的成员名称。</span><span class="sxs-lookup"><span data-stu-id="982b2-127">You use the `aggregateList` parameter of the `Into` clause and the `Group` keyword to identify the member name that is used to reference the group.</span></span> <span data-ttu-id="982b2-128">还可以将聚合函数包括在 `Into` 子句中，以计算分组元素的值。</span><span class="sxs-lookup"><span data-stu-id="982b2-128">You can also include aggregate functions in the `Into` clause to compute values for the grouped elements.</span></span> <span data-ttu-id="982b2-129">有关标准聚合函数的列表，请参阅 [Aggregate Clause](aggregate-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="982b2-129">For a list of standard aggregate functions, see [Aggregate Clause](aggregate-clause.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="982b2-130">示例</span><span class="sxs-lookup"><span data-stu-id="982b2-130">Example</span></span>  

 <span data-ttu-id="982b2-131">下面的代码示例基于其位置 (国家/地区) 对客户列表进行分组，并提供每个组中的客户的计数。</span><span class="sxs-lookup"><span data-stu-id="982b2-131">The following code example groups a list of customers based on their location (country/region) and provides a count of the customers in each group.</span></span> <span data-ttu-id="982b2-132">按国家/地区名称对结果进行排序。</span><span class="sxs-lookup"><span data-stu-id="982b2-132">The results are ordered by country/region name.</span></span> <span data-ttu-id="982b2-133">按城市名称对分组结果进行排序。</span><span class="sxs-lookup"><span data-stu-id="982b2-133">The grouped results are ordered by city name.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#11)]  
  
## <a name="see-also"></a><span data-ttu-id="982b2-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="982b2-134">See also</span></span>

- [<span data-ttu-id="982b2-135">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="982b2-135">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="982b2-136">查询</span><span class="sxs-lookup"><span data-stu-id="982b2-136">Queries</span></span>](index.md)
- [<span data-ttu-id="982b2-137">Select 子句</span><span class="sxs-lookup"><span data-stu-id="982b2-137">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="982b2-138">From 子句</span><span class="sxs-lookup"><span data-stu-id="982b2-138">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="982b2-139">Order By 子句</span><span class="sxs-lookup"><span data-stu-id="982b2-139">Order By Clause</span></span>](order-by-clause.md)
- [<span data-ttu-id="982b2-140">Aggregate Clause</span><span class="sxs-lookup"><span data-stu-id="982b2-140">Aggregate Clause</span></span>](aggregate-clause.md)
- [<span data-ttu-id="982b2-141">Group Join 子句</span><span class="sxs-lookup"><span data-stu-id="982b2-141">Group Join Clause</span></span>](group-join-clause.md)

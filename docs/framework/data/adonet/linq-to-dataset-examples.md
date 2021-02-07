---
description: 了解详细信息： LINQ to DataSet 示例
title: LINQ to DataSet 示例
ms.date: 03/30/2017
ms.assetid: dfd91658-8d8a-45a4-a356-e327e809f21d
ms.openlocfilehash: 65977210fb160439231ea723134c94eb56ca8930
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672746"
---
# <a name="linq-to-dataset-examples"></a><span data-ttu-id="733ce-103">LINQ to DataSet 示例</span><span class="sxs-lookup"><span data-stu-id="733ce-103">LINQ to DataSet Examples</span></span>

<span data-ttu-id="733ce-104">本节提供使用标准查询运算符的 LINQ to DataSet 编程示例。</span><span class="sxs-lookup"><span data-stu-id="733ce-104">This section provides LINQ to DataSet programming examples that use the standard query operators.</span></span> <span data-ttu-id="733ce-105"><xref:System.Data.DataSet>这些示例中使用的是使用方法填充的 `FillDataSet` ，该方法是在将[数据加载到数据集](loading-data-into-a-dataset.md)时指定的。</span><span class="sxs-lookup"><span data-stu-id="733ce-105">The <xref:System.Data.DataSet> used in these examples is populated by using the `FillDataSet` method, which is specified in [Loading Data Into a DataSet](loading-data-into-a-dataset.md).</span></span> <span data-ttu-id="733ce-106">有关详细信息，请参阅 [标准查询运算符概述 (c # ) ](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md) 或 [标准查询运算符概述 (Visual Basic) ](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="733ce-106">For more information, see [Standard Query Operators Overview (C#)](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md) or [Standard Query Operators Overview (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="733ce-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="733ce-107">In This Section</span></span>  

 [<span data-ttu-id="733ce-108">查询表达式示例</span><span class="sxs-lookup"><span data-stu-id="733ce-108">Query Expression Examples</span></span>](query-expression-examples-linq-to-dataset.md)  
 <span data-ttu-id="733ce-109">包含下面的示例：</span><span class="sxs-lookup"><span data-stu-id="733ce-109">Contains the following examples:</span></span>  
  
- [<span data-ttu-id="733ce-110">投影</span><span class="sxs-lookup"><span data-stu-id="733ce-110">Projection</span></span>](query-expression-syntax-examples-projection-linq-to-dataset.md)  
  
- [<span data-ttu-id="733ce-111">限制</span><span class="sxs-lookup"><span data-stu-id="733ce-111">Restriction</span></span>](query-expression-syntax-examples-restriction-linq-to-dataset.md)  
  
- [<span data-ttu-id="733ce-112">分区</span><span class="sxs-lookup"><span data-stu-id="733ce-112">Partitioning</span></span>](query-expression-syntax-examples-partitioning.md)  
  
- [<span data-ttu-id="733ce-113">中间件排序</span><span class="sxs-lookup"><span data-stu-id="733ce-113">Ordering</span></span>](query-expression-syntax-examples-ordering-linq-to-dataset.md)  
  
- [<span data-ttu-id="733ce-114">元素运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-114">Element Operators</span></span>](query-expression-syntax-examples-element-operators.md)  
  
- [<span data-ttu-id="733ce-115">聚合运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-115">Aggregate Operators</span></span>](query-expression-syntax-examples-aggregate-operators.md)  
  
- [<span data-ttu-id="733ce-116">联接运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-116">Join Operators</span></span>](query-expression-syntax-examples-join-operators.md)  
  
 [<span data-ttu-id="733ce-117">基于方法的查询示例</span><span class="sxs-lookup"><span data-stu-id="733ce-117">Method-Based Query Examples</span></span>](method-based-query-examples-linq-to-dataset.md)  
 <span data-ttu-id="733ce-118">包含下面的示例：</span><span class="sxs-lookup"><span data-stu-id="733ce-118">Contains the following examples:</span></span>  
  
- [<span data-ttu-id="733ce-119">投影</span><span class="sxs-lookup"><span data-stu-id="733ce-119">Projection</span></span>](method-based-query-syntax-examples-projection.md)  
  
- [<span data-ttu-id="733ce-120">分区</span><span class="sxs-lookup"><span data-stu-id="733ce-120">Partitioning</span></span>](method-based-query-syntax-examples-partitioning-linq.md)  
  
- [<span data-ttu-id="733ce-121">中间件排序</span><span class="sxs-lookup"><span data-stu-id="733ce-121">Ordering</span></span>](method-based-query-syntax-examples-ordering-linq-to-dataset.md)  
  
- [<span data-ttu-id="733ce-122">集运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-122">Set Operators</span></span>](method-based-query-syntax-examples-set-operators.md)  
  
- [<span data-ttu-id="733ce-123">转换运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-123">Conversion Operators</span></span>](method-based-query-syntax-examples-conversion-operators.md)  
  
- [<span data-ttu-id="733ce-124">元素运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-124">Element Operators</span></span>](method-based-query-syntax-examples-element-operators.md)  
  
- [<span data-ttu-id="733ce-125">聚合运算符</span><span class="sxs-lookup"><span data-stu-id="733ce-125">Aggregate Operators</span></span>](method-based-query-syntax-examples-aggregate-operators.md)  
  
- [<span data-ttu-id="733ce-126">Join</span><span class="sxs-lookup"><span data-stu-id="733ce-126">Join</span></span>](method-based-query-syntax-examples-join-linq-to-dataset.md)  
  
 [<span data-ttu-id="733ce-127">数据集特定的运算符示例</span><span class="sxs-lookup"><span data-stu-id="733ce-127">DataSet-Specific Operator Examples</span></span>](dataset-specific-operator-examples-linq-to-dataset.md)  
 <span data-ttu-id="733ce-128">包含演示如何使用 <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> 方法和 <xref:System.Data.DataRowComparer> 类的示例。</span><span class="sxs-lookup"><span data-stu-id="733ce-128">Contains examples that demonstrate how to use the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method and the <xref:System.Data.DataRowComparer> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="733ce-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="733ce-129">See also</span></span>

- [<span data-ttu-id="733ce-130">编程指南</span><span class="sxs-lookup"><span data-stu-id="733ce-130">Programming Guide</span></span>](programming-guide-linq-to-dataset.md)
- [<span data-ttu-id="733ce-131">将数据加载到数据集中</span><span class="sxs-lookup"><span data-stu-id="733ce-131">Loading Data Into a DataSet</span></span>](loading-data-into-a-dataset.md)

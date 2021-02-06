---
description: '了解详细信息：查询数据集 (LINQ to DataSet) '
title: 查询数据集 (LINQ to DataSet)
ms.date: 03/30/2017
ms.assetid: bb68d2e4-623d-4d60-85e3-965254f6fee7
ms.openlocfilehash: 609de99069d39317d8d372cb2a7f43ea301ada2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663451"
---
# <a name="querying-datasets-linq-to-dataset"></a><span data-ttu-id="2f92e-103">查询数据集 (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="2f92e-103">Querying DataSets (LINQ to DataSet)</span></span>

<span data-ttu-id="2f92e-104">用数据填充 <xref:System.Data.DataSet> 对象后，您可以开始查询该对象。</span><span class="sxs-lookup"><span data-stu-id="2f92e-104">After a <xref:System.Data.DataSet> object has been populated with data, you can begin querying it.</span></span> <span data-ttu-id="2f92e-105">使用 LINQ to DataSet 来表述查询类似于对其他启用 LINQ 的数据源使用 Language-Integrated 查询 (LINQ) 。</span><span class="sxs-lookup"><span data-stu-id="2f92e-105">Formulating queries with LINQ to DataSet is similar to using Language-Integrated Query (LINQ) against other LINQ-enabled data sources.</span></span> <span data-ttu-id="2f92e-106">但请记住，在对对象使用 LINQ 查询时 <xref:System.Data.DataSet> ，您要查询对象的枚举， <xref:System.Data.DataRow> 而不是自定义类型的枚举。</span><span class="sxs-lookup"><span data-stu-id="2f92e-106">Remember, however, that when you use LINQ queries over a <xref:System.Data.DataSet> object, you're querying an enumeration of <xref:System.Data.DataRow> objects instead of an enumeration of a custom type.</span></span> <span data-ttu-id="2f92e-107">这意味着你可以 <xref:System.Data.DataRow> 在 LINQ 查询中使用类的任意成员。</span><span class="sxs-lookup"><span data-stu-id="2f92e-107">This means that you can use any of the members of the <xref:System.Data.DataRow> class in your LINQ queries.</span></span> <span data-ttu-id="2f92e-108">这使您可以创建丰富复杂的查询。</span><span class="sxs-lookup"><span data-stu-id="2f92e-108">This lets you create rich, complex queries.</span></span>  
  
 <span data-ttu-id="2f92e-109">与 LINQ 的其他实现一样，您可以通过两种不同的形式创建 LINQ to DataSet 查询：查询表达式语法和基于方法的查询语法。</span><span class="sxs-lookup"><span data-stu-id="2f92e-109">As with other implementations of LINQ, you can create LINQ to DataSet queries in two different forms: query expression syntax and method-based query syntax.</span></span> <span data-ttu-id="2f92e-110">您可以使用查询表达式语法或基于方法的查询语法对 <xref:System.Data.DataSet> 中的单个表、对 <xref:System.Data.DataSet> 中的多个表或对类型化 <xref:System.Data.DataSet> 中的表执行查询。</span><span class="sxs-lookup"><span data-stu-id="2f92e-110">You can use query expression syntax or method-based query syntax to perform queries against single tables in a <xref:System.Data.DataSet>, against multiple tables in a <xref:System.Data.DataSet>, or against tables in a typed <xref:System.Data.DataSet>.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2f92e-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="2f92e-111">In This Section</span></span>  

 [<span data-ttu-id="2f92e-112">单表查询</span><span class="sxs-lookup"><span data-stu-id="2f92e-112">Single-Table Queries</span></span>](single-table-queries-linq-to-dataset.md)  
 <span data-ttu-id="2f92e-113">说明如何执行单表查询。</span><span class="sxs-lookup"><span data-stu-id="2f92e-113">Describes how to perform single-table queries.</span></span>  
  
 [<span data-ttu-id="2f92e-114">跨表查询</span><span class="sxs-lookup"><span data-stu-id="2f92e-114">Cross-Table Queries</span></span>](cross-table-queries-linq-to-dataset.md)  
 <span data-ttu-id="2f92e-115">说明如何执行交叉表查询。</span><span class="sxs-lookup"><span data-stu-id="2f92e-115">Describes how to perform cross-table queries.</span></span>  
  
 [<span data-ttu-id="2f92e-116">查询类型化数据集</span><span class="sxs-lookup"><span data-stu-id="2f92e-116">Querying Typed DataSets</span></span>](querying-typed-datasets.md)  
 <span data-ttu-id="2f92e-117">说明如何查询类型化 <xref:System.Data.DataSet> 对象。</span><span class="sxs-lookup"><span data-stu-id="2f92e-117">Describes how to query typed <xref:System.Data.DataSet> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f92e-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f92e-118">See also</span></span>

- [<span data-ttu-id="2f92e-119">LINQ to DataSet 示例</span><span class="sxs-lookup"><span data-stu-id="2f92e-119">LINQ to DataSet Examples</span></span>](linq-to-dataset-examples.md)
- [<span data-ttu-id="2f92e-120">将数据加载到数据集中</span><span class="sxs-lookup"><span data-stu-id="2f92e-120">Loading Data Into a DataSet</span></span>](loading-data-into-a-dataset.md)

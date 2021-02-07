---
description: '详细了解： LINQ to DataSet 编程指南 () '
title: 编程指南 (LINQ to DataSet)
ms.date: 03/30/2017
ms.assetid: 977aedd7-0084-46a0-b56f-345787a55da1
ms.openlocfilehash: b7f14d902b7a2df9d6add151b8783aa6fc0dcffd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672317"
---
# <a name="programming-guide-linq-to-dataset"></a><span data-ttu-id="6463e-103">编程指南 (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="6463e-103">Programming Guide (LINQ to DataSet)</span></span>

<span data-ttu-id="6463e-104">本部分提供有关用 LINQ to DataSet 进行编程的概念性信息和示例。</span><span class="sxs-lookup"><span data-stu-id="6463e-104">This section provides conceptual information and examples for programming with LINQ to DataSet.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6463e-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="6463e-105">In This Section</span></span>  

 [<span data-ttu-id="6463e-106">在 LINQ to DataSet 中查询</span><span class="sxs-lookup"><span data-stu-id="6463e-106">Queries in LINQ to DataSet</span></span>](queries-in-linq-to-dataset.md)  
 <span data-ttu-id="6463e-107">提供有关如何编写 LINQ to DataSet 查询的信息。</span><span class="sxs-lookup"><span data-stu-id="6463e-107">Provides information about how to write LINQ to DataSet queries.</span></span>  
  
 [<span data-ttu-id="6463e-108">查询数据集</span><span class="sxs-lookup"><span data-stu-id="6463e-108">Querying DataSets</span></span>](querying-datasets-linq-to-dataset.md)  
 <span data-ttu-id="6463e-109">说明如何查询 <xref:System.Data.DataSet> 对象。</span><span class="sxs-lookup"><span data-stu-id="6463e-109">Describes how to query <xref:System.Data.DataSet> objects.</span></span>  
  
 [<span data-ttu-id="6463e-110">比较 DataRow</span><span class="sxs-lookup"><span data-stu-id="6463e-110">Comparing DataRows</span></span>](comparing-datarows-linq-to-dataset.md)  
 <span data-ttu-id="6463e-111">说明如何使用 <xref:System.Data.DataRowComparer> 对象来比较数据行。</span><span class="sxs-lookup"><span data-stu-id="6463e-111">Describes how to use the <xref:System.Data.DataRowComparer> object to compare data rows.</span></span>  
  
 [<span data-ttu-id="6463e-112">从查询创建数据表</span><span class="sxs-lookup"><span data-stu-id="6463e-112">Creating a DataTable From a Query</span></span>](creating-a-datatable-from-a-query-linq-to-dataset.md)  
 <span data-ttu-id="6463e-113">提供有关 <xref:System.Data.DataTable> 通过使用方法从 LINQ to DataSet 查询创建的信息 <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> 。</span><span class="sxs-lookup"><span data-stu-id="6463e-113">Provides information about creating a <xref:System.Data.DataTable> from a LINQ to DataSet query by using the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method.</span></span>  
  
 [<span data-ttu-id="6463e-114">如何：实现 CopyToDataTable \<T> ，其中泛型类型 T 不是 DataRow</span><span class="sxs-lookup"><span data-stu-id="6463e-114">How to: Implement CopyToDataTable\<T> Where the Generic Type T Is Not a DataRow</span></span>](implement-copytodatatable-where-type-not-a-datarow.md)  
 <span data-ttu-id="6463e-115">描述如何实现自定义的 `CopyToDataTable<T>` 方法，其中泛型参数 T 的类型不是 <xref:System.Data.DataRow>。</span><span class="sxs-lookup"><span data-stu-id="6463e-115">Describes how to implement a custom `CopyToDataTable<T>` method where the generic parameter T is not of type <xref:System.Data.DataRow>.</span></span>  
  
 [<span data-ttu-id="6463e-116">泛型字段和 SetField 方法</span><span class="sxs-lookup"><span data-stu-id="6463e-116">Generic Field and SetField Methods</span></span>](generic-field-and-setfield-methods-linq-to-dataset.md)  
 <span data-ttu-id="6463e-117">提供有关泛型 <xref:System.Data.DataRowExtensions.Field%2A> 和 <xref:System.Data.DataRowExtensions.SetField%2A> 方法的信息。</span><span class="sxs-lookup"><span data-stu-id="6463e-117">Provides information about the generic <xref:System.Data.DataRowExtensions.Field%2A> and <xref:System.Data.DataRowExtensions.SetField%2A> methods.</span></span>  
  
 [<span data-ttu-id="6463e-118">数据绑定和 LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="6463e-118">Data Binding and LINQ to DataSet</span></span>](data-binding-and-linq-to-dataset.md)  
 <span data-ttu-id="6463e-119">说明使用 <xref:System.Data.DataView> 对象的数据绑定。</span><span class="sxs-lookup"><span data-stu-id="6463e-119">Describes databinding using the <xref:System.Data.DataView> object.</span></span>  
  
 [<span data-ttu-id="6463e-120">调试 LINQ to DataSet 查询</span><span class="sxs-lookup"><span data-stu-id="6463e-120">Debugging LINQ to DataSet Queries</span></span>](debugging-linq-to-dataset-queries.md)  
 <span data-ttu-id="6463e-121">提供有关 LINQ to DataSet 查询进行调试和故障排除的信息。</span><span class="sxs-lookup"><span data-stu-id="6463e-121">Provides information about debugging and troubleshooting LINQ to DataSet queries.</span></span>  
  
 [<span data-ttu-id="6463e-122">安全性</span><span class="sxs-lookup"><span data-stu-id="6463e-122">Security</span></span>](security-linq-to-dataset.md)  
 <span data-ttu-id="6463e-123">描述 LINQ to DataSet 中的安全问题。</span><span class="sxs-lookup"><span data-stu-id="6463e-123">Describes security issues in LINQ to DataSet.</span></span>  
  
 [<span data-ttu-id="6463e-124">LINQ to DataSet 示例</span><span class="sxs-lookup"><span data-stu-id="6463e-124">LINQ to DataSet Examples</span></span>](linq-to-dataset-examples.md)  
 <span data-ttu-id="6463e-125">提供使用 LINQ 运算符的查询示例。</span><span class="sxs-lookup"><span data-stu-id="6463e-125">Provides query examples that use the LINQ operators.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="6463e-126">参考</span><span class="sxs-lookup"><span data-stu-id="6463e-126">Reference</span></span>  

 <xref:System.Data.DataRowComparer>  
  
 <xref:System.Data.DataRowExtensions>  
  
 <xref:System.Data.DataTableExtensions>  
  
 <xref:System.Data.DataView>  
  
## <a name="see-also"></a><span data-ttu-id="6463e-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6463e-127">See also</span></span>

- [<span data-ttu-id="6463e-128">LINQ 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="6463e-128">LINQ and ADO.NET</span></span>](linq-and-ado-net.md)
- [<span data-ttu-id="6463e-129">语言集成查询 (LINQ)</span><span class="sxs-lookup"><span data-stu-id="6463e-129">Language Integrated Query (LINQ)</span></span>](../../../csharp/programming-guide/concepts/linq/index.md)

---
description: 了解详细信息： LINQ to DataSet
title: LINQ to DataSet
ms.date: 03/30/2017
ms.assetid: 743e3755-3ecb-45a2-8d9b-9ed41f0dcf17
ms.openlocfilehash: 74b5f97d9fecb05b1fd13e986dd0cbcc10fa1456
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681664"
---
# <a name="linq-to-dataset"></a><span data-ttu-id="ff029-103">LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="ff029-103">LINQ to DataSet</span></span>

<span data-ttu-id="ff029-104">LINQ to DataSet 可以更轻松、更快速地查询在对象中缓存的数据 <xref:System.Data.DataSet> 。</span><span class="sxs-lookup"><span data-stu-id="ff029-104">LINQ to DataSet makes it easier and faster to query over data cached in a <xref:System.Data.DataSet> object.</span></span> <span data-ttu-id="ff029-105">具体而言，LINQ to DataSet 通过使开发人员能够使用编程语言本身而不是使用单独的查询语言来编写查询，可以简化查询。</span><span class="sxs-lookup"><span data-stu-id="ff029-105">Specifically, LINQ to DataSet simplifies querying by enabling developers to write queries from the programming language itself, instead of by using a separate query language.</span></span> <span data-ttu-id="ff029-106">这对于 Visual Studio 开发人员特别有用，现在可以利用 Visual Studio 在其查询中提供的编译时语法检查、静态类型和 IntelliSense 支持。</span><span class="sxs-lookup"><span data-stu-id="ff029-106">This is especially useful for Visual Studio developers, who can now take advantage of the compile-time syntax checking, static typing, and IntelliSense support provided by the Visual Studio in their queries.</span></span>  
  
 <span data-ttu-id="ff029-107">LINQ to DataSet 还可以用于查询从一个或多个数据源合并的数据。</span><span class="sxs-lookup"><span data-stu-id="ff029-107">LINQ to DataSet can also be used to query over data that has been consolidated from one or more data sources.</span></span> <span data-ttu-id="ff029-108">这可以使许多需要灵活表示和处理数据的方案（例如查询本地聚合的数据和 Web 应用程序中的中间层缓存）能够实现。</span><span class="sxs-lookup"><span data-stu-id="ff029-108">This enables many scenarios that require flexibility in how data is represented and handled, such as querying locally aggregated data and middle-tier caching in Web applications.</span></span> <span data-ttu-id="ff029-109">具体地说，一般报告、分析和业务智能应用程序将需要这种操作方法。</span><span class="sxs-lookup"><span data-stu-id="ff029-109">In particular, generic reporting, analysis, and business intelligence applications require this method of manipulation.</span></span>  
  
 <span data-ttu-id="ff029-110">LINQ to DataSet 功能主要通过和类中的扩展方法公开 <xref:System.Data.DataRowExtensions> <xref:System.Data.DataTableExtensions> 。</span><span class="sxs-lookup"><span data-stu-id="ff029-110">The LINQ to DataSet functionality is exposed primarily through the extension methods in the <xref:System.Data.DataRowExtensions> and <xref:System.Data.DataTableExtensions> classes.</span></span> <span data-ttu-id="ff029-111">LINQ to DataSet 在上构建并使用现有的 ADO.NET 体系结构，而不是在应用程序代码中替换 ADO.NET。</span><span class="sxs-lookup"><span data-stu-id="ff029-111">LINQ to DataSet builds on and uses the existing ADO.NET architecture, and is not meant to replace ADO.NET in application code.</span></span> <span data-ttu-id="ff029-112">现有的 ADO.NET 代码将继续在 LINQ to DataSet 应用程序中运行。</span><span class="sxs-lookup"><span data-stu-id="ff029-112">Existing ADO.NET code will continue to function in a LINQ to DataSet application.</span></span> <span data-ttu-id="ff029-113">下图演示了 LINQ to DataSet 与 ADO.NET 和数据存储之间的关系。</span><span class="sxs-lookup"><span data-stu-id="ff029-113">The relationship of LINQ to DataSet to ADO.NET and the data store is illustrated in the following diagram.</span></span>  
  
 ![显示 LINQ to DataSet 基于 ADO.NET 提供程序的关系图。](./media/linq-to-dataset/linq-dataset-ado-dotnet-provider.gif)  
  
## <a name="in-this-section"></a><span data-ttu-id="ff029-115">本节内容</span><span class="sxs-lookup"><span data-stu-id="ff029-115">In This Section</span></span>  

 [<span data-ttu-id="ff029-116">入门</span><span class="sxs-lookup"><span data-stu-id="ff029-116">Getting Started</span></span>](getting-started-linq-to-dataset.md)  
  
 [<span data-ttu-id="ff029-117">编程指南</span><span class="sxs-lookup"><span data-stu-id="ff029-117">Programming Guide</span></span>](programming-guide-linq-to-dataset.md)  
  
## <a name="reference"></a><span data-ttu-id="ff029-118">参考</span><span class="sxs-lookup"><span data-stu-id="ff029-118">Reference</span></span>  

 <xref:System.Data.DataTableExtensions>  
  
 <xref:System.Data.DataRowExtensions>  
  
 <xref:System.Data.DataRowComparer>  
  
## <a name="see-also"></a><span data-ttu-id="ff029-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="ff029-119">See also</span></span>

- [<span data-ttu-id="ff029-120">语言集成查询 (LINQ) - C#</span><span class="sxs-lookup"><span data-stu-id="ff029-120">Language-Integrated Query (LINQ) - C#</span></span>](../../../csharp/programming-guide/concepts/linq/index.md)
- [<span data-ttu-id="ff029-121">语言集成查询 (LINQ) - Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ff029-121">Language-Integrated Query (LINQ) - Visual Basic</span></span>](../../../visual-basic/programming-guide/concepts/linq/index.md)
- [<span data-ttu-id="ff029-122">LINQ 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="ff029-122">LINQ and ADO.NET</span></span>](linq-and-ado-net.md)
- [<span data-ttu-id="ff029-123">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="ff029-123">ADO.NET</span></span>](index.md)

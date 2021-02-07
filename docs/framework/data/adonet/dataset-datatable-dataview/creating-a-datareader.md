---
description: 了解有关以下内容的详细信息：创建 DataReader
title: 创建 DataReader
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 49d4422a-7464-4ab8-8ec7-90185fde3ecf
ms.openlocfilehash: 3a9f47ce90beaa3da4c2835f8b75e770a6179a9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725098"
---
# <a name="creating-a-datareader"></a><span data-ttu-id="f98d3-103">创建 DataReader</span><span class="sxs-lookup"><span data-stu-id="f98d3-103">Creating a DataReader</span></span>

<span data-ttu-id="f98d3-104"><xref:System.Data.DataTable> 和 <xref:System.Data.DataSet> 类具有 <xref:System.Data.DataTable.CreateDataReader%2A> 方法，可以将 <xref:System.Data.DataTable> 的内容或 <xref:System.Data.DataSet> 对象的 <xref:System.Data.DataSet.Tables%2A> 集合的内容作为一个或多个只读、只进的结果集返回。</span><span class="sxs-lookup"><span data-stu-id="f98d3-104">The <xref:System.Data.DataTable> and <xref:System.Data.DataSet> classes have a <xref:System.Data.DataTable.CreateDataReader%2A> method that returns the contents of the <xref:System.Data.DataTable> or the contents of the <xref:System.Data.DataSet> object's <xref:System.Data.DataSet.Tables%2A> collection as one or more read-only, forward-only result sets.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f98d3-105">示例</span><span class="sxs-lookup"><span data-stu-id="f98d3-105">Example</span></span>  

 <span data-ttu-id="f98d3-106">以下控制台应用程序创建一个 <xref:System.Data.DataTable> 实例。</span><span class="sxs-lookup"><span data-stu-id="f98d3-106">The following console application creates a <xref:System.Data.DataTable> instance.</span></span> <span data-ttu-id="f98d3-107">然后，该示例将填充的传递 <xref:System.Data.DataTable> 给调用方法的过程，该过程会 <xref:System.Data.DataTable.CreateDataReader%2A> 循环访问中包含的结果 <xref:System.Data.DataTableReader> 。</span><span class="sxs-lookup"><span data-stu-id="f98d3-107">The example then passes the filled <xref:System.Data.DataTable> to a procedure that calls the <xref:System.Data.DataTable.CreateDataReader%2A> method, which iterates through the results contained within the <xref:System.Data.DataTableReader>.</span></span>  
  
 [!code-csharp[DataWorks DataTable.CreateDataReader#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DataTable.CreateDataReader/CS/source.cs#1)]
 [!code-vb[DataWorks DataTable.CreateDataReader#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DataTable.CreateDataReader/VB/source.vb#1)]  
  
 <span data-ttu-id="f98d3-108">该示例在控制台窗口中显示以下输出：</span><span class="sxs-lookup"><span data-stu-id="f98d3-108">The example displays the following output in the console window:</span></span>  
  
```output  
1 Mary  
2 Andy  
3 Peter  
4 Russ  
```  
  
## <a name="see-also"></a><span data-ttu-id="f98d3-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="f98d3-109">See also</span></span>

- <xref:System.Data.DataTable.CreateDataReader%2A>
- <xref:System.Data.DataSet.CreateDataReader%2A>
- [<span data-ttu-id="f98d3-110">DataTableReader</span><span class="sxs-lookup"><span data-stu-id="f98d3-110">DataTableReaders</span></span>](datatablereaders.md)
- [<span data-ttu-id="f98d3-111">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="f98d3-111">ADO.NET Overview</span></span>](../ado-net-overview.md)

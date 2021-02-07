---
description: 了解详细信息： Childview 和关系
title: ChildView 和关系
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d475d356-6abb-4701-8fd1-2906fb93dfba
ms.openlocfilehash: f27526ef0ad5bee70b0c67542e2611ff85b156f8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739711"
---
# <a name="childviews-and-relations"></a><span data-ttu-id="e7fb8-103">ChildView 和关系</span><span class="sxs-lookup"><span data-stu-id="e7fb8-103">ChildViews and Relations</span></span>

<span data-ttu-id="e7fb8-104">如果 <xref:System.Data.DataSet> 中的表之间存在关系，则可以使用 <xref:System.Data.DataView> 的 <xref:System.Data.DataRowView.CreateChildView%2A> 方法为父表中的行创建一个 <xref:System.Data.DataRowView>，包含相关子表中的行。</span><span class="sxs-lookup"><span data-stu-id="e7fb8-104">If a relationship exists between tables in a <xref:System.Data.DataSet>, you can create a <xref:System.Data.DataView> containing rows from the related child table by using the <xref:System.Data.DataRowView.CreateChildView%2A> method of the <xref:System.Data.DataRowView> for the rows in the parent table.</span></span> <span data-ttu-id="e7fb8-105">例如，以下代码按分类 **名称** 和 **ProductName** 排序按字母顺序显示 **类别** 及其相关的 **产品**。</span><span class="sxs-lookup"><span data-stu-id="e7fb8-105">For example, the following code displays **Categories** and their related **Products** in alphabetical order sorted by **CategoryName** and **ProductName**.</span></span>  
  
```vb  
Dim catTable As DataTable = catDS.Tables("Categories")  
Dim prodTable As DataTable = catDS.Tables("Products")  
  
' Create a relation between the Categories and Products tables.  
Dim relation As DataRelation = catDS.Relations.Add("CatProdRel", _  
  catTable.Columns("CategoryID"), _  
  prodTable.Columns("CategoryID"))  
  
' Create DataViews for the Categories and Products tables.  
Dim catView As DataView = New DataView(catTable, "", _  
  "CategoryName", DataViewRowState.CurrentRows)  
Dim prodView As DataView  
  
' Iterate through the Categories table.  
Dim catDRV, prodDRV As DataRowView  
  
For Each catDRV In catView  
  Console.WriteLine(catDRV("CategoryName"))  
  
  ' Create a DataView of the child product records.  
  prodView = catDRV.CreateChildView(relation)  
  prodView.Sort = "ProductName"  
  
  For Each prodDRV In prodView  
    Console.WriteLine(vbTab & prodDRV("ProductName"))  
  Next  
Next  
```  
  
```csharp  
DataTable catTable = catDS.Tables["Categories"];  
DataTable prodTable = catDS.Tables["Products"];  
  
// Create a relation between the Categories and Products tables.  
DataRelation relation = catDS.Relations.Add("CatProdRel",
  catTable.Columns["CategoryID"],  
                                                            prodTable.Columns["CategoryID"]);  
  
// Create DataViews for the Categories and Products tables.  
DataView catView = new DataView(catTable, "", "CategoryName",
  DataViewRowState.CurrentRows);  
DataView prodView;  
  
// Iterate through the Categories table.  
foreach (DataRowView catDRV in catView)  
{  
  Console.WriteLine(catDRV["CategoryName"]);  
  
  // Create a DataView of the child product records.  
  prodView = catDRV.CreateChildView(relation);  
  prodView.Sort = "ProductName";  
  
  foreach (DataRowView prodDRV in prodView)  
    Console.WriteLine("\t" + prodDRV["ProductName"]);  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="e7fb8-106">请参阅</span><span class="sxs-lookup"><span data-stu-id="e7fb8-106">See also</span></span>

- <xref:System.Data.DataSet>
- <xref:System.Data.DataView>
- <xref:System.Data.DataRowView>
- [<span data-ttu-id="e7fb8-107">DataView</span><span class="sxs-lookup"><span data-stu-id="e7fb8-107">DataViews</span></span>](dataviews.md)
- [<span data-ttu-id="e7fb8-108">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="e7fb8-108">ADO.NET Overview</span></span>](../ado-net-overview.md)

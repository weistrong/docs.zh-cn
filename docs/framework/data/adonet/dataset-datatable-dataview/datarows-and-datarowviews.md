---
description: 了解详细信息： Datarow 和 Datarowview
title: DataRow 和 DataRowView
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8f5eec26-b809-4aca-8778-7e202356d856
ms.openlocfilehash: d7700922a9ae76fb9898412b6a08394059e6e494
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724942"
---
# <a name="datarows-and-datarowviews"></a>DataRow 和 DataRowView

<xref:System.Data.DataView> 公开 <xref:System.Data.DataRowView> 对象的可枚举集合。 **DataRowView** 对象将值公开为按基础表中的列的名称或序号引用进行索引的对象数组。 可以 <xref:System.Data.DataRow> 使用 DataRowView 的属性访问由 **DataRowView** 公开的 <xref:System.Data.DataRowView.Row%2A> 。   
  
 使用 **DataRowView** 查看值时，DataView 的属性将 <xref:System.Data.DataView.RowStateFilter%2A> 确定公开基础 **DataRow** 的行版本。 有关使用 **DataRow** 访问不同行版本的信息，请参阅 [行状态和行版本](row-states-and-row-versions.md)。  
  
 以下代码示例显示一个表中的所有当前值和原始值。  
  
```vb  
Dim catView As DataView = New DataView(catDS.Tables("Categories"))  
Console.WriteLine("Current Values:")  
WriteView(catView)  
Console.WriteLine("Original Values:")  
catView.RowStateFilter = DataViewRowState.ModifiedOriginal  
WriteView(catView)
  
Public Shared Sub WriteView(thisDataView As DataView)  
  Dim rowView As DataRowView  
  Dim i As Integer  
  
  For Each rowView In thisDataView  
    For i = 0 To thisDataView.Table.Columns.Count - 1  
      Console.Write(rowView(i) & vbTab)  
    Next  
    Console.WriteLine()  
  Next  
End Sub  
```  
  
```csharp  
DataView catView = new DataView(catDS.Tables["Categories"]);  
Console.WriteLine("Current Values:");  
WriteView(catView);  
Console.WriteLine("Original Values:");  
catView.RowStateFilter = DataViewRowState.ModifiedOriginal;  
WriteView(catView);  
  
public static void WriteView(DataView thisDataView)  
{  
  foreach (DataRowView rowView in thisDataView)  
  {  
    for (int i = 0; i < thisDataView.Table.Columns.Count; i++)  
      Console.Write(rowView[i] + "\t");  
    Console.WriteLine();  
  }  
}  
```  
  
## <a name="see-also"></a>请参阅

- <xref:System.Data.DataRowVersion>
- <xref:System.Data.DataViewRowState>
- <xref:System.Data.DataView>
- <xref:System.Data.DataRowView>
- [DataView](dataviews.md)
- [ADO.NET 概述](../ado-net-overview.md)

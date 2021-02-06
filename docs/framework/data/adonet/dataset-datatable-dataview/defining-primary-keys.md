---
description: 了解详细信息：定义主键
title: 定义主键
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2ea85959-e763-4669-8bd9-46a9dab894bd
ms.openlocfilehash: 2becfbd124af723f55edb39666352fc501044045
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652544"
---
# <a name="defining-primary-keys"></a><span data-ttu-id="8d281-103">定义主键</span><span class="sxs-lookup"><span data-stu-id="8d281-103">Defining Primary Keys</span></span>

<span data-ttu-id="8d281-104">数据库表通常都有一列或一组列，用于唯一地标识表中的每一行。</span><span class="sxs-lookup"><span data-stu-id="8d281-104">A database table commonly has a column or group of columns that uniquely identifies each row in the table.</span></span> <span data-ttu-id="8d281-105">这种具有标识作用的列或列组称为主键。</span><span class="sxs-lookup"><span data-stu-id="8d281-105">This identifying column or group of columns is called the primary key.</span></span>  
  
 <span data-ttu-id="8d281-106">当你将单个指定 <xref:System.Data.DataColumn> 为的时 <xref:System.Data.DataTable.PrimaryKey%2A> <xref:System.Data.DataTable> ，该表会自动将列的 <xref:System.Data.DataColumn.AllowDBNull%2A> 属性设置为 **false** ，并将 <xref:System.Data.DataColumn.Unique%2A> 属性设置为 **true**。</span><span class="sxs-lookup"><span data-stu-id="8d281-106">When you identify a single <xref:System.Data.DataColumn> as the <xref:System.Data.DataTable.PrimaryKey%2A> for a <xref:System.Data.DataTable>, the table automatically sets the <xref:System.Data.DataColumn.AllowDBNull%2A> property of the column to **false** and the <xref:System.Data.DataColumn.Unique%2A> property to **true**.</span></span> <span data-ttu-id="8d281-107">对于多列主键，仅 **AllowDBNull** 属性自动设置为 **false**。</span><span class="sxs-lookup"><span data-stu-id="8d281-107">For multiple-column primary keys, only the **AllowDBNull** property is automatically set to **false**.</span></span>  
  
 <span data-ttu-id="8d281-108">接收的 **PrimaryKey** 属性的 <xref:System.Data.DataTable> 值是一个或多个 **DataColumn** 对象的数组，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="8d281-108">The **PrimaryKey** property of a <xref:System.Data.DataTable> receives as its value an array of one or more **DataColumn** objects, as shown in the following examples.</span></span> <span data-ttu-id="8d281-109">第一个示例将单独一列定义为主键。</span><span class="sxs-lookup"><span data-stu-id="8d281-109">The first example defines a single column as the primary key.</span></span>  
  
```vb  
workTable.PrimaryKey = New DataColumn() {workTable.Columns("CustID")}  
  
' Or  
  
Dim columns(1) As DataColumn  
columns(0) = workTable.Columns("CustID")  
workTable.PrimaryKey = columns  
```  
  
```csharp  
workTable.PrimaryKey = new DataColumn[] {workTable.Columns["CustID"]};  
  
// Or  
  
DataColumn[] columns = new DataColumn[1];  
columns[0] = workTable.Columns["CustID"];  
workTable.PrimaryKey = columns;  
```  
  
 <span data-ttu-id="8d281-110">下面的示例将两列定义为主键。</span><span class="sxs-lookup"><span data-stu-id="8d281-110">The following example defines two columns as a primary key.</span></span>  
  
```vb  
workTable.PrimaryKey = New DataColumn() {workTable.Columns("CustLName"), _  
                                         workTable.Columns("CustFName")}  
  
' Or  
  
Dim keyColumn(2) As DataColumn  
keyColumn(0) = workTable.Columns("CustLName")  
keyColumn(1) = workTable.Columns("CustFName")  
workTable.PrimaryKey = keyColumn  
```  
  
```csharp  
workTable.PrimaryKey = new DataColumn[] {workTable.Columns["CustLName"],
                                         workTable.Columns["CustFName"]};  
  
// Or  
  
DataColumn[] keyColumn = new DataColumn[2];  
keyColumn[0] = workTable.Columns["CustLName"];  
keyColumn[1] = workTable.Columns["CustFName"];  
workTable.PrimaryKey = keyColumn;  
```  
  
## <a name="see-also"></a><span data-ttu-id="8d281-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d281-111">See also</span></span>

- <xref:System.Data.DataTable>
- [<span data-ttu-id="8d281-112">数据表架构定义</span><span class="sxs-lookup"><span data-stu-id="8d281-112">DataTable Schema Definition</span></span>](datatable-schema-definition.md)
- [<span data-ttu-id="8d281-113">DataTables</span><span class="sxs-lookup"><span data-stu-id="8d281-113">DataTables</span></span>](datatables.md)
- [<span data-ttu-id="8d281-114">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="8d281-114">ADO.NET Overview</span></span>](../ado-net-overview.md)

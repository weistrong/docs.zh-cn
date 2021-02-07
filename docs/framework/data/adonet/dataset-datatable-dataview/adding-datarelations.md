---
description: 了解详细信息：添加 Datarelation
title: 添加 DataRelation
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a4a564fb-c1c4-4135-b6c2-b030e51195e4
ms.openlocfilehash: 56438c9b69fab71c4843582b6cfea50fa057eb44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725215"
---
# <a name="adding-datarelations"></a><span data-ttu-id="f9dfa-103">添加 DataRelation</span><span class="sxs-lookup"><span data-stu-id="f9dfa-103">Adding DataRelations</span></span>

<span data-ttu-id="f9dfa-104">在包含多个 <xref:System.Data.DataSet> 对象的 <xref:System.Data.DataTable> 中，可以使用 <xref:System.Data.DataRelation> 对象来使一个表与另一个表相关，在多个表之间导航，以及从相关表中返回子行或父行。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-104">In a <xref:System.Data.DataSet> with multiple <xref:System.Data.DataTable> objects, you can use <xref:System.Data.DataRelation> objects to relate one table to another, to navigate through the tables, and to return child or parent rows from a related table.</span></span>  
  
 <span data-ttu-id="f9dfa-105">创建 **datarelation** 所需的参数是要创建的 **datarelation** 的名称以及 <xref:System.Data.DataColumn> 对用作关系中父列和子列的列的一个或多个引用的数组。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-105">The arguments required to create a **DataRelation** are a name for the **DataRelation** being created, and an array of one or more <xref:System.Data.DataColumn> references to the columns that serve as the parent and child columns in the relationship.</span></span> <span data-ttu-id="f9dfa-106">创建 **DataRelation** 后，可以使用它在表之间导航和检索值。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-106">After you have created a **DataRelation**, you can use it to navigate between tables and to retrieve values.</span></span>  
  
 <span data-ttu-id="f9dfa-107">默认情况下，将 **DataRelation** 添加到将向 <xref:System.Data.DataSet> <xref:System.Data.UniqueConstraint> 父表和 <xref:System.Data.ForeignKeyConstraint> 子表添加。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-107">Adding a **DataRelation** to a <xref:System.Data.DataSet> adds, by default, a <xref:System.Data.UniqueConstraint> to the parent table and a <xref:System.Data.ForeignKeyConstraint> to the child table.</span></span> <span data-ttu-id="f9dfa-108">有关这些默认约束的详细信息，请参阅 [DataTable 约束](datatable-constraints.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-108">For more information about these default constraints, see [DataTable Constraints](datatable-constraints.md).</span></span>  
  
 <span data-ttu-id="f9dfa-109">下面的代码示例使用中的两个对象创建 **DataRelation** <xref:System.Data.DataTable> <xref:System.Data.DataSet> 。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-109">The following code example creates a **DataRelation** using two <xref:System.Data.DataTable> objects in a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="f9dfa-110">每个都 <xref:System.Data.DataTable> 包含一个名为 **CustID** 的列，它用作两个对象之间的链接 <xref:System.Data.DataTable> 。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-110">Each <xref:System.Data.DataTable> contains a column named **CustID**, which serves as a link between the two <xref:System.Data.DataTable> objects.</span></span> <span data-ttu-id="f9dfa-111">该示例将一个 **DataRelation** 添加到的 **关系** 集合 <xref:System.Data.DataSet> 。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-111">The example adds a single **DataRelation** to the **Relations** collection of the <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="f9dfa-112">该示例中的第一个参数指定所创建的 **DataRelation** 的名称。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-112">The first argument in the example specifies the name of the **DataRelation** being created.</span></span> <span data-ttu-id="f9dfa-113">第二个参数设置父 **datacolumn** ，第三个参数设置子 **datacolumn**。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-113">The second argument sets the parent **DataColumn** and the third argument sets the child **DataColumn**.</span></span>  
  
```vb  
customerOrders.Relations.Add("CustOrders", _  
  customerOrders.Tables("Customers").Columns("CustID"), _  
  customerOrders.Tables("Orders").Columns("CustID"))  
```  
  
```csharp  
customerOrders.Relations.Add("CustOrders",  
  customerOrders.Tables["Customers"].Columns["CustID"],  
  customerOrders.Tables["Orders"].Columns["CustID"]);  
```  
  
 <span data-ttu-id="f9dfa-114">**DataRelation** 还具有一个 **嵌套** 属性，当设置为 **true** 时，将导致子表中的行嵌套在使用编写为 XML 元素的父表中的关联行内 <xref:System.Data.DataSet.WriteXml%2A> 。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-114">A **DataRelation** also has a **Nested** property which, when set to **true**, causes the rows from the child table to be nested within the associated row from the parent table when written as XML elements using <xref:System.Data.DataSet.WriteXml%2A> .</span></span> <span data-ttu-id="f9dfa-115">有关详细信息，请参阅[在数据集中使用 XML](using-xml-in-a-dataset.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dfa-115">For more information, see [Using XML in a DataSet](using-xml-in-a-dataset.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9dfa-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9dfa-116">See also</span></span>

- [<span data-ttu-id="f9dfa-117">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="f9dfa-117">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="f9dfa-118">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="f9dfa-118">ADO.NET Overview</span></span>](../ado-net-overview.md)

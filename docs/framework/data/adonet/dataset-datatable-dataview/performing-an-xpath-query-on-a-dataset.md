---
description: 了解详细信息：对数据集执行 XPath 查询
title: 对数据集执行 XPath 查询
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7e828566-fffe-4d38-abb2-4d68fd73f663
ms.openlocfilehash: 9febcc545f86f048b2d693f8aa6558a1b7883a60
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651712"
---
# <a name="performing-an-xpath-query-on-a-dataset"></a><span data-ttu-id="a1a32-103">对数据集执行 XPath 查询</span><span class="sxs-lookup"><span data-stu-id="a1a32-103">Performing an XPath Query on a DataSet</span></span>

<span data-ttu-id="a1a32-104">同步与之间的关系 <xref:System.Data.DataSet> <xref:System.Xml.XmlDataDocument> 使你可以使用 xml 服务（例如 Xml 路径语言 (XPath) query）访问 **XmlDataDocument** ，并且可以比直接访问 **DataSet** 更方便地执行某些功能。</span><span class="sxs-lookup"><span data-stu-id="a1a32-104">The relationship between a synchronized <xref:System.Data.DataSet> and <xref:System.Xml.XmlDataDocument> allows you to make use of XML services, such as the XML Path Language (XPath) query, that access the **XmlDataDocument** and can perform certain functionality more conveniently than accessing the **DataSet** directly.</span></span> <span data-ttu-id="a1a32-105">例如，您可以对与数据集同步的 XmlDataDocument 执行 XPath 查询，而不是使用的 **Select** 方法 <xref:System.Data.DataTable> 将关系导航到 **dataset** 中的其他表，以获取形式为的 XML 元素列表 <xref:System.Xml.XmlNodeList> 。</span><span class="sxs-lookup"><span data-stu-id="a1a32-105">For example, rather than using the **Select** method of a <xref:System.Data.DataTable> to navigate relationships to other tables in a **DataSet**, you can perform an XPath query on an **XmlDataDocument** that is synchronized with the **DataSet**, to get a list of XML elements in the form of an <xref:System.Xml.XmlNodeList>.</span></span> <span data-ttu-id="a1a32-106">然后，将 **XmlNodeList** 中的节点强制转换为节点，并将其 <xref:System.Xml.XmlElement> 传递给 **XmlDataDocument** 的 **GetRowFromElement** 方法，以返回 <xref:System.Data.DataRow> 对同步 **数据集中** 的表的行的匹配引用。</span><span class="sxs-lookup"><span data-stu-id="a1a32-106">The nodes in the **XmlNodeList**, cast as <xref:System.Xml.XmlElement> nodes, can then be passed to the **GetRowFromElement** method of the **XmlDataDocument**, to return matching <xref:System.Data.DataRow> references to the rows of the table in the synchronized **DataSet**.</span></span>  
  
 <span data-ttu-id="a1a32-107">例如，以下代码示例执行“孙级”XPath 查询。</span><span class="sxs-lookup"><span data-stu-id="a1a32-107">For example, the following code sample performs a "grandchild" XPath query.</span></span> <span data-ttu-id="a1a32-108">**数据集** 填充了三个表： **Customers**、 **Orders** 和 **OrderDetails**。</span><span class="sxs-lookup"><span data-stu-id="a1a32-108">The **DataSet** is filled with three tables: **Customers**, **Orders**, and **OrderDetails**.</span></span> <span data-ttu-id="a1a32-109">在此示例中，首先在 **Customers** 表和 **orders** 表之间以及 **orders** 表和 **OrderDetails** 表之间创建父子关系。</span><span class="sxs-lookup"><span data-stu-id="a1a32-109">In the sample, a parent-child relation is first created between the **Customers** and **Orders** tables, and between the **Orders** and **OrderDetails** tables.</span></span> <span data-ttu-id="a1a32-110">然后，执行 XPath 查询来返回 **XmlNodeList** 的 **客户** 节点，其中孙 **OrderDetails** 节点的 **ProductID** 节点的值为43。</span><span class="sxs-lookup"><span data-stu-id="a1a32-110">An XPath query is then performed to return an **XmlNodeList** of **Customers** nodes where a grandchild **OrderDetails** node has a **ProductID** node with the value of 43.</span></span> <span data-ttu-id="a1a32-111">实质上，该示例使用 XPath 查询来确定哪些客户订购了 **ProductID** 为43的产品。</span><span class="sxs-lookup"><span data-stu-id="a1a32-111">In essence, the sample is using the XPath query to determine which customers have ordered the product that has the **ProductID** of 43.</span></span>  
  
```vb  
' Assumes that connection is a valid SqlConnection.  
connection.Open()  
Dim dataSet As DataSet = New DataSet("CustomerOrders")  
Dim customerAdapter As SqlDataAdapter = New SqlDataAdapter( _  
  "SELECT * FROM Customers", connection)  
customerAdapter.Fill(dataSet, "Customers")  
  
Dim orderAdapter As SqlDataAdapter = New SqlDataAdapter( _  
  "SELECT * FROM Orders", connection)  
orderAdapter.Fill(dataSet, "Orders")  
  
Dim detailAdapter As SqlDataAdapter = New SqlDataAdapter( _  
  "SELECT * FROM [Order Details]", connection)  
detailAdapter.Fill(dataSet, "OrderDetails")  
  
connection.Close()  
  
dataSet.Relations.Add("CustOrders", _  
dataSet.Tables("Customers").Columns("CustomerID"), _  
dataSet.Tables("Orders").Columns("CustomerID")).Nested = true  
  
dataSet.Relations.Add("OrderDetail", _  
  dataSet.Tables("Orders").Columns("OrderID"), _  
dataSet.Tables("OrderDetails").Columns("OrderID"), false).Nested = true  
  
Dim xmlDoc As XmlDataDocument = New XmlDataDocument(dataSet)
  
Dim nodeList As XmlNodeList = xmlDoc.DocumentElement.SelectNodes( _  
  "descendant::Customers[*/OrderDetails/ProductID=43]")  
  
Dim dataRow As DataRow  
Dim xmlNode As XmlNode  
  
For Each xmlNode In nodeList  
  dataRow = xmlDoc.GetRowFromElement(CType(xmlNode, XmlElement))  
  
  If Not dataRow Is Nothing then Console.WriteLine(xmlRow(0).ToString())  
Next  
```  
  
```csharp  
// Assumes that connection is a valid SqlConnection.  
connection.Open();  
  
DataSet dataSet = new DataSet("CustomerOrders");  
  
SqlDataAdapter customerAdapter = new SqlDataAdapter(  
  "SELECT * FROM Customers", connection);  
customerAdapter.Fill(dataSet, "Customers");  
  
SqlDataAdapter orderAdapter = new SqlDataAdapter(  
  "SELECT * FROM Orders", connection);  
orderAdapter.Fill(dataSet, "Orders");  
  
SqlDataAdapter detailAdapter = new SqlDataAdapter(  
  "SELECT * FROM [Order Details]", connection);  
detailAdapter.Fill(dataSet, "OrderDetails");  
  
connection.Close();  
  
dataSet.Relations.Add("CustOrders",  
  dataSet.Tables["Customers"].Columns["CustomerID"],  
 dataSet.Tables["Orders"].Columns["CustomerID"]).Nested = true;  
  
dataSet.Relations.Add("OrderDetail",  
  dataSet.Tables["Orders"].Columns["OrderID"],  
  dataSet.Tables["OrderDetails"].Columns["OrderID"],
  false).Nested = true;  
  
XmlDataDocument xmlDoc = new XmlDataDocument(dataSet);
  
XmlNodeList nodeList = xmlDoc.DocumentElement.SelectNodes(  
  "descendant::Customers[*/OrderDetails/ProductID=43]");  
  
DataRow dataRow;  
foreach (XmlNode xmlNode in nodeList)  
{  
  dataRow = xmlDoc.GetRowFromElement((XmlElement)xmlNode);  
  if (dataRow != null)  
    Console.WriteLine(dataRow[0]);  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="a1a32-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1a32-112">See also</span></span>

- [<span data-ttu-id="a1a32-113">数据集和 XmlDataDocument 同步</span><span class="sxs-lookup"><span data-stu-id="a1a32-113">DataSet and XmlDataDocument Synchronization</span></span>](dataset-and-xmldatadocument-synchronization.md)
- [<span data-ttu-id="a1a32-114">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="a1a32-114">ADO.NET Overview</span></span>](../ado-net-overview.md)

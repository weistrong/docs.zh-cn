---
description: 了解详细信息：以 XSD 形式编写数据集架构信息
title: 写入数据集架构信息作为 XSD
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4e530831-695e-49ff-8f0b-e5b0c526b8eb
ms.openlocfilehash: e05188c74ca21e73ee5151da817e143102640a13
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651348"
---
# <a name="writing-dataset-schema-information-as-xsd"></a><span data-ttu-id="b33b7-103">写入数据集架构信息作为 XSD</span><span class="sxs-lookup"><span data-stu-id="b33b7-103">Writing DataSet Schema Information as XSD</span></span>

<span data-ttu-id="b33b7-104">您可以用 XML 架构定义语言 (XSD) 架构的形式来编写 <xref:System.Data.DataSet> 的架构，以便在 XML 文档中传输包含或不包含相关数据的架构。</span><span class="sxs-lookup"><span data-stu-id="b33b7-104">You can write the schema of a <xref:System.Data.DataSet> as XML Schema definition language (XSD) schema, so that you can transport it, with or without related data, in an XML document.</span></span> <span data-ttu-id="b33b7-105">XML 架构可以写入文件、流、 <xref:System.Xml.XmlWriter> 或字符串; 它可用于生成强类型化 **数据集**。</span><span class="sxs-lookup"><span data-stu-id="b33b7-105">XML Schema can be written to a file, a stream, an <xref:System.Xml.XmlWriter>, or a string; it is useful for generating a strongly typed **DataSet**.</span></span> <span data-ttu-id="b33b7-106">有关强类型化 **数据集** 对象的详细信息，请参阅 [类型化数据集](typed-datasets.md)。</span><span class="sxs-lookup"><span data-stu-id="b33b7-106">For more information about strongly typed **DataSet** objects, see [Typed DataSets](typed-datasets.md).</span></span>  
  
 <span data-ttu-id="b33b7-107">您可以使用对象的 **ColumnMapping** 属性来指定如何在 XML 架构中表示表的列 <xref:System.Data.DataColumn> 。</span><span class="sxs-lookup"><span data-stu-id="b33b7-107">You can specify how a column of a table is represented in XML Schema using the **ColumnMapping** property of the <xref:System.Data.DataColumn> object.</span></span> <span data-ttu-id="b33b7-108">有关详细信息，请参阅以 [Xml 数据形式编写数据集内容](writing-dataset-contents-as-xml-data.md)中的 "将列映射到 xml 元素、属性和文本"。</span><span class="sxs-lookup"><span data-stu-id="b33b7-108">For more information, see "Mapping Columns to XML Elements, Attributes, and Text" in [Writing DataSet Contents as XML Data](writing-dataset-contents-as-xml-data.md).</span></span>  
  
 <span data-ttu-id="b33b7-109">若要将 **数据集** 的架构作为 XML 架构写入文件、流或 **XmlWriter**，请使用 **DataSet** 的 **WriteXmlSchema** 方法。</span><span class="sxs-lookup"><span data-stu-id="b33b7-109">To write the schema of a **DataSet** as XML Schema, to a file, stream, or **XmlWriter**, use the **WriteXmlSchema** method of the **DataSet**.</span></span> <span data-ttu-id="b33b7-110">**WriteXmlSchema** 使用一个参数来指定生成的 XML 架构的目标。</span><span class="sxs-lookup"><span data-stu-id="b33b7-110">**WriteXmlSchema** takes one parameter that specifies the destination of the resulting XML Schema.</span></span> <span data-ttu-id="b33b7-111">下面的代码示例演示如何通过传递包含文件名和对象的字符串，将 **数据集** 的 XML 架构写入文件 <xref:System.IO.StreamWriter> 。</span><span class="sxs-lookup"><span data-stu-id="b33b7-111">The following code examples demonstrate how to write the XML Schema of a **DataSet** to a file by passing a string containing a file name and a <xref:System.IO.StreamWriter> object.</span></span>  
  
```vb  
dataSet.WriteXmlSchema("Customers.xsd")  
```  
  
```csharp  
dataSet.WriteXmlSchema("Customers.xsd");  
```  
  
```vb  
Dim writer As System.IO.StreamWriter = New System.IO.StreamWriter("Customers.xsd")  
dataSet.WriteXmlSchema(writer)  
writer.Close()  
```  
  
```csharp  
System.IO.StreamWriter writer = new System.IO.StreamWriter("Customers.xsd");  
dataSet.WriteXmlSchema(writer);  
writer.Close();  
```  
  
 <span data-ttu-id="b33b7-112">若要获取 **数据集** 的架构并将其作为 XML 架构字符串写入，请使用 **GetXmlSchema** 方法，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="b33b7-112">To obtain the schema of a **DataSet** and write it as an XML Schema string, use the **GetXmlSchema** method, as shown in the following example.</span></span>  
  
```vb  
Dim schemaString As String = dataSet.GetXmlSchema()  
```  
  
```csharp  
string schemaString = dataSet.GetXmlSchema();  
```  
  
## <a name="see-also"></a><span data-ttu-id="b33b7-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="b33b7-113">See also</span></span>

- [<span data-ttu-id="b33b7-114">在数据集中使用 XML</span><span class="sxs-lookup"><span data-stu-id="b33b7-114">Using XML in a DataSet</span></span>](using-xml-in-a-dataset.md)
- [<span data-ttu-id="b33b7-115">写入数据集内容作为 XML 数据</span><span class="sxs-lookup"><span data-stu-id="b33b7-115">Writing DataSet Contents as XML Data</span></span>](writing-dataset-contents-as-xml-data.md)
- [<span data-ttu-id="b33b7-116">类型化数据集</span><span class="sxs-lookup"><span data-stu-id="b33b7-116">Typed DataSets</span></span>](typed-datasets.md)
- [<span data-ttu-id="b33b7-117">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="b33b7-117">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="b33b7-118">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="b33b7-118">ADO.NET Overview</span></span>](../ado-net-overview.md)

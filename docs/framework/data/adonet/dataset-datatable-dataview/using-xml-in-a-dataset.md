---
description: 了解详细信息：在数据集中使用 XML
title: 在数据集中使用 XML
ms.date: 03/30/2017
ms.assetid: 35138159-e199-49ec-baf7-1ec6777e171e
ms.openlocfilehash: 5c4216fce9c1512c95da8e27a622ba228411b641
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651413"
---
# <a name="using-xml-in-a-dataset"></a><span data-ttu-id="f90c5-103">在数据集中使用 XML</span><span class="sxs-lookup"><span data-stu-id="f90c5-103">Using XML in a DataSet</span></span>

<span data-ttu-id="f90c5-104">通过 ADO.NET，您可以从 XML 流或文档填充 <xref:System.Data.DataSet>。</span><span class="sxs-lookup"><span data-stu-id="f90c5-104">With ADO.NET you can fill a <xref:System.Data.DataSet> from an XML stream or document.</span></span> <span data-ttu-id="f90c5-105">可以使用 XML 流或文档向 <xref:System.Data.DataSet> 提供数据和/或架构信息。</span><span class="sxs-lookup"><span data-stu-id="f90c5-105">You can use the XML stream or document to supply to the <xref:System.Data.DataSet> either data, schema information, or both.</span></span> <span data-ttu-id="f90c5-106">从 XML 流或文档中提供的信息可以与已存在于 <xref:System.Data.DataSet> 中的现有数据或架构信息进行组合。</span><span class="sxs-lookup"><span data-stu-id="f90c5-106">The information supplied from the XML stream or document can be combined with existing data or schema information already present in the <xref:System.Data.DataSet>.</span></span>  
  
 <span data-ttu-id="f90c5-107">为了通过 HTTP 将 <xref:System.Data.DataSet> 传输给其他应用程序或启用了 XML 的平台来使用，ADO.NET 还允许您创建 <xref:System.Data.DataSet> 的 XML 表示形式（包含或不包含架构）。</span><span class="sxs-lookup"><span data-stu-id="f90c5-107">ADO.NET also allows you to create an XML representation of a <xref:System.Data.DataSet>, with or without its schema, in order to transport the <xref:System.Data.DataSet> across HTTP for use by another application or XML-enabled platform.</span></span> <span data-ttu-id="f90c5-108">在 <xref:System.Data.DataSet> 的 XML 表示形式中，数据以 XML 形式编写，而架构若以内联形式包含在该表示形式中时，则使用 XML 架构定义语言 (XSD) 来编写。</span><span class="sxs-lookup"><span data-stu-id="f90c5-108">In an XML representation of a <xref:System.Data.DataSet>, the data is written in XML and the schema, if it is included inline in the representation, is written using the XML Schema definition language (XSD).</span></span> <span data-ttu-id="f90c5-109">XML 和 XML 架构提供一种方便的格式与远程客户端之间来回传输 <xref:System.Data.DataSet> 的内容。</span><span class="sxs-lookup"><span data-stu-id="f90c5-109">XML and XML Schema provide a convenient format for transferring the contents of a <xref:System.Data.DataSet> to and from remote clients.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f90c5-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="f90c5-110">In This Section</span></span>  

 [<span data-ttu-id="f90c5-111">DiffGrams</span><span class="sxs-lookup"><span data-stu-id="f90c5-111">DiffGrams</span></span>](diffgrams.md)  
 <span data-ttu-id="f90c5-112">提供有关 DiffGram 的详细信息，DiffGram 是一种用于读写 <xref:System.Data.DataSet> 内容的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="f90c5-112">Provides details on the DiffGram, an XML format used to read and write the contents of a <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="f90c5-113">从 XML 加载数据集</span><span class="sxs-lookup"><span data-stu-id="f90c5-113">Loading a DataSet from XML</span></span>](loading-a-dataset-from-xml.md)  
 <span data-ttu-id="f90c5-114">讨论在从 XML 文档中加载 <xref:System.Data.DataSet> 内容时需考虑的不同选项。</span><span class="sxs-lookup"><span data-stu-id="f90c5-114">Discusses different options to consider when loading the contents of a <xref:System.Data.DataSet> from an XML document.</span></span>  
  
 [<span data-ttu-id="f90c5-115">写入数据集内容作为 XML 数据</span><span class="sxs-lookup"><span data-stu-id="f90c5-115">Writing DataSet Contents as XML Data</span></span>](writing-dataset-contents-as-xml-data.md)  
 <span data-ttu-id="f90c5-116">讨论如何以 XML 数据的形式生成 <xref:System.Data.DataSet> 的内容以及可使用的不同 XML 格式选项。</span><span class="sxs-lookup"><span data-stu-id="f90c5-116">Discusses how to generate the contents of a <xref:System.Data.DataSet> as XML data, and the different XML format options you can use.</span></span>  
  
 [<span data-ttu-id="f90c5-117">从 XML 加载数据集架构信息</span><span class="sxs-lookup"><span data-stu-id="f90c5-117">Loading DataSet Schema Information from XML</span></span>](loading-dataset-schema-information-from-xml.md)  
 <span data-ttu-id="f90c5-118">讨论用于从 XML 中加载 <xref:System.Data.DataSet> 架构的 <xref:System.Data.DataSet> 方法。</span><span class="sxs-lookup"><span data-stu-id="f90c5-118">Discusses the <xref:System.Data.DataSet> methods used to load the schema of a <xref:System.Data.DataSet> from XML.</span></span>  
  
 [<span data-ttu-id="f90c5-119">写入数据集架构信息作为 XSD</span><span class="sxs-lookup"><span data-stu-id="f90c5-119">Writing DataSet Schema Information as XSD</span></span>](writing-dataset-schema-information-as-xsd.md)  
 <span data-ttu-id="f90c5-120">讨论 XML 架构的用途以及如何从 <xref:System.Data.DataSet> 生成 XML 架构。</span><span class="sxs-lookup"><span data-stu-id="f90c5-120">Discusses the uses for an XML Schema and how to generate one from a <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="f90c5-121">数据集和 XmlDataDocument 同步</span><span class="sxs-lookup"><span data-stu-id="f90c5-121">DataSet and XmlDataDocument Synchronization</span></span>](dataset-and-xmldatadocument-synchronization.md)  
 <span data-ttu-id="f90c5-122">讨论 .NET Framework 中提供的同步访问单个数据集的关系和分层视图的功能，并解释如何在 <xref:System.Data.DataSet> 和 <xref:System.Xml.XmlDataDocument> 之间创建同步关系。</span><span class="sxs-lookup"><span data-stu-id="f90c5-122">Discusses the capability available in the .NET Framework of synchronous access to both relational and hierarchical views of a single set of data, and shows how to create a synchronous relationship between a <xref:System.Data.DataSet> and an <xref:System.Xml.XmlDataDocument>.</span></span>  
  
 [<span data-ttu-id="f90c5-123">嵌套 DataRelation</span><span class="sxs-lookup"><span data-stu-id="f90c5-123">Nesting DataRelations</span></span>](nesting-datarelations.md)  
 <span data-ttu-id="f90c5-124">讨论嵌套 <xref:System.Data.DataRelation> 对象在以 XML 数据形式表示 <xref:System.Data.DataSet> 内容时的重要性，并描述如何创建这些对象。</span><span class="sxs-lookup"><span data-stu-id="f90c5-124">Discusses the importance of nested <xref:System.Data.DataRelation> objects when representing the contents of a <xref:System.Data.DataSet> as XML data, and describes how to create them.</span></span>  
  
 [<span data-ttu-id="f90c5-125">从 XML 架构派生数据集关系结构 (XSD)</span><span class="sxs-lookup"><span data-stu-id="f90c5-125">Deriving DataSet Relational Structure from XML Schema (XSD)</span></span>](deriving-dataset-relational-structure-from-xml-schema-xsd.md)  
 <span data-ttu-id="f90c5-126">描述从 XML 架构创建的 <xref:System.Data.DataSet> 的关系结果（即架构）。</span><span class="sxs-lookup"><span data-stu-id="f90c5-126">Describes the relational structure, or schema, of a <xref:System.Data.DataSet> that is created from XML Schema.</span></span>  
  
 [<span data-ttu-id="f90c5-127">从 XML 推断数据集关系结构</span><span class="sxs-lookup"><span data-stu-id="f90c5-127">Inferring DataSet Relational Structure from XML</span></span>](inferring-dataset-relational-structure-from-xml.md)  
 <span data-ttu-id="f90c5-128">描述在从 XML 元素进行推断时所创建的 <xref:System.Data.DataSet> 的结果关系结构（即架构）。</span><span class="sxs-lookup"><span data-stu-id="f90c5-128">Describes the resulting relational structure, or schema, of a <xref:System.Data.DataSet> that is created when inferred from XML elements.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="f90c5-129">相关章节</span><span class="sxs-lookup"><span data-stu-id="f90c5-129">Related Sections</span></span>  

 [<span data-ttu-id="f90c5-130">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="f90c5-130">ADO.NET Overview</span></span>](../ado-net-overview.md)  
 <span data-ttu-id="f90c5-131">描述 ADO.NET 结构和组件，并说明如何使用它们来访问现有的数据源和管理应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="f90c5-131">Describes the ADO.NET architecture and components, and how to use them to access existing data sources as well as to manage application data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f90c5-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="f90c5-132">See also</span></span>

- [<span data-ttu-id="f90c5-133">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="f90c5-133">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="f90c5-134">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="f90c5-134">ADO.NET Overview</span></span>](../ado-net-overview.md)

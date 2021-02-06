---
description: 了解详细信息：从 XML 推断数据集关系结构
title: 从 XML 推断数据集关系结构
ms.date: 03/30/2017
ms.assetid: cd2f41c6-6785-420e-aa43-3ceb0bdccdce
ms.openlocfilehash: d89b6a42e7e1bc3d7514f180329e9c1d877a67ef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652219"
---
# <a name="inferring-dataset-relational-structure-from-xml"></a><span data-ttu-id="e8492-103">从 XML 推断数据集关系结构</span><span class="sxs-lookup"><span data-stu-id="e8492-103">Inferring DataSet Relational Structure from XML</span></span>

<span data-ttu-id="e8492-104"><xref:System.Data.DataSet> 的关系结构（即架构）由表、列、约束和关系组成。</span><span class="sxs-lookup"><span data-stu-id="e8492-104">The relational structure, or schema, of a <xref:System.Data.DataSet> is made up of tables, columns, constraints, and relations.</span></span> <span data-ttu-id="e8492-105">当从 XML 中加载 <xref:System.Data.DataSet> 时，可以预定义架构，也可以从所加载的 XML 显式（或通过推断）创建架构。</span><span class="sxs-lookup"><span data-stu-id="e8492-105">When loading a <xref:System.Data.DataSet> from XML, the schema can be predefined, or it can be created, either explicitly or through inference, from the XML being loaded.</span></span> <span data-ttu-id="e8492-106">有关从 xml 加载的架构和内容的详细信息 <xref:System.Data.DataSet> ，请参阅从 Xml [加载数据集](loading-a-dataset-from-xml.md) 和 [从 Xml 加载数据集架构信息](loading-dataset-schema-information-from-xml.md)。</span><span class="sxs-lookup"><span data-stu-id="e8492-106">For more information about loading the schema and contents of a <xref:System.Data.DataSet> from XML, see [Loading a DataSet from XML](loading-a-dataset-from-xml.md) and [Loading DataSet Schema Information from XML](loading-dataset-schema-information-from-xml.md).</span></span>  
  
 <span data-ttu-id="e8492-107">如果 <xref:System.Data.DataSet> 是从 xml 创建的架构，首选方法是使用 Xml 架构定义语言 (xsd) 来显式指定架构 (如 [从 Xml 架构派生数据集关系结构 (xsd) ](deriving-dataset-relational-structure-from-xml-schema-xsd.md)) 或 XML-Data 减小了 XDR (。</span><span class="sxs-lookup"><span data-stu-id="e8492-107">If the schema of a <xref:System.Data.DataSet> is being created from XML, the preferred method is to explicitly specify the schema using either the XML Schema definition language (XSD) (as described in [Deriving DataSet Relational Structure from XML Schema (XSD)](deriving-dataset-relational-structure-from-xml-schema-xsd.md)) or the XML-Data Reduced (XDR).</span></span> <span data-ttu-id="e8492-108">如果 XML 中没有可用的 XML 架构或 XDR 架构，则可以从 XML 元素和属性的结构推断 <xref:System.Data.DataSet> 的架构。</span><span class="sxs-lookup"><span data-stu-id="e8492-108">If no XML Schema or XDR schema is available in the XML, the schema of the <xref:System.Data.DataSet> can be inferred from the structure of the XML elements and attributes.</span></span>  
  
 <span data-ttu-id="e8492-109">本节通过显示 XML 元素和属性及其结构以及生成的推断 <xref:System.Data.DataSet> 架构来描述推断 <xref:System.Data.DataSet> 架构的规则。</span><span class="sxs-lookup"><span data-stu-id="e8492-109">This section describes the rules for <xref:System.Data.DataSet> schema inference by showing XML elements and attributes and their structure, and the resulting inferred <xref:System.Data.DataSet> schema.</span></span>  
  
 <span data-ttu-id="e8492-110">并非所有出现在 XML 文档中的属性都应包含在推断过程中。</span><span class="sxs-lookup"><span data-stu-id="e8492-110">Not all attributes present in an XML document should be included in the inference process.</span></span> <span data-ttu-id="e8492-111">由命名空间限定的属性可以包含对 XML 文档重要但对 <xref:System.Data.DataSet> 架构不重要的元数据。</span><span class="sxs-lookup"><span data-stu-id="e8492-111">Namespace-qualified attributes can include metadata that is important for the XML document but not for the <xref:System.Data.DataSet> schema.</span></span> <span data-ttu-id="e8492-112">使用 <xref:System.Data.DataSet.InferXmlSchema%2A>，您可以指定要在推断过程中忽略的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e8492-112">Using <xref:System.Data.DataSet.InferXmlSchema%2A>, you can specify namespaces to be ignored during the inference process.</span></span> <span data-ttu-id="e8492-113">有关详细信息，请参阅 [从 XML 加载数据集架构信息](loading-dataset-schema-information-from-xml.md)。</span><span class="sxs-lookup"><span data-stu-id="e8492-113">For more information, see [Loading DataSet Schema Information from XML](loading-dataset-schema-information-from-xml.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e8492-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="e8492-114">In This Section</span></span>  

 [<span data-ttu-id="e8492-115">数据集架构接口过程摘要</span><span class="sxs-lookup"><span data-stu-id="e8492-115">Summary of the DataSet Schema Inference Process</span></span>](summary-of-the-dataset-schema-inference-process.md)  
 <span data-ttu-id="e8492-116">提供从 XML 推断 <xref:System.Data.DataSet> 架构的规则的简要概述。</span><span class="sxs-lookup"><span data-stu-id="e8492-116">Provides a high-level summary of the rules for inferring the schema of a <xref:System.Data.DataSet> from XML.</span></span>  
  
 [<span data-ttu-id="e8492-117">推断表</span><span class="sxs-lookup"><span data-stu-id="e8492-117">Inferring Tables</span></span>](inferring-tables.md)  
 <span data-ttu-id="e8492-118">描述被推断为 <xref:System.Data.DataSet> 中的表的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="e8492-118">Describes the XML elements that are inferred as tables in a <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="e8492-119">推断列</span><span class="sxs-lookup"><span data-stu-id="e8492-119">Inferring Columns</span></span>](inferring-columns.md)  
 <span data-ttu-id="e8492-120">描述被推断为表列的 XML 元素和属性。</span><span class="sxs-lookup"><span data-stu-id="e8492-120">Describes the XML elements and attributes that are inferred as table columns.</span></span>  
  
 [<span data-ttu-id="e8492-121">推断关系</span><span class="sxs-lookup"><span data-stu-id="e8492-121">Inferring Relationships</span></span>](inferring-relationships.md)  
 <span data-ttu-id="e8492-122">描述为嵌套的推断表创建的 <xref:System.Data.DataRelation> 和 <xref:System.Data.ForeignKeyConstraint> 对象。</span><span class="sxs-lookup"><span data-stu-id="e8492-122">Describes the <xref:System.Data.DataRelation> and <xref:System.Data.ForeignKeyConstraint> objects created for nested, inferred tables.</span></span>  
  
 [<span data-ttu-id="e8492-123">推断元素文本</span><span class="sxs-lookup"><span data-stu-id="e8492-123">Inferring Element Text</span></span>](inferring-element-text.md)  
 <span data-ttu-id="e8492-124">描述为 XML 元素中的文本创建的列，并解释何时会忽略 XML 元素中的文本。</span><span class="sxs-lookup"><span data-stu-id="e8492-124">Describes the columns that are created for text in XML elements, and explains when text in XML elements is ignored.</span></span>  
  
 [<span data-ttu-id="e8492-125">推断限制</span><span class="sxs-lookup"><span data-stu-id="e8492-125">Inference Limitations</span></span>](inference-limitations.md)  
 <span data-ttu-id="e8492-126">讨论架构推断的限制。</span><span class="sxs-lookup"><span data-stu-id="e8492-126">Discusses the limitations of schema inference.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="e8492-127">相关章节</span><span class="sxs-lookup"><span data-stu-id="e8492-127">Related Sections</span></span>  

 [<span data-ttu-id="e8492-128">在数据集中使用 XML</span><span class="sxs-lookup"><span data-stu-id="e8492-128">Using XML in a DataSet</span></span>](using-xml-in-a-dataset.md)  
 <span data-ttu-id="e8492-129">描述 <xref:System.Data.DataSet> 对象如何与 XML 数据进行交互。</span><span class="sxs-lookup"><span data-stu-id="e8492-129">Describes how the <xref:System.Data.DataSet> object interacts with XML data.</span></span>  
  
 [<span data-ttu-id="e8492-130">从 XML 架构派生数据集关系结构 (XSD)</span><span class="sxs-lookup"><span data-stu-id="e8492-130">Deriving DataSet Relational Structure from XML Schema (XSD)</span></span>](deriving-dataset-relational-structure-from-xml-schema-xsd.md)  
 <span data-ttu-id="e8492-131">描述从 XML 架构定义语言 (XSD) 架构创建的 <xref:System.Data.DataSet> 的关系结构（即架构）。</span><span class="sxs-lookup"><span data-stu-id="e8492-131">Describes the relational structure, or schema, of a <xref:System.Data.DataSet> that is created from XML Schema definition language (XSD) schema.</span></span>  
  
 [<span data-ttu-id="e8492-132">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="e8492-132">ADO.NET Overview</span></span>](../ado-net-overview.md)  
 <span data-ttu-id="e8492-133">描述 ADO.NET 结构和组件，并说明如何用来访问现有的数据源和管理应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="e8492-133">Describes the ADO.NET architecture and components and how to use them to access existing data sources and manage application data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8492-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="e8492-134">See also</span></span>

- [<span data-ttu-id="e8492-135">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="e8492-135">ADO.NET Overview</span></span>](../ado-net-overview.md)

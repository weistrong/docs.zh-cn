---
description: 了解详细信息：推断元素文本
title: 推断元素文本
ms.date: 03/30/2017
ms.assetid: 789799e5-716f-459f-a168-76c5cf22178b
ms.openlocfilehash: 5d0d9b1b3bb6164cd3cf26b429a4c7d658ee4128
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652206"
---
# <a name="inferring-element-text"></a><span data-ttu-id="c13a2-103">推断元素文本</span><span class="sxs-lookup"><span data-stu-id="c13a2-103">Inferring Element Text</span></span>

<span data-ttu-id="c13a2-104">如果某个元素包含文本，并且没有要推断为表的子元素 (例如) 具有属性或重复元素的元素，则将向为该元素推断的表中添加一个名为 **TableName_Text** 的新列。</span><span class="sxs-lookup"><span data-stu-id="c13a2-104">If an element contains text and has no child elements to be inferred as tables (such as elements with attributes or repeated elements), a new column with the name **TableName_Text** will be added to the table that is inferred for the element.</span></span> <span data-ttu-id="c13a2-105">该元素中包含的文本将添加到此表中的一行，并存储在新列中。</span><span class="sxs-lookup"><span data-stu-id="c13a2-105">The text contained in the element will be added to a row in the table and stored in the new column.</span></span> <span data-ttu-id="c13a2-106">新列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="c13a2-106">The **ColumnMapping** property of the new column will be set to **MappingType.SimpleContent**.</span></span>  
  
 <span data-ttu-id="c13a2-107">例如，考虑以下 XML。</span><span class="sxs-lookup"><span data-stu-id="c13a2-107">For example, consider the following XML.</span></span>  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1">Text1</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="c13a2-108">推理过程将生成一个名为 **Element1** 的表，该表包含两列： **attr1** 和 **Element1_Text**。</span><span class="sxs-lookup"><span data-stu-id="c13a2-108">The inference process will produce a table named **Element1** with two columns: **attr1** and **Element1_Text**.</span></span> <span data-ttu-id="c13a2-109">**Attr1** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="c13a2-109">The **ColumnMapping** property of the **attr1** column will be set to **MappingType.Attribute**.</span></span> <span data-ttu-id="c13a2-110">**Element1_Text** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="c13a2-110">The **ColumnMapping** property of the **Element1_Text** column will be set to **MappingType.SimpleContent**.</span></span>  
  
 <span data-ttu-id="c13a2-111">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="c13a2-111">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="c13a2-112">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="c13a2-112">**Table:** Element1</span></span>  
  
|<span data-ttu-id="c13a2-113">attr1</span><span class="sxs-lookup"><span data-stu-id="c13a2-113">attr1</span></span>|<span data-ttu-id="c13a2-114">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="c13a2-114">Element1_Text</span></span>|  
|-----------|--------------------|  
|<span data-ttu-id="c13a2-115">value1</span><span class="sxs-lookup"><span data-stu-id="c13a2-115">value1</span></span>|<span data-ttu-id="c13a2-116">Text1</span><span class="sxs-lookup"><span data-stu-id="c13a2-116">Text1</span></span>|  
  
 <span data-ttu-id="c13a2-117">如果某元素包含文本，并且还具有包含文本的子元素，则不会将列添加到表中来存储该元素所包含的文本。</span><span class="sxs-lookup"><span data-stu-id="c13a2-117">If an element contains text, but also has child elements that contain text, a column will not be added to the table to store the text contained in the element.</span></span> <span data-ttu-id="c13a2-118">该元素中包含的文本将被忽略，但子元素中的文本将包含在表的一行中。</span><span class="sxs-lookup"><span data-stu-id="c13a2-118">The text contained in the element will be ignored, while the text in the child elements is included in a row in the table.</span></span> <span data-ttu-id="c13a2-119">例如，考虑以下 XML。</span><span class="sxs-lookup"><span data-stu-id="c13a2-119">For example, consider the following XML.</span></span>  
  
```xml  
<Element1>  
  Text1  
  <ChildElement1>Text2</ChildElement1>  
  Text3  
</Element1>  
```  
  
 <span data-ttu-id="c13a2-120">推理过程将生成一个名为 **Element1** 的表，该表包含一个名为 **ChildElement1** 的列。</span><span class="sxs-lookup"><span data-stu-id="c13a2-120">The inference process will produce a table named **Element1** with one column named **ChildElement1**.</span></span> <span data-ttu-id="c13a2-121">**ChildElement1** 元素的文本将包含在表的行中。</span><span class="sxs-lookup"><span data-stu-id="c13a2-121">The text for the **ChildElement1** element will be included in a row in the table.</span></span> <span data-ttu-id="c13a2-122">其他文本则将被忽略。</span><span class="sxs-lookup"><span data-stu-id="c13a2-122">The other text will be ignored.</span></span> <span data-ttu-id="c13a2-123">**ChildElement1** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="c13a2-123">The **ColumnMapping** property of the **ChildElement1** column will be set to **MappingType.Element**.</span></span>  
  
 <span data-ttu-id="c13a2-124">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="c13a2-124">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="c13a2-125">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="c13a2-125">**Table:** Element1</span></span>  
  
|<span data-ttu-id="c13a2-126">ChildElement1</span><span class="sxs-lookup"><span data-stu-id="c13a2-126">ChildElement1</span></span>|  
|-------------------|  
|<span data-ttu-id="c13a2-127">Text2</span><span class="sxs-lookup"><span data-stu-id="c13a2-127">Text2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c13a2-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="c13a2-128">See also</span></span>

- [<span data-ttu-id="c13a2-129">从 XML 推断数据集关系结构</span><span class="sxs-lookup"><span data-stu-id="c13a2-129">Inferring DataSet Relational Structure from XML</span></span>](inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="c13a2-130">从 XML 加载数据集</span><span class="sxs-lookup"><span data-stu-id="c13a2-130">Loading a DataSet from XML</span></span>](loading-a-dataset-from-xml.md)
- [<span data-ttu-id="c13a2-131">从 XML 加载数据集架构信息</span><span class="sxs-lookup"><span data-stu-id="c13a2-131">Loading DataSet Schema Information from XML</span></span>](loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="c13a2-132">在数据集中使用 XML</span><span class="sxs-lookup"><span data-stu-id="c13a2-132">Using XML in a DataSet</span></span>](using-xml-in-a-dataset.md)
- [<span data-ttu-id="c13a2-133">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="c13a2-133">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="c13a2-134">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="c13a2-134">ADO.NET Overview</span></span>](../ado-net-overview.md)

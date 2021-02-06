---
description: 了解详细信息：推断关系
title: 推断关系
ms.date: 03/30/2017
ms.assetid: 8fa86a9d-6545-4a9d-b1f5-58d9742179c7
ms.openlocfilehash: a117581d512c1427c638ea862169ab3c7623d783
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652141"
---
# <a name="inferring-relationships"></a><span data-ttu-id="d2f36-103">推断关系</span><span class="sxs-lookup"><span data-stu-id="d2f36-103">Inferring Relationships</span></span>

<span data-ttu-id="d2f36-104">如果被推断为表的元素具有一个同样被推断为表的子元素，则将在这两个表之间创建 <xref:System.Data.DataRelation>。</span><span class="sxs-lookup"><span data-stu-id="d2f36-104">If an element that is inferred as a table has a child element that is also inferred as a table, a <xref:System.Data.DataRelation> will be created between the two tables.</span></span> <span data-ttu-id="d2f36-105">名称为 " **ParentTableName_Id** " 的新列将添加到为父元素创建的表和为子元素创建的表中。</span><span class="sxs-lookup"><span data-stu-id="d2f36-105">A new column with a name of **ParentTableName_Id** will be added to both the table created for the parent element, and the table created for the child element.</span></span> <span data-ttu-id="d2f36-106">此标识列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-106">The **ColumnMapping** property of this identity column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="d2f36-107">列将是父表的自动递增主键，并将用于这两个表之间的 **DataRelation** 。</span><span class="sxs-lookup"><span data-stu-id="d2f36-107">The column will be an auto-incrementing primary key for the parent table, and will be used for the **DataRelation** between the two tables.</span></span> <span data-ttu-id="d2f36-108">添加的标识列的数据类型将为 system.exception，这与所有其他推断列的数据类型 **不同，后者** 为 **system.string**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-108">The data type of the added identity column will be **System.Int32**, unlike the data type of all other inferred columns, which is **System.String**.</span></span> <span data-ttu-id="d2f36-109"><xref:System.Data.ForeignKeyConstraint>还将  =  使用父表和子表中的新列来创建具有 DeleteRule **级联** 的。</span><span class="sxs-lookup"><span data-stu-id="d2f36-109">A <xref:System.Data.ForeignKeyConstraint> with **DeleteRule** = **Cascade** will also be created using the new column in both the parent and child tables.</span></span>  
  
 <span data-ttu-id="d2f36-110">例如，考虑以下 XML：</span><span class="sxs-lookup"><span data-stu-id="d2f36-110">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1 attr1="value1" attr2="value2"/>  
    <ChildElement2>Text2</ChildElement2>  
  </Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="d2f36-111">推理过程将生成两个表： **Element1** 和 **ChildElement1**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-111">The inference process will produce two tables: **Element1** and **ChildElement1**.</span></span>  
  
 <span data-ttu-id="d2f36-112">**Element1** 表包含两列： **Element1_Id** 和 **ChildElement2**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-112">The **Element1** table will have two columns: **Element1_Id** and **ChildElement2**.</span></span> <span data-ttu-id="d2f36-113">**Element1_Id** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-113">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="d2f36-114">**ChildElement2** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-114">The **ColumnMapping** property of the **ChildElement2** column will be set to **MappingType.Element**.</span></span> <span data-ttu-id="d2f36-115">**Element1_Id** 列将设置为 **Element1** 表的主键。</span><span class="sxs-lookup"><span data-stu-id="d2f36-115">The **Element1_Id** column will be set as the primary key of the **Element1** table.</span></span>  
  
 <span data-ttu-id="d2f36-116">**ChildElement1** 表包含三列： **attr1**、 **attr2** 和 **Element1_Id**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-116">The **ChildElement1** table will have three columns: **attr1**, **attr2** and **Element1_Id**.</span></span> <span data-ttu-id="d2f36-117">**Attr1** 和 **Attr2** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-117">The **ColumnMapping** property for the **attr1** and **attr2** columns will be set to **MappingType.Attribute**.</span></span> <span data-ttu-id="d2f36-118">**Element1_Id** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。</span><span class="sxs-lookup"><span data-stu-id="d2f36-118">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span>  
  
 <span data-ttu-id="d2f36-119">将使用两个表中的 **Element1_Id** 列创建 **DataRelation** 和 **ForeignKeyConstraint** 。</span><span class="sxs-lookup"><span data-stu-id="d2f36-119">A **DataRelation** and **ForeignKeyConstraint** will be created using the **Element1_Id** columns from both tables.</span></span>  
  
 <span data-ttu-id="d2f36-120">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="d2f36-120">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="d2f36-121">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="d2f36-121">**Table:** Element1</span></span>  
  
|<span data-ttu-id="d2f36-122">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="d2f36-122">Element1_Id</span></span>|<span data-ttu-id="d2f36-123">ChildElement2</span><span class="sxs-lookup"><span data-stu-id="d2f36-123">ChildElement2</span></span>|  
|------------------|-------------------|  
|<span data-ttu-id="d2f36-124">0</span><span class="sxs-lookup"><span data-stu-id="d2f36-124">0</span></span>|<span data-ttu-id="d2f36-125">Text2</span><span class="sxs-lookup"><span data-stu-id="d2f36-125">Text2</span></span>|  
  
 <span data-ttu-id="d2f36-126">**表：** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="d2f36-126">**Table:** ChildElement1</span></span>  
  
|<span data-ttu-id="d2f36-127">attr1</span><span class="sxs-lookup"><span data-stu-id="d2f36-127">attr1</span></span>|<span data-ttu-id="d2f36-128">attr2</span><span class="sxs-lookup"><span data-stu-id="d2f36-128">attr2</span></span>|<span data-ttu-id="d2f36-129">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="d2f36-129">Element1_Id</span></span>|  
|-----------|-----------|------------------|  
|<span data-ttu-id="d2f36-130">value1</span><span class="sxs-lookup"><span data-stu-id="d2f36-130">value1</span></span>|<span data-ttu-id="d2f36-131">value2</span><span class="sxs-lookup"><span data-stu-id="d2f36-131">value2</span></span>|<span data-ttu-id="d2f36-132">0</span><span class="sxs-lookup"><span data-stu-id="d2f36-132">0</span></span>|  
  
 <span data-ttu-id="d2f36-133">**DataRelation：** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="d2f36-133">**DataRelation:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="d2f36-134">**ParentTable：** Element1</span><span class="sxs-lookup"><span data-stu-id="d2f36-134">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="d2f36-135">**ParentColumn：** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="d2f36-135">**ParentColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="d2f36-136">**ChildTable：** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="d2f36-136">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="d2f36-137">**ChildColumn：** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="d2f36-137">**ChildColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="d2f36-138">**嵌套：** True</span><span class="sxs-lookup"><span data-stu-id="d2f36-138">**Nested:** True</span></span>  
  
 <span data-ttu-id="d2f36-139">**ForeignKeyConstraint：** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="d2f36-139">**ForeignKeyConstraint:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="d2f36-140">**列：** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="d2f36-140">**Column:** Element1_Id</span></span>  
  
 <span data-ttu-id="d2f36-141">**ParentTable：** Element1</span><span class="sxs-lookup"><span data-stu-id="d2f36-141">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="d2f36-142">**ChildTable：** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="d2f36-142">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="d2f36-143">**DeleteRule：** Cascade</span><span class="sxs-lookup"><span data-stu-id="d2f36-143">**DeleteRule:** Cascade</span></span>  
  
 <span data-ttu-id="d2f36-144">**AcceptRejectRule：** 内容</span><span class="sxs-lookup"><span data-stu-id="d2f36-144">**AcceptRejectRule:** None</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2f36-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2f36-145">See also</span></span>

- [<span data-ttu-id="d2f36-146">从 XML 推断数据集关系结构</span><span class="sxs-lookup"><span data-stu-id="d2f36-146">Inferring DataSet Relational Structure from XML</span></span>](inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="d2f36-147">从 XML 加载数据集</span><span class="sxs-lookup"><span data-stu-id="d2f36-147">Loading a DataSet from XML</span></span>](loading-a-dataset-from-xml.md)
- [<span data-ttu-id="d2f36-148">从 XML 加载数据集架构信息</span><span class="sxs-lookup"><span data-stu-id="d2f36-148">Loading DataSet Schema Information from XML</span></span>](loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="d2f36-149">嵌套 DataRelation</span><span class="sxs-lookup"><span data-stu-id="d2f36-149">Nesting DataRelations</span></span>](nesting-datarelations.md)
- [<span data-ttu-id="d2f36-150">在数据集中使用 XML</span><span class="sxs-lookup"><span data-stu-id="d2f36-150">Using XML in a DataSet</span></span>](using-xml-in-a-dataset.md)
- [<span data-ttu-id="d2f36-151">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="d2f36-151">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="d2f36-152">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="d2f36-152">ADO.NET Overview</span></span>](../ado-net-overview.md)

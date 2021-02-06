---
description: 了解有关：推断表的详细信息
title: 推断表
ms.date: 03/30/2017
ms.assetid: 74a288d4-b8e9-4f1a-b2cd-10df92c1ed1f
ms.openlocfilehash: 00a24cbfc44aea4279b0a115214ec26d3eac59ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652154"
---
# <a name="inferring-tables"></a><span data-ttu-id="eb731-103">推断表</span><span class="sxs-lookup"><span data-stu-id="eb731-103">Inferring Tables</span></span>

<span data-ttu-id="eb731-104">当从 XML 文档推断 <xref:System.Data.DataSet> 的架构时，ADO.NET 首先会确定哪些 XML 元素表示表。</span><span class="sxs-lookup"><span data-stu-id="eb731-104">When inferring a schema for a <xref:System.Data.DataSet> from an XML document, ADO.NET first determines which XML elements represent tables.</span></span> <span data-ttu-id="eb731-105">以下 XML 结构将为 **数据集** 架构生成一个表：</span><span class="sxs-lookup"><span data-stu-id="eb731-105">The following XML structures result in a table for the **DataSet** schema:</span></span>  
  
- <span data-ttu-id="eb731-106">具有属性的元素</span><span class="sxs-lookup"><span data-stu-id="eb731-106">Elements with attributes</span></span>  
  
- <span data-ttu-id="eb731-107">具有子元素的元素</span><span class="sxs-lookup"><span data-stu-id="eb731-107">Elements with child elements</span></span>  
  
- <span data-ttu-id="eb731-108">重复元素</span><span class="sxs-lookup"><span data-stu-id="eb731-108">Repeating elements</span></span>  
  
## <a name="elements-with-attributes"></a><span data-ttu-id="eb731-109">具有属性的元素</span><span class="sxs-lookup"><span data-stu-id="eb731-109">Elements with Attributes</span></span>  

 <span data-ttu-id="eb731-110">在其中指定了属性的元素将生成推断表。</span><span class="sxs-lookup"><span data-stu-id="eb731-110">Elements that have attributes specified in them result in inferred tables.</span></span> <span data-ttu-id="eb731-111">例如，考虑以下 XML：</span><span class="sxs-lookup"><span data-stu-id="eb731-111">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1"/>  
  <Element1 attr1="value2">Text1</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="eb731-112">推断过程将生成名为“Element1”的表。</span><span class="sxs-lookup"><span data-stu-id="eb731-112">The inference process produces a table named "Element1."</span></span>  
  
 <span data-ttu-id="eb731-113">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="eb731-113">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="eb731-114">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="eb731-114">**Table:** Element1</span></span>  
  
|<span data-ttu-id="eb731-115">attr1</span><span class="sxs-lookup"><span data-stu-id="eb731-115">attr1</span></span>|<span data-ttu-id="eb731-116">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="eb731-116">Element1_Text</span></span>|  
|-----------|--------------------|  
|<span data-ttu-id="eb731-117">value1</span><span class="sxs-lookup"><span data-stu-id="eb731-117">value1</span></span>||  
|<span data-ttu-id="eb731-118">value2</span><span class="sxs-lookup"><span data-stu-id="eb731-118">value2</span></span>|<span data-ttu-id="eb731-119">Text1</span><span class="sxs-lookup"><span data-stu-id="eb731-119">Text1</span></span>|  
  
## <a name="elements-with-child-elements"></a><span data-ttu-id="eb731-120">具有子元素的元素</span><span class="sxs-lookup"><span data-stu-id="eb731-120">Elements with Child Elements</span></span>  

 <span data-ttu-id="eb731-121">具有子元素的元素将生成推断表。</span><span class="sxs-lookup"><span data-stu-id="eb731-121">Elements that have child elements result in inferred tables.</span></span> <span data-ttu-id="eb731-122">例如，考虑以下 XML：</span><span class="sxs-lookup"><span data-stu-id="eb731-122">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1>Text1</ChildElement1>  
  </Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="eb731-123">推断过程将生成名为“Element1”的表。</span><span class="sxs-lookup"><span data-stu-id="eb731-123">The inference process produces a table named "Element1."</span></span>  
  
 <span data-ttu-id="eb731-124">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="eb731-124">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="eb731-125">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="eb731-125">**Table:** Element1</span></span>  
  
|<span data-ttu-id="eb731-126">ChildElement1</span><span class="sxs-lookup"><span data-stu-id="eb731-126">ChildElement1</span></span>|  
|-------------------|  
|<span data-ttu-id="eb731-127">Text1</span><span class="sxs-lookup"><span data-stu-id="eb731-127">Text1</span></span>|  
  
 <span data-ttu-id="eb731-128">如果文档元素（即根元素）具有将被推断为列的属性或子元素，将生成推断表。</span><span class="sxs-lookup"><span data-stu-id="eb731-128">The document, or root, element result in an inferred table if it has attributes or child elements that are inferred as columns.</span></span> <span data-ttu-id="eb731-129">如果文档元素没有属性，并且没有任何子元素将被推断为列，则该元素将被推断为 **数据集**。</span><span class="sxs-lookup"><span data-stu-id="eb731-129">If the document element has no attributes and no child elements that would be inferred as columns, the element is inferred as a **DataSet**.</span></span> <span data-ttu-id="eb731-130">例如，考虑以下 XML：</span><span class="sxs-lookup"><span data-stu-id="eb731-130">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element2>Text2</Element2>  
</DocumentElement>  
```  
  
 <span data-ttu-id="eb731-131">推断过程将生成名为“DocumentElement”的表。</span><span class="sxs-lookup"><span data-stu-id="eb731-131">The inference process produces a table named "DocumentElement."</span></span>  
  
 <span data-ttu-id="eb731-132">**数据集：** NewDataSet</span><span class="sxs-lookup"><span data-stu-id="eb731-132">**DataSet:** NewDataSet</span></span>  
  
 <span data-ttu-id="eb731-133">**表：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="eb731-133">**Table:** DocumentElement</span></span>  
  
|<span data-ttu-id="eb731-134">Element1</span><span class="sxs-lookup"><span data-stu-id="eb731-134">Element1</span></span>|<span data-ttu-id="eb731-135">Element2</span><span class="sxs-lookup"><span data-stu-id="eb731-135">Element2</span></span>|  
|--------------|--------------|  
|<span data-ttu-id="eb731-136">Text1</span><span class="sxs-lookup"><span data-stu-id="eb731-136">Text1</span></span>|<span data-ttu-id="eb731-137">Text2</span><span class="sxs-lookup"><span data-stu-id="eb731-137">Text2</span></span>|  
  
 <span data-ttu-id="eb731-138">或者，考虑以下 XML：</span><span class="sxs-lookup"><span data-stu-id="eb731-138">Alternatively, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1" attr2="value2"/>  
</DocumentElement>  
```  
  
 <span data-ttu-id="eb731-139">推理过程将生成一个名为 "DocumentElement" 的 **数据集** ，其中包含一个名为 "Element1" 的表。</span><span class="sxs-lookup"><span data-stu-id="eb731-139">The inference process produces a **DataSet** named "DocumentElement" that contains a table named "Element1."</span></span>  
  
 <span data-ttu-id="eb731-140">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="eb731-140">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="eb731-141">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="eb731-141">**Table:** Element1</span></span>  
  
|<span data-ttu-id="eb731-142">attr1</span><span class="sxs-lookup"><span data-stu-id="eb731-142">attr1</span></span>|<span data-ttu-id="eb731-143">attr2</span><span class="sxs-lookup"><span data-stu-id="eb731-143">attr2</span></span>|  
|-----------|-----------|  
|<span data-ttu-id="eb731-144">value1</span><span class="sxs-lookup"><span data-stu-id="eb731-144">value1</span></span>|<span data-ttu-id="eb731-145">value2</span><span class="sxs-lookup"><span data-stu-id="eb731-145">value2</span></span>|  
  
## <a name="repeating-elements"></a><span data-ttu-id="eb731-146">重复元素</span><span class="sxs-lookup"><span data-stu-id="eb731-146">Repeating Elements</span></span>  

 <span data-ttu-id="eb731-147">重复的元素将生成单个推断表。</span><span class="sxs-lookup"><span data-stu-id="eb731-147">Elements that repeat result in a single inferred table.</span></span> <span data-ttu-id="eb731-148">例如，考虑以下 XML：</span><span class="sxs-lookup"><span data-stu-id="eb731-148">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element1>Text2</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="eb731-149">推断过程将生成名为“Element1”的表。</span><span class="sxs-lookup"><span data-stu-id="eb731-149">The inference process produces a table named "Element1."</span></span>  
  
 <span data-ttu-id="eb731-150">**数据集：** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="eb731-150">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="eb731-151">**表：** Element1</span><span class="sxs-lookup"><span data-stu-id="eb731-151">**Table:** Element1</span></span>  
  
|<span data-ttu-id="eb731-152">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="eb731-152">Element1_Text</span></span>|  
|--------------------|  
|<span data-ttu-id="eb731-153">Text1</span><span class="sxs-lookup"><span data-stu-id="eb731-153">Text1</span></span>|  
|<span data-ttu-id="eb731-154">Text2</span><span class="sxs-lookup"><span data-stu-id="eb731-154">Text2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eb731-155">请参阅</span><span class="sxs-lookup"><span data-stu-id="eb731-155">See also</span></span>

- [<span data-ttu-id="eb731-156">从 XML 推断数据集关系结构</span><span class="sxs-lookup"><span data-stu-id="eb731-156">Inferring DataSet Relational Structure from XML</span></span>](inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="eb731-157">从 XML 加载数据集</span><span class="sxs-lookup"><span data-stu-id="eb731-157">Loading a DataSet from XML</span></span>](loading-a-dataset-from-xml.md)
- [<span data-ttu-id="eb731-158">从 XML 加载数据集架构信息</span><span class="sxs-lookup"><span data-stu-id="eb731-158">Loading DataSet Schema Information from XML</span></span>](loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="eb731-159">在数据集中使用 XML</span><span class="sxs-lookup"><span data-stu-id="eb731-159">Using XML in a DataSet</span></span>](using-xml-in-a-dataset.md)
- [<span data-ttu-id="eb731-160">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="eb731-160">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="eb731-161">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="eb731-161">ADO.NET Overview</span></span>](../ado-net-overview.md)

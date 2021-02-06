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
# <a name="inferring-element-text"></a>推断元素文本

如果某个元素包含文本，并且没有要推断为表的子元素 (例如) 具有属性或重复元素的元素，则将向为该元素推断的表中添加一个名为 **TableName_Text** 的新列。 该元素中包含的文本将添加到此表中的一行，并存储在新列中。 新列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。  
  
 例如，考虑以下 XML。  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1">Text1</Element1>  
</DocumentElement>  
```  
  
 推理过程将生成一个名为 **Element1** 的表，该表包含两列： **attr1** 和 **Element1_Text**。 **Attr1** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。 **Element1_Text** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。  
  
 **数据集：** DocumentElement  
  
 **表：** Element1  
  
|attr1|Element1_Text|  
|-----------|--------------------|  
|value1|Text1|  
  
 如果某元素包含文本，并且还具有包含文本的子元素，则不会将列添加到表中来存储该元素所包含的文本。 该元素中包含的文本将被忽略，但子元素中的文本将包含在表的一行中。 例如，考虑以下 XML。  
  
```xml  
<Element1>  
  Text1  
  <ChildElement1>Text2</ChildElement1>  
  Text3  
</Element1>  
```  
  
 推理过程将生成一个名为 **Element1** 的表，该表包含一个名为 **ChildElement1** 的列。 **ChildElement1** 元素的文本将包含在表的行中。 其他文本则将被忽略。 **ChildElement1** 列的 **ColumnMapping** 属性将设置为 **mappingtype.attribute**。  
  
 **数据集：** DocumentElement  
  
 **表：** Element1  
  
|ChildElement1|  
|-------------------|  
|Text2|  
  
## <a name="see-also"></a>请参阅

- [从 XML 推断数据集关系结构](inferring-dataset-relational-structure-from-xml.md)
- [从 XML 加载数据集](loading-a-dataset-from-xml.md)
- [从 XML 加载数据集架构信息](loading-dataset-schema-information-from-xml.md)
- [在数据集中使用 XML](using-xml-in-a-dataset.md)
- [数据集、数据表和数据视图](index.md)
- [ADO.NET 概述](../ado-net-overview.md)

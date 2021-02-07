---
description: 了解详细信息：如何：将列表示为 Database-Generated
title: 如何：将列表示为数据库生成的
ms.date: 03/30/2017
ms.assetid: 6524b8a6-e5d2-4a3b-8e08-beafc4a84fd2
ms.openlocfilehash: 01828ef3f73257d20023168f0ea471ee7e3863c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695627"
---
# <a name="how-to-represent-columns-as-database-generated"></a>如何：将列表示为数据库生成的

使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> 特性上的属性 <xref:System.Data.Linq.Mapping.ColumnAttribute> 可将字段或属性指定为表示数据库生成的列。  
  
 有关代码示例，请参见<xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>。  
  
### <a name="to-designate-a-field-or-property-as-representing-a-database-generated-column"></a>指定字段或属性表示数据库生成的列  
  
1. 将 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> 属性 (Property) 添加到 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute)。  
  
2. 请将该属性值设置为 `true`。  
  
## <a name="see-also"></a>请参阅

- [LINQ to SQL 对象模型](the-linq-to-sql-object-model.md)
- [如何：通过使用代码编辑器自定义实体类](how-to-customize-entity-classes-by-using-the-code-editor.md)

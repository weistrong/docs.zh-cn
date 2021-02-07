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
# <a name="how-to-represent-columns-as-database-generated"></a><span data-ttu-id="5ef65-103">如何：将列表示为数据库生成的</span><span class="sxs-lookup"><span data-stu-id="5ef65-103">How to: Represent Columns as Database-Generated</span></span>

<span data-ttu-id="5ef65-104">使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> 特性上的属性 <xref:System.Data.Linq.Mapping.ColumnAttribute> 可将字段或属性指定为表示数据库生成的列。</span><span class="sxs-lookup"><span data-stu-id="5ef65-104">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> property on the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to designate a field or property as representing a database-generated column.</span></span>  
  
 <span data-ttu-id="5ef65-105">有关代码示例，请参见<xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>。</span><span class="sxs-lookup"><span data-stu-id="5ef65-105">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span></span>  
  
### <a name="to-designate-a-field-or-property-as-representing-a-database-generated-column"></a><span data-ttu-id="5ef65-106">指定字段或属性表示数据库生成的列</span><span class="sxs-lookup"><span data-stu-id="5ef65-106">To designate a field or property as representing a database-generated column</span></span>  
  
1. <span data-ttu-id="5ef65-107">将 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> 属性 (Property) 添加到 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute)。</span><span class="sxs-lookup"><span data-stu-id="5ef65-107">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="5ef65-108">请将该属性值设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="5ef65-108">Set the property value to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ef65-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="5ef65-109">See also</span></span>

- [<span data-ttu-id="5ef65-110">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="5ef65-110">The LINQ to SQL Object Model</span></span>](the-linq-to-sql-object-model.md)
- [<span data-ttu-id="5ef65-111">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="5ef65-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](how-to-customize-entity-classes-by-using-the-code-editor.md)

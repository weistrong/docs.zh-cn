---
description: 了解详细信息：如何：将列表示为允许 Null 值
title: 如何：将列表示为允许 Null 值
ms.date: 03/30/2017
ms.assetid: ebb71a37-1f4c-4fa7-b2d2-d903f13c4af1
ms.openlocfilehash: 019affd13fa9c2629c6a0ec66c42f19842a4d824
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695900"
---
# <a name="how-to-represent-columns-as-allowing-null-values"></a><span data-ttu-id="96468-103">如何：将列表示为允许 Null 值</span><span class="sxs-lookup"><span data-stu-id="96468-103">How to: Represent Columns as Allowing Null Values</span></span>

<span data-ttu-id="96468-104">使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> 特性上的属性可 <xref:System.Data.Linq.Mapping.ColumnAttribute> 指定关联的数据库列可以包含 null 值。</span><span class="sxs-lookup"><span data-stu-id="96468-104">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> property on the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to specify that the associated database column can hold null values.</span></span>  
  
 <span data-ttu-id="96468-105">有关代码示例，请参见<xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>。</span><span class="sxs-lookup"><span data-stu-id="96468-105">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>.</span></span>  
  
### <a name="to-designate-a-column-as-allowing-null-values"></a><span data-ttu-id="96468-106">将列指定为允许 null 值</span><span class="sxs-lookup"><span data-stu-id="96468-106">To designate a column as allowing null values</span></span>  
  
1. <span data-ttu-id="96468-107">将 <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> 属性 (Property) 添加到 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute)。</span><span class="sxs-lookup"><span data-stu-id="96468-107">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="96468-108">将 <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> 属性值设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="96468-108">Set the <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> property value to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96468-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="96468-109">See also</span></span>

- [<span data-ttu-id="96468-110">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="96468-110">The LINQ to SQL Object Model</span></span>](the-linq-to-sql-object-model.md)
- [<span data-ttu-id="96468-111">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="96468-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](how-to-customize-entity-classes-by-using-the-code-editor.md)

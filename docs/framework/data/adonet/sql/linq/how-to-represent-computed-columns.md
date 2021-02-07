---
description: 了解详细信息：如何：表示计算列
title: 如何：表示计算所得的列
ms.date: 03/30/2017
ms.assetid: 4025f1fd-9dfa-46c0-b04f-34e8bc7957a2
ms.openlocfilehash: 5f3b4898cd29c148665c6696b0b3abab42bd071c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695614"
---
# <a name="how-to-represent-computed-columns"></a><span data-ttu-id="05423-103">如何：表示计算所得的列</span><span class="sxs-lookup"><span data-stu-id="05423-103">How to: Represent Computed Columns</span></span>

<span data-ttu-id="05423-104">使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> 特性上的属性 <xref:System.Data.Linq.Mapping.ColumnAttribute> 表示其内容为计算结果的列。</span><span class="sxs-lookup"><span data-stu-id="05423-104">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> property on a <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to represent a column whose contents are the result of calculation.</span></span>  
  
 <span data-ttu-id="05423-105">有关代码示例，请参见<xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>。</span><span class="sxs-lookup"><span data-stu-id="05423-105">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span></span>  
  
> [!NOTE]
> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="05423-106">不支持作为主键的计算所得列。</span><span class="sxs-lookup"><span data-stu-id="05423-106">does not support computed columns as primary keys.</span></span>  
  
### <a name="to-represent-a-computed-column"></a><span data-ttu-id="05423-107">表示计算所得的列</span><span class="sxs-lookup"><span data-stu-id="05423-107">To represent a computed column</span></span>  
  
1. <span data-ttu-id="05423-108">将 <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> 属性 (Property) 添加到 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute)。</span><span class="sxs-lookup"><span data-stu-id="05423-108">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="05423-109">将公式的字符串表示形式赋给 <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="05423-109">Assign a string representation of the formula to the <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05423-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="05423-110">See also</span></span>

- [<span data-ttu-id="05423-111">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="05423-111">The LINQ to SQL Object Model</span></span>](the-linq-to-sql-object-model.md)
- [<span data-ttu-id="05423-112">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="05423-112">How to: Customize Entity Classes by Using the Code Editor</span></span>](how-to-customize-entity-classes-by-using-the-code-editor.md)

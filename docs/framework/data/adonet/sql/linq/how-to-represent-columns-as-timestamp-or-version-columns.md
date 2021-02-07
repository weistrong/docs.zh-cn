---
description: 了解详细信息：如何：将列表示为时间戳列或版本列
title: 如何：将列表示为时间戳列或版本列
ms.date: 03/30/2017
ms.assetid: 5afd5ce8-1d20-4bc3-a34f-49d95449f493
ms.openlocfilehash: 042e6a62c66b3f1ef522453157560e5e4c0f7de6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712501"
---
# <a name="how-to-represent-columns-as-timestamp-or-version-columns"></a><span data-ttu-id="dc33c-103">如何：将列表示为时间戳列或版本列</span><span class="sxs-lookup"><span data-stu-id="dc33c-103">How to: Represent Columns as Timestamp or Version Columns</span></span>

<span data-ttu-id="dc33c-104">使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> 特性的属性 <xref:System.Data.Linq.Mapping.ColumnAttribute> 可将字段或属性指定为表示保存数据库时间戳或版本号的数据库列。</span><span class="sxs-lookup"><span data-stu-id="dc33c-104">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> property of the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to designate a field or property as representing a database column that holds database timestamps or version numbers.</span></span>  
  
 <span data-ttu-id="dc33c-105">有关代码示例，请参见<xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>。</span><span class="sxs-lookup"><span data-stu-id="dc33c-105">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span></span>  
  
### <a name="to-designate-a-field-or-property-as-representing-a-timestamp-or-version-column"></a><span data-ttu-id="dc33c-106">将字段或属性指定为表示时间戳列或版本列</span><span class="sxs-lookup"><span data-stu-id="dc33c-106">To designate a field or property as representing a timestamp or version column</span></span>  
  
1. <span data-ttu-id="dc33c-107">将 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> 属性 (Property) 添加到 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute)。</span><span class="sxs-lookup"><span data-stu-id="dc33c-107">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="dc33c-108">将 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> 属性值设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="dc33c-108">Set the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> property value to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc33c-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="dc33c-109">See also</span></span>

- [<span data-ttu-id="dc33c-110">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="dc33c-110">The LINQ to SQL Object Model</span></span>](the-linq-to-sql-object-model.md)
- [<span data-ttu-id="dc33c-111">如何：指定要对哪些成员进行并发冲突测试</span><span class="sxs-lookup"><span data-stu-id="dc33c-111">How to: Specify Which Members are Tested for Concurrency Conflicts</span></span>](how-to-specify-which-members-are-tested-for-concurrency-conflicts.md)
- [<span data-ttu-id="dc33c-112">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="dc33c-112">How to: Customize Entity Classes by Using the Code Editor</span></span>](how-to-customize-entity-classes-by-using-the-code-editor.md)

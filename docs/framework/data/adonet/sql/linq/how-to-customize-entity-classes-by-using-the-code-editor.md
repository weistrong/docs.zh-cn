---
description: 了解详细信息：如何：使用代码编辑器自定义实体类
title: 如何：通过使用代码编辑器自定义实体类
ms.date: 03/30/2017
ms.assetid: ec28332f-9f3c-4e0a-baca-60f9141a68c0
ms.openlocfilehash: 6b4e8b5dcd5cb11095667fe95293a376cc63ade8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738983"
---
# <a name="how-to-customize-entity-classes-by-using-the-code-editor"></a><span data-ttu-id="4ff66-103">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="4ff66-103">How to: Customize Entity Classes by Using the Code Editor</span></span>

<span data-ttu-id="4ff66-104">使用 Visual Studio 的开发人员可以使用对象关系设计器来创建或自定义其实体类。</span><span class="sxs-lookup"><span data-stu-id="4ff66-104">Developers using Visual Studio can use the Object Relational Designer to create or customize their entity classes.</span></span>  
  
 <span data-ttu-id="4ff66-105">你还可以使用 Visual Studio 代码编辑器编写你自己的映射代码或自定义已生成的代码。</span><span class="sxs-lookup"><span data-stu-id="4ff66-105">You can also use the Visual Studio code editor to write your own mapping code or to customize code that has already been generated.</span></span> <span data-ttu-id="4ff66-106">有关详细信息，请参阅 [基于属性的映射](attribute-based-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="4ff66-106">For more information, see [Attribute-Based Mapping](attribute-based-mapping.md).</span></span>  
  
 <span data-ttu-id="4ff66-107">本节中的主题说明如何自定义对象模型。</span><span class="sxs-lookup"><span data-stu-id="4ff66-107">The topics in this section describe how to customize your object model.</span></span>  
  
 [<span data-ttu-id="4ff66-108">如何：指定数据库名称</span><span class="sxs-lookup"><span data-stu-id="4ff66-108">How to: Specify Database Names</span></span>](how-to-specify-database-names.md)  
 <span data-ttu-id="4ff66-109">描述如何使用 <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-109">Describes how to use <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-110">如何：将表表示为类</span><span class="sxs-lookup"><span data-stu-id="4ff66-110">How to: Represent Tables as Classes</span></span>](how-to-represent-tables-as-classes.md)  
 <span data-ttu-id="4ff66-111">描述如何使用 <xref:System.Data.Linq.Mapping.TableAttribute>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-111">Describes how to use <xref:System.Data.Linq.Mapping.TableAttribute>.</span></span>  
  
 [<span data-ttu-id="4ff66-112">如何：将列表示为类成员</span><span class="sxs-lookup"><span data-stu-id="4ff66-112">How to: Represent Columns as Class Members</span></span>](how-to-represent-columns-as-class-members.md)  
 <span data-ttu-id="4ff66-113">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-113">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span></span>  
  
 [<span data-ttu-id="4ff66-114">如何：表示主键</span><span class="sxs-lookup"><span data-stu-id="4ff66-114">How to: Represent Primary Keys</span></span>](how-to-represent-primary-keys.md)  
 <span data-ttu-id="4ff66-115">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-115">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-116">如何：映射数据库关系</span><span class="sxs-lookup"><span data-stu-id="4ff66-116">How to: Map Database Relationships</span></span>](how-to-map-database-relationships.md)  
 <span data-ttu-id="4ff66-117">提供使用 <xref:System.Data.Linq.Mapping.AssociationAttribute> 属性的示例。</span><span class="sxs-lookup"><span data-stu-id="4ff66-117">Provides examples of using the <xref:System.Data.Linq.Mapping.AssociationAttribute> attribute.</span></span>  
  
 [<span data-ttu-id="4ff66-118">如何：将列表示为数据库生成的</span><span class="sxs-lookup"><span data-stu-id="4ff66-118">How to: Represent Columns as Database-Generated</span></span>](how-to-represent-columns-as-database-generated.md)  
 <span data-ttu-id="4ff66-119">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-119">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-120">如何：将列表示为时间戳列或版本列</span><span class="sxs-lookup"><span data-stu-id="4ff66-120">How to: Represent Columns as Timestamp or Version Columns</span></span>](how-to-represent-columns-as-timestamp-or-version-columns.md)  
 <span data-ttu-id="4ff66-121">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-121">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-122">如何：指定数据库数据类型</span><span class="sxs-lookup"><span data-stu-id="4ff66-122">How to: Specify Database Data Types</span></span>](how-to-specify-database-data-types.md)  
 <span data-ttu-id="4ff66-123">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-123">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-124">如何：表示计算所得的列</span><span class="sxs-lookup"><span data-stu-id="4ff66-124">How to: Represent Computed Columns</span></span>](how-to-represent-computed-columns.md)  
 <span data-ttu-id="4ff66-125">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-125">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-126">如何：指定专用存储字段</span><span class="sxs-lookup"><span data-stu-id="4ff66-126">How to: Specify Private Storage Fields</span></span>](how-to-specify-private-storage-fields.md)  
 <span data-ttu-id="4ff66-127">描述如何使用 <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-127">Describes how to use <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-128">如何：将列表示为允许 Null 值</span><span class="sxs-lookup"><span data-stu-id="4ff66-128">How to: Represent Columns as Allowing Null Values</span></span>](how-to-represent-columns-as-allowing-null-values.md)  
 <span data-ttu-id="4ff66-129">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-129">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>.</span></span>  
  
 [<span data-ttu-id="4ff66-130">如何：映射继承层次结构</span><span class="sxs-lookup"><span data-stu-id="4ff66-130">How to: Map Inheritance Hierarchies</span></span>](how-to-map-inheritance-hierarchies.md)  
 <span data-ttu-id="4ff66-131">说明指定继承层次结构所需的映射。</span><span class="sxs-lookup"><span data-stu-id="4ff66-131">Describes the mappings required to specify an inheritance hierarchy.</span></span>  
  
 [<span data-ttu-id="4ff66-132">如何：指定并发冲突检查</span><span class="sxs-lookup"><span data-stu-id="4ff66-132">How to: Specify Concurrency-Conflict Checking</span></span>](how-to-specify-concurrency-conflict-checking.md)  
 <span data-ttu-id="4ff66-133">描述如何使用 <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>。</span><span class="sxs-lookup"><span data-stu-id="4ff66-133">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ff66-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="4ff66-134">See also</span></span>

- [<span data-ttu-id="4ff66-135">SqlMetal.exe（代码生成工具）</span><span class="sxs-lookup"><span data-stu-id="4ff66-135">SqlMetal.exe (Code Generation Tool)</span></span>](../../../../tools/sqlmetal-exe-code-generation-tool.md)

---
description: 了解详细信息：实体类型
title: Entity Type — 实体类型
ms.date: 03/30/2017
ms.assetid: a6dee9ab-9e4a-48f2-a169-3f79cc15821c
ms.openlocfilehash: fb801ca8565fce01466f30bddc8c14c39af568c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724357"
---
# <a name="entity-type"></a><span data-ttu-id="462b4-103">Entity Type — 实体类型</span><span class="sxs-lookup"><span data-stu-id="462b4-103">entity type</span></span>

<span data-ttu-id="462b4-104">*实体类型* 是用实体数据模型 (EDM) 来描述数据结构的基本构造块。</span><span class="sxs-lookup"><span data-stu-id="462b4-104">The *entity type* is the fundamental building block for describing the structure of data with the Entity Data Model (EDM).</span></span> <span data-ttu-id="462b4-105">在概念模型中，实体类型表示顶级概念（例如客户或订单）的结构。</span><span class="sxs-lookup"><span data-stu-id="462b4-105">In a conceptual model, an entity type represents the structure of top-level concepts, such as customers or orders.</span></span> <span data-ttu-id="462b4-106">实体类型是实体类型实例的模板。</span><span class="sxs-lookup"><span data-stu-id="462b4-106">An entity type is a template for entity type instances.</span></span> <span data-ttu-id="462b4-107">每个模板都包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="462b4-107">Each template contains the following information:</span></span>  
  
- <span data-ttu-id="462b4-108">唯一名称。</span><span class="sxs-lookup"><span data-stu-id="462b4-108">A unique name.</span></span> <span data-ttu-id="462b4-109">（必选。）</span><span class="sxs-lookup"><span data-stu-id="462b4-109">(Required.)</span></span>  
  
- <span data-ttu-id="462b4-110">由一个或多个属性定义的 [实体键](entity-key.md) 。</span><span class="sxs-lookup"><span data-stu-id="462b4-110">An [entity key](entity-key.md) defined by one or more properties.</span></span> <span data-ttu-id="462b4-111">（必选。）</span><span class="sxs-lookup"><span data-stu-id="462b4-111">(Required.)</span></span>  
  
- <span data-ttu-id="462b4-112">[属性](property.md)形式的数据。</span><span class="sxs-lookup"><span data-stu-id="462b4-112">Data in the form of [properties](property.md).</span></span> <span data-ttu-id="462b4-113">（可选。）</span><span class="sxs-lookup"><span data-stu-id="462b4-113">(Optional.)</span></span>  
  
- <span data-ttu-id="462b4-114">允许从[关联](association-type.md)的[一端](association-end.md)导航到另一端的[导航属性](navigation-property.md)。</span><span class="sxs-lookup"><span data-stu-id="462b4-114">[Navigation properties](navigation-property.md) that allow for navigation from one [end](association-end.md) of an [association](association-type.md) to the other end.</span></span> <span data-ttu-id="462b4-115">(可选)</span><span class="sxs-lookup"><span data-stu-id="462b4-115">(Optional)</span></span>  
  
 <span data-ttu-id="462b4-116">在应用程序中，实体类型的实例表示一个特定对象（例如特定客户或订单）。</span><span class="sxs-lookup"><span data-stu-id="462b4-116">In an application, an instance of an entity type represents a specific object (such as a specific customer or order).</span></span> <span data-ttu-id="462b4-117">实体类型的每个实例都必须在[实体集中](entity-set.md)具有唯一的[实体键](entity-key.md)。</span><span class="sxs-lookup"><span data-stu-id="462b4-117">Each instance of an entity type must have a unique [entity key](entity-key.md) within an [entity set](entity-set.md).</span></span>  
  
 <span data-ttu-id="462b4-118">只有两个实体类型实例的类型相同且其实体键的值也相同时，才认为它们是相等的。</span><span class="sxs-lookup"><span data-stu-id="462b4-118">Two entity type instances are considered equal only if they are of the same type and the values of their entity keys are the same.</span></span>  
  
## <a name="example"></a><span data-ttu-id="462b4-119">示例</span><span class="sxs-lookup"><span data-stu-id="462b4-119">Example</span></span>  

 <span data-ttu-id="462b4-120">下图显示了一个具有三个实体类型的概念模型：`Book`、`Publisher` 和 `Author`：</span><span class="sxs-lookup"><span data-stu-id="462b4-120">The diagram below shows a conceptual model with three entity types: `Book`, `Publisher`, and `Author`:</span></span>  
  
 ![具有三个实体类型的示例模型](./media/entity-type/example-model-three-entity-types.gif)  
  
 <span data-ttu-id="462b4-122">请注意，构成其实体键的每个实体类型的属性均用“(Key)”标示出来。</span><span class="sxs-lookup"><span data-stu-id="462b4-122">Note that the properties of each entity type that make up its entity key are denoted with "(Key)".</span></span>  
  
 <span data-ttu-id="462b4-123">[ADO.NET 实体框架](./ef/index.md)使用一种特定于域的语言 (DSL) 称为概念架构定义语言 ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) 来定义概念模型。</span><span class="sxs-lookup"><span data-stu-id="462b4-123">The [ADO.NET Entity Framework](./ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) to define conceptual models.</span></span> <span data-ttu-id="462b4-124">下面的 CSDL 定义了上图中显示的 `Book` 实体类型。</span><span class="sxs-lookup"><span data-stu-id="462b4-124">The following CSDL defines the `Book` entity type shown in the diagram above:</span></span>  
  
 [!code-xml[EDM_Example_Model#EntityExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]  
  
## <a name="see-also"></a><span data-ttu-id="462b4-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="462b4-125">See also</span></span>

- [<span data-ttu-id="462b4-126">实体数据模型关键概念</span><span class="sxs-lookup"><span data-stu-id="462b4-126">Entity Data Model Key Concepts</span></span>](entity-data-model-key-concepts.md)
- [<span data-ttu-id="462b4-127">实体数据模型</span><span class="sxs-lookup"><span data-stu-id="462b4-127">Entity Data Model</span></span>](entity-data-model.md)
- [<span data-ttu-id="462b4-128">多</span><span class="sxs-lookup"><span data-stu-id="462b4-128">facet</span></span>](facet.md)

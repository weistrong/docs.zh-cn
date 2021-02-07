---
description: 了解详细信息：属性
title: property
ms.date: 03/30/2017
ms.assetid: a941c53f-fc97-42c2-8832-0fb9f1d55c06
ms.openlocfilehash: 8b25c19b0673817945fa6cc786589346462f7e61
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754320"
---
# <a name="property"></a><span data-ttu-id="7e67c-103">property</span><span class="sxs-lookup"><span data-stu-id="7e67c-103">property</span></span>

<span data-ttu-id="7e67c-104">"*属性*" 是 [实体类型](entity-type.md)和 [复杂类型](complex-type.md)的基本构建基块。</span><span class="sxs-lookup"><span data-stu-id="7e67c-104">*Properties* are the fundamental building blocks of [entity types](entity-type.md) and [complex types](complex-type.md).</span></span> <span data-ttu-id="7e67c-105">属性定义了实体类型实例或复杂类型实例要包含的数据的形状和特征。</span><span class="sxs-lookup"><span data-stu-id="7e67c-105">Properties define the shape and characteristics of data that an entity type instance or complex type instance will contain.</span></span> <span data-ttu-id="7e67c-106">概念模型中的属性类似于为类定义的属性。</span><span class="sxs-lookup"><span data-stu-id="7e67c-106">Properties in a conceptual model are analogous to properties defined on a class.</span></span> <span data-ttu-id="7e67c-107">正如类的属性定义类的形状和携带有关对象的信息一样，概念模型中的属性也定义实体类型的形状和携带有关实体类型实例的信息。</span><span class="sxs-lookup"><span data-stu-id="7e67c-107">In the same way that properties on a class define the shape of the class and carry information about objects, properties in a conceptual model define the shape of an entity type and carry information about entity type instances.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7e67c-108">本主题中描述的属性不同于导航属性。</span><span class="sxs-lookup"><span data-stu-id="7e67c-108">Properties, as described in this topic, are different from navigation properties.</span></span> <span data-ttu-id="7e67c-109">有关详细信息，请参阅 [导航属性](navigation-property.md)。</span><span class="sxs-lookup"><span data-stu-id="7e67c-109">For more information, see [navigation properties](navigation-property.md).</span></span>  
  
 <span data-ttu-id="7e67c-110">属性定义包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="7e67c-110">A property definition contains the following information:</span></span>  
  
- <span data-ttu-id="7e67c-111">一个属性名称。</span><span class="sxs-lookup"><span data-stu-id="7e67c-111">A property name.</span></span> <span data-ttu-id="7e67c-112">（必需）</span><span class="sxs-lookup"><span data-stu-id="7e67c-112">(Required)</span></span>  
  
- <span data-ttu-id="7e67c-113">属性类型。</span><span class="sxs-lookup"><span data-stu-id="7e67c-113">A property type.</span></span> <span data-ttu-id="7e67c-114">（必需）</span><span class="sxs-lookup"><span data-stu-id="7e67c-114">(Required)</span></span>  
  
- <span data-ttu-id="7e67c-115">一组 [方面](facet.md)。</span><span class="sxs-lookup"><span data-stu-id="7e67c-115">A set of [facets](facet.md).</span></span> <span data-ttu-id="7e67c-116">(可选)</span><span class="sxs-lookup"><span data-stu-id="7e67c-116">(Optional)</span></span>  
  
 <span data-ttu-id="7e67c-117">属性可以包含基元数据（例如字符串、整数或布尔值）或结构化数据（例如复杂类型）。</span><span class="sxs-lookup"><span data-stu-id="7e67c-117">A property can contain primitive data (such as a string, an integer, or a Boolean value), or structured data (such as a complex type).</span></span> <span data-ttu-id="7e67c-118">基元类型的属性也称为标量属性。</span><span class="sxs-lookup"><span data-stu-id="7e67c-118">Properties that are of primitive type are also called scalar properties.</span></span> <span data-ttu-id="7e67c-119">有关详细信息，请参阅 [实体数据模型：基元数据类型](entity-data-model-primitive-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="7e67c-119">For more information, see [Entity Data Model: Primitive Data Types](entity-data-model-primitive-data-types.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7e67c-120">复杂类型本身可以具有复杂类型的属性。</span><span class="sxs-lookup"><span data-stu-id="7e67c-120">A complex type can, itself, have properties that are complex types.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e67c-121">示例</span><span class="sxs-lookup"><span data-stu-id="7e67c-121">Example</span></span>  

 <span data-ttu-id="7e67c-122">下图显示了一个具有三个实体类型的概念模型：`Book`、`Publisher` 和 `Author`。</span><span class="sxs-lookup"><span data-stu-id="7e67c-122">The diagram below shows a conceptual model with three entity types: `Book`, `Publisher`, and `Author`.</span></span> <span data-ttu-id="7e67c-123">每个实体类型具有多个属性，但图中没有传达每个属性的类型信息。</span><span class="sxs-lookup"><span data-stu-id="7e67c-123">Each entity type has several properties, although type information for each property is not conveyed in the diagram.</span></span> <span data-ttu-id="7e67c-124">作为 [实体键](entity-key.md) 的属性用 (键) 来表示。</span><span class="sxs-lookup"><span data-stu-id="7e67c-124">Properties that are [entity keys](entity-key.md) are denoted with (Key).</span></span>  
  
 ![具有三个实体类型的示例模型](./media/property/example-model-three-entity-types.gif)  
  
 <span data-ttu-id="7e67c-126">[ADO.NET 实体框架](./ef/index.md)使用一种特定于域的语言 (DSL) 称为概念架构定义语言 ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) 来定义概念模型。</span><span class="sxs-lookup"><span data-stu-id="7e67c-126">The [ADO.NET Entity Framework](./ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) to define conceptual models.</span></span> <span data-ttu-id="7e67c-127">下面的 CSDL 定义了 `Book` 实体类型（如上图所示）并使用 XML 特性表明了每个属性的类型和名称。</span><span class="sxs-lookup"><span data-stu-id="7e67c-127">The following CSDL defines the `Book` entity type (as shown in the diagram above) and indicates the type and name of each property by using XML attributes.</span></span> <span data-ttu-id="7e67c-128">此外，还使用 XML 特性定义了一个可选方面 `Nullable`。</span><span class="sxs-lookup"><span data-stu-id="7e67c-128">An optional facet, `Nullable`, is also defined by using an XML attribute.</span></span>  
  
 [!code-xml[EDM_Example_Model#EntityExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]  
  
 <span data-ttu-id="7e67c-129">图中所示的其中一个属性还可以是复杂类型属性。</span><span class="sxs-lookup"><span data-stu-id="7e67c-129">It is possible that one of the properties shown in the diagram is a complex type property.</span></span> <span data-ttu-id="7e67c-130">例如，`Address` 实体类型的 `Publisher` 属性可以是由多个标量属性（例如 `StreetAddress`、`City`、`StateOrProvince`、`Country` 和 `PostalCode`）构成的复杂类型属性。</span><span class="sxs-lookup"><span data-stu-id="7e67c-130">For example, the `Address` property on the `Publisher` entity type could be a complex type property composed of several scalar properties, such as `StreetAddress`, `City`, `StateOrProvince`, `Country`, and `PostalCode`.</span></span> <span data-ttu-id="7e67c-131">这种复杂类型的 CSDL 表示方式如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e67c-131">The CSDL representation of such a complex type would be as follows:</span></span>  
  
 [!code-xml[EDM_Example_Model#ComplexTypeExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books2.edmx#complextypeexample)]  
  
## <a name="see-also"></a><span data-ttu-id="7e67c-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="7e67c-132">See also</span></span>

- [<span data-ttu-id="7e67c-133">实体数据模型关键概念</span><span class="sxs-lookup"><span data-stu-id="7e67c-133">Entity Data Model Key Concepts</span></span>](entity-data-model-key-concepts.md)
- [<span data-ttu-id="7e67c-134">实体数据模型</span><span class="sxs-lookup"><span data-stu-id="7e67c-134">Entity Data Model</span></span>](entity-data-model.md)

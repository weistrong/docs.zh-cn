---
description: '了解有关以下内容的详细信息： XML Value 属性 (Visual Basic) '
title: XML 值属性
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyExtensionValue
helpviewer_keywords:
- Value property [Visual Basic]
- Visual Basic code, accessing XML
- XML axis [Visual Basic], Value
- XML Value property [Visual Basic]
ms.assetid: 7ddd057a-a195-4e9b-ad8b-2ee0e615a20f
ms.openlocfilehash: 49762c1fcc0059472a5be11726aa344a001807ea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768761"
---
# <a name="xml-value-property-visual-basic"></a><span data-ttu-id="8ae7e-103">XML 值属性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8ae7e-103">XML Value Property (Visual Basic)</span></span>

<span data-ttu-id="8ae7e-104">提供对对象集合中第一个元素的值的访问 <xref:System.Xml.Linq.XElement> 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-104">Provides access to the value of the first element of a collection of <xref:System.Xml.Linq.XElement> objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="8ae7e-105">Syntax</span></span>

```vb
object.Value
```

## <a name="parts"></a><span data-ttu-id="8ae7e-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="8ae7e-106">Parts</span></span>

|<span data-ttu-id="8ae7e-107">术语</span><span class="sxs-lookup"><span data-stu-id="8ae7e-107">Term</span></span>|<span data-ttu-id="8ae7e-108">定义</span><span class="sxs-lookup"><span data-stu-id="8ae7e-108">Definition</span></span>|  
|---|---|  
|`object`|<span data-ttu-id="8ae7e-109">必需。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-109">Required.</span></span> <span data-ttu-id="8ae7e-110"><xref:System.Xml.Linq.XElement> 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-110">Collection of <xref:System.Xml.Linq.XElement> objects.</span></span>|  

## <a name="return-value"></a><span data-ttu-id="8ae7e-111">返回值</span><span class="sxs-lookup"><span data-stu-id="8ae7e-111">Return Value</span></span>

 <span data-ttu-id="8ae7e-112">一个 `String` ，它包含集合中第一个元素的值; `Nothing` 如果集合为空，则为。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-112">A `String` that contains the value of the first element of the collection, or `Nothing` if the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae7e-113">备注</span><span class="sxs-lookup"><span data-stu-id="8ae7e-113">Remarks</span></span>

 <span data-ttu-id="8ae7e-114">使用 <xref:System.Xml.Linq.XElement.Value%2A> 属性可以轻松访问对象集合中第一个元素的值 <xref:System.Xml.Linq.XElement> 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-114">The <xref:System.Xml.Linq.XElement.Value%2A> property makes it easy to access the value of the first element in a collection of <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="8ae7e-115">此属性首先检查集合是否包含至少一个对象。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-115">This property first checks whether the collection contains at least one object.</span></span> <span data-ttu-id="8ae7e-116">如果集合为空，则此属性返回 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-116">If the collection is empty, this property returns `Nothing`.</span></span> <span data-ttu-id="8ae7e-117">否则，此属性将返回 <xref:System.Xml.Linq.XElement.Value%2A> 集合中第一个元素的属性的值。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-117">Otherwise, this property returns the value of the <xref:System.Xml.Linq.XElement.Value%2A> property of the first element in the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="8ae7e-118">使用 "" 标识符访问 XML 特性的值时 \@ ，特性值作为返回， `String` 无需显式指定 <xref:System.Xml.Linq.XAttribute.Value%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-118">When you access the value of an XML attribute using the '\@' identifier, the attribute value is returned as a `String` and you do not need to explicitly specify the <xref:System.Xml.Linq.XAttribute.Value%2A> property.</span></span>

 <span data-ttu-id="8ae7e-119">若要访问集合中的其他元素，可以使用 XML 扩展索引器属性。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-119">To access other elements in a collection, you can use the XML extension indexer property.</span></span> <span data-ttu-id="8ae7e-120">有关详细信息，请参阅 [扩展索引器属性](extension-indexer-property.md)。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-120">For more information, see [Extension Indexer Property](extension-indexer-property.md).</span></span>

## <a name="inheritance"></a><span data-ttu-id="8ae7e-121">继承</span><span class="sxs-lookup"><span data-stu-id="8ae7e-121">Inheritance</span></span>

 <span data-ttu-id="8ae7e-122">大多数用户将不必实现 <xref:System.Collections.Generic.IEnumerable%601> ，因此可以忽略此部分。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-122">Most users will not have to implement <xref:System.Collections.Generic.IEnumerable%601>, and can therefore ignore this section.</span></span>

 <span data-ttu-id="8ae7e-123"><xref:System.Xml.Linq.XElement.Value%2A>属性是实现的类型的扩展属性 `IEnumerable(Of XElement)` 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-123">The <xref:System.Xml.Linq.XElement.Value%2A> property is an extension property for types that implement `IEnumerable(Of XElement)`.</span></span> <span data-ttu-id="8ae7e-124">此扩展属性的绑定类似于扩展方法的绑定：如果某个类型实现了一个接口，并定义了一个名称为 "Value" 的属性，则该属性的优先级高于扩展属性。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-124">The binding of this extension property is like the binding of extension methods: if a type implements one of the interfaces and defines a property that has the name "Value", that property has precedence over the extension property.</span></span> <span data-ttu-id="8ae7e-125">换言之， <xref:System.Xml.Linq.XElement.Value%2A> 可以通过在实现的类中定义一个新属性来重写此属性 `IEnumerable(Of XElement)` 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-125">In other words, this <xref:System.Xml.Linq.XElement.Value%2A> property can be overridden by defining a new property in a class that implements `IEnumerable(Of XElement)`.</span></span>

## <a name="example"></a><span data-ttu-id="8ae7e-126">示例</span><span class="sxs-lookup"><span data-stu-id="8ae7e-126">Example</span></span>

 <span data-ttu-id="8ae7e-127">下面的示例演示如何使用 <xref:System.Xml.Linq.XElement.Value%2A> 属性访问对象集合中的第一个节点 <xref:System.Xml.Linq.XElement> 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-127">The following example shows how to use the <xref:System.Xml.Linq.XElement.Value%2A> property to access the first node in a collection of <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="8ae7e-128">该示例使用子轴属性来获取对象中名为的所有子节点的集合 `phone` `contact` 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-128">The example uses the child axis property to get the collection of all child nodes named `phone` that are in the `contact` object.</span></span>

 [!code-vb[VbXMLSamples#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#15)]

 <span data-ttu-id="8ae7e-129">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="8ae7e-129">This code displays the following text:</span></span>

 `Phone number: 206-555-0144`

## <a name="example"></a><span data-ttu-id="8ae7e-130">示例</span><span class="sxs-lookup"><span data-stu-id="8ae7e-130">Example</span></span>

 <span data-ttu-id="8ae7e-131">下面的示例演示如何从对象的集合中获取 XML 特性的值 <xref:System.Xml.Linq.XAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-131">The following example shows how to get the value of an XML attribute from a collection of <xref:System.Xml.Linq.XAttribute> objects.</span></span> <span data-ttu-id="8ae7e-132">该示例使用 "属性轴" 属性显示 `type` 所有元素的属性值 `phone` 。</span><span class="sxs-lookup"><span data-stu-id="8ae7e-132">The example uses the attribute axis property to display the value of the `type` attribute for all of the `phone` elements.</span></span>

 [!code-vb[VbXMLSamples#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#16)]

 <span data-ttu-id="8ae7e-133">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="8ae7e-133">This code displays the following text:</span></span>

 ```console
 home
 work
```

## <a name="see-also"></a><span data-ttu-id="8ae7e-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ae7e-134">See also</span></span>

- <xref:System.Xml.Linq.XElement>
- <xref:System.Collections.Generic.IEnumerable%601>
- [<span data-ttu-id="8ae7e-135">XML 轴属性</span><span class="sxs-lookup"><span data-stu-id="8ae7e-135">XML Axis Properties</span></span>](index.md)
- [<span data-ttu-id="8ae7e-136">XML 文本</span><span class="sxs-lookup"><span data-stu-id="8ae7e-136">XML Literals</span></span>](../xml-literals/index.md)
- [<span data-ttu-id="8ae7e-137">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="8ae7e-137">Creating XML in Visual Basic</span></span>](../../programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="8ae7e-138">扩展方法</span><span class="sxs-lookup"><span data-stu-id="8ae7e-138">Extension Methods</span></span>](../../programming-guide/language-features/procedures/extension-methods.md)
- [<span data-ttu-id="8ae7e-139">扩展索引器属性</span><span class="sxs-lookup"><span data-stu-id="8ae7e-139">Extension Indexer Property</span></span>](extension-indexer-property.md)
- [<span data-ttu-id="8ae7e-140">XML Child Axis Property</span><span class="sxs-lookup"><span data-stu-id="8ae7e-140">XML Child Axis Property</span></span>](xml-child-axis-property.md)
- [<span data-ttu-id="8ae7e-141">XML Attribute Axis Property</span><span class="sxs-lookup"><span data-stu-id="8ae7e-141">XML Attribute Axis Property</span></span>](xml-attribute-axis-property.md)

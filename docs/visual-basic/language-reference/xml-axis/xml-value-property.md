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
# <a name="xml-value-property-visual-basic"></a>XML 值属性 (Visual Basic)

提供对对象集合中第一个元素的值的访问 <xref:System.Xml.Linq.XElement> 。

## <a name="syntax"></a>语法

```vb
object.Value
```

## <a name="parts"></a>组成部分

|术语|定义|  
|---|---|  
|`object`|必需。 <xref:System.Xml.Linq.XElement> 对象的集合。|  

## <a name="return-value"></a>返回值

 一个 `String` ，它包含集合中第一个元素的值; `Nothing` 如果集合为空，则为。

## <a name="remarks"></a>备注

 使用 <xref:System.Xml.Linq.XElement.Value%2A> 属性可以轻松访问对象集合中第一个元素的值 <xref:System.Xml.Linq.XElement> 。 此属性首先检查集合是否包含至少一个对象。 如果集合为空，则此属性返回 `Nothing` 。 否则，此属性将返回 <xref:System.Xml.Linq.XElement.Value%2A> 集合中第一个元素的属性的值。

> [!NOTE]
> 使用 "" 标识符访问 XML 特性的值时 \@ ，特性值作为返回， `String` 无需显式指定 <xref:System.Xml.Linq.XAttribute.Value%2A> 属性。

 若要访问集合中的其他元素，可以使用 XML 扩展索引器属性。 有关详细信息，请参阅 [扩展索引器属性](extension-indexer-property.md)。

## <a name="inheritance"></a>继承

 大多数用户将不必实现 <xref:System.Collections.Generic.IEnumerable%601> ，因此可以忽略此部分。

 <xref:System.Xml.Linq.XElement.Value%2A>属性是实现的类型的扩展属性 `IEnumerable(Of XElement)` 。 此扩展属性的绑定类似于扩展方法的绑定：如果某个类型实现了一个接口，并定义了一个名称为 "Value" 的属性，则该属性的优先级高于扩展属性。 换言之， <xref:System.Xml.Linq.XElement.Value%2A> 可以通过在实现的类中定义一个新属性来重写此属性 `IEnumerable(Of XElement)` 。

## <a name="example"></a>示例

 下面的示例演示如何使用 <xref:System.Xml.Linq.XElement.Value%2A> 属性访问对象集合中的第一个节点 <xref:System.Xml.Linq.XElement> 。 该示例使用子轴属性来获取对象中名为的所有子节点的集合 `phone` `contact` 。

 [!code-vb[VbXMLSamples#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#15)]

 此代码显示以下文本：

 `Phone number: 206-555-0144`

## <a name="example"></a>示例

 下面的示例演示如何从对象的集合中获取 XML 特性的值 <xref:System.Xml.Linq.XAttribute> 。 该示例使用 "属性轴" 属性显示 `type` 所有元素的属性值 `phone` 。

 [!code-vb[VbXMLSamples#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#16)]

 此代码显示以下文本：

 ```console
 home
 work
```

## <a name="see-also"></a>请参阅

- <xref:System.Xml.Linq.XElement>
- <xref:System.Collections.Generic.IEnumerable%601>
- [XML 轴属性](index.md)
- [XML 文本](../xml-literals/index.md)
- [在 Visual Basic 中创建 XML](../../programming-guide/language-features/xml/creating-xml.md)
- [扩展方法](../../programming-guide/language-features/procedures/extension-methods.md)
- [扩展索引器属性](extension-indexer-property.md)
- [XML Child Axis Property](xml-child-axis-property.md)
- [XML Attribute Axis Property](xml-attribute-axis-property.md)

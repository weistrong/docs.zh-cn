---
description: '了解有关以下内容的详细信息：如何：访问 XML 子代元素 (Visual Basic) '
title: 如何：访问 XML 子代元素
ms.date: 07/20/2015
helpviewer_keywords:
- XML descendent axis property [Visual Basic]
- XML axis [Visual Basic], descendent
- descendent axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: aabfa258-4112-4e7e-bab9-403f96072ef7
ms.openlocfilehash: d8f3176a91c2f637f49d2754513f3253399ee8ed
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433169"
---
# <a name="how-to-access-xml-descendant-elements-visual-basic"></a>如何：访问 XML 后代元素 (Visual Basic)

此示例演示如何使用子代轴属性访问具有指定名称并包含在 XML 元素下的所有 XML 元素。 具体而言，它使用 `Value` 属性获取 `name` 子代轴属性返回的集合中第一个元素的值。 `name`子代轴属性获取 `name` 对象中包含的所有名为的元素 `contacts` 。 此示例还使用 `phone` 子代轴属性来访问 `phone` 对象中包含的所有名为的后代 `contacts` 。  
  
## <a name="example"></a>示例  

 [!code-vb[VbXMLSamples#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#31)]  
  
## <a name="compile-the-code"></a>编译代码  

 此示例需要：  
  
- 对 <xref:System.Xml.Linq> 命名空间的引用。  
  
## <a name="see-also"></a>请参阅

- <xref:System.Xml.Linq.XContainer.Descendants%2A?displayProperty=nameWithType>
- [XML Descendant Axis Property](../../../language-reference/xml-axis/xml-descendant-axis-property.md)
- [XML 值属性](../../../language-reference/xml-axis/xml-value-property.md)
- [在 Visual Basic 中访问 XML](accessing-xml.md)
- [XML](index.md)

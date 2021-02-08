---
description: '了解详细信息： XML 注释文字 (Visual Basic) '
title: XML 注释文本
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralComment
helpviewer_keywords:
- comment literal [Visual Basic]
- XML comments, adding [Visual Basic]
- XML comment literal [Visual Basic]
- XML literals [Visual Basic], comment
ms.assetid: 634c1cee-5e01-48d0-88d7-2dd55e4a9e52
ms.openlocfilehash: f44d2e132236d74d312910921fabb3a85afd82d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768735"
---
# <a name="xml-comment-literal-visual-basic"></a>XML 注释文本 (Visual Basic)

表示对象的文本 <xref:System.Xml.Linq.XComment> 。  
  
## <a name="syntax"></a>语法  
  
```xml  
<!-- content -->  
```  
  
## <a name="parts"></a>组成部分  
  
|术语|定义|  
|---|---|  
|`<!--`|必需。 表示 XML 注释的开头。|  
|`content`|必需。 要在 XML 注释中显示的文本。 不能包含由两个连字符组成的序列 (--) 或以与结束标记相邻的连字符结尾。|  
|`-->`|必需。 表示 XML 注释的结尾。|  
  
## <a name="return-value"></a>返回值  

 一个 <xref:System.Xml.Linq.XComment> 对象。  
  
## <a name="remarks"></a>备注  

 XML 注释文本不包含文档内容;它们包含有关文档的信息。 XML 注释部分以序列 "-->" 结尾。 这意味着：  
  
- 不能在 XML 注释文本中使用嵌入表达式，因为嵌入式表达式分隔符是有效的 XML 注释内容。  
  
- XML 注释部分不能嵌套，因为 `content` 不能包含值 "-->"。  
  
 可以将 XML 注释文本分配给一个变量，也可以将其包含在 XML 元素文本中。  
  
> [!NOTE]
> XML 文本可以跨多行，而无需使用行继续符。 此功能使你能够从 XML 文档复制内容并将其直接粘贴到 Visual Basic 程序。  
  
 Visual Basic 编译器将 XML 注释文本转换为对构造函数的调用 <xref:System.Xml.Linq.XComment.%23ctor%2A> 。  
  
## <a name="example"></a>示例  

 下面的示例创建一个包含文本 "This is a comment" 的 XML 注释。  
  
 [!code-vb[VbXMLSamples#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples4.vb#9)]  
  
## <a name="see-also"></a>请参阅

- <xref:System.Xml.Linq.XComment>
- [XML 元素文本](xml-element-literal.md)
- [XML 文本](index.md)
- [在 Visual Basic 中创建 XML](../../programming-guide/language-features/xml/creating-xml.md)

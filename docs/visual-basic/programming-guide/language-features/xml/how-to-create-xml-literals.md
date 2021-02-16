---
description: '了解详细信息：如何：创建 XML 文本 (Visual Basic) '
title: 如何：创建 XML 文本
ms.date: 07/20/2015
helpviewer_keywords:
- XML literals [Visual Basic], creating
ms.assetid: 573a6db5-b14d-4e42-b356-8cc7e2d77745
ms.openlocfilehash: 0e57b037d0567002fd570025e147771c4fab38f4
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433286"
---
# <a name="how-to-create-xml-literals-visual-basic"></a><span data-ttu-id="b2fe0-103">如何：创建 XML 文本 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b2fe0-103">How to: Create XML Literals (Visual Basic)</span></span>

<span data-ttu-id="b2fe0-104">您可以使用 XML 文本直接在代码中创建 XML 文档、片段或元素。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-104">You can create an XML document, fragment, or element directly in code by using an XML literal.</span></span> <span data-ttu-id="b2fe0-105">本主题中的示例演示如何创建包含三个子元素的 XML 元素以及如何创建 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-105">The examples in this topic demonstrate how to create an XML element that has three child elements, and how to create an XML document.</span></span>  
  
 <span data-ttu-id="b2fe0-106">你还可以使用 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] api 来创建 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 对象。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-106">You can also use the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] APIs to create [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objects.</span></span> <span data-ttu-id="b2fe0-107">有关详细信息，请参阅 <xref:System.Xml.Linq.XElement>。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-107">For more information, see <xref:System.Xml.Linq.XElement>.</span></span>  
  
### <a name="to-create-an-xml-element"></a><span data-ttu-id="b2fe0-108">创建 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b2fe0-108">To create an XML element</span></span>  
  
- <span data-ttu-id="b2fe0-109">使用 XML 文本语法（与实际 XML 语法相同）创建 XML 内联。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-109">Create the XML inline by using the XML literal syntax, which is the same as the actual XML syntax.</span></span>  
  
     [!code-vb[VbXMLSamples#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples2.vb#5)]  
  
     <span data-ttu-id="b2fe0-110">运行代码。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-110">Run the code.</span></span> <span data-ttu-id="b2fe0-111">此代码的输出为：</span><span class="sxs-lookup"><span data-stu-id="b2fe0-111">The output of this code is:</span></span>  
  
     `<contact>`  
  
     `<name>Patrick Hines</name>`  
  
     `<phone type="home">206-555-0144</phone>`  
  
     `<phone type="work">425-555-0145</phone>`  
  
     `</contact>`  
  
### <a name="to-create-an-xml-document"></a><span data-ttu-id="b2fe0-112">创建 XML 文档</span><span class="sxs-lookup"><span data-stu-id="b2fe0-112">To create an XML document</span></span>  
  
- <span data-ttu-id="b2fe0-113">以内联方式创建 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-113">Create the XML document inline.</span></span> <span data-ttu-id="b2fe0-114">下面的代码创建一个 XML 文档，该文档具有文本语法、XML 声明、处理指令、注释以及包含其他元素的元素。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-114">The following code creates an XML document that has literal syntax, an XML declaration, a processing instruction, a comment, and an element that contains another element.</span></span>  
  
     [!code-vb[VbXMLSamples#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#30)]  
  
     <span data-ttu-id="b2fe0-115">运行代码。</span><span class="sxs-lookup"><span data-stu-id="b2fe0-115">Run the code.</span></span> <span data-ttu-id="b2fe0-116">此代码的输出为：</span><span class="sxs-lookup"><span data-stu-id="b2fe0-116">The output of this code is:</span></span>  
  
     `<?xml-stylesheet type="text/xsl" href="show_book.xsl"?>`  
  
     `<!-- Tests that the application works. -->`  
  
     `<books>`  
  
     `<book/>`  
  
     `</books>`  
  
## <a name="see-also"></a><span data-ttu-id="b2fe0-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b2fe0-117">See also</span></span>

- [<span data-ttu-id="b2fe0-118">XML</span><span class="sxs-lookup"><span data-stu-id="b2fe0-118">XML</span></span>](index.md)
- [<span data-ttu-id="b2fe0-119">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="b2fe0-119">Creating XML in Visual Basic</span></span>](creating-xml.md)
- [<span data-ttu-id="b2fe0-120">XML 元素文本</span><span class="sxs-lookup"><span data-stu-id="b2fe0-120">XML Element Literal</span></span>](../../../language-reference/xml-literals/xml-element-literal.md)
- [<span data-ttu-id="b2fe0-121">XML 文档文本</span><span class="sxs-lookup"><span data-stu-id="b2fe0-121">XML Document Literal</span></span>](../../../language-reference/xml-literals/xml-document-literal.md)

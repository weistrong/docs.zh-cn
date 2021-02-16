---
description: '了解详细信息： (Visual Basic 的 XML 文本中的空格) '
title: XML 文本中的空白
ms.date: 07/20/2015
helpviewer_keywords:
- white space [XML in Visual Basic]
- XML literals [Visual Basic], white space
ms.assetid: dfe3a9ff-d69a-418e-a6b5-476f4ed84219
ms.openlocfilehash: 9b4134626c0ad1f7f4be2923573eb6058fa7687f
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100428111"
---
# <a name="white-space-in-xml-literals-visual-basic"></a><span data-ttu-id="69a66-103">XML 文本中的空白 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="69a66-103">White Space in XML Literals (Visual Basic)</span></span>

<span data-ttu-id="69a66-104">Visual Basic 编译器在创建对象时仅合并 XML 文本中的有效空白字符 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="69a66-104">The Visual Basic compiler incorporates only the significant white space characters from an XML literal when it creates a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] object.</span></span> <span data-ttu-id="69a66-105">不包含无意义的空白字符。</span><span class="sxs-lookup"><span data-stu-id="69a66-105">The insignificant white space characters are not incorporated.</span></span>  
  
## <a name="significant-and-insignificant-white-space"></a><span data-ttu-id="69a66-106">重要且无意义的空白</span><span class="sxs-lookup"><span data-stu-id="69a66-106">Significant and Insignificant White Space</span></span>  

 <span data-ttu-id="69a66-107">XML 文本中的空格字符仅在三个区域中很重要：</span><span class="sxs-lookup"><span data-stu-id="69a66-107">White space characters in XML literals are significant in only three areas:</span></span>  
  
- <span data-ttu-id="69a66-108">在属性值中。</span><span class="sxs-lookup"><span data-stu-id="69a66-108">When they are in an attribute value.</span></span>  
  
- <span data-ttu-id="69a66-109">当它们是元素的文本内容的一部分并且文本还包含其他字符时。</span><span class="sxs-lookup"><span data-stu-id="69a66-109">When they are part of an element's text content and the text also contains other characters.</span></span>  
  
- <span data-ttu-id="69a66-110">当它们位于元素的文本内容的嵌入式表达式中时。</span><span class="sxs-lookup"><span data-stu-id="69a66-110">When they are in an embedded expression for an element's text content.</span></span>  
  
 <span data-ttu-id="69a66-111">否则，编译器会将空白字符视为不重要的，并且不会在文本的对象中包括 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="69a66-111">Otherwise, the compiler treats white space characters as insignificant and does not include then in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] object for the literal.</span></span>  
  
 <span data-ttu-id="69a66-112">若要在 XML 文本中包含无意义的空白，请使用包含带有空格的字符串文字的嵌入式表达式。</span><span class="sxs-lookup"><span data-stu-id="69a66-112">To include insignificant white space in an XML literal, use an embedded expression that contains a string literal with the white space.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="69a66-113">如果 `xml:space` 属性出现在 XML 元素文本中，则 Visual Basic 编译器在对象中包括属性 <xref:System.Xml.Linq.XElement> ，但添加此属性不会更改编译器处理空白的方式。</span><span class="sxs-lookup"><span data-stu-id="69a66-113">If the `xml:space` attribute appears in an XML element literal, the Visual Basic compiler includes the attribute in the <xref:System.Xml.Linq.XElement> object, but adding this attribute does not change how the compiler treats white space.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="69a66-114">示例</span><span class="sxs-lookup"><span data-stu-id="69a66-114">Examples</span></span>  

 <span data-ttu-id="69a66-115">下面的示例包含两个 XML 元素：外部和内部。</span><span class="sxs-lookup"><span data-stu-id="69a66-115">The following example contains two XML elements, outer and inner.</span></span> <span data-ttu-id="69a66-116">这两个元素在其文本内容中都包含空格。</span><span class="sxs-lookup"><span data-stu-id="69a66-116">Both elements contain white space in their text content.</span></span> <span data-ttu-id="69a66-117">外部元素中的空白是无意义的，因为它仅包含空格和 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="69a66-117">The white space in the outer element is insignificant because it contains only white space and an XML element.</span></span> <span data-ttu-id="69a66-118">内部元素中的空格非常重要，因为它包含空格和文本。</span><span class="sxs-lookup"><span data-stu-id="69a66-118">The white space in the inner element is significant because it contains white space and text.</span></span>  
  
 [!code-vb[VbXMLSamples#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#29)]  
  
 <span data-ttu-id="69a66-119">运行时，此代码显示以下文本。</span><span class="sxs-lookup"><span data-stu-id="69a66-119">When run, this code displays the following text.</span></span>  
  
```xml  
<outer>  
  <inner>  
                                          Inner text  
                                      </inner>  
</outer>  
```  
  
## <a name="see-also"></a><span data-ttu-id="69a66-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="69a66-120">See also</span></span>

- [<span data-ttu-id="69a66-121">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="69a66-121">Creating XML in Visual Basic</span></span>](creating-xml.md)

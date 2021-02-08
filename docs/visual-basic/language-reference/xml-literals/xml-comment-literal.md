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
# <a name="xml-comment-literal-visual-basic"></a><span data-ttu-id="b5902-103">XML 注释文本 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b5902-103">XML Comment Literal (Visual Basic)</span></span>

<span data-ttu-id="b5902-104">表示对象的文本 <xref:System.Xml.Linq.XComment> 。</span><span class="sxs-lookup"><span data-stu-id="b5902-104">A literal representing an <xref:System.Xml.Linq.XComment> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5902-105">语法</span><span class="sxs-lookup"><span data-stu-id="b5902-105">Syntax</span></span>  
  
```xml  
<!-- content -->  
```  
  
## <a name="parts"></a><span data-ttu-id="b5902-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="b5902-106">Parts</span></span>  
  
|<span data-ttu-id="b5902-107">术语</span><span class="sxs-lookup"><span data-stu-id="b5902-107">Term</span></span>|<span data-ttu-id="b5902-108">定义</span><span class="sxs-lookup"><span data-stu-id="b5902-108">Definition</span></span>|  
|---|---|  
|`<!--`|<span data-ttu-id="b5902-109">必需。</span><span class="sxs-lookup"><span data-stu-id="b5902-109">Required.</span></span> <span data-ttu-id="b5902-110">表示 XML 注释的开头。</span><span class="sxs-lookup"><span data-stu-id="b5902-110">Denotes the start of the XML comment.</span></span>|  
|`content`|<span data-ttu-id="b5902-111">必需。</span><span class="sxs-lookup"><span data-stu-id="b5902-111">Required.</span></span> <span data-ttu-id="b5902-112">要在 XML 注释中显示的文本。</span><span class="sxs-lookup"><span data-stu-id="b5902-112">Text to appear in the XML comment.</span></span> <span data-ttu-id="b5902-113">不能包含由两个连字符组成的序列 (--) 或以与结束标记相邻的连字符结尾。</span><span class="sxs-lookup"><span data-stu-id="b5902-113">Cannot contain a series of two hyphens (--) or end with a hyphen adjacent to the closing tag.</span></span>|  
|`-->`|<span data-ttu-id="b5902-114">必需。</span><span class="sxs-lookup"><span data-stu-id="b5902-114">Required.</span></span> <span data-ttu-id="b5902-115">表示 XML 注释的结尾。</span><span class="sxs-lookup"><span data-stu-id="b5902-115">Denotes the end of the XML comment.</span></span>|  
  
## <a name="return-value"></a><span data-ttu-id="b5902-116">返回值</span><span class="sxs-lookup"><span data-stu-id="b5902-116">Return Value</span></span>  

 <span data-ttu-id="b5902-117">一个 <xref:System.Xml.Linq.XComment> 对象。</span><span class="sxs-lookup"><span data-stu-id="b5902-117">An <xref:System.Xml.Linq.XComment> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b5902-118">备注</span><span class="sxs-lookup"><span data-stu-id="b5902-118">Remarks</span></span>  

 <span data-ttu-id="b5902-119">XML 注释文本不包含文档内容;它们包含有关文档的信息。</span><span class="sxs-lookup"><span data-stu-id="b5902-119">XML comment literals do not contain document content; they contain information about the document.</span></span> <span data-ttu-id="b5902-120">XML 注释部分以序列 "-->" 结尾。</span><span class="sxs-lookup"><span data-stu-id="b5902-120">The XML comment section ends with the sequence "-->".</span></span> <span data-ttu-id="b5902-121">这意味着：</span><span class="sxs-lookup"><span data-stu-id="b5902-121">This implies the following points:</span></span>  
  
- <span data-ttu-id="b5902-122">不能在 XML 注释文本中使用嵌入表达式，因为嵌入式表达式分隔符是有效的 XML 注释内容。</span><span class="sxs-lookup"><span data-stu-id="b5902-122">You cannot use an embedded expression in an XML comment literal because the embedded expression delimiters are valid XML comment content.</span></span>  
  
- <span data-ttu-id="b5902-123">XML 注释部分不能嵌套，因为 `content` 不能包含值 "-->"。</span><span class="sxs-lookup"><span data-stu-id="b5902-123">XML comment sections cannot be nested, because `content` cannot contain the value "-->".</span></span>  
  
 <span data-ttu-id="b5902-124">可以将 XML 注释文本分配给一个变量，也可以将其包含在 XML 元素文本中。</span><span class="sxs-lookup"><span data-stu-id="b5902-124">You can assign an XML comment literal to a variable, or you can include it in an XML element literal.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b5902-125">XML 文本可以跨多行，而无需使用行继续符。</span><span class="sxs-lookup"><span data-stu-id="b5902-125">An XML literal can span multiple lines without using line continuation characters.</span></span> <span data-ttu-id="b5902-126">此功能使你能够从 XML 文档复制内容并将其直接粘贴到 Visual Basic 程序。</span><span class="sxs-lookup"><span data-stu-id="b5902-126">This feature enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="b5902-127">Visual Basic 编译器将 XML 注释文本转换为对构造函数的调用 <xref:System.Xml.Linq.XComment.%23ctor%2A> 。</span><span class="sxs-lookup"><span data-stu-id="b5902-127">The Visual Basic compiler converts the XML comment literal to a call to the <xref:System.Xml.Linq.XComment.%23ctor%2A> constructor.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b5902-128">示例</span><span class="sxs-lookup"><span data-stu-id="b5902-128">Example</span></span>  

 <span data-ttu-id="b5902-129">下面的示例创建一个包含文本 "This is a comment" 的 XML 注释。</span><span class="sxs-lookup"><span data-stu-id="b5902-129">The following example creates an XML comment that contains the text "This is a comment".</span></span>  
  
 [!code-vb[VbXMLSamples#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples4.vb#9)]  
  
## <a name="see-also"></a><span data-ttu-id="b5902-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5902-130">See also</span></span>

- <xref:System.Xml.Linq.XComment>
- [<span data-ttu-id="b5902-131">XML 元素文本</span><span class="sxs-lookup"><span data-stu-id="b5902-131">XML Element Literal</span></span>](xml-element-literal.md)
- [<span data-ttu-id="b5902-132">XML 文本</span><span class="sxs-lookup"><span data-stu-id="b5902-132">XML Literals</span></span>](index.md)
- [<span data-ttu-id="b5902-133">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="b5902-133">Creating XML in Visual Basic</span></span>](../../programming-guide/language-features/xml/creating-xml.md)

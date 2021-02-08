---
description: '了解有关以下内容的详细信息： XML CDATA 文字 (Visual Basic) '
title: XML CDATA 文本
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralCdata
helpviewer_keywords:
- CDATA literal [Visual Basic]
- XML CDATA literal [Visual Basic]
- XML literals [Visual Basic], CDATA
ms.assetid: 9eafb6a4-dd9d-4866-85e8-0654c65abc44
ms.openlocfilehash: d0b419954acb5a9e8ae824dbac8234e2116d09b9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768748"
---
# <a name="xml-cdata-literal-visual-basic"></a><span data-ttu-id="fc956-103">XML CDATA 文本 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fc956-103">XML CDATA Literal (Visual Basic)</span></span>

<span data-ttu-id="fc956-104">表示对象的文本 <xref:System.Xml.Linq.XCData> 。</span><span class="sxs-lookup"><span data-stu-id="fc956-104">A literal representing an <xref:System.Xml.Linq.XCData> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fc956-105">语法</span><span class="sxs-lookup"><span data-stu-id="fc956-105">Syntax</span></span>  
  
```xml  
<![CDATA[content]]>  
```  
  
## <a name="parts"></a><span data-ttu-id="fc956-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="fc956-106">Parts</span></span>  

 `<![CDATA[`  
 <span data-ttu-id="fc956-107">必需。</span><span class="sxs-lookup"><span data-stu-id="fc956-107">Required.</span></span> <span data-ttu-id="fc956-108">表示 XML CDATA 部分的开头。</span><span class="sxs-lookup"><span data-stu-id="fc956-108">Denotes the start of the XML CDATA section.</span></span>  
  
 `content`  
 <span data-ttu-id="fc956-109">必需。</span><span class="sxs-lookup"><span data-stu-id="fc956-109">Required.</span></span> <span data-ttu-id="fc956-110">要显示在 XML CDATA 节中的文本内容。</span><span class="sxs-lookup"><span data-stu-id="fc956-110">Text content to appear in the XML CDATA section.</span></span>  
  
 `]]>`  
 <span data-ttu-id="fc956-111">必需。</span><span class="sxs-lookup"><span data-stu-id="fc956-111">Required.</span></span> <span data-ttu-id="fc956-112">表示部分的结尾。</span><span class="sxs-lookup"><span data-stu-id="fc956-112">Denotes the end of the section.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fc956-113">返回值</span><span class="sxs-lookup"><span data-stu-id="fc956-113">Return Value</span></span>  

 <span data-ttu-id="fc956-114">一个 <xref:System.Xml.Linq.XCData> 对象。</span><span class="sxs-lookup"><span data-stu-id="fc956-114">An <xref:System.Xml.Linq.XCData> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fc956-115">备注</span><span class="sxs-lookup"><span data-stu-id="fc956-115">Remarks</span></span>  

 <span data-ttu-id="fc956-116">XML CDATA 节包含应包含的原始文本，但不应在包含它的 XML 中进行分析。</span><span class="sxs-lookup"><span data-stu-id="fc956-116">XML CDATA sections contain raw text that should be included, but not parsed, with the XML that contains it.</span></span> <span data-ttu-id="fc956-117">XML CDATA 节可以包含任何文本。</span><span class="sxs-lookup"><span data-stu-id="fc956-117">A XML CDATA section can contain any text.</span></span> <span data-ttu-id="fc956-118">其中包括保留的 XML 字符。</span><span class="sxs-lookup"><span data-stu-id="fc956-118">This includes reserved XML characters.</span></span> <span data-ttu-id="fc956-119">XML CDATA 部分以序列 "]] 结尾 >"。</span><span class="sxs-lookup"><span data-stu-id="fc956-119">The XML CDATA section ends with the sequence "]]>".</span></span> <span data-ttu-id="fc956-120">这意味着：</span><span class="sxs-lookup"><span data-stu-id="fc956-120">This implies the following points:</span></span>  
  
- <span data-ttu-id="fc956-121">不能在 XML CDATA 文本中使用嵌入式表达式，因为嵌入式表达式分隔符是有效的 XML CDATA 内容。</span><span class="sxs-lookup"><span data-stu-id="fc956-121">You cannot use an embedded expression in an XML CDATA literal because the embedded expression delimiters are valid XML CDATA content.</span></span>  
  
- <span data-ttu-id="fc956-122">XML CDATA 节不能嵌套，因为 `content` 不能包含值 "]] >"。</span><span class="sxs-lookup"><span data-stu-id="fc956-122">XML CDATA sections cannot be nested, because `content` cannot contain the value "]]>".</span></span>  
  
 <span data-ttu-id="fc956-123">可以将 XML CDATA 文本分配给一个变量，也可以将其包含在 XML 元素文本中。</span><span class="sxs-lookup"><span data-stu-id="fc956-123">You can assign an XML CDATA literal to a variable, or include it in an XML element literal.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="fc956-124">XML 文本可以跨多行，但不使用行继续符。</span><span class="sxs-lookup"><span data-stu-id="fc956-124">An XML literal can span multiple lines but does not use line continuation characters.</span></span> <span data-ttu-id="fc956-125">这使你可以从 XML 文档复制内容并将其直接粘贴到 Visual Basic 程序。</span><span class="sxs-lookup"><span data-stu-id="fc956-125">This enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="fc956-126">Visual Basic 编译器会将 XML CDATA 文本转换为对 <xref:System.Xml.Linq.XCData.%23ctor%2A> 构造函数的调用。</span><span class="sxs-lookup"><span data-stu-id="fc956-126">The Visual Basic compiler converts the XML CDATA literal to a call to the <xref:System.Xml.Linq.XCData.%23ctor%2A> constructor.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fc956-127">示例</span><span class="sxs-lookup"><span data-stu-id="fc956-127">Example</span></span>  

 <span data-ttu-id="fc956-128">下面的示例创建一个 CDATA 节，其中包含文本 "可以包含文本 \<XML> 标记"。</span><span class="sxs-lookup"><span data-stu-id="fc956-128">The following example creates a CDATA section that contains the text "Can contain literal \<XML> tags".</span></span>  
  
 [!code-vb[VbXMLSamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples11.vb#23)]  
  
## <a name="see-also"></a><span data-ttu-id="fc956-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="fc956-129">See also</span></span>

- <xref:System.Xml.Linq.XCData>
- [<span data-ttu-id="fc956-130">XML 元素文本</span><span class="sxs-lookup"><span data-stu-id="fc956-130">XML Element Literal</span></span>](xml-element-literal.md)
- [<span data-ttu-id="fc956-131">XML 文本</span><span class="sxs-lookup"><span data-stu-id="fc956-131">XML Literals</span></span>](index.md)
- [<span data-ttu-id="fc956-132">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="fc956-132">Creating XML in Visual Basic</span></span>](../../programming-guide/language-features/xml/creating-xml.md)

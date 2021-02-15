---
description: '了解有关详细信息，请参阅如何：从文件、字符串或流加载 XML (Visual Basic) '
title: 如何：从文件、字符串或流加载 XML
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], loading
- LINQ to XML [Visual Basic], loading XML from files
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
ms.openlocfilehash: 375190642c93d929abe2ae10bb6ccba927e3bc8a
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100480058"
---
# <a name="how-to-load-xml-from-a-file-string-or-stream-visual-basic"></a><span data-ttu-id="c2e71-103">如何：从文件、字符串或流加载 XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c2e71-103">How to: Load XML from a File, String, or Stream (Visual Basic)</span></span>

<span data-ttu-id="c2e71-104">通过使用几种方法，可以创建 [XML 文本](../../../language-reference/xml-literals/index.md) ，并使用外部源（例如文件、字符串或流）中的内容填充这些文本。</span><span class="sxs-lookup"><span data-stu-id="c2e71-104">You can create [XML Literals](../../../language-reference/xml-literals/index.md) and populate them with the contents from an external source such as a file, a string, or a stream by using several methods.</span></span> <span data-ttu-id="c2e71-105">下面的示例演示了这些方法。</span><span class="sxs-lookup"><span data-stu-id="c2e71-105">These methods are shown in the following examples.</span></span>

[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]

## <a name="to-load-xml-from-a-file"></a><span data-ttu-id="c2e71-106">从文件加载 XML</span><span class="sxs-lookup"><span data-stu-id="c2e71-106">To load XML from a file</span></span>

<span data-ttu-id="c2e71-107">若要从文件填充 XML 文本（如 <xref:System.Xml.Linq.XElement> 或 <xref:System.Xml.Linq.XDocument> 对象），请使用 `Load` 方法。</span><span class="sxs-lookup"><span data-stu-id="c2e71-107">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a file, use the `Load` method.</span></span> <span data-ttu-id="c2e71-108">此方法可采用文件路径、文本流或 XML 流作为输入。</span><span class="sxs-lookup"><span data-stu-id="c2e71-108">This method can take a file path, text stream, or XML stream as input.</span></span>

<span data-ttu-id="c2e71-109">下面的代码示例演示 <xref:System.Xml.Linq.XDocument.Load%28System.String%29> 如何使用方法 <xref:System.Xml.Linq.XDocument> 从文本文件中填充具有 XML 的对象。</span><span class="sxs-lookup"><span data-stu-id="c2e71-109">The following code example shows the use of the <xref:System.Xml.Linq.XDocument.Load%28System.String%29> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from a text file.</span></span>

[!code-vb[VbXMLSamples#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples15.vb#43)]

## <a name="to-load-xml-from-a-string"></a><span data-ttu-id="c2e71-110">从字符串加载 XML</span><span class="sxs-lookup"><span data-stu-id="c2e71-110">To load XML from a string</span></span>

<span data-ttu-id="c2e71-111">若要从字符串填充 XML 文本（如 <xref:System.Xml.Linq.XElement> 或 <xref:System.Xml.Linq.XDocument> 对象），可以使用 `Parse` 方法。</span><span class="sxs-lookup"><span data-stu-id="c2e71-111">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a string, you can use the `Parse` method.</span></span>

<span data-ttu-id="c2e71-112">下面的代码示例演示如何使用方法通过 <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=nameWithType> <xref:System.Xml.Linq.XDocument> 字符串中的 XML 来填充对象。</span><span class="sxs-lookup"><span data-stu-id="c2e71-112">The following code example shows the use of the <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=nameWithType> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from a string.</span></span>

[!code-vb[VbXMLSamples#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples15.vb#47)]

## <a name="to-load-xml-from-a-stream"></a><span data-ttu-id="c2e71-113">从流加载 XML</span><span class="sxs-lookup"><span data-stu-id="c2e71-113">To load XML from a stream</span></span>

<span data-ttu-id="c2e71-114">若要从流中填充 XML 文本（如 <xref:System.Xml.Linq.XElement> 或 <xref:System.Xml.Linq.XDocument> 对象），可以使用 `Load` 方法或 <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType> 方法。</span><span class="sxs-lookup"><span data-stu-id="c2e71-114">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a stream, you can use the `Load` method or the <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="c2e71-115">下面的代码示例演示 <xref:System.Xml.Linq.XNode.ReadFrom%2A> 如何使用方法 <xref:System.Xml.Linq.XDocument> 从 xml 流中填充具有 xml 的对象。</span><span class="sxs-lookup"><span data-stu-id="c2e71-115">The following code example shows the use of the <xref:System.Xml.Linq.XNode.ReadFrom%2A> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from an XML stream.</span></span>

[!code-vb[VbXMLSamples#46](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples15.vb#46)]

## <a name="see-also"></a><span data-ttu-id="c2e71-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2e71-116">See also</span></span>

- <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType>
- [<span data-ttu-id="c2e71-117">XML 文本</span><span class="sxs-lookup"><span data-stu-id="c2e71-117">XML Literals</span></span>](../../../language-reference/xml-literals/index.md)
- [<span data-ttu-id="c2e71-118">XML</span><span class="sxs-lookup"><span data-stu-id="c2e71-118">XML</span></span>](index.md)
- [<span data-ttu-id="c2e71-119">在 Visual Basic 中操作 XML</span><span class="sxs-lookup"><span data-stu-id="c2e71-119">Manipulating XML in Visual Basic</span></span>](manipulating-xml.md)

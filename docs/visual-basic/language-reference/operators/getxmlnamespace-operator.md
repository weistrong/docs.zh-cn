---
description: '详细了解： GetXmlNamespace Operator (Visual Basic) '
title: GetXmlNamespace 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.GetXmlNamespace
- GetXmlNamespace
helpviewer_keywords:
- GetXmlNamespace operator [Visual Basic]
- GetXmlNamespace keyword [Visual Basic]
ms.assetid: d0d28cfd-0755-4896-ae0b-4981aa35517c
ms.openlocfilehash: 704ac22493a0d6ce1255d171ae3b418313b74f09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665908"
---
# <a name="getxmlnamespace-operator-visual-basic"></a><span data-ttu-id="0c88d-103">GetXmlNamespace 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0c88d-103">GetXmlNamespace Operator (Visual Basic)</span></span>

<span data-ttu-id="0c88d-104">获取 <xref:System.Xml.Linq.XNamespace> 对应于指定 XML 命名空间前缀的对象。</span><span class="sxs-lookup"><span data-stu-id="0c88d-104">Gets the <xref:System.Xml.Linq.XNamespace> object that corresponds to the specified XML namespace prefix.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c88d-105">语法</span><span class="sxs-lookup"><span data-stu-id="0c88d-105">Syntax</span></span>  
  
```vb  
GetXmlNamespace(xmlNamespacePrefix)  
```  
  
## <a name="parts"></a><span data-ttu-id="0c88d-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="0c88d-106">Parts</span></span>  

 `xmlNamespacePrefix`  
 <span data-ttu-id="0c88d-107">可选。</span><span class="sxs-lookup"><span data-stu-id="0c88d-107">Optional.</span></span> <span data-ttu-id="0c88d-108">标识 XML 命名空间前缀的字符串。</span><span class="sxs-lookup"><span data-stu-id="0c88d-108">The string that identifies the XML namespace prefix.</span></span> <span data-ttu-id="0c88d-109">如果提供，则此字符串必须是有效的 XML 标识符。</span><span class="sxs-lookup"><span data-stu-id="0c88d-109">If supplied, this string must be a valid XML identifier.</span></span> <span data-ttu-id="0c88d-110">有关详细信息，请参阅已 [声明的 XML 元素和属性的名称](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="0c88d-110">For more information, see [Names of Declared XML Elements and Attributes](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span> <span data-ttu-id="0c88d-111">如果未指定前缀，则返回默认命名空间。</span><span class="sxs-lookup"><span data-stu-id="0c88d-111">If no prefix is specified, the default namespace is returned.</span></span> <span data-ttu-id="0c88d-112">如果未指定默认命名空间，则返回空命名空间。</span><span class="sxs-lookup"><span data-stu-id="0c88d-112">If no default namespace is specified, the empty namespace is returned.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0c88d-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0c88d-113">Return Value</span></span>  

 <span data-ttu-id="0c88d-114"><xref:System.Xml.Linq.XNamespace>对应于 XML 命名空间前缀的对象。</span><span class="sxs-lookup"><span data-stu-id="0c88d-114">The <xref:System.Xml.Linq.XNamespace> object that corresponds to the XML namespace prefix.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0c88d-115">备注</span><span class="sxs-lookup"><span data-stu-id="0c88d-115">Remarks</span></span>  

 <span data-ttu-id="0c88d-116">`GetXmlNamespace`运算符获取对应于 <xref:System.Xml.Linq.XNamespace> XML 命名空间前缀的对象 `xmlNamespacePrefix` 。</span><span class="sxs-lookup"><span data-stu-id="0c88d-116">The `GetXmlNamespace` operator gets the <xref:System.Xml.Linq.XNamespace> object that corresponds to the XML namespace prefix `xmlNamespacePrefix`.</span></span>  
  
 <span data-ttu-id="0c88d-117">您可以直接在 XML 文本和 XML 轴属性中使用 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="0c88d-117">You can use XML namespace prefixes directly in XML literals and XML axis properties.</span></span> <span data-ttu-id="0c88d-118">但是，必须使用 `GetXmlNamespace` 运算符将命名空间前缀转换为 <xref:System.Xml.Linq.XNamespace> 对象，然后才能在代码中使用它。</span><span class="sxs-lookup"><span data-stu-id="0c88d-118">However, you must use the `GetXmlNamespace` operator to convert a namespace prefix to an <xref:System.Xml.Linq.XNamespace> object before you can use it in your code.</span></span> <span data-ttu-id="0c88d-119">可以将未限定的元素名称追加到 <xref:System.Xml.Linq.XNamespace> 对象，以获取完全限定的 <xref:System.Xml.Linq.XName> 对象，这是许多 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 方法所需要的。</span><span class="sxs-lookup"><span data-stu-id="0c88d-119">You can append an unqualified element name to an <xref:System.Xml.Linq.XNamespace> object to get a fully qualified <xref:System.Xml.Linq.XName> object, which many [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] methods require.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c88d-120">示例</span><span class="sxs-lookup"><span data-stu-id="0c88d-120">Example</span></span>  

 <span data-ttu-id="0c88d-121">下面的示例将导入 `ns` 为 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="0c88d-121">The following example imports `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="0c88d-122">然后，它使用命名空间的前缀创建 XML 文本，并访问具有限定名称的第一个子节点 `ns:phone` 。</span><span class="sxs-lookup"><span data-stu-id="0c88d-122">It then uses the prefix of the namespace to create an XML literal and access the first child node that has the qualified name `ns:phone`.</span></span> <span data-ttu-id="0c88d-123">然后，它将该子节点传递到 `ShowName` 子例程，该子例程使用运算符构造限定名称 `GetXmlNamespace` 。</span><span class="sxs-lookup"><span data-stu-id="0c88d-123">It then passes that child node to the `ShowName` subroutine, which constructs a qualified name by using the `GetXmlNamespace` operator.</span></span> <span data-ttu-id="0c88d-124">然后，该 `ShowName` 子例程将限定名传递给 <xref:System.Xml.Linq.XNode.Ancestors%2A> 方法以获取父 `ns:contact` 节点。</span><span class="sxs-lookup"><span data-stu-id="0c88d-124">The `ShowName` subroutine then passes the qualified name to the <xref:System.Xml.Linq.XNode.Ancestors%2A> method to get the parent `ns:contact` node.</span></span>  
  
 [!code-vb[VbXMLSamples#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/GetXmlNamespace.vb#38)]  
  
 <span data-ttu-id="0c88d-125">调用时 `TestGetXmlNamespace.RunSample()` ，它会显示一个包含以下文本的消息框：</span><span class="sxs-lookup"><span data-stu-id="0c88d-125">When you call `TestGetXmlNamespace.RunSample()`, it displays a message box that contains the following text:</span></span>  
  
 `Name: Patrick Hines`  
  
## <a name="see-also"></a><span data-ttu-id="0c88d-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c88d-126">See also</span></span>

- [<span data-ttu-id="0c88d-127">Imports 语句（XML 命名空间）</span><span class="sxs-lookup"><span data-stu-id="0c88d-127">Imports Statement (XML Namespace)</span></span>](../statements/imports-statement-xml-namespace.md)
- [<span data-ttu-id="0c88d-128">在 Visual Basic 中访问 XML</span><span class="sxs-lookup"><span data-stu-id="0c88d-128">Accessing XML in Visual Basic</span></span>](../../programming-guide/language-features/xml/accessing-xml.md)

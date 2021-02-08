---
description: '了解有关以下内容的详细信息： XML 子轴属性 (Visual Basic) '
title: XML Child Axis Property
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyChildAxis
helpviewer_keywords:
- Visual Basic code, accessing XML
- XML axis [Visual Basic], child
- child axis property [Visual Basic]
- XML child axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: 89a59d00-985e-4f5c-b59f-29b47bad11cb
ms.openlocfilehash: 54920ebd35635f215eb6cb58867be1e4a7acd847
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768787"
---
# <a name="xml-child-axis-property-visual-basic"></a><span data-ttu-id="30118-103">XML 子轴属性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="30118-103">XML Child Axis Property (Visual Basic)</span></span>

<span data-ttu-id="30118-104">提供对以下一项的子级的访问：<xref:System.Xml.Linq.XElement> 对象、<xref:System.Xml.Linq.XDocument> 对象、<xref:System.Xml.Linq.XElement> 对象的集合或 <xref:System.Xml.Linq.XDocument> 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="30118-104">Provides access to the children of one of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30118-105">语法</span><span class="sxs-lookup"><span data-stu-id="30118-105">Syntax</span></span>  
  
```vb  
object.<child>  
```  
  
## <a name="parts"></a><span data-ttu-id="30118-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="30118-106">Parts</span></span>  
  
|<span data-ttu-id="30118-107">术语</span><span class="sxs-lookup"><span data-stu-id="30118-107">Term</span></span>|<span data-ttu-id="30118-108">定义</span><span class="sxs-lookup"><span data-stu-id="30118-108">Definition</span></span>|  
|---|---|  
|`object`|<span data-ttu-id="30118-109">必需。</span><span class="sxs-lookup"><span data-stu-id="30118-109">Required.</span></span> <span data-ttu-id="30118-110"><xref:System.Xml.Linq.XElement> 对象、<xref:System.Xml.Linq.XDocument> 对象、<xref:System.Xml.Linq.XElement> 对象的集合或 <xref:System.Xml.Linq.XDocument> 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="30118-110">An <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>|  
|<span data-ttu-id="30118-111">。 <</span><span class="sxs-lookup"><span data-stu-id="30118-111">.<</span></span>|<span data-ttu-id="30118-112">必需。</span><span class="sxs-lookup"><span data-stu-id="30118-112">Required.</span></span> <span data-ttu-id="30118-113">表示子轴属性的开头。</span><span class="sxs-lookup"><span data-stu-id="30118-113">Denotes the start of a child axis property.</span></span>|  
|`child`|<span data-ttu-id="30118-114">必需。</span><span class="sxs-lookup"><span data-stu-id="30118-114">Required.</span></span> <span data-ttu-id="30118-115">要访问的子节点的名称，格式为 `[prefix:]name` 。</span><span class="sxs-lookup"><span data-stu-id="30118-115">Name of the child nodes to access, of the form `[prefix:]name`.</span></span><br /><br /> <span data-ttu-id="30118-116">-   `Prefix` 可有可无.</span><span class="sxs-lookup"><span data-stu-id="30118-116">-   `Prefix` - Optional.</span></span> <span data-ttu-id="30118-117">子节点的 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="30118-117">XML namespace prefix for the child node.</span></span> <span data-ttu-id="30118-118">必须是使用 `Imports` 语句定义的全局 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="30118-118">Must be a global XML namespace defined with an `Imports` statement.</span></span><br /><span data-ttu-id="30118-119">-   `Name` 请求.</span><span class="sxs-lookup"><span data-stu-id="30118-119">-   `Name` - Required.</span></span> <span data-ttu-id="30118-120">本地子节点名。</span><span class="sxs-lookup"><span data-stu-id="30118-120">Local child node name.</span></span> <span data-ttu-id="30118-121">请参阅已 [声明的 XML 元素和属性的名称](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="30118-121">See [Names of Declared XML Elements and Attributes](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span>|  
|>|<span data-ttu-id="30118-122">必需。</span><span class="sxs-lookup"><span data-stu-id="30118-122">Required.</span></span> <span data-ttu-id="30118-123">表示子轴属性的结尾。</span><span class="sxs-lookup"><span data-stu-id="30118-123">Denotes the end of a child axis property.</span></span>|  
  
## <a name="return-value"></a><span data-ttu-id="30118-124">返回值</span><span class="sxs-lookup"><span data-stu-id="30118-124">Return Value</span></span>  

 <span data-ttu-id="30118-125"><xref:System.Xml.Linq.XElement> 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="30118-125">A collection of <xref:System.Xml.Linq.XElement> objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="30118-126">备注</span><span class="sxs-lookup"><span data-stu-id="30118-126">Remarks</span></span>  

 <span data-ttu-id="30118-127">可以使用 XML 子轴属性，从 <xref:System.Xml.Linq.XElement> 或 <xref:System.Xml.Linq.XDocument> 对象，或从 <xref:System.Xml.Linq.XElement> 或 <xref:System.Xml.Linq.XDocument> 对象的集合，按名称访问子节点。</span><span class="sxs-lookup"><span data-stu-id="30118-127">You can use an XML child axis property to access child nodes by name from an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object, or from a collection of <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> objects.</span></span> <span data-ttu-id="30118-128">使用 XML `Value` 属性来访问返回的集合中第一个子节点的值。</span><span class="sxs-lookup"><span data-stu-id="30118-128">Use the XML `Value` property to access the value of the first child node in the returned collection.</span></span> <span data-ttu-id="30118-129">有关详细信息，请参阅 [XML Value 属性](xml-value-property.md)。</span><span class="sxs-lookup"><span data-stu-id="30118-129">For more information, see [XML Value Property](xml-value-property.md).</span></span>  
  
 <span data-ttu-id="30118-130">Visual Basic 编译器将子轴属性转换为对方法的调用 <xref:System.Xml.Linq.XContainer.Elements%2A> 。</span><span class="sxs-lookup"><span data-stu-id="30118-130">The Visual Basic compiler converts child axis properties to calls to the <xref:System.Xml.Linq.XContainer.Elements%2A> method.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="30118-131">XML 命名空间</span><span class="sxs-lookup"><span data-stu-id="30118-131">XML Namespaces</span></span>  

 <span data-ttu-id="30118-132">子轴属性中的名称仅可使用通过 `Imports` 语句全局声明的 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="30118-132">The name in a child axis property can use only XML namespace prefixes declared globally with the `Imports` statement.</span></span> <span data-ttu-id="30118-133">它不能使用在 XML 元素文本中局部声明的 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="30118-133">It cannot use XML namespace prefixes declared locally within XML element literals.</span></span> <span data-ttu-id="30118-134">有关详细信息，请参阅 [ (XML 命名空间) 的 Imports 语句 ](../statements/imports-statement-xml-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="30118-134">For more information, see [Imports Statement (XML Namespace)](../statements/imports-statement-xml-namespace.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="30118-135">示例</span><span class="sxs-lookup"><span data-stu-id="30118-135">Example</span></span>  

 <span data-ttu-id="30118-136">下面的示例演示如何从 `contact` 对象访问名为 `phone` 的子节点。</span><span class="sxs-lookup"><span data-stu-id="30118-136">The following example shows how to access the child nodes named `phone` from the `contact` object.</span></span>  
  
 [!code-vb[VbXMLSamples#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#17)]  
  
 <span data-ttu-id="30118-137">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="30118-137">This code displays the following text:</span></span>  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a><span data-ttu-id="30118-138">示例</span><span class="sxs-lookup"><span data-stu-id="30118-138">Example</span></span>  

 <span data-ttu-id="30118-139">下面的示例演示如何从由 `contacts` 对象的 `contact` 子轴属性返回的集合访问名为 `phone` 的子节点。</span><span class="sxs-lookup"><span data-stu-id="30118-139">The following example shows how to access the child nodes named `phone` from the collection returned by the `contact` child axis property of the `contacts` object.</span></span>  
  
 [!code-vb[VbXMLSamples#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#18)]  
  
 <span data-ttu-id="30118-140">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="30118-140">This code displays the following text:</span></span>  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a><span data-ttu-id="30118-141">示例</span><span class="sxs-lookup"><span data-stu-id="30118-141">Example</span></span>  

 <span data-ttu-id="30118-142">下面的示例声明 `ns` 作为 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="30118-142">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="30118-143">然后它使用该命名空间前缀来创建 XML 文本并访问具有限定名称 `ns:name` 的第一个子节点。</span><span class="sxs-lookup"><span data-stu-id="30118-143">It then uses the prefix of the namespace to create an XML literal and access the first child node with the qualified name `ns:name`.</span></span>  
  
 [!code-vb[VbXMLSamples#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples8.vb#19)]  
  
 <span data-ttu-id="30118-144">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="30118-144">This code displays the following text:</span></span>  
  
 `Patrick Hines`  
  
## <a name="see-also"></a><span data-ttu-id="30118-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="30118-145">See also</span></span>

- <xref:System.Xml.Linq.XElement>
- [<span data-ttu-id="30118-146">XML 轴属性</span><span class="sxs-lookup"><span data-stu-id="30118-146">XML Axis Properties</span></span>](index.md)
- [<span data-ttu-id="30118-147">XML 文本</span><span class="sxs-lookup"><span data-stu-id="30118-147">XML Literals</span></span>](../xml-literals/index.md)
- [<span data-ttu-id="30118-148">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="30118-148">Creating XML in Visual Basic</span></span>](../../programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="30118-149">已声明的 XML 元素和属性的名称</span><span class="sxs-lookup"><span data-stu-id="30118-149">Names of Declared XML Elements and Attributes</span></span>](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)

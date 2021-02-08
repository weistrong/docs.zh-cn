---
description: '了解详细信息： XML 元素文本 (Visual Basic) '
title: XML 元素文本
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralElement
helpviewer_keywords:
- XML element literal [Visual Basic]
- element literal [Visual Basic]
- XML literals [Visual Basic], element
ms.assetid: 95039642-7893-48b7-b23f-45a6c55d8f67
ms.openlocfilehash: dfc78beded5c6f472b67fa272835ef0aa29d0187
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787534"
---
# <a name="xml-element-literal-visual-basic"></a><span data-ttu-id="c96a3-103">XML 元素文本 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c96a3-103">XML Element Literal (Visual Basic)</span></span>

<span data-ttu-id="c96a3-104">表示对象的文本 <xref:System.Xml.Linq.XElement> 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-104">A literal that represents an <xref:System.Xml.Linq.XElement> object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="c96a3-105">Syntax</span></span>

```xml
<name [ attributeList ] />
-or-
<name [ attributeList ] > [ elementContents ] </[ name ]>
```

## <a name="parts"></a><span data-ttu-id="c96a3-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="c96a3-106">Parts</span></span>

- `<`

  <span data-ttu-id="c96a3-107">必需。</span><span class="sxs-lookup"><span data-stu-id="c96a3-107">Required.</span></span> <span data-ttu-id="c96a3-108">打开开始元素标记。</span><span class="sxs-lookup"><span data-stu-id="c96a3-108">Opens the starting element tag.</span></span>

- `name`

  <span data-ttu-id="c96a3-109">必需。</span><span class="sxs-lookup"><span data-stu-id="c96a3-109">Required.</span></span> <span data-ttu-id="c96a3-110">元素名称。</span><span class="sxs-lookup"><span data-stu-id="c96a3-110">Name of the element.</span></span> <span data-ttu-id="c96a3-111">格式为以下格式之一：</span><span class="sxs-lookup"><span data-stu-id="c96a3-111">The format is one of the following:</span></span>

  - <span data-ttu-id="c96a3-112">元素名称的文本文本，格式为 `[ePrefix:]eName` ，其中：</span><span class="sxs-lookup"><span data-stu-id="c96a3-112">Literal text for the element name, of the form `[ePrefix:]eName`, where:</span></span>

    |<span data-ttu-id="c96a3-113">组成部分</span><span class="sxs-lookup"><span data-stu-id="c96a3-113">Part</span></span>|<span data-ttu-id="c96a3-114">说明</span><span class="sxs-lookup"><span data-stu-id="c96a3-114">Description</span></span>|
    |---|---|
    |`ePrefix`|<span data-ttu-id="c96a3-115">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-115">Optional.</span></span> <span data-ttu-id="c96a3-116">元素的 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="c96a3-116">XML namespace prefix for the element.</span></span> <span data-ttu-id="c96a3-117">必须是一个全局 XML 命名空间，该命名空间是使用 `Imports` 文件中的语句或项目级别定义的，或是在此元素或父元素中定义的本地 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="c96a3-117">Must be a global XML namespace that is defined with an `Imports` statement in the file or at the project level, or a local XML namespace that is defined in this element or a parent element.</span></span>|
    |`eName`|<span data-ttu-id="c96a3-118">必需。</span><span class="sxs-lookup"><span data-stu-id="c96a3-118">Required.</span></span> <span data-ttu-id="c96a3-119">元素名称。</span><span class="sxs-lookup"><span data-stu-id="c96a3-119">Name of the element.</span></span> <span data-ttu-id="c96a3-120">格式为以下格式之一：</span><span class="sxs-lookup"><span data-stu-id="c96a3-120">The format is one of the following:</span></span><br /><br /> <span data-ttu-id="c96a3-121">文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-121">- Literal text.</span></span> <span data-ttu-id="c96a3-122">请参阅已 [声明的 XML 元素和属性的名称](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-122">See [Names of Declared XML Elements and Attributes](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span><br /><span data-ttu-id="c96a3-123">-窗体的嵌入式表达式 `<%= eNameExp %>` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-123">- Embedded expression of the form `<%= eNameExp %>`.</span></span> <span data-ttu-id="c96a3-124">的类型 `eNameExp` 必须为 `String` 或可隐式转换为的类型 <xref:System.Xml.Linq.XName> 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-124">The type of `eNameExp` must be `String` or a type that is implicitly convertible to <xref:System.Xml.Linq.XName>.</span></span>|

  - <span data-ttu-id="c96a3-125">窗体的嵌入式表达式 `<%= nameExp %>` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-125">Embedded expression of the form `<%= nameExp %>`.</span></span> <span data-ttu-id="c96a3-126">的类型 `nameExp` 必须为 `String` 或可隐式转换为的类型 <xref:System.Xml.Linq.XName> 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-126">The type of `nameExp` must be `String` or a type implicitly convertible to <xref:System.Xml.Linq.XName>.</span></span> <span data-ttu-id="c96a3-127">元素的结束标记中不允许使用嵌入式表达式。</span><span class="sxs-lookup"><span data-stu-id="c96a3-127">An embedded expression is not allowed in a closing tag of an element.</span></span>

- `attributeList`

  <span data-ttu-id="c96a3-128">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-128">Optional.</span></span> <span data-ttu-id="c96a3-129">在文本中声明的属性的列表。</span><span class="sxs-lookup"><span data-stu-id="c96a3-129">List of attributes declared in the literal.</span></span>

  `attribute [ attribute ... ]`

  <span data-ttu-id="c96a3-130">每个 `attribute` 都具有以下语法之一：</span><span class="sxs-lookup"><span data-stu-id="c96a3-130">Each `attribute` has one of the following syntaxes:</span></span>

  - <span data-ttu-id="c96a3-131">属性分配，格式为 `[aPrefix:]aName=aValue` ，其中：</span><span class="sxs-lookup"><span data-stu-id="c96a3-131">Attribute assignment, of the form `[aPrefix:]aName=aValue`, where:</span></span>

    |<span data-ttu-id="c96a3-132">组成部分</span><span class="sxs-lookup"><span data-stu-id="c96a3-132">Part</span></span>|<span data-ttu-id="c96a3-133">说明</span><span class="sxs-lookup"><span data-stu-id="c96a3-133">Description</span></span>|
    |---|---|
    |`aPrefix`|<span data-ttu-id="c96a3-134">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-134">Optional.</span></span> <span data-ttu-id="c96a3-135">特性的 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="c96a3-135">XML namespace prefix for the attribute.</span></span> <span data-ttu-id="c96a3-136">必须是使用语句定义的全局 XML 命名空间 `Imports` ，或此元素或父元素中定义的本地 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="c96a3-136">Must be a global XML namespace that is defined with an `Imports` statement, or a local XML namespace that is defined in this element or a parent element.</span></span>|
    |`aName`|<span data-ttu-id="c96a3-137">必需。</span><span class="sxs-lookup"><span data-stu-id="c96a3-137">Required.</span></span> <span data-ttu-id="c96a3-138">属性的名称。</span><span class="sxs-lookup"><span data-stu-id="c96a3-138">Name of the attribute.</span></span> <span data-ttu-id="c96a3-139">格式为以下格式之一：</span><span class="sxs-lookup"><span data-stu-id="c96a3-139">The format is one of the following:</span></span><br /><br /> <span data-ttu-id="c96a3-140">文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-140">- Literal text.</span></span> <span data-ttu-id="c96a3-141">请参阅已 [声明的 XML 元素和属性的名称](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-141">See [Names of Declared XML Elements and Attributes](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span><br /><span data-ttu-id="c96a3-142">-窗体的嵌入式表达式 `<%= aNameExp %>` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-142">- Embedded expression of the form `<%= aNameExp %>`.</span></span> <span data-ttu-id="c96a3-143">的类型 `aNameExp` 必须为 `String` 或可隐式转换为的类型 <xref:System.Xml.Linq.XName> 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-143">The type of `aNameExp` must be `String` or a type that is implicitly convertible to <xref:System.Xml.Linq.XName>.</span></span>|
    |`aValue`|<span data-ttu-id="c96a3-144">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-144">Optional.</span></span> <span data-ttu-id="c96a3-145">特性的值。</span><span class="sxs-lookup"><span data-stu-id="c96a3-145">Value of the attribute.</span></span> <span data-ttu-id="c96a3-146">格式为以下格式之一：</span><span class="sxs-lookup"><span data-stu-id="c96a3-146">The format is one of the following:</span></span><br /><br /> <span data-ttu-id="c96a3-147">文本文本，用引号引起来。</span><span class="sxs-lookup"><span data-stu-id="c96a3-147">- Literal text, enclosed in quotation marks.</span></span><br /><span data-ttu-id="c96a3-148">-窗体的嵌入式表达式 `<%= aValueExp %>` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-148">- Embedded expression of the form `<%= aValueExp %>`.</span></span> <span data-ttu-id="c96a3-149">允许任何类型。</span><span class="sxs-lookup"><span data-stu-id="c96a3-149">Any type is allowed.</span></span>|

  - <span data-ttu-id="c96a3-150">窗体的嵌入式表达式 `<%= aExp %>` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-150">Embedded expression of the form `<%= aExp %>`.</span></span>

- `/>`

  <span data-ttu-id="c96a3-151">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-151">Optional.</span></span> <span data-ttu-id="c96a3-152">指示元素是一个空元素，不包含内容。</span><span class="sxs-lookup"><span data-stu-id="c96a3-152">Indicates that the element is an empty element, without content.</span></span>

- `>`

  <span data-ttu-id="c96a3-153">必需。</span><span class="sxs-lookup"><span data-stu-id="c96a3-153">Required.</span></span> <span data-ttu-id="c96a3-154">结束开始或空元素标记。</span><span class="sxs-lookup"><span data-stu-id="c96a3-154">Ends the beginning or empty element tag.</span></span>

- `elementContents`

  <span data-ttu-id="c96a3-155">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-155">Optional.</span></span> <span data-ttu-id="c96a3-156">元素的内容。</span><span class="sxs-lookup"><span data-stu-id="c96a3-156">Content of the element.</span></span>

  `content [ content ... ]`

  <span data-ttu-id="c96a3-157">每个 `content` 可以是以下各项之一：</span><span class="sxs-lookup"><span data-stu-id="c96a3-157">Each `content` can be one of the following:</span></span>

  - <span data-ttu-id="c96a3-158">文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-158">Literal text.</span></span> <span data-ttu-id="c96a3-159">如果存在任何文本，则中的所有空白都 `elementContents` 非常重要。</span><span class="sxs-lookup"><span data-stu-id="c96a3-159">All the white space in `elementContents` becomes significant if there is any literal text.</span></span>

  - <span data-ttu-id="c96a3-160">窗体的嵌入式表达式 `<%= contentExp %>` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-160">Embedded expression of the form `<%= contentExp %>`.</span></span>

  - <span data-ttu-id="c96a3-161">XML 元素文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-161">XML element literal.</span></span>

  - <span data-ttu-id="c96a3-162">XML 注释文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-162">XML comment literal.</span></span> <span data-ttu-id="c96a3-163">请参阅 [XML 注释文本](xml-comment-literal.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-163">See [XML Comment Literal](xml-comment-literal.md).</span></span>

  - <span data-ttu-id="c96a3-164">XML 处理指令文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-164">XML processing instruction literal.</span></span> <span data-ttu-id="c96a3-165">请参阅 [XML 处理指令文本](xml-processing-instruction-literal.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-165">See [XML Processing Instruction Literal](xml-processing-instruction-literal.md).</span></span>

  - <span data-ttu-id="c96a3-166">XML CDATA 文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-166">XML CDATA literal.</span></span> <span data-ttu-id="c96a3-167">请参阅 [XML CDATA 文本](xml-cdata-literal.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-167">See [XML CDATA Literal](xml-cdata-literal.md).</span></span>

- `</[name]>`

  <span data-ttu-id="c96a3-168">可选。</span><span class="sxs-lookup"><span data-stu-id="c96a3-168">Optional.</span></span> <span data-ttu-id="c96a3-169">表示元素的结束标记。</span><span class="sxs-lookup"><span data-stu-id="c96a3-169">Represents the closing tag for the element.</span></span> <span data-ttu-id="c96a3-170">`name`如果是嵌入式表达式的结果，则不允许使用可选参数。</span><span class="sxs-lookup"><span data-stu-id="c96a3-170">The optional `name` parameter is not allowed when it is the result of an embedded expression.</span></span>

## <a name="return-value"></a><span data-ttu-id="c96a3-171">返回值</span><span class="sxs-lookup"><span data-stu-id="c96a3-171">Return Value</span></span>

<span data-ttu-id="c96a3-172">一个 <xref:System.Xml.Linq.XElement> 对象。</span><span class="sxs-lookup"><span data-stu-id="c96a3-172">An <xref:System.Xml.Linq.XElement> object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c96a3-173">备注</span><span class="sxs-lookup"><span data-stu-id="c96a3-173">Remarks</span></span>

<span data-ttu-id="c96a3-174">您可以在代码中使用 XML 元素文本语法来创建 <xref:System.Xml.Linq.XElement> 对象。</span><span class="sxs-lookup"><span data-stu-id="c96a3-174">You can use the XML element literal syntax to create <xref:System.Xml.Linq.XElement> objects in your code.</span></span>

> [!NOTE]
> <span data-ttu-id="c96a3-175">XML 文本可以跨多行，而无需使用行继续符。</span><span class="sxs-lookup"><span data-stu-id="c96a3-175">An XML literal can span multiple lines without using line continuation characters.</span></span> <span data-ttu-id="c96a3-176">此功能使你能够从 XML 文档复制内容并将其直接粘贴到 Visual Basic 程序。</span><span class="sxs-lookup"><span data-stu-id="c96a3-176">This feature enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>

<span data-ttu-id="c96a3-177">利用窗体的嵌入式表达式，你可以向 `<%= exp %>` XML 元素文本添加动态信息。</span><span class="sxs-lookup"><span data-stu-id="c96a3-177">Embedded expressions of the form `<%= exp %>` enable you to add dynamic information to an XML element literal.</span></span> <span data-ttu-id="c96a3-178">有关详细信息，请参阅 [XML 中的嵌入式表达式](../../programming-guide/language-features/xml/embedded-expressions-in-xml.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-178">For more information, see [Embedded Expressions in XML](../../programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span></span>

<span data-ttu-id="c96a3-179">Visual Basic 编译器将 XML 元素文本转换为对构造函数的调用， <xref:System.Xml.Linq.XElement.%23ctor%2A> 并在需要时将其转换为 <xref:System.Xml.Linq.XAttribute.%23ctor%2A> 构造函数。</span><span class="sxs-lookup"><span data-stu-id="c96a3-179">The Visual Basic compiler converts the XML element literal into calls to the <xref:System.Xml.Linq.XElement.%23ctor%2A> constructor and, if it is required, the <xref:System.Xml.Linq.XAttribute.%23ctor%2A> constructor.</span></span>

## <a name="xml-namespaces"></a><span data-ttu-id="c96a3-180">XML 命名空间</span><span class="sxs-lookup"><span data-stu-id="c96a3-180">XML Namespaces</span></span>

<span data-ttu-id="c96a3-181">当你必须在代码中多次使用同一命名空间中的元素创建 XML 文本时，XML 命名空间前缀非常有用。</span><span class="sxs-lookup"><span data-stu-id="c96a3-181">XML namespace prefixes are useful when you have to create XML literals with elements from the same namespace many times in code.</span></span> <span data-ttu-id="c96a3-182">你可以使用全局 XML 命名空间前缀，该前缀是使用语句定义的 `Imports` ，或者是使用特性语法定义的本地前缀 `xmlns:xmlPrefix="xmlNamespace"` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-182">You can use global XML namespace prefixes, which you define by using the `Imports` statement, or local prefixes, which you define by using the `xmlns:xmlPrefix="xmlNamespace"` attribute syntax.</span></span> <span data-ttu-id="c96a3-183">有关详细信息，请参阅 [ (XML 命名空间) 的 Imports 语句 ](../statements/imports-statement-xml-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="c96a3-183">For more information, see [Imports Statement (XML Namespace)](../statements/imports-statement-xml-namespace.md).</span></span>

<span data-ttu-id="c96a3-184">根据 XML 命名空间的作用域规则，本地前缀优先于全局前缀。</span><span class="sxs-lookup"><span data-stu-id="c96a3-184">In accordance with the scoping rules for XML namespaces, local prefixes take precedence over global prefixes.</span></span> <span data-ttu-id="c96a3-185">但是，如果 XML 文本定义了 XML 命名空间，则该命名空间不能用于出现在嵌入表达式中的表达式。</span><span class="sxs-lookup"><span data-stu-id="c96a3-185">However, if an XML literal defines an XML namespace, that namespace is not available to expressions that appear in an embedded expression.</span></span> <span data-ttu-id="c96a3-186">嵌入的表达式只能访问全局 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="c96a3-186">The embedded expression can access only the global XML namespace.</span></span>

<span data-ttu-id="c96a3-187">Visual Basic 编译器将 XML 文本使用的每个全局 XML 命名空间转换为生成的代码中的一个本地命名空间定义。</span><span class="sxs-lookup"><span data-stu-id="c96a3-187">The Visual Basic compiler converts each global XML namespace that is used by an XML literal into a one local namespace definition in the generated code.</span></span> <span data-ttu-id="c96a3-188">不使用的全局 XML 命名空间不会出现在生成的代码中。</span><span class="sxs-lookup"><span data-stu-id="c96a3-188">Global XML namespaces that are not used do not appear in the generated code.</span></span>

## <a name="example"></a><span data-ttu-id="c96a3-189">示例</span><span class="sxs-lookup"><span data-stu-id="c96a3-189">Example</span></span>

<span data-ttu-id="c96a3-190">下面的示例演示如何创建一个具有两个嵌套空元素的简单 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="c96a3-190">The following example shows how to create a simple XML element that has two nested empty elements.</span></span>

[!code-vb[VbXMLSamples#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples9.vb#20)]

<span data-ttu-id="c96a3-191">该示例显示以下文本。</span><span class="sxs-lookup"><span data-stu-id="c96a3-191">The example displays the following text.</span></span> <span data-ttu-id="c96a3-192">请注意，文本将保留空元素的结构。</span><span class="sxs-lookup"><span data-stu-id="c96a3-192">Notice that the literal preserves the structure of the empty elements.</span></span>

```xml
<outer>
  <inner1></inner1>
  <inner2 />
</outer>
```

## <a name="example"></a><span data-ttu-id="c96a3-193">示例</span><span class="sxs-lookup"><span data-stu-id="c96a3-193">Example</span></span>

<span data-ttu-id="c96a3-194">下面的示例演示如何使用嵌入的表达式来命名元素并创建属性。</span><span class="sxs-lookup"><span data-stu-id="c96a3-194">The following example shows how to use embedded expressions to name an element and create attributes.</span></span>

[!code-vb[VbXMLSamples#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples9.vb#21)]

<span data-ttu-id="c96a3-195">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="c96a3-195">This code displays the following text:</span></span>

```xml
<book isbn="1234" author="My Author" year="1999" title="My Book" />
```

## <a name="example"></a><span data-ttu-id="c96a3-196">示例</span><span class="sxs-lookup"><span data-stu-id="c96a3-196">Example</span></span>

<span data-ttu-id="c96a3-197">下面的示例声明 `ns` 作为 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="c96a3-197">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="c96a3-198">然后，它使用命名空间的前缀创建 XML 文本，并显示该元素的最终形式。</span><span class="sxs-lookup"><span data-stu-id="c96a3-198">It then uses the prefix of the namespace to create an XML literal and displays the element's final form.</span></span>

[!code-vb[VbXMLSamples#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples10.vb#22)]

<span data-ttu-id="c96a3-199">此代码显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="c96a3-199">This code displays the following text:</span></span>

```xml
<ns:outer xmlns:ns="http://SomeNamespace">
  <ns:middle xmlns:ns="http://NewNamespace">
    <ns:inner1 />
    <inner2 xmlns="http://SomeNamespace" />
  </ns:middle>
</ns:outer>
```

<span data-ttu-id="c96a3-200">请注意，编译器将全局 XML 命名空间的前缀转换为 XML 命名空间的前缀定义。</span><span class="sxs-lookup"><span data-stu-id="c96a3-200">Notice that the compiler converted the prefix of the global XML namespace into a prefix definition for the XML namespace.</span></span> <span data-ttu-id="c96a3-201">\<ns:middle>元素重新定义元素的 XML 命名空间前缀 \<ns:inner1> 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-201">The \<ns:middle> element redefines the XML namespace prefix for the \<ns:inner1> element.</span></span> <span data-ttu-id="c96a3-202">但是， \<ns:inner2> 元素使用语句定义的命名空间 `Imports` 。</span><span class="sxs-lookup"><span data-stu-id="c96a3-202">However, the \<ns:inner2> element uses the namespace defined by the `Imports` statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="c96a3-203">请参阅</span><span class="sxs-lookup"><span data-stu-id="c96a3-203">See also</span></span>

- <xref:System.Xml.Linq.XElement>
- [<span data-ttu-id="c96a3-204">已声明的 XML 元素和属性的名称</span><span class="sxs-lookup"><span data-stu-id="c96a3-204">Names of Declared XML Elements and Attributes</span></span>](../../programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
- [<span data-ttu-id="c96a3-205">XML 注释文本</span><span class="sxs-lookup"><span data-stu-id="c96a3-205">XML Comment Literal</span></span>](xml-comment-literal.md)
- [<span data-ttu-id="c96a3-206">XML CDATA 文本</span><span class="sxs-lookup"><span data-stu-id="c96a3-206">XML CDATA Literal</span></span>](xml-cdata-literal.md)
- [<span data-ttu-id="c96a3-207">XML 文本</span><span class="sxs-lookup"><span data-stu-id="c96a3-207">XML Literals</span></span>](index.md)
- [<span data-ttu-id="c96a3-208">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="c96a3-208">Creating XML in Visual Basic</span></span>](../../programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="c96a3-209">XML 中的嵌入式表达式</span><span class="sxs-lookup"><span data-stu-id="c96a3-209">Embedded Expressions in XML</span></span>](../../programming-guide/language-features/xml/embedded-expressions-in-xml.md)
- [<span data-ttu-id="c96a3-210">Imports 语句（XML 命名空间）</span><span class="sxs-lookup"><span data-stu-id="c96a3-210">Imports Statement (XML Namespace)</span></span>](../statements/imports-statement-xml-namespace.md)

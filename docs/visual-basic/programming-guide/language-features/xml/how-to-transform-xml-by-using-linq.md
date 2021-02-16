---
description: '了解更多相关信息，请参阅如何：使用 LINQ (转换 XML Visual Basic) '
title: 如何：使用 LINQ 转换 XML
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], transforming
- LINQ to XML [Visual Basic], transforming XML
ms.assetid: 815687f4-0bc2-4c0b-adc6-d78744aa356f
ms.openlocfilehash: 67e6f5f94cd71d960f742b660d3f223137bbd6d4
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100483633"
---
# <a name="how-to-transform-xml-by-using-linq-visual-basic"></a><span data-ttu-id="9092d-103">如何：使用 LINQ 转换 XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9092d-103">How to: Transform XML by Using LINQ (Visual Basic)</span></span>

<span data-ttu-id="9092d-104">使用[Xml 文本](../../../language-reference/xml-literals/index.md)可以轻松地从一个源读取 XML，并将其转换为新的 xml 格式。</span><span class="sxs-lookup"><span data-stu-id="9092d-104">[XML Literals](../../../language-reference/xml-literals/index.md) make it easy to read XML from one source and transform it to a new XML format.</span></span> <span data-ttu-id="9092d-105">您可以利用 LINQ 查询来检索要转换的内容，或者将现有文档中的内容更改为新的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="9092d-105">You can take advantage of LINQ queries to retrieve the content to transform, or change content in an existing document to a new XML format.</span></span>

<span data-ttu-id="9092d-106">本主题中的示例将 XML 源文档中的内容转换为 HTML，以便在浏览器中查看。</span><span class="sxs-lookup"><span data-stu-id="9092d-106">The example in this topic transforms content from an XML source document to HTML to be viewed in a browser.</span></span>

[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]

### <a name="to-transform-an-xml-document"></a><span data-ttu-id="9092d-107">转换 XML 文档</span><span class="sxs-lookup"><span data-stu-id="9092d-107">To transform an XML document</span></span>

1. <span data-ttu-id="9092d-108">在 Visual Studio 中，在 " **控制台应用程序** " 项目模板中创建新的 Visual Basic 项目。</span><span class="sxs-lookup"><span data-stu-id="9092d-108">In Visual Studio, create a new Visual Basic project in the **Console Application** project template.</span></span>

2. <span data-ttu-id="9092d-109">双击在项目中创建的 Module1 文件以修改 Visual Basic 代码。</span><span class="sxs-lookup"><span data-stu-id="9092d-109">Double-click the Module1.vb file created in the project to modify the Visual Basic code.</span></span> <span data-ttu-id="9092d-110">将以下代码添加到 `Sub Main` `Module1` 模块的。</span><span class="sxs-lookup"><span data-stu-id="9092d-110">Add the following code to the `Sub Main` of the `Module1` module.</span></span> <span data-ttu-id="9092d-111">此代码将源 XML 文档创建为 <xref:System.Xml.Linq.XDocument> 对象。</span><span class="sxs-lookup"><span data-stu-id="9092d-111">This code creates the source XML document as an <xref:System.Xml.Linq.XDocument> object.</span></span>

    ```vb
    Dim catalog =
      <?xml version="1.0"?>
        <Catalog>
          <Book id="bk101">
            <Author>Garghentini, Davide</Author>
            <Title>XML Developer's Guide</Title>
            <Price>44.95</Price>
            <Description>
              An in-depth look at creating applications
              with <technology>XML</technology>. For
              <audience>beginners</audience> or
              <audience>advanced</audience> developers.
            </Description>
          </Book>
          <Book id="bk331">
            <Author>Spencer, Phil</Author>
            <Title>Developing Applications with Visual Basic .NET</Title>
            <Price>45.95</Price>
            <Description>
              Get the expert insights, practical code samples,
              and best practices you need
              to advance your expertise with <technology>Visual
              Basic .NET</technology>.
              Learn how to create faster, more reliable applications
              based on professional,
              pragmatic guidance by today's top <audience>developers</audience>.
            </Description>
          </Book>
        </Catalog>
    ```

     <span data-ttu-id="9092d-112">[如何：从文件、字符串或流加载 XML](how-to-load-xml-from-a-file-string-or-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="9092d-112">[How to: Load XML from a File, String, or Stream](how-to-load-xml-from-a-file-string-or-stream.md).</span></span>

3. <span data-ttu-id="9092d-113">在代码中创建源 XML 文档后，添加以下代码以检索该 \<Book> 对象中的所有元素，并将其转换为 HTML 文档。</span><span class="sxs-lookup"><span data-stu-id="9092d-113">After the code to create the source XML document, add the following code to retrieve all the \<Book> elements from the object and transform them into an HTML document.</span></span> <span data-ttu-id="9092d-114">\<Book>元素列表是通过使用 LINQ 查询创建的，该查询返回包含已转换的 HTML 的对象的集合 <xref:System.Xml.Linq.XElement> 。</span><span class="sxs-lookup"><span data-stu-id="9092d-114">The list of \<Book> elements is created by using a LINQ query that returns a collection of <xref:System.Xml.Linq.XElement> objects that contain the transformed HTML.</span></span> <span data-ttu-id="9092d-115">您可以使用嵌入式表达式将源文档中的值置于新的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="9092d-115">You can use embedded expressions to put the values from the source document in the new XML format.</span></span>

     <span data-ttu-id="9092d-116">通过使用方法将生成的 HTML 文档写入文件 <xref:System.Xml.Linq.XElement.Save%2A> 。</span><span class="sxs-lookup"><span data-stu-id="9092d-116">The resulting HTML document is written to a file by using the <xref:System.Xml.Linq.XElement.Save%2A> method.</span></span>

    ```vb
    Dim htmlOutput =
      <html>
        <body>
          <%= From book In catalog.<Catalog>.<Book>
              Select <div>
                       <h1><%= book.<Title>.Value %></h1>
                       <h3><%= "By " & book.<Author>.Value %></h3>
                        <h3><%= "Price = " & book.<Price>.Value %></h3>
                        <h2>Description</h2>
                        <%= TransformDescription(book.<Description>(0)) %>
                        <hr/>
                      </div> %>
        </body>
      </html>

    htmlOutput.Save("BookDescription.html")
    ```

4. <span data-ttu-id="9092d-117">在 `Sub Main` 之后 `Module1` ，添加一个新方法 (`Sub`) 将节点转换为 \<Description> 指定的 HTML 格式。</span><span class="sxs-lookup"><span data-stu-id="9092d-117">After `Sub Main` of `Module1`, add a new method (`Sub`) to transform a \<Description> node into the specified HTML format.</span></span> <span data-ttu-id="9092d-118">此方法由上一步中的代码调用，用于保留元素的格式 \<Description> 。</span><span class="sxs-lookup"><span data-stu-id="9092d-118">This method is called by the code in the previous step and is used to preserve the format of the \<Description> elements.</span></span>

     <span data-ttu-id="9092d-119">此方法用 HTML 替换元素的子元素 \<Description> 。</span><span class="sxs-lookup"><span data-stu-id="9092d-119">This method replaces sub-elements of the \<Description> element with HTML.</span></span> <span data-ttu-id="9092d-120">`ReplaceWith`方法用于保留子元素的位置。</span><span class="sxs-lookup"><span data-stu-id="9092d-120">The `ReplaceWith` method is used to preserve the location of the sub-elements.</span></span> <span data-ttu-id="9092d-121">元素的转换内容 \<Description> 包含在 HTML 段落中 (\<p>) 元素。</span><span class="sxs-lookup"><span data-stu-id="9092d-121">The transformed content of the \<Description> element is included in an HTML paragraph (\<p>) element.</span></span> <span data-ttu-id="9092d-122"><xref:System.Xml.Linq.XContainer.Nodes%2A>属性用于检索元素的转换内容 \<Description> 。</span><span class="sxs-lookup"><span data-stu-id="9092d-122">The <xref:System.Xml.Linq.XContainer.Nodes%2A> property is used to retrieve the transformed content of the \<Description> element.</span></span> <span data-ttu-id="9092d-123">这可确保子元素包含在转换后的内容中。</span><span class="sxs-lookup"><span data-stu-id="9092d-123">This ensures that sub-elements are included in the transformed content.</span></span>

     <span data-ttu-id="9092d-124">在的后面添加以下 `Sub Main` 代码 `Module1` 。</span><span class="sxs-lookup"><span data-stu-id="9092d-124">Add the following code after `Sub Main` of `Module1`.</span></span>

    ```vb
    Public Function TransformDescription(ByVal desc As XElement) As XElement

      ' Replace <technology> elements with <b>.
      Dim content = (From element In desc...<technology>).ToList()

      If content.Count > 0 Then
        For i = 0 To content.Count - 1
          content(i).ReplaceWith(<b><%= content(i).Value %></b>)
        Next
      End If

      ' Replace <audience> elements with <i>.
      content = (From element In desc...<audience>).ToList()

      If content.Count > 0 Then
        For i = 0 To content.Count - 1
          content(i).ReplaceWith(<i><%= content(i).Value %></i>)
        Next
      End If

      ' Return the updated contents of the <Description> element.
      Return <p><%= desc.Nodes %></p>
    End Function
    ```

5. <span data-ttu-id="9092d-125">保存所做更改。</span><span class="sxs-lookup"><span data-stu-id="9092d-125">Save your changes.</span></span>

6. <span data-ttu-id="9092d-126">按 F5 运行代码。</span><span class="sxs-lookup"><span data-stu-id="9092d-126">Press F5 to run the code.</span></span> <span data-ttu-id="9092d-127">生成的已保存文档将类似于以下内容：</span><span class="sxs-lookup"><span data-stu-id="9092d-127">The resulting saved document will resemble the following:</span></span>

    ```html
    <?xml version="1.0"?>
    <html>
      <body>
        <div>
          <h1>XML Developer's Guide</h1>
          <h3>By Garghentini, Davide</h3>
          <h3>Price = 44.95</h3>
          <h2>Description</h2>
          <p>
            An in-depth look at creating applications
            with <b>XML</b>. For
            <i>beginners</i> or
            <i>advanced</i> developers.
          </p>
          <hr />
        </div>
        <div>
          <h1>Developing Applications with Visual Basic .NET</h1>
          <h3>By Spencer, Phil</h3>
          <h3>Price = 45.95</h3>
          <h2>Description</h2>
          <p>
            Get the expert insights, practical code
            samples, and best practices you need
            to advance your expertise with <b>Visual
            Basic .NET</b>. Learn how to create faster,
            more reliable applications based on
            professional, pragmatic guidance by today's
            top <i>developers</i>.
          </p>
          <hr />
        </div>
      </body>
    </html>
    ```

## <a name="see-also"></a><span data-ttu-id="9092d-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="9092d-128">See also</span></span>

- [<span data-ttu-id="9092d-129">XML 文本</span><span class="sxs-lookup"><span data-stu-id="9092d-129">XML Literals</span></span>](../../../language-reference/xml-literals/index.md)
- [<span data-ttu-id="9092d-130">在 Visual Basic 中操作 XML</span><span class="sxs-lookup"><span data-stu-id="9092d-130">Manipulating XML in Visual Basic</span></span>](manipulating-xml.md)
- [<span data-ttu-id="9092d-131">XML</span><span class="sxs-lookup"><span data-stu-id="9092d-131">XML</span></span>](index.md)
- [<span data-ttu-id="9092d-132">如何：从文件、字符串或流加载 XML</span><span class="sxs-lookup"><span data-stu-id="9092d-132">How to: Load XML from a File, String, or Stream</span></span>](how-to-load-xml-from-a-file-string-or-stream.md)
- [<span data-ttu-id="9092d-133">LINQ</span><span class="sxs-lookup"><span data-stu-id="9092d-133">LINQ</span></span>](../linq/index.md)
- [<span data-ttu-id="9092d-134">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="9092d-134">Introduction to LINQ in Visual Basic</span></span>](../linq/introduction-to-linq.md)

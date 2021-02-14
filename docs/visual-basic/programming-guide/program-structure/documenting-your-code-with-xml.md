---
description: '了解详细信息：用 XML (Visual Basic 记录代码) '
title: 使用 XML 记录代码
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], documenting code
- XML comments, Visual Basic
- Visual Basic code, documenting with XML
ms.assetid: a0d35dc7-c5f9-4d74-92ff-a1c6f28d5235
ms.openlocfilehash: b554007bdd5183d0d92dc7ff62d08885f4b7f486
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476002"
---
# <a name="document-your-code-with-xml-visual-basic"></a><span data-ttu-id="1d645-103">使用 XML 记录代码 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1d645-103">Document your code with XML (Visual Basic)</span></span>

<span data-ttu-id="1d645-104">在 Visual Basic 中，可以使用 XML 记录代码。</span><span class="sxs-lookup"><span data-stu-id="1d645-104">In Visual Basic, you can document your code using XML.</span></span>

## <a name="xml-documentation-comments"></a><span data-ttu-id="1d645-105">XML 文档注释</span><span class="sxs-lookup"><span data-stu-id="1d645-105">XML documentation comments</span></span>

<span data-ttu-id="1d645-106">Visual Basic 提供了一种简单的方法来自动创建项目的 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="1d645-106">Visual Basic provides an easy way to automatically create XML documentation for projects.</span></span> <span data-ttu-id="1d645-107">可以为类型和成员自动生成 XML 主干，然后提供每个参数的摘要、描述性文档和其他备注。</span><span class="sxs-lookup"><span data-stu-id="1d645-107">You can automatically generate an XML skeleton for your types and members, and then provide summaries, descriptive documentation for each parameter, and other remarks.</span></span> <span data-ttu-id="1d645-108">使用适当的设置，XML 文档将自动发送到具有与项目相同的根文件名的 XML 文件中。</span><span class="sxs-lookup"><span data-stu-id="1d645-108">With the appropriate setup, the XML documentation is automatically emitted into an XML file with the same root file name as your project.</span></span> <span data-ttu-id="1d645-109">有关详细信息，请参阅 [-doc](../../reference/command-line-compiler/doc.md)。</span><span class="sxs-lookup"><span data-stu-id="1d645-109">For more information, see [-doc](../../reference/command-line-compiler/doc.md).</span></span>

<span data-ttu-id="1d645-110">可以使用 XML 文件或以其他方式将其作为 XML 来处理。</span><span class="sxs-lookup"><span data-stu-id="1d645-110">The XML file can be consumed or otherwise manipulated as XML.</span></span> <span data-ttu-id="1d645-111">此文件与项目的输出 .exe 或 .dll 文件位于同一目录中。</span><span class="sxs-lookup"><span data-stu-id="1d645-111">This file is located in the same directory as the output .exe or .dll file of your project.</span></span>

<span data-ttu-id="1d645-112">XML 文档以 `'''` 开头。</span><span class="sxs-lookup"><span data-stu-id="1d645-112">XML documentation starts with `'''`.</span></span> <span data-ttu-id="1d645-113">处理这些注释时存在一些限制：</span><span class="sxs-lookup"><span data-stu-id="1d645-113">The processing of these comments has some restrictions:</span></span>

- <span data-ttu-id="1d645-114">文档必须是格式正确的 XML。</span><span class="sxs-lookup"><span data-stu-id="1d645-114">The documentation must be well-formed XML.</span></span> <span data-ttu-id="1d645-115">如果 XML 格式不正确，则会生成警告，并且文档文件将会显示一条注释，指出遇到了错误。</span><span class="sxs-lookup"><span data-stu-id="1d645-115">If the XML is not well formed, a warning is generated and the documentation file contains a comment saying that an error was encountered.</span></span>

- <span data-ttu-id="1d645-116">开发人员可以随意创建自己的标记集。</span><span class="sxs-lookup"><span data-stu-id="1d645-116">Developers are free to create their own set of tags.</span></span> <span data-ttu-id="1d645-117">建议使用一组标记 (参阅 [XML 注释标记](../../language-reference/xmldoc/index.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1d645-117">There is a recommended set of tags (see [XML Comment Tags](../../language-reference/xmldoc/index.md)).</span></span> <span data-ttu-id="1d645-118">部分建议标记具有特殊含义：</span><span class="sxs-lookup"><span data-stu-id="1d645-118">Some of the recommended tags have special meanings:</span></span>

  - <span data-ttu-id="1d645-119">\<param> 标记用于描述参数。</span><span class="sxs-lookup"><span data-stu-id="1d645-119">The \<param> tag is used to describe parameters.</span></span> <span data-ttu-id="1d645-120">如果使用，编译器将验证该参数是否存在，以及文档是否描述了所有参数。</span><span class="sxs-lookup"><span data-stu-id="1d645-120">If used, the compiler will verify that the parameter exists and that all parameters are described in the documentation.</span></span> <span data-ttu-id="1d645-121">如果验证失败，编译器会发出警告。</span><span class="sxs-lookup"><span data-stu-id="1d645-121">If the verification fails, the compiler issues a warning.</span></span>

  - <span data-ttu-id="1d645-122">`cref` 属性可以附加到任何标记，以提供对代码元素的引用。</span><span class="sxs-lookup"><span data-stu-id="1d645-122">The `cref` attribute can be attached to any tag to provide a reference to a code element.</span></span> <span data-ttu-id="1d645-123">编译器验证此代码元素是否存在。</span><span class="sxs-lookup"><span data-stu-id="1d645-123">The compiler verifies that this code element exists.</span></span> <span data-ttu-id="1d645-124">如果验证失败，编译器会发出警告。</span><span class="sxs-lookup"><span data-stu-id="1d645-124">If the verification fails, the compiler issues a warning.</span></span> <span data-ttu-id="1d645-125">`Imports`查找特性中所述的类型时，编译器还会考虑所有语句 `cref` 。</span><span class="sxs-lookup"><span data-stu-id="1d645-125">The compiler also respects any `Imports` statements when looking for a type described in the `cref` attribute.</span></span>

  - <span data-ttu-id="1d645-126">\<summary>Visual Studio 中的 IntelliSense 使用标记显示关于类型或成员的其他信息。</span><span class="sxs-lookup"><span data-stu-id="1d645-126">The \<summary> tag is used by IntelliSense in Visual Studio to display additional information about a type or member.</span></span>

## <a name="related-sections"></a><span data-ttu-id="1d645-127">相关章节</span><span class="sxs-lookup"><span data-stu-id="1d645-127">Related sections</span></span>

<span data-ttu-id="1d645-128">有关创建包含文档注释的 XML 文件的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="1d645-128">For details on creating an XML file with documentation comments, see the following topics:</span></span>

- [<span data-ttu-id="1d645-129">-doc</span><span class="sxs-lookup"><span data-stu-id="1d645-129">-doc</span></span>](../../reference/command-line-compiler/doc.md)

- [<span data-ttu-id="1d645-130">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="1d645-130">XML Comment Tags</span></span>](../../language-reference/xmldoc/index.md)

- [<span data-ttu-id="1d645-131">处理 XML 文件</span><span class="sxs-lookup"><span data-stu-id="1d645-131">Processing the XML File</span></span>](processing-the-xml-file.md)

- [<span data-ttu-id="1d645-132">如何：创建 XML 文档</span><span class="sxs-lookup"><span data-stu-id="1d645-132">How to: Create XML Documentation</span></span>](how-to-create-xml-documentation.md)

- [<span data-ttu-id="1d645-133">Visual Studio 中的 XML 工具</span><span class="sxs-lookup"><span data-stu-id="1d645-133">XML Tools in Visual Studio</span></span>](/visualstudio/xml-tools/xml-tools-in-visual-studio)

## <a name="see-also"></a><span data-ttu-id="1d645-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d645-134">See also</span></span>

- [<span data-ttu-id="1d645-135">使用 Visual Basic 开发应用程序</span><span class="sxs-lookup"><span data-stu-id="1d645-135">Developing Applications with Visual Basic</span></span>](../../developing-apps/index.md)
- [<span data-ttu-id="1d645-136">Visual Basic 编程指南</span><span class="sxs-lookup"><span data-stu-id="1d645-136">Visual Basic Programming Guide</span></span>](../index.md)

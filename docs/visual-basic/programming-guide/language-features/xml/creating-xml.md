---
description: 了解详细信息：在 Visual Basic 中创建 XML
title: 创建 XML
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], creating
- LINQ to XML [Visual Basic], creating XML
- XML literals [Visual Basic], creating
ms.assetid: 8ae29ec5-e5fb-4137-9df5-60a288df7045
ms.openlocfilehash: 9511253791720d1f45e00669b0abc41a45237f63
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100431641"
---
# <a name="creating-xml-in-visual-basic"></a><span data-ttu-id="b5b2e-103">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="b5b2e-103">Creating XML in Visual Basic</span></span>

<span data-ttu-id="b5b2e-104">Visual Basic 使你能够直接在代码中使用 *XML 文本* 。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-104">Visual Basic enables you to use *XML literals* directly in your code.</span></span> <span data-ttu-id="b5b2e-105">XML 文本语法表示 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 对象，它类似于 XML 1.0 语法。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-105">The XML literal syntax represents [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objects, and it is similar to the XML 1.0 syntax.</span></span> <span data-ttu-id="b5b2e-106">这样可以更轻松地以编程方式创建 XML 元素、文档和片段，因为你的代码具有与最终 XML 相同的结构。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-106">This makes it easier to create XML elements, documents, and fragments programmatically because your code has the same structure as the final XML.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b5b2e-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="b5b2e-107">In This Section</span></span>  
  
|<span data-ttu-id="b5b2e-108">术语</span><span class="sxs-lookup"><span data-stu-id="b5b2e-108">Term</span></span>|<span data-ttu-id="b5b2e-109">定义</span><span class="sxs-lookup"><span data-stu-id="b5b2e-109">Definition</span></span>|  
|---|---|  
|[<span data-ttu-id="b5b2e-110">XML 文本概述</span><span class="sxs-lookup"><span data-stu-id="b5b2e-110">XML Literals Overview</span></span>](xml-literals-overview.md)|<span data-ttu-id="b5b2e-111">XML 文本及其相关方式的简介 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-111">Introduction to XML literals and how they relate to [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span></span>|  
|[<span data-ttu-id="b5b2e-112">XML 中的嵌入式表达式</span><span class="sxs-lookup"><span data-stu-id="b5b2e-112">Embedded Expressions in XML</span></span>](embedded-expressions-in-xml.md)|<span data-ttu-id="b5b2e-113">介绍如何在 XML 文本中使用嵌入表达式。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-113">Describes how to use embedded expressions in XML literals.</span></span>|  
|[<span data-ttu-id="b5b2e-114">如何：创建 XML 文本</span><span class="sxs-lookup"><span data-stu-id="b5b2e-114">How to: Create XML Literals</span></span>](how-to-create-xml-literals.md)|<span data-ttu-id="b5b2e-115">介绍如何在代码中使用 XML 文本创建 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-115">Describes how to create an XML element in code by using an XML literal.</span></span>|  
|[<span data-ttu-id="b5b2e-116">XML 文本中的空白</span><span class="sxs-lookup"><span data-stu-id="b5b2e-116">White Space in XML Literals</span></span>](white-space-in-xml-literals.md)|<span data-ttu-id="b5b2e-117">介绍 Visual Basic 如何处理 XML 文本中的空格。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-117">Describes how Visual Basic treats white space in XML literals.</span></span>|  
|[<span data-ttu-id="b5b2e-118">XML 文本和 XML 1.0 规范</span><span class="sxs-lookup"><span data-stu-id="b5b2e-118">XML Literals and the XML 1.0 Specification</span></span>](xml-literals-and-the-xml-1-0-specification.md)|<span data-ttu-id="b5b2e-119">介绍 Visual Basic 中的 XML 文本语法如何与 XML 1.0 规范相关。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-119">Describes how the XML literal syntax in Visual Basic relates to the XML 1.0 specification.</span></span>|  
|[<span data-ttu-id="b5b2e-120">如何：在 XML 文本中嵌入表达式</span><span class="sxs-lookup"><span data-stu-id="b5b2e-120">How to: Embed Expressions in XML Literals</span></span>](how-to-embed-expressions-in-xml-literals.md)|<span data-ttu-id="b5b2e-121">介绍如何使用 XML 文本中的嵌入表达式在运行时创建内容。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-121">Describes how to use embedded expressions in XML literals to create content at run time.</span></span>|  
|[<span data-ttu-id="b5b2e-122">已声明的 XML 元素和属性的名称</span><span class="sxs-lookup"><span data-stu-id="b5b2e-122">Names of Declared XML Elements and Attributes</span></span>](names-of-declared-xml-elements-and-attributes.md)|<span data-ttu-id="b5b2e-123">介绍命名 XML 元素和属性的准则。</span><span class="sxs-lookup"><span data-stu-id="b5b2e-123">Describes guidelines for naming XML elements and attributes.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b5b2e-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5b2e-124">See also</span></span>

- [<span data-ttu-id="b5b2e-125">XML</span><span class="sxs-lookup"><span data-stu-id="b5b2e-125">XML</span></span>](index.md)

---
description: '了解详细信息：已声明的 XML 元素和属性的名称 (Visual Basic) '
title: 已声明的 XML 元素和属性的名称
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [XML in Visual Basic]
- element names [XML in Visual Basic]
- names in XML literals [Visual Basic]
- attribute names [XML in Visual Basic]
- XML literals [Visual Basic], element names
ms.assetid: cc110118-b6cf-4ff9-a4e4-6233c90c9fbf
ms.openlocfilehash: 0c5d049a7d877a23562b91c5d7b3306d8e68ea3a
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100422726"
---
# <a name="names-of-declared-xml-elements-and-attributes-visual-basic"></a><span data-ttu-id="ded92-103">已声明的 XML 元素和特性的名称 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ded92-103">Names of Declared XML Elements and Attributes (Visual Basic)</span></span>

<span data-ttu-id="ded92-104">本主题提供了在 XML 文本中命名 XML 元素和属性的 Visual Basic 准则。</span><span class="sxs-lookup"><span data-stu-id="ded92-104">This topic provides Visual Basic guidelines for naming XML elements and attributes in XML literals.</span></span>  <span data-ttu-id="ded92-105">在 XML 文本中，可以指定本地名称或限定名称。</span><span class="sxs-lookup"><span data-stu-id="ded92-105">In an XML literal, you can specify a local name or a qualified name.</span></span> <span data-ttu-id="ded92-106">限定名由 XML 命名空间前缀、冒号和本地名称组成。</span><span class="sxs-lookup"><span data-stu-id="ded92-106">A qualified name consists of an XML namespace prefix, a colon, and a local name.</span></span> <span data-ttu-id="ded92-107">有关 XML 命名空间前缀的详细信息，请参阅 [Xml 元素文本](../../../language-reference/xml-literals/xml-element-literal.md)。</span><span class="sxs-lookup"><span data-stu-id="ded92-107">For more information about XML namespace prefixes, see [XML Element Literal](../../../language-reference/xml-literals/xml-element-literal.md).</span></span>  
  
## <a name="rules"></a><span data-ttu-id="ded92-108">规则</span><span class="sxs-lookup"><span data-stu-id="ded92-108">Rules</span></span>  

 <span data-ttu-id="ded92-109">Visual Basic 中的元素或属性的本地名称必须遵循以下规则。</span><span class="sxs-lookup"><span data-stu-id="ded92-109">A local name of an element or attribute in Visual Basic must adhere to the following rules.</span></span>  
  
- <span data-ttu-id="ded92-110">它可以从命名空间开始。</span><span class="sxs-lookup"><span data-stu-id="ded92-110">It can begin with a namespace.</span></span> <span data-ttu-id="ded92-111">它必须以字母字符或下划线开头 (`_`) 。</span><span class="sxs-lookup"><span data-stu-id="ded92-111">It must begin with an alphabetical character or an underscore (`_`).</span></span>  
  
- <span data-ttu-id="ded92-112">它必须只包含字母字符、十进制数字、下划线、句点 ( ) 和连字符 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="ded92-112">It must contain only alphabetical characters, decimal digits, underscores, periods (.), and hyphens (-).</span></span>  
  
- <span data-ttu-id="ded92-113">长度不得超过1024个字符。</span><span class="sxs-lookup"><span data-stu-id="ded92-113">It must not be more than 1,024 characters long.</span></span>  
  
- <span data-ttu-id="ded92-114">名称中出现的冒号指示命名空间分界。</span><span class="sxs-lookup"><span data-stu-id="ded92-114">Colons that appear in names indicate namespace demarcation.</span></span> <span data-ttu-id="ded92-115">因此，您可以使用冒号来指定特定名称的 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="ded92-115">Therefore, you can use colons only to specify an XML namespace for a particular name.</span></span>  
  
 <span data-ttu-id="ded92-116">此外，还应遵循以下准则。</span><span class="sxs-lookup"><span data-stu-id="ded92-116">In addition, you should adhere to the following guideline.</span></span>  
  
- <span data-ttu-id="ded92-117">XML 1.0 规范保留以字符串 "XML" 开头、大小写不同的所有名称。</span><span class="sxs-lookup"><span data-stu-id="ded92-117">The XML 1.0 specification reserves all names starting with the string "xml", of any capitalization variation.</span></span> <span data-ttu-id="ded92-118">因此，请不要将这些名称用于元素和属性名称。</span><span class="sxs-lookup"><span data-stu-id="ded92-118">Therefore, do not use those names for your element and attribute names.</span></span>  
  
### <a name="name-length-guidelines"></a><span data-ttu-id="ded92-119">名称长度准则</span><span class="sxs-lookup"><span data-stu-id="ded92-119">Name Length Guidelines</span></span>  

 <span data-ttu-id="ded92-120">在实际情况下，名称应尽可能简短，同时仍能清楚地确定元素的性质。</span><span class="sxs-lookup"><span data-stu-id="ded92-120">As a practical matter, a name should be as short as possible while still clearly identifying the nature of the element.</span></span> <span data-ttu-id="ded92-121">这可以提高代码的可读性，并减少行长度和源文件大小。</span><span class="sxs-lookup"><span data-stu-id="ded92-121">This improves the readability of your code and reduces line length and source-file size.</span></span>  
  
 <span data-ttu-id="ded92-122">但是，名称不应太短，因为它不能充分描述元素或代码如何使用它。</span><span class="sxs-lookup"><span data-stu-id="ded92-122">However, your name should not be so short that it does not adequately describe the element or how your code uses it.</span></span> <span data-ttu-id="ded92-123">这对于代码的可读性非常重要。</span><span class="sxs-lookup"><span data-stu-id="ded92-123">This is important for the readability of your code.</span></span> <span data-ttu-id="ded92-124">如果其他人正在尝试理解它，或者你在写入它后你需要很长的时间，则适当的元素名称可节省时间。</span><span class="sxs-lookup"><span data-stu-id="ded92-124">If somebody else is trying to understand it, or if you yourself are looking at it a long time after you wrote it, appropriate element names can save time.</span></span>  
  
## <a name="case-sensitivity-in-names"></a><span data-ttu-id="ded92-125">名称区分大小写</span><span class="sxs-lookup"><span data-stu-id="ded92-125">Case Sensitivity in Names</span></span>  

 <span data-ttu-id="ded92-126">XML 元素名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="ded92-126">XML element names are case sensitive.</span></span> <span data-ttu-id="ded92-127">这意味着，当 Visual Basic 编译器仅对字母大小写不同的两个名称进行比较时，它会将它们解释为不同的名称。</span><span class="sxs-lookup"><span data-stu-id="ded92-127">This means that when the Visual Basic compiler compares two names that differ in alphabetical case only, it interprets them as different names.</span></span> <span data-ttu-id="ded92-128">例如，它将 `ABC` 和 `abc` 引用为单独的元素。</span><span class="sxs-lookup"><span data-stu-id="ded92-128">For example, it interprets `ABC` and `abc` as referring to separate elements.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="ded92-129">XML 命名空间</span><span class="sxs-lookup"><span data-stu-id="ded92-129">XML Namespaces</span></span>  

 <span data-ttu-id="ded92-130">创建 XML 元素文本时，可以指定元素名称的 XML 命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="ded92-130">When creating an XML element literal, you can specify the XML namespace prefix for the element name.</span></span> <span data-ttu-id="ded92-131">有关详细信息，请参阅 [XML 元素文本](../../../language-reference/xml-literals/xml-element-literal.md)。</span><span class="sxs-lookup"><span data-stu-id="ded92-131">For more information, see [XML Element Literal](../../../language-reference/xml-literals/xml-element-literal.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ded92-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="ded92-132">See also</span></span>

- [<span data-ttu-id="ded92-133">在 Visual Basic 中创建 XML</span><span class="sxs-lookup"><span data-stu-id="ded92-133">Creating XML in Visual Basic</span></span>](creating-xml.md)
- [<span data-ttu-id="ded92-134">XML 元素文本</span><span class="sxs-lookup"><span data-stu-id="ded92-134">XML Element Literal</span></span>](../../../language-reference/xml-literals/xml-element-literal.md)

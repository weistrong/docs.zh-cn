---
description: '了解详细信息：建议用于文档注释的 XML 标记 (Visual Basic) '
title: 建议用于文档注释的 XML 标记
ms.date: 07/20/2015
f1_keywords:
- vb.XmlDocComment
helpviewer_keywords:
- tags, XML
- XML comments, recommended tags [Visual Basic]
- comments, recommended XML tags
ms.assetid: 294e0736-ff1e-498e-af83-6db71ed41a72
ms.openlocfilehash: 5d3451d98b66817de143cfbddbcb6121de57ca8b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787443"
---
# <a name="recommended-xml-tags-for-documentation-comments-visual-basic"></a><span data-ttu-id="f641c-103">建议的用于文档注释的 XML 标记 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f641c-103">Recommended XML Tags for Documentation Comments (Visual Basic)</span></span>

<span data-ttu-id="f641c-104">Visual Basic 编译器可以在代码中将文档注释处理到 XML 文件中。</span><span class="sxs-lookup"><span data-stu-id="f641c-104">The Visual Basic compiler can process documentation comments in your code to an XML file.</span></span> <span data-ttu-id="f641c-105">您可以使用其他工具将 XML 文件处理到文档中。</span><span class="sxs-lookup"><span data-stu-id="f641c-105">You can use additional tools to process the XML file into documentation.</span></span>  
  
 <span data-ttu-id="f641c-106">允许对代码构造（如类型和类型成员）使用 XML 注释。</span><span class="sxs-lookup"><span data-stu-id="f641c-106">XML comments are allowed on code constructs such as types and type members.</span></span> <span data-ttu-id="f641c-107">对于分部类型，只有一个类型的部分可以有 XML 注释，尽管注释其成员没有限制。</span><span class="sxs-lookup"><span data-stu-id="f641c-107">For partial types, only one part of the type can have XML comments, although there is no restriction on commenting its members.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f641c-108">文档注释不能应用于命名空间。</span><span class="sxs-lookup"><span data-stu-id="f641c-108">Documentation comments cannot be applied to namespaces.</span></span> <span data-ttu-id="f641c-109">原因是一个命名空间可以跨多个程序集，而不是所有程序集都必须同时加载。</span><span class="sxs-lookup"><span data-stu-id="f641c-109">The reason is that one namespace can span several assemblies, and not all assemblies have to be loaded at the same time.</span></span>  
  
 <span data-ttu-id="f641c-110">编译器将处理任何为有效 XML 的标记。</span><span class="sxs-lookup"><span data-stu-id="f641c-110">The compiler processes any tag that is valid XML.</span></span> <span data-ttu-id="f641c-111">以下标记提供用户文档中的常用功能。</span><span class="sxs-lookup"><span data-stu-id="f641c-111">The following tags provide commonly used functionality in user documentation.</span></span>  
  
||||  
|---|---|---|  
|[\<c>](c.md)|[\<code>](code.md)|[\<example>](example.md)|  
|<span data-ttu-id="f641c-112">[\<exception>](exception.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-112">[\<exception>](exception.md) <sup>1</sup></span></span>|<span data-ttu-id="f641c-113">[\<include>](include.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-113">[\<include>](include.md) <sup>1</sup></span></span>|[\<list>](list.md)|  
|[\<para>](para.md)|<span data-ttu-id="f641c-114">[\<param>](param.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-114">[\<param>](param.md) <sup>1</sup></span></span>|[\<paramref>](paramref.md)|  
|<span data-ttu-id="f641c-115">[\<permission>](permission.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-115">[\<permission>](permission.md) <sup>1</sup></span></span>|[\<remarks>](remarks.md)|[\<returns>](returns.md)|  
|<span data-ttu-id="f641c-116">[\<see>](see.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-116">[\<see>](see.md) <sup>1</sup></span></span>|<span data-ttu-id="f641c-117">[\<seealso>](seealso.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-117">[\<seealso>](seealso.md) <sup>1</sup></span></span>|[\<summary>](summary.md)|  
|<span data-ttu-id="f641c-118">[\<typeparam>](typeparam.md)<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f641c-118">[\<typeparam>](typeparam.md) <sup>1</sup></span></span>|[\<value>](value.md)||  
  
 <span data-ttu-id="f641c-119"> (<sup>1</sup> 编译器验证语法。 ) </span><span class="sxs-lookup"><span data-stu-id="f641c-119">(<sup>1</sup> The compiler verifies syntax.)</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f641c-120">如果要在文档注释的文本中显示尖括号，请使用 `&lt;` 和 `&gt;` 。</span><span class="sxs-lookup"><span data-stu-id="f641c-120">If you want angle brackets to appear in the text of a documentation comment, use `&lt;` and `&gt;`.</span></span> <span data-ttu-id="f641c-121">例如，该字符串 `"&lt;text in angle brackets&gt;"` 将显示为 `<text in angle brackets>` 。</span><span class="sxs-lookup"><span data-stu-id="f641c-121">For example, the string `"&lt;text in angle brackets&gt;"` will appear as `<text in angle brackets>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f641c-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="f641c-122">See also</span></span>

- [<span data-ttu-id="f641c-123">使用 XML 记录代码</span><span class="sxs-lookup"><span data-stu-id="f641c-123">Documenting Your Code with XML</span></span>](../../programming-guide/program-structure/documenting-your-code-with-xml.md)
- [<span data-ttu-id="f641c-124">-doc</span><span class="sxs-lookup"><span data-stu-id="f641c-124">-doc</span></span>](../../reference/command-line-compiler/doc.md)
- [<span data-ttu-id="f641c-125">如何：创建 XML 文档</span><span class="sxs-lookup"><span data-stu-id="f641c-125">How to: Create XML Documentation</span></span>](../../programming-guide/program-structure/how-to-create-xml-documentation.md)

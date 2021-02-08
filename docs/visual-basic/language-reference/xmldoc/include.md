---
description: 了解详细信息： <include> (Visual Basic)
title: <include>
ms.date: 07/20/2015
helpviewer_keywords:
- include XML tag
- <include> XML tag
ms.assetid: ba8e9173-82cd-460b-8938-a075a2dfb36d
ms.openlocfilehash: 8207b74ed74bd529f2da865777e287320b23d293
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787456"
---
# <a name="include-visual-basic"></a><span data-ttu-id="c0802-103">\<include> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c0802-103">\<include> (Visual Basic)</span></span>

<span data-ttu-id="c0802-104">引用另一个文件，该文件描述源代码中的类型和成员。</span><span class="sxs-lookup"><span data-stu-id="c0802-104">Refers to another file that describes the types and members in your source code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0802-105">语法</span><span class="sxs-lookup"><span data-stu-id="c0802-105">Syntax</span></span>  
  
```xml  
<include file="filename" path="tagpath[@name='id']" />  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0802-106">参数</span><span class="sxs-lookup"><span data-stu-id="c0802-106">Parameters</span></span>  

 `filename`  
 <span data-ttu-id="c0802-107">必需。</span><span class="sxs-lookup"><span data-stu-id="c0802-107">Required.</span></span> <span data-ttu-id="c0802-108">包含文档的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="c0802-108">The name of the file containing the documentation.</span></span> <span data-ttu-id="c0802-109">可使用路径来限定文件名。</span><span class="sxs-lookup"><span data-stu-id="c0802-109">The file name can be qualified with a path.</span></span> <span data-ttu-id="c0802-110">用 `filename` 双引号将 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="c0802-110">Enclose `filename` in double quotation marks (" ").</span></span>  
  
 `tagpath`  
 <span data-ttu-id="c0802-111">必需。</span><span class="sxs-lookup"><span data-stu-id="c0802-111">Required.</span></span> <span data-ttu-id="c0802-112">`filename` 中标记的路径，它指向标记 `name`。</span><span class="sxs-lookup"><span data-stu-id="c0802-112">The path of the tags in `filename` that leads to the tag `name`.</span></span> <span data-ttu-id="c0802-113">将路径用双引号引起来 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="c0802-113">Enclose the path in double quotation marks (" ").</span></span>  
  
 `name`  
 <span data-ttu-id="c0802-114">必需。</span><span class="sxs-lookup"><span data-stu-id="c0802-114">Required.</span></span> <span data-ttu-id="c0802-115">注释前面的标记中的名称说明符。</span><span class="sxs-lookup"><span data-stu-id="c0802-115">The name specifier in the tag that precedes the comments.</span></span> <span data-ttu-id="c0802-116">`Name` 将有一个 `id` 。</span><span class="sxs-lookup"><span data-stu-id="c0802-116">`Name` will have an `id`.</span></span>  
  
 `id`  
 <span data-ttu-id="c0802-117">必需。</span><span class="sxs-lookup"><span data-stu-id="c0802-117">Required.</span></span> <span data-ttu-id="c0802-118">标记的 ID（位于注释之前）。</span><span class="sxs-lookup"><span data-stu-id="c0802-118">The ID for the tag that precedes the comments.</span></span> <span data-ttu-id="c0802-119">将 ID 括在单引号中 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="c0802-119">Enclose the ID in single quotation marks (' ').</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0802-120">备注</span><span class="sxs-lookup"><span data-stu-id="c0802-120">Remarks</span></span>  

 <span data-ttu-id="c0802-121">使用 `<include>` 标记来引用另一个文件中描述源代码中的类型和成员的注释。</span><span class="sxs-lookup"><span data-stu-id="c0802-121">Use the `<include>` tag to refer to comments in another file that describe the types and members in your source code.</span></span> <span data-ttu-id="c0802-122">这是对直接在源代码文件中放入文档注释的替代方法。</span><span class="sxs-lookup"><span data-stu-id="c0802-122">This is an alternative to placing documentation comments directly in your source code file.</span></span>  
  
 <span data-ttu-id="c0802-123">`<include>`标记使用 W3C XML Path 语言 (XPath) 版本1.0 建议。</span><span class="sxs-lookup"><span data-stu-id="c0802-123">The `<include>` tag uses the W3C XML Path Language (XPath) Version 1.0 Recommendation.</span></span> <span data-ttu-id="c0802-124">有关自定义使用方式的详细信息 `<include>` ，请参阅 <https://www.w3.org/TR/xpath> 。</span><span class="sxs-lookup"><span data-stu-id="c0802-124">For more information about ways to customize your `<include>` use, see <https://www.w3.org/TR/xpath>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c0802-125">示例</span><span class="sxs-lookup"><span data-stu-id="c0802-125">Example</span></span>  

 <span data-ttu-id="c0802-126">此示例使用 `<include>` 标记从名为的文件导入成员文档注释 `commentFile.xml` 。</span><span class="sxs-lookup"><span data-stu-id="c0802-126">This example uses the `<include>` tag to import member documentation comments from a file called `commentFile.xml`.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#4)]  
  
 <span data-ttu-id="c0802-127">的格式如下所示 `commentFile.xml` 。</span><span class="sxs-lookup"><span data-stu-id="c0802-127">The format of the `commentFile.xml` is as follows.</span></span>  
  
```xml  
<Docs>  
<Members name="Open">  
<summary>Opens a file.</summary>  
<param name="filename">File name to open.</param>  
</Members>  
<Members name="Close">  
<summary>Closes a file.</summary>  
<param name="filename">File name to close.</param>  
</Members>  
</Docs>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c0802-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0802-128">See also</span></span>

- [<span data-ttu-id="c0802-129">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="c0802-129">XML Comment Tags</span></span>](index.md)

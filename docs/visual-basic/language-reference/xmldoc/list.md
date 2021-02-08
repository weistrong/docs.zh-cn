---
description: 了解详细信息： <list> (Visual Basic)
title: <list>
ms.date: 07/20/2015
helpviewer_keywords:
- listheader XML tag
- <item> XML tag
- <list> XML tag
- <listheader> XML tag
- term XML tag
- list XML tag
- <description> XML tag
- description XML tag
- item XML tag
- <term> XML tag
ms.assetid: ec35fced-d58e-4520-a764-0691256e014b
ms.openlocfilehash: c9e2e8d1c370bfdeefae4a8f19b25acc6a336ecc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787430"
---
# <a name="list-visual-basic"></a><span data-ttu-id="179f8-103">\<list> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="179f8-103">\<list> (Visual Basic)</span></span>

<span data-ttu-id="179f8-104">定义列表或表。</span><span class="sxs-lookup"><span data-stu-id="179f8-104">Defines a list or table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="179f8-105">语法</span><span class="sxs-lookup"><span data-stu-id="179f8-105">Syntax</span></span>  
  
```xml  
<list type="type">  
   <listheader>  
      <term>term</term>  
      <description>description</description>  
   </listheader>  
   <item>  
      <term>term</term>  
      <description>description</description>  
   </item>  
</list>  
```  
  
## <a name="parameters"></a><span data-ttu-id="179f8-106">参数</span><span class="sxs-lookup"><span data-stu-id="179f8-106">Parameters</span></span>  

 `type`  
 <span data-ttu-id="179f8-107">列表的类型。</span><span class="sxs-lookup"><span data-stu-id="179f8-107">The type of the list.</span></span> <span data-ttu-id="179f8-108">必须是项目符号列表的 "项目符号"、编号列表的 "数字" 或两列表的 "表"。</span><span class="sxs-lookup"><span data-stu-id="179f8-108">Must be a "bullet" for a bulleted list, "number" for a numbered list, or "table" for a two-column table.</span></span>  
  
 `term`  
 <span data-ttu-id="179f8-109">仅当为 "table" 时才使用 `type` 。</span><span class="sxs-lookup"><span data-stu-id="179f8-109">Only used when `type` is "table."</span></span> <span data-ttu-id="179f8-110">要定义的术语，在 description 标记中定义。</span><span class="sxs-lookup"><span data-stu-id="179f8-110">A term to define, which is defined in the description tag.</span></span>  
  
 `description`  
 <span data-ttu-id="179f8-111">当为 "表" 时，为列表中的项，而 "表" 是的 `type` `description` `type` `description` 定义 `term` 。</span><span class="sxs-lookup"><span data-stu-id="179f8-111">When `type` is "bullet" or "number," `description` is an item in the list When `type` is "table," `description` is the definition of `term`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="179f8-112">备注</span><span class="sxs-lookup"><span data-stu-id="179f8-112">Remarks</span></span>  

 <span data-ttu-id="179f8-113">`<listheader>`块定义表或定义列表的标题。</span><span class="sxs-lookup"><span data-stu-id="179f8-113">The `<listheader>` block defines the heading of either a table or definition list.</span></span> <span data-ttu-id="179f8-114">定义表时，只需为标题中的提供一个条目 `term` 。</span><span class="sxs-lookup"><span data-stu-id="179f8-114">When defining a table, you only have to supply an entry for `term` in the heading.</span></span>  
  
 <span data-ttu-id="179f8-115">列表中的每个项均使用 `<item>` 块指定。</span><span class="sxs-lookup"><span data-stu-id="179f8-115">Each item in the list is specified with an `<item>` block.</span></span> <span data-ttu-id="179f8-116">创建定义列表时，必须同时指定 `term` 和 `description` 。</span><span class="sxs-lookup"><span data-stu-id="179f8-116">When creating a definition list, you must specify both `term` and `description`.</span></span> <span data-ttu-id="179f8-117">但是，对于表、项目符号列表或编号列表，你只需为提供一个条目 `description` 。</span><span class="sxs-lookup"><span data-stu-id="179f8-117">However, for a table, bulleted list, or numbered list, you only have to supply an entry for `description`.</span></span>  
  
 <span data-ttu-id="179f8-118">列表或表可根据需要具有多个 `<item>` 块。</span><span class="sxs-lookup"><span data-stu-id="179f8-118">A list or table can have as many `<item>` blocks as needed.</span></span>  
  
 <span data-ttu-id="179f8-119">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="179f8-119">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="179f8-120">示例</span><span class="sxs-lookup"><span data-stu-id="179f8-120">Example</span></span>  

 <span data-ttu-id="179f8-121">此示例使用 `<list>` 标记在 "备注" 部分中定义项目符号列表。</span><span class="sxs-lookup"><span data-stu-id="179f8-121">This example uses the `<list>` tag to define a bulleted list in the remarks section.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="179f8-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="179f8-122">See also</span></span>

- [<span data-ttu-id="179f8-123">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="179f8-123">XML Comment Tags</span></span>](index.md)

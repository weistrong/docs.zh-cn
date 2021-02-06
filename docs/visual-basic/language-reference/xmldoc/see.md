---
description: '了解详细信息： <see> (Visual Basic) '
title: <see>
ms.date: 07/20/2015
helpviewer_keywords:
- see XML tag
- <see> XML tag
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
ms.openlocfilehash: 46dd67710f83d6c4549ddfeb6b7bbc1503b7aa1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640337"
---
# <a name="see-visual-basic"></a><span data-ttu-id="bc5cc-102">\<see> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bc5cc-102">\<see> (Visual Basic)</span></span>

<span data-ttu-id="bc5cc-103">指定指向另一个成员的链接。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-103">Specifies a link to another member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc5cc-104">语法</span><span class="sxs-lookup"><span data-stu-id="bc5cc-104">Syntax</span></span>  
  
```xml  
<see cref="member"/>  
```  
  
## <a name="parameters"></a><span data-ttu-id="bc5cc-105">参数</span><span class="sxs-lookup"><span data-stu-id="bc5cc-105">Parameters</span></span>  

 `member`  
 <span data-ttu-id="bc5cc-106">对可从当前编译环境调用的成员或字段的引用。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="bc5cc-107">编译器检查是否存在给定的码位元素，并将 `member` 传递到输出 XML 中的元素名称。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.</span></span> <span data-ttu-id="bc5cc-108">`member` 必须出现在双引号 (" ") 内。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-108">`member` must appear within double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bc5cc-109">备注</span><span class="sxs-lookup"><span data-stu-id="bc5cc-109">Remarks</span></span>  

 <span data-ttu-id="bc5cc-110">使用 `<see>` 标记可以指定文本内的链接。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-110">Use the `<see>` tag to specify a link from within text.</span></span> <span data-ttu-id="bc5cc-111">用于 [\<seealso>](seealso.md) 指示你可能希望在 "另请参见" 部分中显示的文本。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-111">Use [\<seealso>](seealso.md) to indicate text that you might want to appear in a "See Also" section.</span></span>  
  
 <span data-ttu-id="bc5cc-112">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-112">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc5cc-113">示例</span><span class="sxs-lookup"><span data-stu-id="bc5cc-113">Example</span></span>  

 <span data-ttu-id="bc5cc-114">此示例使用 " `<see>` 备注" 部分中的标记 `UpdateRecord` 来引用 `DoesRecordExist` 方法。</span><span class="sxs-lookup"><span data-stu-id="bc5cc-114">This example uses the `<see>` tag in the `UpdateRecord` remarks section to refer to the `DoesRecordExist` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="bc5cc-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="bc5cc-115">See also</span></span>

- [<span data-ttu-id="bc5cc-116">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="bc5cc-116">XML Comment Tags</span></span>](index.md)

---
description: 了解详细信息： <seealso> (Visual Basic)
title: <seealso>
ms.date: 07/20/2015
helpviewer_keywords:
- <seealso> XML tag
- seealso XML tag
ms.assetid: 36050c95-1af2-4284-b9b6-1a70691ed978
ms.openlocfilehash: 0bf6fa69ad63db016b42e31f717f521f82bbe20e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640311"
---
# <a name="seealso-visual-basic"></a><span data-ttu-id="9d791-103">\<seealso> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9d791-103">\<seealso> (Visual Basic)</span></span>

<span data-ttu-id="9d791-104">指定显示在 "另请参见" 部分中的链接。</span><span class="sxs-lookup"><span data-stu-id="9d791-104">Specifies a link that appears in the See Also section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d791-105">语法</span><span class="sxs-lookup"><span data-stu-id="9d791-105">Syntax</span></span>  
  
```xml  
<seealso cref="member"/>  
```  
  
## <a name="parameters"></a><span data-ttu-id="9d791-106">参数</span><span class="sxs-lookup"><span data-stu-id="9d791-106">Parameters</span></span>  

 `member`  
 <span data-ttu-id="9d791-107">对可从当前编译环境调用的成员或字段的引用。</span><span class="sxs-lookup"><span data-stu-id="9d791-107">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="9d791-108">编译器检查是否存在给定的码位元素，并将 `member` 传递到输出 XML 中的元素名称。</span><span class="sxs-lookup"><span data-stu-id="9d791-108">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.</span></span> <span data-ttu-id="9d791-109">`member` 必须出现在双引号 (" ") 内。</span><span class="sxs-lookup"><span data-stu-id="9d791-109">`member` must appear within double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9d791-110">备注</span><span class="sxs-lookup"><span data-stu-id="9d791-110">Remarks</span></span>  

 <span data-ttu-id="9d791-111">使用 `<seealso>` 标记来指定要在 "另请参见" 部分中显示的文本。</span><span class="sxs-lookup"><span data-stu-id="9d791-111">Use the `<seealso>` tag to specify the text that you want to appear in a See Also section.</span></span> <span data-ttu-id="9d791-112">使用 [\<see>](see.md) 从文本内指定链接。</span><span class="sxs-lookup"><span data-stu-id="9d791-112">Use [\<see>](see.md) to specify a link from within text.</span></span>  
  
 <span data-ttu-id="9d791-113">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="9d791-113">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9d791-114">示例</span><span class="sxs-lookup"><span data-stu-id="9d791-114">Example</span></span>  

 <span data-ttu-id="9d791-115">此示例使用 " `<seealso>` 备注" 部分中的标记 `DoesRecordExist` 来引用 `UpdateRecord` 方法。</span><span class="sxs-lookup"><span data-stu-id="9d791-115">This example uses the `<seealso>` tag in the `DoesRecordExist` remarks section to refer to the `UpdateRecord` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="9d791-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d791-116">See also</span></span>

- [<span data-ttu-id="9d791-117">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="9d791-117">XML Comment Tags</span></span>](index.md)

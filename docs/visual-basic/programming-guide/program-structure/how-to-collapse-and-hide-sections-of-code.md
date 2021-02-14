---
description: '了解详细信息：如何：折叠和隐藏代码段 (Visual Basic) '
title: 如何：折叠和隐藏代码节
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic, code collapsing
- Visual Basic, code hiding
- Visual Basic code, collapsing and hiding
ms.assetid: b770e8f5-e07d-491a-ab4b-a977980f9ba2
ms.openlocfilehash: b93a2190bd6266c6f9fa5cb06eb249ca174c8067
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475963"
---
# <a name="how-to-collapse-and-hide-sections-of-code-visual-basic"></a><span data-ttu-id="ba323-103">如何：折叠和隐藏代码节 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ba323-103">How to: Collapse and Hide Sections of Code (Visual Basic)</span></span>

<span data-ttu-id="ba323-104">`#Region`指令使你可以折叠和隐藏 Visual Basic 文件中的代码段。</span><span class="sxs-lookup"><span data-stu-id="ba323-104">The `#Region` directive enables you to collapse and hide sections of code in Visual Basic files.</span></span> <span data-ttu-id="ba323-105">`#Region`使用指令，可以指定在使用 Visual Studio code 编辑器时可展开或折叠的代码块。</span><span class="sxs-lookup"><span data-stu-id="ba323-105">The `#Region` directive lets you specify a block of code that you can expand or collapse when using the Visual Studio code editor.</span></span> <span data-ttu-id="ba323-106">可以有选择地隐藏代码，使文件更易于管理且更易于阅读。</span><span class="sxs-lookup"><span data-stu-id="ba323-106">The ability to hide code selectively makes your files more manageable and easier to read.</span></span> <span data-ttu-id="ba323-107">有关详细信息，请参阅[大纲显示](/visualstudio/ide/outlining)。</span><span class="sxs-lookup"><span data-stu-id="ba323-107">For more information, see [Outlining](/visualstudio/ide/outlining).</span></span>

<span data-ttu-id="ba323-108">`#Region` 指令支持代码块语义，如 `#If...#End If` 。</span><span class="sxs-lookup"><span data-stu-id="ba323-108">`#Region` directives support code block semantics such as `#If...#End If`.</span></span> <span data-ttu-id="ba323-109">这意味着它们不能以一个块开始，并在另一个块中结束;开始和结束必须在同一个块中。</span><span class="sxs-lookup"><span data-stu-id="ba323-109">This means they cannot begin in one block and end in another; the start and end must be in the same block.</span></span> <span data-ttu-id="ba323-110">`#Region` 函数内不支持指令。</span><span class="sxs-lookup"><span data-stu-id="ba323-110">`#Region` directives are not supported within functions.</span></span>

## <a name="to-collapse-and-hide-a-section-of-code"></a><span data-ttu-id="ba323-111">折叠和隐藏代码段</span><span class="sxs-lookup"><span data-stu-id="ba323-111">To collapse and hide a section of code</span></span>

<span data-ttu-id="ba323-112">将代码段放置在 `#Region` 和语句之间 `#End Region` ，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="ba323-112">Place the section of code between the `#Region` and `#End Region` statements, as in the following example:</span></span>

[!code-vb[VbVbalrConditionalComp#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#6)]

<span data-ttu-id="ba323-113">`#Region`块可以在一个代码文件中多次使用; 因此，用户可以定义自己的过程和类块，进而可以进行折叠。</span><span class="sxs-lookup"><span data-stu-id="ba323-113">The `#Region` block can be used multiple times in a code file; thus, users can define their own blocks of procedures and classes that can, in turn, be collapsed.</span></span> <span data-ttu-id="ba323-114">`#Region` 块还可以嵌套在其他 `#Region` 块内。</span><span class="sxs-lookup"><span data-stu-id="ba323-114">`#Region` blocks can also be nested within other `#Region` blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="ba323-115">隐藏代码不会阻止编译代码，也不会影响 `#If...#End If` 语句。</span><span class="sxs-lookup"><span data-stu-id="ba323-115">Hiding code does not prevent it from being compiled and does not affect `#If...#End If` statements.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba323-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba323-116">See also</span></span>

- [<span data-ttu-id="ba323-117">条件编译</span><span class="sxs-lookup"><span data-stu-id="ba323-117">Conditional Compilation</span></span>](conditional-compilation.md)
- [<span data-ttu-id="ba323-118">#Region 指令</span><span class="sxs-lookup"><span data-stu-id="ba323-118">#Region Directive</span></span>](../../language-reference/directives/region-directive.md)
- [<span data-ttu-id="ba323-119">#If...Then...#Else 指令</span><span class="sxs-lookup"><span data-stu-id="ba323-119">#If...Then...#Else Directives</span></span>](../../language-reference/directives/if-then-else-directives.md)
- [<span data-ttu-id="ba323-120">大纲显示</span><span class="sxs-lookup"><span data-stu-id="ba323-120">Outlining</span></span>](/visualstudio/ide/outlining)

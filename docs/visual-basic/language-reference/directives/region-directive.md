---
description: '了解详细信息： #Region 指令'
title: '#Region 指令'
ms.date: 07/20/2015
f1_keywords:
- vb.Region
- vb.#Region
helpviewer_keywords:
- Visual Basic compiler, compiler directives
- '#region directive'
- region directive (#region)
- '#Region keyword [Visual Basic]'
ms.assetid: 90a6a104-3cbf-47d0-bdc4-b585d0921b87
ms.openlocfilehash: 4ba1645cfc51a69d39e6a60b5ea236dd65883e1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797219"
---
# <a name="region-directive"></a><span data-ttu-id="70136-103">#Region 指令</span><span class="sxs-lookup"><span data-stu-id="70136-103">#Region Directive</span></span>

<span data-ttu-id="70136-104">折叠并隐藏 Visual Basic 文件中的代码段。</span><span class="sxs-lookup"><span data-stu-id="70136-104">Collapses and hides sections of code in Visual Basic files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70136-105">语法</span><span class="sxs-lookup"><span data-stu-id="70136-105">Syntax</span></span>  

```vb
#Region "identifier_string"  
#End Region  
```  
  
## <a name="parts"></a><span data-ttu-id="70136-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="70136-106">Parts</span></span>  
  
|<span data-ttu-id="70136-107">术语</span><span class="sxs-lookup"><span data-stu-id="70136-107">Term</span></span>|<span data-ttu-id="70136-108">定义</span><span class="sxs-lookup"><span data-stu-id="70136-108">Definition</span></span>|  
|---|---|  
|`identifier_string`|<span data-ttu-id="70136-109">必需。</span><span class="sxs-lookup"><span data-stu-id="70136-109">Required.</span></span> <span data-ttu-id="70136-110">当区域处于折叠状态时充当区域标题的字符串。</span><span class="sxs-lookup"><span data-stu-id="70136-110">String that acts as the title of a region when it is collapsed.</span></span> <span data-ttu-id="70136-111">默认情况下，区域处于折叠状态。</span><span class="sxs-lookup"><span data-stu-id="70136-111">Regions are collapsed by default.</span></span>|  
|`#End Region`|<span data-ttu-id="70136-112">终止 `#Region` 块。</span><span class="sxs-lookup"><span data-stu-id="70136-112">Terminates the `#Region` block.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="70136-113">备注</span><span class="sxs-lookup"><span data-stu-id="70136-113">Remarks</span></span>  

 <span data-ttu-id="70136-114">使用 `#Region` 指令指定使用 Visual Studio Code 编辑器的大纲显示功能时要展开或折叠的代码块。</span><span class="sxs-lookup"><span data-stu-id="70136-114">Use the `#Region` directive to specify a block of code to expand or collapse when using the outlining feature of the Visual Studio Code Editor.</span></span> <span data-ttu-id="70136-115">您可以在其他区域中放置或 *嵌套* 区域，以将类似区域组合在一起。</span><span class="sxs-lookup"><span data-stu-id="70136-115">You can place, or *nest*, regions within other regions to group similar regions together.</span></span>  
  
## <a name="example"></a><span data-ttu-id="70136-116">示例</span><span class="sxs-lookup"><span data-stu-id="70136-116">Example</span></span>  

 <span data-ttu-id="70136-117">此示例使用 `#Region` 指令。</span><span class="sxs-lookup"><span data-stu-id="70136-117">This example uses the `#Region` directive.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="70136-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="70136-118">See also</span></span>

- [<span data-ttu-id="70136-119">#If...Then...#Else 指令</span><span class="sxs-lookup"><span data-stu-id="70136-119">#If...Then...#Else Directives</span></span>](if-then-else-directives.md)
- [<span data-ttu-id="70136-120">大纲显示</span><span class="sxs-lookup"><span data-stu-id="70136-120">Outlining</span></span>](/visualstudio/ide/outlining)
- [<span data-ttu-id="70136-121">如何：折叠和隐藏代码节</span><span class="sxs-lookup"><span data-stu-id="70136-121">How to: Collapse and Hide Sections of Code</span></span>](../../programming-guide/program-structure/how-to-collapse-and-hide-sections-of-code.md)

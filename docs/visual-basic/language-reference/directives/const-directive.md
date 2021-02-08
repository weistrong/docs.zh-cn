---
description: '了解详细信息： #Const 指令'
title: '#Const 指令'
ms.date: 07/20/2015
f1_keywords:
- vb.#Const
- '#vb.Const'
- '#Const'
helpviewer_keywords:
- '#Const directive'
- conditional compilation [Visual Basic], directives
- Const directive (#Const)
- Visual Basic compiler, compiler directives
- constants [Visual Basic], Const directive
- constants [Visual Basic], declaring
- Const statement [Visual Basic], directive (#Const)
- 'declaring constants [Visual Basic], #const directive'
ms.assetid: 707669e5-23f9-4f17-8622-a0d534429386
ms.openlocfilehash: 9597666ee1320f5dfda226040f93a84eb60a3deb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797271"
---
# <a name="const-directive"></a><span data-ttu-id="c25a7-103">#Const 指令</span><span class="sxs-lookup"><span data-stu-id="c25a7-103">#Const Directive</span></span>

<span data-ttu-id="c25a7-104">为 Visual Basic 定义条件编译器常量。</span><span class="sxs-lookup"><span data-stu-id="c25a7-104">Defines conditional compiler constants for Visual Basic.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c25a7-105">语法</span><span class="sxs-lookup"><span data-stu-id="c25a7-105">Syntax</span></span>  
  
```vb  
#Const constname = expression  
```  
  
## <a name="parts"></a><span data-ttu-id="c25a7-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="c25a7-106">Parts</span></span>  

 `constname`  
 <span data-ttu-id="c25a7-107">必需。</span><span class="sxs-lookup"><span data-stu-id="c25a7-107">Required.</span></span> <span data-ttu-id="c25a7-108">要定义的常数的名称。</span><span class="sxs-lookup"><span data-stu-id="c25a7-108">Name of the constant being defined.</span></span>  
  
 `expression`  
 <span data-ttu-id="c25a7-109">必需。</span><span class="sxs-lookup"><span data-stu-id="c25a7-109">Required.</span></span> <span data-ttu-id="c25a7-110">文本、其他条件编译器常量或包含除以外的任何或所有算术或逻辑运算符的任意组合 `Is` 。</span><span class="sxs-lookup"><span data-stu-id="c25a7-110">Literal, other conditional compiler constant, or any combination that includes any or all arithmetic or logical operators except `Is`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c25a7-111">备注</span><span class="sxs-lookup"><span data-stu-id="c25a7-111">Remarks</span></span>  

 <span data-ttu-id="c25a7-112">条件编译器常量总是专用于它们所在的文件。</span><span class="sxs-lookup"><span data-stu-id="c25a7-112">Conditional compiler constants are always private to the file in which they appear.</span></span> <span data-ttu-id="c25a7-113">不能使用指令创建公共编译器常量 `#Const` ; 只能在用户界面中或使用 `/define` 编译器选项创建它们。</span><span class="sxs-lookup"><span data-stu-id="c25a7-113">You cannot create public compiler constants using the `#Const` directive; you can create them only in the user interface or with the `/define` compiler option.</span></span>  
  
 <span data-ttu-id="c25a7-114">只能在中使用条件编译器常量和文本 `expression` 。</span><span class="sxs-lookup"><span data-stu-id="c25a7-114">You can use only conditional compiler constants and literals in `expression`.</span></span> <span data-ttu-id="c25a7-115">使用定义的标准常数 `Const` 会导致错误。</span><span class="sxs-lookup"><span data-stu-id="c25a7-115">Using a standard constant defined with `Const` causes an error.</span></span> <span data-ttu-id="c25a7-116">相反，您可以使用只使用关键字定义 `#Const` 的常量进行条件编译。</span><span class="sxs-lookup"><span data-stu-id="c25a7-116">Conversely, you can use constants defined with the `#Const` keyword only for conditional compilation.</span></span> <span data-ttu-id="c25a7-117">常数也可以是未定义的，在这种情况下，它们的值为 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="c25a7-117">Constants can also be undefined, in which case they have a value of `Nothing`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c25a7-118">示例</span><span class="sxs-lookup"><span data-stu-id="c25a7-118">Example</span></span>  

 <span data-ttu-id="c25a7-119">此示例使用 `#Const` 指令。</span><span class="sxs-lookup"><span data-stu-id="c25a7-119">This example uses the `#Const` directive.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="c25a7-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c25a7-120">See also</span></span>

- [<span data-ttu-id="c25a7-121">-define (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c25a7-121">-define (Visual Basic)</span></span>](../../reference/command-line-compiler/define.md)
- [<span data-ttu-id="c25a7-122">#If...Then...#Else 指令</span><span class="sxs-lookup"><span data-stu-id="c25a7-122">#If...Then...#Else Directives</span></span>](if-then-else-directives.md)
- [<span data-ttu-id="c25a7-123">Const 语句</span><span class="sxs-lookup"><span data-stu-id="c25a7-123">Const Statement</span></span>](../statements/const-statement.md)
- [<span data-ttu-id="c25a7-124">条件编译</span><span class="sxs-lookup"><span data-stu-id="c25a7-124">Conditional Compilation</span></span>](../../programming-guide/program-structure/conditional-compilation.md)
- [<span data-ttu-id="c25a7-125">If...Then...Else 语句</span><span class="sxs-lookup"><span data-stu-id="c25a7-125">If...Then...Else Statement</span></span>](../statements/if-then-else-statement.md)

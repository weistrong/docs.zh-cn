---
description: '了解详细信息： REM 语句 (Visual Basic) '
title: REM 语句
ms.date: 07/20/2015
f1_keywords:
- vb.'
- vb.Rem
- Rem
- "'"
helpviewer_keywords:
- REM statement [Visual Basic]
- comments, Visual Basic code
- code comments, Visual Basic
- Visual Basic code, comments
- "' comment marker character [Visual Basic]"
ms.assetid: 34126d7f-e0f9-476d-91e6-b31b398615dc
ms.openlocfilehash: c82621db98dc66060ae098ee6537ee58b24046a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741310"
---
# <a name="rem-statement-visual-basic"></a><span data-ttu-id="16b29-103">REM 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="16b29-103">REM Statement (Visual Basic)</span></span>

<span data-ttu-id="16b29-104">用于在程序的源代码中包括解释性注释。</span><span class="sxs-lookup"><span data-stu-id="16b29-104">Used to include explanatory remarks in the source code of a program.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16b29-105">语法</span><span class="sxs-lookup"><span data-stu-id="16b29-105">Syntax</span></span>  
  
```vb  
REM comment  
' comment  
```  
  
## <a name="parts"></a><span data-ttu-id="16b29-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="16b29-106">Parts</span></span>  

 `comment`  
 <span data-ttu-id="16b29-107">可选。</span><span class="sxs-lookup"><span data-stu-id="16b29-107">Optional.</span></span> <span data-ttu-id="16b29-108">要包括的任何注释的文本。</span><span class="sxs-lookup"><span data-stu-id="16b29-108">The text of any comment you want to include.</span></span> <span data-ttu-id="16b29-109">关键字和之间必须有一个空格 `REM` `comment` 。</span><span class="sxs-lookup"><span data-stu-id="16b29-109">A space is required between the `REM` keyword and `comment`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="16b29-110">备注</span><span class="sxs-lookup"><span data-stu-id="16b29-110">Remarks</span></span>  

 <span data-ttu-id="16b29-111">您可以将 `REM` 语句放在一行上，也可以将其放在另一语句后面的行上。</span><span class="sxs-lookup"><span data-stu-id="16b29-111">You can put a `REM` statement alone on a line, or you can put it on a line following another statement.</span></span> <span data-ttu-id="16b29-112">`REM`语句必须是行中的最后一条语句。</span><span class="sxs-lookup"><span data-stu-id="16b29-112">The `REM` statement must be the last statement on the line.</span></span> <span data-ttu-id="16b29-113">如果它跟在另一语句之后，则 `REM` 必须用空格将其与该语句分隔开。</span><span class="sxs-lookup"><span data-stu-id="16b29-113">If it follows another statement, the `REM` must be separated from that statement by a space.</span></span>  
  
 <span data-ttu-id="16b29-114">您可以 (`'`) 而不是使用单引号 `REM` 。</span><span class="sxs-lookup"><span data-stu-id="16b29-114">You can use a single quotation mark (`'`) instead of `REM`.</span></span> <span data-ttu-id="16b29-115">无论您的注释是在同一行后面还是单独的行上，都是如此。</span><span class="sxs-lookup"><span data-stu-id="16b29-115">This is true whether your comment follows another statement on the same line or sits alone on a line.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="16b29-116">不能 `REM` 使用行继续符序列 () 继续执行语句 `_` 。</span><span class="sxs-lookup"><span data-stu-id="16b29-116">You cannot continue a `REM` statement by using a line-continuation sequence (`_`).</span></span> <span data-ttu-id="16b29-117">注释开始后，编译器不会检查字符的特殊含义。</span><span class="sxs-lookup"><span data-stu-id="16b29-117">Once a comment begins, the compiler does not examine the characters for special meaning.</span></span> <span data-ttu-id="16b29-118">对于多行注释，请 `REM` 在每行上使用另一个语句或注释符号 (`'`) 。</span><span class="sxs-lookup"><span data-stu-id="16b29-118">For a multiple-line comment, use another `REM` statement or a comment symbol (`'`) on each line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="16b29-119">示例</span><span class="sxs-lookup"><span data-stu-id="16b29-119">Example</span></span>  

 <span data-ttu-id="16b29-120">下面的示例说明 `REM` 语句，该语句用于在程序中包含解释性注释。</span><span class="sxs-lookup"><span data-stu-id="16b29-120">The following example illustrates the `REM` statement, which is used to include explanatory remarks in a program.</span></span> <span data-ttu-id="16b29-121">它还显示了使用单引号字符 (`'`) 而不是的另一种方法 `REM` 。</span><span class="sxs-lookup"><span data-stu-id="16b29-121">It also shows the alternative of using the single quotation-mark character (`'`) instead of `REM`.</span></span>  
  
 [!code-vb[VbVbalrStatements#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="16b29-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="16b29-122">See also</span></span>

- [<span data-ttu-id="16b29-123">代码中的注释</span><span class="sxs-lookup"><span data-stu-id="16b29-123">Comments in Code</span></span>](../../programming-guide/program-structure/comments-in-code.md)
- [<span data-ttu-id="16b29-124">如何：在代码中拆分和合并语句</span><span class="sxs-lookup"><span data-stu-id="16b29-124">How to: Break and Combine Statements in Code</span></span>](../../programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)

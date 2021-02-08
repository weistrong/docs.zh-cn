---
description: 了解详细信息： BC30205：应为语句结尾
title: 需要语句结束
ms.date: 07/20/2015
f1_keywords:
- bc30205
- vbc30205
helpviewer_keywords:
- BC30205
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
ms.openlocfilehash: a3f309a4674f6de34c0be8abfef31e293a10dec5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796543"
---
# <a name="bc30205-end-of-statement-expected"></a><span data-ttu-id="be883-103">BC30205：应为语句结尾</span><span class="sxs-lookup"><span data-stu-id="be883-103">BC30205: End of statement expected</span></span>

<span data-ttu-id="be883-104">语句在语法上完成，但在完成该语句的元素后附加了一个编程元素。</span><span class="sxs-lookup"><span data-stu-id="be883-104">The statement is syntactically complete, but an additional programming element follows the element that completes the statement.</span></span> <span data-ttu-id="be883-105">每个语句的末尾都需要行结束符。</span><span class="sxs-lookup"><span data-stu-id="be883-105">A line terminator is required at the end of every statement.</span></span>

 <span data-ttu-id="be883-106">行结束符将 Visual Basic 源文件中的字符分为多行。</span><span class="sxs-lookup"><span data-stu-id="be883-106">A line terminator divides the characters of a Visual Basic source file into lines.</span></span> <span data-ttu-id="be883-107">行结束符的示例包括 Unicode 回车符 ( # B0 HD) ，Unicode 换行符 ( # B1 HA) ，Unicode 回车符后跟 Unicode 换行符。</span><span class="sxs-lookup"><span data-stu-id="be883-107">Examples of line terminators are the Unicode carriage return character (&HD), the Unicode linefeed character (&HA), and the Unicode carriage return character followed by the Unicode linefeed character.</span></span> <span data-ttu-id="be883-108">有关行终止符的详细信息，请参阅 [Visual Basic 语言规范](~/_vblang/spec/lexical-grammar.md#line-terminators)。</span><span class="sxs-lookup"><span data-stu-id="be883-108">For more information about line terminators, see the [Visual Basic Language Specification](~/_vblang/spec/lexical-grammar.md#line-terminators).</span></span>

 <span data-ttu-id="be883-109">**错误 ID：** BC30205</span><span class="sxs-lookup"><span data-stu-id="be883-109">**Error ID:** BC30205</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="be883-110">更正此错误</span><span class="sxs-lookup"><span data-stu-id="be883-110">To correct this error</span></span>

1. <span data-ttu-id="be883-111">检查两个不同的语句是否被无意中放在同一行上。</span><span class="sxs-lookup"><span data-stu-id="be883-111">Check to see if two different statements have inadvertently been put on the same line.</span></span>

2. <span data-ttu-id="be883-112">在完成该语句的元素之后插入一个行结束符。</span><span class="sxs-lookup"><span data-stu-id="be883-112">Insert a line terminator after the element that completes the statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="be883-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="be883-113">See also</span></span>

- [<span data-ttu-id="be883-114">如何：在代码中拆分和合并语句</span><span class="sxs-lookup"><span data-stu-id="be883-114">How to: Break and Combine Statements in Code</span></span>](../../programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
- [<span data-ttu-id="be883-115">语句</span><span class="sxs-lookup"><span data-stu-id="be883-115">Statements</span></span>](../../programming-guide/language-features/statements.md)

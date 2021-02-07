---
description: '了解详细信息： Throw 语句 (Visual Basic) '
title: Throw 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Throw
helpviewer_keywords:
- structured exception handling, throw statements
- try-catch exception handling, throw statements
- throw statement [Visual Basic], about throw statements
- throwing exceptions, throw statement
- exception handling, throw statement
- On Error statement [Visual Basic], throwing exceptions
- throwing exceptions
- exception handling, unstructured
- throw statement [Visual Basic]
ms.assetid: a6e07406-5c8a-4498-87a2-8339f3651d62
ms.openlocfilehash: b7fa4183b5997e5dac8045502a8eed1afe66fc0d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740933"
---
# <a name="throw-statement-visual-basic"></a><span data-ttu-id="f471d-103">Throw 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f471d-103">Throw Statement (Visual Basic)</span></span>

<span data-ttu-id="f471d-104">在过程中引发异常。</span><span class="sxs-lookup"><span data-stu-id="f471d-104">Throws an exception within a procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f471d-105">语法</span><span class="sxs-lookup"><span data-stu-id="f471d-105">Syntax</span></span>

```vb
Throw [ expression ]
```

## <a name="part"></a><span data-ttu-id="f471d-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="f471d-106">Part</span></span>

`expression`\
<span data-ttu-id="f471d-107">提供有关要引发的异常的信息。</span><span class="sxs-lookup"><span data-stu-id="f471d-107">Provides information about the exception to be thrown.</span></span> <span data-ttu-id="f471d-108">如果位于 `Catch` 语句中，则为可选; 否则为必需。</span><span class="sxs-lookup"><span data-stu-id="f471d-108">Optional when residing in a `Catch` statement, otherwise required.</span></span>

## <a name="remarks"></a><span data-ttu-id="f471d-109">备注</span><span class="sxs-lookup"><span data-stu-id="f471d-109">Remarks</span></span>

<span data-ttu-id="f471d-110">`Throw`语句引发异常，你可以使用结构化异常处理代码处理 (`Try` ... `Catch`...`Finally` () 的) 或非结构化异常处理代码 `On Error GoTo` 。</span><span class="sxs-lookup"><span data-stu-id="f471d-110">The `Throw` statement throws an exception that you can handle with structured exception-handling code (`Try`...`Catch`...`Finally`) or unstructured exception-handling code (`On Error GoTo`).</span></span> <span data-ttu-id="f471d-111">您可以使用 `Throw` 语句来捕获代码中的错误，因为 Visual Basic 在调用堆栈中向上移动，直到找到相应的异常处理代码。</span><span class="sxs-lookup"><span data-stu-id="f471d-111">You can use the `Throw` statement to trap errors within your code because Visual Basic moves up the call stack until it finds the appropriate exception-handling code.</span></span>

<span data-ttu-id="f471d-112">`Throw`不带 expression 的语句只能用在 `Catch` 语句中，在这种情况下，该语句重新引发语句当前正在处理的异常 `Catch` 。</span><span class="sxs-lookup"><span data-stu-id="f471d-112">A `Throw` statement with no expression can only be used in a `Catch` statement, in which case the statement rethrows the exception currently being handled by the `Catch` statement.</span></span>

<span data-ttu-id="f471d-113">`Throw`语句重置异常的调用堆栈 `expression` 。</span><span class="sxs-lookup"><span data-stu-id="f471d-113">The `Throw` statement resets the call stack for the `expression` exception.</span></span> <span data-ttu-id="f471d-114">如果 `expression` 未提供，则调用堆栈保持不变。</span><span class="sxs-lookup"><span data-stu-id="f471d-114">If `expression` is not provided, the call stack is left unchanged.</span></span> <span data-ttu-id="f471d-115">您可以通过属性访问异常的调用堆栈 <xref:System.Exception.StackTrace%2A> 。</span><span class="sxs-lookup"><span data-stu-id="f471d-115">You can access the call stack for the exception through the <xref:System.Exception.StackTrace%2A> property.</span></span>

## <a name="example"></a><span data-ttu-id="f471d-116">示例</span><span class="sxs-lookup"><span data-stu-id="f471d-116">Example</span></span>

<span data-ttu-id="f471d-117">下面的代码使用 `Throw` 语句引发异常：</span><span class="sxs-lookup"><span data-stu-id="f471d-117">The following code uses the `Throw` statement to throw an exception:</span></span>

[!code-vb[VbVbalrStatements#84](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#84)]

## <a name="see-also"></a><span data-ttu-id="f471d-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f471d-118">See also</span></span>

- [<span data-ttu-id="f471d-119">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="f471d-119">Try...Catch...Finally Statement</span></span>](try-catch-finally-statement.md)
- [<span data-ttu-id="f471d-120">On Error 语句</span><span class="sxs-lookup"><span data-stu-id="f471d-120">On Error Statement</span></span>](on-error-statement.md)

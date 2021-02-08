---
description: 了解更多相关信息： BC32025： "#Region" 和 "#End Region" 语句在方法体/多行 lambda 内无效
title: “#Region”和“#End Region”语句在方法体/多行 lambda 内无效
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 0746b9caf677699d6fbbf0c5a7063b1b33d86f3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792019"
---
# <a name="bc32025-region-and-end-region-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a><span data-ttu-id="2c1d4-103">BC32025： "#Region" 和 "#End Region" 语句在方法体/多行 lambda 内无效</span><span class="sxs-lookup"><span data-stu-id="2c1d4-103">BC32025: '#Region' and '#End Region' statements are not valid within method bodies/multiline lambdas</span></span>

<span data-ttu-id="2c1d4-104">`#Region`必须在类、模块或命名空间级别声明块。</span><span class="sxs-lookup"><span data-stu-id="2c1d4-104">The `#Region` block must be declared at a class, module, or namespace level.</span></span> <span data-ttu-id="2c1d4-105">可折叠区域可以包含一个或多个过程，但不能在过程中开始或结束。</span><span class="sxs-lookup"><span data-stu-id="2c1d4-105">A collapsible region can include one or more procedures, but it cannot begin or end inside of a procedure.</span></span>

 <span data-ttu-id="2c1d4-106">**错误 ID：** BC32025</span><span class="sxs-lookup"><span data-stu-id="2c1d4-106">**Error ID:** BC32025</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="2c1d4-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2c1d4-107">To correct this error</span></span>

1. <span data-ttu-id="2c1d4-108">确保使用或语句正确终止前面的过程 `End Function` `End Sub` 。</span><span class="sxs-lookup"><span data-stu-id="2c1d4-108">Ensure that the preceding procedure is properly terminated with an `End Function` or `End Sub` statement.</span></span>

2. <span data-ttu-id="2c1d4-109">确保 `#Region` 和 `#End Region` 指令位于同一个代码块中。</span><span class="sxs-lookup"><span data-stu-id="2c1d4-109">Ensure that the `#Region` and `#End Region` directives are in the same code block.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c1d4-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="2c1d4-110">See also</span></span>

- [<span data-ttu-id="2c1d4-111">#Region 指令</span><span class="sxs-lookup"><span data-stu-id="2c1d4-111">#Region Directive</span></span>](../directives/region-directive.md)

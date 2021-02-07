---
description: 了解详细信息： BC32005：语句不能在行 "If" 语句外结束块
title: 语句不能在“If”语句行之外结束块
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: afe856b2c2ea3fa1db029d35c5b876f5d67da411
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731107"
---
# <a name="bc32005-statement-cannot-end-a-block-outside-of-a-line-if-statement"></a><span data-ttu-id="8e98c-103">BC32005：语句不能在行 "If" 语句外结束块</span><span class="sxs-lookup"><span data-stu-id="8e98c-103">BC32005: Statement cannot end a block outside of a line 'If' statement</span></span>

<span data-ttu-id="8e98c-104">单行 `If` 语句包含用冒号分隔的多个语句 (： ) ，其中一个语句 `End` 用于单个行外的控制块 `If` 。</span><span class="sxs-lookup"><span data-stu-id="8e98c-104">A single-line `If` statement contains several statements separated by colons (:), one of which is an `End` statement for a control block outside the single-line `If`.</span></span> <span data-ttu-id="8e98c-105">单行 `If` 语句不使用 `End If` 语句。</span><span class="sxs-lookup"><span data-stu-id="8e98c-105">Single-line `If` statements do not use the `End If` statement.</span></span>

 <span data-ttu-id="8e98c-106">**错误 ID：** BC32005</span><span class="sxs-lookup"><span data-stu-id="8e98c-106">**Error ID:** BC32005</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="8e98c-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="8e98c-107">To correct this error</span></span>

- <span data-ttu-id="8e98c-108">在 `If` 包含语句的控制块外移动单行语句 `End If` 。</span><span class="sxs-lookup"><span data-stu-id="8e98c-108">Move the single-line `If` statement outside the control block that contains the `End If` statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e98c-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="8e98c-109">See also</span></span>

- [<span data-ttu-id="8e98c-110">If...Then...Else 语句</span><span class="sxs-lookup"><span data-stu-id="8e98c-110">If...Then...Else Statement</span></span>](../statements/if-then-else-statement.md)

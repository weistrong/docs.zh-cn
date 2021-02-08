---
description: 了解详细信息： BC30481： "Class" 语句必须以匹配的 "End" 类结束
title: “Class”语句必须以匹配的“End Class”结束
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: b0d2d89e9e3549b24f9c923e271b15b3b02026b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796776"
---
# <a name="bc30481-class-statement-must-end-with-a-matching-end-class"></a><span data-ttu-id="d7c4d-103">BC30481： "Class" 语句必须以匹配的 "End Class" 结束</span><span class="sxs-lookup"><span data-stu-id="d7c4d-103">BC30481: 'Class' statement must end with a matching 'End Class'</span></span>

<span data-ttu-id="d7c4d-104">`Class` 用于启动 `Class` 块; 因此它只能出现在块的开头，并以匹配的 `End Class` 语句结束块。</span><span class="sxs-lookup"><span data-stu-id="d7c4d-104">`Class` is used to initiate a `Class` block; hence it can only appear at the beginning of the block, with a matching `End Class` statement ending the block.</span></span> <span data-ttu-id="d7c4d-105">您有冗余的 `Class` 语句，或者您没有 `Class` 用结束块 `End Class` 。</span><span class="sxs-lookup"><span data-stu-id="d7c4d-105">Either you have a redundant `Class` statement, or you have not ended your `Class` block with `End Class`.</span></span>

 <span data-ttu-id="d7c4d-106">**错误 ID：** BC30481</span><span class="sxs-lookup"><span data-stu-id="d7c4d-106">**Error ID:** BC30481</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="d7c4d-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="d7c4d-107">To correct this error</span></span>

- <span data-ttu-id="d7c4d-108">找到并删除不必要的 `Class` 语句。</span><span class="sxs-lookup"><span data-stu-id="d7c4d-108">Locate and remove the unnecessary `Class` statement.</span></span>

- <span data-ttu-id="d7c4d-109">`Class`使用匹配的结束块 `End Class` 。</span><span class="sxs-lookup"><span data-stu-id="d7c4d-109">Conclude the `Class` block with a matching `End Class`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7c4d-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7c4d-110">See also</span></span>

- [<span data-ttu-id="d7c4d-111">End \<keyword> 语句</span><span class="sxs-lookup"><span data-stu-id="d7c4d-111">End \<keyword> Statement</span></span>](../statements/end-keyword-statement.md)
- [<span data-ttu-id="d7c4d-112">Class 语句</span><span class="sxs-lookup"><span data-stu-id="d7c4d-112">Class Statement</span></span>](../statements/class-statement.md)

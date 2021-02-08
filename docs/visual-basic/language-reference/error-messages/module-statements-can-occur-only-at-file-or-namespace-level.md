---
description: 了解详细信息： BC30617： "Module" 语句只能出现在文件级或命名空间级
title: “Module”语句只能出现在文件级或命名空间级
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: f5c3ea0cd1c08fb0243043ae50e707e2c59b00f2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795776"
---
# <a name="bc30617-module-statements-can-occur-only-at-file-or-namespace-level"></a><span data-ttu-id="4caf1-103">BC30617： "Module" 语句只能出现在文件级或命名空间级</span><span class="sxs-lookup"><span data-stu-id="4caf1-103">BC30617: 'Module' statements can occur only at file or namespace level</span></span>

<span data-ttu-id="4caf1-104">`Module` 语句必须紧跟在 `Option` 和 `Imports` 语句、全局特性和命名空间声明之后、但在其他所有声明之前。</span><span class="sxs-lookup"><span data-stu-id="4caf1-104">`Module` statements must appear at the top of your source file immediately after `Option` and `Imports` statements, global attributes, and namespace declarations, but before all other declarations.</span></span>

 <span data-ttu-id="4caf1-105">**错误 ID：** BC30617</span><span class="sxs-lookup"><span data-stu-id="4caf1-105">**Error ID:** BC30617</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4caf1-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4caf1-106">To correct this error</span></span>

- <span data-ttu-id="4caf1-107">将 `Module` 语句移动到命名空间声明或源文件的顶部。</span><span class="sxs-lookup"><span data-stu-id="4caf1-107">Move the `Module` statement to the top of your namespace declaration or source file.</span></span>

## <a name="see-also"></a><span data-ttu-id="4caf1-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="4caf1-108">See also</span></span>

- [<span data-ttu-id="4caf1-109">Module 语句</span><span class="sxs-lookup"><span data-stu-id="4caf1-109">Module Statement</span></span>](../statements/module-statement.md)

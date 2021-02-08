---
description: 了解详细信息： BC30594：共享 WithEvents 变量的事件不能由非共享方法处理
title: 共享 WithEvents 变量的事件不能由非共享方法处理
ms.date: 07/20/2015
f1_keywords:
- bc30594
- vbc30594
helpviewer_keywords:
- BC30594
ms.assetid: 5b9fceb4-ab11-41bb-ad3b-6f1a9da8ae7e
ms.openlocfilehash: f9e8bf6e0d365c4ee747deb6be0e809904d87117
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796413"
---
# <a name="bc30594-events-of-shared-withevents-variables-cannot-be-handled-by-non-shared-methods"></a><span data-ttu-id="22a54-103">BC30594：共享 WithEvents 变量的事件不能由非共享方法处理</span><span class="sxs-lookup"><span data-stu-id="22a54-103">BC30594: Events of shared WithEvents variables cannot be handled by non-shared methods</span></span>

<span data-ttu-id="22a54-104">使用修饰符声明的变量 `Shared` 是共享变量。</span><span class="sxs-lookup"><span data-stu-id="22a54-104">A variable declared with the `Shared` modifier is a shared variable.</span></span> <span data-ttu-id="22a54-105">共享变量精确标识一个存储位置。</span><span class="sxs-lookup"><span data-stu-id="22a54-105">A shared variable identifies exactly one storage location.</span></span> <span data-ttu-id="22a54-106">使用修饰符声明的变量 `WithEvents` 断言变量所属的类型将处理变量引发的事件集。</span><span class="sxs-lookup"><span data-stu-id="22a54-106">A variable declared with the `WithEvents` modifier asserts that the type to which the variable belongs handles the set of events the variable raises.</span></span> <span data-ttu-id="22a54-107">将值分配给变量时，由声明创建的属性将 `WithEvents` 卸载任何现有的事件处理程序，并通过方法挂钩新的事件处理程序 `Add` 。</span><span class="sxs-lookup"><span data-stu-id="22a54-107">When a value is assigned to the variable, the property created by the `WithEvents` declaration unhooks any existing event handler and hooks up the new event handler via the `Add` method.</span></span>

 <span data-ttu-id="22a54-108">**错误 ID：** BC30594</span><span class="sxs-lookup"><span data-stu-id="22a54-108">**Error ID:** BC30594</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="22a54-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="22a54-109">To correct this error</span></span>

- <span data-ttu-id="22a54-110">声明事件处理程序 `Shared` 。</span><span class="sxs-lookup"><span data-stu-id="22a54-110">Declare your event handler `Shared`.</span></span>

## <a name="see-also"></a><span data-ttu-id="22a54-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="22a54-111">See also</span></span>

- [<span data-ttu-id="22a54-112">共享</span><span class="sxs-lookup"><span data-stu-id="22a54-112">Shared</span></span>](../modifiers/shared.md)
- [<span data-ttu-id="22a54-113">WithEvents</span><span class="sxs-lookup"><span data-stu-id="22a54-113">WithEvents</span></span>](../modifiers/withevents.md)

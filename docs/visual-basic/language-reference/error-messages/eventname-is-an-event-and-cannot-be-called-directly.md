---
description: 了解更多相关信息： BC32022： " <eventname> " 是事件，不能直接调用
title: “<eventname>”是事件，不能直接调用
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: f9d4b8fe54e1101e7963933f871cf5af2c1af903
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796439"
---
# <a name="bc32022-eventname-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="b5272-103">BC32022： " \<eventname> " 是事件，不能直接调用</span><span class="sxs-lookup"><span data-stu-id="b5272-103">BC32022: '\<eventname>' is an event, and cannot be called directly</span></span>

<span data-ttu-id="b5272-104">"<`eventname`>" 是一个事件，因此不能直接调用。</span><span class="sxs-lookup"><span data-stu-id="b5272-104">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="b5272-105">使用 `RaiseEvent` 语句引发事件。</span><span class="sxs-lookup"><span data-stu-id="b5272-105">Use a `RaiseEvent` statement to raise an event.</span></span>

 <span data-ttu-id="b5272-106">过程调用指定过程名称的事件。</span><span class="sxs-lookup"><span data-stu-id="b5272-106">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="b5272-107">事件处理程序是一个过程，但事件本身就是信号设备，必须引发并处理。</span><span class="sxs-lookup"><span data-stu-id="b5272-107">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>

 <span data-ttu-id="b5272-108">**错误 ID：** BC32022</span><span class="sxs-lookup"><span data-stu-id="b5272-108">**Error ID:** BC32022</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="b5272-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="b5272-109">To correct this error</span></span>

- <span data-ttu-id="b5272-110">使用 `RaiseEvent` 语句对事件发出信号并调用处理该事件的过程。</span><span class="sxs-lookup"><span data-stu-id="b5272-110">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5272-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5272-111">See also</span></span>

- [<span data-ttu-id="b5272-112">RaiseEvent 语句</span><span class="sxs-lookup"><span data-stu-id="b5272-112">RaiseEvent Statement</span></span>](../statements/raiseevent-statement.md)

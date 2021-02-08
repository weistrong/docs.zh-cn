---
description: 了解详细信息： BC30029：派生类无法引发基类事件
title: 派生类无法引发基类事件
ms.date: 07/20/2015
f1_keywords:
- vbc30029
- bc30029
helpviewer_keywords:
- BC30029
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
ms.openlocfilehash: 68546f2654f7c34fcb309d5af68e237d5f1eac79
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796595"
---
# <a name="bc30029-derived-classes-cannot-raise-base-class-events"></a><span data-ttu-id="24d66-103">BC30029：派生类无法引发基类事件</span><span class="sxs-lookup"><span data-stu-id="24d66-103">BC30029: Derived classes cannot raise base class events</span></span>

<span data-ttu-id="24d66-104">事件只能从声明它的声明空间引发。</span><span class="sxs-lookup"><span data-stu-id="24d66-104">An event can be raised only from the declaration space in which it is declared.</span></span> <span data-ttu-id="24d66-105">因此，类无法从任何其他类（甚至是从中派生的类）引发事件。</span><span class="sxs-lookup"><span data-stu-id="24d66-105">Therefore, a class cannot raise events from any other class, even one from which it is derived.</span></span>

 <span data-ttu-id="24d66-106">**错误 ID：** BC30029</span><span class="sxs-lookup"><span data-stu-id="24d66-106">**Error ID:** BC30029</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="24d66-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="24d66-107">To correct this error</span></span>

- <span data-ttu-id="24d66-108">移动 `Event` 语句或 `RaiseEvent` 语句，使其位于同一个类中。</span><span class="sxs-lookup"><span data-stu-id="24d66-108">Move the `Event` statement or the `RaiseEvent` statement so they are in the same class.</span></span>

## <a name="see-also"></a><span data-ttu-id="24d66-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="24d66-109">See also</span></span>

- [<span data-ttu-id="24d66-110">Event 语句</span><span class="sxs-lookup"><span data-stu-id="24d66-110">Event Statement</span></span>](../statements/event-statement.md)
- [<span data-ttu-id="24d66-111">RaiseEvent 语句</span><span class="sxs-lookup"><span data-stu-id="24d66-111">RaiseEvent Statement</span></span>](../statements/raiseevent-statement.md)

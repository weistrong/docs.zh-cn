---
description: 了解详细信息： BC31423：事件 " <eventname1> " 无法实现 <eventname2> 接口 "" 上的事件 "" <interface> ，因为它们的委托类型 " <delegate1> " 和 " <delegate2> " 不匹配
title: 事件“<eventname1>”无法实现接口“<eventname2>”上的事件“<interface>”，因为它们的委托类型“<delegate1>”和“<delegate2>”不匹配
ms.date: 07/20/2015
f1_keywords:
- vbc31423
- bc31423
helpviewer_keywords:
- BC31423
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
ms.openlocfilehash: cfb967d2b43ce1f34f56f3d019a9a663b000296c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796452"
---
# <a name="bc31423-event-eventname1-cannot-implement-event-eventname2-on-interface-interface-because-their-delegate-types-delegate1-and-delegate2-do-not-match"></a>BC31423：事件 "" \<eventname1> 无法实现 \<eventname2> 接口 "" 上的事件 "" \<interface> ，因为它们的委托类型 " \<delegate1> " 和 " \<delegate2> " 不匹配

Visual Basic 无法实现事件，因为该事件的委托类型与接口中事件的委托类型不匹配。 如果在接口中定义了多个事件，然后试图用一个事件同时实现这些事件，则可能发生此错误。 只有当所有要实现的事件都使用 `As` 语法进行声明并指定相同的委托类型时，事件才能实现两个或更多个事件。

 **错误 ID：** BC31423

## <a name="to-correct-this-error"></a>更正此错误

- 单独实现事件。

     \- 或 -

- 使用语法定义接口中的事件 `As` ，并指定相同的委托类型。

## <a name="see-also"></a>请参阅

- [Event 语句](../statements/event-statement.md)
- [Delegate 语句](../statements/delegate-statement.md)
- [事件](../../programming-guide/language-features/events/index.md)

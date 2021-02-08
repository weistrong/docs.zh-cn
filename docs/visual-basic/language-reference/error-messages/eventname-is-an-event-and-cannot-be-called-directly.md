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
# <a name="bc32022-eventname-is-an-event-and-cannot-be-called-directly"></a>BC32022： " \<eventname> " 是事件，不能直接调用

"<`eventname`>" 是一个事件，因此不能直接调用。 使用 `RaiseEvent` 语句引发事件。

 过程调用指定过程名称的事件。 事件处理程序是一个过程，但事件本身就是信号设备，必须引发并处理。

 **错误 ID：** BC32022

## <a name="to-correct-this-error"></a>更正此错误

- 使用 `RaiseEvent` 语句对事件发出信号并调用处理该事件的过程。

## <a name="see-also"></a>请参阅

- [RaiseEvent 语句](../statements/raiseevent-statement.md)

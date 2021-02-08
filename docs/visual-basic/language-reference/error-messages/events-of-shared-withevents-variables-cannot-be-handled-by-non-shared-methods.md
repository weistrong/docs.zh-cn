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
# <a name="bc30594-events-of-shared-withevents-variables-cannot-be-handled-by-non-shared-methods"></a>BC30594：共享 WithEvents 变量的事件不能由非共享方法处理

使用修饰符声明的变量 `Shared` 是共享变量。 共享变量精确标识一个存储位置。 使用修饰符声明的变量 `WithEvents` 断言变量所属的类型将处理变量引发的事件集。 将值分配给变量时，由声明创建的属性将 `WithEvents` 卸载任何现有的事件处理程序，并通过方法挂钩新的事件处理程序 `Add` 。

 **错误 ID：** BC30594

## <a name="to-correct-this-error"></a>更正此错误

- 声明事件处理程序 `Shared` 。

## <a name="see-also"></a>请参阅

- [共享](../modifiers/shared.md)
- [WithEvents](../modifiers/withevents.md)

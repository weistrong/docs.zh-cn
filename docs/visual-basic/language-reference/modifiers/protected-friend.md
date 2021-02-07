---
description: '了解有关以下内容的详细信息：受保护的 Friend (Visual Basic) '
title: Protected Friend
ms.date: 05/10/2018
f1_keywords:
- vb.ProtectedFriend
helpviewer_keywords:
- Protected Friend keyword [Visual Basic]
- Protected Friend keyword [Visual Basic], syntax
ms.openlocfilehash: dcc8fd2b1aa99f910f002ac05178d379532fb73d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700970"
---
# <a name="protected-friend-visual-basic"></a>受保护的 Friend (Visual Basic) 

`Protected Friend` 关键字组合是一种成员访问修饰符。 它在已声明的元素上授予 [朋友](friend.md) 访问和 [受保护](protected.md) 的访问，因此可以从同一程序集中的任何位置、从其自己的类和派生类中访问它们。 只能 `Protected Friend` 在类的成员上指定; 无法应用 `Protected Friend` 于结构的成员，因为结构不能继承。

> [!NOTE]
> 在 Visual Studio 中，选择 "F1 帮助" `protected friend` 可为 [受保护](protected.md) 的或 [朋友](friend.md)提供帮助。 IDE 将选取光标下的单个标记，而不是组合词。

## <a name="rules"></a>规则

**声明上下文。** `Protected Friend`只能在类级别使用。 这意味着元素的声明上下文 `Protected` 必须是类，且不能是源文件、命名空间、接口、模块、结构或过程。

## <a name="see-also"></a>请参阅

- [公共](public.md)
- [Protected](protected.md)
- [Friend](friend.md)
- [专用](private.md)
- [Private Protected](./private-protected.md)
- [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)
- [过程](../../programming-guide/language-features/procedures/index.md)
- [结构](../../programming-guide/language-features/data-types/structures.md)
- [对象和类](../../programming-guide/language-features/objects-and-classes/index.md)

---
description: 了解更多相关信息： BC30020： "Is" 需要具有引用类型的操作数，但此操作数具有值类型 "<typename>
title: “Is”要求具有引用类型的操作数，但此操作数的值类型为“<typename>”。
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: f12d4bb4787c3d003c9afc6a0367f7f9e9248f15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795997"
---
# <a name="bc30020-is-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-typename"></a>BC30020： "Is" 需要具有引用类型的操作数，但此操作数的值类型为 " \<typename> "

`Is`比较运算符确定两个对象变量是否引用相同的实例。 没有为值类型定义此比较。

 **错误 ID：** BC30020

## <a name="to-correct-this-error"></a>更正此错误

- 使用适当的算术比较运算符或 `Like` 运算符比较两个值类型。

## <a name="see-also"></a>请参阅

- [Is 运算符](../operators/is-operator.md)
- [Like 运算符](../operators/like-operator.md)
- [比较运算符](../operators/comparison-operators.md)

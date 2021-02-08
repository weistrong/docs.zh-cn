---
description: 了解详细信息： BC30188：需要声明
title: 需要声明
ms.date: 07/20/2015
f1_keywords:
- vbc30188
- bc30188
helpviewer_keywords:
- BC30188
ms.assetid: da6b1df3-fe6b-4415-88e6-0977e5189e0b
ms.openlocfilehash: b86c182fb9dc8ab7d624833136f0e87b072aed92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796660"
---
# <a name="bc30188-declaration-expected"></a>BC30188：应为声明

Nondeclarative 语句，如赋值语句或循环语句，在任何过程外发生。 仅允许在过程外使用声明。

 或者，在没有声明关键字（如或）的情况下声明编程元素 `Dim` `Const` 。

 **错误 ID：** BC30188

## <a name="to-correct-this-error"></a>更正此错误

- 将 nondeclarative 语句移到过程的主体。

- 使用适当的声明关键字开始声明。

- 确保声明关键字没有拼写错误。

## <a name="see-also"></a>请参阅

- [过程](../../programming-guide/language-features/procedures/index.md)
- [Dim 语句](../statements/dim-statement.md)

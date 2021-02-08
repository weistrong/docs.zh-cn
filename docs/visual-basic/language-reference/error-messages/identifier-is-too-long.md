---
description: 了解详细信息： BC30033：标识符太长
title: 标识符太长
ms.date: 07/20/2015
f1_keywords:
- bc30033
- vbc30033
helpviewer_keywords:
- BC30033
ms.assetid: 3d07f6d0-9a2f-49ca-94e8-1e354932e855
ms.openlocfilehash: f2439c4bfc53f906fdc277b0de1faac0941c8808
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796088"
---
# <a name="bc30033-identifier-is-too-long"></a>BC30033：标识符太长

每个编程元素的名称或标识符限制为1023个字符。 此外，完全限定的名称不能超过1023个字符。 这意味着 () 的整个标识符字符串的 `<namespace>.<...>.<namespace>.<class>.<element>` 长度不能超过1023个字符，包括成员访问运算符 (`.`) 字符。

 **错误 ID：** BC30033

## <a name="to-correct-this-error"></a>更正此错误

- 减小标识符的长度。

## <a name="see-also"></a>请参阅

- [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)

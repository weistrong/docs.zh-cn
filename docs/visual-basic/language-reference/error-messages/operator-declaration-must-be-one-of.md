---
description: 了解详细信息： BC33000：运算符声明必须是以下之一： +,-, *、、/、^、 &amp; 、Like、Mod、And、Or、Xor、Not、 <<、 >> .。。
title: 运算符声明必须是以下其中之一： +,-, *,-,-, ^、 &amp; 、Like、Mod、And、Or、Xor、Not、 <<、 >>、=、 <>、<、<=、>、>=、CType、IsTrue、IsFalse
ms.date: 07/20/2015
f1_keywords:
- bc33000
- vbc33000
helpviewer_keywords:
- BC33000
ms.assetid: 15c5d8eb-3a8c-4141-8f41-33151afabf97
ms.openlocfilehash: 0ad82a6414387278622a10624952ebc35e7e9b83
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795555"
---
# <a name="bc33000-operator-declaration-must-be-one-of----amp-like-mod-and-or-xor-not--"></a>BC33000：运算符声明必须是以下之一： +,-, *、 \, /、^、 &amp; 、Like、Mod、And、Or、Xor、Not、 \<\<, >> .。。

您只能声明一个适合重载的运算符。 下表列出了可以声明的运算符。

|类型|运算符|
|----------|---------------|
|一元|`+`, `-`, `IsFalse`, `IsTrue`, `Not`|
|二进制|`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`|
|转换（一元）|`CType`|

 请注意， `=` 二元列表中的运算符是比较运算符，而不是赋值运算符。

 **错误 ID：** BC33000

## <a name="to-correct-this-error"></a>更正此错误

- 从一组可重载运算符中选择一个运算符。

- 如果你需要重载无法直接重载的运算符这一功能，请创建用于获取适当参数并返回适当值的 `Function` 过程。

## <a name="see-also"></a>请参阅

- [Operator Statement](../statements/operator-statement.md)
- [运算符过程](../../programming-guide/language-features/procedures/operator-procedures.md)
- [如何：定义运算符](../../programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [如何：定义转换运算符](../../programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [Function 语句](../statements/function-statement.md)

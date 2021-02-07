---
description: 了解详细信息： BC32008： " <typename> " 是委托类型
title: “<typename>”是委托类型
ms.date: 07/20/2015
f1_keywords:
- bc32008
- vbc32008
helpviewer_keywords:
- BC32008
ms.assetid: dc6abba0-a9ad-450f-8899-87265bc84abc
ms.openlocfilehash: 72aac48038c433b7938c54e7f1138a5b91bf7689
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99675021"
---
# <a name="bc32008-typename-is-a-delegate-type"></a>BC32008： " \<typename> " 是委托类型

" \<typename> " 是委托类型。 委托构造仅允许将单个 AddressOf 表达式作为参数列表。 通常可以使用 AddressOf 表达式，而不是委托构造。

 `New`创建委托类的实例的子句为委托构造函数提供了无效的参数列表。

 `AddressOf`创建新的委托实例时，只能提供单个表达式。

 如果传递多个参数，或者传递的单个自变量不是有效的表达式，则可能会导致此错误的原因 `AddressOf` 。

 **错误 ID：** BC32008

## <a name="to-correct-this-error"></a>更正此错误

- 使用子句中的 `AddressOf` 委托类的参数列表中的单个表达式 `New` 。

## <a name="see-also"></a>请参阅

- [新建操作员](../operators/new-operator.md)
- [AddressOf 运算符](../operators/addressof-operator.md)
- [委托](../../programming-guide/language-features/delegates/index.md)
- [如何：调用委托方法](../../programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)

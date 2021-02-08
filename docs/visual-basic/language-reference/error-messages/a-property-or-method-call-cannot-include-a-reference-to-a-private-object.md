---
description: 了解详细信息：属性或方法调用不能包括对私有对象的引用，不管是作为参数还是作为返回值
title: 无论是作为参数还是作为返回值，属性或方法调用都不能包括对私有对象的引用
ms.date: 07/20/2015
f1_keywords:
- vbrID98
ms.assetid: 059b43e1-202d-4fa2-806b-7bad63c1e7ca
ms.openlocfilehash: 8fe570c9ed789a5bac36aafa9b1ec2f507a55d51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797193"
---
# <a name="a-property-or-method-call-cannot-include-a-reference-to-a-private-object-either-as-an-argument-or-as-a-return-value"></a>无论是作为参数还是作为返回值，属性或方法调用都不能包括对私有对象的引用

此错误的可能原因包括：

- 客户端调用了进程外组件的属性或方法，并且试图将对私有对象的引用作为参数之一进行传递。

- 进程外组件调用了其客户端上的回调方法，并试图传递对私有对象的引用。

- 进程外组件试图将对私有对象的引用作为它所引发的事件的参数进行传递。

- 客户端试图将私有对象引用赋给它正在处理的事件的 `ByRef` 参数。

## <a name="to-correct-this-error"></a>更正此错误

- 删除引用。

## <a name="see-also"></a>请参阅

- [专用](../modifiers/private.md)

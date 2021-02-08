---
description: 了解详细信息： BC31535：友元程序集引用 <reference> 无效
title: 友元程序集引用 <reference> 无效
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: e3e08edede9bee4710c415a61592857229ea4f35
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796192"
---
# <a name="bc31535-friend-assembly-reference-reference-is-invalid"></a>BC31535：友元程序集引用 \<reference> 无效

友元程序集引用 \<reference> 无效。 用强名称签名的程序集必须在他们的 InternalsVisibleTo 声明中指定一个公钥。

 传递给特性构造函数的程序集名称 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> 标识强名称程序集，但不包括 `PublicKey` 特性。

 **错误 ID：** BC31535

## <a name="to-correct-this-error"></a>更正此错误

1. 确定强名称友元程序集的公钥。 使用属性将公钥包含为传递给特性构造函数的程序集名称的一部分 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> `PublicKey` 。

## <a name="see-also"></a>请参阅

- <xref:System.Reflection.AssemblyName>
- [友元程序集](../../../standard/assembly/friend.md)

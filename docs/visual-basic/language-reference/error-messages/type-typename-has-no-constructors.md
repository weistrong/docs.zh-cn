---
description: 了解详细信息： BC30251：类型 " <typename> " 没有构造函数
title: 类型“<typename>”没有构造函数
ms.date: 07/20/2015
f1_keywords:
- bc30251
- vbc30251
helpviewer_keywords:
- BC30251
ms.assetid: aff3e1df-abe6-4bc0-9abc-a1e70514c561
ms.openlocfilehash: 32ae854e9f1b037a17d9c378ce7ee4a3f9b43ad2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641169"
---
# <a name="bc30251-type-typename-has-no-constructors"></a>BC30251：类型 " \<typename> " 没有构造函数

某个类型不支持对 `Sub New()` 的调用。 一个可能的原因是编译器或二进制文件被损坏。

 **错误 ID：** BC30251

## <a name="to-correct-this-error"></a>更正此错误

1. 如果该类型位于其他项目或一个引用的文件中，则重新安装此项目或文件。

2. 如果该类型位于同一个项目中，则重新编译包含该类型的程序集。

3. 如果错误重复出现，请重新安装 Visual Basic 编译器。

4. 如果仍然出现错误，则收集有关该情况的信息并通知 Microsoft 产品支持服务。

## <a name="see-also"></a>请参阅

- [对象和类](../../programming-guide/language-features/objects-and-classes/index.md)
- [与我们交流](/visualstudio/ide/feedback-options)

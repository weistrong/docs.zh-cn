---
description: 了解更多相关信息： BC30043： " <keyword> " 仅在实例方法中有效
title: “<keyword>”只在实例方法中有效
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: 0bca2df44e096da016c9cb0c2031a8ef6faeb2b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795971"
---
# <a name="bc30043-keyword-is-valid-only-within-an-instance-method"></a>BC30043： " \<keyword> " 仅在实例方法中有效

`Me`、 `MyClass` 和 `MyBase` 关键字引用特定的类实例。 不能在共享或过程中使用它们 `Function` `Sub` 。

*错误 ID：** BC30043

## <a name="to-correct-this-error"></a>更正此错误

- 从过程中删除关键字，或 `Shared` 从过程声明中删除关键字。

## <a name="see-also"></a>请参阅

- [对象变量赋值](../../programming-guide/language-features/variables/object-variable-assignment.md)
- [Me、My、MyBase 和 MyClass](../../programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [继承基础知识](../../programming-guide/language-features/objects-and-classes/inheritance-basics.md)

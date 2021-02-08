---
description: 了解详细信息： BC30617： "Module" 语句只能出现在文件级或命名空间级
title: “Module”语句只能出现在文件级或命名空间级
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: f5c3ea0cd1c08fb0243043ae50e707e2c59b00f2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795776"
---
# <a name="bc30617-module-statements-can-occur-only-at-file-or-namespace-level"></a>BC30617： "Module" 语句只能出现在文件级或命名空间级

`Module` 语句必须紧跟在 `Option` 和 `Imports` 语句、全局特性和命名空间声明之后、但在其他所有声明之前。

 **错误 ID：** BC30617

## <a name="to-correct-this-error"></a>更正此错误

- 将 `Module` 语句移动到命名空间声明或源文件的顶部。

## <a name="see-also"></a>请参阅

- [Module 语句](../statements/module-statement.md)

---
description: 了解有关以下内容的详细信息： BC30157：前导 "." 或 "！" 只能出现在 "With" 语句内
title: 前导“.”或“!”只能出现在“With”语句内
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: e0325ac3c54046718d71df37edaac1edaf12f43e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795893"
---
# <a name="bc30157-leading--or--can-only-appear-inside-a-with-statement"></a>BC30157：前导 "." 或 "！" 只能出现在 "With" 语句内

不在块内部的 ) 或惊叹号 (！ ) 的句点 ( 没有 `With` 左侧的表达式。 成员访问 (`.`) 和字典成员访问 (`!`) 要求一个表达式，该表达式指定包含成员的元素。 这必须立即出现在访问器的左侧，或作为 `With` 包含成员访问的块的目标。

 **错误 ID：** BC30157

## <a name="to-correct-this-error"></a>更正此错误

1. 确保块的 `With` 格式正确。

2. 如果没有 `With` 块，请在取值函数左侧添加一个表达式，该表达式的计算结果为包含成员的已定义元素。

## <a name="see-also"></a>请参阅

- [代码中的特殊字符](../../programming-guide/program-structure/special-characters-in-code.md)
- [With...End With 语句](../statements/with-end-with-statement.md)

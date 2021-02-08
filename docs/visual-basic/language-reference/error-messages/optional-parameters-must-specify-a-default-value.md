---
description: 了解详细信息： BC30812：可选参数必须指定默认值
title: 可选参数必须指定默认值
ms.date: 07/20/2015
f1_keywords:
- vbc30812
- bc30812
helpviewer_keywords:
- BC30812
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
ms.openlocfilehash: 1cbed1c0f1297ecacdae94d9234d18a3d268f487
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795529"
---
# <a name="bc30812-optional-parameters-must-specify-a-default-value"></a>BC30812：可选参数必须指定默认值

可选参数必须提供默认值，如果调用过程未提供任何参数，则可以使用这些默认值。

**错误 ID：** BC30812

## <a name="example"></a>示例

下面的示例生成 BC30812：

```vb
Sub Proc1(x As Integer, Optional y As String)
    Console.WriteLine("Default argument is: " & y)
End Sub
```

## <a name="to-correct-this-error"></a>更正此错误

指定可选参数的默认值：

```vb
Sub Proc1(x As Integer, Optional y As String = "Default Value")
    Console.WriteLine("Default argument is: " & y)
End Sub
```

## <a name="see-also"></a>请参阅

- [可选](../modifiers/optional.md)

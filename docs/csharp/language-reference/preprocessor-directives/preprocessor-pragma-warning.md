---
description: '#pragma warning - C# 参考'
title: '#pragma warning - C# 参考'
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 16582a74bd34f2c0d89950280f1d5fde25435eea
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99215987"
---
# <a name="pragma-warning-c-reference"></a>#pragma warning（C# 参考）

`#pragma warning` 可以启用或禁用特定警告。

## <a name="syntax"></a>语法

```csharp
#pragma warning disable warning-list
#pragma warning restore warning-list
```

## <a name="parameters"></a>参数

 `warning-list` 以逗号分隔的警告编号的列表。 “CS”前缀是可选的。

 未指定警告编号时，`disable` 会禁用所有警告，`restore` 会启用所有警告。

> [!NOTE]
> 若要在 Visual Studio 中查找警告编号，请生成项目，然后在“输出”窗口中查找警告编号。

## <a name="example"></a>示例

```csharp
// pragma_warning.cs
using System;

#pragma warning disable 414, CS3021
[CLSCompliant(false)]
public class C
{
    int i = 1;
    static void Main()
    {
    }
}
#pragma warning restore CS3021
[CLSCompliant(false)]  // CS3021
public class D
{
    int i = 1;
    public static void F()
    {
    }
}
```

## <a name="see-also"></a>请参阅

- [C# 参考](../index.md)
- [C# 编程指南](../../programming-guide/index.md)
- [C# 预处理器指令](./index.md)
- [C# 编译器错误](../compiler-messages/index.md)
- [如何禁止显示代码分析警告](../../../fundamentals/code-analysis/suppress-warnings.md)

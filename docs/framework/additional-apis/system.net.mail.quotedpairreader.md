---
description: 了解详细信息： QuotedPairReader 类
title: 'QuotedPairReader 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Mail.QuotedPairReader
- System.Net.Mail.QuotedPairReader.CountQuotedChars
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 810a7b02948a1b7aa542a179563af9a6d79dd763
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699657"
---
# <a name="quotedpairreader-class"></a>QuotedPairReader 类

确定在带引号的字符串中 (转义) 的引号字符。 此类不能被继承。

```csharp
internal static class QuotedPairReader
```

> [!WARNING]
> 此类是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此类。

## <a name="countquotedchars-method"></a>CountQuotedChars 方法

计算指定字符串中连续带引号的字符数（包括多个前面带引号的反斜杠）。 例如，给定的字符串 `a\\\b` 和索引 `4` ，该方法返回 `4` ，因为带有引号， `b` 因此是前面三个反斜杠。

```csharp
internal static int CountQuotedChars(string data, int index, bool permitUnicodeEscaping)
```

### <a name="parameters"></a>参数

- `data` <xref:System.String>

  用于对连续带引号字符进行计数的数据字符串。

- `index` <xref:System.Int32>

  指定字符串中的位置，最多包含和包括应对哪些连续的带引号字符进行计数。

- `permitUnicodeEscaping` <xref:System.Boolean>

  `true` 允许转义 Unicode 字符;否则为 `false` 。

### <a name="return-value"></a>返回值

<xref:System.Int32?displayProperty=nameWithType>

`0` 如果指定索引处的字符未转义，则为; 否则为。否则，则为，最多包含中的字符（包括字符） `index` 。

### <a name="exceptions"></a>异常

<xref:System.FormatException?displayProperty=nameWithType>

找到了一个转义的 Unicode 字符，但不允许这样做。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 

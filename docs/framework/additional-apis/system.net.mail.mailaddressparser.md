---
description: 了解详细信息： MailAddressParser 类
title: 'MailAddressParser 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Mail.MailAddressParser
- System.Net.Mail.MailAddressParser.ParseAddress
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 5ad534e731e283f5449b3b8cc8e87628716da9b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699761"
---
# <a name="mailaddressparser-class"></a>MailAddressParser 类

如 RFC 2822 中所述分析电子邮件地址。 此类不能被继承。

```csharp
internal static class MailAddressParser
```

> [!WARNING]
> 此类是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此类。

## <a name="parseaddress-method"></a>ParseAddress 方法

分析指定字符串中的单个电子邮件地址。

```csharp
internal static MailAddress ParseAddress(string data)
```

### <a name="parameters"></a>参数

`data` <xref:System.String>

包含要分析的电子邮件地址的字符串。

### <a name="return-value"></a>返回值

<xref:System.Net.Mail.MailAddress>

有效的电子邮件地址。

### <a name="exceptions"></a>异常

<xref:System.FormatException?displayProperty=nameWithType>

电子邮件地址无效。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 

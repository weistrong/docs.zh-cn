---
description: 了解详细信息： SqlStreamChars (Char []，Int32，Int32) 方法
title: 'SqlStreamChars (Char []，Int32，Int32) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Read
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: a899ddff7b7242fcc32aaf7b7f7794970596027b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802575"
---
# <a name="sqlstreamcharsreadchar-int32-int32-method"></a>SqlStreamChars (Char []，Int32，Int32) 方法

当在派生类中重写时，从输入流中读取下一组字符。 包含此方法的程序集与 SQLAccess.dll 具有友元关系。 它旨在 SQL Server 使用。 对于其他数据库，请使用该数据库提供的托管机制。

```csharp
public abstract int Read (char[] buffer, int offset, int count);
```

## <a name="parameters"></a>参数

`buffer`\
要读取的字符数组。

`offset`\
相对于原点的偏移量。

`count`\
要从当前流中读取的字符数。

## <a name="returns"></a>返回

<xref:System.Int32>\
读入缓冲区的总字符数。

## <a name="remarks"></a>备注

> [!WARNING]
> `SqlStreamChars.Read`方法是私有的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Data.SqlTypes>

**程序集：** System.Data（在 System.Data.dll 中）

**.NET Framework 版本：** 自2.0 起可用。

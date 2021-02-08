---
description: 详细了解： SqlStreamChars. SetLength (Int64) 方法
title: 'SqlStreamChars. SetLength (Int64) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.SetLength
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d10ce55126ae09062fe895c3a686ce5d94174554
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804135"
---
# <a name="sqlstreamcharssetlengthint64-method"></a>SqlStreamChars)  (Int64 方法

当在派生类中重写时，释放流使用的资源。 包含此方法的程序集与 SQLAccess.dll 具有友元关系。 它旨在 SQL Server 使用。 对于其他数据库，请使用该数据库提供的托管机制。

```csharp
public abstract void SetLength (long value);
```

## <a name="parameters"></a>参数

`value`\
所需的当前流的长度（以字节表示）。

## <a name="remarks"></a>备注

> [!WARNING]
> `SqlStreamChars.SetLength`方法是私有的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Data.SqlTypes>

**程序集：** System.Data（在 System.Data.dll 中）

**.NET Framework 版本：** 自2.0 起可用。

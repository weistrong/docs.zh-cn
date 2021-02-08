---
description: 详细了解： SqlStreamChars (Int64、SeekOrigin) 方法
title: 'SqlStreamChars (Int64，SeekOrigin) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 00f71aff95045d566b7932aec3f7e18259b4dfa0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802562"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a>SqlStreamChars (Int64，SeekOrigin) 方法

当在派生类中重写时，设置当前流中的位置。 包含此方法的程序集与 SQLAccess.dll 具有友元关系。 它旨在 SQL Server 使用。 对于其他数据库，请使用该数据库提供的托管机制。

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a>参数

`offset`\
相对于 `origin` 的字节偏移量。

`origin`\
枚举值之一，指示要从中获取新位置的参考点。

## <a name="returns"></a>返回

<xref:System.Int32>\
当前流中的新位置。

## <a name="remarks"></a>备注

> [!WARNING]
> `SqlStreamChars.Seek`方法是私有的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Data.SqlTypes>

**程序集：** System.Data（在 System.Data.dll 中）

**.NET Framework 版本：** 自2.0 起可用。

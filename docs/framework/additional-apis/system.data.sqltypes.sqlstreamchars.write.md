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
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 3031b57902215df01c5c30625281a99be73ba2d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802549"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a>SqlStreamChars (Char []，Int32，Int32) 方法

当在派生类中重写时，将字符序列写入当前流，并将此流中的当前位置提升写入的字符数。 包含此方法的程序集与 SQLAccess.dll 具有友元关系。 它旨在 SQL Server 使用。 对于其他数据库，请使用该数据库提供的托管机制。

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a>参数

`buffer`  
要写入的字符数组。

`offset`  
相对于原点的偏移量。

`count`  
要写入当前流的字符数。

## <a name="remarks"></a>备注

> [!WARNING]
> `SqlStreamChars.Write`方法是私有的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Data.SqlTypes>

**程序集：** System.Data（在 System.Data.dll 中）

**.NET Framework 版本：** 自2.0 起可用。

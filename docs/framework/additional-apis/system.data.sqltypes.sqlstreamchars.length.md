---
description: 了解详细信息： SqlStreamChars 属性
title: 'SqlStreamChars 属性 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Length
- System.Data.SqlTypes.SqlStreamChars.get_Length
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: b0a9686cadc6d4018c7f291f0326b71195fd5cf5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802588"
---
# <a name="sqlstreamcharslength-property"></a>SqlStreamChars 属性

当在派生类中重写时，获取当前流的长度。 包含此属性的程序集与 SQLAccess.dll 具有友元关系。 它旨在 SQL Server 使用。 对于其他数据库，请使用该数据库提供的托管机制。

## <a name="syntax"></a>语法

```csharp
public abstract long Length { get; }
```

## <a name="property-value"></a>属性值

<xref:System.Int64>\
流的长度。

## <a name="remarks"></a>备注

> [!WARNING]
> `SqlStreamChars.Length`属性是私有的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Data.SqlTypes>

**程序集：** System.Data（在 System.Data.dll 中）

**.NET Framework 版本：** 自2.0 起可用。

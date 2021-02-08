---
description: 了解详细信息： SmiOrderProperty 属性
title: SmiOrderProperty)  (项属性
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- Microsoft.SqlServer.Server.SmiOrderProperty.Item
- Microsoft.SqlServer.Server.SmiOrderProperty.get_Item
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: fc2151d3f36a6746e80e2fd6d611a803b2c3162e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767981"
---
# <a name="smiorderpropertyitem-property"></a>SmiOrderProperty 属性

获取实体的列顺序。 包含此属性的程序集与 SQLAccess.dll 具有友元关系。 它旨在 SQL Server 使用。 对于其他数据库，请使用该数据库提供的托管机制。

## <a name="syntax"></a>语法

```csharp
internal SmiColumnOrder Item { get; }
```

## <a name="property-value"></a>属性值

列顺序。

## <a name="remarks"></a>备注

> [!WARNING]
> `SmiOrderProperty.Item`属性是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。

## <a name="requirements"></a>要求

**命名空间：** <xref:Microsoft.SqlServer.Server>

**程序集：** System.Data（在 System.Data.dll 中）

**.NET Framework 版本：** 自2.0 起可用。

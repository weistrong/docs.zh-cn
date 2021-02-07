---
description: 了解详细信息：设置了 webheadercollection. AddInternal 方法
title: '设置了 webheadercollection. AddInternal 方法 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.WebHeaderCollection.AddInternal
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 7bc84f84e6656dba5230b627fe9decfc4e0b4746
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699475"
---
# <a name="webheadercollectionaddinternal-method"></a>设置了 webheadercollection. AddInternal 方法

将具有指定名称和值的新标头添加到集合，并跳过检查。

```csharp
internal void AddInternal(string name, string value)
```

> [!WARNING]
> 此方法是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="parameters"></a>参数

- `name` <xref:System.String>

  标头的名称。

- `value` <xref:System.String>

  标头的值。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 

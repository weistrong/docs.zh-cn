---
description: 了解详细信息： TlsStream.m_Worker 字段
title: 'TlsStream.m_Worker 字段 (System.Net) '
ms.date: 10/21/2019
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.TlsStream.m_Worker
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: d929b0b1949bc1902425c016bfd770d4c66a3257
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699514"
---
# <a name="tlsstreamm_worker-field"></a>TlsStream.m_Worker 字段

表示 SSL 流的状态。

## <a name="syntax"></a>语法

```csharp
private SslState m_Worker;
```

## <a name="field-value"></a>字段值

`System.Net.Security.SslState`  
SSL 流的状态。

## <a name="remarks"></a>备注

> [!WARNING]
> 此 `TlsStream.m_Worker` 字段是专用的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此字段。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 

**.NET Framework 版本：** 自2.0 起可用。

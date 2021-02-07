---
description: 了解详细信息： SslState. SslProtocol 属性
title: SslState)  (系统 .Net。安全
ms.date: 10/21/2019
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Security.SslState.SslProtocol
- System.Net.Security.SslState.get_SslProtocol
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: b0b9bebf23fcd8d643d06f1cff10c260c77a7c08
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699618"
---
# <a name="sslstatesslprotocol-property"></a>SslState. SslProtocol 属性

获取 SSL 协议版本。

## <a name="syntax"></a>语法

```csharp
internal SslProtocols SslProtocol { get; }
```

## <a name="property-value"></a>属性值

<xref:System.Security.Authentication.SslProtocols>  
枚举值的按位组合，这些枚举值指定 SSL 协议版本。

## <a name="remarks"></a>备注

> [!WARNING]
> `SslState.SslProtocol`属性是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net.Security>

**程序集：** System.dll 中的系统 () 

**.NET Framework 版本：** 自2.0 起可用。

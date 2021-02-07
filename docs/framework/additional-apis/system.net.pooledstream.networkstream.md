---
description: 了解详细信息： PooledStream. NetworkStream 属性
title: 'PooledStream NetworkStream (System.Net) '
ms.date: 10/21/2019
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.PooledStream.NetworkStream
- System.Net.PooledStream.get_NetworkStream
- System.Net.PooledStream.set_NetworkStream
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 8a4f1d6bd9297028e763ef73bf96f85cbbfdafd6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699631"
---
# <a name="pooledstreamnetworkstream-property"></a>PooledStream. NetworkStream 属性

获取或设置套接字的网络流 `PooledStream` 。

## <a name="syntax"></a>语法

```csharp
internal NetworkStream NetworkStream { get; set; }
```

## <a name="property-value"></a>属性值

<xref:System.Net.Sockets.NetworkStream>  
套接字的网络流 `PooledStream` 。

## <a name="remarks"></a>备注

> [!WARNING]
> `PooledStream.NetworkStream`属性是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 

**.NET Framework 版本：** 自2.0 起可用。

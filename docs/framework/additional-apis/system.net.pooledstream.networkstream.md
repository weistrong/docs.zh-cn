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
# <a name="pooledstreamnetworkstream-property"></a><span data-ttu-id="0d0c7-103">PooledStream. NetworkStream 属性</span><span class="sxs-lookup"><span data-stu-id="0d0c7-103">PooledStream.NetworkStream Property</span></span>

<span data-ttu-id="0d0c7-104">获取或设置套接字的网络流 `PooledStream` 。</span><span class="sxs-lookup"><span data-stu-id="0d0c7-104">Gets or sets the network stream for the `PooledStream` socket.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0c7-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d0c7-105">Syntax</span></span>

```csharp
internal NetworkStream NetworkStream { get; set; }
```

## <a name="property-value"></a><span data-ttu-id="0d0c7-106">属性值</span><span class="sxs-lookup"><span data-stu-id="0d0c7-106">Property value</span></span>

<xref:System.Net.Sockets.NetworkStream>  
<span data-ttu-id="0d0c7-107">套接字的网络流 `PooledStream` 。</span><span class="sxs-lookup"><span data-stu-id="0d0c7-107">The network stream for the `PooledStream` socket.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0c7-108">备注</span><span class="sxs-lookup"><span data-stu-id="0d0c7-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="0d0c7-109">`PooledStream.NetworkStream`属性是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="0d0c7-109">The `PooledStream.NetworkStream` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="0d0c7-110">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="0d0c7-110">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0c7-111">要求</span><span class="sxs-lookup"><span data-stu-id="0d0c7-111">Requirements</span></span>

<span data-ttu-id="0d0c7-112">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="0d0c7-112">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="0d0c7-113">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="0d0c7-113">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="0d0c7-114">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="0d0c7-114">**.NET Framework versions:** Available since 2.0.</span></span>

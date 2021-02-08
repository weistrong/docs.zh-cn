---
description: 了解详细信息： SqlStreamChars (布尔) 方法
title: 'SqlStreamChars (布尔) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Dispose
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: ce24cc885d87a3ff0bbcdbea7992ca78ee592454
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802601"
---
# <a name="sqlstreamcharsdisposeboolean-method"></a><span data-ttu-id="b1c5f-103">SqlStreamChars (布尔) 方法</span><span class="sxs-lookup"><span data-stu-id="b1c5f-103">SqlStreamChars.Dispose(Boolean) Method</span></span>

<span data-ttu-id="b1c5f-104">当在派生类中重写时，释放流使用的资源。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-104">When overridden in a derived class, releases the resources used by the stream.</span></span> <span data-ttu-id="b1c5f-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="b1c5f-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="b1c5f-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
protected virtual void Dispose (bool disposing);
```

## <a name="parameters"></a><span data-ttu-id="b1c5f-108">参数</span><span class="sxs-lookup"><span data-stu-id="b1c5f-108">Parameters</span></span>

`disposing`\
<span data-ttu-id="b1c5f-109">若要释放托管资源和非托管资源，则为 `true`；若仅释放非托管资源，则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-109">`true` to release both managed and unmanaged resources; `false` to release only unmanaged resources.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1c5f-110">备注</span><span class="sxs-lookup"><span data-stu-id="b1c5f-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="b1c5f-111">`SqlStreamChars.Dispose`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-111">The `SqlStreamChars.Dispose` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="b1c5f-112">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-112">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1c5f-113">要求</span><span class="sxs-lookup"><span data-stu-id="b1c5f-113">Requirements</span></span>

<span data-ttu-id="b1c5f-114">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="b1c5f-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="b1c5f-115">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="b1c5f-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="b1c5f-116">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="b1c5f-116">**.NET Framework versions:** Available since 2.0.</span></span>

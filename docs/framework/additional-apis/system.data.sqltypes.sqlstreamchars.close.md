---
description: 了解详细信息： SqlStreamChars 方法
title: 'SqlStreamChars 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Close
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 27f2ea6e288d166f3b63979a83a1cf80eeced334
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782372"
---
# <a name="sqlstreamcharsclose-method"></a><span data-ttu-id="1043f-103">SqlStreamChars 方法</span><span class="sxs-lookup"><span data-stu-id="1043f-103">SqlStreamChars.Close Method</span></span>

<span data-ttu-id="1043f-104">关闭当前流并释放与该流关联的任何系统资源。</span><span class="sxs-lookup"><span data-stu-id="1043f-104">Closes the current stream and releases any system resources associated with the stream.</span></span> <span data-ttu-id="1043f-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="1043f-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="1043f-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="1043f-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="1043f-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="1043f-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public virtual void Close ();
```

## <a name="remarks"></a><span data-ttu-id="1043f-108">备注</span><span class="sxs-lookup"><span data-stu-id="1043f-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="1043f-109">`SqlStreamChars.Close`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="1043f-109">The `SqlStreamChars.Close` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="1043f-110">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="1043f-110">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="1043f-111">要求</span><span class="sxs-lookup"><span data-stu-id="1043f-111">Requirements</span></span>

<span data-ttu-id="1043f-112">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="1043f-112">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="1043f-113">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="1043f-113">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="1043f-114">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="1043f-114">**.NET Framework versions:** Available since 2.0.</span></span>

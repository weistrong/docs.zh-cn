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
- System.Data.SqlTypes.SqlStreamChars.Flush
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 8f519ffb8248a17608319eb0fbfe598f9ee3487a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684459"
---
# <a name="sqlstreamcharsflush-method"></a><span data-ttu-id="540c0-103">SqlStreamChars 方法</span><span class="sxs-lookup"><span data-stu-id="540c0-103">SqlStreamChars.Flush Method</span></span>

<span data-ttu-id="540c0-104">当在派生类中重写时，将清除该流的所有缓冲区，并使得所有缓冲数据被写入到基础设备。</span><span class="sxs-lookup"><span data-stu-id="540c0-104">When overridden in a derived class, clears all buffers for this stream and causes any buffered data to be written to the underlying device.</span></span> <span data-ttu-id="540c0-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="540c0-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="540c0-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="540c0-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="540c0-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="540c0-107">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="540c0-108">语法</span><span class="sxs-lookup"><span data-stu-id="540c0-108">Syntax</span></span>

```csharp
public abstract void Flush ();
```

## <a name="remarks"></a><span data-ttu-id="540c0-109">备注</span><span class="sxs-lookup"><span data-stu-id="540c0-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="540c0-110">`SqlStreamChars.Flush`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="540c0-110">The `SqlStreamChars.Flush` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="540c0-111">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="540c0-111">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="540c0-112">要求</span><span class="sxs-lookup"><span data-stu-id="540c0-112">Requirements</span></span>

<span data-ttu-id="540c0-113">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="540c0-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="540c0-114">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="540c0-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="540c0-115">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="540c0-115">**.NET Framework versions:** Available since 2.0.</span></span>

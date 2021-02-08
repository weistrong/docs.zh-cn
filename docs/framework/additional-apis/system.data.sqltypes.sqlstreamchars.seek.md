---
description: 详细了解： SqlStreamChars (Int64、SeekOrigin) 方法
title: 'SqlStreamChars (Int64，SeekOrigin) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 00f71aff95045d566b7932aec3f7e18259b4dfa0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802562"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a><span data-ttu-id="45b78-103">SqlStreamChars (Int64，SeekOrigin) 方法</span><span class="sxs-lookup"><span data-stu-id="45b78-103">SqlStreamChars.Seek(Int64, SeekOrigin) Method</span></span>

<span data-ttu-id="45b78-104">当在派生类中重写时，设置当前流中的位置。</span><span class="sxs-lookup"><span data-stu-id="45b78-104">When overridden in a derived class, sets the position within the current stream.</span></span> <span data-ttu-id="45b78-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="45b78-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="45b78-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="45b78-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="45b78-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="45b78-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a><span data-ttu-id="45b78-108">参数</span><span class="sxs-lookup"><span data-stu-id="45b78-108">Parameters</span></span>

`offset`\
<span data-ttu-id="45b78-109">相对于 `origin` 的字节偏移量。</span><span class="sxs-lookup"><span data-stu-id="45b78-109">A byte offset relative to `origin`.</span></span>

`origin`\
<span data-ttu-id="45b78-110">枚举值之一，指示要从中获取新位置的参考点。</span><span class="sxs-lookup"><span data-stu-id="45b78-110">One of the enumeration values that indicates the reference point from which to obtain the new position.</span></span>

## <a name="returns"></a><span data-ttu-id="45b78-111">返回</span><span class="sxs-lookup"><span data-stu-id="45b78-111">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="45b78-112">当前流中的新位置。</span><span class="sxs-lookup"><span data-stu-id="45b78-112">The new position within the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b78-113">备注</span><span class="sxs-lookup"><span data-stu-id="45b78-113">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="45b78-114">`SqlStreamChars.Seek`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="45b78-114">The `SqlStreamChars.Seek` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="45b78-115">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="45b78-115">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b78-116">要求</span><span class="sxs-lookup"><span data-stu-id="45b78-116">Requirements</span></span>

<span data-ttu-id="45b78-117">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="45b78-117">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="45b78-118">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="45b78-118">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="45b78-119">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="45b78-119">**.NET Framework versions:** Available since 2.0.</span></span>

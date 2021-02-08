---
description: 了解详细信息： SqlStreamChars (Char []，Int32，Int32) 方法
title: 'SqlStreamChars (Char []，Int32，Int32) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 3031b57902215df01c5c30625281a99be73ba2d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802549"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a><span data-ttu-id="04cc6-103">SqlStreamChars (Char []，Int32，Int32) 方法</span><span class="sxs-lookup"><span data-stu-id="04cc6-103">SqlStreamChars.Write(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="04cc6-104">当在派生类中重写时，将字符序列写入当前流，并将此流中的当前位置提升写入的字符数。</span><span class="sxs-lookup"><span data-stu-id="04cc6-104">When overridden in a derived class, writes a sequence of characters to the current stream and advances the current position within this stream by the number of characters written.</span></span> <span data-ttu-id="04cc6-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="04cc6-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="04cc6-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="04cc6-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="04cc6-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="04cc6-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="04cc6-108">参数</span><span class="sxs-lookup"><span data-stu-id="04cc6-108">Parameters</span></span>

`buffer`  
<span data-ttu-id="04cc6-109">要写入的字符数组。</span><span class="sxs-lookup"><span data-stu-id="04cc6-109">A char array to write.</span></span>

`offset`  
<span data-ttu-id="04cc6-110">相对于原点的偏移量。</span><span class="sxs-lookup"><span data-stu-id="04cc6-110">An offset relative to origin.</span></span>

`count`  
<span data-ttu-id="04cc6-111">要写入当前流的字符数。</span><span class="sxs-lookup"><span data-stu-id="04cc6-111">The number of characters to be written to the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="04cc6-112">备注</span><span class="sxs-lookup"><span data-stu-id="04cc6-112">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="04cc6-113">`SqlStreamChars.Write`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="04cc6-113">The `SqlStreamChars.Write` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="04cc6-114">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="04cc6-114">Microsoft does not support the use of this method write in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="04cc6-115">要求</span><span class="sxs-lookup"><span data-stu-id="04cc6-115">Requirements</span></span>

<span data-ttu-id="04cc6-116">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="04cc6-116">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="04cc6-117">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="04cc6-117">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="04cc6-118">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="04cc6-118">**.NET Framework versions:** Available since 2.0.</span></span>

---
description: 详细了解： SqlStreamChars. SetLength (Int64) 方法
title: 'SqlStreamChars. SetLength (Int64) 方法 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.SetLength
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d10ce55126ae09062fe895c3a686ce5d94174554
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804135"
---
# <a name="sqlstreamcharssetlengthint64-method"></a><span data-ttu-id="c7bfc-103">SqlStreamChars)  (Int64 方法</span><span class="sxs-lookup"><span data-stu-id="c7bfc-103">SqlStreamChars.SetLength(Int64) Method</span></span>

<span data-ttu-id="c7bfc-104">当在派生类中重写时，释放流使用的资源。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-104">When overridden in a derived class, releases the resources used by the stream.</span></span> <span data-ttu-id="c7bfc-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="c7bfc-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="c7bfc-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void SetLength (long value);
```

## <a name="parameters"></a><span data-ttu-id="c7bfc-108">参数</span><span class="sxs-lookup"><span data-stu-id="c7bfc-108">Parameters</span></span>

`value`\
<span data-ttu-id="c7bfc-109">所需的当前流的长度（以字节表示）。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-109">The desired length of the current stream in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7bfc-110">备注</span><span class="sxs-lookup"><span data-stu-id="c7bfc-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="c7bfc-111">`SqlStreamChars.SetLength`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-111">The `SqlStreamChars.SetLength` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="c7bfc-112">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-112">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bfc-113">要求</span><span class="sxs-lookup"><span data-stu-id="c7bfc-113">Requirements</span></span>

<span data-ttu-id="c7bfc-114">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="c7bfc-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="c7bfc-115">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="c7bfc-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="c7bfc-116">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="c7bfc-116">**.NET Framework versions:** Available since 2.0.</span></span>

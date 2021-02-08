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
- System.Data.SqlTypes.SqlStreamChars.Read
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: a899ddff7b7242fcc32aaf7b7f7794970596027b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802575"
---
# <a name="sqlstreamcharsreadchar-int32-int32-method"></a><span data-ttu-id="5f125-103">SqlStreamChars (Char []，Int32，Int32) 方法</span><span class="sxs-lookup"><span data-stu-id="5f125-103">SqlStreamChars.Read(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="5f125-104">当在派生类中重写时，从输入流中读取下一组字符。</span><span class="sxs-lookup"><span data-stu-id="5f125-104">When overridden in a derived class, reads the next set of characters from the input stream.</span></span> <span data-ttu-id="5f125-105">包含此方法的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="5f125-105">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="5f125-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="5f125-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="5f125-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="5f125-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract int Read (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="5f125-108">参数</span><span class="sxs-lookup"><span data-stu-id="5f125-108">Parameters</span></span>

`buffer`\
<span data-ttu-id="5f125-109">要读取的字符数组。</span><span class="sxs-lookup"><span data-stu-id="5f125-109">A char array to read.</span></span>

`offset`\
<span data-ttu-id="5f125-110">相对于原点的偏移量。</span><span class="sxs-lookup"><span data-stu-id="5f125-110">An offset relative to origin.</span></span>

`count`\
<span data-ttu-id="5f125-111">要从当前流中读取的字符数。</span><span class="sxs-lookup"><span data-stu-id="5f125-111">The number of characters to be read from the current stream.</span></span>

## <a name="returns"></a><span data-ttu-id="5f125-112">返回</span><span class="sxs-lookup"><span data-stu-id="5f125-112">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="5f125-113">读入缓冲区的总字符数。</span><span class="sxs-lookup"><span data-stu-id="5f125-113">The total number of characters read into the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f125-114">备注</span><span class="sxs-lookup"><span data-stu-id="5f125-114">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="5f125-115">`SqlStreamChars.Read`方法是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="5f125-115">The `SqlStreamChars.Read` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="5f125-116">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="5f125-116">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f125-117">要求</span><span class="sxs-lookup"><span data-stu-id="5f125-117">Requirements</span></span>

<span data-ttu-id="5f125-118">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="5f125-118">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="5f125-119">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="5f125-119">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="5f125-120">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="5f125-120">**.NET Framework versions:** Available since 2.0.</span></span>

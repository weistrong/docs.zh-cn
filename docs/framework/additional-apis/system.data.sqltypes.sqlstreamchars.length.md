---
description: 了解详细信息： SqlStreamChars 属性
title: 'SqlStreamChars 属性 (SqlTypes) '
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Length
- System.Data.SqlTypes.SqlStreamChars.get_Length
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: b0a9686cadc6d4018c7f291f0326b71195fd5cf5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802588"
---
# <a name="sqlstreamcharslength-property"></a><span data-ttu-id="ceccc-103">SqlStreamChars 属性</span><span class="sxs-lookup"><span data-stu-id="ceccc-103">SqlStreamChars.Length Property</span></span>

<span data-ttu-id="ceccc-104">当在派生类中重写时，获取当前流的长度。</span><span class="sxs-lookup"><span data-stu-id="ceccc-104">When overridden in a derived class, gets the length of the current stream.</span></span> <span data-ttu-id="ceccc-105">包含此属性的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="ceccc-105">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="ceccc-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="ceccc-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="ceccc-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="ceccc-107">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceccc-108">语法</span><span class="sxs-lookup"><span data-stu-id="ceccc-108">Syntax</span></span>

```csharp
public abstract long Length { get; }
```

## <a name="property-value"></a><span data-ttu-id="ceccc-109">属性值</span><span class="sxs-lookup"><span data-stu-id="ceccc-109">Property value</span></span>

<xref:System.Int64>\
<span data-ttu-id="ceccc-110">流的长度。</span><span class="sxs-lookup"><span data-stu-id="ceccc-110">The length of the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceccc-111">备注</span><span class="sxs-lookup"><span data-stu-id="ceccc-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="ceccc-112">`SqlStreamChars.Length`属性是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="ceccc-112">The `SqlStreamChars.Length` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="ceccc-113">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="ceccc-113">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceccc-114">要求</span><span class="sxs-lookup"><span data-stu-id="ceccc-114">Requirements</span></span>

<span data-ttu-id="ceccc-115">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="ceccc-115">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="ceccc-116">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="ceccc-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="ceccc-117">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="ceccc-117">**.NET Framework versions:** Available since 2.0.</span></span>

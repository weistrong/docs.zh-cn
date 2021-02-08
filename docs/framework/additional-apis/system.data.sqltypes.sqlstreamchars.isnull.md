---
description: 了解详细信息： SqlStreamChars 属性
title: SqlStreamChars (SqlTypes) 的属性
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.IsNull
- System.Data.SqlTypes.SqlStreamChars.get_IsNull
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: b1408a8ba9cd1c38f73d5fa6b818f441d6223bc8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791915"
---
# <a name="sqlstreamcharsisnull-property"></a><span data-ttu-id="e44ba-103">SqlStreamChars 属性</span><span class="sxs-lookup"><span data-stu-id="e44ba-103">SqlStreamChars.IsNull Property</span></span>

<span data-ttu-id="e44ba-104">当在派生类中重写时，获取一个值，该值指示流是否为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="e44ba-104">When overridden in a derived class, gets a value that indicates whether the stream is `null`.</span></span> <span data-ttu-id="e44ba-105">包含此属性的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="e44ba-105">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="e44ba-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="e44ba-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="e44ba-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="e44ba-107">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44ba-108">语法</span><span class="sxs-lookup"><span data-stu-id="e44ba-108">Syntax</span></span>

```csharp
public abstract bool IsNull { get; }
```

## <a name="property-value"></a><span data-ttu-id="e44ba-109">属性值</span><span class="sxs-lookup"><span data-stu-id="e44ba-109">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="e44ba-110">`true` 如果流为 `null` ，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="e44ba-110">`true` if the stream is `null`; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e44ba-111">备注</span><span class="sxs-lookup"><span data-stu-id="e44ba-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="e44ba-112">`SqlStreamChars.IsNull`属性是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="e44ba-112">The `SqlStreamChars.IsNull` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="e44ba-113">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="e44ba-113">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44ba-114">要求</span><span class="sxs-lookup"><span data-stu-id="e44ba-114">Requirements</span></span>

<span data-ttu-id="e44ba-115">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="e44ba-115">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="e44ba-116">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="e44ba-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="e44ba-117">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="e44ba-117">**.NET Framework versions:** Available since 2.0.</span></span>

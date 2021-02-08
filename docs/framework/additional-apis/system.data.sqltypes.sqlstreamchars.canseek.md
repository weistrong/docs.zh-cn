---
description: 了解详细信息： SqlStreamChars. CanSeek 属性
title: SqlStreamChars. SqlTypes)  (CanSeek 属性
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.CanSeek
- System.Data.SqlTypes.SqlStreamChars.get_CanSeek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 5919a66bef9ac31e0ef15ad4af64b456700605f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802614"
---
# <a name="sqlstreamcharscanseek-property"></a><span data-ttu-id="e0dd7-103">SqlStreamChars. CanSeek 属性</span><span class="sxs-lookup"><span data-stu-id="e0dd7-103">SqlStreamChars.CanSeek Property</span></span>

<span data-ttu-id="e0dd7-104">当在派生类中重写时，获取一个值，该值指示当前流是否支持查找操作。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-104">When overridden in a derived class, gets a value that indicates whether the current steam supports the seek operation.</span></span> <span data-ttu-id="e0dd7-105">包含此属性的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-105">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="e0dd7-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="e0dd7-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract bool CanSeek { get; }
```

## <a name="property-value"></a><span data-ttu-id="e0dd7-108">属性值</span><span class="sxs-lookup"><span data-stu-id="e0dd7-108">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="e0dd7-109">`true` 如果当前流支持查找操作，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-109">`true` if the current steam supports the seek operation; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0dd7-110">备注</span><span class="sxs-lookup"><span data-stu-id="e0dd7-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="e0dd7-111">`SqlStreamChars.CanSeek`属性是私有的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-111">The `SqlStreamChars.CanSeek` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="e0dd7-112">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-112">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dd7-113">要求</span><span class="sxs-lookup"><span data-stu-id="e0dd7-113">Requirements</span></span>

<span data-ttu-id="e0dd7-114">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="e0dd7-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="e0dd7-115">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="e0dd7-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="e0dd7-116">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="e0dd7-116">**.NET Framework versions:** Available since 2.0.</span></span>

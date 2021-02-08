---
description: 了解详细信息： SqlChars 属性
title: SqlChars (SqlTypes) 的属性
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlChars.Stream
- System.Data.SqlTypes.SqlChars.get_Stream
- System.Data.SqlTypes.SqlChars.set_Stream
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 9af0df98b268a749d890ab1b40dddbbe98ced8d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802640"
---
# <a name="sqlcharsstream-property"></a><span data-ttu-id="be566-103">SqlChars.Stream 属性</span><span class="sxs-lookup"><span data-stu-id="be566-103">SqlChars.Stream Property</span></span>

<span data-ttu-id="be566-104">获取或设置字符流。</span><span class="sxs-lookup"><span data-stu-id="be566-104">Gets or sets the character stream.</span></span> <span data-ttu-id="be566-105">包含此属性的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="be566-105">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="be566-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="be566-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="be566-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="be566-107">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
internal SqlStreamChars Stream { get; set; }
```

## <a name="property-value"></a><span data-ttu-id="be566-108">属性值</span><span class="sxs-lookup"><span data-stu-id="be566-108">Property value</span></span>

`System.Data.SqlTypes.SqlStreamChars`\
<span data-ttu-id="be566-109">字符流。</span><span class="sxs-lookup"><span data-stu-id="be566-109">The character stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="be566-110">备注</span><span class="sxs-lookup"><span data-stu-id="be566-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="be566-111">`SqlChars.Stream`属性是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="be566-111">The `SqlChars.Stream` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="be566-112">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="be566-112">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="be566-113">要求</span><span class="sxs-lookup"><span data-stu-id="be566-113">Requirements</span></span>

<span data-ttu-id="be566-114">**命名空间：** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="be566-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="be566-115">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="be566-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="be566-116">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="be566-116">**.NET Framework versions:** Available since 2.0.</span></span>

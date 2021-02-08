---
description: 了解详细信息： SmiOrderProperty 属性
title: SmiOrderProperty)  (项属性
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- Microsoft.SqlServer.Server.SmiOrderProperty.Item
- Microsoft.SqlServer.Server.SmiOrderProperty.get_Item
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: fc2151d3f36a6746e80e2fd6d611a803b2c3162e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767981"
---
# <a name="smiorderpropertyitem-property"></a><span data-ttu-id="2a50e-103">SmiOrderProperty 属性</span><span class="sxs-lookup"><span data-stu-id="2a50e-103">SmiOrderProperty.Item Property</span></span>

<span data-ttu-id="2a50e-104">获取实体的列顺序。</span><span class="sxs-lookup"><span data-stu-id="2a50e-104">Gets the column order for the entity.</span></span> <span data-ttu-id="2a50e-105">包含此属性的程序集与 SQLAccess.dll 具有友元关系。</span><span class="sxs-lookup"><span data-stu-id="2a50e-105">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="2a50e-106">它旨在 SQL Server 使用。</span><span class="sxs-lookup"><span data-stu-id="2a50e-106">It's intended for use by SQL Server.</span></span> <span data-ttu-id="2a50e-107">对于其他数据库，请使用该数据库提供的托管机制。</span><span class="sxs-lookup"><span data-stu-id="2a50e-107">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a50e-108">语法</span><span class="sxs-lookup"><span data-stu-id="2a50e-108">Syntax</span></span>

```csharp
internal SmiColumnOrder Item { get; }
```

## <a name="property-value"></a><span data-ttu-id="2a50e-109">属性值</span><span class="sxs-lookup"><span data-stu-id="2a50e-109">Property value</span></span>

<span data-ttu-id="2a50e-110">列顺序。</span><span class="sxs-lookup"><span data-stu-id="2a50e-110">The column order.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a50e-111">备注</span><span class="sxs-lookup"><span data-stu-id="2a50e-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="2a50e-112">`SmiOrderProperty.Item`属性是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="2a50e-112">The `SmiOrderProperty.Item` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="2a50e-113">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="2a50e-113">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a50e-114">要求</span><span class="sxs-lookup"><span data-stu-id="2a50e-114">Requirements</span></span>

<span data-ttu-id="2a50e-115">**命名空间：** <xref:Microsoft.SqlServer.Server></span><span class="sxs-lookup"><span data-stu-id="2a50e-115">**Namespace:** <xref:Microsoft.SqlServer.Server></span></span>

<span data-ttu-id="2a50e-116">**程序集：** System.Data（在 System.Data.dll 中）</span><span class="sxs-lookup"><span data-stu-id="2a50e-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="2a50e-117">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="2a50e-117">**.NET Framework versions:** Available since 2.0.</span></span>

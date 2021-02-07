---
description: 了解详细信息： ServicePointManager. CloseConnectionGroups 方法
title: 'ServicePointManager. CloseConnectionGroups 方法 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.ServicePointManager.CloseConnectionGroups
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 8cd1a1f0f4dbdaeaee117e6a7ae4219680363a6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699553"
---
# <a name="servicepointmanagercloseconnectiongroups-method"></a><span data-ttu-id="b7970-103">ServicePointManager. CloseConnectionGroups 方法</span><span class="sxs-lookup"><span data-stu-id="b7970-103">ServicePointManager.CloseConnectionGroups method</span></span>

<span data-ttu-id="b7970-104">循环访问所有服务点并关闭具有指定名称的连接组。</span><span class="sxs-lookup"><span data-stu-id="b7970-104">Iterates through all service points and closes connection groups that have the specified name.</span></span>

```csharp
internal static void CloseConnectionGroups(string connectionGroupName)
```

> [!WARNING]
> <span data-ttu-id="b7970-105">此方法是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="b7970-105">This method is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="b7970-106">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="b7970-106">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7970-107">参数</span><span class="sxs-lookup"><span data-stu-id="b7970-107">Parameters</span></span>

<span data-ttu-id="b7970-108">`connectionGroupName` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="b7970-108">`connectionGroupName` <xref:System.String></span></span>

<span data-ttu-id="b7970-109">要关闭的连接组的名称。</span><span class="sxs-lookup"><span data-stu-id="b7970-109">The name of the connection group to close.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7970-110">要求</span><span class="sxs-lookup"><span data-stu-id="b7970-110">Requirements</span></span>

<span data-ttu-id="b7970-111">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="b7970-111">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="b7970-112">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="b7970-112">**Assembly:** System (in System.dll)</span></span>

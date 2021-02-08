---
description: 了解详细信息： IXCLRDataProcess：： GetAppDomainByUniqueId 方法
title: IXCLRDataProcess：： GetAppDomainByUniqueId 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 7087362efbb810fcb6e1b6f7eb9f23c54c38fade
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800664"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="8d774-103">IXCLRDataProcess：： GetAppDomainByUniqueId 方法</span><span class="sxs-lookup"><span data-stu-id="8d774-103">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="8d774-104">`AppDomain`基于其唯一标识符，在进程中获取。</span><span class="sxs-lookup"><span data-stu-id="8d774-104">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="8d774-105">语法</span><span class="sxs-lookup"><span data-stu-id="8d774-105">Syntax</span></span>

```cpp
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

## <a name="parameters"></a><span data-ttu-id="8d774-106">参数</span><span class="sxs-lookup"><span data-stu-id="8d774-106">Parameters</span></span>

`id`\
<span data-ttu-id="8d774-107">中AppDomain 的唯一标识符</span><span class="sxs-lookup"><span data-stu-id="8d774-107">[in] The unique identifier of the AppDomain</span></span>

`appDomain`\
<span data-ttu-id="8d774-108">弄AppDomain</span><span class="sxs-lookup"><span data-stu-id="8d774-108">[out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="8d774-109">备注</span><span class="sxs-lookup"><span data-stu-id="8d774-109">Remarks</span></span>

<span data-ttu-id="8d774-110">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第20个槽。</span><span class="sxs-lookup"><span data-stu-id="8d774-110">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="8d774-111">`IXCLRDataAppDomain*`返回的用于与其他 api 交互。</span><span class="sxs-lookup"><span data-stu-id="8d774-111">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d774-112">要求</span><span class="sxs-lookup"><span data-stu-id="8d774-112">Requirements</span></span>

<span data-ttu-id="8d774-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8d774-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>
<span data-ttu-id="8d774-114">**标头：** 无 **库：** 无 **.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8d774-114">**Header:** None **Library:** None **.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="8d774-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d774-115">See also</span></span>

- [<span data-ttu-id="8d774-116">调试</span><span class="sxs-lookup"><span data-stu-id="8d774-116">Debugging</span></span>](index.md)
- [<span data-ttu-id="8d774-117">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="8d774-117">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)

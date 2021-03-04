---
description: 了解详细信息： ICorProfilerInfo10：： IsFrozenObject 方法
title: ICorProfilerInfo10::IsFrozenObject
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.IsFrozenObject
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 3b47204630056e2797b5cf126bd7c291830cea05
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102103447"
---
# <a name="icorprofilerinfo10isfrozenobject-method"></a><span data-ttu-id="30f91-103">ICorProfilerInfo10：： IsFrozenObject 方法</span><span class="sxs-lookup"><span data-stu-id="30f91-103">ICorProfilerInfo10::IsFrozenObject Method</span></span>

<span data-ttu-id="30f91-104">给定 ObjectID，确定对象是否位于只读段。</span><span class="sxs-lookup"><span data-stu-id="30f91-104">Given an ObjectID, determines whether the object is in a read-only segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f91-105">语法</span><span class="sxs-lookup"><span data-stu-id="30f91-105">Syntax</span></span>

```cpp
HRESULT IsFrozenObject( [in]  ObjectID objectId,
                        [out] BOOL *pbFrozen);
```

## <a name="parameters"></a><span data-ttu-id="30f91-106">参数</span><span class="sxs-lookup"><span data-stu-id="30f91-106">Parameters</span></span>

- `objectId`

  <span data-ttu-id="30f91-107">\[in] 要检查的对象。</span><span class="sxs-lookup"><span data-stu-id="30f91-107">\[in] The object to examine.</span></span>

- `pbFrozen`

  <span data-ttu-id="30f91-108">\[out] 一个 `BOOL` 值，该值指示对象是否位于只读段中。</span><span class="sxs-lookup"><span data-stu-id="30f91-108">\[out] A `BOOL` indicating if the object is in a read-only segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f91-109">要求</span><span class="sxs-lookup"><span data-stu-id="30f91-109">Requirements</span></span>

<span data-ttu-id="30f91-110">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="30f91-110">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="30f91-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="30f91-111">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="30f91-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="30f91-112">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="30f91-113">**.Net 版本：**[!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30f91-113">**.NET Versions:** [!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="30f91-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30f91-114">See also</span></span>

- [<span data-ttu-id="30f91-115">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="30f91-115">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)

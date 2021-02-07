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
ms.openlocfilehash: b07e456f7fa9c328217b8779733d45dfe2793fe2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753271"
---
# <a name="icorprofilerinfo10isfrozenobject-method"></a><span data-ttu-id="feb6f-103">ICorProfilerInfo10：： IsFrozenObject 方法</span><span class="sxs-lookup"><span data-stu-id="feb6f-103">ICorProfilerInfo10::IsFrozenObject Method</span></span>

<span data-ttu-id="feb6f-104">给定 ObjectID，确定对象是否位于只读段。</span><span class="sxs-lookup"><span data-stu-id="feb6f-104">Given an ObjectID, determines whether the object is in a read-only segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb6f-105">语法</span><span class="sxs-lookup"><span data-stu-id="feb6f-105">Syntax</span></span>

```cpp
HRESULT IsFrozenObject( [in]  ObjectID objectId,
                        [out] BOOL *pbFrozen);
```

## <a name="parameters"></a><span data-ttu-id="feb6f-106">参数</span><span class="sxs-lookup"><span data-stu-id="feb6f-106">Parameters</span></span>

- `objectId`

  <span data-ttu-id="feb6f-107">\[in] 要检查的对象。</span><span class="sxs-lookup"><span data-stu-id="feb6f-107">\[in] The object to examine.</span></span>

- `pbFrozen`

  <span data-ttu-id="feb6f-108">\[out] 一个 `BOOL` 值，该值指示对象是否位于只读段中。</span><span class="sxs-lookup"><span data-stu-id="feb6f-108">\[out] A `BOOL` indicating if the object is in a read-only segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb6f-109">要求</span><span class="sxs-lookup"><span data-stu-id="feb6f-109">Requirements</span></span>

<span data-ttu-id="feb6f-110">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="feb6f-110">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="feb6f-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="feb6f-111">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="feb6f-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="feb6f-112">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="feb6f-113">**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="feb6f-113">**.NET Versions:** [!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="feb6f-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="feb6f-114">See also</span></span>

- [<span data-ttu-id="feb6f-115">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="feb6f-115">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)

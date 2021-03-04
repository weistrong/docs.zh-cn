---
description: 了解详细信息： ICorProfilerInfo10：： EnumerateObjectReferences 方法
title: ICorProfilerInfo10::EnumerateObjectReferences
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.EnumerateObjectReferences
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: c18532450e420f38413028a18630dbf3e308fa61
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102106717"
---
# <a name="icorprofilerinfo10enumerateobjectreferences-method"></a><span data-ttu-id="9c396-103">ICorProfilerInfo10：： EnumerateObjectReferences 方法</span><span class="sxs-lookup"><span data-stu-id="9c396-103">ICorProfilerInfo10::EnumerateObjectReferences Method</span></span>

<span data-ttu-id="9c396-104">给定 ObjectID、callback 和 clientData，如果有任何) ，则枚举 (的每个对象引用。</span><span class="sxs-lookup"><span data-stu-id="9c396-104">Given an ObjectID, callback and clientData, enumerates each object reference (if any).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c396-105">语法</span><span class="sxs-lookup"><span data-stu-id="9c396-105">Syntax</span></span>

```cpp
HRESULT EnumerateObjectReferences( [in] ObjectID objectId,
                                   [in] ObjectReferenceCallback callback,
                                   [in] void* clientData);
```

## <a name="parameters"></a><span data-ttu-id="9c396-106">参数</span><span class="sxs-lookup"><span data-stu-id="9c396-106">Parameters</span></span>

- `objectId`

  <span data-ttu-id="9c396-107">\[in] 要在其上枚举引用的对象。</span><span class="sxs-lookup"><span data-stu-id="9c396-107">\[in] The object to enumerate references on.</span></span>

- `callback`

  <span data-ttu-id="9c396-108">\[in] 将与对象的引用一起调用的函数。</span><span class="sxs-lookup"><span data-stu-id="9c396-108">\[in] The function that will be called with the references for the object.</span></span>

- `clientData`

  <span data-ttu-id="9c396-109">\[in] 探查器提供的要传递给函数的数据 `callback` 。</span><span class="sxs-lookup"><span data-stu-id="9c396-109">\[in] Profiler-provided data to pass to the `callback` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c396-110">备注</span><span class="sxs-lookup"><span data-stu-id="9c396-110">Remarks</span></span>

<span data-ttu-id="9c396-111">`EnumerateObjectReferences`方法类似于[ObjectReferences](icorprofilercallback-objectreferences-method.md)，只不过它会按需对探查器进行引用，而不是预先分配用于存储引用的数组。</span><span class="sxs-lookup"><span data-stu-id="9c396-111">The `EnumerateObjectReferences` method is similar to [ObjectReferences](icorprofilercallback-objectreferences-method.md), except that it walks the references on demand for the profiler instead of pre-allocating an array to store the references.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c396-112">要求</span><span class="sxs-lookup"><span data-stu-id="9c396-112">Requirements</span></span>

<span data-ttu-id="9c396-113">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="9c396-113">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="9c396-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9c396-114">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="9c396-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9c396-115">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="9c396-116">**.Net 版本：**[!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c396-116">**.NET Versions:** [!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="9c396-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9c396-117">See also</span></span>

- [<span data-ttu-id="9c396-118">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="9c396-118">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)

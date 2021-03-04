---
description: 了解详细信息： ICorProfilerInfo10：： GetLOHObjectSizeThreshold 方法
title: ICorProfilerInfo10::GetLOHObjectSizeThreshold
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.GetLOHObjectSizeThreshold
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 96c502dba5b2807f9cd9c3c5cceb6b3b9985a406
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102106951"
---
# <a name="icorprofilerinfo10getlohobjectsizethreshold-method"></a><span data-ttu-id="33919-103">ICorProfilerInfo10：： GetLOHObjectSizeThreshold 方法</span><span class="sxs-lookup"><span data-stu-id="33919-103">ICorProfilerInfo10::GetLOHObjectSizeThreshold Method</span></span>

<span data-ttu-id="33919-104">获取已配置的大型对象堆的值 (LOH) 阈值。</span><span class="sxs-lookup"><span data-stu-id="33919-104">Gets the value of the configured large object heap (LOH) threshold.</span></span>

## <a name="syntax"></a><span data-ttu-id="33919-105">语法</span><span class="sxs-lookup"><span data-stu-id="33919-105">Syntax</span></span>

```cpp
HRESULT GetLOHObjectSizeThreshold( [out] DWORD *pThreshold );
```

## <a name="parameters"></a><span data-ttu-id="33919-106">参数</span><span class="sxs-lookup"><span data-stu-id="33919-106">Parameters</span></span>

- `pThreshold`

  <span data-ttu-id="33919-107">\[out] 大对象堆阈值（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="33919-107">\[out] The large object heap threshold in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="33919-108">备注</span><span class="sxs-lookup"><span data-stu-id="33919-108">Remarks</span></span>

<span data-ttu-id="33919-109">大于大型对象堆阈值的对象将在大型对象堆上分配。</span><span class="sxs-lookup"><span data-stu-id="33919-109">Objects larger than the large object heap threshold will be allocated on the large object heap.</span></span> <span data-ttu-id="33919-110">从 .NET Core 3.0 开始，大型对象堆阈值是可配置的， `pThreshold` 将包含活动的大型对象堆阈值大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="33919-110">Starting with .NET Core 3.0 the large object heap threshold is configurable, `pThreshold` will contain the active large object heap threshold size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="33919-111">要求</span><span class="sxs-lookup"><span data-stu-id="33919-111">Requirements</span></span>

<span data-ttu-id="33919-112">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="33919-112">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="33919-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="33919-113">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="33919-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="33919-114">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="33919-115">**.Net 版本：**[!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33919-115">**.NET Versions:** [!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="33919-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="33919-116">See also</span></span>

- [<span data-ttu-id="33919-117">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="33919-117">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)

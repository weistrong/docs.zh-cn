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
ms.openlocfilehash: 665a08ae226f04d5282b9584932078736751d5d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737302"
---
# <a name="icorprofilerinfo10getlohobjectsizethreshold-method"></a><span data-ttu-id="a0764-103">ICorProfilerInfo10：： GetLOHObjectSizeThreshold 方法</span><span class="sxs-lookup"><span data-stu-id="a0764-103">ICorProfilerInfo10::GetLOHObjectSizeThreshold Method</span></span>

<span data-ttu-id="a0764-104">获取已配置的大型对象堆的值 (LOH) 阈值。</span><span class="sxs-lookup"><span data-stu-id="a0764-104">Gets the value of the configured large object heap (LOH) threshold.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0764-105">语法</span><span class="sxs-lookup"><span data-stu-id="a0764-105">Syntax</span></span>

```cpp
HRESULT GetLOHObjectSizeThreshold( [out] DWORD *pThreshold );
```

## <a name="parameters"></a><span data-ttu-id="a0764-106">参数</span><span class="sxs-lookup"><span data-stu-id="a0764-106">Parameters</span></span>

- `pThreshold`

  <span data-ttu-id="a0764-107">\[out] 大对象堆阈值（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a0764-107">\[out] The large object heap threshold in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0764-108">备注</span><span class="sxs-lookup"><span data-stu-id="a0764-108">Remarks</span></span>

<span data-ttu-id="a0764-109">大于大型对象堆阈值的对象将在大型对象堆上分配。</span><span class="sxs-lookup"><span data-stu-id="a0764-109">Objects larger than the large object heap threshold will be allocated on the large object heap.</span></span> <span data-ttu-id="a0764-110">从 .NET Core 3.0 开始，大型对象堆阈值是可配置的， `pThreshold` 将包含活动的大型对象堆阈值大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a0764-110">Starting with .NET Core 3.0 the large object heap threshold is configurable, `pThreshold` will contain the active large object heap threshold size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0764-111">要求</span><span class="sxs-lookup"><span data-stu-id="a0764-111">Requirements</span></span>

<span data-ttu-id="a0764-112">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="a0764-112">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="a0764-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a0764-113">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="a0764-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a0764-114">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="a0764-115">**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0764-115">**.NET Versions:** [!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="a0764-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0764-116">See also</span></span>

- [<span data-ttu-id="a0764-117">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="a0764-117">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)

---
description: 了解详细信息： ICorProfilerInfo10：： RequestReJITWithInliners 方法
title: ICorProfilerInfo10::RequestReJITWithInliners
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.RequestReJITWithInliners
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: da3434926b36408adfdee2171d56f23ba764f0eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753258"
---
# <a name="icorprofilerinfo10requestrejitwithinliners-method"></a><span data-ttu-id="04d09-103">ICorProfilerInfo10：： RequestReJITWithInliners 方法</span><span class="sxs-lookup"><span data-stu-id="04d09-103">ICorProfilerInfo10::RequestReJITWithInliners Method</span></span>

<span data-ttu-id="04d09-104">ReJITs 请求的方法，以及所请求的方法的任何 inliners。</span><span class="sxs-lookup"><span data-stu-id="04d09-104">ReJITs the methods requested, as well as any inliners of the methods requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d09-105">语法</span><span class="sxs-lookup"><span data-stu-id="04d09-105">Syntax</span></span>

```cpp
HRESULT RequestReJITWithInliners( [in]                       DWORD       dwRejitFlags,
                                  [in]                       ULONG       cFunctions,
                                  [in, size_is(cFunctions)]  ModuleID    moduleIds[],
                                  [in, size_is(cFunctions)]  mdMethodDef methodIds[]);
```

## <a name="parameters"></a><span data-ttu-id="04d09-106">参数</span><span class="sxs-lookup"><span data-stu-id="04d09-106">Parameters</span></span>

- `dwRejitFlags`

  <span data-ttu-id="04d09-107">\[in] [COR_PRF_REJIT_FLAGS](cor-prf-rejit-flags-enumeration.md)的位掩码。</span><span class="sxs-lookup"><span data-stu-id="04d09-107">\[in] A bitmask of [COR_PRF_REJIT_FLAGS](cor-prf-rejit-flags-enumeration.md).</span></span>

- `cFunctions`

  <span data-ttu-id="04d09-108">\[in] 要重新编译的函数的数目。</span><span class="sxs-lookup"><span data-stu-id="04d09-108">\[in] The number of functions to recompile.</span></span>

- `moduleIds`

  <span data-ttu-id="04d09-109">\[in] 指定 `moduleId` (的部分 `module` ，) 对，用于 `methodDef` 标识要重新编译的函数。</span><span class="sxs-lookup"><span data-stu-id="04d09-109">\[in] Specifies the `moduleId` portion of the (`module`, `methodDef`) pairs that identify the functions to be recompiled.</span></span>

- `methodIds`

  <span data-ttu-id="04d09-110">\[in] 指定 `methodId` (的部分 `module` ，) 对，用于 `methodDef` 标识要重新编译的函数。</span><span class="sxs-lookup"><span data-stu-id="04d09-110">\[in] Specifies the `methodId` portion of the (`module`, `methodDef`) pairs that identify the functions to be recompiled.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d09-111">备注</span><span class="sxs-lookup"><span data-stu-id="04d09-111">Remarks</span></span>

<span data-ttu-id="04d09-112">[RequestReJIT](icorprofilerinfo4-requestrejit-method.md) 不会对内联方法进行任何跟踪。</span><span class="sxs-lookup"><span data-stu-id="04d09-112">[RequestReJIT](icorprofilerinfo4-requestrejit-method.md) does not do any tracking of inlined methods.</span></span> <span data-ttu-id="04d09-113">探查器应阻止内联或跟踪内联，并 `RequestReJIT` 为所有 inliners 调用以确保内联方法的每个实例都已 ReJITted。</span><span class="sxs-lookup"><span data-stu-id="04d09-113">The profiler was expected to either block inlining or track inlining and call `RequestReJIT` for all inliners to make sure every instance of an inlined method was ReJITted.</span></span> <span data-ttu-id="04d09-114">这会在附加上出现 ReJIT 问题，因为探查器不会监视内联。</span><span class="sxs-lookup"><span data-stu-id="04d09-114">This poses a problem with ReJIT on attach, since the profiler is not present to monitor inlining.</span></span> <span data-ttu-id="04d09-115">可以调用此方法来保证完整的 inliners 集也会 ReJITted。</span><span class="sxs-lookup"><span data-stu-id="04d09-115">This method can be called to guarantee that the full set of inliners will be ReJITted as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d09-116">要求</span><span class="sxs-lookup"><span data-stu-id="04d09-116">Requirements</span></span>

<span data-ttu-id="04d09-117">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="04d09-117">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="04d09-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="04d09-118">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="04d09-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="04d09-119">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="04d09-120">**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04d09-120">**.NET Versions:** [!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="04d09-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="04d09-121">See also</span></span>

- [<span data-ttu-id="04d09-122">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="04d09-122">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)

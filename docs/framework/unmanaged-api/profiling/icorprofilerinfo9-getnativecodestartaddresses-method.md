---
description: 了解详细信息： ICorProfilerInfo9：： GetNativeCodeStartAddresses 方法
title: ICorProfilerInfo9::GetNativeCodeStartAddresses
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo9.GetNativeCodeStartAddresses
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 1ca686cef4a45ebb9e05190fa790ed5300c0d816
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646486"
---
# <a name="icorprofilerinfo9getnativecodestartaddresses-method"></a><span data-ttu-id="43f26-103">ICorProfilerInfo9：： GetNativeCodeStartAddresses 方法</span><span class="sxs-lookup"><span data-stu-id="43f26-103">ICorProfilerInfo9::GetNativeCodeStartAddresses Method</span></span>

<span data-ttu-id="43f26-104">给定一个 functionId 和 rejitId，枚举此代码当前存在的所有实时编译版本的本机代码起始地址。</span><span class="sxs-lookup"><span data-stu-id="43f26-104">Given a functionId and rejitId, enumerates the native code start address of all jitted versions of this code that currently exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f26-105">语法</span><span class="sxs-lookup"><span data-stu-id="43f26-105">Syntax</span></span>

```cpp
HRESULT GetNativeCodeStartAddresses( [in]  FunctionID functionID,
                                     [in]  ReJITID reJitId,
                                     [in]  ULONG32 cCodeStartAddresses,
                                     [out] ULONG32 *pcCodeStartAddresses,
                                     [out] UINT_PTR codeStartAddresses[]);
```

## <a name="parameters"></a><span data-ttu-id="43f26-106">参数</span><span class="sxs-lookup"><span data-stu-id="43f26-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="43f26-107">\[in] 应返回其本机代码起始地址的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="43f26-107">\[in] The ID of the function whose native code start addresses should be returned.</span></span>

- `reJitId`

  <span data-ttu-id="43f26-108">\[in] JIT 重新编译的函数的标识。</span><span class="sxs-lookup"><span data-stu-id="43f26-108">\[in] The identity of the JIT-recompiled function.</span></span>

- `cCodeStartAddresses`

  <span data-ttu-id="43f26-109">\[in] 数组的最大大小 `codeStartAddresses` 。</span><span class="sxs-lookup"><span data-stu-id="43f26-109">\[in] The maximum size of the `codeStartAddresses` array.</span></span>

- `pcCodeStartAddresses`

  <span data-ttu-id="43f26-110">\[out] 可用地址的数量。</span><span class="sxs-lookup"><span data-stu-id="43f26-110">\[out] The number of available addresses.</span></span>

- `codeStartAddresses`

  <span data-ttu-id="43f26-111">\[out] 的数组 `UINT_PTR` ，其中每个都是指定函数的本机正文的开始地址。</span><span class="sxs-lookup"><span data-stu-id="43f26-111">\[out] An array of `UINT_PTR`, each one of which is the start address for a native body for the specified function.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f26-112">备注</span><span class="sxs-lookup"><span data-stu-id="43f26-112">Remarks</span></span>

<span data-ttu-id="43f26-113">启用分层编译后，函数可能有多个本机代码体。</span><span class="sxs-lookup"><span data-stu-id="43f26-113">When tiered compilation is enabled, a function may have more than one native code body.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f26-114">要求</span><span class="sxs-lookup"><span data-stu-id="43f26-114">Requirements</span></span>

<span data-ttu-id="43f26-115">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="43f26-115">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="43f26-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="43f26-116">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="43f26-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="43f26-117">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="43f26-118">**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-22-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43f26-118">**.NET Versions:** [!INCLUDE[net_core_22](../../../../includes/net-core-22-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="43f26-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="43f26-119">See also</span></span>

- [<span data-ttu-id="43f26-120">ICorProfilerInfo9 接口</span><span class="sxs-lookup"><span data-stu-id="43f26-120">ICorProfilerInfo9 Interface</span></span>](icorprofilerinfo9-interface.md)

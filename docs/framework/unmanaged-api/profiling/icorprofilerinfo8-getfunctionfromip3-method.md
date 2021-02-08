---
description: 了解详细信息： ICorProfilerInfo8：： GetFunctionFromIP3 方法
title: ICorProfilerInfo8::GetFunctionFromIP3
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo8.GetFunctionFromIP3
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 3ce0a0964e26254ab09e515826b6bceb657e07bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783828"
---
# <a name="icorprofilerinfo8getfunctionfromip3-method"></a><span data-ttu-id="18fb4-103">ICorProfilerInfo8：： GetFunctionFromIP3 方法</span><span class="sxs-lookup"><span data-stu-id="18fb4-103">ICorProfilerInfo8::GetFunctionFromIP3 Method</span></span>

<span data-ttu-id="18fb4-104">将托管代码指令指针映射到 FunctionID。</span><span class="sxs-lookup"><span data-stu-id="18fb4-104">Maps a managed code instruction pointer to a FunctionID.</span></span> <span data-ttu-id="18fb4-105">此方法适用于动态和非动态方法。</span><span class="sxs-lookup"><span data-stu-id="18fb4-105">This method works for both dynamic and non-dynamic methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="18fb4-106">语法</span><span class="sxs-lookup"><span data-stu-id="18fb4-106">Syntax</span></span>

```cpp
HRESULT GetFunctionFromIP3([in] LPCBYTE ip,
                           [out] FunctionID *functionId,
                           [out] ReJITID * pReJitId);
```

## <a name="parameters"></a><span data-ttu-id="18fb4-107">参数</span><span class="sxs-lookup"><span data-stu-id="18fb4-107">Parameters</span></span>

- `ip`

  <span data-ttu-id="18fb4-108">\[in] 托管代码中的指令指针。</span><span class="sxs-lookup"><span data-stu-id="18fb4-108">\[in] The instruction pointer in managed code.</span></span>

- `pFunctionId`

  <span data-ttu-id="18fb4-109">\[out] 函数 ID。</span><span class="sxs-lookup"><span data-stu-id="18fb4-109">\[out] The function ID.</span></span>

- `pReJitId`

  <span data-ttu-id="18fb4-110">\[out] 函数的 JIT 重新编译版本的标识。</span><span class="sxs-lookup"><span data-stu-id="18fb4-110">\[out] The identity of the JIT-recompiled version of the function.</span></span>

## <a name="remarks"></a><span data-ttu-id="18fb4-111">备注</span><span class="sxs-lookup"><span data-stu-id="18fb4-111">Remarks</span></span>

<span data-ttu-id="18fb4-112">此方法适用于动态和非动态方法。</span><span class="sxs-lookup"><span data-stu-id="18fb4-112">This method works for both dynamic and non-dynamic methods.</span></span> <span data-ttu-id="18fb4-113">它是 [GetFunctionFromIP2](icorprofilerinfo4-getfunctionfromip2-method.md)的超集，只适用于具有元数据的函数。</span><span class="sxs-lookup"><span data-stu-id="18fb4-113">It is a superset of [GetFunctionFromIP2](icorprofilerinfo4-getfunctionfromip2-method.md), which only works for functions with metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="18fb4-114">要求</span><span class="sxs-lookup"><span data-stu-id="18fb4-114">Requirements</span></span>

<span data-ttu-id="18fb4-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="18fb4-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="18fb4-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="18fb4-116">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="18fb4-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18fb4-117">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="18fb4-118">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="18fb4-118">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="18fb4-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="18fb4-119">See also</span></span>

- [<span data-ttu-id="18fb4-120">ICorProfilerInfo8 接口</span><span class="sxs-lookup"><span data-stu-id="18fb4-120">ICorProfilerInfo8 Interface</span></span>](icorprofilerinfo8-interface.md)

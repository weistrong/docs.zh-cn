---
description: 了解详细信息： ICorProfilerInfo4：： GetFunctionFromIP2 方法
title: ICorProfilerInfo4::GetFunctionFromIP2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetFunctionFromIP2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetFunctionFromIP2
helpviewer_keywords:
- ICorProfilerInfo4::GetFunctionFromIP2 method [.NET Framework profiling]
- GetFunctionFromIP2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
ms.assetid: 46ff70f4-13e9-40a0-802a-0a40abcfc6a0
topic_type:
- apiref
ms.openlocfilehash: f6abda7c9e7d4abcc0f0b256d6a7785cea205d7a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99686799"
---
# <a name="icorprofilerinfo4getfunctionfromip2-method"></a><span data-ttu-id="d6359-103">ICorProfilerInfo4::GetFunctionFromIP2 方法</span><span class="sxs-lookup"><span data-stu-id="d6359-103">ICorProfilerInfo4::GetFunctionFromIP2 Method</span></span>

<span data-ttu-id="d6359-104">将托管代码指令指针映射到函数的 JIT 重新编译版本。</span><span class="sxs-lookup"><span data-stu-id="d6359-104">Maps a managed code instruction pointer to the JIT-recompiled version of a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6359-105">语法</span><span class="sxs-lookup"><span data-stu-id="d6359-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionFromIP2(  
    [in]  LPCBYTE    ip,  
    [out] FunctionID *pFunctionId,  
    [out] ReJITID *pReJitId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d6359-106">参数</span><span class="sxs-lookup"><span data-stu-id="d6359-106">Parameters</span></span>  

 `ip`  
 <span data-ttu-id="d6359-107">中托管代码中的指令指针。</span><span class="sxs-lookup"><span data-stu-id="d6359-107">[in] The instruction pointer in managed code.</span></span>  
  
 `pFunctionId`  
 <span data-ttu-id="d6359-108">弄函数 ID。</span><span class="sxs-lookup"><span data-stu-id="d6359-108">[out] The function ID.</span></span>  
  
 `pReJitId`  
 <span data-ttu-id="d6359-109">弄函数的 JIT 重新编译版本的标识。</span><span class="sxs-lookup"><span data-stu-id="d6359-109">[out] The identity of the JIT-recompiled version of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d6359-110">备注</span><span class="sxs-lookup"><span data-stu-id="d6359-110">Remarks</span></span>  

 <span data-ttu-id="d6359-111">`GetFunctionFromIP2` 类似于 `GetFunctionFromIP` ，只不过它会获取 JIT 重新编译的 ID，而不是包含指定 IP 地址的函数的函数 ID。</span><span class="sxs-lookup"><span data-stu-id="d6359-111">`GetFunctionFromIP2` is similar to `GetFunctionFromIP`, except that it gets the JIT-recompiled ID instead of the function ID of the function that contains the specified IP address.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d6359-112">`GetFunctionFromIP2` 可以触发垃圾回收，而 `GetFunctionFromIP` 不会。</span><span class="sxs-lookup"><span data-stu-id="d6359-112">`GetFunctionFromIP2` can trigger a garbage collection, whereas `GetFunctionFromIP` will not.</span></span>  <span data-ttu-id="d6359-113">有关详细信息，请参阅 [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](corprof-e-unsupported-call-sequence-hresult.md)。</span><span class="sxs-lookup"><span data-stu-id="d6359-113">For more information, see [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](corprof-e-unsupported-call-sequence-hresult.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d6359-114">要求</span><span class="sxs-lookup"><span data-stu-id="d6359-114">Requirements</span></span>  

 <span data-ttu-id="d6359-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d6359-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6359-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d6359-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d6359-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d6359-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d6359-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6359-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6359-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6359-119">See also</span></span>

- [<span data-ttu-id="d6359-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="d6359-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)

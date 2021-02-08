---
description: 了解详细信息： ICorProfilerFunctionControl：： SetILInstrumentedCodeMap 方法
title: ICorProfilerFunctionControl::SetILInstrumentedCodeMap 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl.SetILInstrumentedCodeMap
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl::SetILInstrumentedCodeMap
helpviewer_keywords:
- ICorProfilerFunctionControl::SetILInstrumentedCodeMap method [.NET Framework profiling]
- SetIILInstrumentedCodeMap method, ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: ecf56646-7e5f-46c4-8340-f3a04e88920f
topic_type:
- apiref
ms.openlocfilehash: bb345f737459342e0146cbb0e0bd7dd4b1e9a037
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781540"
---
# <a name="icorprofilerfunctioncontrolsetilinstrumentedcodemap-method"></a><span data-ttu-id="d5b63-103">ICorProfilerFunctionControl::SetILInstrumentedCodeMap 方法</span><span class="sxs-lookup"><span data-stu-id="d5b63-103">ICorProfilerFunctionControl::SetILInstrumentedCodeMap Method</span></span>

<span data-ttu-id="d5b63-104">使用指定的公共中间语言 (CIL) 映射项为指定的函数设置代码图。</span><span class="sxs-lookup"><span data-stu-id="d5b63-104">Sets a code map for the specified function by using the specified Common Intermediate Language (CIL) map entries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5b63-105">语法</span><span class="sxs-lookup"><span data-stu-id="d5b63-105">Syntax</span></span>  
  
```cpp  
HRESULT SetILInstrumentedCodeMap(  
    [in]   ULONG      cILMapEntries,  
    [in, size_is(cILMapEntries)] COR_IL_MAP rgILMapEntries[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5b63-106">参数</span><span class="sxs-lookup"><span data-stu-id="d5b63-106">Parameters</span></span>  

 `cILMapEntries`  
 <span data-ttu-id="d5b63-107">[in] 映射中的项数。</span><span class="sxs-lookup"><span data-stu-id="d5b63-107">[in] The number of entries in the map.</span></span>  
  
 `rgILMapEntries`  
 <span data-ttu-id="d5b63-108">[in] 调用方分配的 COR_IL_MAP 项的数组。</span><span class="sxs-lookup"><span data-stu-id="d5b63-108">[in] The caller-allocated array of COR_IL_MAP  entries.</span></span> <span data-ttu-id="d5b63-109">对于 [ICorProfilerInfo：： SetILInstrumentedCodeMap](icorprofilerinfo-setilinstrumentedcodemap-method.md) 方法，这些项的解释是相同的。</span><span class="sxs-lookup"><span data-stu-id="d5b63-109">The interpretation of these entries is the same as for the [ICorProfilerInfo::SetILInstrumentedCodeMap](icorprofilerinfo-setilinstrumentedcodemap-method.md) method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d5b63-110">备注</span><span class="sxs-lookup"><span data-stu-id="d5b63-110">Remarks</span></span>  

 <span data-ttu-id="d5b63-111">通过调用此方法设置映射，使调试器可以通过调用 [ICorDebugILCode2：： GetInstrumentedILMap](../debugging/icordebugilcode2-getinstrumentedilmap-method.md)来检索映射。</span><span class="sxs-lookup"><span data-stu-id="d5b63-111">Setting the mapping by calling this method allows the debugger to retrieve the mapping by calling [ICorDebugILCode2::GetInstrumentedILMap](../debugging/icordebugilcode2-getinstrumentedilmap-method.md).</span></span> <span data-ttu-id="d5b63-112">在计算堆栈跟踪和变量生存期的 IL 偏移量时，它还允许调试器在内部使用该映射。</span><span class="sxs-lookup"><span data-stu-id="d5b63-112">It also allows the debugger to use the mapping internally when calculating IL offsets for stack traces and variable lifetimes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5b63-113">要求</span><span class="sxs-lookup"><span data-stu-id="d5b63-113">Requirements</span></span>  

 <span data-ttu-id="d5b63-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d5b63-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5b63-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d5b63-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d5b63-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d5b63-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d5b63-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5b63-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5b63-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5b63-118">See also</span></span>

- [<span data-ttu-id="d5b63-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="d5b63-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)

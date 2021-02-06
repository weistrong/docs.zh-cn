---
description: 了解详细信息： ICorProfilerInfo3：： EnumJITedFunctions 方法
title: ICorProfilerInfo3::EnumJITedFunctions 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.EnumJITedFunctions Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::EnumJITedFunctions
helpviewer_keywords:
- ICorProfilerInfo3::EnumJITedFunctions method [.NET Framework profiling]
- EnumJITedFunctions method [.NET Framework profiling]
ms.assetid: e2847a36-f460-45e2-9b6c-b33b008f40d9
topic_type:
- apiref
ms.openlocfilehash: 2f5f8358e7f01c20fc6edee60869bad01b0936c1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646928"
---
# <a name="icorprofilerinfo3enumjitedfunctions-method"></a><span data-ttu-id="fe75a-103">ICorProfilerInfo3::EnumJITedFunctions 方法</span><span class="sxs-lookup"><span data-stu-id="fe75a-103">ICorProfilerInfo3::EnumJITedFunctions Method</span></span>

<span data-ttu-id="fe75a-104">返回之前 JIT 编译的所有函数的枚举器。</span><span class="sxs-lookup"><span data-stu-id="fe75a-104">Returns an enumerator for all functions that were previously JIT-compiled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe75a-105">语法</span><span class="sxs-lookup"><span data-stu-id="fe75a-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumJITedFunctions([out] ICorProfilerFunctionEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fe75a-106">参数</span><span class="sxs-lookup"><span data-stu-id="fe75a-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="fe75a-107">弄指向 [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) 枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="fe75a-107">[out] A pointer to the [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) enumerator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe75a-108">备注</span><span class="sxs-lookup"><span data-stu-id="fe75a-108">Remarks</span></span>  

 <span data-ttu-id="fe75a-109">此方法可能与 `JITCompilation` 回调（如 [ICorProfilerCallback：： JITCompilationStarted](icorprofilercallback-jitcompilationstarted-method.md) 方法）重叠。</span><span class="sxs-lookup"><span data-stu-id="fe75a-109">This method may overlap with `JITCompilation` callbacks such as the [ICorProfilerCallback::JITCompilationStarted](icorprofilercallback-jitcompilationstarted-method.md) method.</span></span> <span data-ttu-id="fe75a-110">此方法返回的枚举器不包含从使用 Ngen.exe 生成的本机映像加载的函数。</span><span class="sxs-lookup"><span data-stu-id="fe75a-110">The enumerator returned by this method does not include functions that are loaded from native images generated with Ngen.exe.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="fe75a-111">对于字段的值，返回的枚举只包含 "0" `COR_PRF_FUNCTION::reJitId` 。</span><span class="sxs-lookup"><span data-stu-id="fe75a-111">The returned enumeration includes only "0" for the value of the `COR_PRF_FUNCTION::reJitId` field.</span></span>  <span data-ttu-id="fe75a-112">如果需要有效值 `COR_PRF_FUNCTION::reJitId` ，请使用 [ICorProfilerInfo4：： EnumJITedFunctions2](icorprofilerinfo4-enumjitedfunctions2-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fe75a-112">If you require valid `COR_PRF_FUNCTION::reJitId` values, use the [ICorProfilerInfo4::EnumJITedFunctions2](icorprofilerinfo4-enumjitedfunctions2-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe75a-113">要求</span><span class="sxs-lookup"><span data-stu-id="fe75a-113">Requirements</span></span>  

 <span data-ttu-id="fe75a-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fe75a-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe75a-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fe75a-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fe75a-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe75a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe75a-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe75a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe75a-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="fe75a-118">See also</span></span>

- [<span data-ttu-id="fe75a-119">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="fe75a-119">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="fe75a-120">分析接口</span><span class="sxs-lookup"><span data-stu-id="fe75a-120">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="fe75a-121">分析</span><span class="sxs-lookup"><span data-stu-id="fe75a-121">Profiling</span></span>](index.md)

---
description: 了解详细信息： ICorProfilerInfo：： SetFunctionIDMapper 方法
title: ICorProfilerInfo::SetFunctionIDMapper 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetFunctionIDMapper
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetFunctionIDMapper
helpviewer_keywords:
- ICorProfilerInfo::SetFunctionIDMapper method [.NET Framework profiling]
- SetFunctionIDMapper method [.NET Framework profiling]
ms.assetid: 1a6e5dae-d366-4497-9c02-7b5b1f43f9ec
topic_type:
- apiref
ms.openlocfilehash: c03c225db3b4126c3ac46ef6e5d36a5f72e529f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647198"
---
# <a name="icorprofilerinfosetfunctionidmapper-method"></a><span data-ttu-id="27f6e-103">ICorProfilerInfo::SetFunctionIDMapper 方法</span><span class="sxs-lookup"><span data-stu-id="27f6e-103">ICorProfilerInfo::SetFunctionIDMapper Method</span></span>

<span data-ttu-id="27f6e-104">指定将调用以将 `FunctionID` 值映射至替换值（传递至探查器的输入/退出挂钩）的探查器实现函数。</span><span class="sxs-lookup"><span data-stu-id="27f6e-104">Specifies the profiler-implemented function that will be called to map `FunctionID` values to alternative values, which are passed to the profiler's function entry/exit hooks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27f6e-105">语法</span><span class="sxs-lookup"><span data-stu-id="27f6e-105">Syntax</span></span>  
  
```cpp  
HRESULT SetFunctionIDMapper (  
    [in] FunctionIDMapper *pFunc);  
```  
  
## <a name="parameters"></a><span data-ttu-id="27f6e-106">参数</span><span class="sxs-lookup"><span data-stu-id="27f6e-106">Parameters</span></span>  

 `pFunc`  
 <span data-ttu-id="27f6e-107">中指向 [FunctionIDMapper](functionidmapper-function.md) 实现的指针，将调用该指针以将 `FunctionID` 值映射到其可选值。</span><span class="sxs-lookup"><span data-stu-id="27f6e-107">[in] A pointer to the [FunctionIDMapper](functionidmapper-function.md) implementation that will be called to map the `FunctionID` values to their alternative values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="27f6e-108">备注</span><span class="sxs-lookup"><span data-stu-id="27f6e-108">Remarks</span></span>  

 <span data-ttu-id="27f6e-109">值的替代 `FunctionID` 项将传递到探查器的函数入口/出口挂钩 (由[ICorProfilerInfo2：： SetEnterLeaveFunctionHooks2](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)方法指定的[FunctionEnter2](functionenter2-function.md)、 [FunctionLeave2](functionleave2-function.md)和[FunctionTailcall2](functiontailcall2-function.md)) 。</span><span class="sxs-lookup"><span data-stu-id="27f6e-109">The alternatives for the `FunctionID` values will be passed to the profiler's function entry/exit hooks ([FunctionEnter2](functionenter2-function.md), [FunctionLeave2](functionleave2-function.md), and [FunctionTailcall2](functiontailcall2-function.md)) that are specified by the [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](icorprofilerinfo2-setenterleavefunctionhooks2-method.md) method.</span></span>  
  
 <span data-ttu-id="27f6e-110">只能 `FunctionIDMapper` 设置一次，并建议你在 [ICorProfilerCallback：： Initialize](icorprofilercallback-initialize-method.md) 回调中对其进行设置。</span><span class="sxs-lookup"><span data-stu-id="27f6e-110">The `FunctionIDMapper` can be set only once and it is recommended that you set it in the [ICorProfilerCallback::Initialize](icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27f6e-111">要求</span><span class="sxs-lookup"><span data-stu-id="27f6e-111">Requirements</span></span>  

 <span data-ttu-id="27f6e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27f6e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27f6e-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="27f6e-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="27f6e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="27f6e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="27f6e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27f6e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27f6e-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="27f6e-116">See also</span></span>

- [<span data-ttu-id="27f6e-117">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="27f6e-117">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)

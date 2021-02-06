---
description: 了解详细信息： ICorProfilerInfo：： GetCurrentThreadID 方法
title: ICorProfilerInfo::GetCurrentThreadID 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetCurrentThreadID
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetCurrentThreadID
helpviewer_keywords:
- GetCurrentThreadID method, ICorProfilerInfo interface [.NET Framework profiling]
- ICorProfilerInfo::GetCurrentThreadID method [.NET Framework profiling]
ms.assetid: 39bbdb30-6a7a-4202-8da3-67ae9a0ab3a8
topic_type:
- apiref
ms.openlocfilehash: 562c6cb61f13e9ab568d18c7d179872cbc7cdb06
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647634"
---
# <a name="icorprofilerinfogetcurrentthreadid-method"></a><span data-ttu-id="d9b2e-103">ICorProfilerInfo::GetCurrentThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="d9b2e-103">ICorProfilerInfo::GetCurrentThreadID Method</span></span>

<span data-ttu-id="d9b2e-104">获取当前线程的 ID （如果它是托管线程）。</span><span class="sxs-lookup"><span data-stu-id="d9b2e-104">Gets the ID of the current thread, if it is a managed thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9b2e-105">语法</span><span class="sxs-lookup"><span data-stu-id="d9b2e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentThreadID(  
    [out] ThreadID *pThreadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9b2e-106">参数</span><span class="sxs-lookup"><span data-stu-id="d9b2e-106">Parameters</span></span>  

 `pThreadId`  
 <span data-ttu-id="d9b2e-107">弄指向托管线程的返回 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="d9b2e-107">[out] A pointer to the returned ID of the managed thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9b2e-108">备注</span><span class="sxs-lookup"><span data-stu-id="d9b2e-108">Remarks</span></span>  

 <span data-ttu-id="d9b2e-109">如果当前线程是内部运行时线程或其他非托管线程，则 `GetCurrentThreadID` 返回 CORPROF_E_NOT_MANAGED_THREAD 作为 HRESULT，并且参数的返回值 `pThreadId` 将为 null。</span><span class="sxs-lookup"><span data-stu-id="d9b2e-109">If the current thread is an internal runtime thread or other unmanaged thread, `GetCurrentThreadID` returns CORPROF_E_NOT_MANAGED_THREAD as the HRESULT, and the returned value of the `pThreadId` parameter will be null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9b2e-110">要求</span><span class="sxs-lookup"><span data-stu-id="d9b2e-110">Requirements</span></span>  

 <span data-ttu-id="d9b2e-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9b2e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9b2e-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d9b2e-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d9b2e-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d9b2e-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d9b2e-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9b2e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9b2e-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d9b2e-115">See also</span></span>

- [<span data-ttu-id="d9b2e-116">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="d9b2e-116">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)

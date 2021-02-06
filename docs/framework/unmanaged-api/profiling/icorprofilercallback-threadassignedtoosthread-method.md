---
description: 了解详细信息： ICorProfilerCallback：： ThreadAssignedToOSThread 方法
title: ICorProfilerCallback::ThreadAssignedToOSThread 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadAssignedToOSThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadAssignedToOSThread
helpviewer_keywords:
- ThreadAssignedToOSThread method [.NET Framework profiling]
- ICorProfilerCallback::ThreadAssignedToOSThread method [.NET Framework profiling]
ms.assetid: f9671e5a-7b14-4f5b-8404-58136422c8b2
topic_type:
- apiref
ms.openlocfilehash: 04fba4cabb0ac58b3afeaae1fd579865335a9e14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647981"
---
# <a name="icorprofilercallbackthreadassignedtoosthread-method"></a><span data-ttu-id="15556-103">ICorProfilerCallback::ThreadAssignedToOSThread 方法</span><span class="sxs-lookup"><span data-stu-id="15556-103">ICorProfilerCallback::ThreadAssignedToOSThread Method</span></span>

<span data-ttu-id="15556-104">通知探查器使用特定操作系统线程实现了托管线程。</span><span class="sxs-lookup"><span data-stu-id="15556-104">Notifies the profiler that a managed thread is being implemented using a particular operating system thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15556-105">语法</span><span class="sxs-lookup"><span data-stu-id="15556-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadAssignedToOSThread(  
    [in] ThreadID managedThreadId,  
    [in] DWORD    osThreadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="15556-106">参数</span><span class="sxs-lookup"><span data-stu-id="15556-106">Parameters</span></span>  

 `managedThreadId`  
 <span data-ttu-id="15556-107">中托管线程的标识符。</span><span class="sxs-lookup"><span data-stu-id="15556-107">[in] The identifier of the managed thread.</span></span>  
  
 `osThreadId`  
 <span data-ttu-id="15556-108">中操作系统线程的标识符。</span><span class="sxs-lookup"><span data-stu-id="15556-108">[in] The identifier of the operating system thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="15556-109">备注</span><span class="sxs-lookup"><span data-stu-id="15556-109">Remarks</span></span>  

 <span data-ttu-id="15556-110">`ThreadAssignedToOSThread`回调存在，以便探查器能够在操作系统线程的纤程之间保持准确映射到托管线程。</span><span class="sxs-lookup"><span data-stu-id="15556-110">The `ThreadAssignedToOSThread` callback exists so that the profiler can maintain an accurate mapping across fibers of operating system threads to managed threads.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15556-111">要求</span><span class="sxs-lookup"><span data-stu-id="15556-111">Requirements</span></span>  

 <span data-ttu-id="15556-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="15556-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15556-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="15556-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="15556-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="15556-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="15556-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15556-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15556-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="15556-116">See also</span></span>

- [<span data-ttu-id="15556-117">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="15556-117">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)

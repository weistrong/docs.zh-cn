---
description: 了解详细信息： ICorProfilerInfo：： GetHandleFromThread 方法
title: ICorProfilerInfo::GetHandleFromThread 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetHandleFromThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetHandleFromThread
helpviewer_keywords:
- GetHandleFromThread method [.NET Framework profiling]
- ICorProfilerInfo::GetHandleFromThread method [.NET Framework profiling]
ms.assetid: 36cdc9f5-7579-4cd2-aa36-fc05c741584c
topic_type:
- apiref
ms.openlocfilehash: 541a2872bc3cbbe8233e09283b9773957b0a7daf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647516"
---
# <a name="icorprofilerinfogethandlefromthread-method"></a><span data-ttu-id="5f690-103">ICorProfilerInfo::GetHandleFromThread 方法</span><span class="sxs-lookup"><span data-stu-id="5f690-103">ICorProfilerInfo::GetHandleFromThread Method</span></span>

<span data-ttu-id="5f690-104">将线程的 ID 映射到 Win32 线程句柄。</span><span class="sxs-lookup"><span data-stu-id="5f690-104">Maps the ID of a thread to a Win32 thread handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f690-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f690-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHandleFromThread(  
    [in]  ThreadID threadId,  
    [out] HANDLE  *phThread);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f690-106">参数</span><span class="sxs-lookup"><span data-stu-id="5f690-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="5f690-107">中要映射的线程 ID。</span><span class="sxs-lookup"><span data-stu-id="5f690-107">[in] The thread ID to be mapped.</span></span>  
  
 `phThread`  
 <span data-ttu-id="5f690-108">弄指向 Win32 线程句柄的指针。</span><span class="sxs-lookup"><span data-stu-id="5f690-108">[out] A pointer to a Win32 thread handle.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5f690-109">备注</span><span class="sxs-lookup"><span data-stu-id="5f690-109">Remarks</span></span>  

 <span data-ttu-id="5f690-110">探查器必须 `DuplicateHandle` 先对句柄调用 Win32 函数，然后才能使用该句柄。</span><span class="sxs-lookup"><span data-stu-id="5f690-110">The profiler must call the Win32 `DuplicateHandle` function on the handle before using it.</span></span>  

 <span data-ttu-id="5f690-111">此方法返回的句柄由运行时所拥有，并且探查器不应将其关闭。</span><span class="sxs-lookup"><span data-stu-id="5f690-111">The handle returned from this method is owned by the runtime and the profiler should never close it.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="5f690-112">要求</span><span class="sxs-lookup"><span data-stu-id="5f690-112">Requirements</span></span>  

 <span data-ttu-id="5f690-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f690-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f690-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5f690-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5f690-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5f690-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5f690-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f690-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f690-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f690-117">See also</span></span>

- [<span data-ttu-id="5f690-118">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="5f690-118">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)

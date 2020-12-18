---
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
ms.openlocfilehash: 94c2c6e01e4188f1fa13c3b6a9f638d4b79a502f
ms.sourcegitcommit: 4b79862c5b41fbd86cf38f926f6a49516059f6f2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2020
ms.locfileid: "97678194"
---
# <a name="icorprofilerinfogethandlefromthread-method"></a><span data-ttu-id="5e6b9-102">ICorProfilerInfo::GetHandleFromThread 方法</span><span class="sxs-lookup"><span data-stu-id="5e6b9-102">ICorProfilerInfo::GetHandleFromThread Method</span></span>

<span data-ttu-id="5e6b9-103">将线程的 ID 映射到 Win32 线程句柄。</span><span class="sxs-lookup"><span data-stu-id="5e6b9-103">Maps the ID of a thread to a Win32 thread handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e6b9-104">语法</span><span class="sxs-lookup"><span data-stu-id="5e6b9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetHandleFromThread(  
    [in]  ThreadID threadId,  
    [out] HANDLE  *phThread);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5e6b9-105">参数</span><span class="sxs-lookup"><span data-stu-id="5e6b9-105">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="5e6b9-106">中要映射的线程 ID。</span><span class="sxs-lookup"><span data-stu-id="5e6b9-106">[in] The thread ID to be mapped.</span></span>  
  
 `phThread`  
 <span data-ttu-id="5e6b9-107">弄指向 Win32 线程句柄的指针。</span><span class="sxs-lookup"><span data-stu-id="5e6b9-107">[out] A pointer to a Win32 thread handle.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5e6b9-108">备注</span><span class="sxs-lookup"><span data-stu-id="5e6b9-108">Remarks</span></span>  

 <span data-ttu-id="5e6b9-109">探查器必须 `DuplicateHandle` 先对句柄调用 Win32 函数，然后才能使用该句柄。</span><span class="sxs-lookup"><span data-stu-id="5e6b9-109">The profiler must call the Win32 `DuplicateHandle` function on the handle before using it.</span></span>  

 <span data-ttu-id="5e6b9-110">此方法返回的句柄由运行时所拥有，并且探查器不应将其关闭。</span><span class="sxs-lookup"><span data-stu-id="5e6b9-110">The handle returned from this method is owned by the runtime and the profiler should never close it.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="5e6b9-111">要求</span><span class="sxs-lookup"><span data-stu-id="5e6b9-111">Requirements</span></span>  

 <span data-ttu-id="5e6b9-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5e6b9-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e6b9-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5e6b9-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5e6b9-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5e6b9-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5e6b9-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e6b9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e6b9-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5e6b9-116">See also</span></span>

- [<span data-ttu-id="5e6b9-117">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="5e6b9-117">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)

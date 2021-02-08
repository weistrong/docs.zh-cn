---
description: 了解详细信息： ICorProfilerCallback3：:P rofilerDetachSucceeded 方法
title: ICorProfilerCallback3::ProfilerDetachSucceeded 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3.ProfilerDetachSucceeded Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3::ProfilerDetachSucceeded
helpviewer_keywords:
- ProfilerDetachSucceeded method [.NET Framework profiling]
- ICorProfilerCallback3::ProfilerDetachSucceeded method [.NET Framework profiling]
ms.assetid: 05164966-16ce-4cc9-a530-43a640c00711
topic_type:
- apiref
ms.openlocfilehash: bc80b5bd5301bb5b0278534cfba6ac23e5968620
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788769"
---
# <a name="icorprofilercallback3profilerdetachsucceeded-method"></a><span data-ttu-id="db83e-103">ICorProfilerCallback3::ProfilerDetachSucceeded 方法</span><span class="sxs-lookup"><span data-stu-id="db83e-103">ICorProfilerCallback3::ProfilerDetachSucceeded Method</span></span>

<span data-ttu-id="db83e-104">通知探查器公共语言运行时 (CLR) 将要卸载探查器 DLL。</span><span class="sxs-lookup"><span data-stu-id="db83e-104">Notifies the profiler that the common language runtime (CLR) is about to unload the profiler DLL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db83e-105">语法</span><span class="sxs-lookup"><span data-stu-id="db83e-105">Syntax</span></span>  
  
```cpp  
HRESULT ProfilerDetachSucceeded();  
```  
  
## <a name="return-value"></a><span data-ttu-id="db83e-106">返回值</span><span class="sxs-lookup"><span data-stu-id="db83e-106">Return Value</span></span>  

 <span data-ttu-id="db83e-107">将忽略来自此回调的返回值。</span><span class="sxs-lookup"><span data-stu-id="db83e-107">The return value from this callback is ignored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db83e-108">备注</span><span class="sxs-lookup"><span data-stu-id="db83e-108">Remarks</span></span>  

 <span data-ttu-id="db83e-109">在所有线程均退出探查器的代码之后，发出`ProfilerDetachSucceeded` 回调。</span><span class="sxs-lookup"><span data-stu-id="db83e-109">The `ProfilerDetachSucceeded` callback is issued after all threads have exited the profiler's code.</span></span> <span data-ttu-id="db83e-110">当调用此方法时，探查器应执行任何不适合用于其析构函数的的最后执行的任务，例如通知其 UI 或日志记录组件。</span><span class="sxs-lookup"><span data-stu-id="db83e-110">When this method is called, the profiler should perform any last-minute tasks that are not appropriate for its destructor, such as notifying its UI or logging component.</span></span> <span data-ttu-id="db83e-111">但是，探查器不能在此 (回调期间（如 [ICorProfilerInfo](icorprofilerinfo-interface.md) 或接口) ）调用 CLR 提供的接口上的函数 `IMetaData*` 。</span><span class="sxs-lookup"><span data-stu-id="db83e-111">However, the profiler must not call functions on interfaces that are provided by the CLR during this callback (such as the [ICorProfilerInfo](icorprofilerinfo-interface.md) or `IMetaData*` interfaces).</span></span>  
  
 <span data-ttu-id="db83e-112">CLR 在 Windows 应用程序事件日志中创建条目，用于表示分离操作成功。</span><span class="sxs-lookup"><span data-stu-id="db83e-112">The CLR creates an entry in the Windows Application event log to indicate that the detach operation is successful.</span></span>  
  
 <span data-ttu-id="db83e-113">探查器从此回调返回后，CLR 将释放探查器对象并卸载探查器 DLL。</span><span class="sxs-lookup"><span data-stu-id="db83e-113">After the profiler returns from this callback, the CLR releases the profiler object and unloads the profiler DLL.</span></span> <span data-ttu-id="db83e-114">因此，探查器不可执行任何会导致探查器 DLL 从此回调返回后其内部进行执行的操作。</span><span class="sxs-lookup"><span data-stu-id="db83e-114">Therefore, the profiler must not perform any actions that would cause execution to occur inside the profiler DLL after it returns from this callback.</span></span> <span data-ttu-id="db83e-115">例如，它不能创建线程或注册计时器回调。</span><span class="sxs-lookup"><span data-stu-id="db83e-115">For example, it must not create threads or register timer callbacks.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db83e-116">要求</span><span class="sxs-lookup"><span data-stu-id="db83e-116">Requirements</span></span>  

 <span data-ttu-id="db83e-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db83e-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db83e-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="db83e-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="db83e-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db83e-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db83e-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db83e-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db83e-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="db83e-121">See also</span></span>

- [<span data-ttu-id="db83e-122">元数据接口</span><span class="sxs-lookup"><span data-stu-id="db83e-122">Metadata Interfaces</span></span>](../metadata/metadata-interfaces.md)
- [<span data-ttu-id="db83e-123">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="db83e-123">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="db83e-124">分析接口</span><span class="sxs-lookup"><span data-stu-id="db83e-124">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="db83e-125">分析</span><span class="sxs-lookup"><span data-stu-id="db83e-125">Profiling</span></span>](index.md)

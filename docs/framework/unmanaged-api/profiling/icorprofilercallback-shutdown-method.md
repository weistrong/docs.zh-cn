---
description: 了解详细信息： ICorProfilerCallback：： Shutdown 方法
title: ICorProfilerCallback::Shutdown 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.Shutdown
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::Shutdown
helpviewer_keywords:
- ICorProfilerCallback::Shutdown method [.NET Framework profiling]
- Shutdown method [.NET Framework profiling]
ms.assetid: 1ea194f0-a331-4855-a2ce-37393b8e5f84
topic_type:
- apiref
ms.openlocfilehash: 7afc274579f248ee190e379160f2709b5cb9881a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657289"
---
# <a name="icorprofilercallbackshutdown-method"></a><span data-ttu-id="7b5f4-103">ICorProfilerCallback::Shutdown 方法</span><span class="sxs-lookup"><span data-stu-id="7b5f4-103">ICorProfilerCallback::Shutdown Method</span></span>

<span data-ttu-id="7b5f4-104">通知探查器应用程序正在关闭。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-104">Notifies the profiler that the application is shutting down.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b5f4-105">语法</span><span class="sxs-lookup"><span data-stu-id="7b5f4-105">Syntax</span></span>  
  
```cpp  
HRESULT Shutdown();  
```  
  
## <a name="remarks"></a><span data-ttu-id="7b5f4-106">备注</span><span class="sxs-lookup"><span data-stu-id="7b5f4-106">Remarks</span></span>  

 <span data-ttu-id="7b5f4-107">调用方法后，探查器代码无法安全调用 [ICorProfilerInfo](icorprofilerinfo-interface.md) 接口的方法 `Shutdown` 。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-107">The profiler code cannot safely call methods of the [ICorProfilerInfo](icorprofilerinfo-interface.md) interface after the `Shutdown` method is called.</span></span> <span data-ttu-id="7b5f4-108">对方法的任何调用都会 `ICorProfilerInfo` 导致在方法返回后出现未定义的行为 `Shutdown` 。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-108">Any calls to `ICorProfilerInfo` methods result in undefined behavior after the `Shutdown` method returns.</span></span> <span data-ttu-id="7b5f4-109">某些不可变事件可能仍会在关闭后发生;此事件发生时，探查器应小心立即返回。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-109">Certain immutable events may still occur after shutdown; the profiler should take care to return immediately when this occurs.</span></span>  
  
 <span data-ttu-id="7b5f4-110">`Shutdown`仅当要分析的托管应用程序作为托管代码启动时，才会调用此方法 (也就是说，处理堆栈上的初始帧是) 管理的。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-110">The `Shutdown` method will be called only if the managed application that is being profiled started as managed code (that is, the initial frame on the process stack is managed).</span></span> <span data-ttu-id="7b5f4-111">如果应用程序启动为非托管代码，但后来跳转到托管代码，则 (CLR) 创建公共语言运行时的实例，则 `Shutdown` 不会调用。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-111">If the application started as unmanaged code but later jumped into managed code, thereby creating an instance of the common language runtime (CLR), then `Shutdown` will not be called.</span></span> <span data-ttu-id="7b5f4-112">对于这些情况，探查器应在其库中包含一个 `DllMain` 例程，该例程使用 DLL_PROCESS_DETACH 值来释放所有资源并对其数据执行清理处理，如将跟踪刷新到磁盘等。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-112">For these cases, the profiler should include in its library a `DllMain` routine that uses the DLL_PROCESS_DETACH value to free any resources and perform clean-up processing of its data, such as flushing traces to disk and so on.</span></span>  
  
 <span data-ttu-id="7b5f4-113">通常，探查器必须处理意外关闭。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-113">In general, the profiler must cope with unexpected shutdowns.</span></span> <span data-ttu-id="7b5f4-114">例如，进程可能由 `TerminateProcess` 在 winbase.h) 中声明 (win32 方法中止。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-114">For example, a process might be halted by Win32's `TerminateProcess` method (declared in Winbase.h).</span></span> <span data-ttu-id="7b5f4-115">在其他情况下，CLR 将暂停特定的托管线程 (后台线程) 而不为它们传递有序的析构消息。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-115">In other cases, the CLR will halt certain managed threads (background threads) without delivering orderly destruction messages for them.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b5f4-116">要求</span><span class="sxs-lookup"><span data-stu-id="7b5f4-116">Requirements</span></span>  

 <span data-ttu-id="7b5f4-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7b5f4-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b5f4-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7b5f4-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7b5f4-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7b5f4-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7b5f4-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b5f4-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b5f4-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="7b5f4-121">See also</span></span>

- [<span data-ttu-id="7b5f4-122">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7b5f4-122">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="7b5f4-123">Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="7b5f4-123">Initialize Method</span></span>](icorprofilercallback-initialize-method.md)

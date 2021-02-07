---
description: 了解详细信息： ICorDebugProcess2 接口
title: ICorDebugProcess2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2
helpviewer_keywords:
- ICorDebugProcess2 interface [.NET Framework debugging]
ms.assetid: 73332138-5fea-441f-b893-61af87d45a42
topic_type:
- apiref
ms.openlocfilehash: 47e94ee8ee4f45e365fa9efe888cb706f8bb1dfd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746589"
---
# <a name="icordebugprocess2-interface"></a><span data-ttu-id="3f665-103">ICorDebugProcess2 接口</span><span class="sxs-lookup"><span data-stu-id="3f665-103">ICorDebugProcess2 Interface</span></span>

<span data-ttu-id="3f665-104">ICorDebugProcess 接口的逻辑扩展，它表示运行托管代码的进程。</span><span class="sxs-lookup"><span data-stu-id="3f665-104">A logical extension of the ICorDebugProcess interface, which represents a process running managed code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3f665-105">方法</span><span class="sxs-lookup"><span data-stu-id="3f665-105">Methods</span></span>  
  
|<span data-ttu-id="3f665-106">方法</span><span class="sxs-lookup"><span data-stu-id="3f665-106">Method</span></span>|<span data-ttu-id="3f665-107">说明</span><span class="sxs-lookup"><span data-stu-id="3f665-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3f665-108">ClearUnmanagedBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-108">ClearUnmanagedBreakpoint Method</span></span>](icordebugprocess2-clearunmanagedbreakpoint-method.md)|<span data-ttu-id="3f665-109">删除由之前对的调用所设置的指定偏移量处的断点 `ICorDebugProcess2::SetUnmanagedBreakpoint` 。</span><span class="sxs-lookup"><span data-stu-id="3f665-109">Removes a breakpoint at the specified offset that was set by an earlier call to `ICorDebugProcess2::SetUnmanagedBreakpoint`.</span></span>|  
|[<span data-ttu-id="3f665-110">GetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-110">GetDesiredNGENCompilerFlags Method</span></span>](icordebugprocess2-getdesiredngencompilerflags-method.md)|<span data-ttu-id="3f665-111">获取必须设置为公共语言运行时 (CLR) 的标志，以将图像加载到由此引用的进程中 `ICorDebugProcess2` 。</span><span class="sxs-lookup"><span data-stu-id="3f665-111">Gets the flags that must be set for the common language runtime (CLR) to load the image into the process referenced by this `ICorDebugProcess2`.</span></span>|  
|[<span data-ttu-id="3f665-112">GetReferenceValueFromGCHandle 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-112">GetReferenceValueFromGCHandle Method</span></span>](icordebugprocess2-getreferencevaluefromgchandle-method.md)|<span data-ttu-id="3f665-113">获取指向具有垃圾回收句柄的指定托管对象的引用指针。</span><span class="sxs-lookup"><span data-stu-id="3f665-113">Gets a reference pointer to the specified managed object that has a garbage collection handle.</span></span>|  
|[<span data-ttu-id="3f665-114">GetThreadForTaskID 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-114">GetThreadForTaskID Method</span></span>](icordebugprocess2-getthreadfortaskid-method.md)|<span data-ttu-id="3f665-115">获取执行具有指定标识符的任务的线程。</span><span class="sxs-lookup"><span data-stu-id="3f665-115">Gets the thread upon which the task with the specified identifier is executing.</span></span>|  
|[<span data-ttu-id="3f665-116">GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-116">GetVersion Method</span></span>](icordebugprocess2-getversion-method.md)|<span data-ttu-id="3f665-117">获取正在运行正在调试的进程的 CLR 的版本。</span><span class="sxs-lookup"><span data-stu-id="3f665-117">Gets the version of the CLR upon which the process being debugged is running.</span></span>|  
|[<span data-ttu-id="3f665-118">SetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-118">SetDesiredNGENCompilerFlags Method</span></span>](icordebugprocess2-setdesiredngencompilerflags-method.md)|<span data-ttu-id="3f665-119">设置实时 (JIT) 编译器所需的标志，以将图像加载到正在调试的进程中。</span><span class="sxs-lookup"><span data-stu-id="3f665-119">Sets the flags that are required for the just-in-time (JIT) compiler to load an image into the process being debugged.</span></span>|  
|[<span data-ttu-id="3f665-120">SetUnmanagedBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="3f665-120">SetUnmanagedBreakpoint Method</span></span>](icordebugprocess2-setunmanagedbreakpoint-method.md)|<span data-ttu-id="3f665-121">在指定的本机映像偏移量处设置非托管断点。</span><span class="sxs-lookup"><span data-stu-id="3f665-121">Sets an unmanaged breakpoint at the specified native image offset.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3f665-122">备注</span><span class="sxs-lookup"><span data-stu-id="3f665-122">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3f665-123">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3f665-123">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f665-124">要求</span><span class="sxs-lookup"><span data-stu-id="3f665-124">Requirements</span></span>  

 <span data-ttu-id="3f665-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f665-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f665-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3f665-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3f665-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3f665-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3f665-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f665-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f665-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f665-129">See also</span></span>

- [<span data-ttu-id="3f665-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="3f665-130">Debugging Interfaces</span></span>](debugging-interfaces.md)

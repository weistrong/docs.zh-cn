---
description: 了解详细信息： ICorDebugChain 接口
title: ICorDebugChain 接口
ms.date: 03/30/2017
api_name:
- ICorDebugChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain
helpviewer_keywords:
- ICorDebugChain interface [.NET Framework debugging]
ms.assetid: f671f519-1cb3-4ae5-b9f1-abc5e783459f
topic_type:
- apiref
ms.openlocfilehash: 391c9a3e54d06d303728da5ab7f105bc8e2558ef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661189"
---
# <a name="icordebugchain-interface"></a><span data-ttu-id="15ef2-103">ICorDebugChain 接口</span><span class="sxs-lookup"><span data-stu-id="15ef2-103">ICorDebugChain Interface</span></span>

<span data-ttu-id="15ef2-104">表示一个物理或逻辑调用堆栈段。</span><span class="sxs-lookup"><span data-stu-id="15ef2-104">Represents a segment of a physical or logical call stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="15ef2-105">方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-105">Methods</span></span>  
  
|<span data-ttu-id="15ef2-106">方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-106">Method</span></span>|<span data-ttu-id="15ef2-107">说明</span><span class="sxs-lookup"><span data-stu-id="15ef2-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="15ef2-108">EnumerateFrames 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-108">EnumerateFrames Method</span></span>](icordebugchain-enumerateframes-method.md)|<span data-ttu-id="15ef2-109">获取一个枚举数，该枚举数包含链中所有托管堆栈帧（从最新帧开始）。</span><span class="sxs-lookup"><span data-stu-id="15ef2-109">Gets an enumerator that contains all the managed stack frames in the chain, starting with the most recent frame.</span></span>|  
|[<span data-ttu-id="15ef2-110">GetActiveFrame 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-110">GetActiveFrame Method</span></span>](icordebugchain-getactiveframe-method.md)|<span data-ttu-id="15ef2-111">获取当前链上的活动 (，即最近) 的帧。</span><span class="sxs-lookup"><span data-stu-id="15ef2-111">Gets the active (that is, most recent) frame on the chain.</span></span>|  
|[<span data-ttu-id="15ef2-112">GetCallee 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-112">GetCallee Method</span></span>](icordebugchain-getcallee-method.md)|<span data-ttu-id="15ef2-113">获取此链调用的链。</span><span class="sxs-lookup"><span data-stu-id="15ef2-113">Gets the chain that was called by this chain.</span></span>|  
|[<span data-ttu-id="15ef2-114">GetCaller 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-114">GetCaller Method</span></span>](icordebugchain-getcaller-method.md)|<span data-ttu-id="15ef2-115">获取调用此链的链。</span><span class="sxs-lookup"><span data-stu-id="15ef2-115">Gets the chain that called this chain.</span></span>|  
|[<span data-ttu-id="15ef2-116">GetContext 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-116">GetContext Method</span></span>](icordebugchain-getcontext-method.md)|<span data-ttu-id="15ef2-117">未实现。</span><span class="sxs-lookup"><span data-stu-id="15ef2-117">Not implemented.</span></span>|  
|[<span data-ttu-id="15ef2-118">GetNext 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-118">GetNext Method</span></span>](icordebugchain-getnext-method.md)|<span data-ttu-id="15ef2-119">获取线程的下一个帧链。</span><span class="sxs-lookup"><span data-stu-id="15ef2-119">Gets the next chain of frames for the thread.</span></span>|  
|[<span data-ttu-id="15ef2-120">GetPrevious 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-120">GetPrevious Method</span></span>](icordebugchain-getprevious-method.md)|<span data-ttu-id="15ef2-121">获取线程的上一个帧链。</span><span class="sxs-lookup"><span data-stu-id="15ef2-121">Gets the previous chain of frames for the thread.</span></span>|  
|[<span data-ttu-id="15ef2-122">GetReason 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-122">GetReason Method</span></span>](icordebugchain-getreason-method.md)|<span data-ttu-id="15ef2-123">获取此调用链的 genesis 的原因。</span><span class="sxs-lookup"><span data-stu-id="15ef2-123">Gets the reason for the genesis of this calling chain.</span></span>|  
|[<span data-ttu-id="15ef2-124">GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-124">GetRegisterSet Method</span></span>](icordebugchain-getregisterset-method.md)|<span data-ttu-id="15ef2-125">获取此链的活动部分的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="15ef2-125">Gets the register set for the active part of this chain.</span></span>|  
|[<span data-ttu-id="15ef2-126">GetStackRange 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-126">GetStackRange Method</span></span>](icordebugchain-getstackrange-method.md)|<span data-ttu-id="15ef2-127">获取此链的堆栈段的地址范围。</span><span class="sxs-lookup"><span data-stu-id="15ef2-127">Gets the address range of the stack segment for this chain.</span></span>|  
|[<span data-ttu-id="15ef2-128">GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-128">GetThread Method</span></span>](icordebugchain-getthread-method.md)|<span data-ttu-id="15ef2-129">获取此调用链所属的物理线程。</span><span class="sxs-lookup"><span data-stu-id="15ef2-129">Gets the physical thread this call chain is part of.</span></span>|  
|[<span data-ttu-id="15ef2-130">IsManaged 方法</span><span class="sxs-lookup"><span data-stu-id="15ef2-130">IsManaged Method</span></span>](icordebugchain-ismanaged-method.md)|<span data-ttu-id="15ef2-131">获取一个值，该值指示此链是否正在运行托管代码。</span><span class="sxs-lookup"><span data-stu-id="15ef2-131">Gets a value that indicates whether this chain is running managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15ef2-132">备注</span><span class="sxs-lookup"><span data-stu-id="15ef2-132">Remarks</span></span>  

 <span data-ttu-id="15ef2-133">链中的堆栈帧占用连续堆栈空间并共享相同的线程和上下文。</span><span class="sxs-lookup"><span data-stu-id="15ef2-133">The stack frames in a chain occupy contiguous stack space and share the same thread and context.</span></span> <span data-ttu-id="15ef2-134">链可以表示托管或非托管代码链。</span><span class="sxs-lookup"><span data-stu-id="15ef2-134">A chain may represent either managed or unmanaged code chains.</span></span> <span data-ttu-id="15ef2-135">空 `ICorDebugChain` 实例表示非托管代码链。</span><span class="sxs-lookup"><span data-stu-id="15ef2-135">An empty `ICorDebugChain` instance represents an unmanaged code chain.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="15ef2-136">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="15ef2-136">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15ef2-137">要求</span><span class="sxs-lookup"><span data-stu-id="15ef2-137">Requirements</span></span>  

 <span data-ttu-id="15ef2-138">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="15ef2-138">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15ef2-139">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="15ef2-139">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="15ef2-140">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="15ef2-140">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="15ef2-141">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15ef2-141">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15ef2-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="15ef2-142">See also</span></span>

- [<span data-ttu-id="15ef2-143">调试接口</span><span class="sxs-lookup"><span data-stu-id="15ef2-143">Debugging Interfaces</span></span>](debugging-interfaces.md)

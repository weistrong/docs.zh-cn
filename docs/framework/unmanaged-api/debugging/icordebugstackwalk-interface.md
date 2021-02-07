---
description: 了解详细信息： ICorDebugStackWalk 接口
title: ICorDebugStackWalk 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk
helpviewer_keywords:
- ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 16d695e8-975d-431b-8421-e9e6c3e3f476
topic_type:
- apiref
ms.openlocfilehash: 27dcdfc90829a3a28d81ad28dce0cd4d1d674948
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738086"
---
# <a name="icordebugstackwalk-interface"></a><span data-ttu-id="7ca9e-103">ICorDebugStackWalk 接口</span><span class="sxs-lookup"><span data-stu-id="7ca9e-103">ICorDebugStackWalk Interface</span></span>

<span data-ttu-id="7ca9e-104">提供用于获取线程堆栈上的托管方法或帧的方法。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-104">Provides methods for getting the managed methods, or frames, on a thread’s stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7ca9e-105">方法</span><span class="sxs-lookup"><span data-stu-id="7ca9e-105">Methods</span></span>  
  
|<span data-ttu-id="7ca9e-106">方法</span><span class="sxs-lookup"><span data-stu-id="7ca9e-106">Method</span></span>|<span data-ttu-id="7ca9e-107">说明</span><span class="sxs-lookup"><span data-stu-id="7ca9e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7ca9e-108">GetContext 方法</span><span class="sxs-lookup"><span data-stu-id="7ca9e-108">GetContext Method</span></span>](icordebugstackwalk-getcontext-method.md)|<span data-ttu-id="7ca9e-109">返回对象中当前帧的上下文 `ICorDebugStackWalk` 。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-109">Returns the context for the current frame in the `ICorDebugStackWalk` object.</span></span>|  
|[<span data-ttu-id="7ca9e-110">SetContext 方法</span><span class="sxs-lookup"><span data-stu-id="7ca9e-110">SetContext Method</span></span>](icordebugstackwalk-setcontext-method.md)|<span data-ttu-id="7ca9e-111">将 `ICorDebugStackWalk` 对象的当前上下文设置为线程的有效上下文。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-111">Sets the `ICorDebugStackWalk` object’s current context to a valid context for the thread.</span></span>|  
|[<span data-ttu-id="7ca9e-112">下一方法</span><span class="sxs-lookup"><span data-stu-id="7ca9e-112">Next Method</span></span>](icordebugstackwalk-next-method.md)|<span data-ttu-id="7ca9e-113">将 `ICorDebugStackWalk` 对象移动到下一帧。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-113">Moves the `ICorDebugStackWalk` object to the next frame.</span></span>|  
|[<span data-ttu-id="7ca9e-114">GetFrame 方法</span><span class="sxs-lookup"><span data-stu-id="7ca9e-114">GetFrame Method</span></span>](icordebugstackwalk-getframe-method.md)|<span data-ttu-id="7ca9e-115">获取对象中的当前帧 `ICorDebugStackWalk` 。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-115">Gets the current frame in the `ICorDebugStackWalk` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7ca9e-116">备注</span><span class="sxs-lookup"><span data-stu-id="7ca9e-116">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7ca9e-117">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-117">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7ca9e-118">要求</span><span class="sxs-lookup"><span data-stu-id="7ca9e-118">Requirements</span></span>  

 <span data-ttu-id="7ca9e-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7ca9e-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7ca9e-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7ca9e-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7ca9e-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7ca9e-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7ca9e-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7ca9e-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ca9e-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="7ca9e-123">See also</span></span>

- [<span data-ttu-id="7ca9e-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="7ca9e-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="7ca9e-125">调试</span><span class="sxs-lookup"><span data-stu-id="7ca9e-125">Debugging</span></span>](index.md)

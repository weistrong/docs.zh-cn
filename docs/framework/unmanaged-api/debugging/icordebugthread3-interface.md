---
description: 了解详细信息： ICorDebugThread3 接口
title: ICorDebugThread3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThread3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread3
helpviewer_keywords:
- ICorDebugThread3 interface [.NET Framework debugging]
ms.assetid: eb2860ef-06cb-4968-a6c3-6d048ecda2a4
topic_type:
- apiref
ms.openlocfilehash: 88c668f1e08d0843f26d231937c85d80e03bee6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800963"
---
# <a name="icordebugthread3-interface"></a><span data-ttu-id="0ff4d-103">ICorDebugThread3 接口</span><span class="sxs-lookup"><span data-stu-id="0ff4d-103">ICorDebugThread3 Interface</span></span>

<span data-ttu-id="0ff4d-104">提供 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 和相应接口的入口点。</span><span class="sxs-lookup"><span data-stu-id="0ff4d-104">Provides the entry point to the [ICorDebugStackWalk](icordebugstackwalk-interface.md) and corresponding interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0ff4d-105">方法</span><span class="sxs-lookup"><span data-stu-id="0ff4d-105">Methods</span></span>  
  
|<span data-ttu-id="0ff4d-106">方法</span><span class="sxs-lookup"><span data-stu-id="0ff4d-106">Method</span></span>|<span data-ttu-id="0ff4d-107">说明</span><span class="sxs-lookup"><span data-stu-id="0ff4d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0ff4d-108">CreateStackWalk 方法</span><span class="sxs-lookup"><span data-stu-id="0ff4d-108">CreateStackWalk Method</span></span>](icordebugthread3-createstackwalk-method.md)|<span data-ttu-id="0ff4d-109">为要展开其堆栈的线程创建 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="0ff4d-109">Creates an [ICorDebugStackWalk](icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>|  
|[<span data-ttu-id="0ff4d-110">GetActiveInternalFrames 方法</span><span class="sxs-lookup"><span data-stu-id="0ff4d-110">GetActiveInternalFrames Method</span></span>](icordebugthread3-getactiveinternalframes-method.md)|<span data-ttu-id="0ff4d-111">返回堆栈 ([ICorDebugInternalFrame2](icordebuginternalframe2-interface.md) 对象) 内部帧的数组。</span><span class="sxs-lookup"><span data-stu-id="0ff4d-111">Returns an array of internal frames ([ICorDebugInternalFrame2](icordebuginternalframe2-interface.md) objects) on the stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0ff4d-112">备注</span><span class="sxs-lookup"><span data-stu-id="0ff4d-112">Remarks</span></span>  

 <span data-ttu-id="0ff4d-113">`ICorDebugThread3` 是 ICorDebugThread 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="0ff4d-113">`ICorDebugThread3` is a logical extension to the ICorDebugThread interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0ff4d-114">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="0ff4d-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ff4d-115">要求</span><span class="sxs-lookup"><span data-stu-id="0ff4d-115">Requirements</span></span>  

 <span data-ttu-id="0ff4d-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0ff4d-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ff4d-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0ff4d-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0ff4d-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0ff4d-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0ff4d-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ff4d-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ff4d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ff4d-120">See also</span></span>

- [<span data-ttu-id="0ff4d-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="0ff4d-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="0ff4d-122">调试</span><span class="sxs-lookup"><span data-stu-id="0ff4d-122">Debugging</span></span>](index.md)

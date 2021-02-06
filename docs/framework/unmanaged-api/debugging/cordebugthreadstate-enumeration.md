---
description: 了解详细信息： CorDebugThreadState 枚举
title: CorDebugThreadState 枚举
ms.date: 03/30/2017
api_name:
- CorDebugThreadState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugThreadState
helpviewer_keywords:
- CorDebugThreadState enumeration [.NET Framework debugging]
ms.assetid: a3ccdf18-4ec6-494d-9024-48e5c8c724f5
topic_type:
- apiref
ms.openlocfilehash: 0cf83ee31547e49ccc7d09e0ab4ee85548688b36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661800"
---
# <a name="cordebugthreadstate-enumeration"></a><span data-ttu-id="8cc56-103">CorDebugThreadState 枚举</span><span class="sxs-lookup"><span data-stu-id="8cc56-103">CorDebugThreadState Enumeration</span></span>

<span data-ttu-id="8cc56-104">指定用于调试的线程的状态。</span><span class="sxs-lookup"><span data-stu-id="8cc56-104">Specifies the state of a thread for debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cc56-105">语法</span><span class="sxs-lookup"><span data-stu-id="8cc56-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugThreadState {  
    THREAD_RUN,  
    THREAD_SUSPEND  
} CorDebugThreadState;  
```  
  
## <a name="members"></a><span data-ttu-id="8cc56-106">成员</span><span class="sxs-lookup"><span data-stu-id="8cc56-106">Members</span></span>  
  
|<span data-ttu-id="8cc56-107">成员</span><span class="sxs-lookup"><span data-stu-id="8cc56-107">Member</span></span>|<span data-ttu-id="8cc56-108">说明</span><span class="sxs-lookup"><span data-stu-id="8cc56-108">Description</span></span>|  
|------------|-----------------|  
|`THREAD_RUN`|<span data-ttu-id="8cc56-109">线程自由运行，除非调试事件发生。</span><span class="sxs-lookup"><span data-stu-id="8cc56-109">The thread runs freely, unless a debug event occurs.</span></span>|  
|`THREAD_SUSPEND`|<span data-ttu-id="8cc56-110">线程无法运行。</span><span class="sxs-lookup"><span data-stu-id="8cc56-110">The thread cannot run.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8cc56-111">备注</span><span class="sxs-lookup"><span data-stu-id="8cc56-111">Remarks</span></span>  

 <span data-ttu-id="8cc56-112">调试器使用 `CorDebugThreadState` 枚举来控制线程的执行。</span><span class="sxs-lookup"><span data-stu-id="8cc56-112">The debugger uses the `CorDebugThreadState` enumeration to control a thread's execution.</span></span> <span data-ttu-id="8cc56-113">可以使用 [ICorDebugThread：： SetDebugState](icordebugthread-setdebugstate-method.md) 或 [ICorDebugController：： SetAllThreadsDebugState](icordebugcontroller-setallthreadsdebugstate-method.md) 方法设置线程的状态。</span><span class="sxs-lookup"><span data-stu-id="8cc56-113">The state of a thread can be set by using the [ICorDebugThread::SetDebugState](icordebugthread-setdebugstate-method.md) or [ICorDebugController::SetAllThreadsDebugState](icordebugcontroller-setallthreadsdebugstate-method.md) method.</span></span>  
  
 <span data-ttu-id="8cc56-114">向 [宿主 API](../hosting/index.md) 提供的回调启用消息泵，因此不需要中断的状态。</span><span class="sxs-lookup"><span data-stu-id="8cc56-114">A callback provided to the [hosting API](../hosting/index.md) enables message pumping, so an interrupted state is not needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8cc56-115">要求</span><span class="sxs-lookup"><span data-stu-id="8cc56-115">Requirements</span></span>  

 <span data-ttu-id="8cc56-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8cc56-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8cc56-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8cc56-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8cc56-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8cc56-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8cc56-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8cc56-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cc56-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="8cc56-120">See also</span></span>

- [<span data-ttu-id="8cc56-121">调试枚举</span><span class="sxs-lookup"><span data-stu-id="8cc56-121">Debugging Enumerations</span></span>](debugging-enumerations.md)

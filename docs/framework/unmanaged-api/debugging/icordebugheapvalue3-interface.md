---
description: 了解详细信息： ICorDebugHeapValue3 接口
title: ICorDebugHeapValue3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3
helpviewer_keywords:
- ICorDebugHeapValue3 interface [.NET Framework debugging]
ms.assetid: 9c421bb0-e647-4b2d-a986-f3d578cc7f20
topic_type:
- apiref
ms.openlocfilehash: 2483f74e2cfc105fd23c37af6ada467f17b9556b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791460"
---
# <a name="icordebugheapvalue3-interface"></a><span data-ttu-id="b7b30-103">ICorDebugHeapValue3 接口</span><span class="sxs-lookup"><span data-stu-id="b7b30-103">ICorDebugHeapValue3 Interface</span></span>

<span data-ttu-id="b7b30-104">公开对象的监视器锁属性。</span><span class="sxs-lookup"><span data-stu-id="b7b30-104">Exposes the monitor lock properties of objects.</span></span> <span data-ttu-id="b7b30-105">此接口扩展 ICorDebugHeapValue 和 ICorDebugHeapValue2 接口。</span><span class="sxs-lookup"><span data-stu-id="b7b30-105">This interface extends the ICorDebugHeapValue and ICorDebugHeapValue2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b7b30-106">方法</span><span class="sxs-lookup"><span data-stu-id="b7b30-106">Methods</span></span>  
  
|<span data-ttu-id="b7b30-107">方法</span><span class="sxs-lookup"><span data-stu-id="b7b30-107">Method</span></span>|<span data-ttu-id="b7b30-108">说明</span><span class="sxs-lookup"><span data-stu-id="b7b30-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b7b30-109">GetThreadOwningMonitorLock 方法</span><span class="sxs-lookup"><span data-stu-id="b7b30-109">GetThreadOwningMonitorLock Method</span></span>](icordebugheapvalue3-getthreadowningmonitorlock-method.md)|<span data-ttu-id="b7b30-110">返回拥有此对象的监视器锁的托管线程。</span><span class="sxs-lookup"><span data-stu-id="b7b30-110">Returns the managed thread that owns the monitor lock on this object.</span></span>|  
|[<span data-ttu-id="b7b30-111">GetMonitorEventWaitList 方法</span><span class="sxs-lookup"><span data-stu-id="b7b30-111">GetMonitorEventWaitList Method</span></span>](icordebugheapvalue3-getmonitoreventwaitlist-method.md)|<span data-ttu-id="b7b30-112">提供在与监视器锁关联的事件上排队的线程的排序列表。</span><span class="sxs-lookup"><span data-stu-id="b7b30-112">Provides an ordered list of threads that are queued on the event that is associated with a monitor lock.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b7b30-113">备注</span><span class="sxs-lookup"><span data-stu-id="b7b30-113">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b7b30-114">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b7b30-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7b30-115">要求</span><span class="sxs-lookup"><span data-stu-id="b7b30-115">Requirements</span></span>  

 <span data-ttu-id="b7b30-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b7b30-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7b30-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b7b30-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b7b30-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7b30-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7b30-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7b30-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7b30-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7b30-120">See also</span></span>

- [<span data-ttu-id="b7b30-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="b7b30-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="b7b30-122">调试</span><span class="sxs-lookup"><span data-stu-id="b7b30-122">Debugging</span></span>](index.md)

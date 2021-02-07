---
description: 了解详细信息： CorDebugBlockingReason 枚举
title: CorDebugBlockingReason 枚举
ms.date: 03/30/2017
api_name:
- CorDebugBlockingReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugBlockingReason
helpviewer_keywords:
- CorDebugBlockingReason enumeration [.NET Framework debugging]
ms.assetid: a6ac2531-ddfe-46fd-88fe-8b1eabe0b255
topic_type:
- apiref
ms.openlocfilehash: c2d9c805549d046fe40ab5ea00f30e2fd0a680a3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747096"
---
# <a name="cordebugblockingreason-enumeration"></a><span data-ttu-id="d370d-103">CorDebugBlockingReason 枚举</span><span class="sxs-lookup"><span data-stu-id="d370d-103">CorDebugBlockingReason Enumeration</span></span>

<span data-ttu-id="d370d-104">指定线程可能在给定对象上受到阻塞的原因。</span><span class="sxs-lookup"><span data-stu-id="d370d-104">Specifies the reasons why a thread may become blocked on a given object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d370d-105">语法</span><span class="sxs-lookup"><span data-stu-id="d370d-105">Syntax</span></span>  
  
```cpp  
Typedef enum CorDebugBlockingReason  
{  
   BLOCKING_NONE = 0  
   BLOCKING_MONITOR_CRITICAL_SECTION = 1  
   BLOCKING_MONITOR_EVENT = 2  
}  CorDebugBlockingReason;  
```  
  
## <a name="members"></a><span data-ttu-id="d370d-106">成员</span><span class="sxs-lookup"><span data-stu-id="d370d-106">Members</span></span>  
  
|<span data-ttu-id="d370d-107">成员</span><span class="sxs-lookup"><span data-stu-id="d370d-107">Member</span></span>|<span data-ttu-id="d370d-108">说明</span><span class="sxs-lookup"><span data-stu-id="d370d-108">Description</span></span>|  
|------------|-----------------|  
|`BLOCKING_NONE`|<span data-ttu-id="d370d-109">仅限内部使用。</span><span class="sxs-lookup"><span data-stu-id="d370d-109">Internal use only.</span></span>|  
|`BLOCKING_MONITOR_CRITICAL_SECTION`|<span data-ttu-id="d370d-110">线程尝试获取与对象上的监视器锁关联的临界区。</span><span class="sxs-lookup"><span data-stu-id="d370d-110">A thread is trying to acquire the critical section that is associated with the monitor lock on an object.</span></span> <span data-ttu-id="d370d-111">通常，在调用或方法之一时，会发生这种情况 <xref:System.Threading.Monitor.Enter%2A?displayProperty=nameWithType> <xref:System.Threading.Monitor.TryEnter%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="d370d-111">Typically, this occurs when you call one of the <xref:System.Threading.Monitor.Enter%2A?displayProperty=nameWithType> or <xref:System.Threading.Monitor.TryEnter%2A?displayProperty=nameWithType> methods.</span></span>|  
|`BLOCKING_MONITOR_EVENT`|<span data-ttu-id="d370d-112">线程正在等待与对象的监视器锁关联的事件。</span><span class="sxs-lookup"><span data-stu-id="d370d-112">A thread is waiting on the event that is associated with a monitor lock for an object.</span></span> <span data-ttu-id="d370d-113">通常情况下，当调用其中一个方法时，会发生这种情况 <xref:System.Threading.Monitor?displayProperty=nameWithType> `Wait` 。</span><span class="sxs-lookup"><span data-stu-id="d370d-113">Typically, this occurs when you call one of the <xref:System.Threading.Monitor?displayProperty=nameWithType>`Wait` methods.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d370d-114">备注</span><span class="sxs-lookup"><span data-stu-id="d370d-114">Remarks</span></span>  

 <span data-ttu-id="d370d-115">当 `BLOCKING_MONITOR_CRITICAL_SECTION` `BLOCKING_MONITOR_EVENT` 在 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构中使用或成员时，结构的 `pBlockingObject` 成员指向一个 "ICorDebugValue" 接口，该接口表示正在输入的对象。</span><span class="sxs-lookup"><span data-stu-id="d370d-115">When the `BLOCKING_MONITOR_CRITICAL_SECTION` or `BLOCKING_MONITOR_EVENT` member is used in a [CorDebugBlockingObject](cordebugblockingobject-structure.md) structure, the `pBlockingObject` member of the structure points to an "ICorDebugValue" interface that represents the object that is being entered.</span></span> <span data-ttu-id="d370d-116">还保证实现 [ICorDebugHeapValue3](icordebugheapvalue3-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="d370d-116">It is also guaranteed to implement the [ICorDebugHeapValue3](icordebugheapvalue3-interface.md) interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d370d-117">要求</span><span class="sxs-lookup"><span data-stu-id="d370d-117">Requirements</span></span>  

 <span data-ttu-id="d370d-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d370d-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d370d-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d370d-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d370d-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d370d-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d370d-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d370d-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d370d-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="d370d-122">See also</span></span>

- [<span data-ttu-id="d370d-123">调试枚举</span><span class="sxs-lookup"><span data-stu-id="d370d-123">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="d370d-124">调试</span><span class="sxs-lookup"><span data-stu-id="d370d-124">Debugging</span></span>](index.md)

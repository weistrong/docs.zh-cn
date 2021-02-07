---
description: 了解详细信息： CorDebugBlockingObject 结构
title: CorDebugBlockingObject 结构
ms.date: 03/30/2017
api_name:
- CorDebugBlockingObject Structure
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugBlockingObject
helpviewer_keywords:
- CorDebugBlockingObject structure [.NET Framework debugging]
ms.assetid: 5944edd1-0914-4efa-aba0-d5a277c38b1a
topic_type:
- apiref
ms.openlocfilehash: 2b16af5eecb01067c2ee6811613f964af391f345
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712204"
---
# <a name="cordebugblockingobject-structure"></a><span data-ttu-id="2291e-103">CorDebugBlockingObject 结构</span><span class="sxs-lookup"><span data-stu-id="2291e-103">CorDebugBlockingObject Structure</span></span>

<span data-ttu-id="2291e-104">定义一个对象，该对象阻止线程，并且该线程被阻止的特定原因。</span><span class="sxs-lookup"><span data-stu-id="2291e-104">Defines an object that is blocking a thread and the specific reason that the thread is blocked.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2291e-105">语法</span><span class="sxs-lookup"><span data-stu-id="2291e-105">Syntax</span></span>  
  
```cpp  
Typedef struct CorDebugBlockingObject  
{  
ICorDebugValue pBlockingObject;  
DWORD dwTimeout;  
CorDebugBlockingReason blockingReason;  
}  CorDebugBlockingObject;  
```  
  
## <a name="members"></a><span data-ttu-id="2291e-106">成员</span><span class="sxs-lookup"><span data-stu-id="2291e-106">Members</span></span>  
  
|<span data-ttu-id="2291e-107">成员</span><span class="sxs-lookup"><span data-stu-id="2291e-107">Member</span></span>|<span data-ttu-id="2291e-108">说明</span><span class="sxs-lookup"><span data-stu-id="2291e-108">Description</span></span>|  
|------------|-----------------|  
|`pBlockingObject`|<span data-ttu-id="2291e-109">线程要阻止的对象。</span><span class="sxs-lookup"><span data-stu-id="2291e-109">The object on which the thread is blocking.</span></span> <span data-ttu-id="2291e-110">此对象仅在当前已同步状态的持续时间内有效。</span><span class="sxs-lookup"><span data-stu-id="2291e-110">This object is valid only for the duration of the current synchronized state.</span></span> <span data-ttu-id="2291e-111">如果两个线程在同一对象处于相同的同步状态，则可能需要 [ICorDebugValue：： GetAddress](icordebugvalue-getaddress-method.md) 方法返回相同的值。</span><span class="sxs-lookup"><span data-stu-id="2291e-111">If two threads are blocking on the same object within the same synchronized state, you may expect the [ICorDebugValue::GetAddress](icordebugvalue-getaddress-method.md) method to return the same value.</span></span> <span data-ttu-id="2291e-112">但是，接口可能与指针等效。</span><span class="sxs-lookup"><span data-stu-id="2291e-112">However, the interfaces may or may not be pointer equivalent.</span></span>|  
|`dwTimeout`|<span data-ttu-id="2291e-113">阻止操作超时前等待的毫秒数，或值无限，这表示不会超时。超时值指定阻止操作的总时间长度，而不是剩余时间。</span><span class="sxs-lookup"><span data-stu-id="2291e-113">The number of milliseconds before the blocking operation will time out, or the value INFINITE, which indicates that it will not time out. The time-out value specifies the total length of time for the blocking operation, not the time that is still remaining.</span></span>|  
|`blockingReason`|<span data-ttu-id="2291e-114">此对象上阻塞线程的原因。</span><span class="sxs-lookup"><span data-stu-id="2291e-114">The reason that the thread is blocked on this object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2291e-115">备注</span><span class="sxs-lookup"><span data-stu-id="2291e-115">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2291e-116">要求</span><span class="sxs-lookup"><span data-stu-id="2291e-116">Requirements</span></span>  

 <span data-ttu-id="2291e-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2291e-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2291e-118">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="2291e-118">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="2291e-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2291e-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2291e-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2291e-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2291e-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="2291e-121">See also</span></span>

- [<span data-ttu-id="2291e-122">调试结构</span><span class="sxs-lookup"><span data-stu-id="2291e-122">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="2291e-123">调试</span><span class="sxs-lookup"><span data-stu-id="2291e-123">Debugging</span></span>](index.md)

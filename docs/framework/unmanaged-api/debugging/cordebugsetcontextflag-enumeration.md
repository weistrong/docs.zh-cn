---
description: 了解详细信息： CorDebugSetContextFlag 枚举
title: CorDebugSetContextFlag 枚举
ms.date: 03/30/2017
api_name:
- CorDebugSetContextFlag
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugSetContextFlag
helpviewer_keywords:
- CorDebugSetContextFlag enumeration [.NET Framework debugging]
ms.assetid: b30280bb-fe75-44ed-8589-bcff081fae44
topic_type:
- apiref
ms.openlocfilehash: 625f24e516ff462cf3d0e628dfff6c08793807ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801548"
---
# <a name="cordebugsetcontextflag-enumeration"></a><span data-ttu-id="e8d8d-103">CorDebugSetContextFlag 枚举</span><span class="sxs-lookup"><span data-stu-id="e8d8d-103">CorDebugSetContextFlag Enumeration</span></span>

<span data-ttu-id="e8d8d-104">指示上下文是来自堆栈上的活动（或叶）帧，还是已通过从另一个帧展开来进行计算。</span><span class="sxs-lookup"><span data-stu-id="e8d8d-104">Indicates whether the context is from the active (or leaf) frame on the stack or has been computed by unwinding from another frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8d8d-105">语法</span><span class="sxs-lookup"><span data-stu-id="e8d8d-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugSetContextFlag  
{  
   SET_CONTEXT_FLAG_ACTIVE_FRAME = 1  
   SET_CONTEXT_FLAG_UNWIND_FRAME = 2  
}  CorDebugSetContextFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="e8d8d-106">成员</span><span class="sxs-lookup"><span data-stu-id="e8d8d-106">Members</span></span>  
  
|<span data-ttu-id="e8d8d-107">成员</span><span class="sxs-lookup"><span data-stu-id="e8d8d-107">Member</span></span>|<span data-ttu-id="e8d8d-108">说明</span><span class="sxs-lookup"><span data-stu-id="e8d8d-108">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="e8d8d-109">SET_CONTEXT_FLAG_ACTIVE_FRAME</span><span class="sxs-lookup"><span data-stu-id="e8d8d-109">SET_CONTEXT_FLAG_ACTIVE_FRAME</span></span>|<span data-ttu-id="e8d8d-110">上下文是线程的活动上下文。</span><span class="sxs-lookup"><span data-stu-id="e8d8d-110">The context is the thread’s active context.</span></span>|  
|<span data-ttu-id="e8d8d-111">SET_CONTEXT_FLAG_UNWIND_FRAME</span><span class="sxs-lookup"><span data-stu-id="e8d8d-111">SET_CONTEXT_FLAG_UNWIND_FRAME</span></span>|<span data-ttu-id="e8d8d-112">已通过从另一个帧展开上下文来计算上下文。</span><span class="sxs-lookup"><span data-stu-id="e8d8d-112">The context has been computed by unwinding from another frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e8d8d-113">备注</span><span class="sxs-lookup"><span data-stu-id="e8d8d-113">Remarks</span></span>  

 <span data-ttu-id="e8d8d-114">`CorDebugSetContextFlag` 提供 [ICorDebugStackWalk：： SetContext](icordebugstackwalk-setcontext-method.md) 方法使用的值。</span><span class="sxs-lookup"><span data-stu-id="e8d8d-114">`CorDebugSetContextFlag` provides values that are used by the [ICorDebugStackWalk::SetContext](icordebugstackwalk-setcontext-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8d8d-115">要求</span><span class="sxs-lookup"><span data-stu-id="e8d8d-115">Requirements</span></span>  

 <span data-ttu-id="e8d8d-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8d8d-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8d8d-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e8d8d-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e8d8d-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8d8d-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8d8d-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8d8d-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8d8d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e8d8d-120">See also</span></span>

- [<span data-ttu-id="e8d8d-121">调试枚举</span><span class="sxs-lookup"><span data-stu-id="e8d8d-121">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="e8d8d-122">调试</span><span class="sxs-lookup"><span data-stu-id="e8d8d-122">Debugging</span></span>](index.md)

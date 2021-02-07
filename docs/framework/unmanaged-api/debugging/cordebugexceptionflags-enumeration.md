---
description: 了解详细信息： CorDebugExceptionFlags 枚举
title: CorDebugExceptionFlags 枚举
ms.date: 03/30/2017
api_name:
- CorDebugExceptionFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionFlags
helpviewer_keywords:
- CorDebugExceptionFlags enumeration [.NET Framework debugging]
ms.assetid: b22687a8-e9cf-4e65-a1b0-f92a81bc524e
topic_type:
- apiref
ms.openlocfilehash: c0036c2674f3202623da1a8fdeea14165a2a6e62
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747030"
---
# <a name="cordebugexceptionflags-enumeration"></a><span data-ttu-id="76de1-103">CorDebugExceptionFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="76de1-103">CorDebugExceptionFlags Enumeration</span></span>

<span data-ttu-id="76de1-104">提供有关异常的附加信息。</span><span class="sxs-lookup"><span data-stu-id="76de1-104">Provides additional information about an exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76de1-105">语法</span><span class="sxs-lookup"><span data-stu-id="76de1-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugExceptionFlags {  
    DEBUG_EXCEPTION_NONE = 0,  
    DEBUG_EXCEPTION_CAN_BE_INTERCEPTED = 0x0001  
} CorDebugExceptionFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="76de1-106">成员</span><span class="sxs-lookup"><span data-stu-id="76de1-106">Members</span></span>  
  
|<span data-ttu-id="76de1-107">成员</span><span class="sxs-lookup"><span data-stu-id="76de1-107">Member</span></span>|<span data-ttu-id="76de1-108">说明</span><span class="sxs-lookup"><span data-stu-id="76de1-108">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EXCEPTION_NONE`|<span data-ttu-id="76de1-109">没有异常。</span><span class="sxs-lookup"><span data-stu-id="76de1-109">There is no exception.</span></span>|  
|`DEBUG_EXCEPTION_CAN_BE_INTERCEPTED`|<span data-ttu-id="76de1-110">异常是可截获的。</span><span class="sxs-lookup"><span data-stu-id="76de1-110">The exception is interceptable.</span></span><br /><br /> <span data-ttu-id="76de1-111">异常的发生时间可能仍然会使调试器无法截获异常。</span><span class="sxs-lookup"><span data-stu-id="76de1-111">The timing of the exception may still be such that the debugger cannot intercept it.</span></span> <span data-ttu-id="76de1-112">例如，如果当前回调或实时 (JIT) 连接引起的异常事件下没有托管代码，则无法截获异常。</span><span class="sxs-lookup"><span data-stu-id="76de1-112">For example, if there is no managed code below the current callback or the exception event resulted from a just-in-time (JIT) attachment, the exception cannot be intercepted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="76de1-113">备注</span><span class="sxs-lookup"><span data-stu-id="76de1-113">Remarks</span></span>  

 <span data-ttu-id="76de1-114">以后的版本可能会向此枚举中添加新值，因此你应针对意外值准备使用 `CorDebugExceptionFlags` 的代码。</span><span class="sxs-lookup"><span data-stu-id="76de1-114">New values may be added to this enumeration in later versions, so you should prepare code that uses `CorDebugExceptionFlags` for unexpected values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76de1-115">要求</span><span class="sxs-lookup"><span data-stu-id="76de1-115">Requirements</span></span>  

 <span data-ttu-id="76de1-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="76de1-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76de1-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="76de1-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="76de1-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="76de1-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="76de1-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76de1-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76de1-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="76de1-120">See also</span></span>

- [<span data-ttu-id="76de1-121">调试枚举</span><span class="sxs-lookup"><span data-stu-id="76de1-121">Debugging Enumerations</span></span>](debugging-enumerations.md)

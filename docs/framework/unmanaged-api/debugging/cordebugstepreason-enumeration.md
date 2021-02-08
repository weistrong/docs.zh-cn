---
description: 了解详细信息： CorDebugStepReason 枚举
title: CorDebugStepReason 枚举
ms.date: 03/30/2017
api_name:
- CorDebugStepReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugStepReason
helpviewer_keywords:
- CorDebugStepReason enumeration [.NET Framework debugging]
ms.assetid: fe248069-b33c-48e1-a777-06ac9b239c54
topic_type:
- apiref
ms.openlocfilehash: 2a331b09709ffb6179f2e481baf4bf421d60ea99
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801535"
---
# <a name="cordebugstepreason-enumeration"></a><span data-ttu-id="a6fe4-103">CorDebugStepReason 枚举</span><span class="sxs-lookup"><span data-stu-id="a6fe4-103">CorDebugStepReason Enumeration</span></span>

<span data-ttu-id="a6fe4-104">指示一个单步执行的结果。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-104">Indicates the outcome of an individual step.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6fe4-105">语法</span><span class="sxs-lookup"><span data-stu-id="a6fe4-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugStepReason {  
    STEP_NORMAL,  
    STEP_RETURN,  
    STEP_CALL,  
    STEP_EXCEPTION_FILTER,  
    STEP_EXCEPTION_HANDLER,  
    STEP_INTERCEPT,  
    STEP_EXIT  
} CorDebugStepReason;  
```  
  
## <a name="members"></a><span data-ttu-id="a6fe4-106">成员</span><span class="sxs-lookup"><span data-stu-id="a6fe4-106">Members</span></span>  
  
|<span data-ttu-id="a6fe4-107">成员</span><span class="sxs-lookup"><span data-stu-id="a6fe4-107">Member</span></span>|<span data-ttu-id="a6fe4-108">说明</span><span class="sxs-lookup"><span data-stu-id="a6fe4-108">Description</span></span>|  
|------------|-----------------|  
|`STEP_NORMAL`|<span data-ttu-id="a6fe4-109">单步执行在同一函数内正常完成。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-109">Stepping completed normally, within the same function.</span></span>|  
|`STEP_RETURN`|<span data-ttu-id="a6fe4-110">在函数返回后，按正常方式继续执行。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-110">Stepping continued normally, after the function returned.</span></span>|  
|`STEP_CALL`|<span data-ttu-id="a6fe4-111">在新调用的函数开始时以正常方式继续执行。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-111">Stepping continued normally, at the beginning of a newly called function.</span></span>|  
|`STEP_EXCEPTION_FILTER`|<span data-ttu-id="a6fe4-112">已生成异常，并已将控制权传递给异常筛选器。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-112">An exception was generated and control was passed to an exception filter.</span></span>|  
|`STEP_EXCEPTION_HANDLER`|<span data-ttu-id="a6fe4-113">已生成异常，并已将控制权传递给异常处理程序。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-113">An exception was generated and control was passed to an exception handler.</span></span>|  
|`STEP_INTERCEPT`|<span data-ttu-id="a6fe4-114">控件已传递给侦听器。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-114">Control was passed to an interceptor.</span></span>|  
|`STEP_EXIT`|<span data-ttu-id="a6fe4-115">线程在步骤完成之前退出。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-115">The thread exited before the step was completed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a6fe4-116">要求</span><span class="sxs-lookup"><span data-stu-id="a6fe4-116">Requirements</span></span>  

 <span data-ttu-id="a6fe4-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6fe4-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6fe4-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a6fe4-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a6fe4-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a6fe4-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a6fe4-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6fe4-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6fe4-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6fe4-121">See also</span></span>

- [<span data-ttu-id="a6fe4-122">StepComplete 方法</span><span class="sxs-lookup"><span data-stu-id="a6fe4-122">StepComplete Method</span></span>](icordebugmanagedcallback-stepcomplete-method.md)
- [<span data-ttu-id="a6fe4-123">调试枚举</span><span class="sxs-lookup"><span data-stu-id="a6fe4-123">Debugging Enumerations</span></span>](debugging-enumerations.md)

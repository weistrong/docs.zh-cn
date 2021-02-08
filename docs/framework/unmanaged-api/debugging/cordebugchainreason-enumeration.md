---
description: 了解详细信息： CorDebugChainReason 枚举
title: CorDebugChainReason 枚举
ms.date: 03/30/2017
api_name:
- CorDebugChainReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugChainReason
helpviewer_keywords:
- CorDebugChainReason enumeration [.NET Framework debugging]
ms.assetid: c915da51-50b2-41df-841a-2b971f4d0975
topic_type:
- apiref
ms.openlocfilehash: 18b6ac9c50c3a44a77a0f63a680b84c70e667e9f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801743"
---
# <a name="cordebugchainreason-enumeration"></a><span data-ttu-id="f4f0e-103">CorDebugChainReason 枚举</span><span class="sxs-lookup"><span data-stu-id="f4f0e-103">CorDebugChainReason Enumeration</span></span>

<span data-ttu-id="f4f0e-104">指示启动调用链的一个或多个原因。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-104">Indicates the reason or reasons for the initiation of a call chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4f0e-105">语法</span><span class="sxs-lookup"><span data-stu-id="f4f0e-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugChainReason {  
    CHAIN_NONE              = 0x000,  
    CHAIN_CLASS_INIT        = 0x001,  
    CHAIN_EXCEPTION_FILTER  = 0x002,  
    CHAIN_SECURITY          = 0x004,  
    CHAIN_CONTEXT_POLICY    = 0x008,  
    CHAIN_INTERCEPTION      = 0x010,  
    CHAIN_PROCESS_START     = 0x020,  
    CHAIN_THREAD_START      = 0x040,  
    CHAIN_ENTER_MANAGED     = 0x080,  
    CHAIN_ENTER_UNMANAGED   = 0x100,  
    CHAIN_DEBUGGER_EVAL     = 0x200,  
    CHAIN_CONTEXT_SWITCH    = 0x400,  
    CHAIN_FUNC_EVAL         = 0x800  
} CorDebugChainReason;  
```  
  
## <a name="members"></a><span data-ttu-id="f4f0e-106">成员</span><span class="sxs-lookup"><span data-stu-id="f4f0e-106">Members</span></span>  
  
|<span data-ttu-id="f4f0e-107">成员</span><span class="sxs-lookup"><span data-stu-id="f4f0e-107">Member</span></span>|<span data-ttu-id="f4f0e-108">说明</span><span class="sxs-lookup"><span data-stu-id="f4f0e-108">Description</span></span>|  
|------------|-----------------|  
|`CHAIN_NONE`|<span data-ttu-id="f4f0e-109">尚未启动任何调用链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-109">No call chain has been initiated.</span></span>|  
|`CHAIN_CLASS_INIT`|<span data-ttu-id="f4f0e-110">由构造函数启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-110">The chain was initiated by a constructor.</span></span>|  
|`CHAIN_EXCEPTION_FILTER`|<span data-ttu-id="f4f0e-111">由异常筛选器启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-111">The chain was initiated by an exception filter.</span></span>|  
|`CHAIN_SECURITY`|<span data-ttu-id="f4f0e-112">由强制实施安全的代码启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-112">The chain was initiated by code that enforces security.</span></span>|  
|`CHAIN_CONTEXT_POLICY`|<span data-ttu-id="f4f0e-113">由上下文策略启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-113">The chain was initiated by a context policy.</span></span>|  
|`CHAIN_INTERCEPTION`|<span data-ttu-id="f4f0e-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-114">Not used.</span></span>|  
|`CHAIN_PROCESS_START`|<span data-ttu-id="f4f0e-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-115">Not used.</span></span>|  
|`CHAIN_THREAD_START`|<span data-ttu-id="f4f0e-116">由线程执行开始启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-116">The chain was initiated by the start of a thread execution.</span></span>|  
|`CHAIN_ENTER_MANAGED`|<span data-ttu-id="f4f0e-117">由托管代码中的条目启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-117">The chain was initiated by entry into managed code.</span></span>|  
|`CHAIN_ENTER_UNMANAGED`|<span data-ttu-id="f4f0e-118">由非托管代码中的条目启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-118">The chain was initiated by entry into unmanaged code.</span></span>|  
|`CHAIN_DEBUGGER_EVAL`|<span data-ttu-id="f4f0e-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-119">Not used.</span></span>|  
|`CHAIN_CONTEXT_SWITCH`|<span data-ttu-id="f4f0e-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-120">Not used.</span></span>|  
|`CHAIN_FUNC_EVAL`|<span data-ttu-id="f4f0e-121">由函数求值启动该链。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-121">The chain was initiated by a function evaluation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f4f0e-122">备注</span><span class="sxs-lookup"><span data-stu-id="f4f0e-122">Remarks</span></span>  

 <span data-ttu-id="f4f0e-123">使用 [ICorDebugChain：： GetReason](icordebugchain-getreason-method.md) 方法来确定启动调用链的原因。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-123">Use the [ICorDebugChain::GetReason](icordebugchain-getreason-method.md) method to ascertain the reasons for the initiation of a call chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4f0e-124">要求</span><span class="sxs-lookup"><span data-stu-id="f4f0e-124">Requirements</span></span>  

 <span data-ttu-id="f4f0e-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f4f0e-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4f0e-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f4f0e-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f4f0e-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f4f0e-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f4f0e-128">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4f0e-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4f0e-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="f4f0e-129">See also</span></span>

- [<span data-ttu-id="f4f0e-130">调试枚举</span><span class="sxs-lookup"><span data-stu-id="f4f0e-130">Debugging Enumerations</span></span>](debugging-enumerations.md)

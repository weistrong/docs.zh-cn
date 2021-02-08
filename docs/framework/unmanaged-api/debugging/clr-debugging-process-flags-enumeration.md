---
description: 了解详细信息： CLR_DEBUGGING_PROCESS_FLAGS 枚举
title: CLR_DEBUGGING_PROCESS_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- CLR_DEBUGGING_PROCESS_FLAGS
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLR_DEBUGGING_PROCESS_FLAG
helpviewer_keywords:
- CLR_DEBUGGING_PROCESS_FLAGS enumeration [.NET Framework debugging]
ms.assetid: 85b85fde-1f87-490b-ba8d-d604670959c3
topic_type:
- apiref
ms.openlocfilehash: 81510bde123ef9a8adefaec5b0708086dacbbf2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772804"
---
# <a name="clr_debugging_process_flags-enumeration"></a><span data-ttu-id="bc86d-103">CLR_DEBUGGING_PROCESS_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="bc86d-103">CLR_DEBUGGING_PROCESS_FLAGS Enumeration</span></span>

<span data-ttu-id="bc86d-104">提供 [ICLRDebugging：： OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) 方法使用的值。</span><span class="sxs-lookup"><span data-stu-id="bc86d-104">Provides values that are used by the [ICLRDebugging::OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc86d-105">语法</span><span class="sxs-lookup"><span data-stu-id="bc86d-105">Syntax</span></span>  
  
```cpp  
typedef enum CLR_DEBUGGING_PROCESS_FLAGS  
{  
   CLR_DEBUGGING_MANAGED_EVENT_PENDING = 1,  
   CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH = 2  
}  CLR_DEBUGGING_PROCESS_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="bc86d-106">成员</span><span class="sxs-lookup"><span data-stu-id="bc86d-106">Members</span></span>  
  
|<span data-ttu-id="bc86d-107">成员</span><span class="sxs-lookup"><span data-stu-id="bc86d-107">Member</span></span>|<span data-ttu-id="bc86d-108">说明</span><span class="sxs-lookup"><span data-stu-id="bc86d-108">Description</span></span>|  
|------------|-----------------|  
|`CLR_DEBUGGING_MANAGED_EVENT_PENDING`|<span data-ttu-id="bc86d-109">此运行时有一个要发送的非追赶托管调试器事件。</span><span class="sxs-lookup"><span data-stu-id="bc86d-109">This runtime has a non-catch-up managed debugger event to send.</span></span> <span data-ttu-id="bc86d-110">请参阅 "备注" 部分，了解追赶事件与非追赶事件之间的区别。</span><span class="sxs-lookup"><span data-stu-id="bc86d-110">See the Remarks section for the distinction between catch-up and non-catch-up events.</span></span>|  
|`CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH`|<span data-ttu-id="bc86d-111">挂起的托管事件是 <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> 请求。</span><span class="sxs-lookup"><span data-stu-id="bc86d-111">The managed event that is pending is a <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bc86d-112">备注</span><span class="sxs-lookup"><span data-stu-id="bc86d-112">Remarks</span></span>  

 <span data-ttu-id="bc86d-113">追赶事件包括进程、应用程序域、程序集、模块和线程创建通知，这会使调试器在附加到进程后进入当前状态。</span><span class="sxs-lookup"><span data-stu-id="bc86d-113">Catch-up events include process, application domain, assembly, module, and thread creation notifications that bring the debugger up to the current state after it has attached to a process.</span></span> <span data-ttu-id="bc86d-114">标记指示的非追赶事件 `CLR_DEBUGGING_MANAGED_EVENT_PENDING` 包含所有其他调试器事件，例如异常和托管调试助手 (MDA) 通知。</span><span class="sxs-lookup"><span data-stu-id="bc86d-114">Non-catch-up events, which are indicated by the `CLR_DEBUGGING_MANAGED_EVENT_PENDING` flag, include all other debugger events, such as exceptions and managed debugging assistant (MDA) notifications.</span></span>  
  
 <span data-ttu-id="bc86d-115">该 `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` 标志使运行时能够区分终止异常和请求以附加可取消的托管调试器。</span><span class="sxs-lookup"><span data-stu-id="bc86d-115">The `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` flag enables the runtime to differentiate between a terminating exception and a request to attach a managed debugger that can be canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc86d-116">要求</span><span class="sxs-lookup"><span data-stu-id="bc86d-116">Requirements</span></span>  

 <span data-ttu-id="bc86d-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bc86d-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bc86d-118">**标头：** Metahost，Metahost</span><span class="sxs-lookup"><span data-stu-id="bc86d-118">**Header:** Metahost.idl, Metahost.h</span></span>  
  
 <span data-ttu-id="bc86d-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bc86d-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bc86d-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bc86d-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc86d-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="bc86d-121">See also</span></span>

- [<span data-ttu-id="bc86d-122">调试枚举</span><span class="sxs-lookup"><span data-stu-id="bc86d-122">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="bc86d-123">调试</span><span class="sxs-lookup"><span data-stu-id="bc86d-123">Debugging</span></span>](index.md)

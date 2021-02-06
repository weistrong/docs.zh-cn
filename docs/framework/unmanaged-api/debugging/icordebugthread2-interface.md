---
description: 了解详细信息： ICorDebugThread2 接口
title: ICorDebugThread2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThread2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2
helpviewer_keywords:
- ICorDebugThread2 interface [.NET Framework debugging]
ms.assetid: 678f89f9-cce7-46d1-af87-5e989abaa93c
topic_type:
- apiref
ms.openlocfilehash: 81f687f6daff9ffa7298ec6d818a214b8934bcc3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658482"
---
# <a name="icordebugthread2-interface"></a><span data-ttu-id="14b92-103">ICorDebugThread2 接口</span><span class="sxs-lookup"><span data-stu-id="14b92-103">ICorDebugThread2 Interface</span></span>

<span data-ttu-id="14b92-104">用作 ICorDebugThread 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="14b92-104">Serves as a logical extension to the ICorDebugThread interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="14b92-105">方法</span><span class="sxs-lookup"><span data-stu-id="14b92-105">Methods</span></span>  
  
|<span data-ttu-id="14b92-106">方法</span><span class="sxs-lookup"><span data-stu-id="14b92-106">Method</span></span>|<span data-ttu-id="14b92-107">说明</span><span class="sxs-lookup"><span data-stu-id="14b92-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="14b92-108">GetActiveFunctions 方法</span><span class="sxs-lookup"><span data-stu-id="14b92-108">GetActiveFunctions Method</span></span>](icordebugthread2-getactivefunctions-method.md)|<span data-ttu-id="14b92-109">获取 COR_ACTIVE_FUNCTION 实例的数组，这些实例包含有关线程帧中的活动函数的数据。</span><span class="sxs-lookup"><span data-stu-id="14b92-109">Gets an array of COR_ACTIVE_FUNCTION instances that contain data about the active functions in a thread's frames.</span></span>|  
|[<span data-ttu-id="14b92-110">GetConnectionID 方法</span><span class="sxs-lookup"><span data-stu-id="14b92-110">GetConnectionID Method</span></span>](icordebugthread2-getconnectionid-method.md)|<span data-ttu-id="14b92-111">获取此的连接标识符 `ICorDebugThread2` 。</span><span class="sxs-lookup"><span data-stu-id="14b92-111">Gets a connection identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="14b92-112">GetTaskID 方法</span><span class="sxs-lookup"><span data-stu-id="14b92-112">GetTaskID Method</span></span>](icordebugthread2-gettaskid-method.md)|<span data-ttu-id="14b92-113">获取此的任务标识符 `ICorDebugThread2` 。</span><span class="sxs-lookup"><span data-stu-id="14b92-113">Gets a task identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="14b92-114">GetVolatileOSThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="14b92-114">GetVolatileOSThreadID Method</span></span>](icordebugthread2-getvolatileosthreadid-method.md)|<span data-ttu-id="14b92-115">获取此的操作系统线程标识符 `ICorDebugThread2` 。</span><span class="sxs-lookup"><span data-stu-id="14b92-115">Gets the operating system thread identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="14b92-116">InterceptCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="14b92-116">InterceptCurrentException Method</span></span>](icordebugthread2-interceptcurrentexception-method.md)|<span data-ttu-id="14b92-117">允许调试器截获线程上的当前异常。</span><span class="sxs-lookup"><span data-stu-id="14b92-117">Allows a debugger to intercept the current exception on a thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="14b92-118">备注</span><span class="sxs-lookup"><span data-stu-id="14b92-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="14b92-119">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="14b92-119">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="14b92-120">要求</span><span class="sxs-lookup"><span data-stu-id="14b92-120">Requirements</span></span>  

 <span data-ttu-id="14b92-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="14b92-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="14b92-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="14b92-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="14b92-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="14b92-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="14b92-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="14b92-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="14b92-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="14b92-125">See also</span></span>

- [<span data-ttu-id="14b92-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="14b92-126">Debugging Interfaces</span></span>](debugging-interfaces.md)

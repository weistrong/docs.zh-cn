---
description: 了解详细信息： ICorDebugBreakpoint 接口
title: ICorDebugBreakpoint 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint
helpviewer_keywords:
- ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: aa5ad3d7-e1bb-42af-99bc-471224e3bcaa
topic_type:
- apiref
ms.openlocfilehash: 63917512cceeccedea37acdf2ba7ab3b849d9fad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711799"
---
# <a name="icordebugbreakpoint-interface"></a><span data-ttu-id="aedbc-103">ICorDebugBreakpoint 接口</span><span class="sxs-lookup"><span data-stu-id="aedbc-103">ICorDebugBreakpoint Interface</span></span>

<span data-ttu-id="aedbc-104">表示函数中的断点或某个值的监视点。</span><span class="sxs-lookup"><span data-stu-id="aedbc-104">Represents a breakpoint in a function, or a watch point on a value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="aedbc-105">方法</span><span class="sxs-lookup"><span data-stu-id="aedbc-105">Methods</span></span>  
  
|<span data-ttu-id="aedbc-106">方法</span><span class="sxs-lookup"><span data-stu-id="aedbc-106">Method</span></span>|<span data-ttu-id="aedbc-107">说明</span><span class="sxs-lookup"><span data-stu-id="aedbc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="aedbc-108">Activate 方法</span><span class="sxs-lookup"><span data-stu-id="aedbc-108">Activate Method</span></span>](icordebugbreakpoint-activate-method.md)|<span data-ttu-id="aedbc-109">设置此的活动状态 `ICorDebugBreakpoint` 。</span><span class="sxs-lookup"><span data-stu-id="aedbc-109">Sets the active state of this `ICorDebugBreakpoint`.</span></span>|  
|[<span data-ttu-id="aedbc-110">IsActive 方法</span><span class="sxs-lookup"><span data-stu-id="aedbc-110">IsActive Method</span></span>](icordebugbreakpoint-isactive-method.md)|<span data-ttu-id="aedbc-111">获取一个值，该值指示此是否处于 `ICorDebugBreakpoint` 活动状态。</span><span class="sxs-lookup"><span data-stu-id="aedbc-111">Gets a value that indicates whether this `ICorDebugBreakpoint` is active.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aedbc-112">备注</span><span class="sxs-lookup"><span data-stu-id="aedbc-112">Remarks</span></span>  

 <span data-ttu-id="aedbc-113">断点不直接支持条件表达式。</span><span class="sxs-lookup"><span data-stu-id="aedbc-113">Breakpoints do not directly support conditional expressions.</span></span> <span data-ttu-id="aedbc-114">如果需要此类功能，调试程序必须在顶层实现它 `ICorDebugBreakpoint` 。</span><span class="sxs-lookup"><span data-stu-id="aedbc-114">If such functionality is desired, a debugger must implement it on top of `ICorDebugBreakpoint`.</span></span>  
  
 <span data-ttu-id="aedbc-115">ICorDebugFunctionBreakpoint 接口扩展 `ICorDebugBreakpoint` 以支持函数内的断点。</span><span class="sxs-lookup"><span data-stu-id="aedbc-115">The ICorDebugFunctionBreakpoint interface extends `ICorDebugBreakpoint` to support breakpoints within functions.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="aedbc-116">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="aedbc-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aedbc-117">要求</span><span class="sxs-lookup"><span data-stu-id="aedbc-117">Requirements</span></span>  

 <span data-ttu-id="aedbc-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aedbc-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aedbc-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aedbc-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aedbc-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aedbc-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aedbc-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aedbc-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aedbc-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="aedbc-122">See also</span></span>

- [<span data-ttu-id="aedbc-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="aedbc-123">Debugging Interfaces</span></span>](debugging-interfaces.md)

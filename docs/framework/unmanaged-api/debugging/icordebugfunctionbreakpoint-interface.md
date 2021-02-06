---
description: 了解详细信息： ICorDebugFunctionBreakpoint 接口
title: ICorDebugFunctionBreakpoint 接口
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint
helpviewer_keywords:
- ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: 9c149303-14b1-4138-83d7-e8c3e0fcd332
topic_type:
- apiref
ms.openlocfilehash: 5d7597369241272d91de4b94a60d787304dc1c6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661124"
---
# <a name="icordebugfunctionbreakpoint-interface"></a><span data-ttu-id="c25cc-103">ICorDebugFunctionBreakpoint 接口</span><span class="sxs-lookup"><span data-stu-id="c25cc-103">ICorDebugFunctionBreakpoint Interface</span></span>

<span data-ttu-id="c25cc-104">扩展 ICorDebugBreakpoint 接口以支持函数内的断点。</span><span class="sxs-lookup"><span data-stu-id="c25cc-104">Extends the ICorDebugBreakpoint interface to support breakpoints within functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c25cc-105">方法</span><span class="sxs-lookup"><span data-stu-id="c25cc-105">Methods</span></span>  
  
|<span data-ttu-id="c25cc-106">方法</span><span class="sxs-lookup"><span data-stu-id="c25cc-106">Method</span></span>|<span data-ttu-id="c25cc-107">说明</span><span class="sxs-lookup"><span data-stu-id="c25cc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c25cc-108">GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="c25cc-108">GetFunction Method</span></span>](icordebugfunctionbreakpoint-getfunction-method.md)|<span data-ttu-id="c25cc-109">获取一个指向 ICorDebugFunction 的接口指针，该指针引用在其中设置断点的函数。</span><span class="sxs-lookup"><span data-stu-id="c25cc-109">Gets an interface pointer to an ICorDebugFunction that references the function in which the breakpoint is set.</span></span>|  
|[<span data-ttu-id="c25cc-110">GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="c25cc-110">GetOffset Method</span></span>](icordebugfunctionbreakpoint-getoffset-method.md)|<span data-ttu-id="c25cc-111">获取函数内断点的偏移量。</span><span class="sxs-lookup"><span data-stu-id="c25cc-111">Gets the offset of the breakpoint within the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c25cc-112">备注</span><span class="sxs-lookup"><span data-stu-id="c25cc-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c25cc-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="c25cc-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c25cc-114">要求</span><span class="sxs-lookup"><span data-stu-id="c25cc-114">Requirements</span></span>  

 <span data-ttu-id="c25cc-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c25cc-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c25cc-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c25cc-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c25cc-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c25cc-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c25cc-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c25cc-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c25cc-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="c25cc-119">See also</span></span>

- [<span data-ttu-id="c25cc-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="c25cc-120">Debugging Interfaces</span></span>](debugging-interfaces.md)

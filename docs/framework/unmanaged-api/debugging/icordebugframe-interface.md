---
description: 了解详细信息： ICorDebugFrame 接口
title: ICorDebugFrame 接口
ms.date: 03/30/2017
api_name:
- ICorDebugFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame
helpviewer_keywords:
- ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 0c48f764-3c64-4602-b2f4-4ffc60eb2c65
topic_type:
- apiref
ms.openlocfilehash: d0fd629672d535f89fe78c178032937443d9dfbd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692844"
---
# <a name="icordebugframe-interface"></a><span data-ttu-id="ee052-103">ICorDebugFrame 接口</span><span class="sxs-lookup"><span data-stu-id="ee052-103">ICorDebugFrame Interface</span></span>

<span data-ttu-id="ee052-104">表示当前堆栈上的帧。</span><span class="sxs-lookup"><span data-stu-id="ee052-104">Represents a frame on the current stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ee052-105">方法</span><span class="sxs-lookup"><span data-stu-id="ee052-105">Methods</span></span>  
  
|<span data-ttu-id="ee052-106">方法</span><span class="sxs-lookup"><span data-stu-id="ee052-106">Method</span></span>|<span data-ttu-id="ee052-107">说明</span><span class="sxs-lookup"><span data-stu-id="ee052-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ee052-108">CreateStepper 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-108">CreateStepper Method</span></span>](icordebugframe-createstepper-method.md)|<span data-ttu-id="ee052-109">获取用于执行与此相关的单步执行操作的 ICorDebugStepper `ICorDebugFrame` 。</span><span class="sxs-lookup"><span data-stu-id="ee052-109">Gets an ICorDebugStepper to perform stepping operations relative to this `ICorDebugFrame`.</span></span>|  
|[<span data-ttu-id="ee052-110">GetCallee 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-110">GetCallee Method</span></span>](icordebugframe-getcallee-method.md)|<span data-ttu-id="ee052-111">获取一个指针，该指针指向 `ICorDebugFrame` 此框架调用的当前链中的，如果这是链中的最内层帧，则返回 null。</span><span class="sxs-lookup"><span data-stu-id="ee052-111">Gets a pointer to the `ICorDebugFrame` in the current chain that this frame called, or returns null if this is the innermost frame in the chain.</span></span>|  
|[<span data-ttu-id="ee052-112">GetCaller 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-112">GetCaller Method</span></span>](icordebugframe-getcaller-method.md)|<span data-ttu-id="ee052-113">获取指向 `ICorDebugFrame` 当前链中调用此帧的的指针，如果这是链中最外层的帧，则返回 null。</span><span class="sxs-lookup"><span data-stu-id="ee052-113">Gets a pointer to the `ICorDebugFrame` in the current chain that called this frame, or returns null if this is the outermost frame in the chain.</span></span>|  
|[<span data-ttu-id="ee052-114">GetChain 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-114">GetChain Method</span></span>](icordebugframe-getchain-method.md)|<span data-ttu-id="ee052-115">获取一个指针，该指针指向作为的一部分的 ICorDebugChain `ICorDebugFrame` 。</span><span class="sxs-lookup"><span data-stu-id="ee052-115">Gets a pointer to the ICorDebugChain this `ICorDebugFrame` is a part of.</span></span>|  
|[<span data-ttu-id="ee052-116">GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-116">GetCode Method</span></span>](icordebugframe-getcode-method.md)|<span data-ttu-id="ee052-117">获取一个指针，该指针指向与此堆栈帧关联的 ICorDebugCode。</span><span class="sxs-lookup"><span data-stu-id="ee052-117">Gets a pointer to the ICorDebugCode associated with this stack frame.</span></span>|  
|[<span data-ttu-id="ee052-118">GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-118">GetFunction Method</span></span>](icordebugframe-getfunction-method.md)|<span data-ttu-id="ee052-119">获取一个指向 ICorDebugFunction 的指针，该指针包含与此堆栈帧关联的代码。</span><span class="sxs-lookup"><span data-stu-id="ee052-119">Gets a pointer to the ICorDebugFunction that contains the code associated with this stack frame.</span></span>|  
|[<span data-ttu-id="ee052-120">GetFunctionToken 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-120">GetFunctionToken Method</span></span>](icordebugframe-getfunctiontoken-method.md)|<span data-ttu-id="ee052-121">获取包含与此堆栈帧关联的代码的函数的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ee052-121">Gets the metadata token for the function that contains the code associated with this stack frame.</span></span>|  
|[<span data-ttu-id="ee052-122">GetStackRange 方法</span><span class="sxs-lookup"><span data-stu-id="ee052-122">GetStackRange Method</span></span>](icordebugframe-getstackrange-method.md)|<span data-ttu-id="ee052-123">获取此所表示的堆栈帧的绝对地址范围 `ICorDebugFrame` 。</span><span class="sxs-lookup"><span data-stu-id="ee052-123">Gets the absolute address range of the stack frame represented by this `ICorDebugFrame`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ee052-124">备注</span><span class="sxs-lookup"><span data-stu-id="ee052-124">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ee052-125">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="ee052-125">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ee052-126">要求</span><span class="sxs-lookup"><span data-stu-id="ee052-126">Requirements</span></span>  

 <span data-ttu-id="ee052-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ee052-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee052-128">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ee052-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ee052-129">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee052-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee052-130">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee052-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee052-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee052-131">See also</span></span>

- [<span data-ttu-id="ee052-132">调试接口</span><span class="sxs-lookup"><span data-stu-id="ee052-132">Debugging Interfaces</span></span>](debugging-interfaces.md)

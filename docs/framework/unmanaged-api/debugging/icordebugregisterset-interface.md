---
description: 了解详细信息： ICorDebugRegisterSet 接口
title: ICorDebugRegisterSet 接口
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet
helpviewer_keywords:
- ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: d3d9676d-0b87-4bc3-b679-7bbc7a186c88
topic_type:
- apiref
ms.openlocfilehash: 7d888e9e395e9f5fa88c6a6d96b2b8e3171ef4ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690777"
---
# <a name="icordebugregisterset-interface"></a><span data-ttu-id="4cb3b-103">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="4cb3b-103">ICorDebugRegisterSet Interface</span></span>

<span data-ttu-id="4cb3b-104">表示在当前正在执行代码的计算机上可用的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-104">Represents the set of registers available on the computer that is currently executing code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4cb3b-105">方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-105">Methods</span></span>  
  
|<span data-ttu-id="4cb3b-106">方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-106">Method</span></span>|<span data-ttu-id="4cb3b-107">说明</span><span class="sxs-lookup"><span data-stu-id="4cb3b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4cb3b-108">GetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-108">GetRegisters Method</span></span>](icordebugregisterset-getregisters-method.md)|<span data-ttu-id="4cb3b-109">获取计算机上每个寄存器 (的值，该计算机当前正在执行位掩码指定的代码) 。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-109">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="4cb3b-110">GetRegistersAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-110">GetRegistersAvailable Method</span></span>](icordebugregisterset-getregistersavailable-method.md)|<span data-ttu-id="4cb3b-111">获取一个位掩码，指示此中的哪些寄存器 `ICorDebugRegisterSet` 当前可用。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-111">Gets a bit mask indicating which registers in this `ICorDebugRegisterSet` are currently available.</span></span>|  
|[<span data-ttu-id="4cb3b-112">GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-112">GetThreadContext Method</span></span>](icordebugregisterset-getthreadcontext-method.md)|<span data-ttu-id="4cb3b-113">获取当前线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-113">Gets the context of the current thread.</span></span>|  
|[<span data-ttu-id="4cb3b-114">SetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-114">SetRegisters Method</span></span>](icordebugregisterset-setregisters-method.md)|<span data-ttu-id="4cb3b-115">未实现 .NET Framework 版本2.0。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-115">Not implemented for the .NET Framework version 2.0.</span></span>|  
|[<span data-ttu-id="4cb3b-116">SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="4cb3b-116">SetThreadContext Method</span></span>](icordebugregisterset-setthreadcontext-method.md)|<span data-ttu-id="4cb3b-117">未实现 2.0 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-117">Not implemented for the .NET Framework 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4cb3b-118">备注</span><span class="sxs-lookup"><span data-stu-id="4cb3b-118">Remarks</span></span>  

 <span data-ttu-id="4cb3b-119">`ICorDebugRegisterSet`接口仅支持32位寄存器。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-119">The `ICorDebugRegisterSet` interface supports only 32-bit registers.</span></span> <span data-ttu-id="4cb3b-120">使用需要额外注册的平台（如 IA-64）上的 [ICorDebugRegisterSet2](icordebugregisterset2-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-120">Use the [ICorDebugRegisterSet2](icordebugregisterset2-interface.md) interface on platforms such as IA-64 that require additional registers.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="4cb3b-121">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4cb3b-122">要求</span><span class="sxs-lookup"><span data-stu-id="4cb3b-122">Requirements</span></span>  

 <span data-ttu-id="4cb3b-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4cb3b-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4cb3b-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4cb3b-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4cb3b-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4cb3b-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4cb3b-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4cb3b-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cb3b-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="4cb3b-127">See also</span></span>

- [<span data-ttu-id="4cb3b-128">调试接口</span><span class="sxs-lookup"><span data-stu-id="4cb3b-128">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="4cb3b-129">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="4cb3b-129">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)

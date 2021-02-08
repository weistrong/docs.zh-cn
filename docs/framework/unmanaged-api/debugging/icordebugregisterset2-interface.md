---
description: 了解详细信息： ICorDebugRegisterSet2 接口
title: ICorDebugRegisterSet2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet2
helpviewer_keywords:
- ICorDebugRegisterSet2 interface [.NET Framework debugging]
ms.assetid: d7fbccbf-3b6b-4db8-a96d-768e1cb6b1a6
topic_type:
- apiref
ms.openlocfilehash: 3501325df188879f5687347ef329f490b487d9d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803602"
---
# <a name="icordebugregisterset2-interface"></a><span data-ttu-id="64fe6-103">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="64fe6-103">ICorDebugRegisterSet2 Interface</span></span>

<span data-ttu-id="64fe6-104">为包含64个以上注册的硬件平台扩展了 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 接口的功能。</span><span class="sxs-lookup"><span data-stu-id="64fe6-104">Extends the capabilities of the [ICorDebugRegisterSet](icordebugregisterset-interface.md) interface for hardware platforms that have more than 64 registers.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="64fe6-105">方法</span><span class="sxs-lookup"><span data-stu-id="64fe6-105">Methods</span></span>  
  
|<span data-ttu-id="64fe6-106">方法</span><span class="sxs-lookup"><span data-stu-id="64fe6-106">Method</span></span>|<span data-ttu-id="64fe6-107">说明</span><span class="sxs-lookup"><span data-stu-id="64fe6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="64fe6-108">GetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="64fe6-108">GetRegisters Method</span></span>](icordebugregisterset2-getregisters-method.md)|<span data-ttu-id="64fe6-109">获取计算机上每个寄存器 (的值，该计算机当前正在执行位掩码指定的代码) 。</span><span class="sxs-lookup"><span data-stu-id="64fe6-109">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="64fe6-110">GetRegistersAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="64fe6-110">GetRegistersAvailable Method</span></span>](icordebugregisterset2-getregistersavailable-method.md)|<span data-ttu-id="64fe6-111">获取提供可用寄存器的位图的字节数组。</span><span class="sxs-lookup"><span data-stu-id="64fe6-111">Gets an array of bytes that provides a bitmap of the available registers.</span></span>|  
|[<span data-ttu-id="64fe6-112">SetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="64fe6-112">SetRegisters Method</span></span>](icordebugregisterset2-setregisters-method.md)|<span data-ttu-id="64fe6-113">在 .NET Framework 版本2.0 中未实现。</span><span class="sxs-lookup"><span data-stu-id="64fe6-113">Not implemented in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64fe6-114">备注</span><span class="sxs-lookup"><span data-stu-id="64fe6-114">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="64fe6-115">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="64fe6-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64fe6-116">要求</span><span class="sxs-lookup"><span data-stu-id="64fe6-116">Requirements</span></span>  

 <span data-ttu-id="64fe6-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="64fe6-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64fe6-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="64fe6-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="64fe6-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="64fe6-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="64fe6-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64fe6-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64fe6-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="64fe6-121">See also</span></span>

- [<span data-ttu-id="64fe6-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="64fe6-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="64fe6-123">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="64fe6-123">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)

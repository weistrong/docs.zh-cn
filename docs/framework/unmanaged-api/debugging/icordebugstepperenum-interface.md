---
description: 了解详细信息： ICorDebugStepperEnum 接口
title: ICorDebugStepperEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum
helpviewer_keywords:
- ICorDebugStepperEnum interface [.NET Framework debugging]
ms.assetid: 988718c1-1a4a-40f2-a04c-7d67e5cfe1e2
topic_type:
- apiref
ms.openlocfilehash: d645b20d54af6898afe00d19029747f9d53cdbe4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717519"
---
# <a name="icordebugstepperenum-interface"></a><span data-ttu-id="51304-103">ICorDebugStepperEnum 接口</span><span class="sxs-lookup"><span data-stu-id="51304-103">ICorDebugStepperEnum Interface</span></span>

<span data-ttu-id="51304-104">实现 ICorDebugEnum 方法，并枚举 ICorDebugStepper 数组。</span><span class="sxs-lookup"><span data-stu-id="51304-104">Implements ICorDebugEnum methods, and enumerates ICorDebugStepper arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="51304-105">方法</span><span class="sxs-lookup"><span data-stu-id="51304-105">Methods</span></span>  
  
|<span data-ttu-id="51304-106">方法</span><span class="sxs-lookup"><span data-stu-id="51304-106">Method</span></span>|<span data-ttu-id="51304-107">说明</span><span class="sxs-lookup"><span data-stu-id="51304-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="51304-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="51304-108">Next Method</span></span>](icordebugstepperenum-next-method.md)|<span data-ttu-id="51304-109">`ICorDebugStepper`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="51304-109">Gets the specified number of `ICorDebugStepper` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="51304-110">备注</span><span class="sxs-lookup"><span data-stu-id="51304-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="51304-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="51304-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51304-112">要求</span><span class="sxs-lookup"><span data-stu-id="51304-112">Requirements</span></span>  

 <span data-ttu-id="51304-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="51304-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="51304-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="51304-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="51304-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="51304-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="51304-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="51304-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51304-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="51304-117">See also</span></span>

- [<span data-ttu-id="51304-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="51304-118">Debugging Interfaces</span></span>](debugging-interfaces.md)

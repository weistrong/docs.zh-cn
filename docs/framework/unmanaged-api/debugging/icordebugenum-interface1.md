---
description: 了解详细信息： ICorDebugEnum 接口
title: ICorDebugEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum
helpviewer_keywords:
- ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 80be7efe-2c32-4b9f-8c52-40c6f6268219
topic_type:
- apiref
ms.openlocfilehash: 20d2bb14bddcaf40802567ec78a8e318ac1db380
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694469"
---
# <a name="icordebugenum-interface"></a><span data-ttu-id="7130a-103">ICorDebugEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7130a-103">ICorDebugEnum Interface</span></span>

<span data-ttu-id="7130a-104">用作调试应用程序所使用的枚举器的抽象基接口。</span><span class="sxs-lookup"><span data-stu-id="7130a-104">Serves as the abstract base interface for the enumerators that are used by a debugging application.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7130a-105">方法</span><span class="sxs-lookup"><span data-stu-id="7130a-105">Methods</span></span>  
  
|<span data-ttu-id="7130a-106">方法</span><span class="sxs-lookup"><span data-stu-id="7130a-106">Method</span></span>|<span data-ttu-id="7130a-107">说明</span><span class="sxs-lookup"><span data-stu-id="7130a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7130a-108">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="7130a-108">Clone Method</span></span>](icordebugenum-clone-method.md)|<span data-ttu-id="7130a-109">创建此 `ICorDebugEnum` 对象的一个副本。</span><span class="sxs-lookup"><span data-stu-id="7130a-109">Creates a copy of this `ICorDebugEnum` object.</span></span>|  
|[<span data-ttu-id="7130a-110">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="7130a-110">GetCount Method</span></span>](icordebugenum-getcount-method.md)|<span data-ttu-id="7130a-111">获取枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="7130a-111">Gets the number of items in the enumeration.</span></span>|  
|[<span data-ttu-id="7130a-112">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="7130a-112">Reset Method</span></span>](icordebugenum-reset-method.md)|<span data-ttu-id="7130a-113">将光标移到枚举的开头。</span><span class="sxs-lookup"><span data-stu-id="7130a-113">Moves the cursor to the beginning of the enumeration.</span></span>|  
|[<span data-ttu-id="7130a-114">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="7130a-114">Skip Method</span></span>](icordebugenum-skip-method.md)|<span data-ttu-id="7130a-115">按指定的项数在枚举中向前移动光标。</span><span class="sxs-lookup"><span data-stu-id="7130a-115">Moves the cursor forward in the enumeration by the specified number of items.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7130a-116">备注</span><span class="sxs-lookup"><span data-stu-id="7130a-116">Remarks</span></span>  

 <span data-ttu-id="7130a-117">以下枚举器派生自 `ICorDebugEnum` ：</span><span class="sxs-lookup"><span data-stu-id="7130a-117">The following enumerators derive from `ICorDebugEnum`:</span></span>  
  
- <span data-ttu-id="7130a-118">ICorDebugAppDomainEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-118">"ICorDebugAppDomainEnum"</span></span>  
  
- <span data-ttu-id="7130a-119">ICorDebugAssemblyEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-119">"ICorDebugAssemblyEnum"</span></span>  
  
- [<span data-ttu-id="7130a-120">ICorDebugBlockingObjectEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-120">ICorDebugBlockingObjectEnum</span></span>](icordebugblockingobjectenum-interface.md)  
  
- <span data-ttu-id="7130a-121">ICorDebugBreakpointEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-121">"ICorDebugBreakpointEnum"</span></span>  
  
- <span data-ttu-id="7130a-122">ICorDebugChainEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-122">"ICorDebugChainEnum"</span></span>  
  
- <span data-ttu-id="7130a-123">ICorDebugCodeEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-123">"ICorDebugCodeEnum"</span></span>  
  
- <span data-ttu-id="7130a-124">ICorDebugErrorInfoEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-124">"ICorDebugErrorInfoEnum"</span></span>  
  
- [<span data-ttu-id="7130a-125">ICorDebugExceptionObjectCallStackEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-125">ICorDebugExceptionObjectCallStackEnum</span></span>](icordebugexceptionobjectcallstackenum-interface.md)  
  
- <span data-ttu-id="7130a-126">ICorDebugFrameEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-126">"ICorDebugFrameEnum"</span></span>  
  
- [<span data-ttu-id="7130a-127">ICorDebugGCReferenceEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-127">ICorDebugGCReferenceEnum</span></span>](icordebuggcreferenceenum-interface.md)  
  
- [<span data-ttu-id="7130a-128">ICorDebugGuidToTypeEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-128">ICorDebugGuidToTypeEnum</span></span>](icordebugguidtotypeenum-interface.md)  
  
- [<span data-ttu-id="7130a-129">ICorDebugHeapEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-129">ICorDebugHeapEnum</span></span>](icordebugheapenum-interface.md)  
  
- [<span data-ttu-id="7130a-130">ICorDebugHeapSegmentEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-130">ICorDebugHeapSegmentEnum</span></span>](icordebugheapsegmentenum-interface.md)  
  
- <span data-ttu-id="7130a-131">ICorDebugModuleEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-131">"ICorDebugModuleEnum"</span></span>  
  
- <span data-ttu-id="7130a-132">ICorDebugObjectEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-132">"ICorDebugObjectEnum"</span></span>  
  
- <span data-ttu-id="7130a-133">ICorDebugProcessEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-133">"ICorDebugProcessEnum"</span></span>  
  
- <span data-ttu-id="7130a-134">ICorDebugStepperEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-134">"ICorDebugStepperEnum"</span></span>  
  
- <span data-ttu-id="7130a-135">ICorDebugThreadEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-135">"ICorDebugThreadEnum"</span></span>  
  
- <span data-ttu-id="7130a-136">ICorDebugTypeEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-136">"ICorDebugTypeEnum"</span></span>  
  
- <span data-ttu-id="7130a-137">ICorDebugValueEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-137">"ICorDebugValueEnum"</span></span>  
  
- [<span data-ttu-id="7130a-138">ICorDebugVariableHomeEnum</span><span class="sxs-lookup"><span data-stu-id="7130a-138">ICorDebugVariableHomeEnum</span></span>](icordebugvariablehomeenum-interface.md)  
  
> [!NOTE]
> <span data-ttu-id="7130a-139">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="7130a-139">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7130a-140">要求</span><span class="sxs-lookup"><span data-stu-id="7130a-140">Requirements</span></span>  

 <span data-ttu-id="7130a-141">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7130a-141">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7130a-142">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7130a-142">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7130a-143">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7130a-143">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7130a-144">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7130a-144">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7130a-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="7130a-145">See also</span></span>

- [<span data-ttu-id="7130a-146">调试接口</span><span class="sxs-lookup"><span data-stu-id="7130a-146">Debugging Interfaces</span></span>](debugging-interfaces.md)

---
description: 了解详细信息： ICorDebugStepper：： SetInterceptMask 方法
title: ICorDebugStepper::SetInterceptMask 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.SetInterceptMask
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::SetInterceptMask
helpviewer_keywords:
- SetInterceptMask method [.NET Framework debugging]
- ICorDebugStepper::SetInterceptMask method [.NET Framework debugging]
ms.assetid: 6245e2ae-5cc2-43ff-8cc1-71953d12113a
topic_type:
- apiref
ms.openlocfilehash: 33a42b154d063a29022034fd8061599a5e0e5503
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803537"
---
# <a name="icordebugsteppersetinterceptmask-method"></a><span data-ttu-id="a2752-103">ICorDebugStepper::SetInterceptMask 方法</span><span class="sxs-lookup"><span data-stu-id="a2752-103">ICorDebugStepper::SetInterceptMask Method</span></span>

<span data-ttu-id="a2752-104">设置一个值，该值指定要单步执行的代码的类型。</span><span class="sxs-lookup"><span data-stu-id="a2752-104">Sets a value that specifies the types of code that are stepped into.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2752-105">语法</span><span class="sxs-lookup"><span data-stu-id="a2752-105">Syntax</span></span>  
  
```cpp  
HRESULT SetInterceptMask (  
    [in] CorDebugIntercept    mask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a2752-106">参数</span><span class="sxs-lookup"><span data-stu-id="a2752-106">Parameters</span></span>  

 `mask`  
 <span data-ttu-id="a2752-107">中CorDebugIntercept 枚举的值的组合，用于指定代码的类型。</span><span class="sxs-lookup"><span data-stu-id="a2752-107">[in] A combination of values of the CorDebugIntercept enumeration that specifies the types of code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a2752-108">备注</span><span class="sxs-lookup"><span data-stu-id="a2752-108">Remarks</span></span>  

 <span data-ttu-id="a2752-109">如果设置了侦听器的位，则遇到给定类型的截取代码时，分档器将完成。</span><span class="sxs-lookup"><span data-stu-id="a2752-109">If the bit for an interceptor is set, the stepper will complete when the given type of intercepting code is encountered.</span></span> <span data-ttu-id="a2752-110">如果清除该位，则将跳过拦截代码。</span><span class="sxs-lookup"><span data-stu-id="a2752-110">If the bit is cleared, the intercepting code will be skipped.</span></span>  
  
 <span data-ttu-id="a2752-111">此 `SetInterceptMask` 方法可能与 [ICorDebugStepper：： SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) (从用户的观点) 交互。</span><span class="sxs-lookup"><span data-stu-id="a2752-111">The `SetInterceptMask` method may have unforeseen interactions with [ICorDebugStepper::SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) (from the user's point of view).</span></span> <span data-ttu-id="a2752-112">例如，如果唯一可见的 (是：类初始化代码的非内部) 部分缺少映射信息，并且未设置 STOP_NO_MAPPING_INFO (参见 [ICorDebugStepper：： SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) 方法和 CorDebugUnmappedStop 枚举) ，则分档器将逐过程执行类初始化。</span><span class="sxs-lookup"><span data-stu-id="a2752-112">For example, if the only visible (that is, non-internal) portion of class initialization code lacks mapping information and STOP_NO_MAPPING_INFO isn't set (see the [ICorDebugStepper::SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) method and the CorDebugUnmappedStop enumeration), the stepper will step over the class initialization.</span></span> <span data-ttu-id="a2752-113">默认情况下，将只使用枚举的 INTERCEPT_NONE 值 `CorDebugIntercept` 。</span><span class="sxs-lookup"><span data-stu-id="a2752-113">By default, only the INTERCEPT_NONE value of the `CorDebugIntercept` enumeration will be used.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2752-114">要求</span><span class="sxs-lookup"><span data-stu-id="a2752-114">Requirements</span></span>  

 <span data-ttu-id="a2752-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a2752-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2752-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a2752-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a2752-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a2752-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a2752-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2752-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

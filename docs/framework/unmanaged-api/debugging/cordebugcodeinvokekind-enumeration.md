---
description: 了解详细信息： CorDebugCodeInvokeKind 枚举
title: “Cor调试代码调用类型”枚举
ms.date: 03/30/2017
api_name:
- CorDebugCodeInvokeKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: e795e6a2-1008-4a81-af88-d777888e942e
topic_type:
- apiref
ms.openlocfilehash: d3fc3fe6f7568adcb2d1bbbe18c98d9d84bac337
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747083"
---
# <a name="cordebugcodeinvokekind-enumeration"></a><span data-ttu-id="c7a14-103">“Cor调试代码调用类型”枚举</span><span class="sxs-lookup"><span data-stu-id="c7a14-103">CorDebugCodeInvokeKind Enumeration</span></span>

<span data-ttu-id="c7a14-104">描述导出函数如何调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="c7a14-104">Describes how an exported function invokes managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7a14-105">语法</span><span class="sxs-lookup"><span data-stu-id="c7a14-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugCodeInvokeKind  
{  
    CODE_INVOKE_KIND_NONE,
    CODE_INVOKE_KIND_RETURN,
    CODE_INVOKE_KIND_TAILCALL,
} CorDebugCodeInvokeKind;  
```  
  
## <a name="members"></a><span data-ttu-id="c7a14-106">成员</span><span class="sxs-lookup"><span data-stu-id="c7a14-106">Members</span></span>  
  
|<span data-ttu-id="c7a14-107">成员</span><span class="sxs-lookup"><span data-stu-id="c7a14-107">Member</span></span>|<span data-ttu-id="c7a14-108">说明</span><span class="sxs-lookup"><span data-stu-id="c7a14-108">Description</span></span>|  
|------------|-----------------|  
|`CODE_INVOKE_KIND_NONE`|<span data-ttu-id="c7a14-109">如果任何托管代码遭该方法调用，稍后将必须接受显式事件或断点定位。</span><span class="sxs-lookup"><span data-stu-id="c7a14-109">If any managed code is invoked by this method, it will have to be located by explicit events or breakpoints later.</span></span><br /><br /> <span data-ttu-id="c7a14-110">--或者--</span><span class="sxs-lookup"><span data-stu-id="c7a14-110">--or--</span></span><br /><br /> <span data-ttu-id="c7a14-111">我们或许只能错过该方法调用的一些托管代码，因为很难停在上面。</span><span class="sxs-lookup"><span data-stu-id="c7a14-111">We may just miss some of the managed code this method calls because there is no easy way to stop on it.</span></span><br /><br /> <span data-ttu-id="c7a14-112">--或者--</span><span class="sxs-lookup"><span data-stu-id="c7a14-112">--or--</span></span><br /><br /> <span data-ttu-id="c7a14-113">该方法可能无法调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="c7a14-113">The method may never invoke managed code.</span></span>|  
|`CODE_INVOKE_KIND_RETURN`|<span data-ttu-id="c7a14-114">该方法可通过返回指令调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="c7a14-114">This method will invoke managed code via a return instruction.</span></span> <span data-ttu-id="c7a14-115">在下一个托管代码处应跳出。</span><span class="sxs-lookup"><span data-stu-id="c7a14-115">Stepping out should arrive at the next managed code.</span></span>|  
|`CODE_INVOKE_KIND_TAILCALL`|<span data-ttu-id="c7a14-116">该方法可通过尾调调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="c7a14-116">This method will invoke managed code via a tail-call.</span></span> <span data-ttu-id="c7a14-117">在托管代码处应单步执行所有调用指令。</span><span class="sxs-lookup"><span data-stu-id="c7a14-117">Single-stepping and stepping over any call instructions should arrive at managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c7a14-118">备注</span><span class="sxs-lookup"><span data-stu-id="c7a14-118">Remarks</span></span>  

 <span data-ttu-id="c7a14-119">此枚举由 [ICorDebugProcess6：： GetExportStepInfo](icordebugprocess6-getexportstepinfo-method.md) 方法用来提供有关单步执行托管代码的信息。</span><span class="sxs-lookup"><span data-stu-id="c7a14-119">This enumeration is used by the [ICorDebugProcess6::GetExportStepInfo](icordebugprocess6-getexportstepinfo-method.md) method to provide information about stepping through managed code.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c7a14-120">此枚举仅用于 .NET Native 调试方案。</span><span class="sxs-lookup"><span data-stu-id="c7a14-120">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7a14-121">要求</span><span class="sxs-lookup"><span data-stu-id="c7a14-121">Requirements</span></span>  

 <span data-ttu-id="c7a14-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a14-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7a14-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7a14-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7a14-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7a14-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7a14-125">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7a14-125">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7a14-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7a14-126">See also</span></span>

- [<span data-ttu-id="c7a14-127">调试枚举</span><span class="sxs-lookup"><span data-stu-id="c7a14-127">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="c7a14-128">调试</span><span class="sxs-lookup"><span data-stu-id="c7a14-128">Debugging</span></span>](index.md)

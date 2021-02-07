---
description: 了解详细信息： ICorDebugDebugEvent 接口
title: “ICor调试调试事件”接口
ms.date: 03/30/2017
ms.assetid: a226737a-cb99-4e97-bd94-9a37094ded41
ms.openlocfilehash: 5735be22b76e9f74847bb5138c00130f28dbfc96
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764302"
---
# <a name="icordebugdebugevent-interface"></a><span data-ttu-id="368b3-103">“ICor调试调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="368b3-103">ICorDebugDebugEvent Interface</span></span>

<span data-ttu-id="368b3-104">定义所有 `ICorDebug` 调试事件派生的基接口。</span><span class="sxs-lookup"><span data-stu-id="368b3-104">Defines the base interface from which all `ICorDebug` debug events derive.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="368b3-105">方法</span><span class="sxs-lookup"><span data-stu-id="368b3-105">Methods</span></span>  
  
|<span data-ttu-id="368b3-106">方法</span><span class="sxs-lookup"><span data-stu-id="368b3-106">Method</span></span>|<span data-ttu-id="368b3-107">说明</span><span class="sxs-lookup"><span data-stu-id="368b3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="368b3-108">GetEventKind 方法</span><span class="sxs-lookup"><span data-stu-id="368b3-108">GetEventKind Method</span></span>](icordebugdebugevent-geteventkind-method.md)|<span data-ttu-id="368b3-109">指出该 `ICorDebugDebugEvent` 对象代表的事件类型。</span><span class="sxs-lookup"><span data-stu-id="368b3-109">Indicates what kind of event this `ICorDebugDebugEvent` object represents.</span></span>|  
|[<span data-ttu-id="368b3-110">GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="368b3-110">GetThread Method</span></span>](icordebugdebugevent-getthread-method.md)|<span data-ttu-id="368b3-111">获取发生事件的线程。</span><span class="sxs-lookup"><span data-stu-id="368b3-111">Gets the thread on which the event occurred.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="368b3-112">备注</span><span class="sxs-lookup"><span data-stu-id="368b3-112">Remarks</span></span>  

 <span data-ttu-id="368b3-113">以下接口派生自 `ICorDebugDebugEvent` 接口：</span><span class="sxs-lookup"><span data-stu-id="368b3-113">The following interfaces are derived from the `ICorDebugDebugEvent` interface:</span></span>  
  
- [<span data-ttu-id="368b3-114">ICorDebugExceptionDebugEvent</span><span class="sxs-lookup"><span data-stu-id="368b3-114">ICorDebugExceptionDebugEvent</span></span>](icordebugexceptiondebugevent-interface.md)  
  
- [<span data-ttu-id="368b3-115">ICorDebugModuleDebugEvent</span><span class="sxs-lookup"><span data-stu-id="368b3-115">ICorDebugModuleDebugEvent</span></span>](icordebugmoduledebugevent-interface.md)  
  
> [!NOTE]
> <span data-ttu-id="368b3-116">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="368b3-116">The interface is available with .NET Native only.</span></span> <span data-ttu-id="368b3-117">尝试调用 `QueryInterface` 来检索接口指针会为 .NET Native 外部的 ICorDebug 方案返回 `E_NOINTERFACE`。</span><span class="sxs-lookup"><span data-stu-id="368b3-117">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="368b3-118">要求</span><span class="sxs-lookup"><span data-stu-id="368b3-118">Requirements</span></span>  

 <span data-ttu-id="368b3-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="368b3-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="368b3-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="368b3-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="368b3-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="368b3-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="368b3-122">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="368b3-122">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="368b3-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="368b3-123">See also</span></span>

- [<span data-ttu-id="368b3-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="368b3-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="368b3-125">调试</span><span class="sxs-lookup"><span data-stu-id="368b3-125">Debugging</span></span>](index.md)

---
description: 了解详细信息： ICorDebugManagedCallback3 接口
title: ICorDebugManagedCallback3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback3
helpviewer_keywords:
- ICorDebugManagedCallback3 interface [.NET Framework debugging]
ms.assetid: a95389d3-cf2e-47a4-9805-61426acc6b65
topic_type:
- apiref
ms.openlocfilehash: 9fb3d44b1d793935ac997e8e4d8d86de4466f7b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801184"
---
# <a name="icordebugmanagedcallback3-interface"></a><span data-ttu-id="012bc-103">ICorDebugManagedCallback3 接口</span><span class="sxs-lookup"><span data-stu-id="012bc-103">ICorDebugManagedCallback3 Interface</span></span>

<span data-ttu-id="012bc-104">提供一个回调方法，该方法指示已发出启用的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="012bc-104">Provides a callback method that indicates that an enabled custom debugger notification has been raised.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="012bc-105">方法</span><span class="sxs-lookup"><span data-stu-id="012bc-105">Methods</span></span>  
  
|<span data-ttu-id="012bc-106">方法</span><span class="sxs-lookup"><span data-stu-id="012bc-106">Method</span></span>|<span data-ttu-id="012bc-107">说明</span><span class="sxs-lookup"><span data-stu-id="012bc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="012bc-108">CustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="012bc-108">CustomNotification Method</span></span>](icordebugmanagedcallback3-customnotification-method.md)|<span data-ttu-id="012bc-109">指示已引发启用的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="012bc-109">Indicates that an enabled custom debugger notification has been raised.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="012bc-110">备注</span><span class="sxs-lookup"><span data-stu-id="012bc-110">Remarks</span></span>  

 <span data-ttu-id="012bc-111">此接口是 [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) 和 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="012bc-111">This interface is a logical extension of the [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) and [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="012bc-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="012bc-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="012bc-113">要求</span><span class="sxs-lookup"><span data-stu-id="012bc-113">Requirements</span></span>  

 <span data-ttu-id="012bc-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="012bc-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="012bc-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="012bc-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="012bc-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="012bc-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="012bc-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="012bc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="012bc-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="012bc-118">See also</span></span>

- [<span data-ttu-id="012bc-119">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="012bc-119">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
- [<span data-ttu-id="012bc-120">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="012bc-120">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="012bc-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="012bc-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="012bc-122">调试</span><span class="sxs-lookup"><span data-stu-id="012bc-122">Debugging</span></span>](index.md)

---
description: 了解详细信息： ICorDebug：： SetUnmanagedHandler 方法
title: ICorDebug::SetUnmanagedHandler 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.SetUnmanagedHandler
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::SetUnmanagerHandler
helpviewer_keywords:
- SetUnmanagedHandler method [.NET Framework debugging]
- ICorDebug::SetUnmanagedHandler method [.NET Framework debugging]
ms.assetid: 6b546be4-f86d-4536-8cfc-1d08e5066eb6
topic_type:
- apiref
ms.openlocfilehash: ffd4eb7ff0056a2468ec53eb3534434c2c8d556a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754311"
---
# <a name="icordebugsetunmanagedhandler-method"></a><span data-ttu-id="5f879-103">ICorDebug::SetUnmanagedHandler 方法</span><span class="sxs-lookup"><span data-stu-id="5f879-103">ICorDebug::SetUnmanagedHandler Method</span></span>

<span data-ttu-id="5f879-104">指定非托管事件的事件处理程序对象。</span><span class="sxs-lookup"><span data-stu-id="5f879-104">Specifies the event handler object for unmanaged events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f879-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f879-105">Syntax</span></span>  
  
```cpp  
HRESULT SetUnmanagedHandler (  
    [in] ICorDebugUnmanagedCallback  *pCallback  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f879-106">参数</span><span class="sxs-lookup"><span data-stu-id="5f879-106">Parameters</span></span>  

 `pCallback`  
 <span data-ttu-id="5f879-107">中指向 [ICorDebugUnmanagedCallback](icordebugunmanagedcallback-interface.md) 对象的指针，该对象表示非托管事件的事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="5f879-107">[in] A pointer to an [ICorDebugUnmanagedCallback](icordebugunmanagedcallback-interface.md) object that represents the event handler for unmanaged events.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5f879-108">备注</span><span class="sxs-lookup"><span data-stu-id="5f879-108">Remarks</span></span>  

 <span data-ttu-id="5f879-109">非托管事件的事件处理程序对象必须在调用 [ICorDebug：： Initialize](icordebug-initialize-method.md) 之后以及对 [ICorDebug：： CreateProcess](icordebug-createprocess-method.md) 或 [ICorDebug：:D ebugactiveprocess](icordebug-debugactiveprocess-method.md)的任何调用之前设置。</span><span class="sxs-lookup"><span data-stu-id="5f879-109">The event handler object for unmanaged events must be set after a call to [ICorDebug::Initialize](icordebug-initialize-method.md) and before any calls to [ICorDebug::CreateProcess](icordebug-createprocess-method.md) or [ICorDebug::DebugActiveProcess](icordebug-debugactiveprocess-method.md).</span></span> <span data-ttu-id="5f879-110">但出于传统目的，在引发第一个本机调试事件之前，不需要为非托管事件设置事件处理程序对象。</span><span class="sxs-lookup"><span data-stu-id="5f879-110">However, for legacy purposes, you are not required to set the event handler object for unmanaged events until the first native debug event is raised.</span></span> <span data-ttu-id="5f879-111">具体来说，如果 `ICorDebug::CreateProcess` 已经设置了 CREATE_SUSPENDED 标志，则在主线程恢复之前，不能调度本机调试事件。</span><span class="sxs-lookup"><span data-stu-id="5f879-111">Specifically, if `ICorDebug::CreateProcess` has set the CREATE_SUSPENDED flag, native debug events cannot be dispatched until the main thread is resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f879-112">要求</span><span class="sxs-lookup"><span data-stu-id="5f879-112">Requirements</span></span>  

 <span data-ttu-id="5f879-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f879-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f879-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5f879-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5f879-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5f879-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5f879-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f879-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f879-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f879-117">See also</span></span>

- [<span data-ttu-id="5f879-118">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="5f879-118">ICorDebug Interface</span></span>](icordebug-interface.md)

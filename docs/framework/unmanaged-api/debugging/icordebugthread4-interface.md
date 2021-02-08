---
description: 了解详细信息： ICorDebugThread4 接口
title: ICorDebugThread4 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThread4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4
helpviewer_keywords:
- ICorDebugThread4 interface [.NET Framework debugging]
ms.assetid: a8c7719a-322b-4133-8566-4c27218dc104
topic_type:
- apiref
ms.openlocfilehash: 4ad587cee81ce635df0a8917b7a6d68e60aaf0b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800911"
---
# <a name="icordebugthread4-interface"></a><span data-ttu-id="1240c-103">ICorDebugThread4 接口</span><span class="sxs-lookup"><span data-stu-id="1240c-103">ICorDebugThread4 Interface</span></span>

<span data-ttu-id="1240c-104">提供线程阻塞信息。</span><span class="sxs-lookup"><span data-stu-id="1240c-104">Provides thread blocking information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1240c-105">方法</span><span class="sxs-lookup"><span data-stu-id="1240c-105">Methods</span></span>  
  
|<span data-ttu-id="1240c-106">方法</span><span class="sxs-lookup"><span data-stu-id="1240c-106">Method</span></span>|<span data-ttu-id="1240c-107">说明</span><span class="sxs-lookup"><span data-stu-id="1240c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1240c-108">GetBlockingObjects 方法</span><span class="sxs-lookup"><span data-stu-id="1240c-108">GetBlockingObjects Method</span></span>](icordebugthread4-getblockingobjects-method.md)|<span data-ttu-id="1240c-109">提供 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的有序枚举，这些结构提供线程阻塞信息。</span><span class="sxs-lookup"><span data-stu-id="1240c-109">Provides an ordered enumeration of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures that provide thread blocking information.</span></span>|  
|[<span data-ttu-id="1240c-110">HadUnhandledException 方法</span><span class="sxs-lookup"><span data-stu-id="1240c-110">HadUnhandledException Method</span></span>](icordebugthread4-hadunhandledexception-method.md)|<span data-ttu-id="1240c-111">指示线程是否曾经出现过未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="1240c-111">Indicates whether the thread has ever had an unhandled exception.</span></span>|  
|[<span data-ttu-id="1240c-112">GetCurrentCustomDebuggerNotification 方法</span><span class="sxs-lookup"><span data-stu-id="1240c-112">GetCurrentCustomDebuggerNotification Method</span></span>](icordebugthread4-getcurrentcustomdebuggernotification-method.md)|<span data-ttu-id="1240c-113">获取当前线程上的当前 [ICorDebugManagedCallback3：： CustomNotification](icordebugmanagedcallback3-customnotification-method.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="1240c-113">Gets the current [ICorDebugManagedCallback3::CustomNotification](icordebugmanagedcallback3-customnotification-method.md) object on the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1240c-114">备注</span><span class="sxs-lookup"><span data-stu-id="1240c-114">Remarks</span></span>  

 <span data-ttu-id="1240c-115">此接口是 ICorDebugThread、ICorDebugThread2 和 [ICorDebugThread3](icordebugthread3-interface.md) 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="1240c-115">This interface is a logical extension of the ICorDebugThread, ICorDebugThread2, and [ICorDebugThread3](icordebugthread3-interface.md) interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1240c-116">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="1240c-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1240c-117">要求</span><span class="sxs-lookup"><span data-stu-id="1240c-117">Requirements</span></span>  

 <span data-ttu-id="1240c-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1240c-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1240c-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1240c-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1240c-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1240c-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1240c-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1240c-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1240c-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="1240c-122">See also</span></span>

- [<span data-ttu-id="1240c-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="1240c-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="1240c-124">调试</span><span class="sxs-lookup"><span data-stu-id="1240c-124">Debugging</span></span>](index.md)

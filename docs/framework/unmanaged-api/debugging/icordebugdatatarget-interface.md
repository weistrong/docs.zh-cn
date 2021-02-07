---
description: 了解详细信息： ICorDebugDataTarget 接口
title: ICorDebugDataTarget 接口
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget
helpviewer_keywords:
- ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: df5f05be-bed7-4f3c-bc89-dbb435d79a0b
topic_type:
- apiref
ms.openlocfilehash: 34121b56080a8adc17543ce5716962c17c1a156d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764419"
---
# <a name="icordebugdatatarget-interface"></a><span data-ttu-id="3f187-103">ICorDebugDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="3f187-103">ICorDebugDataTarget Interface</span></span>

<span data-ttu-id="3f187-104">提供一个回调接口，该接口可提供对特定目标进程的访问。</span><span class="sxs-lookup"><span data-stu-id="3f187-104">Provides a callback interface that provides access to a particular target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3f187-105">方法</span><span class="sxs-lookup"><span data-stu-id="3f187-105">Methods</span></span>  
  
|<span data-ttu-id="3f187-106">方法</span><span class="sxs-lookup"><span data-stu-id="3f187-106">Method</span></span>|<span data-ttu-id="3f187-107">说明</span><span class="sxs-lookup"><span data-stu-id="3f187-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3f187-108">GetPlatform 方法</span><span class="sxs-lookup"><span data-stu-id="3f187-108">GetPlatform Method</span></span>](icordebugdatatarget-getplatform-method.md)|<span data-ttu-id="3f187-109">提供有关平台的信息，包括在其上运行目标进程的处理器体系结构和操作系统。</span><span class="sxs-lookup"><span data-stu-id="3f187-109">Provides information about the platform, including processor architecture and operating system, on which the target process is running.</span></span>|  
|[<span data-ttu-id="3f187-110">ReadVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="3f187-110">ReadVirtual Method</span></span>](icordebugdatatarget-readvirtual-method.md)|<span data-ttu-id="3f187-111">获取从指定地址开始的连续内存块，并将其返回到提供的缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="3f187-111">Gets a block of contiguous memory starting at the specified address, and returns it in the supplied buffer.</span></span>|  
|[<span data-ttu-id="3f187-112">GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="3f187-112">GetThreadContext Method</span></span>](icordebugdatatarget-getthreadcontext-method.md)|<span data-ttu-id="3f187-113">请求指定线程的当前线程上下文。</span><span class="sxs-lookup"><span data-stu-id="3f187-113">Requests the current thread context for the specified thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3f187-114">备注</span><span class="sxs-lookup"><span data-stu-id="3f187-114">Remarks</span></span>  

 <span data-ttu-id="3f187-115">`ICorDebugDataTarget` 及其方法具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="3f187-115">`ICorDebugDataTarget` and its methods have the following characteristics:</span></span>  
  
- <span data-ttu-id="3f187-116">调试服务调用此接口上的方法以访问目标进程中的内存和其他数据。</span><span class="sxs-lookup"><span data-stu-id="3f187-116">The debugging services call methods on this interface to access memory and other data in the target process.</span></span>  
  
- <span data-ttu-id="3f187-117">调试器客户端必须根据特定目标 (（例如，实时进程或内存转储) ）实现此接口。</span><span class="sxs-lookup"><span data-stu-id="3f187-117">The debugger client must implement this interface as appropriate for the particular target (for example, a live process or a memory dump).</span></span>  
  
- <span data-ttu-id="3f187-118">只能 `ICorDebugDataTarget` 从其他接口实现的方法中调用方法 `ICorDebug*` 。</span><span class="sxs-lookup"><span data-stu-id="3f187-118">The `ICorDebugDataTarget` methods can be invoked only from within methods implemented in other `ICorDebug*` interfaces.</span></span> <span data-ttu-id="3f187-119">这确保了调试器客户端可以控制调用它的线程和时间。</span><span class="sxs-lookup"><span data-stu-id="3f187-119">This ensures that the debugger client has control over which thread it is invoked on, and when.</span></span>  
  
- <span data-ttu-id="3f187-120">`ICorDebugDataTarget`实现必须始终返回有关目标的最新信息。</span><span class="sxs-lookup"><span data-stu-id="3f187-120">The `ICorDebugDataTarget` implementation must always return up-to-date information about the target.</span></span>  
  
 <span data-ttu-id="3f187-121">当 `ICorDebug*` 接口 (，因此调用) 的方法时，目标进程应停止并且不以任何方式更改 `ICorDebugDataTarget` 。</span><span class="sxs-lookup"><span data-stu-id="3f187-121">The target process should be stopped and not changed in any way while `ICorDebug*` interfaces (and therefore `ICorDebugDataTarget` methods) are being called.</span></span> <span data-ttu-id="3f187-122">如果目标是实时进程并且其状态发生更改，则必须再次调用 [ICLRDebugging：： OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) 方法以提供替换 ICorDebugProcess 实例。</span><span class="sxs-lookup"><span data-stu-id="3f187-122">If the target is a live process and its state changes, the [ICLRDebugging::OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) method has to be called again to provide a replacement ICorDebugProcess instance.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3f187-123">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3f187-123">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f187-124">要求</span><span class="sxs-lookup"><span data-stu-id="3f187-124">Requirements</span></span>  

 <span data-ttu-id="3f187-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f187-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f187-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3f187-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3f187-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3f187-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3f187-128">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f187-128">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f187-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f187-129">See also</span></span>

- [<span data-ttu-id="3f187-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="3f187-130">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="3f187-131">调试</span><span class="sxs-lookup"><span data-stu-id="3f187-131">Debugging</span></span>](index.md)

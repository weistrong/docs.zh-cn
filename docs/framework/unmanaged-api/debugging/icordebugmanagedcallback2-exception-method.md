---
description: 了解详细信息： ICorDebugManagedCallback2：： Exception 方法
title: ICorDebugManagedCallback2::Exception 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.Exception
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::Exception
helpviewer_keywords:
- ICorDebugManagedCallback2::Exception method [.NET Framework debugging]
- Exception method, ICorDebugManagedCallback2 interface [.NET Framework debugging]
ms.assetid: 78b0f14f-2fae-4e63-8412-4df119ee8468
topic_type:
- apiref
ms.openlocfilehash: 18fd4efcfbd1f13ce527b212d7450ba0d7651a3c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790875"
---
# <a name="icordebugmanagedcallback2exception-method"></a><span data-ttu-id="2911d-103">ICorDebugManagedCallback2::Exception 方法</span><span class="sxs-lookup"><span data-stu-id="2911d-103">ICorDebugManagedCallback2::Exception Method</span></span>

<span data-ttu-id="2911d-104">通知调试器已开始搜索异常处理程序。</span><span class="sxs-lookup"><span data-stu-id="2911d-104">Notifies the debugger that a search for an exception handler has started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2911d-105">语法</span><span class="sxs-lookup"><span data-stu-id="2911d-105">Syntax</span></span>  
  
```cpp  
HRESULT Exception (  
    [in] ICorDebugAppDomain   *pAppDomain,  
    [in] ICorDebugThread      *pThread,  
    [in] ICorDebugFrame       *pFrame,  
    [in] ULONG32              nOffset,  
    [in] CorDebugExceptionCallbackType dwEventType,  
    [in] DWORD                dwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2911d-106">参数</span><span class="sxs-lookup"><span data-stu-id="2911d-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="2911d-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含引发异常的线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="2911d-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the thread on which the exception was thrown.</span></span>  
  
 `pThread`  
 <span data-ttu-id="2911d-108">中指向 ICorDebugThread 对象的指针，该对象表示引发异常的线程。</span><span class="sxs-lookup"><span data-stu-id="2911d-108">[in] A pointer to an ICorDebugThread object that represents the thread on which the exception was thrown.</span></span>  
  
 `pFrame`  
 <span data-ttu-id="2911d-109">中指向 ICorDebugFrame 对象的指针，该对象表示由参数确定的帧 `dwEventType` 。</span><span class="sxs-lookup"><span data-stu-id="2911d-109">[in] A pointer to an ICorDebugFrame object that represents a frame, as determined by the `dwEventType` parameter.</span></span> <span data-ttu-id="2911d-110">有关详细信息，请参阅 "备注" 部分中的表。</span><span class="sxs-lookup"><span data-stu-id="2911d-110">For more information, see the table in the Remarks section.</span></span>  
  
 `nOffset`  
 <span data-ttu-id="2911d-111">中一个整数，指定由参数确定的偏移量 `dwEventType` 。</span><span class="sxs-lookup"><span data-stu-id="2911d-111">[in] An integer that specifies an offset, as determined by the `dwEventType` parameter.</span></span> <span data-ttu-id="2911d-112">有关详细信息，请参阅 "备注" 部分中的表。</span><span class="sxs-lookup"><span data-stu-id="2911d-112">For more information, see the table in the Remarks section.</span></span>  
  
 `dwEventType`  
 <span data-ttu-id="2911d-113">中CorDebugExceptionCallbackType 枚举的一个值，该值指定此异常回调的类型。</span><span class="sxs-lookup"><span data-stu-id="2911d-113">[in] A value of the CorDebugExceptionCallbackType enumeration that specifies the type of this exception callback.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="2911d-114">中 [CorDebugExceptionFlags](cordebugexceptionflags-enumeration.md) 枚举的一个值，该值指定有关异常的其他信息</span><span class="sxs-lookup"><span data-stu-id="2911d-114">[in] A value of the [CorDebugExceptionFlags](cordebugexceptionflags-enumeration.md) enumeration that specifies additional information about the exception</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2911d-115">备注</span><span class="sxs-lookup"><span data-stu-id="2911d-115">Remarks</span></span>  

 <span data-ttu-id="2911d-116">在 `Exception` 异常处理过程的搜索阶段，会在不同的点调用回调。</span><span class="sxs-lookup"><span data-stu-id="2911d-116">The `Exception` callback is called at various points during the search phase of the exception-handling process.</span></span> <span data-ttu-id="2911d-117">也就是说，可以在展开异常时多次调用它。</span><span class="sxs-lookup"><span data-stu-id="2911d-117">That is, it can be called more than once while unwinding an exception.</span></span>  
  
 <span data-ttu-id="2911d-118">可以从参数引用的 ICorDebugThread 对象中检索正在处理的异常 `pThread` 。</span><span class="sxs-lookup"><span data-stu-id="2911d-118">The exception being processed can be retrieved from the ICorDebugThread object referenced by the `pThread` parameter.</span></span>  
  
 <span data-ttu-id="2911d-119">特定的帧和偏移由参数确定， `dwEventType` 如下所示：</span><span class="sxs-lookup"><span data-stu-id="2911d-119">The particular frame and offset are determined by the `dwEventType` parameter as follows:</span></span>  
  
|<span data-ttu-id="2911d-120">`dwEventType` 的值</span><span class="sxs-lookup"><span data-stu-id="2911d-120">Value of `dwEventType`</span></span>|<span data-ttu-id="2911d-121">`pFrame` 的值</span><span class="sxs-lookup"><span data-stu-id="2911d-121">Value of `pFrame`</span></span>|<span data-ttu-id="2911d-122">`nOffset` 的值</span><span class="sxs-lookup"><span data-stu-id="2911d-122">Value of `nOffset`</span></span>|  
|----------------------------|-----------------------|------------------------|  
|<span data-ttu-id="2911d-123">DEBUG_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="2911d-123">DEBUG_EXCEPTION_FIRST_CHANCE</span></span>|<span data-ttu-id="2911d-124">引发异常的帧。</span><span class="sxs-lookup"><span data-stu-id="2911d-124">The frame that threw the exception.</span></span>|<span data-ttu-id="2911d-125">帧中的指令指针。</span><span class="sxs-lookup"><span data-stu-id="2911d-125">The instruction pointer in the frame.</span></span>|  
|<span data-ttu-id="2911d-126">DEBUG_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="2911d-126">DEBUG_EXCEPTION_USER_FIRST_CHANCE</span></span>|<span data-ttu-id="2911d-127">最接近引发的异常点的用户代码框架。</span><span class="sxs-lookup"><span data-stu-id="2911d-127">The user-code frame closest to the point of the thrown exception.</span></span>|<span data-ttu-id="2911d-128">帧中的指令指针。</span><span class="sxs-lookup"><span data-stu-id="2911d-128">The instruction pointer in the frame.</span></span>|  
|<span data-ttu-id="2911d-129">DEBUG_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="2911d-129">DEBUG_EXCEPTION_CATCH_HANDLER_FOUND</span></span>|<span data-ttu-id="2911d-130">包含 catch 处理程序的帧。</span><span class="sxs-lookup"><span data-stu-id="2911d-130">The frame that contains the catch handler.</span></span>|<span data-ttu-id="2911d-131">Microsoft 中间语言 (MSIL) catch 处理程序开头的偏移量。</span><span class="sxs-lookup"><span data-stu-id="2911d-131">The Microsoft intermediate language (MSIL) offset of the beginning of the catch handler.</span></span>|  
|<span data-ttu-id="2911d-132">DEBUG_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="2911d-132">DEBUG_EXCEPTION_UNHANDLED</span></span>|<span data-ttu-id="2911d-133">Null</span><span class="sxs-lookup"><span data-stu-id="2911d-133">NULL</span></span>|<span data-ttu-id="2911d-134">未定义。</span><span class="sxs-lookup"><span data-stu-id="2911d-134">Undefined.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2911d-135">要求</span><span class="sxs-lookup"><span data-stu-id="2911d-135">Requirements</span></span>  

 <span data-ttu-id="2911d-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2911d-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2911d-137">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2911d-137">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2911d-138">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2911d-138">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2911d-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2911d-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2911d-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="2911d-140">See also</span></span>

- [<span data-ttu-id="2911d-141">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="2911d-141">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="2911d-142">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="2911d-142">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)

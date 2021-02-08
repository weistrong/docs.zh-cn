---
description: 了解详细信息： IActionOnCLREvent：： OnEvent 方法
title: IActionOnCLREvent::OnEvent 方法
ms.date: 03/30/2017
api_name:
- IActionOnCLREvent.OnEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IActionOnCLREvent::OnEvent
helpviewer_keywords:
- OnEvent method [.NET Framework hosting]
- IActionOnCLREvent::OnEvent method [.NET Framework hosting]
ms.assetid: 0970f10c-4304-4c12-91c0-83e51455afb4
topic_type:
- apiref
ms.openlocfilehash: 163956ab319eb34d58da23d2c4ef2a6b592aab0d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785128"
---
# <a name="iactiononclreventonevent-method"></a><span data-ttu-id="a2a63-103">IActionOnCLREvent::OnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="a2a63-103">IActionOnCLREvent::OnEvent Method</span></span>

<span data-ttu-id="a2a63-104">对已使用 [ICLROnEventManager：： RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) 方法的调用注册的事件执行回调。</span><span class="sxs-lookup"><span data-stu-id="a2a63-104">Performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2a63-105">语法</span><span class="sxs-lookup"><span data-stu-id="a2a63-105">Syntax</span></span>  
  
```cpp  
HRESULT OnEvent (  
    [in] EClrEvent event,  
    [in] PVOID     data  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a2a63-106">参数</span><span class="sxs-lookup"><span data-stu-id="a2a63-106">Parameters</span></span>  

 `event`  
 <span data-ttu-id="a2a63-107">中 [EClrEvent](eclrevent-enumeration.md) 值之一，指示事件的类型。</span><span class="sxs-lookup"><span data-stu-id="a2a63-107">[in] One of the [EClrEvent](eclrevent-enumeration.md) values, which indicates the type of event.</span></span>  
  
 `data`  
 <span data-ttu-id="a2a63-108">中指向对象的指针，该对象包含有关的详细信息 `event` 。</span><span class="sxs-lookup"><span data-stu-id="a2a63-108">[in] A pointer to an object that contains details about `event`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a2a63-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a2a63-109">Return Value</span></span>  
  
|<span data-ttu-id="a2a63-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a2a63-110">HRESULT</span></span>|<span data-ttu-id="a2a63-111">说明</span><span class="sxs-lookup"><span data-stu-id="a2a63-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a2a63-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2a63-112">S_OK</span></span>|<span data-ttu-id="a2a63-113">`OnEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a2a63-113">`OnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="a2a63-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a2a63-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a2a63-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a2a63-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a2a63-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a2a63-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a2a63-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="a2a63-117">The call timed out.</span></span>|  
|<span data-ttu-id="a2a63-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a2a63-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a2a63-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a2a63-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a2a63-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a2a63-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a2a63-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="a2a63-121">An event was cancelled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a2a63-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a2a63-122">E_FAIL</span></span>|<span data-ttu-id="a2a63-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a2a63-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a2a63-124">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="a2a63-124">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a2a63-125">对任何宿主方法的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a2a63-125">Subsequent calls to any hosting method return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a2a63-126">备注</span><span class="sxs-lookup"><span data-stu-id="a2a63-126">Remarks</span></span>  

 <span data-ttu-id="a2a63-127">`data`参数是指向未指定类型的对象的指针。</span><span class="sxs-lookup"><span data-stu-id="a2a63-127">The `data` parameter is a pointer to an object of unspecified type.</span></span> <span data-ttu-id="a2a63-128">如果 `event` 参数为 `Event_DomainUnload` ， `data` 则是已卸载的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="a2a63-128">If the `event` parameter is `Event_DomainUnload`, `data` is the numeric identifier for the <xref:System.AppDomain> that was unloaded.</span></span> <span data-ttu-id="a2a63-129">主机可以使用此标识符作为键来执行适当的操作。</span><span class="sxs-lookup"><span data-stu-id="a2a63-129">The host can take appropriate action using this identifier as a key.</span></span>  
  
 <span data-ttu-id="a2a63-130">如果 `event` 为 `Event_MDAFired` ， `data` 则为指向 [MDAInfo](mdainfo-structure.md) 实例的指针，该实例包含从托管调试助手 (MDA) 的消息输出。</span><span class="sxs-lookup"><span data-stu-id="a2a63-130">If `event` is `Event_MDAFired`, `data` is a pointer to an [MDAInfo](mdainfo-structure.md) instance that contains the message output from a Managed Debugging Assistant (MDA).</span></span> <span data-ttu-id="a2a63-131">Mda 是 CLR 的一项功能，可帮助开发人员进行调试，方法是生成有关其他难以捕获的事件的 XML 消息。</span><span class="sxs-lookup"><span data-stu-id="a2a63-131">MDAs are a feature of the CLR that help developers with debugging, by generating XML messages about events that are otherwise difficult to trap.</span></span> <span data-ttu-id="a2a63-132">在调试托管代码和非托管代码之间的转换时，此类消息特别有用。</span><span class="sxs-lookup"><span data-stu-id="a2a63-132">Such messages can be especially useful in debugging transitions between managed and unmanaged code.</span></span> <span data-ttu-id="a2a63-133">有关详细信息，请参阅 [诊断托管调试助手的错误](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a63-133">For more information, see [Diagnosing Errors with Managed Debugging Assistants](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2a63-134">要求</span><span class="sxs-lookup"><span data-stu-id="a2a63-134">Requirements</span></span>  

 <span data-ttu-id="a2a63-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a63-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2a63-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a2a63-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a2a63-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a2a63-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a2a63-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2a63-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2a63-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="a2a63-139">See also</span></span>

- [<span data-ttu-id="a2a63-140">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="a2a63-140">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="a2a63-141">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="a2a63-141">EClrEvent Enumeration</span></span>](eclrevent-enumeration.md)
- [<span data-ttu-id="a2a63-142">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="a2a63-142">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)
- [<span data-ttu-id="a2a63-143">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="a2a63-143">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="a2a63-144">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="a2a63-144">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)
- [<span data-ttu-id="a2a63-145">MDAInfo 结构</span><span class="sxs-lookup"><span data-stu-id="a2a63-145">MDAInfo Structure</span></span>](mdainfo-structure.md)

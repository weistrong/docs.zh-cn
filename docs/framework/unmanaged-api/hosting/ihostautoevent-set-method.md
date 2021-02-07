---
description: 了解详细信息： IHostAutoEvent：： Set 方法
title: IHostAutoEvent::Set 方法
ms.date: 03/30/2017
api_name:
- IHostAutoEvent.Set
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAutoEvent::Set
helpviewer_keywords:
- Set method, IHostAutoEvent interface [.NET Framework hosting]
- IHostAutoEvent::Set method [.NET Framework hosting]
ms.assetid: 46becf3e-bc0e-4338-85c0-9ab0df76a1d0
topic_type:
- apiref
ms.openlocfilehash: e4ba63b5250a383431e410cd6e552f8344fedf5d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708907"
---
# <a name="ihostautoeventset-method"></a><span data-ttu-id="c42d5-103">IHostAutoEvent::Set 方法</span><span class="sxs-lookup"><span data-stu-id="c42d5-103">IHostAutoEvent::Set Method</span></span>

<span data-ttu-id="c42d5-104">将当前的 [IHostAutoEvent](ihostautoevent-interface.md) 实例设置为终止状态。</span><span class="sxs-lookup"><span data-stu-id="c42d5-104">Sets the current [IHostAutoEvent](ihostautoevent-interface.md) instance to a signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c42d5-105">语法</span><span class="sxs-lookup"><span data-stu-id="c42d5-105">Syntax</span></span>  
  
```cpp  
HRESULT Set ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="c42d5-106">返回值</span><span class="sxs-lookup"><span data-stu-id="c42d5-106">Return Value</span></span>  
  
|<span data-ttu-id="c42d5-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c42d5-107">HRESULT</span></span>|<span data-ttu-id="c42d5-108">说明</span><span class="sxs-lookup"><span data-stu-id="c42d5-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c42d5-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="c42d5-109">S_OK</span></span>|<span data-ttu-id="c42d5-110">`Set` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="c42d5-110">`Set` returned successfully.</span></span>|  
|<span data-ttu-id="c42d5-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c42d5-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c42d5-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="c42d5-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c42d5-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c42d5-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c42d5-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="c42d5-114">The call timed out.</span></span>|  
|<span data-ttu-id="c42d5-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c42d5-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c42d5-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="c42d5-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c42d5-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c42d5-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c42d5-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="c42d5-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c42d5-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c42d5-119">E_FAIL</span></span>|<span data-ttu-id="c42d5-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="c42d5-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c42d5-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="c42d5-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c42d5-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="c42d5-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c42d5-123">要求</span><span class="sxs-lookup"><span data-stu-id="c42d5-123">Requirements</span></span>  

 <span data-ttu-id="c42d5-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c42d5-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c42d5-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c42d5-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c42d5-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c42d5-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c42d5-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c42d5-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c42d5-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="c42d5-128">See also</span></span>

- [<span data-ttu-id="c42d5-129">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="c42d5-129">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="c42d5-130">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="c42d5-130">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="c42d5-131">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="c42d5-131">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="c42d5-132">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="c42d5-132">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)

---
description: 了解详细信息： ICLRIoCompletionManager：： OnComplete 方法
title: ICLRIoCompletionManager::OnComplete 方法
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager.OnComplete
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager::OnComplete
helpviewer_keywords:
- OnComplete method [.NET Framework hosting]
- ICLRIoCompletionManager::OnComplete method [.NET Framework hosting]
ms.assetid: 003f6974-9727-4322-bed5-e330d1224d0b
topic_type:
- apiref
ms.openlocfilehash: d54b189debdfc2959676b53fd3fb51b2c10dce17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789874"
---
# <a name="iclriocompletionmanageroncomplete-method"></a><span data-ttu-id="a9917-103">ICLRIoCompletionManager::OnComplete 方法</span><span class="sxs-lookup"><span data-stu-id="a9917-103">ICLRIoCompletionManager::OnComplete Method</span></span>

<span data-ttu-id="a9917-104">通知公共语言运行时 (CLR) 通过调用 [IHostIoCompletionManager：： Bind](ihostiocompletionmanager-bind-method.md) 方法发出的 i/o 请求的状态。</span><span class="sxs-lookup"><span data-stu-id="a9917-104">Notifies the common language runtime (CLR) of the status of an I/O request that was made by using a call to the [IHostIoCompletionManager::Bind](ihostiocompletionmanager-bind-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9917-105">语法</span><span class="sxs-lookup"><span data-stu-id="a9917-105">Syntax</span></span>  
  
```cpp  
HRESULT OnComplete (  
    [in] DWORD dwErrorCode,  
    [in] DWORD NumberOfBytesTransferred,  
    [in] void* pvOverlapped  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9917-106">参数</span><span class="sxs-lookup"><span data-stu-id="a9917-106">Parameters</span></span>  

 `dwErrorCode`  
 <span data-ttu-id="a9917-107">中一个 HRESULT 值，指示绑定操作的状态。</span><span class="sxs-lookup"><span data-stu-id="a9917-107">[in] An HRESULT value that indicates the status of the bind operation.</span></span>  
  
- <span data-ttu-id="a9917-108">S_OK 指示操作已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a9917-108">S_OK indicates that the operation completed successfully.</span></span>  
  
- <span data-ttu-id="a9917-109">HOST_E_INTERRUPTED 指示调用在完成前终止。</span><span class="sxs-lookup"><span data-stu-id="a9917-109">HOST_E_INTERRUPTED indicates that the call terminated before completion.</span></span>  
  
- <span data-ttu-id="a9917-110">E_FAIL 指示发生了未知、无法恢复的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a9917-110">E_FAIL indicates that an unknown, unrecoverable, catastrophic failure occurred.</span></span>  
  
 `NumberOfBytesTransferred`  
 <span data-ttu-id="a9917-111">中处理 i/o 请求过程中传输的字节数。</span><span class="sxs-lookup"><span data-stu-id="a9917-111">[in] The number of bytes transferred during the processing of the I/O request.</span></span>  
  
 `pvOverlapped`  
 <span data-ttu-id="a9917-112">中指向 `OVERLAPPED` 传递给方法调用的结构的指针 `IHostIoCompletionManager::Bind` 。</span><span class="sxs-lookup"><span data-stu-id="a9917-112">[in] A pointer to the `OVERLAPPED` structure that was passed to the call to the `IHostIoCompletionManager::Bind` method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a9917-113">返回值</span><span class="sxs-lookup"><span data-stu-id="a9917-113">Return Value</span></span>  
  
|<span data-ttu-id="a9917-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a9917-114">HRESULT</span></span>|<span data-ttu-id="a9917-115">说明</span><span class="sxs-lookup"><span data-stu-id="a9917-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a9917-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9917-116">S_OK</span></span>|<span data-ttu-id="a9917-117">`OnComplete` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a9917-117">`OnComplete` returned successfully.</span></span>|  
|<span data-ttu-id="a9917-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a9917-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a9917-119">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a9917-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a9917-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a9917-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a9917-121">调用超时。</span><span class="sxs-lookup"><span data-stu-id="a9917-121">The call timed out.</span></span>|  
|<span data-ttu-id="a9917-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a9917-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a9917-123">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a9917-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a9917-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a9917-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a9917-125">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="a9917-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a9917-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a9917-126">E_FAIL</span></span>|<span data-ttu-id="a9917-127">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a9917-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a9917-128">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="a9917-128">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a9917-129">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a9917-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a9917-130">备注</span><span class="sxs-lookup"><span data-stu-id="a9917-130">Remarks</span></span>  

 <span data-ttu-id="a9917-131">如果主机实现 i/o 完成抽象，则 CLR 通过使用 [IHostIoCompletionManager](ihostiocompletionmanager-interface.md)的方法在主机上发出 i/o 请求。</span><span class="sxs-lookup"><span data-stu-id="a9917-131">If the host implements an I/O completion abstraction, the CLR makes I/O requests through the host by using methods of [IHostIoCompletionManager](ihostiocompletionmanager-interface.md).</span></span> <span data-ttu-id="a9917-132">然后，宿主调用 `OnComplete` 方法以通知运行时此类请求的结果。</span><span class="sxs-lookup"><span data-stu-id="a9917-132">The host then calls the `OnComplete` method to notify the runtime of the outcome of such requests.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9917-133">要求</span><span class="sxs-lookup"><span data-stu-id="a9917-133">Requirements</span></span>  

 <span data-ttu-id="a9917-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9917-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9917-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a9917-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a9917-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a9917-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a9917-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9917-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9917-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9917-138">See also</span></span>

- [<span data-ttu-id="a9917-139">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="a9917-139">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="a9917-140">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="a9917-140">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
- [<span data-ttu-id="a9917-141">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="a9917-141">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)

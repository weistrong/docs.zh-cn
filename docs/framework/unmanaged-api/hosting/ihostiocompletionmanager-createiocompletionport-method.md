---
description: 了解详细信息： IHostIoCompletionManager：： CreateIoCompletionPort 方法
title: IHostIoCompletionManager::CreateIoCompletionPort 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.CreateIoCompletionPort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort
helpviewer_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort method [.NET Framework hosting]
- CreateIoCompletionPort method [.NET Framework hosting]
ms.assetid: 907a2b43-68db-44a7-acac-89e792e7bb3c
topic_type:
- apiref
ms.openlocfilehash: da4cd595e84c341eb15837ff97f4ba23cac23210
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789432"
---
# <a name="ihostiocompletionmanagercreateiocompletionport-method"></a><span data-ttu-id="f2aea-103">IHostIoCompletionManager::CreateIoCompletionPort 方法</span><span class="sxs-lookup"><span data-stu-id="f2aea-103">IHostIoCompletionManager::CreateIoCompletionPort Method</span></span>

<span data-ttu-id="f2aea-104">请求宿主创建新的 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="f2aea-104">Requests that the host create a new I/O completion port.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2aea-105">语法</span><span class="sxs-lookup"><span data-stu-id="f2aea-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateIoCompletionPort (  
    [out] HANDLE *phPort  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2aea-106">参数</span><span class="sxs-lookup"><span data-stu-id="f2aea-106">Parameters</span></span>  

 `phPort`  
 <span data-ttu-id="f2aea-107">弄指向新创建的 i/o 完成端口的句柄的指针; 如果无法创建端口，则为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f2aea-107">[out] A pointer to a handle to the newly created I/O completion port, or 0 (zero), if the port could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f2aea-108">返回值</span><span class="sxs-lookup"><span data-stu-id="f2aea-108">Return Value</span></span>  
  
|<span data-ttu-id="f2aea-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f2aea-109">HRESULT</span></span>|<span data-ttu-id="f2aea-110">说明</span><span class="sxs-lookup"><span data-stu-id="f2aea-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f2aea-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2aea-111">S_OK</span></span>|<span data-ttu-id="f2aea-112">`CreateIoCompletionPort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f2aea-112">`CreateIoCompletionPort` returned successfully.</span></span>|  
|<span data-ttu-id="f2aea-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f2aea-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f2aea-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f2aea-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f2aea-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f2aea-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f2aea-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f2aea-116">The call timed out.</span></span>|  
|<span data-ttu-id="f2aea-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f2aea-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f2aea-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f2aea-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f2aea-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f2aea-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f2aea-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f2aea-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f2aea-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f2aea-121">E_FAIL</span></span>|<span data-ttu-id="f2aea-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f2aea-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f2aea-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f2aea-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f2aea-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f2aea-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f2aea-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f2aea-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="f2aea-126">没有足够的内存可用于分配请求的资源。</span><span class="sxs-lookup"><span data-stu-id="f2aea-126">Not enough memory was available to allocate the requested resource.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f2aea-127">备注</span><span class="sxs-lookup"><span data-stu-id="f2aea-127">Remarks</span></span>  

 <span data-ttu-id="f2aea-128">CLR 调用 `CreateIoCompletionPort` 方法来请求宿主创建新的 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="f2aea-128">The CLR calls the `CreateIoCompletionPort` method to request that the host create a new I/O completion port.</span></span> <span data-ttu-id="f2aea-129">它通过调用 [IHostIoCompletionManager：： Bind](ihostiocompletionmanager-bind-method.md) 方法将 i/o 操作绑定到此端口。</span><span class="sxs-lookup"><span data-stu-id="f2aea-129">It binds I/O operations to this port through a call to the [IHostIoCompletionManager::Bind](ihostiocompletionmanager-bind-method.md) method.</span></span> <span data-ttu-id="f2aea-130">主机通过调用 [ICLRIoCompletionManager：： OnComplete](iclriocompletionmanager-oncomplete-method.md)将状态报告回 CLR。</span><span class="sxs-lookup"><span data-stu-id="f2aea-130">The host reports status back to the CLR by calling [ICLRIoCompletionManager::OnComplete](iclriocompletionmanager-oncomplete-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2aea-131">要求</span><span class="sxs-lookup"><span data-stu-id="f2aea-131">Requirements</span></span>  

 <span data-ttu-id="f2aea-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2aea-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2aea-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f2aea-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f2aea-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f2aea-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2aea-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2aea-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2aea-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="f2aea-136">See also</span></span>

- [<span data-ttu-id="f2aea-137">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2aea-137">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="f2aea-138">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2aea-138">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)

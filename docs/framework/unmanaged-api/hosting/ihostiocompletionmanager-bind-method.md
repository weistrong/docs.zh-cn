---
description: 了解详细信息： IHostIoCompletionManager：： Bind 方法
title: IHostIoCompletionManager::Bind 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.Bind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::Bind
helpviewer_keywords:
- IHostIoCompletionManager::Bind method [.NET Framework hosting]
- Bind method [.NET Framework hosting]
ms.assetid: acd74cb5-7e22-4a07-83c3-82288e1abd9f
topic_type:
- apiref
ms.openlocfilehash: 2105bf06c23f70588d0c1bc0cd849b8e810d121e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784855"
---
# <a name="ihostiocompletionmanagerbind-method"></a><span data-ttu-id="ee601-103">IHostIoCompletionManager::Bind 方法</span><span class="sxs-lookup"><span data-stu-id="ee601-103">IHostIoCompletionManager::Bind Method</span></span>

<span data-ttu-id="ee601-104">将指定的句柄绑定到由之前对 [CreateIoCompletionPort](ihostiocompletionmanager-createiocompletionport-method.md)的调用创建的 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="ee601-104">Binds the specified handle to an I/O completion port that has been created by an earlier call to [CreateIoCompletionPort](ihostiocompletionmanager-createiocompletionport-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee601-105">语法</span><span class="sxs-lookup"><span data-stu-id="ee601-105">Syntax</span></span>  
  
```cpp  
HRESULT Bind (  
    [in] HANDLE hPort,  
    [in] HANDLE hHandle  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ee601-106">参数</span><span class="sxs-lookup"><span data-stu-id="ee601-106">Parameters</span></span>  

 `hPort`  
 <span data-ttu-id="ee601-107">中要绑定到的 i/o 完成端口 `hHandle` 。</span><span class="sxs-lookup"><span data-stu-id="ee601-107">[in] The I/O completion port to which to bind `hHandle`.</span></span> <span data-ttu-id="ee601-108">如果的值 `hPort` 为 null， `hHandle` 则绑定到默认 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="ee601-108">If the value of `hPort` is null, `hHandle` is bound to the default I/O completion port.</span></span>  
  
 `hHandle`  
 <span data-ttu-id="ee601-109">中要绑定到的操作系统句柄 `hPort` 。</span><span class="sxs-lookup"><span data-stu-id="ee601-109">[in] The operating system handle to bind to `hPort`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ee601-110">返回值</span><span class="sxs-lookup"><span data-stu-id="ee601-110">Return Value</span></span>  
  
|<span data-ttu-id="ee601-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ee601-111">HRESULT</span></span>|<span data-ttu-id="ee601-112">说明</span><span class="sxs-lookup"><span data-stu-id="ee601-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ee601-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee601-113">S_OK</span></span>|<span data-ttu-id="ee601-114">`Bind` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ee601-114">`Bind` returned successfully.</span></span>|  
|<span data-ttu-id="ee601-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ee601-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ee601-116"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ee601-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ee601-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ee601-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ee601-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ee601-118">The call timed out.</span></span>|  
|<span data-ttu-id="ee601-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ee601-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ee601-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ee601-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ee601-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ee601-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ee601-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ee601-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ee601-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ee601-123">E_FAIL</span></span>|<span data-ttu-id="ee601-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ee601-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ee601-125">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ee601-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ee601-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ee601-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ee601-127">备注</span><span class="sxs-lookup"><span data-stu-id="ee601-127">Remarks</span></span>  

 <span data-ttu-id="ee601-128">I/o 完成端口是使用对的调用创建的 `CreateIoCompletionPort` 。</span><span class="sxs-lookup"><span data-stu-id="ee601-128">An I/O completion port is created by using a call to `CreateIoCompletionPort`.</span></span> <span data-ttu-id="ee601-129">CLR 调用 `Bind` 将句柄绑定到该端口。</span><span class="sxs-lookup"><span data-stu-id="ee601-129">The CLR calls `Bind` to bind a handle to that port.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ee601-130">当 i/o 请求完成时，主机必须调用 [ICLRIoCompletionManager：： OnComplete](iclriocompletionmanager-oncomplete-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ee601-130">When an I/O request completes, the host must call the [ICLRIoCompletionManager::OnComplete](iclriocompletionmanager-oncomplete-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ee601-131">要求</span><span class="sxs-lookup"><span data-stu-id="ee601-131">Requirements</span></span>  

 <span data-ttu-id="ee601-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ee601-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee601-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ee601-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ee601-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ee601-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ee601-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee601-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee601-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee601-136">See also</span></span>

- [<span data-ttu-id="ee601-137">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="ee601-137">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)

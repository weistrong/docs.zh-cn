---
description: 了解详细信息： IHostIoCompletionManager：： CloseIoCompletionPort 方法
title: IHostIoCompletionManager::CloseIoCompletionPort 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.CloseIoCompletionPort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::CloseIoCompletionPort
helpviewer_keywords:
- IHostIoCompletionManager::CloseIoCompletionPort method [.NET Framework hosting]
- CloseIoCompletionPort method [.NET Framework hosting]
ms.assetid: e86ad7be-3758-498a-a972-5522d69dfbb3
topic_type:
- apiref
ms.openlocfilehash: 987b9f4e0fa22fa977fa1b14c77c8c0381e3e399
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728504"
---
# <a name="ihostiocompletionmanagercloseiocompletionport-method"></a><span data-ttu-id="29e95-103">IHostIoCompletionManager::CloseIoCompletionPort 方法</span><span class="sxs-lookup"><span data-stu-id="29e95-103">IHostIoCompletionManager::CloseIoCompletionPort Method</span></span>

<span data-ttu-id="29e95-104">请求宿主关闭通过之前对 [CreateIoCompletionPort](ihostiocompletionmanager-createiocompletionport-method.md)的调用打开的端口。</span><span class="sxs-lookup"><span data-stu-id="29e95-104">Requests that the host close a port that was opened through an earlier call to [CreateIoCompletionPort](ihostiocompletionmanager-createiocompletionport-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29e95-105">语法</span><span class="sxs-lookup"><span data-stu-id="29e95-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseIoCompletionPort (  
    [in] HANDLE hPort  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="29e95-106">参数</span><span class="sxs-lookup"><span data-stu-id="29e95-106">Parameters</span></span>  

 `hPort`  
 <span data-ttu-id="29e95-107">中要关闭的端口的句柄。</span><span class="sxs-lookup"><span data-stu-id="29e95-107">[in] The handle of the port to close.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="29e95-108">返回值</span><span class="sxs-lookup"><span data-stu-id="29e95-108">Return Value</span></span>  
  
|<span data-ttu-id="29e95-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="29e95-109">HRESULT</span></span>|<span data-ttu-id="29e95-110">说明</span><span class="sxs-lookup"><span data-stu-id="29e95-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="29e95-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="29e95-111">S_OK</span></span>|<span data-ttu-id="29e95-112">`CloseIoCompletionPort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="29e95-112">`CloseIoCompletionPort` returned successfully.</span></span>|  
|<span data-ttu-id="29e95-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="29e95-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="29e95-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="29e95-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="29e95-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="29e95-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="29e95-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="29e95-116">The call timed out.</span></span>|  
|<span data-ttu-id="29e95-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="29e95-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="29e95-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="29e95-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="29e95-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="29e95-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="29e95-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="29e95-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="29e95-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="29e95-121">E_FAIL</span></span>|<span data-ttu-id="29e95-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="29e95-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="29e95-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="29e95-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="29e95-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="29e95-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="29e95-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="29e95-125">E_INVALIDARG</span></span>|<span data-ttu-id="29e95-126">传递了无效的端口句柄。</span><span class="sxs-lookup"><span data-stu-id="29e95-126">An invalid port handle was passed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="29e95-127">备注</span><span class="sxs-lookup"><span data-stu-id="29e95-127">Remarks</span></span>  

 <span data-ttu-id="29e95-128">`hPort` 必须是由先前对的调用创建的端口的句柄 `CreateIoCompletionPort` 。</span><span class="sxs-lookup"><span data-stu-id="29e95-128">`hPort` must be a handle to a port that was created by an earlier call to `CreateIoCompletionPort`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29e95-129">要求</span><span class="sxs-lookup"><span data-stu-id="29e95-129">Requirements</span></span>  

 <span data-ttu-id="29e95-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="29e95-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="29e95-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="29e95-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="29e95-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="29e95-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="29e95-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="29e95-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29e95-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="29e95-134">See also</span></span>

- [<span data-ttu-id="29e95-135">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="29e95-135">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="29e95-136">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="29e95-136">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)

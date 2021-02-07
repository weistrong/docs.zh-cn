---
description: 了解详细信息： ICLRTaskManager：： GetCurrentTask 方法
title: ICLRTaskManager::GetCurrentTask 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTask
helpviewer_keywords:
- GetCurrentTask method, ICLRTaskManager interface [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTask method [.NET Framework hosting]
ms.assetid: c0b82a9f-edc6-4878-9c81-48de53c02142
topic_type:
- apiref
ms.openlocfilehash: d7435f9099d6a8ceb173afbf79c1d0f5d4005980
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728530"
---
# <a name="iclrtaskmanagergetcurrenttask-method"></a><span data-ttu-id="ac557-103">ICLRTaskManager::GetCurrentTask 方法</span><span class="sxs-lookup"><span data-stu-id="ac557-103">ICLRTaskManager::GetCurrentTask Method</span></span>

<span data-ttu-id="ac557-104">获取当前在该方法调用所源自的操作系统线程上运行的 [ICLRTask](iclrtask-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="ac557-104">Gets the [ICLRTask](iclrtask-interface.md) instance that is currently running on the operating system thread from which the method call originated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac557-105">语法</span><span class="sxs-lookup"><span data-stu-id="ac557-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentTask (  
    [out] ICLRTask **ppTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac557-106">参数</span><span class="sxs-lookup"><span data-stu-id="ac557-106">Parameters</span></span>  

 `ppTask`  
 <span data-ttu-id="ac557-107">弄一个指针 `ICLRTask` ，指向从其发出调用的操作系统线程上当前正在执行的实例的地址，如果此线程上当前未执行任何任务，则为 null。</span><span class="sxs-lookup"><span data-stu-id="ac557-107">[out] A pointer to the address of an `ICLRTask` instance that is currently executing on the operating system thread from which the call originated, or null if no task is currently executing on this thread.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ac557-108">返回值</span><span class="sxs-lookup"><span data-stu-id="ac557-108">Return Value</span></span>  
  
|<span data-ttu-id="ac557-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ac557-109">HRESULT</span></span>|<span data-ttu-id="ac557-110">说明</span><span class="sxs-lookup"><span data-stu-id="ac557-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ac557-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac557-111">S_OK</span></span>|<span data-ttu-id="ac557-112">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ac557-112">The method returned successfully.</span></span>|  
|<span data-ttu-id="ac557-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ac557-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ac557-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ac557-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ac557-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ac557-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ac557-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ac557-116">The call timed out.</span></span>|  
|<span data-ttu-id="ac557-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ac557-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ac557-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ac557-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ac557-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ac557-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ac557-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ac557-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ac557-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ac557-121">E_FAIL</span></span>|<span data-ttu-id="ac557-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ac557-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ac557-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ac557-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ac557-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ac557-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac557-125">备注</span><span class="sxs-lookup"><span data-stu-id="ac557-125">Remarks</span></span>  

 <span data-ttu-id="ac557-126">`ICLRTask`参数指向的实例 `ppTask` 表示 CLR 当前正在执行的任务。</span><span class="sxs-lookup"><span data-stu-id="ac557-126">The `ICLRTask` instance that the `ppTask` parameter points to represents the currently executing task for the CLR.</span></span> <span data-ttu-id="ac557-127">`ICLRTask`实例与表示宿主任务的相应[IHostTask](ihosttask-interface.md)实例相关联。</span><span class="sxs-lookup"><span data-stu-id="ac557-127">The `ICLRTask` instance is associated with a corresponding [IHostTask](ihosttask-interface.md) instance that represents the task for the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac557-128">要求</span><span class="sxs-lookup"><span data-stu-id="ac557-128">Requirements</span></span>  

 <span data-ttu-id="ac557-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ac557-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac557-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ac557-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ac557-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ac557-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ac557-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac557-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac557-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac557-133">See also</span></span>

- [<span data-ttu-id="ac557-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="ac557-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="ac557-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="ac557-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="ac557-136">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="ac557-136">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="ac557-137">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="ac557-137">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)

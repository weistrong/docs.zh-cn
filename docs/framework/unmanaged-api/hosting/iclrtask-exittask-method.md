---
description: 了解详细信息： ICLRTask：： ExitTask 方法
title: ICLRTask::ExitTask 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.ExitTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::ExitTask
helpviewer_keywords:
- ExitTask method [.NET Framework hosting]
- ICLRTask::ExitTask method [.NET Framework hosting]
ms.assetid: 746c85a6-4b33-4f72-a2e9-379fdf2e96af
topic_type:
- apiref
ms.openlocfilehash: 267b7f284ccac5b535a72dab425c035b6c689361
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784959"
---
# <a name="iclrtaskexittask-method"></a><span data-ttu-id="358bc-103">ICLRTask::ExitTask 方法</span><span class="sxs-lookup"><span data-stu-id="358bc-103">ICLRTask::ExitTask Method</span></span>

<span data-ttu-id="358bc-104">通知公共语言运行时 (CLR) 当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务正在结束，并尝试正常关闭任务。</span><span class="sxs-lookup"><span data-stu-id="358bc-104">Notifies the common language runtime (CLR) that the task represented by the current [ICLRTask](iclrtask-interface.md) instance is ending, and attempts to shut the task down gracefully.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="358bc-105">语法</span><span class="sxs-lookup"><span data-stu-id="358bc-105">Syntax</span></span>  
  
```cpp  
HRESULT ExitTask ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="358bc-106">返回值</span><span class="sxs-lookup"><span data-stu-id="358bc-106">Return Value</span></span>  
  
|<span data-ttu-id="358bc-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="358bc-107">HRESULT</span></span>|<span data-ttu-id="358bc-108">说明</span><span class="sxs-lookup"><span data-stu-id="358bc-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="358bc-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="358bc-109">S_OK</span></span>|<span data-ttu-id="358bc-110">`ExitTask` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="358bc-110">`ExitTask` returned successfully.</span></span>|  
|<span data-ttu-id="358bc-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="358bc-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="358bc-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="358bc-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="358bc-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="358bc-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="358bc-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="358bc-114">The call timed out.</span></span>|  
|<span data-ttu-id="358bc-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="358bc-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="358bc-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="358bc-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="358bc-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="358bc-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="358bc-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="358bc-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="358bc-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="358bc-119">E_FAIL</span></span>|<span data-ttu-id="358bc-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="358bc-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="358bc-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="358bc-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="358bc-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="358bc-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="358bc-123">备注</span><span class="sxs-lookup"><span data-stu-id="358bc-123">Remarks</span></span>  

 <span data-ttu-id="358bc-124">`ExitTask` 尝试完全关闭任务，其方式类似于从非托管类型库分离线程。</span><span class="sxs-lookup"><span data-stu-id="358bc-124">`ExitTask` attempts a clean shutdown of a task, in a manner analogous to detaching a thread from an unmanaged type library.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="358bc-125">要求</span><span class="sxs-lookup"><span data-stu-id="358bc-125">Requirements</span></span>  

 <span data-ttu-id="358bc-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="358bc-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="358bc-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="358bc-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="358bc-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="358bc-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="358bc-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="358bc-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="358bc-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="358bc-130">See also</span></span>

- [<span data-ttu-id="358bc-131">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="358bc-131">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="358bc-132">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="358bc-132">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="358bc-133">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="358bc-133">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="358bc-134">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="358bc-134">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)

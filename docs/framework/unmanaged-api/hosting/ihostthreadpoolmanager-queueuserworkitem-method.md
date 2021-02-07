---
description: 了解详细信息： IHostThreadPoolManager：： QueueUserWorkItem 方法
title: IHostThreadPoolManager::QueueUserWorkItem 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.QueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::QueueUserWorkItem
helpviewer_keywords:
- IHostThreadPoolManager::QueueUserWorkItem method [.NET Framework hosting]
- QueueUserWorkItem method [.NET Framework hosting]
ms.assetid: 41602053-8670-4827-9d61-cbfcba509b9c
topic_type:
- apiref
ms.openlocfilehash: edfbf5cfb34473a5fd920307981237fd5deab9aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753778"
---
# <a name="ihostthreadpoolmanagerqueueuserworkitem-method"></a><span data-ttu-id="8c34d-103">IHostThreadPoolManager::QueueUserWorkItem 方法</span><span class="sxs-lookup"><span data-stu-id="8c34d-103">IHostThreadPoolManager::QueueUserWorkItem Method</span></span>

<span data-ttu-id="8c34d-104">将函数排队以便执行，并指定包含该函数要使用的数据的对象。</span><span class="sxs-lookup"><span data-stu-id="8c34d-104">Queues a function for execution, and specifies an object containing data to be used by that function.</span></span> <span data-ttu-id="8c34d-105">当线程变为可用时，该函数执行。</span><span class="sxs-lookup"><span data-stu-id="8c34d-105">The function executes when a thread becomes available.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c34d-106">语法</span><span class="sxs-lookup"><span data-stu-id="8c34d-106">Syntax</span></span>  
  
```cpp  
HRESULT QueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID Context,  
    [in] ULONG Flags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8c34d-107">参数</span><span class="sxs-lookup"><span data-stu-id="8c34d-107">Parameters</span></span>  

 `Function`  
 <span data-ttu-id="8c34d-108">中表示要执行的函数的函数指针。</span><span class="sxs-lookup"><span data-stu-id="8c34d-108">[in] A function pointer that represents the function to execute.</span></span>  
  
 `Context`  
 <span data-ttu-id="8c34d-109">中包含要使用的数据的对象 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="8c34d-109">[in] An object that contains data to be used by `Function`.</span></span>  
  
 `Flags`  
 <span data-ttu-id="8c34d-110">中用于控制执行的、针对 Win32 方法定义的标志值之一 `QueueUserWorkItem` 。</span><span class="sxs-lookup"><span data-stu-id="8c34d-110">[in] One of the flags values, as defined for the Win32 `QueueUserWorkItem` method, that control execution.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8c34d-111">返回值</span><span class="sxs-lookup"><span data-stu-id="8c34d-111">Return Value</span></span>  
  
|<span data-ttu-id="8c34d-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8c34d-112">HRESULT</span></span>|<span data-ttu-id="8c34d-113">说明</span><span class="sxs-lookup"><span data-stu-id="8c34d-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8c34d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c34d-114">S_OK</span></span>|<span data-ttu-id="8c34d-115">`QueueUserWorkItem` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="8c34d-115">`QueueUserWorkItem` returned successfully.</span></span>|  
|<span data-ttu-id="8c34d-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8c34d-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8c34d-117"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="8c34d-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8c34d-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8c34d-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8c34d-119">调用超时。</span><span class="sxs-lookup"><span data-stu-id="8c34d-119">The call timed out.</span></span>|  
|<span data-ttu-id="8c34d-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8c34d-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8c34d-121">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="8c34d-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8c34d-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8c34d-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8c34d-123">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="8c34d-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8c34d-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8c34d-124">E_FAIL</span></span>|<span data-ttu-id="8c34d-125">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="8c34d-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8c34d-126">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="8c34d-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8c34d-127">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="8c34d-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8c34d-128">备注</span><span class="sxs-lookup"><span data-stu-id="8c34d-128">Remarks</span></span>  

 <span data-ttu-id="8c34d-129">`QueueUserWorkItem` 将工作项排队到线程池中的工作线程。</span><span class="sxs-lookup"><span data-stu-id="8c34d-129">`QueueUserWorkItem` queues a work item to a worker thread in the thread pool.</span></span> <span data-ttu-id="8c34d-130">其签名和参数类型与具有相同名称的对应 Win32 函数的签名和参数类型相同。</span><span class="sxs-lookup"><span data-stu-id="8c34d-130">Its signature and parameter types are identical to those of the corresponding Win32 function, which has the same name.</span></span> <span data-ttu-id="8c34d-131">有关详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="8c34d-131">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8c34d-132">要求</span><span class="sxs-lookup"><span data-stu-id="8c34d-132">Requirements</span></span>  

 <span data-ttu-id="8c34d-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8c34d-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8c34d-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8c34d-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8c34d-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8c34d-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8c34d-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8c34d-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c34d-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="8c34d-137">See also</span></span>

- <xref:System.Threading.ThreadPool.QueueUserWorkItem%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="8c34d-138">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="8c34d-138">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)

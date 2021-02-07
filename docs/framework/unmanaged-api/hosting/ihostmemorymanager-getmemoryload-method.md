---
description: 了解详细信息： IHostMemoryManager：： GetMemoryLoad 方法
title: IHostMemoryManager::GetMemoryLoad 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.GetMemoryLoad
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::GetMemoryLoad
helpviewer_keywords:
- IHostMemoryManager::GetMemoryLoad method [.NET Framework hosting]
- GetMemoryLoad method [.NET Framework hosting]
ms.assetid: e8138f6e-a0a4-48d4-8dae-9466b4dc6180
topic_type:
- apiref
ms.openlocfilehash: 82288e6a705b014c2768c75e15376f7e6a0af428
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707836"
---
# <a name="ihostmemorymanagergetmemoryload-method"></a><span data-ttu-id="9cc21-103">IHostMemoryManager::GetMemoryLoad 方法</span><span class="sxs-lookup"><span data-stu-id="9cc21-103">IHostMemoryManager::GetMemoryLoad Method</span></span>

<span data-ttu-id="9cc21-104">获取主机报告的当前正在使用的物理内存量，因而不可用。</span><span class="sxs-lookup"><span data-stu-id="9cc21-104">Gets the amount of physical memory that is currently in use, and therefore unavailable, as reported by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cc21-105">语法</span><span class="sxs-lookup"><span data-stu-id="9cc21-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMemoryLoad (  
    [out] DWORD*  pMemoryLoad,
    [out] SIZE_T  *pAvailableBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9cc21-106">参数</span><span class="sxs-lookup"><span data-stu-id="9cc21-106">Parameters</span></span>  

 `pMemoryLoad`  
 <span data-ttu-id="9cc21-107">弄一个指针，指向当前正在使用的总物理内存的百分比。</span><span class="sxs-lookup"><span data-stu-id="9cc21-107">[out] A pointer to the approximate percentage of total physical memory that is currently in use.</span></span>  
  
 `pAvailableBytes`  
 <span data-ttu-id="9cc21-108">弄一个指针，它指向公共语言运行时可 (CLR) 使用的字节数。</span><span class="sxs-lookup"><span data-stu-id="9cc21-108">[out] A pointer to the number of bytes available to the common language runtime (CLR).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9cc21-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9cc21-109">Return Value</span></span>  
  
|<span data-ttu-id="9cc21-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9cc21-110">HRESULT</span></span>|<span data-ttu-id="9cc21-111">说明</span><span class="sxs-lookup"><span data-stu-id="9cc21-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9cc21-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9cc21-112">S_OK</span></span>|<span data-ttu-id="9cc21-113">`GetMemoryLoad` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="9cc21-113">`GetMemoryLoad` returned successfully.</span></span>|  
|<span data-ttu-id="9cc21-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9cc21-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9cc21-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="9cc21-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="9cc21-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9cc21-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="9cc21-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="9cc21-117">The call timed out.</span></span>|  
|<span data-ttu-id="9cc21-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="9cc21-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="9cc21-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="9cc21-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="9cc21-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="9cc21-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="9cc21-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="9cc21-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="9cc21-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9cc21-122">E_FAIL</span></span>|<span data-ttu-id="9cc21-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="9cc21-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="9cc21-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="9cc21-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="9cc21-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="9cc21-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9cc21-126">备注</span><span class="sxs-lookup"><span data-stu-id="9cc21-126">Remarks</span></span>  

 <span data-ttu-id="9cc21-127">`GetMemoryLoad` 包装 Win32 `GlobalMemoryStatus` 函数。</span><span class="sxs-lookup"><span data-stu-id="9cc21-127">`GetMemoryLoad` wraps the Win32 `GlobalMemoryStatus` function.</span></span> <span data-ttu-id="9cc21-128">的值与 `pMemoryLoad` `dwMemoryLoad` 从返回的结构中的字段等效 `MEMORYSTATUS` `GlobalMemoryStatus` 。</span><span class="sxs-lookup"><span data-stu-id="9cc21-128">The value of `pMemoryLoad` is the equivalent of the `dwMemoryLoad` field in the `MEMORYSTATUS` structure returned from `GlobalMemoryStatus`.</span></span>  
  
 <span data-ttu-id="9cc21-129">运行时使用返回值作为垃圾回收器的试探法。</span><span class="sxs-lookup"><span data-stu-id="9cc21-129">The runtime uses the return value as a heuristic for the garbage collector.</span></span> <span data-ttu-id="9cc21-130">例如，如果主机报告大部分内存正在使用中，垃圾回收器可能会选择从多个代进行收集，以增加可能会变得可用的内存量。</span><span class="sxs-lookup"><span data-stu-id="9cc21-130">For example, if the host reports that the majority of memory is in use, the garbage collector may elect to collect from multiple generations to increase the amount of memory that can potentially become available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9cc21-131">要求</span><span class="sxs-lookup"><span data-stu-id="9cc21-131">Requirements</span></span>  

 <span data-ttu-id="9cc21-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc21-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9cc21-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9cc21-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9cc21-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9cc21-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9cc21-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cc21-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cc21-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="9cc21-136">See also</span></span>

- <xref:System.GC?displayProperty=nameWithType>
- [<span data-ttu-id="9cc21-137">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="9cc21-137">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)

---
description: 了解详细信息： IHostMAlloc：： Free 方法
title: IHostMAlloc::Free 方法
ms.date: 03/30/2017
api_name:
- IHostMAlloc.Free
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc::Free
helpviewer_keywords:
- IHostMAlloc::Free method [.NET Framework hosting]
- Free method, IHostMAlloc interface [.NET Framework hosting]
ms.assetid: c89abf5b-1120-4437-8b57-4a99fb3ae7f9
topic_type:
- apiref
ms.openlocfilehash: 097e2e95b6dfb9d6a1bae68f9e0455a96383159e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708198"
---
# <a name="ihostmallocfree-method"></a><span data-ttu-id="0b177-103">IHostMAlloc::Free 方法</span><span class="sxs-lookup"><span data-stu-id="0b177-103">IHostMAlloc::Free Method</span></span>

<span data-ttu-id="0b177-104">释放使用 [分配](ihostmalloc-alloc-method.md) 函数分配的内存。</span><span class="sxs-lookup"><span data-stu-id="0b177-104">Frees memory that was allocated by using the [Alloc](ihostmalloc-alloc-method.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b177-105">语法</span><span class="sxs-lookup"><span data-stu-id="0b177-105">Syntax</span></span>  
  
```cpp  
HRESULT Free (  
    [in] void* pMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0b177-106">参数</span><span class="sxs-lookup"><span data-stu-id="0b177-106">Parameters</span></span>  

 `pMem`  
 <span data-ttu-id="0b177-107">中指向要释放的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="0b177-107">[in] A pointer to the memory to be freed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0b177-108">返回值</span><span class="sxs-lookup"><span data-stu-id="0b177-108">Return Value</span></span>  
  
|<span data-ttu-id="0b177-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0b177-109">HRESULT</span></span>|<span data-ttu-id="0b177-110">说明</span><span class="sxs-lookup"><span data-stu-id="0b177-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0b177-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b177-111">S_OK</span></span>|<span data-ttu-id="0b177-112">`Free` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="0b177-112">`Free` returned successfully.</span></span>|  
|<span data-ttu-id="0b177-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0b177-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0b177-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="0b177-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0b177-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0b177-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0b177-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="0b177-116">The call timed out.</span></span>|  
|<span data-ttu-id="0b177-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0b177-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0b177-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="0b177-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0b177-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0b177-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0b177-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="0b177-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0b177-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0b177-121">E_FAIL</span></span>|<span data-ttu-id="0b177-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="0b177-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0b177-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="0b177-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0b177-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="0b177-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="0b177-125">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="0b177-125">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="0b177-126">尝试释放未通过主机分配的内存。</span><span class="sxs-lookup"><span data-stu-id="0b177-126">An attempt was made to free memory that was not allocated through the host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0b177-127">备注</span><span class="sxs-lookup"><span data-stu-id="0b177-127">Remarks</span></span>  

 <span data-ttu-id="0b177-128">如果 `pMem` 参数引用未使用调用分配的内存区域 `Alloc` ，则宿主应返回 HOST_E_INVALIDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="0b177-128">If the `pMem` parameter refers to a region of memory that was not allocated by using a call to `Alloc`, the host should return HOST_E_INVALIDOPERATION.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b177-129">要求</span><span class="sxs-lookup"><span data-stu-id="0b177-129">Requirements</span></span>  

 <span data-ttu-id="0b177-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0b177-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b177-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0b177-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0b177-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0b177-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0b177-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b177-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b177-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="0b177-134">See also</span></span>

- [<span data-ttu-id="0b177-135">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="0b177-135">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="0b177-136">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="0b177-136">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)

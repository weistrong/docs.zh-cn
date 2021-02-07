---
description: 了解详细信息： IHostMemoryManager：： VirtualProtect 方法
title: IHostMemoryManager::VirtualProtect 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualProtect
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualProtect
helpviewer_keywords:
- IHostMemoryManager::VirtualProtect method [.NET Framework hosting]
- VirtualProtect method [.NET Framework hosting]
ms.assetid: 13be0299-df0d-4951-aabf-0676a30b385f
topic_type:
- apiref
ms.openlocfilehash: 66e1fb5afdc3aa5c400ed0ffa9cea569d300e6a3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707421"
---
# <a name="ihostmemorymanagervirtualprotect-method"></a><span data-ttu-id="2873c-103">IHostMemoryManager::VirtualProtect 方法</span><span class="sxs-lookup"><span data-stu-id="2873c-103">IHostMemoryManager::VirtualProtect Method</span></span>

<span data-ttu-id="2873c-104">用作相应 Win32 函数的逻辑包装。</span><span class="sxs-lookup"><span data-stu-id="2873c-104">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="2873c-105">的 Win32 实现在 `VirtualProtect` 调用进程的虚拟地址空间中更改已提交页面区域的保护。</span><span class="sxs-lookup"><span data-stu-id="2873c-105">The Win32 implementation of `VirtualProtect` changes the protection on a region of committed pages in the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2873c-106">语法</span><span class="sxs-lookup"><span data-stu-id="2873c-106">Syntax</span></span>  
  
```cpp  
HRESULT VirtualProtect (  
    [in]  void*   lpAddress,  
    [in]  SIZE_T  dwSize,  
    [in]  DWORD   flNewProtect,  
    [out] DWORD*  pflOldProtect  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2873c-107">参数</span><span class="sxs-lookup"><span data-stu-id="2873c-107">Parameters</span></span>  

 `lpAddress`  
 <span data-ttu-id="2873c-108">中指向要更改其保护属性的虚拟内存基址的指针。</span><span class="sxs-lookup"><span data-stu-id="2873c-108">[in] A pointer to the base address of the virtual memory whose protection attributes are to be changed.</span></span>  
  
 `dwSize`  
 <span data-ttu-id="2873c-109">中要更改的内存页区域的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="2873c-109">[in] The size, in bytes, of the region of memory pages to be changed.</span></span>  
  
 `flNewProtect`  
 <span data-ttu-id="2873c-110">中要应用的内存保护的类型。</span><span class="sxs-lookup"><span data-stu-id="2873c-110">[in] The type of memory protection to apply.</span></span>  
  
 `pflOldProtect`  
 <span data-ttu-id="2873c-111">弄指向上一个内存保护值的指针。</span><span class="sxs-lookup"><span data-stu-id="2873c-111">[out] A pointer to the previous memory protection value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2873c-112">返回值</span><span class="sxs-lookup"><span data-stu-id="2873c-112">Return Value</span></span>  
  
|<span data-ttu-id="2873c-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2873c-113">HRESULT</span></span>|<span data-ttu-id="2873c-114">说明</span><span class="sxs-lookup"><span data-stu-id="2873c-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2873c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="2873c-115">S_OK</span></span>|<span data-ttu-id="2873c-116">`VirtualProtect` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="2873c-116">`VirtualProtect` returned successfully.</span></span>|  
|<span data-ttu-id="2873c-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2873c-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2873c-118"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="2873c-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2873c-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2873c-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2873c-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="2873c-120">The call timed out.</span></span>|  
|<span data-ttu-id="2873c-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2873c-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2873c-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="2873c-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2873c-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2873c-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2873c-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="2873c-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2873c-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2873c-125">E_FAIL</span></span>|<span data-ttu-id="2873c-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="2873c-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2873c-127">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="2873c-127">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2873c-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="2873c-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2873c-129">备注</span><span class="sxs-lookup"><span data-stu-id="2873c-129">Remarks</span></span>  

 <span data-ttu-id="2873c-130">的此实现 `VirtualProtect` 返回一个 HRESULT 值，而 Win32 实现返回非零值以指示成功，并返回一个零值以指示失败。</span><span class="sxs-lookup"><span data-stu-id="2873c-130">This implementation of `VirtualProtect` returns an HRESULT value, while the Win32 implementation returns a non-zero value to indicate success, and a zero value to indicate failure.</span></span> <span data-ttu-id="2873c-131">有关详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="2873c-131">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2873c-132">要求</span><span class="sxs-lookup"><span data-stu-id="2873c-132">Requirements</span></span>  

 <span data-ttu-id="2873c-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2873c-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2873c-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2873c-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2873c-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2873c-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2873c-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2873c-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2873c-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="2873c-137">See also</span></span>

- [<span data-ttu-id="2873c-138">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="2873c-138">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)

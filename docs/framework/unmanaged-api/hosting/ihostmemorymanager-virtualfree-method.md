---
description: 了解详细信息： IHostMemoryManager：： VirtualFree 方法
title: IHostMemoryManager::VirtualFree 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualFree
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualFree
helpviewer_keywords:
- IHostMemoryManager::VirtualFree method [.NET Framework hosting]
- VirtualFree method [.NET Framework hosting]
ms.assetid: 1a436e89-eb28-4d15-bcf1-a072f86dbd99
topic_type:
- apiref
ms.openlocfilehash: 987661ce1b7bfd08f757f53082313b8eb60ff282
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707475"
---
# <a name="ihostmemorymanagervirtualfree-method"></a><span data-ttu-id="449bc-103">IHostMemoryManager::VirtualFree 方法</span><span class="sxs-lookup"><span data-stu-id="449bc-103">IHostMemoryManager::VirtualFree Method</span></span>

<span data-ttu-id="449bc-104">用作相应 Win32 函数的逻辑包装。</span><span class="sxs-lookup"><span data-stu-id="449bc-104">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="449bc-105">在 `VirtualFree` 调用进程的虚拟地址空间内释放、解除或释放和解除页区域的 Win32 实现。</span><span class="sxs-lookup"><span data-stu-id="449bc-105">The Win32 implementation of `VirtualFree` releases, decommits, or releases and decommits a region of pages within the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="449bc-106">语法</span><span class="sxs-lookup"><span data-stu-id="449bc-106">Syntax</span></span>  
  
```cpp  
HRESULT VirtualFree (  
    [in] LPVOID  lpAddress,  
    [in] SIZE_T  dwSize,  
    [in] DWORD   dwFreeType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="449bc-107">参数</span><span class="sxs-lookup"><span data-stu-id="449bc-107">Parameters</span></span>  

 `lpAddress`  
 <span data-ttu-id="449bc-108">中一个指针，指向要释放的虚拟内存页的基址。</span><span class="sxs-lookup"><span data-stu-id="449bc-108">[in] A pointer to the base address of the virtual memory pages to be freed.</span></span>  
  
 `dwSize`  
 <span data-ttu-id="449bc-109">中要释放的区域的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="449bc-109">[in] The size, in bytes, of the region to be freed.</span></span>  
  
 `dwFreeType`  
 <span data-ttu-id="449bc-110">中释放操作的类型。</span><span class="sxs-lookup"><span data-stu-id="449bc-110">[in] The type of freeing operation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="449bc-111">返回值</span><span class="sxs-lookup"><span data-stu-id="449bc-111">Return Value</span></span>  
  
|<span data-ttu-id="449bc-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="449bc-112">HRESULT</span></span>|<span data-ttu-id="449bc-113">说明</span><span class="sxs-lookup"><span data-stu-id="449bc-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="449bc-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="449bc-114">S_OK</span></span>|<span data-ttu-id="449bc-115">`VirtualFree` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="449bc-115">`VirtualFree` returned successfully.</span></span>|  
|<span data-ttu-id="449bc-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="449bc-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="449bc-117"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="449bc-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="449bc-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="449bc-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="449bc-119">调用超时。</span><span class="sxs-lookup"><span data-stu-id="449bc-119">The call timed out.</span></span>|  
|<span data-ttu-id="449bc-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="449bc-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="449bc-121">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="449bc-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="449bc-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="449bc-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="449bc-123">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="449bc-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="449bc-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="449bc-124">E_FAIL</span></span>|<span data-ttu-id="449bc-125">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="449bc-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="449bc-126">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="449bc-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="449bc-127">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="449bc-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="449bc-128">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="449bc-128">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="449bc-129">尝试释放未通过主机分配的内存。</span><span class="sxs-lookup"><span data-stu-id="449bc-129">An attempt was made to free memory that was not allocated through the host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="449bc-130">备注</span><span class="sxs-lookup"><span data-stu-id="449bc-130">Remarks</span></span>  

 <span data-ttu-id="449bc-131">`VirtualFree``lpAddress`通过对[IHostMemoryManager：： VirtualAlloc](ihostmemorymanager-virtualalloc-method.md)函数的更早调用来释放与参数关联的虚拟内存页。</span><span class="sxs-lookup"><span data-stu-id="449bc-131">`VirtualFree` frees virtual memory pages associated with the `lpAddress` parameter through an earlier call to the [IHostMemoryManager::VirtualAlloc](ihostmemorymanager-virtualalloc-method.md) function.</span></span> <span data-ttu-id="449bc-132">尝试释放未通过主机分配的内存应返回 HOST_E_INVALIDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="449bc-132">Attempts to free memory that was not allocated through the host should return HOST_E_INVALIDOPERATION.</span></span>  
  
 <span data-ttu-id="449bc-133">语义与的 Win32 实现的语义相同 `VirtualFree` 。</span><span class="sxs-lookup"><span data-stu-id="449bc-133">The semantics are identical to those of the Win32 implementation of `VirtualFree`.</span></span> <span data-ttu-id="449bc-134">有关详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="449bc-134">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="449bc-135">要求</span><span class="sxs-lookup"><span data-stu-id="449bc-135">Requirements</span></span>  

 <span data-ttu-id="449bc-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="449bc-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="449bc-137">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="449bc-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="449bc-138">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="449bc-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="449bc-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="449bc-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="449bc-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="449bc-140">See also</span></span>

- [<span data-ttu-id="449bc-141">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="449bc-141">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="449bc-142">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="449bc-142">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)

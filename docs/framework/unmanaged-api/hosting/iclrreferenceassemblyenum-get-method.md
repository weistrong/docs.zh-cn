---
description: 了解详细信息： ICLRReferenceAssemblyEnum：： Get 方法
title: ICLRReferenceAssemblyEnum::Get 方法
ms.date: 03/30/2017
api_name:
- ICLRReferenceAssemblyEnum.Get
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRReferenceAssemblyEnum::Get
helpviewer_keywords:
- ICLRReferenceAssemblyEnum::Get method [.NET Framework hosting]
- Get method, ICLRReferenceAssemblyEnum interface [.NET Framework hosting]
ms.assetid: f21c1612-9c5d-4abc-a337-577086d29c17
topic_type:
- apiref
ms.openlocfilehash: ea4e71631a9ebb381f721b78f17507603891a032
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637295"
---
# <a name="iclrreferenceassemblyenumget-method"></a><span data-ttu-id="27126-103">ICLRReferenceAssemblyEnum::Get 方法</span><span class="sxs-lookup"><span data-stu-id="27126-103">ICLRReferenceAssemblyEnum::Get Method</span></span>

<span data-ttu-id="27126-104">获取所提供索引处的程序集标识。</span><span class="sxs-lookup"><span data-stu-id="27126-104">Gets the assembly identity at the supplied index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27126-105">语法</span><span class="sxs-lookup"><span data-stu-id="27126-105">Syntax</span></span>  
  
```cpp  
HRESULT Get (  
    [in] DWORD dwIndex,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="27126-106">参数</span><span class="sxs-lookup"><span data-stu-id="27126-106">Parameters</span></span>  

 `dwIndex`  
 <span data-ttu-id="27126-107">中要返回的程序集标识的从零开始的索引。</span><span class="sxs-lookup"><span data-stu-id="27126-107">[in] The zero-based index of the assembly identity to return.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="27126-108">弄包含程序集标识数据的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="27126-108">[out] A buffer containing the assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="27126-109">[in，out]缓冲区的大小 `pwzBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="27126-109">[in, out] The size of the `pwzBuffer` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="27126-110">返回值</span><span class="sxs-lookup"><span data-stu-id="27126-110">Return Value</span></span>  
  
|<span data-ttu-id="27126-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="27126-111">HRESULT</span></span>|<span data-ttu-id="27126-112">说明</span><span class="sxs-lookup"><span data-stu-id="27126-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="27126-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="27126-113">S_OK</span></span>|<span data-ttu-id="27126-114">`Get` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="27126-114">`Get` returned successfully.</span></span>|  
|<span data-ttu-id="27126-115">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="27126-115">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="27126-116">`pwzBuffer` 太小。</span><span class="sxs-lookup"><span data-stu-id="27126-116">`pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="27126-117">ERROR_NO_MORE_ITEMS</span><span class="sxs-lookup"><span data-stu-id="27126-117">ERROR_NO_MORE_ITEMS</span></span>|<span data-ttu-id="27126-118">枚举中没有更多的项。</span><span class="sxs-lookup"><span data-stu-id="27126-118">The enumeration contains no more items.</span></span>|  
|<span data-ttu-id="27126-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="27126-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="27126-120"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="27126-120">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="27126-121">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="27126-121">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="27126-122">调用超时。</span><span class="sxs-lookup"><span data-stu-id="27126-122">The call timed out.</span></span>|  
|<span data-ttu-id="27126-123">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="27126-123">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="27126-124">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="27126-124">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="27126-125">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="27126-125">HOST_E_ABANDONED</span></span>|<span data-ttu-id="27126-126">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="27126-126">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="27126-127">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="27126-127">E_FAIL</span></span>|<span data-ttu-id="27126-128">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="27126-128">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="27126-129">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="27126-129">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="27126-130">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="27126-130">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="27126-131">备注</span><span class="sxs-lookup"><span data-stu-id="27126-131">Remarks</span></span>  

 <span data-ttu-id="27126-132">`Get` 通常称为两次。</span><span class="sxs-lookup"><span data-stu-id="27126-132">`Get` is typically called twice.</span></span> <span data-ttu-id="27126-133">第一次调用为提供 null 值 `pwzBuffer` ，并将设置 `pcchBufferSize` 为适合的大小 `pwzBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="27126-133">The first call supplies a null value for `pwzBuffer`, and sets `pcchBufferSize` to the size appropriate for `pwzBuffer`.</span></span> <span data-ttu-id="27126-134">第二个调用提供适当大小的 `pwzBuffer` ，并在完成时包含规范程序集标识数据。</span><span class="sxs-lookup"><span data-stu-id="27126-134">The second call supplies an appropriately sized `pwzBuffer`, and contains the canonical assembly identity data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27126-135">要求</span><span class="sxs-lookup"><span data-stu-id="27126-135">Requirements</span></span>  

 <span data-ttu-id="27126-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27126-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27126-137">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="27126-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="27126-138">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="27126-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="27126-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27126-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27126-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="27126-140">See also</span></span>

- [<span data-ttu-id="27126-141">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="27126-141">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="27126-142">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="27126-142">ICLRReferenceAssemblyEnum Interface</span></span>](iclrreferenceassemblyenum-interface.md)

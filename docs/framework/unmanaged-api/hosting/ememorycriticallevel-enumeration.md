---
description: 了解详细信息： EMemoryCriticalLevel 枚举
title: EMemoryCriticalLevel 枚举
ms.date: 03/30/2017
api_name:
- EMemoryCriticalLevel
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EMemoryCriticalLevel
helpviewer_keywords:
- EMemoryCriticalLevel enumeration [.NET Framework hosting]
ms.assetid: 2ca8a7a2-7b54-4ba3-8e73-277c7df485f3
topic_type:
- apiref
ms.openlocfilehash: 88965a29164de1ec7b01c2fcc8f51415127e69fd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785427"
---
# <a name="ememorycriticallevel-enumeration"></a><span data-ttu-id="8b8bc-103">EMemoryCriticalLevel 枚举</span><span class="sxs-lookup"><span data-stu-id="8b8bc-103">EMemoryCriticalLevel Enumeration</span></span>

<span data-ttu-id="8b8bc-104">包含一些值，这些值指示在请求特定内存分配但无法满足时，失败所造成的影响。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-104">Contains values that indicate the impact of a failure when a specific memory allocation has been requested but cannot be satisfied.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b8bc-105">语法</span><span class="sxs-lookup"><span data-stu-id="8b8bc-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eTaskCritical      = 0,  
    eAppDomainCritical = 1,  
    eProcessCritical   = 2  
} EMemoryCriticalLevel;  
```  
  
## <a name="members"></a><span data-ttu-id="8b8bc-106">成员</span><span class="sxs-lookup"><span data-stu-id="8b8bc-106">Members</span></span>  
  
|<span data-ttu-id="8b8bc-107">成员</span><span class="sxs-lookup"><span data-stu-id="8b8bc-107">Member</span></span>|<span data-ttu-id="8b8bc-108">说明</span><span class="sxs-lookup"><span data-stu-id="8b8bc-108">Description</span></span>|  
|------------|-----------------|  
|`eAppDomainCritical`|<span data-ttu-id="8b8bc-109">指示分配对于在已请求分配的域中执行托管代码是至关重要的。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-109">Indicates that the allocation is critical for executing managed code in the domain that has requested the allocation.</span></span> <span data-ttu-id="8b8bc-110">如果无法分配内存，则 CLR 无法保证域仍可用。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-110">If memory cannot be allocated, the CLR cannot guarantee that the domain is still usable.</span></span> <span data-ttu-id="8b8bc-111">主机决定当无法满足分配时要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-111">The host decides what action to take when the allocation cannot be satisfied.</span></span> <span data-ttu-id="8b8bc-112">它可以指示 CLR `AppDomain` 自动中止，或通过在 [ICLRPolicyManager](iclrpolicymanager-interface.md)上调用方法来使其保持运行。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-112">It can instruct the CLR to abort the `AppDomain` automatically, or allow it to keep running by calling methods on [ICLRPolicyManager](iclrpolicymanager-interface.md).</span></span>|  
|`eProcessCritical`|<span data-ttu-id="8b8bc-113">指示分配对于进程中的托管代码执行至关重要。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-113">Indicates that the allocation is critical to the execution of managed code in the process.</span></span> <span data-ttu-id="8b8bc-114">此值在启动和运行终结器时使用。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-114">This value is used during startup and when running finalizers.</span></span> <span data-ttu-id="8b8bc-115">如果无法分配内存，则 CLR 无法在进程中运行。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-115">If memory cannot be allocated, the CLR cannot operate in the process.</span></span> <span data-ttu-id="8b8bc-116">如果分配失败，则会有效地禁用 CLR。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-116">If the allocation fails, the CLR is effectively disabled.</span></span> <span data-ttu-id="8b8bc-117">对 CLR 的所有后续调用都将失败，并 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-117">All subsequent calls into the CLR fail with HOST_E_CLRNOTAVAILABLE.</span></span>|  
|`eTaskCritical`|<span data-ttu-id="8b8bc-118">指示分配对于运行已请求分配的任务至关重要。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-118">Indicates that the allocation is critical to running the task that has requested the allocation.</span></span> <span data-ttu-id="8b8bc-119">如果无法分配内存，则 CLR 无法保证任务能够执行。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-119">If memory cannot be allocated, the CLR cannot guarantee that the task can be executed.</span></span> <span data-ttu-id="8b8bc-120">发生故障时，CLR 将 <xref:System.Threading.ThreadAbortException> 在物理操作系统线程上引发。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-120">In the event of failure, the CLR raises a <xref:System.Threading.ThreadAbortException> on the physical operation system thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8b8bc-121">备注</span><span class="sxs-lookup"><span data-stu-id="8b8bc-121">Remarks</span></span>  

 <span data-ttu-id="8b8bc-122">[IHostMemoryManager](ihostmemorymanager-interface.md)和[IHostMAlloc](ihostmalloc-interface.md)接口中定义的内存分配方法采用此类型的参数。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-122">The memory allocation methods defined in the [IHostMemoryManager](ihostmemorymanager-interface.md) and [IHostMAlloc](ihostmalloc-interface.md) interfaces take a parameter of this type.</span></span> <span data-ttu-id="8b8bc-123">根据故障的严重性，主机可以决定是立即对分配请求进行故障转移还是要等待，直到它得以满足。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-123">Depending upon the severity of a failure, a host can decide whether to fail the allocation request immediately or to wait until it can be satisfied.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b8bc-124">要求</span><span class="sxs-lookup"><span data-stu-id="8b8bc-124">Requirements</span></span>  

 <span data-ttu-id="8b8bc-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8b8bc-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b8bc-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8b8bc-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8b8bc-127">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8b8bc-127">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8b8bc-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b8bc-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b8bc-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="8b8bc-129">See also</span></span>

- [<span data-ttu-id="8b8bc-130">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="8b8bc-130">ICLRMemoryNotificationCallback Interface</span></span>](iclrmemorynotificationcallback-interface.md)
- [<span data-ttu-id="8b8bc-131">承载枚举</span><span class="sxs-lookup"><span data-stu-id="8b8bc-131">Hosting Enumerations</span></span>](hosting-enumerations.md)

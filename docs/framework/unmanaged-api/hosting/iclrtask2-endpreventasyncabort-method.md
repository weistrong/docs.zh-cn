---
description: 了解详细信息： ICLRTask2：： EndPreventAsyncAbort 方法
title: ICLRTask2::EndPreventAsyncAbort 方法
ms.date: 03/30/2017
api_name:
- ICLRTask2.EndPreventAsyncAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2::EndPreventAsyncAbort
helpviewer_keywords:
- EndPreventAsyncAbort method [.NET Framework hosting]
- ICLRTask2::EndPreventAsyncAbort method [.NET Framework hosting]
ms.assetid: d8013659-e3df-44b3-814f-a6b534ce62f8
topic_type:
- apiref
ms.openlocfilehash: 964a68c1ad6d5aa6a95560d2870e135640283590
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799494"
---
# <a name="iclrtask2endpreventasyncabort-method"></a><span data-ttu-id="cd5d3-103">ICLRTask2::EndPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="cd5d3-103">ICLRTask2::EndPreventAsyncAbort Method</span></span>

<span data-ttu-id="cd5d3-104">允许新的或挂起的线程中止请求导致在当前线程上中止线程。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-104">Allows new or pending thread abort requests to result in thread aborts on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd5d3-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd5d3-105">Syntax</span></span>  
  
```cpp  
HRESULT EndPreventAsyncAbort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="cd5d3-106">返回值</span><span class="sxs-lookup"><span data-stu-id="cd5d3-106">Return Value</span></span>  

 <span data-ttu-id="cd5d3-107">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-107">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="cd5d3-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cd5d3-108">HRESULT</span></span>|<span data-ttu-id="cd5d3-109">说明</span><span class="sxs-lookup"><span data-stu-id="cd5d3-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cd5d3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd5d3-110">S_OK</span></span>|<span data-ttu-id="cd5d3-111">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-111">The method completed successfully.</span></span>|  
|<span data-ttu-id="cd5d3-112">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="cd5d3-112">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="cd5d3-113">在不是当前线程的线程上调用了方法。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-113">The method was called on a thread which is not the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd5d3-114">备注</span><span class="sxs-lookup"><span data-stu-id="cd5d3-114">Remarks</span></span>  

 <span data-ttu-id="cd5d3-115">调用此方法会将当前线程的延迟线程中止计数器减一。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-115">Calling this method decrements the delay-thread-abort counter for the current thread by one.</span></span>  
  
 <span data-ttu-id="cd5d3-116">调用 [ICLRTask2：： BeginPreventAsyncAbort](iclrtask2-beginpreventasyncabort-method.md) ， `EndPreventAsyncAbort` 可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-116">Calls to [ICLRTask2::BeginPreventAsyncAbort](iclrtask2-beginpreventasyncabort-method.md) and `EndPreventAsyncAbort` can be nested.</span></span> <span data-ttu-id="cd5d3-117">只要计数器大于零，就会延迟当前线程的线程中止。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-117">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span>  
  
 <span data-ttu-id="cd5d3-118">此功能公开的功能由虚拟机在内部使用 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-118">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="cd5d3-119">滥用这些方法可能会导致 VM 中未指定的行为。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-119">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="cd5d3-120">例如， `EndPreventAsyncAbort` 如果未通过第一次调用调用，则在 `BeginPreventAsyncAbort` VM 之前将计数器设置为零。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-120">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="cd5d3-121">同样，不检查内部计数器是否溢出。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-121">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="cd5d3-122">如果它超过其整数限制，原因是主机和 VM 均递增，则未指定产生的行为。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-122">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd5d3-123">要求</span><span class="sxs-lookup"><span data-stu-id="cd5d3-123">Requirements</span></span>  

 <span data-ttu-id="cd5d3-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd5d3-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd5d3-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cd5d3-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cd5d3-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cd5d3-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cd5d3-127">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd5d3-127">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd5d3-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd5d3-128">See also</span></span>

- [<span data-ttu-id="cd5d3-129">BeginPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="cd5d3-129">BeginPreventAsyncAbort Method</span></span>](iclrtask2-beginpreventasyncabort-method.md)
- [<span data-ttu-id="cd5d3-130">ICLRTask2 接口</span><span class="sxs-lookup"><span data-stu-id="cd5d3-130">ICLRTask2 Interface</span></span>](iclrtask2-interface.md)
- [<span data-ttu-id="cd5d3-131">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cd5d3-131">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="cd5d3-132">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="cd5d3-132">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="cd5d3-133">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cd5d3-133">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="cd5d3-134">承载接口</span><span class="sxs-lookup"><span data-stu-id="cd5d3-134">Hosting Interfaces</span></span>](hosting-interfaces.md)

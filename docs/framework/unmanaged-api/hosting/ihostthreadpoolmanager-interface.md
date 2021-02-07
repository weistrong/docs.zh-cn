---
description: 了解详细信息： IHostThreadPoolManager 接口
title: IHostThreadPoolManager 接口
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager
helpviewer_keywords:
- IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: c3a2cd90-7c4e-4374-bb87-b41befb8344f
topic_type:
- apiref
ms.openlocfilehash: 0361b7a08f781a8748e43959f65ce0e9f21bbac1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728394"
---
# <a name="ihostthreadpoolmanager-interface"></a><span data-ttu-id="25e17-103">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="25e17-103">IHostThreadPoolManager Interface</span></span>

<span data-ttu-id="25e17-104">提供一些方法，这些方法使公共语言运行时 (CLR) 配置线程池并将工作项排队到线程池。</span><span class="sxs-lookup"><span data-stu-id="25e17-104">Provides methods that enable the common language runtime (CLR) to configure the thread pool and to queue work items to the thread pool.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="25e17-105">方法</span><span class="sxs-lookup"><span data-stu-id="25e17-105">Methods</span></span>  
  
|<span data-ttu-id="25e17-106">方法</span><span class="sxs-lookup"><span data-stu-id="25e17-106">Method</span></span>|<span data-ttu-id="25e17-107">说明</span><span class="sxs-lookup"><span data-stu-id="25e17-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="25e17-108">GetAvailableThreads 方法</span><span class="sxs-lookup"><span data-stu-id="25e17-108">GetAvailableThreads Method</span></span>](ihostthreadpoolmanager-getavailablethreads-method.md)|<span data-ttu-id="25e17-109">获取线程池中当前未处理工作项的线程的数目。</span><span class="sxs-lookup"><span data-stu-id="25e17-109">Gets the number of threads in the thread pool that are not currently processing work items.</span></span>|  
|[<span data-ttu-id="25e17-110">GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="25e17-110">GetMaxThreads Method</span></span>](ihostthreadpoolmanager-getmaxthreads-method.md)|<span data-ttu-id="25e17-111">获取主机在线程池中并发维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="25e17-111">Gets the maximum number of threads that the host maintains concurrently in the thread pool.</span></span>|  
|[<span data-ttu-id="25e17-112">GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="25e17-112">GetMinThreads Method</span></span>](ihostthreadpoolmanager-getminthreads-method.md)|<span data-ttu-id="25e17-113">获取主机为获得请求而保留的空闲线程的最小数目。</span><span class="sxs-lookup"><span data-stu-id="25e17-113">Gets the minimum number of idle threads that the host maintains in anticipation of requests.</span></span>|  
|[<span data-ttu-id="25e17-114">QueueUserWorkItem 方法</span><span class="sxs-lookup"><span data-stu-id="25e17-114">QueueUserWorkItem Method</span></span>](ihostthreadpoolmanager-queueuserworkitem-method.md)|<span data-ttu-id="25e17-115">将函数排队以便执行，并提供包含函数要使用的数据的对象。</span><span class="sxs-lookup"><span data-stu-id="25e17-115">Queues a function for execution, and provides an object containing data to be used by the function.</span></span>|  
|[<span data-ttu-id="25e17-116">SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="25e17-116">SetMaxThreads Method</span></span>](ihostthreadpoolmanager-setmaxthreads-method.md)|<span data-ttu-id="25e17-117">设置宿主可在线程池中维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="25e17-117">Sets the maximum number of threads that the host can maintain in the thread pool.</span></span>|  
|[<span data-ttu-id="25e17-118">SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="25e17-118">SetMinThreads Method</span></span>](ihostthreadpoolmanager-setminthreads-method.md)|<span data-ttu-id="25e17-119">设置主机在预期请求中必须保持的空闲线程的最小数目。</span><span class="sxs-lookup"><span data-stu-id="25e17-119">Sets the minimum number of idle threads that the host must maintain in anticipation of requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="25e17-120">备注</span><span class="sxs-lookup"><span data-stu-id="25e17-120">Remarks</span></span>  

 <span data-ttu-id="25e17-121">主机不需要使用对和方法的调用中指定的值来配置线程池 `SetMaxThreads` `SetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="25e17-121">The host is not required to configure the thread pool by using the values specified in calls to the `SetMaxThreads` and `SetMinThreads` methods.</span></span> <span data-ttu-id="25e17-122">在这种情况下，宿主应从这些方法返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="25e17-122">In this case, the host should return an HRESULT value of E_NOTIMPL from these methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25e17-123">要求</span><span class="sxs-lookup"><span data-stu-id="25e17-123">Requirements</span></span>  

 <span data-ttu-id="25e17-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="25e17-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="25e17-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="25e17-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="25e17-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="25e17-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="25e17-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="25e17-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25e17-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="25e17-128">See also</span></span>

- <xref:System.Threading>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="25e17-129">承载接口</span><span class="sxs-lookup"><span data-stu-id="25e17-129">Hosting Interfaces</span></span>](hosting-interfaces.md)

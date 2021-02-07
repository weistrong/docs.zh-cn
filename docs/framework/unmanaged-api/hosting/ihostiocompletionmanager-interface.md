---
description: 了解详细信息： IHostIoCompletionManager 接口
title: IHostIoCompletionManager 接口
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager
helpviewer_keywords:
- IHostIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c28d1983-83f7-46e2-990f-dbb9dc07c818
topic_type:
- apiref
ms.openlocfilehash: 30cb0ecbfd9645bc0374e3570751832d6fa8eced
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708315"
---
# <a name="ihostiocompletionmanager-interface"></a><span data-ttu-id="038e6-103">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="038e6-103">IHostIoCompletionManager Interface</span></span>

<span data-ttu-id="038e6-104">提供一些方法，这些方法允许公共语言运行时 (CLR) 与主机提供的 i/o 完成端口交互。</span><span class="sxs-lookup"><span data-stu-id="038e6-104">Provides methods that allow the common language runtime (CLR) to interact with I/O completion ports provided by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="038e6-105">方法</span><span class="sxs-lookup"><span data-stu-id="038e6-105">Methods</span></span>  
  
|<span data-ttu-id="038e6-106">方法</span><span class="sxs-lookup"><span data-stu-id="038e6-106">Method</span></span>|<span data-ttu-id="038e6-107">说明</span><span class="sxs-lookup"><span data-stu-id="038e6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="038e6-108">Bind 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-108">Bind Method</span></span>](ihostiocompletionmanager-bind-method.md)|<span data-ttu-id="038e6-109">将句柄绑定到 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="038e6-109">Binds a handle to an I/O completion port.</span></span>|  
|[<span data-ttu-id="038e6-110">CloseIoCompletionPort 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-110">CloseIoCompletionPort Method</span></span>](ihostiocompletionmanager-closeiocompletionport-method.md)|<span data-ttu-id="038e6-111">关闭通过先前对的调用创建的端口 `CreateIoCompletionPort` 。</span><span class="sxs-lookup"><span data-stu-id="038e6-111">Closes a port that was created through an earlier call to `CreateIoCompletionPort`.</span></span>|  
|[<span data-ttu-id="038e6-112">CreateIoCompletionPort 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-112">CreateIoCompletionPort Method</span></span>](ihostiocompletionmanager-createiocompletionport-method.md)|<span data-ttu-id="038e6-113">请求宿主创建新的 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="038e6-113">Requests that the host create a new I/O completion port.</span></span>|  
|[<span data-ttu-id="038e6-114">GetAvailableThreads 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-114">GetAvailableThreads Method</span></span>](ihostiocompletionmanager-getavailablethreads-method.md)|<span data-ttu-id="038e6-115">获取当前未处理请求的 i/o 完成线程数。</span><span class="sxs-lookup"><span data-stu-id="038e6-115">Gets the number of I/O completion threads that are not currently processing requests.</span></span>|  
|[<span data-ttu-id="038e6-116">GetHostOverlappedSize 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-116">GetHostOverlappedSize Method</span></span>](ihostiocompletionmanager-gethostoverlappedsize-method.md)|<span data-ttu-id="038e6-117">获取宿主打算追加到 i/o 请求的任何自定义数据的大小。</span><span class="sxs-lookup"><span data-stu-id="038e6-117">Gets the size of any custom data the host intends to append to I/O requests.</span></span>|  
|[<span data-ttu-id="038e6-118">GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-118">GetMaxThreads Method</span></span>](ihostiocompletionmanager-getmaxthreads-method.md)|<span data-ttu-id="038e6-119">获取主机可为服务 i/o 请求分配的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="038e6-119">Gets the maximum number of threads that the host can allot to service I/O requests.</span></span>|  
|[<span data-ttu-id="038e6-120">GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-120">GetMinThreads Method</span></span>](ihostiocompletionmanager-getminthreads-method.md)|<span data-ttu-id="038e6-121">获取主机提供的用于处理 i/o 请求的最小线程数。</span><span class="sxs-lookup"><span data-stu-id="038e6-121">Gets the minimum number of threads that the host provides to service I/O requests.</span></span>|  
|[<span data-ttu-id="038e6-122">InitializeHostOverlapped 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-122">InitializeHostOverlapped Method</span></span>](ihostiocompletionmanager-initializehostoverlapped-method.md)|<span data-ttu-id="038e6-123">向宿主提供初始化有关 i/o 请求的任何自定义数据的机会。</span><span class="sxs-lookup"><span data-stu-id="038e6-123">Provides the host with an opportunity to initialize any custom data about an I/O request.</span></span>|  
|[<span data-ttu-id="038e6-124">SetCLRIoCompletionManager 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-124">SetCLRIoCompletionManager Method</span></span>](ihostiocompletionmanager-setclriocompletionmanager-method.md)|<span data-ttu-id="038e6-125">向宿主提供一个接口指针，该指针指向 CLR 实现的 [ICLRIoCompletionManager](iclriocompletionmanager-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="038e6-125">Provides the host with an interface pointer to an [ICLRIoCompletionManager](iclriocompletionmanager-interface.md) instance implemented by the CLR.</span></span>|  
|[<span data-ttu-id="038e6-126">SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-126">SetMaxThreads Method</span></span>](ihostiocompletionmanager-setmaxthreads-method.md)|<span data-ttu-id="038e6-127">设置主机 allots i/o 请求的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="038e6-127">Sets the maximum number of threads that the host allots to service I/O requests.</span></span>|  
|[<span data-ttu-id="038e6-128">SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="038e6-128">SetMinThreads Method</span></span>](ihostiocompletionmanager-setminthreads-method.md)|<span data-ttu-id="038e6-129">设置主机应为 i/o 完成分配的最小线程数。</span><span class="sxs-lookup"><span data-stu-id="038e6-129">Sets the minimum number of threads that the host should allot to I/O completion.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="038e6-130">备注</span><span class="sxs-lookup"><span data-stu-id="038e6-130">Remarks</span></span>  

 <span data-ttu-id="038e6-131">`IHostIoCompletionManager` 对应于 `ICLRIoCompletionManager` CLR 实现的接口。</span><span class="sxs-lookup"><span data-stu-id="038e6-131">`IHostIoCompletionManager` corresponds to the `ICLRIoCompletionManager` interface implemented by the CLR.</span></span> <span data-ttu-id="038e6-132">CLR 调用的方法将 `IHostIoCompletionManager` 句柄绑定到主机提供的端口，并且宿主将调用的方法 `ICLRIoCompletionManager` 来报告 i/o 请求的完成。</span><span class="sxs-lookup"><span data-stu-id="038e6-132">The CLR calls the methods of `IHostIoCompletionManager` to bind handles to the ports that the host provides, and the host calls the methods of `ICLRIoCompletionManager` to report the completion of I/O requests.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="038e6-133">要求</span><span class="sxs-lookup"><span data-stu-id="038e6-133">Requirements</span></span>  

 <span data-ttu-id="038e6-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="038e6-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="038e6-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="038e6-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="038e6-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="038e6-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="038e6-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="038e6-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="038e6-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="038e6-138">See also</span></span>

- [<span data-ttu-id="038e6-139">承载接口</span><span class="sxs-lookup"><span data-stu-id="038e6-139">Hosting Interfaces</span></span>](hosting-interfaces.md)

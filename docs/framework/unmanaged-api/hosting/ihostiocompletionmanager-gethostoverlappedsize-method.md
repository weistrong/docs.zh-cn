---
description: 了解详细信息： IHostIoCompletionManager：： GetHostOverlappedSize 方法
title: IHostIoCompletionManager::GetHostOverlappedSize 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.GetHostOverlappedSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::GetHostOverlappedSize
helpviewer_keywords:
- IHostIoCompletionManager::GetHostOverlappedSize method [.NET Framework hosting]
- GetHostOverlappedSize method [.NET Framework hosting]
ms.assetid: 2902578b-d5e2-4f8d-a103-0c7b6dceda9e
topic_type:
- apiref
ms.openlocfilehash: 2a2ebe1da82c5702269b634eadfe98b72739e3df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708540"
---
# <a name="ihostiocompletionmanagergethostoverlappedsize-method"></a><span data-ttu-id="84ae2-103">IHostIoCompletionManager::GetHostOverlappedSize 方法</span><span class="sxs-lookup"><span data-stu-id="84ae2-103">IHostIoCompletionManager::GetHostOverlappedSize Method</span></span>

<span data-ttu-id="84ae2-104">获取宿主打算追加到 i/o 请求的任何自定义数据的大小。</span><span class="sxs-lookup"><span data-stu-id="84ae2-104">Gets the size of any custom data the host intends to append to I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84ae2-105">语法</span><span class="sxs-lookup"><span data-stu-id="84ae2-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHostOverlappedSize (  
    [out] DWORD *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84ae2-106">参数</span><span class="sxs-lookup"><span data-stu-id="84ae2-106">Parameters</span></span>  

 `pcbSize`  
 <span data-ttu-id="84ae2-107">弄一个指针，它指向公共语言运行时 (CLR) 应分配的字节数，以及 Win32 对象的大小 `OVERLAPPED` 。</span><span class="sxs-lookup"><span data-stu-id="84ae2-107">[out] A pointer to the number of bytes that the common language runtime (CLR) should allocate in addition to the size of the Win32 `OVERLAPPED` object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="84ae2-108">返回值</span><span class="sxs-lookup"><span data-stu-id="84ae2-108">Return Value</span></span>  
  
|<span data-ttu-id="84ae2-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="84ae2-109">HRESULT</span></span>|<span data-ttu-id="84ae2-110">说明</span><span class="sxs-lookup"><span data-stu-id="84ae2-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="84ae2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="84ae2-111">S_OK</span></span>|<span data-ttu-id="84ae2-112">`GetHostOverlappedSize` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="84ae2-112">`GetHostOverlappedSize` returned successfully.</span></span>|  
|<span data-ttu-id="84ae2-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="84ae2-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="84ae2-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="84ae2-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="84ae2-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="84ae2-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="84ae2-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="84ae2-116">The call timed out.</span></span>|  
|<span data-ttu-id="84ae2-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="84ae2-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="84ae2-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="84ae2-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="84ae2-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="84ae2-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="84ae2-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="84ae2-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="84ae2-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="84ae2-121">E_FAIL</span></span>|<span data-ttu-id="84ae2-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="84ae2-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="84ae2-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="84ae2-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="84ae2-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="84ae2-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="84ae2-125">备注</span><span class="sxs-lookup"><span data-stu-id="84ae2-125">Remarks</span></span>  

 <span data-ttu-id="84ae2-126">对 Windows 平台 Api 的所有异步 i/o 调用都采用 Win32 `OVERLAPPED` 对象，后者提供了文件指针位置等信息。</span><span class="sxs-lookup"><span data-stu-id="84ae2-126">All asynchronous I/O calls to Windows Platform APIs take a Win32 `OVERLAPPED` object, which provides information such as the file pointer position.</span></span> <span data-ttu-id="84ae2-127">若要维护状态，执行异步 i/o 调用的应用程序通常会将自定义数据添加到该结构中。</span><span class="sxs-lookup"><span data-stu-id="84ae2-127">To maintain state, applications that make asynchronous I/O calls typically add custom data to the structure.</span></span> <span data-ttu-id="84ae2-128">`GetHostOverlappedSize` 和 [IHostIoCompletionManager：： InitializeHostOverlapped](ihostiocompletionmanager-initializehostoverlapped-method.md) 为主机提供了一个机会，使其包括此类自定义数据。</span><span class="sxs-lookup"><span data-stu-id="84ae2-128">`GetHostOverlappedSize` and [IHostIoCompletionManager::InitializeHostOverlapped](ihostiocompletionmanager-initializehostoverlapped-method.md) provide an opportunity for the host to include such custom data.</span></span>  
  
 <span data-ttu-id="84ae2-129">CLR 调用 `GetHostOverlappedSize` 方法来确定宿主打算追加到对象的自定义数据的大小 `OVERLAPPED` 。</span><span class="sxs-lookup"><span data-stu-id="84ae2-129">The CLR calls the `GetHostOverlappedSize` method to determine the size of the custom data that the host intends to append to the `OVERLAPPED` object.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="84ae2-130">`GetHostOverlappedSize` 只调用一次。</span><span class="sxs-lookup"><span data-stu-id="84ae2-130">`GetHostOverlappedSize` is called only once.</span></span> <span data-ttu-id="84ae2-131">主机的自定义数据必须与每个 i/o 请求的大小相同。</span><span class="sxs-lookup"><span data-stu-id="84ae2-131">The host's custom data must be the same size for every I/O request.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="84ae2-132">对象本身的大小 `OVERLAPPED` 不包含在的值中 `pcbSize` 。</span><span class="sxs-lookup"><span data-stu-id="84ae2-132">The size of the `OVERLAPPED` object itself is not included in the value of `pcbSize`.</span></span>  
  
 <span data-ttu-id="84ae2-133">有关结构的详细信息 `OVERLAPPED` ，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="84ae2-133">For more information about the `OVERLAPPED` structure, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84ae2-134">要求</span><span class="sxs-lookup"><span data-stu-id="84ae2-134">Requirements</span></span>  

 <span data-ttu-id="84ae2-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84ae2-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84ae2-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="84ae2-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="84ae2-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="84ae2-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="84ae2-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84ae2-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84ae2-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="84ae2-139">See also</span></span>

- <xref:System.Threading.NativeOverlapped>
- [<span data-ttu-id="84ae2-140">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="84ae2-140">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="84ae2-141">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="84ae2-141">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)

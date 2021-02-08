---
description: 了解详细信息： ICLRRuntimeHost：： Stop 方法
title: ICLRRuntimeHost::Stop 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.Stop
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::Stop
helpviewer_keywords:
- ICLRRuntimeHost::Stop method [.NET Framework hosting]
- Stop method, ICLRRuntimeHost interface [.NET Framework hosting]
ms.assetid: b8fd7daf-8f8d-4ad7-92ae-019db244cec1
topic_type:
- apiref
ms.openlocfilehash: 3e6b1cf2aee95af6354905f6dcdcb678ff785aa6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799716"
---
# <a name="iclrruntimehoststop-method"></a><span data-ttu-id="91ee6-103">ICLRRuntimeHost::Stop 方法</span><span class="sxs-lookup"><span data-stu-id="91ee6-103">ICLRRuntimeHost::Stop Method</span></span>

<span data-ttu-id="91ee6-104"> (CLR) ，停止由公共语言运行时执行代码。</span><span class="sxs-lookup"><span data-stu-id="91ee6-104">Stops the execution of code by the common language runtime (CLR).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="91ee6-105">此方法不会向主机释放资源、卸载应用程序域或销毁线程。</span><span class="sxs-lookup"><span data-stu-id="91ee6-105">This method does not release resources to the host, unload application domains, or destroy threads.</span></span> <span data-ttu-id="91ee6-106">必须终止进程才能释放这些资源。</span><span class="sxs-lookup"><span data-stu-id="91ee6-106">You must terminate the process to release these resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91ee6-107">语法</span><span class="sxs-lookup"><span data-stu-id="91ee6-107">Syntax</span></span>  
  
```cpp  
HRESULT Stop();  
```  
  
## <a name="return-value"></a><span data-ttu-id="91ee6-108">返回值</span><span class="sxs-lookup"><span data-stu-id="91ee6-108">Return Value</span></span>  
  
|<span data-ttu-id="91ee6-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="91ee6-109">HRESULT</span></span>|<span data-ttu-id="91ee6-110">说明</span><span class="sxs-lookup"><span data-stu-id="91ee6-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="91ee6-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="91ee6-111">S_OK</span></span>|<span data-ttu-id="91ee6-112">`Stop` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="91ee6-112">`Stop` returned successfully.</span></span>|  
|<span data-ttu-id="91ee6-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="91ee6-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="91ee6-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="91ee6-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="91ee6-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="91ee6-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="91ee6-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="91ee6-116">The call timed out.</span></span>|  
|<span data-ttu-id="91ee6-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="91ee6-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="91ee6-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="91ee6-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="91ee6-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="91ee6-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="91ee6-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="91ee6-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="91ee6-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="91ee6-121">E_FAIL</span></span>|<span data-ttu-id="91ee6-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="91ee6-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="91ee6-123">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="91ee6-123">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="91ee6-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="91ee6-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="91ee6-125">要求</span><span class="sxs-lookup"><span data-stu-id="91ee6-125">Requirements</span></span>  

 <span data-ttu-id="91ee6-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91ee6-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91ee6-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="91ee6-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="91ee6-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="91ee6-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="91ee6-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91ee6-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91ee6-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="91ee6-130">See also</span></span>

- [<span data-ttu-id="91ee6-131">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="91ee6-131">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)

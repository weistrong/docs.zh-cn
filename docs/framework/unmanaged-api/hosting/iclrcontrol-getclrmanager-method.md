---
description: 了解详细信息： ICLRControl：： GetCLRManager 方法
title: ICLRControl::GetCLRManager 方法
ms.date: 03/30/2017
api_name:
- ICLRControl.GetCLRManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl::GetCLRManager
helpviewer_keywords:
- GetCLRManager method [.NET Framework hosting]
- ICLRControl::GetCLRManager method [.NET Framework hosting]
ms.assetid: 8a11bfa4-cbb0-4082-82b5-f9fba66c93f5
topic_type:
- apiref
ms.openlocfilehash: fc24cbdfd4bebfff5c2f8d73a9cd6961a8c94e94
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716713"
---
# <a name="iclrcontrolgetclrmanager-method"></a><span data-ttu-id="33cc9-103">ICLRControl::GetCLRManager 方法</span><span class="sxs-lookup"><span data-stu-id="33cc9-103">ICLRControl::GetCLRManager Method</span></span>

<span data-ttu-id="33cc9-104">获取一个接口指针，该指针指向主机可用于配置公共语言运行时 (CLR) 的任何管理器类型的实例。</span><span class="sxs-lookup"><span data-stu-id="33cc9-104">Gets an interface pointer to an instance of any of the manager types the host can use to configure the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33cc9-105">语法</span><span class="sxs-lookup"><span data-stu-id="33cc9-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCLRManager (  
    [in]  REFIID  riid,  
    [out] void  **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="33cc9-106">参数</span><span class="sxs-lookup"><span data-stu-id="33cc9-106">Parameters</span></span>  

 `riid`  
 <span data-ttu-id="33cc9-107">中 `IID` 要返回的管理器类型的。</span><span class="sxs-lookup"><span data-stu-id="33cc9-107">[in] The `IID` of the manager type to return.</span></span> <span data-ttu-id="33cc9-108">支持以下 `IID` 值。</span><span class="sxs-lookup"><span data-stu-id="33cc9-108">The following `IID` values are supported.</span></span>  
  
- <span data-ttu-id="33cc9-109">IID_ICLRDebugManager：指定 `ppObject` 将为 [ICLRDebugManager](iclrdebugmanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-109">IID_ICLRDebugManager: Specifies that `ppObject` will be of type [ICLRDebugManager](iclrdebugmanager-interface.md).</span></span>  
  
- <span data-ttu-id="33cc9-110">IID_ICLRErrorReportingManager：指定 `ppObject` 将为 [ICLRErrorReportingManager](iclrerrorreportingmanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-110">IID_ICLRErrorReportingManager: Specifies that `ppObject` will be of type [ICLRErrorReportingManager](iclrerrorreportingmanager-interface.md).</span></span>  
  
- <span data-ttu-id="33cc9-111">IID_ICLRGCManager：指定 `ppObject` 将为 [ICLRGCManager](iclrgcmanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-111">IID_ICLRGCManager: Specifies that `ppObject` will be of type [ICLRGCManager](iclrgcmanager-interface.md).</span></span>  
  
- <span data-ttu-id="33cc9-112">IID_ICLRHostProtectionManager：指定 `ppObject` 将为 [ICLRHostProtectionManager](iclrhostprotectionmanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-112">IID_ICLRHostProtectionManager: Specifies that `ppObject` will be of type [ICLRHostProtectionManager](iclrhostprotectionmanager-interface.md).</span></span>  
  
- <span data-ttu-id="33cc9-113">IID_ICLROnEventManager：指定 `ppObject` 将为 [ICLROnEventManager](iclroneventmanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-113">IID_ICLROnEventManager: Specifies that `ppObject` will be of type [ICLROnEventManager](iclroneventmanager-interface.md).</span></span>  
  
- <span data-ttu-id="33cc9-114">IID_ICLRPolicyManager：指定 `ppObject` 将为 [ICLRPolicyManager](iclrpolicymanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-114">IID_ICLRPolicyManager: Specifies that `ppObject` will be of type [ICLRPolicyManager](iclrpolicymanager-interface.md).</span></span>  
  
- <span data-ttu-id="33cc9-115">IID_ICLRTaskManager：指定 `ppObject` 将为 [ICLRTaskManager](iclrtaskmanager-interface.md)类型。</span><span class="sxs-lookup"><span data-stu-id="33cc9-115">IID_ICLRTaskManager: Specifies that `ppObject` will be of type [ICLRTaskManager](iclrtaskmanager-interface.md).</span></span>  
  
 `ppObject`  
 <span data-ttu-id="33cc9-116">弄指向请求的管理器的接口指针; 如果请求的管理器类型无效，则为 null。</span><span class="sxs-lookup"><span data-stu-id="33cc9-116">[out] An interface pointer to the requested manager, or null, if an invalid manager type was requested.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="33cc9-117">返回值</span><span class="sxs-lookup"><span data-stu-id="33cc9-117">Return Value</span></span>  
  
|<span data-ttu-id="33cc9-118">HRESULT</span><span class="sxs-lookup"><span data-stu-id="33cc9-118">HRESULT</span></span>|<span data-ttu-id="33cc9-119">说明</span><span class="sxs-lookup"><span data-stu-id="33cc9-119">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="33cc9-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="33cc9-120">S_OK</span></span>|<span data-ttu-id="33cc9-121">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="33cc9-121">The method returned successfully.</span></span>|  
|<span data-ttu-id="33cc9-122">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="33cc9-122">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="33cc9-123">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="33cc9-123">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="33cc9-124">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="33cc9-124">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="33cc9-125">调用超时。</span><span class="sxs-lookup"><span data-stu-id="33cc9-125">The call timed out.</span></span>|  
|<span data-ttu-id="33cc9-126">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="33cc9-126">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="33cc9-127">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="33cc9-127">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="33cc9-128">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="33cc9-128">HOST_E_ABANDONED</span></span>|<span data-ttu-id="33cc9-129">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="33cc9-129">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="33cc9-130">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="33cc9-130">E_FAIL</span></span>|<span data-ttu-id="33cc9-131">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="33cc9-131">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="33cc9-132">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="33cc9-132">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="33cc9-133">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="33cc9-133">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="33cc9-134">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="33cc9-134">E_NOINTERFACE</span></span>|<span data-ttu-id="33cc9-135">接口类型不受支持。</span><span class="sxs-lookup"><span data-stu-id="33cc9-135">The interface type is not supported.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="33cc9-136">要求</span><span class="sxs-lookup"><span data-stu-id="33cc9-136">Requirements</span></span>  

 <span data-ttu-id="33cc9-137">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="33cc9-137">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33cc9-138">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="33cc9-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="33cc9-139">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="33cc9-139">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="33cc9-140">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33cc9-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33cc9-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="33cc9-141">See also</span></span>

- [<span data-ttu-id="33cc9-142">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="33cc9-142">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="33cc9-143">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="33cc9-143">IHostControl Interface</span></span>](ihostcontrol-interface.md)

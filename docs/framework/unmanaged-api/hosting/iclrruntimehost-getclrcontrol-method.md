---
description: 了解详细信息： ICLRRuntimeHost：： GetCLRControl 方法
title: ICLRRuntimeHost::GetCLRControl 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.GetCLRControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::GetCLRControl
helpviewer_keywords:
- ICLRRuntimeHost::GetCLRControl method [.NET Framework hosting]
- GetCLRControl method [.NET Framework hosting]
ms.assetid: e47e3655-efd5-4572-a1dc-50c69bf2a468
topic_type:
- apiref
ms.openlocfilehash: 832ae03c0126f0c08afa9b5c0312a636ec1de294
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753922"
---
# <a name="iclrruntimehostgetclrcontrol-method"></a><span data-ttu-id="7bd2e-103">ICLRRuntimeHost::GetCLRControl 方法</span><span class="sxs-lookup"><span data-stu-id="7bd2e-103">ICLRRuntimeHost::GetCLRControl Method</span></span>

<span data-ttu-id="7bd2e-104">获取 [ICLRControl 接口](iclrcontrol-interface.md) 类型的接口指针，宿主可以使用该接口自定义公共语言运行时 (CLR) 的各个方面。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-104">Gets an interface pointer of type [ICLRControl Interface](iclrcontrol-interface.md) that hosts can use to customize aspects of the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bd2e-105">语法</span><span class="sxs-lookup"><span data-stu-id="7bd2e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCLRControl(  
    [out] ICLRControl** pCLRControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7bd2e-106">参数</span><span class="sxs-lookup"><span data-stu-id="7bd2e-106">Parameters</span></span>  

 `pCLRControl`  
 <span data-ttu-id="7bd2e-107">弄类型为 [ICLRControl 接口](iclrcontrol-interface.md) 的接口指针，该接口允许主机配置 CLR 的其他方面。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-107">[out] An interface pointer of type [ICLRControl Interface](iclrcontrol-interface.md) that enables hosts to configure additional aspects of the CLR.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7bd2e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="7bd2e-108">Return Value</span></span>  
  
|<span data-ttu-id="7bd2e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7bd2e-109">HRESULT</span></span>|<span data-ttu-id="7bd2e-110">说明</span><span class="sxs-lookup"><span data-stu-id="7bd2e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7bd2e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bd2e-111">S_OK</span></span>|<span data-ttu-id="7bd2e-112">`GetCLRControl` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-112">`GetCLRControl` returned successfully.</span></span>|  
|<span data-ttu-id="7bd2e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7bd2e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7bd2e-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7bd2e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7bd2e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7bd2e-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-116">The call timed out.</span></span>|  
|<span data-ttu-id="7bd2e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7bd2e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7bd2e-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7bd2e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7bd2e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7bd2e-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7bd2e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7bd2e-121">E_FAIL</span></span>|<span data-ttu-id="7bd2e-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7bd2e-123">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-123">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7bd2e-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="7bd2e-125">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="7bd2e-125">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="7bd2e-126">CLR 已经开始。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-126">The CLR has already started.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7bd2e-127">备注</span><span class="sxs-lookup"><span data-stu-id="7bd2e-127">Remarks</span></span>  

 <span data-ttu-id="7bd2e-128">`ICLRControl` 提供 [GetCLRManager 方法](iclrcontrol-getclrmanager-method.md) ，该方法使宿主可以获取指向某个管理器类型的接口指针。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-128">`ICLRControl` provides the [GetCLRManager Method](iclrcontrol-getclrmanager-method.md) method, which enables the host to get an interface pointer to one of the manager types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7bd2e-129">要求</span><span class="sxs-lookup"><span data-stu-id="7bd2e-129">Requirements</span></span>  

 <span data-ttu-id="7bd2e-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7bd2e-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7bd2e-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7bd2e-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7bd2e-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7bd2e-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7bd2e-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7bd2e-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bd2e-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bd2e-134">See also</span></span>

- [<span data-ttu-id="7bd2e-135">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="7bd2e-135">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="7bd2e-136">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="7bd2e-136">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)

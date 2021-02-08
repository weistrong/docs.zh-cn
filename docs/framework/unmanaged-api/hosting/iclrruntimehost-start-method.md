---
description: 了解详细信息： ICLRRuntimeHost：： Start 方法
title: ICLRRuntimeHost::Start 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::Start
helpviewer_keywords:
- ICLRRuntimeHost::Start method [.NET Framework hosting]
- Start method, ICLRRuntimeHost interface [.NET Framework hosting]
ms.assetid: c0a6dce5-0a8d-42e8-808b-6ca14df9d289
topic_type:
- apiref
ms.openlocfilehash: 0ada729c9a90b23fb1573a2101845028e5e2fe76
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785076"
---
# <a name="iclrruntimehoststart-method"></a><span data-ttu-id="41f0f-103">ICLRRuntimeHost::Start 方法</span><span class="sxs-lookup"><span data-stu-id="41f0f-103">ICLRRuntimeHost::Start Method</span></span>

<span data-ttu-id="41f0f-104">将 CLR)  (公共语言运行时初始化为一个进程。</span><span class="sxs-lookup"><span data-stu-id="41f0f-104">Initializes the common language runtime (CLR) into a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41f0f-105">语法</span><span class="sxs-lookup"><span data-stu-id="41f0f-105">Syntax</span></span>  
  
```cpp  
HRESULT Start();  
```  
  
## <a name="return-value"></a><span data-ttu-id="41f0f-106">返回值</span><span class="sxs-lookup"><span data-stu-id="41f0f-106">Return Value</span></span>  
  
|<span data-ttu-id="41f0f-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="41f0f-107">HRESULT</span></span>|<span data-ttu-id="41f0f-108">说明</span><span class="sxs-lookup"><span data-stu-id="41f0f-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="41f0f-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="41f0f-109">S_OK</span></span>|<span data-ttu-id="41f0f-110">`Start` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="41f0f-110">`Start` returned successfully.</span></span>|  
|<span data-ttu-id="41f0f-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="41f0f-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="41f0f-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="41f0f-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="41f0f-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="41f0f-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="41f0f-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="41f0f-114">The call timed out.</span></span>|  
|<span data-ttu-id="41f0f-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="41f0f-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="41f0f-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="41f0f-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="41f0f-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="41f0f-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="41f0f-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="41f0f-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="41f0f-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="41f0f-119">E_FAIL</span></span>|<span data-ttu-id="41f0f-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="41f0f-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="41f0f-121">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="41f0f-121">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="41f0f-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="41f0f-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="41f0f-123">备注</span><span class="sxs-lookup"><span data-stu-id="41f0f-123">Remarks</span></span>  

 <span data-ttu-id="41f0f-124">在许多情况下，不需要调用 `Start` ，因为运行时将在首次运行托管代码请求时自动初始化自身。</span><span class="sxs-lookup"><span data-stu-id="41f0f-124">In many scenarios it is not necessary to call `Start`, because the runtime will initialize itself automatically upon the first request to run managed code.</span></span> <span data-ttu-id="41f0f-125">但是，可以使用 `Start` 来准确指定运行时应初始化的时间。</span><span class="sxs-lookup"><span data-stu-id="41f0f-125">You can, however, use `Start` to specify exactly when the runtime should be initialized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41f0f-126">要求</span><span class="sxs-lookup"><span data-stu-id="41f0f-126">Requirements</span></span>  

 <span data-ttu-id="41f0f-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="41f0f-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41f0f-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="41f0f-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="41f0f-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="41f0f-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="41f0f-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41f0f-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41f0f-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="41f0f-131">See also</span></span>

- <xref:System.AppDomain>
- [<span data-ttu-id="41f0f-132">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="41f0f-132">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)

---
description: 了解详细信息： ICLRHostProtectionManager：： SetEagerSerializeGrantSets 方法
title: ICLRHostProtectionManager::SetEagerSerializeGrantSets 方法
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager.SetEagerSerializeGrantSets
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager::SetEagerSerializeGrantSets
helpviewer_keywords:
- SetEagerSerializeGrantSets method [.NET Framework hosting]
- ICLRHostProtectionManager::SetEagerSerializeGrantSets method [.NET Framework hosting]
ms.assetid: d6158360-22b1-4ace-ad85-d830b9964783
topic_type:
- apiref
ms.openlocfilehash: 04eb00b1422523e8057c3a0fc27dfe7e49f98f08
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789902"
---
# <a name="iclrhostprotectionmanagerseteagerserializegrantsets-method"></a><span data-ttu-id="a1d90-103">ICLRHostProtectionManager::SetEagerSerializeGrantSets 方法</span><span class="sxs-lookup"><span data-stu-id="a1d90-103">ICLRHostProtectionManager::SetEagerSerializeGrantSets Method</span></span>

<span data-ttu-id="a1d90-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="a1d90-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1d90-105">语法</span><span class="sxs-lookup"><span data-stu-id="a1d90-105">Syntax</span></span>  
  
```cpp  
HRESULT SetEagerSerializeGrantSets ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="a1d90-106">返回值</span><span class="sxs-lookup"><span data-stu-id="a1d90-106">Return Value</span></span>  
  
|<span data-ttu-id="a1d90-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a1d90-107">HRESULT</span></span>|<span data-ttu-id="a1d90-108">说明</span><span class="sxs-lookup"><span data-stu-id="a1d90-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a1d90-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1d90-109">S_OK</span></span>|<span data-ttu-id="a1d90-110">`SetEagerSerializeGrantSets` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a1d90-110">`SetEagerSerializeGrantSets` returned successfully.</span></span>|  
|<span data-ttu-id="a1d90-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a1d90-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a1d90-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a1d90-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a1d90-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a1d90-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a1d90-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="a1d90-114">The call timed out.</span></span>|  
|<span data-ttu-id="a1d90-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a1d90-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a1d90-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a1d90-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a1d90-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a1d90-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a1d90-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="a1d90-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a1d90-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a1d90-119">E_FAIL</span></span>|<span data-ttu-id="a1d90-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a1d90-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a1d90-121">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="a1d90-121">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a1d90-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a1d90-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a1d90-123">要求</span><span class="sxs-lookup"><span data-stu-id="a1d90-123">Requirements</span></span>  

 <span data-ttu-id="a1d90-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1d90-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1d90-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a1d90-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a1d90-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a1d90-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a1d90-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1d90-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1d90-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1d90-128">See also</span></span>

- [<span data-ttu-id="a1d90-129">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="a1d90-129">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="a1d90-130">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="a1d90-130">ICLRHostProtectionManager Interface</span></span>](iclrhostprotectionmanager-interface.md)

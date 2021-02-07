---
description: 了解详细信息： ICLRErrorReportingManager：： EndCustomDump 方法
title: ICLRErrorReportingManager::EndCustomDump 方法
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.EndCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::EndCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::EndCustomDump method [.NET Framework hosting]
- EndCustomDump method [.NET Framework hosting]
ms.assetid: 88a5da04-8729-4108-82c4-af206a7d483e
topic_type:
- apiref
ms.openlocfilehash: 406d7d77f4cd63c69fec56acb0819d56c6271630
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689464"
---
# <a name="iclrerrorreportingmanagerendcustomdump-method"></a><span data-ttu-id="8c373-103">ICLRErrorReportingManager::EndCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="8c373-103">ICLRErrorReportingManager::EndCustomDump Method</span></span>

<span data-ttu-id="8c373-104">删除在先前对 [ICLRErrorReportingManager：： BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) 方法的调用中指定的自定义堆栈转储配置。</span><span class="sxs-lookup"><span data-stu-id="8c373-104">Removes the custom stack dump configuration that was specified in an earlier call to the [ICLRErrorReportingManager::BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c373-105">语法</span><span class="sxs-lookup"><span data-stu-id="8c373-105">Syntax</span></span>  
  
```cpp  
HRESULT EndCustomDump ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="8c373-106">返回值</span><span class="sxs-lookup"><span data-stu-id="8c373-106">Return Value</span></span>  
  
|<span data-ttu-id="8c373-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8c373-107">HRESULT</span></span>|<span data-ttu-id="8c373-108">说明</span><span class="sxs-lookup"><span data-stu-id="8c373-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8c373-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c373-109">S_OK</span></span>|<span data-ttu-id="8c373-110">`EndCustomDump` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="8c373-110">`EndCustomDump` returned successfully.</span></span>|  
|<span data-ttu-id="8c373-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8c373-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8c373-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="8c373-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8c373-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8c373-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8c373-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="8c373-114">The call timed out.</span></span>|  
|<span data-ttu-id="8c373-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8c373-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8c373-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="8c373-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8c373-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8c373-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8c373-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="8c373-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8c373-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8c373-119">E_FAIL</span></span>|<span data-ttu-id="8c373-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="8c373-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8c373-121">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="8c373-121">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8c373-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="8c373-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8c373-123">备注</span><span class="sxs-lookup"><span data-stu-id="8c373-123">Remarks</span></span>  

 <span data-ttu-id="8c373-124">`EndCustomDump`方法通过对方法的更早调用来清除自定义堆栈转储配置 `BeginCustomDump` ，并释放任何关联的状态。</span><span class="sxs-lookup"><span data-stu-id="8c373-124">The `EndCustomDump` method clears the custom stack dump configuration set by an earlier call to the `BeginCustomDump` method and frees any associated state.</span></span> <span data-ttu-id="8c373-125">应在自定义堆栈转储完成后调用它。</span><span class="sxs-lookup"><span data-stu-id="8c373-125">It should be called after the custom stack dump is complete.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="8c373-126">调用失败 `EndCustomDump` 会导致内存泄露。</span><span class="sxs-lookup"><span data-stu-id="8c373-126">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8c373-127">要求</span><span class="sxs-lookup"><span data-stu-id="8c373-127">Requirements</span></span>  

 <span data-ttu-id="8c373-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8c373-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8c373-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8c373-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8c373-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8c373-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8c373-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8c373-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c373-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="8c373-132">See also</span></span>

- [<span data-ttu-id="8c373-133">CustomDumpItem 结构</span><span class="sxs-lookup"><span data-stu-id="8c373-133">CustomDumpItem Structure</span></span>](customdumpitem-structure.md)
- [<span data-ttu-id="8c373-134">ECustomDumpFlavor 枚举</span><span class="sxs-lookup"><span data-stu-id="8c373-134">ECustomDumpFlavor Enumeration</span></span>](ecustomdumpflavor-enumeration.md)
- [<span data-ttu-id="8c373-135">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="8c373-135">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)

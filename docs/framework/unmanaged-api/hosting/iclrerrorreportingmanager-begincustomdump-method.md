---
description: 了解详细信息： ICLRErrorReportingManager：： BeginCustomDump 方法
title: ICLRErrorReportingManager::BeginCustomDump 方法
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.BeginCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::BeginCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::BeginCustomDump method [.NET Framework hosting]
- BeginCustomDump method
ms.assetid: 93424a87-ba13-4fa1-b4dc-69d44437b7ae
topic_type:
- apiref
ms.openlocfilehash: 3f8498068d50ffc6ea00cf4f08f969c92f010d6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689477"
---
# <a name="iclrerrorreportingmanagerbegincustomdump-method"></a><span data-ttu-id="4b31b-103">ICLRErrorReportingManager::BeginCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="4b31b-103">ICLRErrorReportingManager::BeginCustomDump Method</span></span>

<span data-ttu-id="4b31b-104">指定用于错误报告的自定义堆转储配置。</span><span class="sxs-lookup"><span data-stu-id="4b31b-104">Specifies the configuration of custom heap dumps for error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b31b-105">语法</span><span class="sxs-lookup"><span data-stu-id="4b31b-105">Syntax</span></span>  
  
```cpp  
HRESULT BeginCustomDump (  
    [in] ECustomDumpFlavor dwFlavor,  
    [in] DWORD dwNumItems,  
    [in, size_is(dwNumItems), length_is(dwNumItems)] CustomDumpItem items[],  
    DWORD dwReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b31b-106">参数</span><span class="sxs-lookup"><span data-stu-id="4b31b-106">Parameters</span></span>  

 `dwFlavor`  
 <span data-ttu-id="4b31b-107">中一个 [ECustomDumpFlavor](ecustomdumpflavor-enumeration.md) 值，指示用于生成自定义堆转储的堆转储的种类。</span><span class="sxs-lookup"><span data-stu-id="4b31b-107">[in] A [ECustomDumpFlavor](ecustomdumpflavor-enumeration.md) value that indicates the kind of heap dump upon which to build the custom heap dump.</span></span>  
  
 `dwNumItems`  
 <span data-ttu-id="4b31b-108">中数组的长度 `items` 。</span><span class="sxs-lookup"><span data-stu-id="4b31b-108">[in] The length of the `items` array.</span></span> <span data-ttu-id="4b31b-109">如果 `dwFlavor` 不是 DUMP_FLAVOR_Mini，则 `dwNumItems` 应为零。</span><span class="sxs-lookup"><span data-stu-id="4b31b-109">If `dwFlavor` is not DUMP_FLAVOR_Mini, `dwNumItems` should be zero.</span></span>  
  
 `items`  
 <span data-ttu-id="4b31b-110">中 [CustomDumpItem](customdumpitem-structure.md) 实例的数组，指定要添加到小型转储中的项。</span><span class="sxs-lookup"><span data-stu-id="4b31b-110">[in] An array of [CustomDumpItem](customdumpitem-structure.md) instances, specifying the items to add to the mini-dump.</span></span> <span data-ttu-id="4b31b-111">如果 `dwFlavor` 不 DUMP_FLAVOR_Mini，则 `items` 应为 null。</span><span class="sxs-lookup"><span data-stu-id="4b31b-111">If `dwFlavor` is not DUMP_FLAVOR_Mini, `items` should be null.</span></span>  
  
 `dwReserved`  
 <span data-ttu-id="4b31b-112">中保留供将来使用。</span><span class="sxs-lookup"><span data-stu-id="4b31b-112">[in] Reserved for future use.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b31b-113">返回值</span><span class="sxs-lookup"><span data-stu-id="4b31b-113">Return Value</span></span>  
  
|<span data-ttu-id="4b31b-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4b31b-114">HRESULT</span></span>|<span data-ttu-id="4b31b-115">说明</span><span class="sxs-lookup"><span data-stu-id="4b31b-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4b31b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b31b-116">S_OK</span></span>|<span data-ttu-id="4b31b-117">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="4b31b-117">The method returned successfully.</span></span>|  
|<span data-ttu-id="4b31b-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="4b31b-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="4b31b-119"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="4b31b-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="4b31b-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="4b31b-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="4b31b-121">调用超时。</span><span class="sxs-lookup"><span data-stu-id="4b31b-121">The call timed out.</span></span>|  
|<span data-ttu-id="4b31b-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="4b31b-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="4b31b-123">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="4b31b-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="4b31b-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="4b31b-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="4b31b-125">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="4b31b-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="4b31b-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="4b31b-126">E_FAIL</span></span>|<span data-ttu-id="4b31b-127">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="4b31b-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="4b31b-128">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="4b31b-128">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="4b31b-129">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="4b31b-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4b31b-130">备注</span><span class="sxs-lookup"><span data-stu-id="4b31b-130">Remarks</span></span>  

 <span data-ttu-id="4b31b-131">`BeginCustomDump`方法设置自定义堆转储配置。</span><span class="sxs-lookup"><span data-stu-id="4b31b-131">The `BeginCustomDump` method sets custom heap dump configuration.</span></span> <span data-ttu-id="4b31b-132">[EndCustomDump](iclrerrorreportingmanager-endcustomdump-method.md)方法清除自定义堆转储配置并释放任何关联的状态。</span><span class="sxs-lookup"><span data-stu-id="4b31b-132">The [EndCustomDump](iclrerrorreportingmanager-endcustomdump-method.md) method clears the custom heap dump configuration and frees any associated state.</span></span> <span data-ttu-id="4b31b-133">应在自定义堆转储完成后调用它。</span><span class="sxs-lookup"><span data-stu-id="4b31b-133">It should be called after the custom heap dump is complete.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="4b31b-134">调用失败 `EndCustomDump` 会导致内存泄露。</span><span class="sxs-lookup"><span data-stu-id="4b31b-134">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b31b-135">要求</span><span class="sxs-lookup"><span data-stu-id="4b31b-135">Requirements</span></span>  

 <span data-ttu-id="4b31b-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4b31b-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b31b-137">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="4b31b-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4b31b-138">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4b31b-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4b31b-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b31b-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b31b-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b31b-140">See also</span></span>

- [<span data-ttu-id="4b31b-141">CustomDumpItem 结构</span><span class="sxs-lookup"><span data-stu-id="4b31b-141">CustomDumpItem Structure</span></span>](customdumpitem-structure.md)
- [<span data-ttu-id="4b31b-142">ECustomDumpFlavor 枚举</span><span class="sxs-lookup"><span data-stu-id="4b31b-142">ECustomDumpFlavor Enumeration</span></span>](ecustomdumpflavor-enumeration.md)
- [<span data-ttu-id="4b31b-143">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="4b31b-143">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)

---
description: 了解详细信息： ICLRRuntimeInfo：： GetInterface 方法
title: ICLRRuntimeInfo::GetInterface 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetInterface
helpviewer_keywords:
- GetInterface method [.NET Framework hosting]
- ICLRRuntimeInfo::GetInterface method [.NET Framework hosting]
ms.assetid: cc7b0e5b-48c3-4509-8ebb-611ddb1f7ec2
topic_type:
- apiref
ms.openlocfilehash: 5a5c55823ff9954735a712423d8aaab1256c947d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637113"
---
# <a name="iclrruntimeinfogetinterface-method"></a><span data-ttu-id="9e5e4-103">ICLRRuntimeInfo::GetInterface 方法</span><span class="sxs-lookup"><span data-stu-id="9e5e4-103">ICLRRuntimeInfo::GetInterface Method</span></span>

<span data-ttu-id="9e5e4-104">将 CLR 加载到当前进程并返回运行时接口指针，如 [ICLRRuntimeHost](iclrruntimehost-interface.md)、 [ICLRStrongName](iclrstrongname-interface.md)和 [IMetaDataDispenserEx](../metadata/imetadatadispenser-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-104">Loads the CLR into the current process and returns runtime interface pointers, such as [ICLRRuntimeHost](iclrruntimehost-interface.md), [ICLRStrongName](iclrstrongname-interface.md), and [IMetaDataDispenserEx](../metadata/imetadatadispenser-interface.md).</span></span>  
  
 <span data-ttu-id="9e5e4-105">此方法取代 `CorBindTo` [弃用的 CLR 承载函数](deprecated-clr-hosting-functions.md) 部分中的所有 \* 函数。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-105">This method supersedes all the `CorBindTo`\* functions in the [Deprecated CLR Hosting Functions](deprecated-clr-hosting-functions.md) section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e5e4-106">语法</span><span class="sxs-lookup"><span data-stu-id="9e5e4-106">Syntax</span></span>  
  
```cpp  
HRESULT GetInterface(  
[in]  REFCLSID rclsid,  
[in]  REFIID   riid,  
[out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9e5e4-107">参数</span><span class="sxs-lookup"><span data-stu-id="9e5e4-107">Parameters</span></span>  

 `rclsid`  
 <span data-ttu-id="9e5e4-108">中Coclass 的 CLSID 接口。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-108">[in] The CLSID interface for the coclass.</span></span>  
  
 `riid`  
 <span data-ttu-id="9e5e4-109">中所请求的接口的 IID `rclsid` 。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-109">[in] The IID of the requested `rclsid` interface.</span></span>  
  
 `ppUnk`  
 <span data-ttu-id="9e5e4-110">弄指向查询的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-110">[out] A pointer to the queried interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9e5e4-111">返回值</span><span class="sxs-lookup"><span data-stu-id="9e5e4-111">Return Value</span></span>  

 <span data-ttu-id="9e5e4-112">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-112">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="9e5e4-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9e5e4-113">HRESULT</span></span>|<span data-ttu-id="9e5e4-114">说明</span><span class="sxs-lookup"><span data-stu-id="9e5e4-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9e5e4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e5e4-115">S_OK</span></span>|<span data-ttu-id="9e5e4-116">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-116">The method completed successfully.</span></span>|  
|<span data-ttu-id="9e5e4-117">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="9e5e4-117">E_POINTER</span></span>|<span data-ttu-id="9e5e4-118">`ppUnk` 为 null。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-118">`ppUnk` is null.</span></span>|  
|<span data-ttu-id="9e5e4-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="9e5e4-119">E_OUTOFMEMORY</span></span>|<span data-ttu-id="9e5e4-120">没有足够的内存可用来处理请求。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-120">Not enough memory is available to handle the request.</span></span>|  
|<span data-ttu-id="9e5e4-121">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="9e5e4-121">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="9e5e4-122">已将其他运行时绑定到旧版 CLR 版本2激活策略。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-122">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9e5e4-123">备注</span><span class="sxs-lookup"><span data-stu-id="9e5e4-123">Remarks</span></span>  

 <span data-ttu-id="9e5e4-124">此方法导致加载但不初始化 CLR。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-124">This method causes the CLR to be loaded but not initialized.</span></span>  
  
 <span data-ttu-id="9e5e4-125">下表显示了和支持的组合 `rclsid` `riid` 。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-125">The following table shows the supported combinations for `rclsid` and `riid`.</span></span>  
  
|`rclsid`|`riid`|  
|--------------|------------|  
|<span data-ttu-id="9e5e4-126">CLSID_CorMetaDataDispenser</span><span class="sxs-lookup"><span data-stu-id="9e5e4-126">CLSID_CorMetaDataDispenser</span></span>|<span data-ttu-id="9e5e4-127">IID_IMetaDataDispenser，IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="9e5e4-127">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="9e5e4-128">CLSID_CorMetaDataDispenserRuntime</span><span class="sxs-lookup"><span data-stu-id="9e5e4-128">CLSID_CorMetaDataDispenserRuntime</span></span>|<span data-ttu-id="9e5e4-129">IID_IMetaDataDispenser，IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="9e5e4-129">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="9e5e4-130">CLSID_CorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="9e5e4-130">CLSID_CorRuntimeHost</span></span>|<span data-ttu-id="9e5e4-131">IID_ICorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="9e5e4-131">IID_ICorRuntimeHost</span></span>|  
|<span data-ttu-id="9e5e4-132">CLSID_CLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="9e5e4-132">CLSID_CLRRuntimeHost</span></span>|<span data-ttu-id="9e5e4-133">IID_ICLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="9e5e4-133">IID_ICLRRuntimeHost</span></span>|  
|<span data-ttu-id="9e5e4-134">CLSID_TypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="9e5e4-134">CLSID_TypeNameFactory</span></span>|<span data-ttu-id="9e5e4-135">IID_ITypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="9e5e4-135">IID_ITypeNameFactory</span></span>|  
|<span data-ttu-id="9e5e4-136">CLSID_CLRDebuggingLegacy</span><span class="sxs-lookup"><span data-stu-id="9e5e4-136">CLSID_CLRDebuggingLegacy</span></span>|<span data-ttu-id="9e5e4-137">IID_ICorDebug</span><span class="sxs-lookup"><span data-stu-id="9e5e4-137">IID_ICorDebug</span></span>|  
|||  
|<span data-ttu-id="9e5e4-138">CLSID_CLRStrongName</span><span class="sxs-lookup"><span data-stu-id="9e5e4-138">CLSID_CLRStrongName</span></span>|<span data-ttu-id="9e5e4-139">IID_ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="9e5e4-139">IID_ICLRStrongName</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9e5e4-140">要求</span><span class="sxs-lookup"><span data-stu-id="9e5e4-140">Requirements</span></span>  

 <span data-ttu-id="9e5e4-141">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9e5e4-141">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9e5e4-142">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="9e5e4-142">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="9e5e4-143">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9e5e4-143">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9e5e4-144">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9e5e4-144">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e5e4-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="9e5e4-145">See also</span></span>

- [<span data-ttu-id="9e5e4-146">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="9e5e4-146">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="9e5e4-147">承载接口</span><span class="sxs-lookup"><span data-stu-id="9e5e4-147">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="9e5e4-148">承载</span><span class="sxs-lookup"><span data-stu-id="9e5e4-148">Hosting</span></span>](index.md)

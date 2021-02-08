---
description: 了解详细信息： ICLRRuntimeInfo：： IsLoaded 方法
title: ICLRRuntimeInfo::IsLoaded 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsLoaded
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsLoaded
helpviewer_keywords:
- IsLoaded method [.NET Framework hosting]
- ICLRRuntimeInfo::IsLoaded method [.NET Framework hosting]
ms.assetid: fdc5a3a7-71ff-4025-99a1-59e4ee0bfe1b
topic_type:
- apiref
ms.openlocfilehash: e6a5984dbd2340fe07af546dd48ae6760d5b4271
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799694"
---
# <a name="iclrruntimeinfoisloaded-method"></a><span data-ttu-id="67ff4-103">ICLRRuntimeInfo::IsLoaded 方法</span><span class="sxs-lookup"><span data-stu-id="67ff4-103">ICLRRuntimeInfo::IsLoaded Method</span></span>

<span data-ttu-id="67ff4-104">指示公共语言运行时 (与 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口关联的 CLR) 是否已加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="67ff4-104">Indicates whether the common language runtime (CLR) associated with the [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface is loaded into a process.</span></span> <span data-ttu-id="67ff4-105">可以在不启动的情况下加载运行时。</span><span class="sxs-lookup"><span data-stu-id="67ff4-105">A runtime can be loaded without also being started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67ff4-106">语法</span><span class="sxs-lookup"><span data-stu-id="67ff4-106">Syntax</span></span>  
  
```cpp  
HRESULT IsLoaded(  
[in]  HANDLE hndProcess,  
[out, retval] BOOL *pbLoaded);  
```  
  
## <a name="parameters"></a><span data-ttu-id="67ff4-107">参数</span><span class="sxs-lookup"><span data-stu-id="67ff4-107">Parameters</span></span>  

 `hndProcess`  
 <span data-ttu-id="67ff4-108">中进程的句柄。</span><span class="sxs-lookup"><span data-stu-id="67ff4-108">[in] A handle to the process.</span></span>  
  
 `pbLoaded`  
 <span data-ttu-id="67ff4-109">[out] `true` 如果 CLR 加载到进程中，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="67ff4-109">[out] `true` if the CLR is loaded into the process; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="67ff4-110">返回值</span><span class="sxs-lookup"><span data-stu-id="67ff4-110">Return Value</span></span>  

 <span data-ttu-id="67ff4-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="67ff4-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="67ff4-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="67ff4-112">HRESULT</span></span>|<span data-ttu-id="67ff4-113">说明</span><span class="sxs-lookup"><span data-stu-id="67ff4-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="67ff4-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="67ff4-114">S_OK</span></span>|<span data-ttu-id="67ff4-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="67ff4-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="67ff4-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="67ff4-116">E_POINTER</span></span>|<span data-ttu-id="67ff4-117">`pbLoaded` 为 null。</span><span class="sxs-lookup"><span data-stu-id="67ff4-117">`pbLoaded` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="67ff4-118">备注</span><span class="sxs-lookup"><span data-stu-id="67ff4-118">Remarks</span></span>  

 <span data-ttu-id="67ff4-119">此方法与以下函数和接口向后兼容：</span><span class="sxs-lookup"><span data-stu-id="67ff4-119">This method is backward-compatible with the following functions and interfaces:</span></span>  
  
- <span data-ttu-id="67ff4-120">[ICorRuntimeHost](icorruntimehost-interface.md) 接口在 .NET Framework 版本1宿主 API) 中 (。</span><span class="sxs-lookup"><span data-stu-id="67ff4-120">[ICorRuntimeHost](icorruntimehost-interface.md) interface (in the .NET Framework version 1 hosting API).</span></span>  
  
- <span data-ttu-id="67ff4-121">.NET Framework 2.0 托管 API) 中 ([ICLRRuntimeHost](iclrruntimehost-interface.md)接口。</span><span class="sxs-lookup"><span data-stu-id="67ff4-121">[ICLRRuntimeHost](iclrruntimehost-interface.md) interface (in the .NET Framework 2.0 hosting API).</span></span>  
  
- <span data-ttu-id="67ff4-122">弃用 `CorBindTo*` 的函数 (参阅 .NET Framework 2.0 托管 API) 中 [弃用的 CLR 承载函数](deprecated-clr-hosting-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="67ff4-122">Deprecated `CorBindTo*` functions (see [Deprecated CLR Hosting Functions](deprecated-clr-hosting-functions.md) in the .NET Framework 2.0 hosting API).</span></span>  
  
 <span data-ttu-id="67ff4-123">宿主可以调用某个弃用的函数（ `CorBindTo*` 如 [CorBindToRuntime](corbindtoruntime-function.md) 函数）来实例化特定版本的 CLR。</span><span class="sxs-lookup"><span data-stu-id="67ff4-123">A host may call one of the deprecated `CorBindTo*` functions, such as the [CorBindToRuntime](corbindtoruntime-function.md) function, to instantiate a specific version of the CLR.</span></span> <span data-ttu-id="67ff4-124">然后，宿主可以调用 [ICLRMetaHost：： GetRuntime](iclrmetahost-getruntime-method.md) 方法，并指定相同的版本号以获取 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="67ff4-124">The host could then call the [ICLRMetaHost::GetRuntime](iclrmetahost-getruntime-method.md) method and specify the same version number to obtain a [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="67ff4-125">如果宿主在 `IsLoaded` 返回的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口上调用方法，则 `pbLoaded` 返回 `true` ; 否则返回 `false` 。</span><span class="sxs-lookup"><span data-stu-id="67ff4-125">If the host then calls the `IsLoaded` method on the returned [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface, `pbLoaded` returns `true`; otherwise, it returns `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67ff4-126">要求</span><span class="sxs-lookup"><span data-stu-id="67ff4-126">Requirements</span></span>  

 <span data-ttu-id="67ff4-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="67ff4-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67ff4-128">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="67ff4-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="67ff4-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="67ff4-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="67ff4-130">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67ff4-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67ff4-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="67ff4-131">See also</span></span>

- [<span data-ttu-id="67ff4-132">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="67ff4-132">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="67ff4-133">承载接口</span><span class="sxs-lookup"><span data-stu-id="67ff4-133">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="67ff4-134">承载</span><span class="sxs-lookup"><span data-stu-id="67ff4-134">Hosting</span></span>](index.md)

---
description: 了解详细信息： ICLRMetaHost：： RequestRuntimeLoadedNotification 方法
title: ICLRMetaHost::RequestRuntimeLoadedNotification 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.RequestRuntimeLoadedNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::RequestRuntimeLoadedNotification
helpviewer_keywords:
- RequestRuntimeLoadedNotification method [.NET Framework hosting]
- ICLRMetaHost::RequestRuntimeLoadedNotification method [.NET Framework hosting]
ms.assetid: 0d5ccc4d-0193-41f5-af54-45d7b70d5321
topic_type:
- apiref
ms.openlocfilehash: c385d2d845642605ad47944794f6274e8d472071
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637490"
---
# <a name="iclrmetahostrequestruntimeloadednotification-method"></a><span data-ttu-id="37d18-103">ICLRMetaHost::RequestRuntimeLoadedNotification 方法</span><span class="sxs-lookup"><span data-stu-id="37d18-103">ICLRMetaHost::RequestRuntimeLoadedNotification Method</span></span>

<span data-ttu-id="37d18-104">提供一个回调函数，在公共语言运行时 (CLR) 版本第一次加载但尚未启动时，保证调用此函数。</span><span class="sxs-lookup"><span data-stu-id="37d18-104">Provides a callback function that is guaranteed to be called when a common language runtime (CLR) version is first loaded, but not yet started.</span></span> <span data-ttu-id="37d18-105">此方法取代了 [LockClrVersion](lockclrversion-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="37d18-105">This method supersedes the [LockClrVersion](lockclrversion-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37d18-106">语法</span><span class="sxs-lookup"><span data-stu-id="37d18-106">Syntax</span></span>  
  
```cpp  
HRESULT RequestRuntimeLoadedNotification (  
    [in] RuntimeLoadedCallbackFnPtr pCallbackFunction);  
```  
  
## <a name="parameters"></a><span data-ttu-id="37d18-107">参数</span><span class="sxs-lookup"><span data-stu-id="37d18-107">Parameters</span></span>  

 `pCallbackFunction`  
 <span data-ttu-id="37d18-108">中已加载新的运行时调用的回调函数。</span><span class="sxs-lookup"><span data-stu-id="37d18-108">[in] The callback function that is invoked when a new runtime has been loaded.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="37d18-109">返回值</span><span class="sxs-lookup"><span data-stu-id="37d18-109">Return Value</span></span>  

 <span data-ttu-id="37d18-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="37d18-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="37d18-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="37d18-111">HRESULT</span></span>|<span data-ttu-id="37d18-112">说明</span><span class="sxs-lookup"><span data-stu-id="37d18-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="37d18-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="37d18-113">S_OK</span></span>|<span data-ttu-id="37d18-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="37d18-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="37d18-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="37d18-115">E_POINTER</span></span>|<span data-ttu-id="37d18-116">`pCallbackFunction` 为 null。</span><span class="sxs-lookup"><span data-stu-id="37d18-116">`pCallbackFunction` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="37d18-117">备注</span><span class="sxs-lookup"><span data-stu-id="37d18-117">Remarks</span></span>  

 <span data-ttu-id="37d18-118">回调的工作方式如下：</span><span class="sxs-lookup"><span data-stu-id="37d18-118">The callback works in the following way:</span></span>  
  
- <span data-ttu-id="37d18-119">只有首次加载运行时才会调用回调。</span><span class="sxs-lookup"><span data-stu-id="37d18-119">The callback is invoked only when a runtime is loaded for the first time.</span></span>  
  
- <span data-ttu-id="37d18-120">对于同一运行时的可重入加载，不调用回调。</span><span class="sxs-lookup"><span data-stu-id="37d18-120">The callback is not invoked for reentrant loads of the same runtime.</span></span>  
  
- <span data-ttu-id="37d18-121">对于非重入的运行时加载，对回调函数的调用将进行序列化。</span><span class="sxs-lookup"><span data-stu-id="37d18-121">For non-reentrant runtime loads, calls to the callback function are serialized.</span></span>  
  
 <span data-ttu-id="37d18-122">回调函数具有以下原型：</span><span class="sxs-lookup"><span data-stu-id="37d18-122">The callback function has the following prototype:</span></span>  
  
```cpp  
typedef void (__stdcall *RuntimeLoadedCallbackFnPtr)(  
                     ICLRRuntimeInfo *pRuntimeInfo,  
                     CallbackThreadSetFnPtr pfnCallbackThreadSet,  
                     CallbackThreadUnsetFnPtr pfnCallbackThreadUnset);  
```  
  
 <span data-ttu-id="37d18-123">回调函数的原型如下所示：</span><span class="sxs-lookup"><span data-stu-id="37d18-123">The callback function prototypes are as follows:</span></span>  
  
- <span data-ttu-id="37d18-124">`pfnCallbackThreadSet`:</span><span class="sxs-lookup"><span data-stu-id="37d18-124">`pfnCallbackThreadSet`:</span></span>  
  
    ```cpp  
    typedef HRESULT (__stdcall *CallbackThreadSetFnPtr)();  
    ```  
  
- <span data-ttu-id="37d18-125">`pfnCallbackThreadUnset`:</span><span class="sxs-lookup"><span data-stu-id="37d18-125">`pfnCallbackThreadUnset`:</span></span>  
  
    ```cpp  
    typedef HRESULT (__stdcall *CallbackThreadUnsetFnPtr)();  
    ```  
  
 <span data-ttu-id="37d18-126">如果宿主打算加载或导致以重入方式加载另一个运行时，则 `pfnCallbackThreadSet` `pfnCallbackThreadUnset` 必须按以下方式使用回调函数中提供的和参数：</span><span class="sxs-lookup"><span data-stu-id="37d18-126">If the host intends to load or cause another runtime to be loaded in a reentrant manner, the `pfnCallbackThreadSet` and `pfnCallbackThreadUnset` parameters that are provided in the callback function must be used in the following way:</span></span>  
  
- <span data-ttu-id="37d18-127">`pfnCallbackThreadSet` 在尝试执行此类加载之前，必须由可能导致运行时加载的线程调用。</span><span class="sxs-lookup"><span data-stu-id="37d18-127">`pfnCallbackThreadSet` must be called by the thread that might cause a runtime load before such a load is attempted.</span></span>  
  
- <span data-ttu-id="37d18-128">`pfnCallbackThreadUnset` 当线程不再导致此类运行时加载 (和从初始回调) 返回之前，必须调用。</span><span class="sxs-lookup"><span data-stu-id="37d18-128">`pfnCallbackThreadUnset` must be called when the thread will no longer cause such a runtime load (and before returning from the initial callback).</span></span>  
  
- <span data-ttu-id="37d18-129">`pfnCallbackThreadSet` 和 `pfnCallbackThreadUnset` 都是不可重入的。</span><span class="sxs-lookup"><span data-stu-id="37d18-129">`pfnCallbackThreadSet` and `pfnCallbackThreadUnset` are both non-reentrant.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="37d18-130">主机应用程序不得调用 `pfnCallbackThreadSet` `pfnCallbackThreadUnset` 参数范围和参数范围之外的 `pCallbackFunction` 。</span><span class="sxs-lookup"><span data-stu-id="37d18-130">Host applications must not call `pfnCallbackThreadSet` and `pfnCallbackThreadUnset` outside the scope of the `pCallbackFunction` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="37d18-131">要求</span><span class="sxs-lookup"><span data-stu-id="37d18-131">Requirements</span></span>  

 <span data-ttu-id="37d18-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="37d18-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="37d18-133">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="37d18-133">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="37d18-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="37d18-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="37d18-135">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37d18-135">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37d18-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="37d18-136">See also</span></span>

- [<span data-ttu-id="37d18-137">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="37d18-137">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="37d18-138">承载</span><span class="sxs-lookup"><span data-stu-id="37d18-138">Hosting</span></span>](index.md)

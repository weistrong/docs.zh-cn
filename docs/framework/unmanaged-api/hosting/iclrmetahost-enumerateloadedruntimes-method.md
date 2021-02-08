---
description: 了解详细信息： ICLRMetaHost：： EnumerateLoadedRuntimes 方法
title: ICLRMetaHost::EnumerateLoadedRuntimes 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.EnumerateLoadedRuntimes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::EnumerateLoadedRuntimes
helpviewer_keywords:
- EnumerateLoadedRuntimes method [.NET Framework hosting]
- ICLRMetaHost::EnumerateLoadedRuntimes method [.NET Framework hosting]
ms.assetid: 22fc0a3f-dce4-4766-9a3c-9fab15f4b4ca
topic_type:
- apiref
ms.openlocfilehash: 508c4daca7e34366e0da35591f4e7a780301e823
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789861"
---
# <a name="iclrmetahostenumerateloadedruntimes-method"></a><span data-ttu-id="a77a9-103">ICLRMetaHost::EnumerateLoadedRuntimes 方法</span><span class="sxs-lookup"><span data-stu-id="a77a9-103">ICLRMetaHost::EnumerateLoadedRuntimes Method</span></span>

<span data-ttu-id="a77a9-104">返回一个枚举，其中包含给定进程中加载 (CLR) 的每个版本的公共语言运行时的有效 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口指针。</span><span class="sxs-lookup"><span data-stu-id="a77a9-104">Returns an enumeration that includes a valid [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface pointer for each version of the common language runtime (CLR) that is loaded in a given process.</span></span> <span data-ttu-id="a77a9-105">此方法取代了 [GetVersionFromProcess](getversionfromprocess-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="a77a9-105">This method supersedes the [GetVersionFromProcess](getversionfromprocess-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a77a9-106">语法</span><span class="sxs-lookup"><span data-stu-id="a77a9-106">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateLoadedRuntimes (  
    [in] HANDLE hndProcess,  
    [out, retval] IEnumUnknown **ppEnumerator  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a77a9-107">参数</span><span class="sxs-lookup"><span data-stu-id="a77a9-107">Parameters</span></span>  

 `hndProcess`  
 <span data-ttu-id="a77a9-108">中要检查加载的运行时的进程的句柄。</span><span class="sxs-lookup"><span data-stu-id="a77a9-108">[in] The handle of the process to inspect for loaded runtimes.</span></span>  
  
 `ppEnumerator`  
 <span data-ttu-id="a77a9-109">弄 <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown> 与进程加载的每个 CLR 相对应的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口的枚举。</span><span class="sxs-lookup"><span data-stu-id="a77a9-109">[out] An <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown> enumeration of [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interfaces corresponding to each CLR that is loaded by the process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a77a9-110">返回值</span><span class="sxs-lookup"><span data-stu-id="a77a9-110">Return Value</span></span>  

 <span data-ttu-id="a77a9-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="a77a9-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="a77a9-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a77a9-112">HRESULT</span></span>|<span data-ttu-id="a77a9-113">说明</span><span class="sxs-lookup"><span data-stu-id="a77a9-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a77a9-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a77a9-114">S_OK</span></span>|<span data-ttu-id="a77a9-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a77a9-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="a77a9-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="a77a9-116">E_POINTER</span></span>|<span data-ttu-id="a77a9-117">`ppEnumerator` 为 null。</span><span class="sxs-lookup"><span data-stu-id="a77a9-117">`ppEnumerator` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a77a9-118">备注</span><span class="sxs-lookup"><span data-stu-id="a77a9-118">Remarks</span></span>  

 <span data-ttu-id="a77a9-119">此方法列出所有加载的运行时，即使它们是用弃用的函数（如 [CorBindToRuntime](corbindtoruntime-function.md)）加载的。</span><span class="sxs-lookup"><span data-stu-id="a77a9-119">This method is lists all loaded runtimes, even if they were loaded with deprecated functions such as [CorBindToRuntime](corbindtoruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a77a9-120">要求</span><span class="sxs-lookup"><span data-stu-id="a77a9-120">Requirements</span></span>  

 <span data-ttu-id="a77a9-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a77a9-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a77a9-122">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="a77a9-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a77a9-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a77a9-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a77a9-124">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a77a9-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a77a9-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="a77a9-125">See also</span></span>

- [<span data-ttu-id="a77a9-126">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="a77a9-126">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="a77a9-127">承载</span><span class="sxs-lookup"><span data-stu-id="a77a9-127">Hosting</span></span>](index.md)

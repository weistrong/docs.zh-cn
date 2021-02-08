---
description: 了解详细信息： ICLRRuntimeInfo：： LoadLibrary 方法
title: ICLRRuntimeInfo::LoadLibrary 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.LoadLibrary
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::LoadLibrary
helpviewer_keywords:
- ICLRRuntimeInfo::LoadLibrary method [.NET Framework hosting]
- LoadLibrary method [.NET Framework hosting]
ms.assetid: 4517ada3-4417-4ac5-a150-73da7a87c686
topic_type:
- apiref
ms.openlocfilehash: 47557934868c7c1b68b23bf4eded0e90705d7252
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785050"
---
# <a name="iclrruntimeinfoloadlibrary-method"></a><span data-ttu-id="babf2-103">ICLRRuntimeInfo::LoadLibrary 方法</span><span class="sxs-lookup"><span data-stu-id="babf2-103">ICLRRuntimeInfo::LoadLibrary Method</span></span>

<span data-ttu-id="babf2-104">从公共语言运行时加载 .NET Framework 库， (CLR) 用 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口表示。</span><span class="sxs-lookup"><span data-stu-id="babf2-104">Loads a .NET Framework library from the common language runtime (CLR) represented by an [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="babf2-105">此方法取代了 [LoadLibraryShim](loadlibraryshim-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="babf2-105">This method supersedes the [LoadLibraryShim](loadlibraryshim-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="babf2-106">语法</span><span class="sxs-lookup"><span data-stu-id="babf2-106">Syntax</span></span>  
  
```cpp  
HRESULT LoadLibrary(  
     [in]  LPCWSTR pwzDllName,  
     [out, retval] HMODULE *phndModule);  
```  
  
## <a name="parameters"></a><span data-ttu-id="babf2-107">参数</span><span class="sxs-lookup"><span data-stu-id="babf2-107">Parameters</span></span>  

 `pwzDllName`  
 <span data-ttu-id="babf2-108">中要加载的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="babf2-108">[in] The name of the assembly to be loaded.</span></span>  
  
 `phndModule`  
 <span data-ttu-id="babf2-109">弄已加载的程序集的句柄。</span><span class="sxs-lookup"><span data-stu-id="babf2-109">[out] A handle to the loaded assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="babf2-110">返回值</span><span class="sxs-lookup"><span data-stu-id="babf2-110">Return Value</span></span>  

 <span data-ttu-id="babf2-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="babf2-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="babf2-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="babf2-112">HRESULT</span></span>|<span data-ttu-id="babf2-113">说明</span><span class="sxs-lookup"><span data-stu-id="babf2-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="babf2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="babf2-114">S_OK</span></span>|<span data-ttu-id="babf2-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="babf2-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="babf2-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="babf2-116">E_POINTER</span></span>|<span data-ttu-id="babf2-117">`pwzDllName` 或 `phndModule` 为 null。</span><span class="sxs-lookup"><span data-stu-id="babf2-117">`pwzDllName` or `phndModule` is null.</span></span>|  
|<span data-ttu-id="babf2-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="babf2-118">E_OUTOFMEMORY</span></span>|<span data-ttu-id="babf2-119">没有足够的内存可用来处理请求。</span><span class="sxs-lookup"><span data-stu-id="babf2-119">Not enough memory is available to handle the request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="babf2-120">备注</span><span class="sxs-lookup"><span data-stu-id="babf2-120">Remarks</span></span>  

 <span data-ttu-id="babf2-121">此方法仅加载 .NET Framework 可再发行组件包中包含的 Dll。</span><span class="sxs-lookup"><span data-stu-id="babf2-121">This method only loads DLLs included in the .NET Framework redistributable package.</span></span> <span data-ttu-id="babf2-122">它无法加载用户生成的程序集。</span><span class="sxs-lookup"><span data-stu-id="babf2-122">It can not load user-generated assemblies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="babf2-123">要求</span><span class="sxs-lookup"><span data-stu-id="babf2-123">Requirements</span></span>  

 <span data-ttu-id="babf2-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="babf2-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="babf2-125">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="babf2-125">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="babf2-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="babf2-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="babf2-127">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="babf2-127">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="babf2-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="babf2-128">See also</span></span>

- [<span data-ttu-id="babf2-129">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="babf2-129">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="babf2-130">承载接口</span><span class="sxs-lookup"><span data-stu-id="babf2-130">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="babf2-131">承载</span><span class="sxs-lookup"><span data-stu-id="babf2-131">Hosting</span></span>](index.md)

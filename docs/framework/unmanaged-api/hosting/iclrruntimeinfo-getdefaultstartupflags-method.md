---
description: 了解详细信息： ICLRRuntimeInfo：： GetDefaultStartupFlags 方法
title: ICLRRuntimeInfo::GetDefaultStartupFlags 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetDefaultStartupFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetDefaultStartupFlags
helpviewer_keywords:
- ICLRRuntimeInfo::GetDefaultStartupFlags method [.NET Framework hosting]
- GetDefaultStartupFlags method [.NET Framework hosting]
ms.assetid: 35c2173e-3b0b-4b2a-950d-e0a01c6df052
topic_type:
- apiref
ms.openlocfilehash: c6afb19319fd24d499c2c216f2ce0adc2e7a886c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637166"
---
# <a name="iclrruntimeinfogetdefaultstartupflags-method"></a><span data-ttu-id="9ad5d-103">ICLRRuntimeInfo::GetDefaultStartupFlags 方法</span><span class="sxs-lookup"><span data-stu-id="9ad5d-103">ICLRRuntimeInfo::GetDefaultStartupFlags Method</span></span>

<span data-ttu-id="9ad5d-104">获取启动标志和主机配置文件，该文件将用于启动运行时。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-104">Gets the startup flags and host configuration file that will be used to start the runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ad5d-105">语法</span><span class="sxs-lookup"><span data-stu-id="9ad5d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDefaultStartupFlags(  
     [out]  DWORD *pdwStartupFlags,  
     [out, size_is(*pcchHostConfigFile)] LPWSTR pwzHostConfigFile,  
     [in, out]  DWORD *pcchHostConfigFile);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ad5d-106">参数</span><span class="sxs-lookup"><span data-stu-id="9ad5d-106">Parameters</span></span>  

 `pdwStartupFlags`  
 <span data-ttu-id="9ad5d-107">弄指向当前设置的主机启动标志的指针。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-107">[out] A pointer to the host startup flags that are currently set.</span></span>  
  
 `pwzHostConfigFile`  
 <span data-ttu-id="9ad5d-108">弄一个指针，指向当前宿主配置文件的目录路径。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-108">[out] A pointer to the directory path of the current host configuration file.</span></span>  
  
 `pcchHostConfigFile`  
 <span data-ttu-id="9ad5d-109">[in，out]输入时， `pwzHostConfigFile` 为避免缓冲区溢出。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-109">[in, out] On input, the size of `pwzHostConfigFile`, to avoid buffer overruns.</span></span> <span data-ttu-id="9ad5d-110">如果 `pwzHostConfigFile` 为 null，则该方法为预分配返回所需的大小 `pwzHostConfigFile` 。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-110">If `pwzHostConfigFile` is null, the method returns the required size of `pwzHostConfigFile` for pre-allocation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9ad5d-111">返回值</span><span class="sxs-lookup"><span data-stu-id="9ad5d-111">Return Value</span></span>  

 <span data-ttu-id="9ad5d-112">此方法返回以下特定的 HRESULT 以及指示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-112">This method returns the following specific HRESULT as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="9ad5d-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9ad5d-113">HRESULT</span></span>|<span data-ttu-id="9ad5d-114">说明</span><span class="sxs-lookup"><span data-stu-id="9ad5d-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9ad5d-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ad5d-115">S_OK</span></span>|<span data-ttu-id="9ad5d-116">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-116">The method completed successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ad5d-117">备注</span><span class="sxs-lookup"><span data-stu-id="9ad5d-117">Remarks</span></span>  

 <span data-ttu-id="9ad5d-118">此方法返回 (和) 的默认标志值 `STARTUP_CONCURRENT_GC` `NULL` ，或者通过对 [ICLRRuntimeInfo：： SetDefaultStartupFlags 方法](iclrruntimeinfo-setdefaultstartupflags-method.md)的前一次调用提供的值或任何 `CorBind*` 方法（如果它们绑定到此运行时）所设置的值。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-118">This method returns the default flag values (`STARTUP_CONCURRENT_GC` and `NULL`), or the values provided by a previous call to the [ICLRRuntimeInfo::SetDefaultStartupFlags method](iclrruntimeinfo-setdefaultstartupflags-method.md), or the values set by any of the `CorBind*` methods if they are bound to this runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ad5d-119">要求</span><span class="sxs-lookup"><span data-stu-id="9ad5d-119">Requirements</span></span>  

 <span data-ttu-id="9ad5d-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad5d-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ad5d-121">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="9ad5d-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="9ad5d-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9ad5d-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9ad5d-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ad5d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ad5d-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ad5d-124">See also</span></span>

- [<span data-ttu-id="9ad5d-125">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="9ad5d-125">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="9ad5d-126">承载接口</span><span class="sxs-lookup"><span data-stu-id="9ad5d-126">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="9ad5d-127">承载</span><span class="sxs-lookup"><span data-stu-id="9ad5d-127">Hosting</span></span>](index.md)

---
description: 了解详细信息： ICLRRuntimeInfo：： GetProcAddress 方法
title: ICLRRuntimeInfo::GetProcAddress 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetProcAddress
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetProcAddress
helpviewer_keywords:
- GetProcAddress method [.NET Framework hosting]
- ICLRRuntimeInfo::GetProcAddress method [.NET Framework hosting]
ms.assetid: a7732bfc-689a-4926-88fd-4f81e6f9ed78
topic_type:
- apiref
ms.openlocfilehash: 1e5d08ed118930418106b28541b4081d6acad927
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637139"
---
# <a name="iclrruntimeinfogetprocaddress-method"></a><span data-ttu-id="06b7b-103">ICLRRuntimeInfo::GetProcAddress 方法</span><span class="sxs-lookup"><span data-stu-id="06b7b-103">ICLRRuntimeInfo::GetProcAddress Method</span></span>

<span data-ttu-id="06b7b-104">获取从公共语言运行时导出的、与此接口关联 (CLR) 的指定函数的地址。</span><span class="sxs-lookup"><span data-stu-id="06b7b-104">Gets the address of a specified function that was exported from the common language runtime (CLR) associated with this interface.</span></span>  
  
 <span data-ttu-id="06b7b-105">此方法取代了 [GetRealProcAddress](getrealprocaddress-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="06b7b-105">This method supersedes the [GetRealProcAddress](getrealprocaddress-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06b7b-106">语法</span><span class="sxs-lookup"><span data-stu-id="06b7b-106">Syntax</span></span>  
  
```cpp  
HRESULT GetProcAddress(  
     [in]  LPCSTR pszProcName,  
     [out, retval] LPVOID *ppProc);  
```  
  
## <a name="parameters"></a><span data-ttu-id="06b7b-107">参数</span><span class="sxs-lookup"><span data-stu-id="06b7b-107">Parameters</span></span>  

 `pszProcName`  
 <span data-ttu-id="06b7b-108">中导出的函数的名称。</span><span class="sxs-lookup"><span data-stu-id="06b7b-108">[in] The name of the exported function.</span></span>  
  
 `ppProc`  
 <span data-ttu-id="06b7b-109">弄导出函数的地址。</span><span class="sxs-lookup"><span data-stu-id="06b7b-109">[out] The address of the exported function.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="06b7b-110">返回值</span><span class="sxs-lookup"><span data-stu-id="06b7b-110">Return Value</span></span>  

 <span data-ttu-id="06b7b-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="06b7b-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="06b7b-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="06b7b-112">HRESULT</span></span>|<span data-ttu-id="06b7b-113">说明</span><span class="sxs-lookup"><span data-stu-id="06b7b-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="06b7b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="06b7b-114">S_OK</span></span>|<span data-ttu-id="06b7b-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="06b7b-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="06b7b-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="06b7b-116">E_POINTER</span></span>|<span data-ttu-id="06b7b-117">`pszProcName` 或 `ppProc` 为 null。</span><span class="sxs-lookup"><span data-stu-id="06b7b-117">`pszProcName` or `ppProc` is null.</span></span>|  
|<span data-ttu-id="06b7b-118">CLR_E_SHIM_RUNTIMEEXPORT</span><span class="sxs-lookup"><span data-stu-id="06b7b-118">CLR_E_SHIM_RUNTIMEEXPORT</span></span>|<span data-ttu-id="06b7b-119">指定的函数不是已导出的函数。</span><span class="sxs-lookup"><span data-stu-id="06b7b-119">The specified function is not an exported function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06b7b-120">备注</span><span class="sxs-lookup"><span data-stu-id="06b7b-120">Remarks</span></span>  

 <span data-ttu-id="06b7b-121">此方法导致加载但不初始化 CLR。</span><span class="sxs-lookup"><span data-stu-id="06b7b-121">This method causes the CLR to be loaded but not initialized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06b7b-122">要求</span><span class="sxs-lookup"><span data-stu-id="06b7b-122">Requirements</span></span>  

 <span data-ttu-id="06b7b-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06b7b-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06b7b-124">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="06b7b-124">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="06b7b-125">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="06b7b-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="06b7b-126">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06b7b-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06b7b-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="06b7b-127">See also</span></span>

- [<span data-ttu-id="06b7b-128">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="06b7b-128">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="06b7b-129">承载接口</span><span class="sxs-lookup"><span data-stu-id="06b7b-129">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="06b7b-130">承载</span><span class="sxs-lookup"><span data-stu-id="06b7b-130">Hosting</span></span>](index.md)

---
description: 了解详细信息： ICLRRuntimeInfo：： LoadErrorString 方法
title: ICLRRuntimeInfo::LoadErrorString 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.LoadErrorString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::LoadErrorString
helpviewer_keywords:
- ICLRRuntimeInfo::LoadErrorString method [.NET Framework hosting]
- LoadErrorString method [.NET Framework hosting]
ms.assetid: 52c543ab-9ef5-4ee7-b836-c0ffc35cd45b
topic_type:
- apiref
ms.openlocfilehash: 0523b5b89072db50c83c52065c22e9df7167a027
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785063"
---
# <a name="iclrruntimeinfoloaderrorstring-method"></a><span data-ttu-id="4990f-103">ICLRRuntimeInfo::LoadErrorString 方法</span><span class="sxs-lookup"><span data-stu-id="4990f-103">ICLRRuntimeInfo::LoadErrorString Method</span></span>

<span data-ttu-id="4990f-104">将 HRESULT 值转换为指定区域性的适当错误消息。</span><span class="sxs-lookup"><span data-stu-id="4990f-104">Translates an HRESULT value into an appropriate error message for the specified culture.</span></span>  
  
 <span data-ttu-id="4990f-105">此方法取代了以下函数：</span><span class="sxs-lookup"><span data-stu-id="4990f-105">This method supersedes the following functions:</span></span>  
  
- [<span data-ttu-id="4990f-106">LoadStringRC</span><span class="sxs-lookup"><span data-stu-id="4990f-106">LoadStringRC</span></span>](loadstringrc-function.md)  
  
- [<span data-ttu-id="4990f-107">LoadStringRCEx</span><span class="sxs-lookup"><span data-stu-id="4990f-107">LoadStringRCEx</span></span>](loadstringrcex-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="4990f-108">语法</span><span class="sxs-lookup"><span data-stu-id="4990f-108">Syntax</span></span>  
  
```cpp  
HRESULT LoadErrorString(  
     [in] UINT iResourceID,  
     [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
     [in, out]  DWORD *pcchBuffer,  
     [in, lcid] LONG iLocaleID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4990f-109">参数</span><span class="sxs-lookup"><span data-stu-id="4990f-109">Parameters</span></span>  

 `iResourceID`  
 <span data-ttu-id="4990f-110">中要转换的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="4990f-110">[in] The HRESULT to translate.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="4990f-111">弄与给定的 HRESULT 关联的消息字符串。</span><span class="sxs-lookup"><span data-stu-id="4990f-111">[out] The message string associated with the given HRESULT.</span></span>  
  
 `pcchBuffer`  
 <span data-ttu-id="4990f-112">[in，out] `pwzbuffer` 用于避免缓冲区溢出的的大小。</span><span class="sxs-lookup"><span data-stu-id="4990f-112">[in, out] The size of `pwzbuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="4990f-113">如果 `pwzbuffer` 为 null，则 `pcchBuffer` 提供的预期大小 `pwzbuffer` 允许预先分配。</span><span class="sxs-lookup"><span data-stu-id="4990f-113">If `pwzbuffer` is null, `pcchBuffer` provides the expected size of `pwzbuffer` to allow preallocation.</span></span>  
  
 `iLocaleID`  
 <span data-ttu-id="4990f-114">中区域性标识符。</span><span class="sxs-lookup"><span data-stu-id="4990f-114">[in] The culture identifier.</span></span> <span data-ttu-id="4990f-115">若要使用默认区域性，则必须指定-1。</span><span class="sxs-lookup"><span data-stu-id="4990f-115">To use the default culture, you must specify -1.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4990f-116">返回值</span><span class="sxs-lookup"><span data-stu-id="4990f-116">Return Value</span></span>  

 <span data-ttu-id="4990f-117">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="4990f-117">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="4990f-118">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4990f-118">HRESULT</span></span>|<span data-ttu-id="4990f-119">说明</span><span class="sxs-lookup"><span data-stu-id="4990f-119">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4990f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="4990f-120">S_OK</span></span>|<span data-ttu-id="4990f-121">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4990f-121">The method completed successfully.</span></span>|  
|<span data-ttu-id="4990f-122">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="4990f-122">E_POINTER</span></span>|<span data-ttu-id="4990f-123">`pcchBuffer` 为 null。</span><span class="sxs-lookup"><span data-stu-id="4990f-123">`pcchBuffer` is null.</span></span>|  
|<span data-ttu-id="4990f-124">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4990f-124">E_INVALIDARG</span></span>|<span data-ttu-id="4990f-125">`pwzBuffer` 为 null。</span><span class="sxs-lookup"><span data-stu-id="4990f-125">`pwzBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4990f-126">要求</span><span class="sxs-lookup"><span data-stu-id="4990f-126">Requirements</span></span>  

 <span data-ttu-id="4990f-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4990f-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4990f-128">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="4990f-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="4990f-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4990f-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4990f-130">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4990f-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4990f-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="4990f-131">See also</span></span>

- [<span data-ttu-id="4990f-132">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="4990f-132">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="4990f-133">承载接口</span><span class="sxs-lookup"><span data-stu-id="4990f-133">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="4990f-134">承载</span><span class="sxs-lookup"><span data-stu-id="4990f-134">Hosting</span></span>](index.md)

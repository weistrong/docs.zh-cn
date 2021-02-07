---
description: 了解详细信息： ICLRRuntimeInfo：： IsStarted 方法
title: ICLRRuntimeInfo::IsStarted 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsStarted
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsStarted
helpviewer_keywords:
- IsStarted method [.NET Framework hosting]
- ICLRRuntimeInfo::IsStarted method [.NET Framework hosting]
ms.assetid: ef6f2662-323b-4534-aa82-6d1afb7b9309
ms.openlocfilehash: 22059ecbded9eae9659cdaae8b9b92f2d7df0650
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753843"
---
# <a name="iclrruntimeinfoisstarted-method"></a><span data-ttu-id="7bb12-103">ICLRRuntimeInfo::IsStarted 方法</span><span class="sxs-lookup"><span data-stu-id="7bb12-103">ICLRRuntimeInfo::IsStarted Method</span></span>

<span data-ttu-id="7bb12-104">指示运行时是否已启动 (即是否已调用 [ICLRRuntimeHost：： Start 方法](iclrruntimehost-start-method.md) 并且已成功) 。</span><span class="sxs-lookup"><span data-stu-id="7bb12-104">Indicates whether the runtime has been started (that is, whether the [ICLRRuntimeHost::Start method](iclrruntimehost-start-method.md) has been called and has succeeded).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bb12-105">语法</span><span class="sxs-lookup"><span data-stu-id="7bb12-105">Syntax</span></span>  
  
```cpp  
HRESULT IsStarted(  
        [out] BOOL     *pbStarted,  
        [out] DWORD    *pdwStartupFlags);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7bb12-106">参数</span><span class="sxs-lookup"><span data-stu-id="7bb12-106">Parameters</span></span>  

 `pbStarted`  
 <span data-ttu-id="7bb12-107">[out] `true` 如果此运行时已启动，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="7bb12-107">[out] `true` if this runtime is started; otherwise, `false`.</span></span>  
  
 `pdwStartupFlags`  
 <span data-ttu-id="7bb12-108">弄返回用于启动运行时的标志。</span><span class="sxs-lookup"><span data-stu-id="7bb12-108">[out] Returns the flags that were used to start the runtime.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7bb12-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7bb12-109">Return Value</span></span>  

 <span data-ttu-id="7bb12-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="7bb12-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="7bb12-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7bb12-111">HRESULT</span></span>|<span data-ttu-id="7bb12-112">说明</span><span class="sxs-lookup"><span data-stu-id="7bb12-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7bb12-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bb12-113">S_OK</span></span>|<span data-ttu-id="7bb12-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="7bb12-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="7bb12-115">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="7bb12-115">E_NOTIMPL</span></span>|<span data-ttu-id="7bb12-116">公共语言运行时 (CLR) 版本早于 .NET Framework 4 中的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="7bb12-116">The common language runtime (CLR) version is earlier than the CLR version in the .NET Framework 4.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7bb12-117">备注</span><span class="sxs-lookup"><span data-stu-id="7bb12-117">Remarks</span></span>  

 <span data-ttu-id="7bb12-118">此方法不适用于 CLR 版本早于 .NET Framework 4 的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="7bb12-118">This method does not work with CLR versions earlier than the CLR version in the .NET Framework 4.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7bb12-119">要求</span><span class="sxs-lookup"><span data-stu-id="7bb12-119">Requirements</span></span>  

 <span data-ttu-id="7bb12-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7bb12-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7bb12-121">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="7bb12-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="7bb12-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7bb12-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7bb12-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7bb12-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bb12-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bb12-124">See also</span></span>

- [<span data-ttu-id="7bb12-125">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="7bb12-125">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="7bb12-126">承载接口</span><span class="sxs-lookup"><span data-stu-id="7bb12-126">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="7bb12-127">承载</span><span class="sxs-lookup"><span data-stu-id="7bb12-127">Hosting</span></span>](index.md)

---
description: 了解详细信息： IGCHost：： SetGCStartupLimits 方法
title: IGCHost::SetGCStartupLimits 方法
ms.date: 03/30/2017
api_name:
- IGCHost.SetGCStartupLimits
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCStartupLimits
helpviewer_keywords:
- SetGCStartupLimits method, IGCHost interface [.NET Framework hosting]
- IGCHost::SetGCStartupLimits method [.NET Framework hosting]
ms.assetid: cae53926-82ac-4d1d-b297-0bde0bd1bebb
topic_type:
- apiref
ms.openlocfilehash: 91c74d54189bbfb7e9f208e507fe6e75b7023e00
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709472"
---
# <a name="igchostsetgcstartuplimits-method"></a><span data-ttu-id="bdd5d-103">IGCHost::SetGCStartupLimits 方法</span><span class="sxs-lookup"><span data-stu-id="bdd5d-103">IGCHost::SetGCStartupLimits Method</span></span>

<span data-ttu-id="bdd5d-104">设置第0代的段大小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-104">Sets the segment size and the maximum size for generation 0.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="bdd5d-105">从 .NET Framework 4.5 开始，可以 `DWORD` 使用 [IGCHost2：： SetGCStartupLimitsEx](igchost2-setgcstartuplimitsex-method.md) 方法将段大小和最大第0代大小设置为大于的值。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-105">Starting with the .NET Framework 4.5, you can set segment size and maximum generation 0 size to values greater than `DWORD` by using the [IGCHost2::SetGCStartupLimitsEx](igchost2-setgcstartuplimitsex-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdd5d-106">语法</span><span class="sxs-lookup"><span data-stu-id="bdd5d-106">Syntax</span></span>  
  
```cpp  
HRESULT SetGCStartupLimits (  
    [in] DWORD SegmentSize,  
    [in] DWORD MaxGen0Size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bdd5d-107">参数</span><span class="sxs-lookup"><span data-stu-id="bdd5d-107">Parameters</span></span>  

 `SegmentSize`  
 <span data-ttu-id="bdd5d-108">中垃圾收集系统使用的段大小。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-108">[in] The size of the segment used by the garbage collection system.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="bdd5d-109">中第0代的最大大小。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-109">[in] The maximum size for generation 0.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bdd5d-110">备注</span><span class="sxs-lookup"><span data-stu-id="bdd5d-110">Remarks</span></span>  

 <span data-ttu-id="bdd5d-111">`SetGCStartupLimits`方法只能调用一次。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-111">The `SetGCStartupLimits` method may be called only once.</span></span> <span data-ttu-id="bdd5d-112">以后不能更改这些值。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-112">These values cannot be changed later.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdd5d-113">要求</span><span class="sxs-lookup"><span data-stu-id="bdd5d-113">Requirements</span></span>  

 <span data-ttu-id="bdd5d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bdd5d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdd5d-115">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="bdd5d-115">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="bdd5d-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bdd5d-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bdd5d-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdd5d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdd5d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="bdd5d-118">See also</span></span>

- [<span data-ttu-id="bdd5d-119">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="bdd5d-119">IGCHost Interface</span></span>](igchost-interface.md)

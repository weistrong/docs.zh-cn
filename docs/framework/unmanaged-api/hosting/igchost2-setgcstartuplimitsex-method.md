---
description: 了解详细信息： IGCHost2：： SetGCStartupLimitsEx 方法
title: IGCHost2::SetGCStartupLimitsEx 方法
ms.date: 03/30/2017
api_name:
- IGCHost2.SetGCStartupLimitsEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost2::SetGCStartupLimitsEx
helpviewer_keywords:
- IGCHost2::SetGCStartupLimitsEx method [.NET Framework hosting]
- SetGCStartupLimitsEx method, IGCHost2 interface [.NET Framework hosting]
ms.assetid: bba941c2-1c57-46d3-bbf5-5fb92700c490
topic_type:
- apiref
ms.openlocfilehash: 32d3bcbb467a1a418c7123779c881c46e983edef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709302"
---
# <a name="igchost2setgcstartuplimitsex-method"></a><span data-ttu-id="5a811-103">IGCHost2::SetGCStartupLimitsEx 方法</span><span class="sxs-lookup"><span data-stu-id="5a811-103">IGCHost2::SetGCStartupLimitsEx Method</span></span>

<span data-ttu-id="5a811-104">设置第0代的段大小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="5a811-104">Sets the segment size and the maximum size for generation 0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a811-105">语法</span><span class="sxs-lookup"><span data-stu-id="5a811-105">Syntax</span></span>  
  
```cpp  
HRESULT SetGCStartupLimitsEx (  
    [in] SIZE_T SegmentSize,  
    [in] SIZE_T MaxGen0Size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5a811-106">参数</span><span class="sxs-lookup"><span data-stu-id="5a811-106">Parameters</span></span>  

 `SegmentSize`  
 <span data-ttu-id="5a811-107">中垃圾收集系统使用的段大小。</span><span class="sxs-lookup"><span data-stu-id="5a811-107">[in] The size of the segment used by the garbage collection system.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="5a811-108">中第0代的最大大小。</span><span class="sxs-lookup"><span data-stu-id="5a811-108">[in] The maximum size for generation 0.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5a811-109">备注</span><span class="sxs-lookup"><span data-stu-id="5a811-109">Remarks</span></span>  

 <span data-ttu-id="5a811-110">`SetGCStartupLimitsEx`只能在启动主机之前指定设置的值。</span><span class="sxs-lookup"><span data-stu-id="5a811-110">The values that `SetGCStartupLimitsEx` sets can be specified only before the host is started.</span></span> <span data-ttu-id="5a811-111">以后不能更改这些值。</span><span class="sxs-lookup"><span data-stu-id="5a811-111">These values cannot be changed later.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5a811-112">要求</span><span class="sxs-lookup"><span data-stu-id="5a811-112">Requirements</span></span>  

 <span data-ttu-id="5a811-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5a811-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5a811-114">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="5a811-114">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="5a811-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5a811-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5a811-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5a811-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a811-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="5a811-117">See also</span></span>

- [<span data-ttu-id="5a811-118">IGCHost2 接口</span><span class="sxs-lookup"><span data-stu-id="5a811-118">IGCHost2 Interface</span></span>](igchost2-interface.md)

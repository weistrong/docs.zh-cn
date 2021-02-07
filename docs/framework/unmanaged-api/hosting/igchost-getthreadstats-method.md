---
description: 了解详细信息： IGCHost：： GetThreadStats 方法
title: IGCHost::GetThreadStats 方法
ms.date: 03/30/2017
api_name:
- IGCHost.GetThreadStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetThreadStats
helpviewer_keywords:
- IGCHost::GetThreadStats method [.NET Framework hosting]
- GetThreadStats method [.NET Framework hosting]
ms.assetid: 826baa9b-9218-4736-a509-7ab193b125a0
topic_type:
- apiref
ms.openlocfilehash: 2d923560e915a0c88035caad70ad91149d793cb8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709641"
---
# <a name="igchostgetthreadstats-method"></a><span data-ttu-id="43a8e-103">IGCHost::GetThreadStats 方法</span><span class="sxs-lookup"><span data-stu-id="43a8e-103">IGCHost::GetThreadStats Method</span></span>

<span data-ttu-id="43a8e-104">获取用于垃圾回收的每个线程的统计信息。</span><span class="sxs-lookup"><span data-stu-id="43a8e-104">Gets the per-thread statistics for garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43a8e-105">语法</span><span class="sxs-lookup"><span data-stu-id="43a8e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadStats (  
    [in] DWORD *pFiberCookie,  
    [in, out] COR_GC_THREAD_STATS *pStats  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="43a8e-106">参数</span><span class="sxs-lookup"><span data-stu-id="43a8e-106">Parameters</span></span>  

 `pFiberCookie`  
 <span data-ttu-id="43a8e-107">中指向指定要检索其统计信息的线程的纤程 cookie 的指针。</span><span class="sxs-lookup"><span data-stu-id="43a8e-107">[in] A pointer to a fiber cookie that specifies the thread for which to retrieve the statistics.</span></span>  
  
 `pStats`  
 <span data-ttu-id="43a8e-108">[in，out]指向 [COR_GC_THREAD_STATS](cor-gc-thread-stats-structure.md) 结构的指针，该结构包含指定线程的垃圾回收统计信息。</span><span class="sxs-lookup"><span data-stu-id="43a8e-108">[in, out] A pointer to a [COR_GC_THREAD_STATS](cor-gc-thread-stats-structure.md) structure that contains the garbage collection statistics for the specified thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="43a8e-109">要求</span><span class="sxs-lookup"><span data-stu-id="43a8e-109">Requirements</span></span>  

 <span data-ttu-id="43a8e-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="43a8e-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43a8e-111">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="43a8e-111">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="43a8e-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="43a8e-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="43a8e-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43a8e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43a8e-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="43a8e-114">See also</span></span>

- [<span data-ttu-id="43a8e-115">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="43a8e-115">IGCHost Interface</span></span>](igchost-interface.md)

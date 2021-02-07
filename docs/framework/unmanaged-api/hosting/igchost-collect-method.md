---
description: 了解详细信息： IGCHost：： Collect 方法
title: IGCHost::Collect 方法
ms.date: 03/30/2017
api_name:
- IGCHost.Collect
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Collect
helpviewer_keywords:
- Collect method, IGCHost interface [.NET Framework hosting]
- IGCHost::Collect method [.NET Framework hosting]
ms.assetid: fc7d9448-3186-494d-9f0d-ea39717e9a82
topic_type:
- apiref
ms.openlocfilehash: b4c249e07709dc443ae7dd6c6a5bfd206b7f1caa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709679"
---
# <a name="igchostcollect-method"></a><span data-ttu-id="836bb-103">IGCHost::Collect 方法</span><span class="sxs-lookup"><span data-stu-id="836bb-103">IGCHost::Collect Method</span></span>

<span data-ttu-id="836bb-104">为给定的生成强制执行回收，而不考虑当前垃圾回收的状态。</span><span class="sxs-lookup"><span data-stu-id="836bb-104">Forces a collection to occur for the given generation, regardless of the state of the current garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="836bb-105">语法</span><span class="sxs-lookup"><span data-stu-id="836bb-105">Syntax</span></span>  
  
```cpp  
HRESULT Collect (  
    [in] LONG Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="836bb-106">参数</span><span class="sxs-lookup"><span data-stu-id="836bb-106">Parameters</span></span>  

 `Generation`  
 <span data-ttu-id="836bb-107">中要对其执行垃圾回收的代。</span><span class="sxs-lookup"><span data-stu-id="836bb-107">[in] The generation on which to perform the garbage collection.</span></span> <span data-ttu-id="836bb-108">如果值为-1，则表示所有代将进行垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="836bb-108">A value of -1 indicates that all generations will undergo a garbage collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="836bb-109">要求</span><span class="sxs-lookup"><span data-stu-id="836bb-109">Requirements</span></span>  

 <span data-ttu-id="836bb-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="836bb-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="836bb-111">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="836bb-111">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="836bb-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="836bb-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="836bb-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="836bb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="836bb-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="836bb-114">See also</span></span>

- [<span data-ttu-id="836bb-115">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="836bb-115">IGCHost Interface</span></span>](igchost-interface.md)

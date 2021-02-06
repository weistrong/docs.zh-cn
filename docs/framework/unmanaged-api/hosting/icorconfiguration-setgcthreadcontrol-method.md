---
description: 了解详细信息： ICorConfiguration：： SetGCThreadControl 方法
title: ICorConfiguration::SetGCThreadControl 方法
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetGCThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCThreadControl
helpviewer_keywords:
- ICorConfiguration::SetGCThreadControl method [.NET Framework hosting]
- SetGCThreadControl method [.NET Framework hosting]
ms.assetid: 72e38e61-3d56-4ae3-b8f6-0ab7922aaf11
topic_type:
- apiref
ms.openlocfilehash: 8b9388bdefb9da2ce51b62ab68eeee54645e43ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636619"
---
# <a name="icorconfigurationsetgcthreadcontrol-method"></a><span data-ttu-id="735b0-103">ICorConfiguration::SetGCThreadControl 方法</span><span class="sxs-lookup"><span data-stu-id="735b0-103">ICorConfiguration::SetGCThreadControl Method</span></span>

<span data-ttu-id="735b0-104">设置回调接口，用于为非运行时任务计划线程，否则将阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="735b0-104">Sets the callback interface for scheduling threads for non-runtime tasks that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="735b0-105">语法</span><span class="sxs-lookup"><span data-stu-id="735b0-105">Syntax</span></span>  
  
```cpp  
HRESULT SetGCThreadControl (  
    [in] IGCThreadControl* pGCThreadControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="735b0-106">参数</span><span class="sxs-lookup"><span data-stu-id="735b0-106">Parameters</span></span>  

 `pGCThreadControl`  
 <span data-ttu-id="735b0-107">中指向 [IGCThreadControl](igcthreadcontrol-interface.md) 对象的指针，该对象向宿主通知非运行时任务的线程挂起。</span><span class="sxs-lookup"><span data-stu-id="735b0-107">[in] A pointer to an [IGCThreadControl](igcthreadcontrol-interface.md) object that notifies the host about the suspension of threads for non-runtime tasks.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="735b0-108">备注</span><span class="sxs-lookup"><span data-stu-id="735b0-108">Remarks</span></span>  

 <span data-ttu-id="735b0-109">宿主可以在 [IGCThreadControl：： ThreadIsBlockingForSuspension](igcthreadcontrol-threadisblockingforsuspension-method.md) 回调中选择是否重新计划线程。</span><span class="sxs-lookup"><span data-stu-id="735b0-109">The host may choose within the [IGCThreadControl::ThreadIsBlockingForSuspension](igcthreadcontrol-threadisblockingforsuspension-method.md) callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="735b0-110">要求</span><span class="sxs-lookup"><span data-stu-id="735b0-110">Requirements</span></span>  

 <span data-ttu-id="735b0-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="735b0-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="735b0-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="735b0-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="735b0-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="735b0-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="735b0-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="735b0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="735b0-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="735b0-115">See also</span></span>

- [<span data-ttu-id="735b0-116">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="735b0-116">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)

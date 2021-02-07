---
description: 了解详细信息： IGCThreadControl：： SuspensionEnding 方法
title: IGCThreadControl::SuspensionEnding 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
ms.openlocfilehash: 5ff889f45ea3664312060f373907e65c367276f1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709264"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="0cfd0-103">IGCThreadControl::SuspensionEnding 方法</span><span class="sxs-lookup"><span data-stu-id="0cfd0-103">IGCThreadControl::SuspensionEnding Method</span></span>

<span data-ttu-id="0cfd0-104">向宿主通知运行时在垃圾回收或其他挂起后正在恢复线程。</span><span class="sxs-lookup"><span data-stu-id="0cfd0-104">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0cfd0-105">语法</span><span class="sxs-lookup"><span data-stu-id="0cfd0-105">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0cfd0-106">参数</span><span class="sxs-lookup"><span data-stu-id="0cfd0-106">Parameters</span></span>  

 `Generation`  
 <span data-ttu-id="0cfd0-107">中已对其执行垃圾回收的代。</span><span class="sxs-lookup"><span data-stu-id="0cfd0-107">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0cfd0-108">备注</span><span class="sxs-lookup"><span data-stu-id="0cfd0-108">Remarks</span></span>  

 <span data-ttu-id="0cfd0-109">不要在回调过程中重新计划任何线程 `SuspensionEnding` 。</span><span class="sxs-lookup"><span data-stu-id="0cfd0-109">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0cfd0-110">要求</span><span class="sxs-lookup"><span data-stu-id="0cfd0-110">Requirements</span></span>  

 <span data-ttu-id="0cfd0-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0cfd0-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0cfd0-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0cfd0-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0cfd0-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0cfd0-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0cfd0-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0cfd0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0cfd0-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="0cfd0-115">See also</span></span>

- [<span data-ttu-id="0cfd0-116">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="0cfd0-116">IGCThreadControl Interface</span></span>](igcthreadcontrol-interface.md)

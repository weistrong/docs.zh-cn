---
description: 了解详细信息： IGCThreadControl 接口
title: IGCThreadControl 接口
ms.date: 03/30/2017
api_name:
- IGCThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCThreadControl
helpviewer_keywords:
- IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 3ff04d75-85ac-4df9-886d-dbaa037c0552
topic_type:
- apiref
ms.openlocfilehash: 07c76848668b1525f4ff45ba5de746beefe0e004
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709277"
---
# <a name="igcthreadcontrol-interface"></a><span data-ttu-id="766be-103">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="766be-103">IGCThreadControl Interface</span></span>

<span data-ttu-id="766be-104">提供一些方法，这些方法用于参与要阻止垃圾回收的线程的计划。</span><span class="sxs-lookup"><span data-stu-id="766be-104">Provides methods for participating in the scheduling of threads that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="766be-105">方法</span><span class="sxs-lookup"><span data-stu-id="766be-105">Methods</span></span>  
  
|<span data-ttu-id="766be-106">方法</span><span class="sxs-lookup"><span data-stu-id="766be-106">Method</span></span>|<span data-ttu-id="766be-107">说明</span><span class="sxs-lookup"><span data-stu-id="766be-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="766be-108">SuspensionEnding 方法</span><span class="sxs-lookup"><span data-stu-id="766be-108">SuspensionEnding Method</span></span>](igcthreadcontrol-suspensionending-method.md)|<span data-ttu-id="766be-109">向宿主通知运行时在垃圾回收或其他挂起后正在恢复线程。</span><span class="sxs-lookup"><span data-stu-id="766be-109">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="766be-110">SuspensionStarting 方法</span><span class="sxs-lookup"><span data-stu-id="766be-110">SuspensionStarting Method</span></span>](igcthreadcontrol-suspensionstarting-method.md)|<span data-ttu-id="766be-111">通知宿主运行时正在为垃圾回收或其他挂起开始线程挂起。</span><span class="sxs-lookup"><span data-stu-id="766be-111">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="766be-112">ThreadIsBlockingForSuspension 方法</span><span class="sxs-lookup"><span data-stu-id="766be-112">ThreadIsBlockingForSuspension Method</span></span>](igcthreadcontrol-threadisblockingforsuspension-method.md)|<span data-ttu-id="766be-113">通知宿主发出调用的线程将要阻止，可能用于垃圾回收或其他挂起。</span><span class="sxs-lookup"><span data-stu-id="766be-113">Notifies the host that the thread making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="766be-114">要求</span><span class="sxs-lookup"><span data-stu-id="766be-114">Requirements</span></span>  

 <span data-ttu-id="766be-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="766be-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="766be-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="766be-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="766be-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="766be-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="766be-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="766be-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="766be-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="766be-119">See also</span></span>

- [<span data-ttu-id="766be-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="766be-120">Hosting Interfaces</span></span>](hosting-interfaces.md)

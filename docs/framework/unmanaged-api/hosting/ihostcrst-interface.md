---
description: 了解详细信息： IHostCrst 接口
title: IHostCrst 接口
ms.date: 03/30/2017
api_name:
- IHostCrst
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst
helpviewer_keywords:
- IHostCrst interface [.NET Framework hosting]
ms.assetid: ac298ebd-0815-47e4-a823-30b31baab903
topic_type:
- apiref
ms.openlocfilehash: 7945f0087667c1d610a1a2370528b055af74d579
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708861"
---
# <a name="ihostcrst-interface"></a><span data-ttu-id="b61d4-103">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="b61d4-103">IHostCrst Interface</span></span>

<span data-ttu-id="b61d4-104">用作线程的关键部分的宿主表示形式。</span><span class="sxs-lookup"><span data-stu-id="b61d4-104">Serves as the host's representation of a critical section for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b61d4-105">方法</span><span class="sxs-lookup"><span data-stu-id="b61d4-105">Methods</span></span>  
  
|<span data-ttu-id="b61d4-106">方法</span><span class="sxs-lookup"><span data-stu-id="b61d4-106">Method</span></span>|<span data-ttu-id="b61d4-107">说明</span><span class="sxs-lookup"><span data-stu-id="b61d4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b61d4-108">Enter 方法</span><span class="sxs-lookup"><span data-stu-id="b61d4-108">Enter Method</span></span>](ihostcrst-enter-method.md)|<span data-ttu-id="b61d4-109">输入临界区。</span><span class="sxs-lookup"><span data-stu-id="b61d4-109">Enters the critical section.</span></span>|  
|[<span data-ttu-id="b61d4-110">Leave 方法</span><span class="sxs-lookup"><span data-stu-id="b61d4-110">Leave Method</span></span>](ihostcrst-leave-method.md)|<span data-ttu-id="b61d4-111">离开临界区。</span><span class="sxs-lookup"><span data-stu-id="b61d4-111">Leaves the critical section.</span></span>|  
|[<span data-ttu-id="b61d4-112">SetSpinCount 方法</span><span class="sxs-lookup"><span data-stu-id="b61d4-112">SetSpinCount Method</span></span>](ihostcrst-setspincount-method.md)|<span data-ttu-id="b61d4-113">设置临界区的旋转计数。</span><span class="sxs-lookup"><span data-stu-id="b61d4-113">Sets the spin count for the critical section.</span></span>|  
|[<span data-ttu-id="b61d4-114">TryEnter 方法</span><span class="sxs-lookup"><span data-stu-id="b61d4-114">TryEnter Method</span></span>](ihostcrst-tryenter-method.md)|<span data-ttu-id="b61d4-115">尝试输入临界区，并立即报告成功或失败。</span><span class="sxs-lookup"><span data-stu-id="b61d4-115">Attempts to enter the critical section, and reports success or failure immediately.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b61d4-116">备注</span><span class="sxs-lookup"><span data-stu-id="b61d4-116">Remarks</span></span>  

 <span data-ttu-id="b61d4-117">`IHostCrst` 允许公共语言运行时 (CLR) 直接与关键节的主机表示形式进行通信，而不是使用或等 Win32 函数 `EnterCriticalSection` `LeaveCriticalSection` 。</span><span class="sxs-lookup"><span data-stu-id="b61d4-117">`IHostCrst` allows the common language runtime (CLR) to communicate directly with the host's representation of a critical section, rather than using Win32 functions such as `EnterCriticalSection` or `LeaveCriticalSection`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b61d4-118">要求</span><span class="sxs-lookup"><span data-stu-id="b61d4-118">Requirements</span></span>  

 <span data-ttu-id="b61d4-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b61d4-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b61d4-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b61d4-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b61d4-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b61d4-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b61d4-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b61d4-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b61d4-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b61d4-123">See also</span></span>

- [<span data-ttu-id="b61d4-124">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="b61d4-124">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="b61d4-125">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="b61d4-125">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="b61d4-126">承载接口</span><span class="sxs-lookup"><span data-stu-id="b61d4-126">Hosting Interfaces</span></span>](hosting-interfaces.md)

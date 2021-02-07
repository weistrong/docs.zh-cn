---
description: 了解详细信息： IGCThreadControl：： ThreadIsBlockingForSuspension 方法
title: IGCThreadControl::ThreadIsBlockingForSuspension 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForSuspension
helpviewer_keywords:
- IGCThreadControl::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: ed5b5b58-7db7-46b5-9e2c-278db7159cee
topic_type:
- apiref
ms.openlocfilehash: 13023a75ab1c438abebbeb16fd9fe7c4b95c37ab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709199"
---
# <a name="igcthreadcontrolthreadisblockingforsuspension-method"></a><span data-ttu-id="944e5-103">IGCThreadControl::ThreadIsBlockingForSuspension 方法</span><span class="sxs-lookup"><span data-stu-id="944e5-103">IGCThreadControl::ThreadIsBlockingForSuspension Method</span></span>

<span data-ttu-id="944e5-104">通知宿主正在进行调用的线程将要阻止，可能用于垃圾回收或其他挂起。</span><span class="sxs-lookup"><span data-stu-id="944e5-104">Notifies the host that the thread that is making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="944e5-105">语法</span><span class="sxs-lookup"><span data-stu-id="944e5-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadIsBlockingForSuspension ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="944e5-106">备注</span><span class="sxs-lookup"><span data-stu-id="944e5-106">Remarks</span></span>  

 <span data-ttu-id="944e5-107">宿主可以在回调内选择 `ThreadIsBlockingForSuspension` 是否重新计划线程。</span><span class="sxs-lookup"><span data-stu-id="944e5-107">The host may choose within the `ThreadIsBlockingForSuspension` callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="944e5-108">要求</span><span class="sxs-lookup"><span data-stu-id="944e5-108">Requirements</span></span>  

 <span data-ttu-id="944e5-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="944e5-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="944e5-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="944e5-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="944e5-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="944e5-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="944e5-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="944e5-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="944e5-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="944e5-113">See also</span></span>

- [<span data-ttu-id="944e5-114">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="944e5-114">IGCThreadControl Interface</span></span>](igcthreadcontrol-interface.md)

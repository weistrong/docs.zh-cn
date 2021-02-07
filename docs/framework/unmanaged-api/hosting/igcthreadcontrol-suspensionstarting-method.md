---
description: 了解详细信息： IGCThreadControl：： SuspensionStarting 方法
title: IGCThreadControl::SuspensionStarting 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionStarting
helpviewer_keywords:
- IGCThreadControl::SuspensionStarting method [.NET Framework hosting]
- SuspensionStarting method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 0af312af-98e9-415e-b182-42e80a1aee51
topic_type:
- apiref
ms.openlocfilehash: b9d068e6995a73e9a9a31d5d5debf008f9748630
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709287"
---
# <a name="igcthreadcontrolsuspensionstarting-method"></a><span data-ttu-id="a726c-103">IGCThreadControl::SuspensionStarting 方法</span><span class="sxs-lookup"><span data-stu-id="a726c-103">IGCThreadControl::SuspensionStarting Method</span></span>

<span data-ttu-id="a726c-104">通知宿主运行时正在为垃圾回收或其他挂起开始线程挂起。</span><span class="sxs-lookup"><span data-stu-id="a726c-104">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a726c-105">语法</span><span class="sxs-lookup"><span data-stu-id="a726c-105">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionStarting ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="a726c-106">备注</span><span class="sxs-lookup"><span data-stu-id="a726c-106">Remarks</span></span>  

 <span data-ttu-id="a726c-107">不要在回调过程中重新计划任何线程 `SuspensionStarting` 。</span><span class="sxs-lookup"><span data-stu-id="a726c-107">Do not reschedule any threads during the `SuspensionStarting` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a726c-108">要求</span><span class="sxs-lookup"><span data-stu-id="a726c-108">Requirements</span></span>  

 <span data-ttu-id="a726c-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a726c-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a726c-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a726c-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a726c-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a726c-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a726c-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a726c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a726c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a726c-113">See also</span></span>

- [<span data-ttu-id="a726c-114">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="a726c-114">IGCThreadControl Interface</span></span>](igcthreadcontrol-interface.md)

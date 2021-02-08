---
description: 了解详细信息： IHostTask：： Start 方法
title: IHostTask::Start 方法
ms.date: 03/30/2017
api_name:
- IHostTask.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Start
helpviewer_keywords:
- IHostTask::Start method [.NET Framework hosting]
- Start method, IHostTask interface [.NET Framework hosting]
ms.assetid: b18742b0-d8c4-401c-ae89-e6eccdaa81d0
topic_type:
- apiref
ms.openlocfilehash: 48352a3df49ba2ef3e008ed211da19f54deb82f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784621"
---
# <a name="ihosttaskstart-method"></a><span data-ttu-id="363e1-103">IHostTask::Start 方法</span><span class="sxs-lookup"><span data-stu-id="363e1-103">IHostTask::Start Method</span></span>

<span data-ttu-id="363e1-104">请求宿主将当前 [IHostTask](ihosttask-interface.md) 实例表示的任务从挂起状态移动到实时状态，在此状态下可以执行代码。</span><span class="sxs-lookup"><span data-stu-id="363e1-104">Requests that the host move the task represented by the current [IHostTask](ihosttask-interface.md) instance from a suspended to a live state, in which code can be executed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="363e1-105">语法</span><span class="sxs-lookup"><span data-stu-id="363e1-105">Syntax</span></span>  
  
```cpp  
HRESULT Start ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="363e1-106">返回值</span><span class="sxs-lookup"><span data-stu-id="363e1-106">Return Value</span></span>  
  
|<span data-ttu-id="363e1-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="363e1-107">HRESULT</span></span>|<span data-ttu-id="363e1-108">说明</span><span class="sxs-lookup"><span data-stu-id="363e1-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="363e1-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="363e1-109">S_OK</span></span>|<span data-ttu-id="363e1-110">已成功启动。</span><span class="sxs-lookup"><span data-stu-id="363e1-110">Start returned successfully.</span></span>|  
|<span data-ttu-id="363e1-111">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="363e1-111">E_FAIL</span></span>|<span data-ttu-id="363e1-112">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="363e1-112">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="363e1-113">当方法返回 E_FAIL 时，公共语言运行时 (CLR) 在该进程内不再可用。</span><span class="sxs-lookup"><span data-stu-id="363e1-113">When a method returns E_FAIL, the common language runtime (CLR) is no longer usable within the process.</span></span> <span data-ttu-id="363e1-114">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="363e1-114">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="363e1-115">备注</span><span class="sxs-lookup"><span data-stu-id="363e1-115">Remarks</span></span>  

 <span data-ttu-id="363e1-116">`Start` 始终返回 S_OK 的 HRESULT 值，但发生灾难性故障的情况除外。</span><span class="sxs-lookup"><span data-stu-id="363e1-116">`Start` always returns an HRESULT value of S_OK, except in cases where a catastrophic failure has occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="363e1-117">要求</span><span class="sxs-lookup"><span data-stu-id="363e1-117">Requirements</span></span>  

 <span data-ttu-id="363e1-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="363e1-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="363e1-119">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="363e1-119">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="363e1-120">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="363e1-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="363e1-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="363e1-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="363e1-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="363e1-122">See also</span></span>

- [<span data-ttu-id="363e1-123">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="363e1-123">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="363e1-124">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="363e1-124">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="363e1-125">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="363e1-125">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="363e1-126">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="363e1-126">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)

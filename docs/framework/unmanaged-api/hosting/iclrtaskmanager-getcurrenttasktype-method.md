---
description: 了解详细信息： ICLRTaskManager：： GetCurrentTaskType 方法
title: ICLRTaskManager::GetCurrentTaskType 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTaskType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTaskType
helpviewer_keywords:
- GetCurrentTaskType method [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTaskType method [.NET Framework hosting]
ms.assetid: 6b0d9259-dbe2-45bb-b34d-990f60c73424
topic_type:
- apiref
ms.openlocfilehash: 984cc490123d6146737d3f018fdf712c7c528635
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799473"
---
# <a name="iclrtaskmanagergetcurrenttasktype-method"></a><span data-ttu-id="c4c96-103">ICLRTaskManager::GetCurrentTaskType 方法</span><span class="sxs-lookup"><span data-stu-id="c4c96-103">ICLRTaskManager::GetCurrentTaskType Method</span></span>

<span data-ttu-id="c4c96-104">获取当前正在执行的任务的类型。</span><span class="sxs-lookup"><span data-stu-id="c4c96-104">Gets the type of the task that is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4c96-105">语法</span><span class="sxs-lookup"><span data-stu-id="c4c96-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentTaskType(  
    [out] ETaskType *pTaskType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c4c96-106">参数</span><span class="sxs-lookup"><span data-stu-id="c4c96-106">Parameters</span></span>  

 `pTaskType`  
 <span data-ttu-id="c4c96-107">弄一个指针，指向 [ETaskType](etasktype-enumeration.md) 枚举的值，该值指示当前正在执行的任务的类型。</span><span class="sxs-lookup"><span data-stu-id="c4c96-107">[out] A pointer to a value of the [ETaskType](etasktype-enumeration.md) enumeration that indicates the type of task that is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4c96-108">要求</span><span class="sxs-lookup"><span data-stu-id="c4c96-108">Requirements</span></span>  

 <span data-ttu-id="c4c96-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c4c96-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4c96-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c4c96-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c4c96-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c4c96-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c4c96-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4c96-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4c96-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="c4c96-113">See also</span></span>

- [<span data-ttu-id="c4c96-114">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="c4c96-114">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)

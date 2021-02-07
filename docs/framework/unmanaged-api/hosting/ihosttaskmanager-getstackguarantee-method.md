---
description: 了解详细信息： IHostTaskManager：： GetStackGuarantee 方法
title: IHostTaskManager::GetStackGuarantee 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.GetStackGuarantee
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::GetStackGuarantee
helpviewer_keywords:
- GetStackGuarantee method [.NET Framework hosting]
- IHostTaskManager::GetStackGuarantee method [.NET Framework hosting]
ms.assetid: 8176d732-c25c-4520-811d-e3310f339947
topic_type:
- apiref
ms.openlocfilehash: 6c8bd9839ea0c1fdb72fbbd296061d1a2b6edfe1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753791"
---
# <a name="ihosttaskmanagergetstackguarantee-method"></a><span data-ttu-id="175a8-103">IHostTaskManager::GetStackGuarantee 方法</span><span class="sxs-lookup"><span data-stu-id="175a8-103">IHostTaskManager::GetStackGuarantee Method</span></span>

<span data-ttu-id="175a8-104">获取在堆栈操作完成之后但在关闭进程之前保证可用的堆栈空间量。</span><span class="sxs-lookup"><span data-stu-id="175a8-104">Gets the amount of stack space that is guaranteed to be available after a stack operation completes, but before the closing of a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="175a8-105">语法</span><span class="sxs-lookup"><span data-stu-id="175a8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStackGuarantee(  
    [out] ULONG *pGuarantee  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="175a8-106">参数</span><span class="sxs-lookup"><span data-stu-id="175a8-106">Parameters</span></span>  

 `pGuarantee`  
 <span data-ttu-id="175a8-107">弄指向可用字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="175a8-107">[out] A pointer to the number of bytes that are available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="175a8-108">要求</span><span class="sxs-lookup"><span data-stu-id="175a8-108">Requirements</span></span>  

 <span data-ttu-id="175a8-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="175a8-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="175a8-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="175a8-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="175a8-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="175a8-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="175a8-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="175a8-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="175a8-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="175a8-113">See also</span></span>

- [<span data-ttu-id="175a8-114">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="175a8-114">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)

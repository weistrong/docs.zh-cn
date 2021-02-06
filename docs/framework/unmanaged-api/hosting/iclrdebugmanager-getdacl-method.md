---
description: 了解详细信息： ICLRDebugManager：： GetDacl 方法
title: ICLRDebugManager::GetDacl 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.GetDacl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::GetDacl
helpviewer_keywords:
- GetDacl method [.NET Framework hosting]
- ICLRDebugManager::GetDacl method [.NET Framework hosting]
ms.assetid: 7115e920-aaff-440a-824e-39497139c6f6
topic_type:
- apiref
ms.openlocfilehash: 8a1b747851d0c5104dbe18e5a66742d57b09aa22
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649463"
---
# <a name="iclrdebugmanagergetdacl-method"></a><span data-ttu-id="1fecd-103">ICLRDebugManager::GetDacl 方法</span><span class="sxs-lookup"><span data-stu-id="1fecd-103">ICLRDebugManager::GetDacl Method</span></span>

<span data-ttu-id="1fecd-104">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="1fecd-104">This method is not implemented.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fecd-105">语法</span><span class="sxs-lookup"><span data-stu-id="1fecd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDacl (  
    [out] PACL* ppacl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1fecd-106">参数</span><span class="sxs-lookup"><span data-stu-id="1fecd-106">Parameters</span></span>  

 `ppacl`  
 <span data-ttu-id="1fecd-107">弄指向访问控制列表 (ACL) 的接口指针。</span><span class="sxs-lookup"><span data-stu-id="1fecd-107">[out] An interface pointer to the Access Control List (ACL).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1fecd-108">返回值</span><span class="sxs-lookup"><span data-stu-id="1fecd-108">Return Value</span></span>  
  
|<span data-ttu-id="1fecd-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1fecd-109">HRESULT</span></span>|<span data-ttu-id="1fecd-110">说明</span><span class="sxs-lookup"><span data-stu-id="1fecd-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1fecd-111">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="1fecd-111">E_NOTIMPL</span></span>|<span data-ttu-id="1fecd-112">该方法未实现。</span><span class="sxs-lookup"><span data-stu-id="1fecd-112">The method is not implemented.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1fecd-113">要求</span><span class="sxs-lookup"><span data-stu-id="1fecd-113">Requirements</span></span>  

 <span data-ttu-id="1fecd-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fecd-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fecd-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1fecd-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1fecd-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1fecd-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1fecd-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fecd-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fecd-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="1fecd-118">See also</span></span>

- [<span data-ttu-id="1fecd-119">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="1fecd-119">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="1fecd-120">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="1fecd-120">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)
- [<span data-ttu-id="1fecd-121">SetDacl 方法</span><span class="sxs-lookup"><span data-stu-id="1fecd-121">SetDacl Method</span></span>](iclrdebugmanager-setdacl-method.md)
- [<span data-ttu-id="1fecd-122">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="1fecd-122">IHostControl Interface</span></span>](ihostcontrol-interface.md)

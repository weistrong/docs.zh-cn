---
description: 了解详细信息： ICLRDebugManager：： SetSymbolReadingPolicy 方法
title: ICLRDebugManager::SetSymbolReadingPolicy 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.SetSymbolReadingPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::SetSymbolReadingPolicy
helpviewer_keywords:
- ICLRDebugManager, SetSymbolREadingPolicy method
- SetSymbolReadingPolicy method [.NET Framework hosting]
- ICLRDebugManager::SetSymbolReadingPolicy method [.NET Framework hosting]
ms.assetid: bd921fa2-d377-4d79-acfc-64c38d4dcae9
topic_type:
- apiref
ms.openlocfilehash: 2c0862f3c572808ffbf418b275e1ad1c62c2ac89
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781943"
---
# <a name="iclrdebugmanagersetsymbolreadingpolicy-method"></a><span data-ttu-id="7015a-103">ICLRDebugManager::SetSymbolReadingPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="7015a-103">ICLRDebugManager::SetSymbolReadingPolicy Method</span></span>

<span data-ttu-id="7015a-104">设置用于读取程序数据库 (PDB) 文件的策略。</span><span class="sxs-lookup"><span data-stu-id="7015a-104">Sets the policy for reading program database (PDB) files.</span></span> <span data-ttu-id="7015a-105">策略确定有关行号和文件的信息是否包含在调用堆栈中。</span><span class="sxs-lookup"><span data-stu-id="7015a-105">The policy determines whether information about line numbers and files is included in call stacks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7015a-106">语法</span><span class="sxs-lookup"><span data-stu-id="7015a-106">Syntax</span></span>  
  
```cpp  
HRESULT SetSymbolReadingPolicy (  
    [in] ESymbolReadingPolicy policy  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7015a-107">参数</span><span class="sxs-lookup"><span data-stu-id="7015a-107">Parameters</span></span>  

 `policy`  
 <span data-ttu-id="7015a-108">中 [ESymbolReadingPolicy](esymbolreadingpolicy-enumeration.md) 枚举的成员。</span><span class="sxs-lookup"><span data-stu-id="7015a-108">[in] A member of the [ESymbolReadingPolicy](esymbolreadingpolicy-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7015a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7015a-109">Return Value</span></span>  
  
|<span data-ttu-id="7015a-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7015a-110">HRESULT</span></span>|<span data-ttu-id="7015a-111">说明</span><span class="sxs-lookup"><span data-stu-id="7015a-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7015a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7015a-112">S_OK</span></span>|<span data-ttu-id="7015a-113">`SetSymbolReadingPolicy` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="7015a-113">`SetSymbolReadingPolicy` returned successfully.</span></span>|  
|<span data-ttu-id="7015a-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7015a-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7015a-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7015a-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7015a-116">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7015a-116">E_FAIL</span></span>|<span data-ttu-id="7015a-117">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7015a-117">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7015a-118">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7015a-118">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7015a-119">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7015a-119">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7015a-120">要求</span><span class="sxs-lookup"><span data-stu-id="7015a-120">Requirements</span></span>  

 <span data-ttu-id="7015a-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7015a-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7015a-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7015a-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7015a-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7015a-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7015a-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7015a-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7015a-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="7015a-125">See also</span></span>

- [<span data-ttu-id="7015a-126">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="7015a-126">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)

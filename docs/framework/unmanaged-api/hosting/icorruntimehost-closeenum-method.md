---
description: 了解详细信息： ICorRuntimeHost：： CloseEnum 方法
title: ICorRuntimeHost::CloseEnum 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CloseEnum
helpviewer_keywords:
- CloseEnum method, ICorRuntimeHost interface [.NET Framework hosting]
- ICorRuntimeHost::CloseEnum method [.NET Framework hosting]
ms.assetid: f7ce7e8c-0a3e-4587-a180-063e2b85940e
topic_type:
- apiref
ms.openlocfilehash: 1fc18ff3e00f85a4f047417f880ec2b0e06496b7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789718"
---
# <a name="icorruntimehostcloseenum-method"></a><span data-ttu-id="45c00-103">ICorRuntimeHost::CloseEnum 方法</span><span class="sxs-lookup"><span data-stu-id="45c00-103">ICorRuntimeHost::CloseEnum Method</span></span>

<span data-ttu-id="45c00-104">将域枚举器重置回域列表的开头。</span><span class="sxs-lookup"><span data-stu-id="45c00-104">Resets a domain enumerator back to the beginning of the domain list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45c00-105">语法</span><span class="sxs-lookup"><span data-stu-id="45c00-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseEnum (  
    [in] HCORENUM hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="45c00-106">参数</span><span class="sxs-lookup"><span data-stu-id="45c00-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="45c00-107">中要重置的枚举数。</span><span class="sxs-lookup"><span data-stu-id="45c00-107">[in] The enumerator to reset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="45c00-108">返回值</span><span class="sxs-lookup"><span data-stu-id="45c00-108">Return Value</span></span>  
  
|<span data-ttu-id="45c00-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="45c00-109">HRESULT</span></span>|<span data-ttu-id="45c00-110">说明</span><span class="sxs-lookup"><span data-stu-id="45c00-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="45c00-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="45c00-111">S_OK</span></span>|<span data-ttu-id="45c00-112">操作成功。</span><span class="sxs-lookup"><span data-stu-id="45c00-112">The operation was successful.</span></span>|  
|<span data-ttu-id="45c00-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="45c00-113">S_FALSE</span></span>|<span data-ttu-id="45c00-114">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="45c00-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="45c00-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="45c00-115">E_FAIL</span></span>|<span data-ttu-id="45c00-116">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="45c00-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="45c00-117">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="45c00-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="45c00-118">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="45c00-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="45c00-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="45c00-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="45c00-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="45c00-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="45c00-121">要求</span><span class="sxs-lookup"><span data-stu-id="45c00-121">Requirements</span></span>  

 <span data-ttu-id="45c00-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="45c00-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45c00-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="45c00-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="45c00-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="45c00-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="45c00-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="45c00-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45c00-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="45c00-126">See also</span></span>

- [<span data-ttu-id="45c00-127">CorBindToRuntimeEx 函数</span><span class="sxs-lookup"><span data-stu-id="45c00-127">CorBindToRuntimeEx Function</span></span>](corbindtoruntimeex-function.md)
- [<span data-ttu-id="45c00-128">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="45c00-128">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)

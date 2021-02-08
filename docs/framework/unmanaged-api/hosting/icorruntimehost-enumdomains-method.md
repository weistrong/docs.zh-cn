---
description: 了解详细信息： ICorRuntimeHost：： EnumDomains 方法
title: ICorRuntimeHost::EnumDomains 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.EnumDomains
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::EnumDomains
helpviewer_keywords:
- ICorRuntimeHost::EnumDomains method [.NET Framework hosting]
- EnumDomains method [.NET Framework hosting]
ms.assetid: 96b74995-0cde-4876-b6df-7fc164e6a5d1
topic_type:
- apiref
ms.openlocfilehash: e581fe95a78a4f55d50a99e4925e03a1777268a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784868"
---
# <a name="icorruntimehostenumdomains-method"></a><span data-ttu-id="bb486-103">ICorRuntimeHost::EnumDomains 方法</span><span class="sxs-lookup"><span data-stu-id="bb486-103">ICorRuntimeHost::EnumDomains Method</span></span>

<span data-ttu-id="bb486-104">获取当前进程中的域的枚举数。</span><span class="sxs-lookup"><span data-stu-id="bb486-104">Gets an enumerator for the domains in the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb486-105">语法</span><span class="sxs-lookup"><span data-stu-id="bb486-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumDomains (  
    [out] HCORENUM *hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb486-106">参数</span><span class="sxs-lookup"><span data-stu-id="bb486-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="bb486-107">弄域的枚举数。</span><span class="sxs-lookup"><span data-stu-id="bb486-107">[out] An enumerator for the domains.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bb486-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bb486-108">Return Value</span></span>  
  
|<span data-ttu-id="bb486-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bb486-109">HRESULT</span></span>|<span data-ttu-id="bb486-110">说明</span><span class="sxs-lookup"><span data-stu-id="bb486-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bb486-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb486-111">S_OK</span></span>|<span data-ttu-id="bb486-112">操作成功。</span><span class="sxs-lookup"><span data-stu-id="bb486-112">The operation was successful.</span></span>|  
|<span data-ttu-id="bb486-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="bb486-113">S_FALSE</span></span>|<span data-ttu-id="bb486-114">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="bb486-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="bb486-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bb486-115">E_FAIL</span></span>|<span data-ttu-id="bb486-116">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="bb486-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="bb486-117">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="bb486-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="bb486-118">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="bb486-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="bb486-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bb486-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bb486-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="bb486-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bb486-121">要求</span><span class="sxs-lookup"><span data-stu-id="bb486-121">Requirements</span></span>  

 <span data-ttu-id="bb486-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb486-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb486-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="bb486-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bb486-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bb486-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bb486-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="bb486-125">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb486-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb486-126">See also</span></span>

- [<span data-ttu-id="bb486-127">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="bb486-127">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)

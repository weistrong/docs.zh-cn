---
description: 了解详细信息： ICorRuntimeHost：： UnloadDomain 方法
title: ICorRuntimeHost::UnloadDomain 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.UnloadDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::UnloadDomain
helpviewer_keywords:
- ICorRuntimeHost::UnloadDomain method [.NET Framework hosting]
- UnloadDomain method [.NET Framework hosting]
ms.assetid: dd9e9204-a80d-44f3-8192-779224b35056
topic_type:
- apiref
ms.openlocfilehash: b191f2342778b2f2ed7ddb7b1fb548c73be96599
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799392"
---
# <a name="icorruntimehostunloaddomain-method"></a><span data-ttu-id="166e3-103">ICorRuntimeHost::UnloadDomain 方法</span><span class="sxs-lookup"><span data-stu-id="166e3-103">ICorRuntimeHost::UnloadDomain Method</span></span>

<span data-ttu-id="166e3-104">从当前进程中卸载指定的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="166e3-104">Unloads the specified application domain from the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="166e3-105">语法</span><span class="sxs-lookup"><span data-stu-id="166e3-105">Syntax</span></span>  
  
```cpp  
HRESULT UnloadDomain (  
    [in] IUnknown* pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="166e3-106">参数</span><span class="sxs-lookup"><span data-stu-id="166e3-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="166e3-107">中表示要卸载的域的类型的指针 <xref:System._AppDomain?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="166e3-107">[in] A pointer of type <xref:System._AppDomain?displayProperty=nameWithType> that represents the domain to be unloaded.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="166e3-108">返回值</span><span class="sxs-lookup"><span data-stu-id="166e3-108">Return Value</span></span>  
  
|<span data-ttu-id="166e3-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="166e3-109">HRESULT</span></span>|<span data-ttu-id="166e3-110">说明</span><span class="sxs-lookup"><span data-stu-id="166e3-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="166e3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="166e3-111">S_OK</span></span>|<span data-ttu-id="166e3-112">操作成功。</span><span class="sxs-lookup"><span data-stu-id="166e3-112">The operation was successful.</span></span>|  
|<span data-ttu-id="166e3-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="166e3-113">S_FALSE</span></span>|<span data-ttu-id="166e3-114">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="166e3-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="166e3-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="166e3-115">E_FAIL</span></span>|<span data-ttu-id="166e3-116">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="166e3-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="166e3-117">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="166e3-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="166e3-118">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="166e3-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="166e3-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="166e3-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="166e3-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="166e3-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="166e3-121">要求</span><span class="sxs-lookup"><span data-stu-id="166e3-121">Requirements</span></span>  

 <span data-ttu-id="166e3-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="166e3-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="166e3-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="166e3-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="166e3-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="166e3-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="166e3-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="166e3-125">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="166e3-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="166e3-126">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="166e3-127">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="166e3-127">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)

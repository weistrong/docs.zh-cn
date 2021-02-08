---
description: 了解详细信息： ICorRuntimeHost：： CurrentDomain 方法
title: ICorRuntimeHost::CurrentDomain 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CurrentDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CurrentDomain
helpviewer_keywords:
- ICorRuntimeHost::CreateDomain method [.NET Framework hosting]
- CurrentDomain method [.NET Framework hosting]
ms.assetid: dd2afb38-675b-4c3c-a9f3-8ab3b133eb02
topic_type:
- apiref
ms.openlocfilehash: fd75028b57475a620cc88a75016911dd0ab55b2e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784894"
---
# <a name="icorruntimehostcurrentdomain-method"></a><span data-ttu-id="e0acd-103">ICorRuntimeHost::CurrentDomain 方法</span><span class="sxs-lookup"><span data-stu-id="e0acd-103">ICorRuntimeHost::CurrentDomain Method</span></span>

<span data-ttu-id="e0acd-104">获取类型的接口指针 <xref:System.AppDomain?displayProperty=nameWithType> ，该指针表示当前线程上加载的域。</span><span class="sxs-lookup"><span data-stu-id="e0acd-104">Gets an interface pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the domain loaded on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0acd-105">语法</span><span class="sxs-lookup"><span data-stu-id="e0acd-105">Syntax</span></span>  
  
```cpp  
HRESULT CurrentDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e0acd-106">参数</span><span class="sxs-lookup"><span data-stu-id="e0acd-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="e0acd-107">弄 <xref:System.AppDomain?displayProperty=nameWithType> 表示线程的当前应用程序域的类型的指针。</span><span class="sxs-lookup"><span data-stu-id="e0acd-107">[out] A pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the thread's current application domain.</span></span> <span data-ttu-id="e0acd-108">此指针的类型为 `IUnknown` ，因此调用方通常应调用 `QueryInterface` 以获取类型的指针 <xref:System._AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="e0acd-108">This pointer is typed `IUnknown`, so callers should generally call `QueryInterface` to obtain a pointer of type <xref:System._AppDomain>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e0acd-109">返回值</span><span class="sxs-lookup"><span data-stu-id="e0acd-109">Return Value</span></span>  
  
|<span data-ttu-id="e0acd-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e0acd-110">HRESULT</span></span>|<span data-ttu-id="e0acd-111">说明</span><span class="sxs-lookup"><span data-stu-id="e0acd-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e0acd-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0acd-112">S_OK</span></span>|<span data-ttu-id="e0acd-113">操作成功。</span><span class="sxs-lookup"><span data-stu-id="e0acd-113">The operation was successful.</span></span>|  
|<span data-ttu-id="e0acd-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e0acd-114">S_FALSE</span></span>|<span data-ttu-id="e0acd-115">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="e0acd-115">The operation failed to complete.</span></span>|  
|<span data-ttu-id="e0acd-116">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e0acd-116">E_FAIL</span></span>|<span data-ttu-id="e0acd-117">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="e0acd-117">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="e0acd-118">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="e0acd-118">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="e0acd-119">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="e0acd-119">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="e0acd-120">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e0acd-120">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e0acd-121">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="e0acd-121">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e0acd-122">要求</span><span class="sxs-lookup"><span data-stu-id="e0acd-122">Requirements</span></span>  

 <span data-ttu-id="e0acd-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e0acd-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0acd-124">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e0acd-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e0acd-125">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e0acd-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e0acd-126">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="e0acd-126">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0acd-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="e0acd-127">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="e0acd-128">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="e0acd-128">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)

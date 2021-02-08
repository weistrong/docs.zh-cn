---
description: 了解详细信息： ICorRuntimeHost：： Start 方法
title: ICorRuntimeHost::Start 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::Start
helpviewer_keywords:
- Start method, ICorRuntimeHost interface [.NET Framework hosting]
- ICorRuntimeHost::Start method [.NET Framework hosting]
ms.assetid: c66f3ac5-6489-484a-9bed-c31b711cee01
topic_type:
- apiref
ms.openlocfilehash: d07c0144c7192bc2f57927c294ea472cd6b47f9f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789601"
---
# <a name="icorruntimehoststart-method"></a><span data-ttu-id="fab40-103">ICorRuntimeHost::Start 方法</span><span class="sxs-lookup"><span data-stu-id="fab40-103">ICorRuntimeHost::Start Method</span></span>

<span data-ttu-id="fab40-104"> (CLR) 启动公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="fab40-104">Starts the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fab40-105">语法</span><span class="sxs-lookup"><span data-stu-id="fab40-105">Syntax</span></span>  
  
```cpp  
HRESULT Start ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="fab40-106">返回值</span><span class="sxs-lookup"><span data-stu-id="fab40-106">Return Value</span></span>  
  
|<span data-ttu-id="fab40-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fab40-107">HRESULT</span></span>|<span data-ttu-id="fab40-108">说明</span><span class="sxs-lookup"><span data-stu-id="fab40-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fab40-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="fab40-109">S_OK</span></span>|<span data-ttu-id="fab40-110">操作成功。</span><span class="sxs-lookup"><span data-stu-id="fab40-110">The operation was successful.</span></span>|  
|<span data-ttu-id="fab40-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fab40-111">S_FALSE</span></span>|<span data-ttu-id="fab40-112">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="fab40-112">The operation failed to complete.</span></span>|  
|<span data-ttu-id="fab40-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fab40-113">E_FAIL</span></span>|<span data-ttu-id="fab40-114">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="fab40-114">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="fab40-115">如果某个方法返回 E_FAIL，则 CLR 将无法再在进程中使用。</span><span class="sxs-lookup"><span data-stu-id="fab40-115">If a method returns E_FAIL, the CLR is no longer usable in the process.</span></span> <span data-ttu-id="fab40-116">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="fab40-116">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="fab40-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fab40-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fab40-118">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="fab40-118">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fab40-119">备注</span><span class="sxs-lookup"><span data-stu-id="fab40-119">Remarks</span></span>  

 <span data-ttu-id="fab40-120">通常不需要调用 `Start` 方法，因为 CLR 会在首次运行托管代码请求时自动启动。</span><span class="sxs-lookup"><span data-stu-id="fab40-120">It is typically not necessary to call the `Start` method, because the CLR starts automatically upon the first request to run managed code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fab40-121">要求</span><span class="sxs-lookup"><span data-stu-id="fab40-121">Requirements</span></span>  

 <span data-ttu-id="fab40-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fab40-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fab40-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="fab40-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fab40-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fab40-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fab40-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="fab40-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fab40-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="fab40-126">See also</span></span>

- [<span data-ttu-id="fab40-127">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="fab40-127">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)

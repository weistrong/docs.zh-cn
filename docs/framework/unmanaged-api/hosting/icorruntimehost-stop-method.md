---
description: 了解详细信息： ICorRuntimeHost：： Stop 方法
title: ICorRuntimeHost::Stop 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.Stop
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::Stop
helpviewer_keywords:
- Stop method, ICorRuntimeHost interface [.NET Framework hosting]
- ICorRuntimeHost::Stop method [.NET Framework hosting]
ms.assetid: 46a0d450-b516-4bef-8b71-8d3bf265cbed
topic_type:
- apiref
ms.openlocfilehash: b44c77b7d0fe3a078efa11756f5fac7ba400ca5e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789588"
---
# <a name="icorruntimehoststop-method"></a><span data-ttu-id="712cd-103">ICorRuntimeHost::Stop 方法</span><span class="sxs-lookup"><span data-stu-id="712cd-103">ICorRuntimeHost::Stop Method</span></span>

<span data-ttu-id="712cd-104">停止执行当前进程的运行时中的代码。</span><span class="sxs-lookup"><span data-stu-id="712cd-104">Stops the execution of code in the runtime for the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="712cd-105">语法</span><span class="sxs-lookup"><span data-stu-id="712cd-105">Syntax</span></span>  
  
```cpp  
HRESULT Stop ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="712cd-106">返回值</span><span class="sxs-lookup"><span data-stu-id="712cd-106">Return Value</span></span>  
  
|<span data-ttu-id="712cd-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="712cd-107">HRESULT</span></span>|<span data-ttu-id="712cd-108">说明</span><span class="sxs-lookup"><span data-stu-id="712cd-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="712cd-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="712cd-109">S_OK</span></span>|<span data-ttu-id="712cd-110">操作成功。</span><span class="sxs-lookup"><span data-stu-id="712cd-110">The operation was successful.</span></span>|  
|<span data-ttu-id="712cd-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="712cd-111">S_FALSE</span></span>|<span data-ttu-id="712cd-112">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="712cd-112">The operation failed to complete.</span></span>|  
|<span data-ttu-id="712cd-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="712cd-113">E_FAIL</span></span>|<span data-ttu-id="712cd-114">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="712cd-114">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="712cd-115">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="712cd-115">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="712cd-116">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="712cd-116">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="712cd-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="712cd-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="712cd-118">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="712cd-118">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="712cd-119">备注</span><span class="sxs-lookup"><span data-stu-id="712cd-119">Remarks</span></span>  

 <span data-ttu-id="712cd-120">通常不需要调用 `Stop` 方法，因为在进程退出时代码将停止执行。</span><span class="sxs-lookup"><span data-stu-id="712cd-120">It is typically unnecessary to call the `Stop` method, because the code stops executing when the process exits.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="712cd-121">调用后 `Stop` ，无法将 CLR 重新初始化为同一进程。</span><span class="sxs-lookup"><span data-stu-id="712cd-121">After a call to `Stop`, the CLR cannot be reinitialized into the same process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="712cd-122">要求</span><span class="sxs-lookup"><span data-stu-id="712cd-122">Requirements</span></span>  

 <span data-ttu-id="712cd-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="712cd-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="712cd-124">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="712cd-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="712cd-125">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="712cd-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="712cd-126">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="712cd-126">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="712cd-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="712cd-127">See also</span></span>

- [<span data-ttu-id="712cd-128">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="712cd-128">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)

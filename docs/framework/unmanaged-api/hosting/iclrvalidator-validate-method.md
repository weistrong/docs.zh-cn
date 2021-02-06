---
description: 了解详细信息： ICLRValidator：： Validate 方法
title: ICLRValidator::Validate 方法
ms.date: 03/30/2017
api_name:
- ICLRValidator.Validate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRValidator::Validate
helpviewer_keywords:
- Validate method, ICLRValidator interface [.NET Framework hosting]
- ICLRValidator::Validate method [.NET Framework hosting]
ms.assetid: 0b1b432a-d234-4002-839b-81366c3a8bdc
topic_type:
- apiref
ms.openlocfilehash: a188315d44021fc8bf40be9bb9aecac436351467
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636736"
---
# <a name="iclrvalidatorvalidate-method"></a><span data-ttu-id="54954-103">ICLRValidator::Validate 方法</span><span class="sxs-lookup"><span data-stu-id="54954-103">ICLRValidator::Validate Method</span></span>

<span data-ttu-id="54954-104">验证指定文件中 (PE) 或 Microsoft 中间语言 (MSIL) 的可移植可执行文件。</span><span class="sxs-lookup"><span data-stu-id="54954-104">Validates the portable executable (PE) or Microsoft intermediate language (MSIL) in the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54954-105">语法</span><span class="sxs-lookup"><span data-stu-id="54954-105">Syntax</span></span>  
  
```cpp  
HRESULT Validate (  
    [in] IVEHandler        *veh,  
    [in] unsigned long      ulAppDomainId,  
    [in] unsigned long      ulFlags,  
    [in] unsigned long      ulMaxError,  
    [in] unsigned long      token,  
    [in] LPWSTR             fileName,  
    [in, size_is(ulSize)] BYTE *pe,  
    [in] unsigned long      ulSize  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="54954-106">参数</span><span class="sxs-lookup"><span data-stu-id="54954-106">Parameters</span></span>  

 `veh`  
 <span data-ttu-id="54954-107">中指向 `IVEHandler` 处理验证错误的实例的指针。</span><span class="sxs-lookup"><span data-stu-id="54954-107">[in] A pointer to an `IVEHandler` instance that handles validation errors.</span></span>  
  
 `ulAppDomainId`  
 <span data-ttu-id="54954-108">中当前的标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="54954-108">[in] The identifier for the current <xref:System.AppDomain>.</span></span>  
  
 `ulFlags`  
 <span data-ttu-id="54954-109">中 [ValidatorFlags](validatorflags-enumeration.md) 值的组合，用于指示应执行的验证类型。</span><span class="sxs-lookup"><span data-stu-id="54954-109">[in] A combination of [ValidatorFlags](validatorflags-enumeration.md) values, indicating the kind of validation that should be performed.</span></span>  
  
 `ulMaxError`  
 <span data-ttu-id="54954-110">中在退出验证之前允许的最大错误数。</span><span class="sxs-lookup"><span data-stu-id="54954-110">[in] The maximum number of errors to allow before exiting the validation.</span></span>  
  
 `token`  
 <span data-ttu-id="54954-111">中用.</span><span class="sxs-lookup"><span data-stu-id="54954-111">[in] Unused.</span></span>  
  
 `fileName`  
 <span data-ttu-id="54954-112">中要验证的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="54954-112">[in] The name of the file to be validated.</span></span>  
  
 `pe`  
 <span data-ttu-id="54954-113">中指向文件缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="54954-113">[in] A pointer to the file buffer.</span></span>  
  
 `ulSize`  
 <span data-ttu-id="54954-114">中要验证的文件的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="54954-114">[in] The size, in bytes, of the file to be validated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="54954-115">返回值</span><span class="sxs-lookup"><span data-stu-id="54954-115">Return Value</span></span>  
  
|<span data-ttu-id="54954-116">HRESULT</span><span class="sxs-lookup"><span data-stu-id="54954-116">HRESULT</span></span>|<span data-ttu-id="54954-117">说明</span><span class="sxs-lookup"><span data-stu-id="54954-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="54954-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="54954-118">S_OK</span></span>|<span data-ttu-id="54954-119">`Validate` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="54954-119">`Validate` returned successfully.</span></span>|  
|<span data-ttu-id="54954-120">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="54954-120">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="54954-121"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="54954-121">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="54954-122">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="54954-122">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="54954-123">调用超时。</span><span class="sxs-lookup"><span data-stu-id="54954-123">The call timed out.</span></span>|  
|<span data-ttu-id="54954-124">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="54954-124">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="54954-125">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="54954-125">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="54954-126">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="54954-126">HOST_E_ABANDONED</span></span>|<span data-ttu-id="54954-127">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="54954-127">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="54954-128">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="54954-128">E_FAIL</span></span>|<span data-ttu-id="54954-129">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="54954-129">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="54954-130">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="54954-130">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="54954-131">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="54954-131">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="54954-132">要求</span><span class="sxs-lookup"><span data-stu-id="54954-132">Requirements</span></span>  

 <span data-ttu-id="54954-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="54954-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54954-134">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="54954-134">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="54954-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="54954-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="54954-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54954-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54954-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="54954-137">See also</span></span>

- [<span data-ttu-id="54954-138">ICLRValidator 接口</span><span class="sxs-lookup"><span data-stu-id="54954-138">ICLRValidator Interface</span></span>](iclrvalidator-interface.md)

---
description: 了解详细信息： ICLRPolicyManager 接口
title: ICLRPolicyManager 接口
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager
helpviewer_keywords:
- ICLRPolicyManager interface [.NET Framework hosting]
ms.assetid: 5c834aa1-f2db-408a-b230-c7bec093d364
topic_type:
- apiref
ms.openlocfilehash: 8823f1db8b15b327306ff3c592b46c94537f4331
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637373"
---
# <a name="iclrpolicymanager-interface"></a><span data-ttu-id="a95dd-103">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="a95dd-103">ICLRPolicyManager Interface</span></span>

<span data-ttu-id="a95dd-104">提供允许主机指定在发生故障和超时时要执行的策略操作的方法。</span><span class="sxs-lookup"><span data-stu-id="a95dd-104">Provides methods that allow the host to specify policy actions to be taken in the event of failures and timeouts.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a95dd-105">方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-105">Methods</span></span>  
  
|<span data-ttu-id="a95dd-106">方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-106">Method</span></span>|<span data-ttu-id="a95dd-107">说明</span><span class="sxs-lookup"><span data-stu-id="a95dd-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a95dd-108">SetActionOnFailure 方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-108">SetActionOnFailure Method</span></span>](iclrpolicymanager-setactiononfailure-method.md)|<span data-ttu-id="a95dd-109">指定发生指定的故障时公共语言运行时 (CLR) 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="a95dd-109">Specifies the policy action the common language runtime (CLR) should take when the specified failure occurs.</span></span>|  
|[<span data-ttu-id="a95dd-110">SetActionOnTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-110">SetActionOnTimeout Method</span></span>](iclrpolicymanager-setactionontimeout-method.md)|<span data-ttu-id="a95dd-111">指定在指定操作超时时 CLR 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="a95dd-111">Specifies the policy action the CLR should take when the specified operation times out.</span></span>|  
|[<span data-ttu-id="a95dd-112">SetDefaultAction 方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-112">SetDefaultAction Method</span></span>](iclrpolicymanager-setdefaultaction-method.md)|<span data-ttu-id="a95dd-113">指定发生指定操作时 CLR 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="a95dd-113">Specifies the policy action the CLR should take when the specified operation occurs.</span></span>|  
|[<span data-ttu-id="a95dd-114">SetTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-114">SetTimeout Method</span></span>](iclrpolicymanager-settimeout-method.md)|<span data-ttu-id="a95dd-115">设置指定操作的超时值。</span><span class="sxs-lookup"><span data-stu-id="a95dd-115">Sets a timeout value for the specified operation.</span></span>|  
|[<span data-ttu-id="a95dd-116">SetTimeoutAndAction 方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-116">SetTimeoutAndAction Method</span></span>](iclrpolicymanager-settimeoutandaction-method.md)|<span data-ttu-id="a95dd-117">设置指定操作的超时值，并指定该操作发生时 CLR 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="a95dd-117">Sets a timeout value for the specified operation, and specifies the policy action the CLR should take when the operation occurs.</span></span>|  
|[<span data-ttu-id="a95dd-118">SetUnhandledExceptionPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="a95dd-118">SetUnhandledExceptionPolicy Method</span></span>](iclrpolicymanager-setunhandledexceptionpolicy-method.md)|<span data-ttu-id="a95dd-119">指定发生未经处理的异常时 CLR 的行为。</span><span class="sxs-lookup"><span data-stu-id="a95dd-119">Specifies the behavior of the CLR when an unhandled exception occurs.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a95dd-120">要求</span><span class="sxs-lookup"><span data-stu-id="a95dd-120">Requirements</span></span>  

 <span data-ttu-id="a95dd-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a95dd-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a95dd-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a95dd-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a95dd-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a95dd-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a95dd-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a95dd-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a95dd-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="a95dd-125">See also</span></span>

- [<span data-ttu-id="a95dd-126">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="a95dd-126">EClrFailure Enumeration</span></span>](eclrfailure-enumeration.md)
- [<span data-ttu-id="a95dd-127">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="a95dd-127">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="a95dd-128">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="a95dd-128">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="a95dd-129">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="a95dd-129">ICLRControl Interface</span></span>](iclrcontrol-interface.md)

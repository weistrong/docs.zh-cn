---
description: 了解详细信息： EPolicyAction 枚举
title: EPolicyAction 枚举
ms.date: 03/30/2017
api_name:
- EPolicyAction
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EPolicyAction
helpviewer_keywords:
- EPolicyAction enumeration [.NET Framework hosting]
ms.assetid: 72dd76ba-239e-45ac-9ded-318fb07d6c6d
topic_type:
- apiref
ms.openlocfilehash: fb66de2211972bd4d25ccfbab4965f315c0144a2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785447"
---
# <a name="epolicyaction-enumeration"></a><span data-ttu-id="cdc52-103">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="cdc52-103">EPolicyAction Enumeration</span></span>

<span data-ttu-id="cdc52-104">描述主机可为 [EClrOperation](eclroperation-enumeration.md) 描述的操作设置的策略操作以及 [EClrFailure](eclrfailure-enumeration.md)描述的故障。</span><span class="sxs-lookup"><span data-stu-id="cdc52-104">Describes the policy actions the host can set for operations described by [EClrOperation](eclroperation-enumeration.md) and failures described by [EClrFailure](eclrfailure-enumeration.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdc52-105">语法</span><span class="sxs-lookup"><span data-stu-id="cdc52-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eNoAction,  
    eThrowException,  
    eAbortThread,  
    eRudeAbortThread,  
    eUnloadAppDomain,  
    eRudeUnloadAppDomain,  
    eExitProcess,  
    eFastExitProcess,  
    eRudeExitProcess,  
    eDisableRuntime  
} EPolicyAction;  
```  
  
## <a name="members"></a><span data-ttu-id="cdc52-106">成员</span><span class="sxs-lookup"><span data-stu-id="cdc52-106">Members</span></span>  
  
|<span data-ttu-id="cdc52-107">成员</span><span class="sxs-lookup"><span data-stu-id="cdc52-107">Member</span></span>|<span data-ttu-id="cdc52-108">说明</span><span class="sxs-lookup"><span data-stu-id="cdc52-108">Description</span></span>|  
|------------|-----------------|  
|`eAbortThread`|<span data-ttu-id="cdc52-109">指定公共语言运行时 (CLR) 应正常中止线程。</span><span class="sxs-lookup"><span data-stu-id="cdc52-109">Specifies that the common language runtime (CLR) should abort the thread gracefully.</span></span> <span data-ttu-id="cdc52-110">正常中止包括尝试运行所有 `finally` 块、 `catch` 与线程中止相关的任何块和终结器。</span><span class="sxs-lookup"><span data-stu-id="cdc52-110">A graceful abort includes attempts to run all `finally` blocks, any `catch` blocks related to thread aborts, and finalizers.</span></span>|  
|`eDisableRuntime`|<span data-ttu-id="cdc52-111">指定 CLR 应进入禁用状态。</span><span class="sxs-lookup"><span data-stu-id="cdc52-111">Specifies that the CLR should enter a disabled state.</span></span> <span data-ttu-id="cdc52-112">在受影响的进程中，不能再执行其他托管代码，并且阻止线程进入 CLR。</span><span class="sxs-lookup"><span data-stu-id="cdc52-112">No further managed code can be executed in the affected process, and threads are blocked from entering the CLR.</span></span>|  
|`eExitProcess`|<span data-ttu-id="cdc52-113">指定 CLR 应尝试正常退出进程，包括运行终结器并执行清理和日志记录操作。</span><span class="sxs-lookup"><span data-stu-id="cdc52-113">Specifies that the CLR should attempt a graceful exit of the process, including running finalizers and performing cleanup and logging operations.</span></span>|  
|`eFastExitProcess`|<span data-ttu-id="cdc52-114">指定 CLR 应立即退出进程，而无需运行终结器或执行清理和日志记录操作。</span><span class="sxs-lookup"><span data-stu-id="cdc52-114">Specifies that the CLR should exit the process immediately, without running finalizers or performing cleanup and logging operations.</span></span> <span data-ttu-id="cdc52-115">但是，通知将发送到调试器。</span><span class="sxs-lookup"><span data-stu-id="cdc52-115">However, notification is sent to the debugger.</span></span>|  
|`eNoAction`|<span data-ttu-id="cdc52-116">指定不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="cdc52-116">Specifies that no action should be taken.</span></span>|  
|`eRudeAbortThread`|<span data-ttu-id="cdc52-117">指定 CLR 应执行强制的线程中止。</span><span class="sxs-lookup"><span data-stu-id="cdc52-117">Specifies that the CLR should perform a rude thread abort.</span></span> <span data-ttu-id="cdc52-118">只 `catch` `finally` 会执行标记为的和块 <xref:System.EnterpriseServices.MustRunInClientContextAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="cdc52-118">Only those `catch` and `finally` blocks marked with <xref:System.EnterpriseServices.MustRunInClientContextAttribute> are executed.</span></span>|  
|`eRudeExitProcess`|<span data-ttu-id="cdc52-119">指定 CLR 应退出进程，而不运行终结器或日志记录操作。</span><span class="sxs-lookup"><span data-stu-id="cdc52-119">Specifies that the CLR should exit the process without running finalizers or logging operations.</span></span>|  
|`eRudeUnloadAppDomain`|<span data-ttu-id="cdc52-120">指定 CLR 应执行的强制卸载 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="cdc52-120">Specifies that the CLR should perform a rude unload of the <xref:System.AppDomain>.</span></span> <span data-ttu-id="cdc52-121">仅执行标记为的终结器 <xref:System.EnterpriseServices.MustRunInClientContextAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="cdc52-121">Only finalizers marked with <xref:System.EnterpriseServices.MustRunInClientContextAttribute> are executed.</span></span> <span data-ttu-id="cdc52-122">同样，在其堆栈中具有此类的所有线程都 <xref:System.AppDomain> 将接收 `ThreadAbortException` ，但仅 `catch` 执行标记为的和 `finally` 块 <xref:System.EnterpriseServices.MustRunInClientContextAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="cdc52-122">Similarly, all threads with this <xref:System.AppDomain> in their stack receive a `ThreadAbortException`, but only those `catch` and `finally` blocks marked with <xref:System.EnterpriseServices.MustRunInClientContextAttribute> are executed.</span></span>|  
|`eThrowException`|<span data-ttu-id="cdc52-123">指定应引发适用于条件的异常，例如内存不足、缓冲区溢出，等等。</span><span class="sxs-lookup"><span data-stu-id="cdc52-123">Specifies that an exception appropriate to the condition, such as out-of-memory, buffer overflow, and so forth, should be thrown.</span></span>|  
|`eUnloadAppDomain`|<span data-ttu-id="cdc52-124">指定 <xref:System.AppDomain> 应卸载。</span><span class="sxs-lookup"><span data-stu-id="cdc52-124">Specifies that the <xref:System.AppDomain> should be unloaded.</span></span> <span data-ttu-id="cdc52-125">CLR 尝试运行终结器。</span><span class="sxs-lookup"><span data-stu-id="cdc52-125">The CLR attempts to run finalizers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cdc52-126">备注</span><span class="sxs-lookup"><span data-stu-id="cdc52-126">Remarks</span></span>  

 <span data-ttu-id="cdc52-127">宿主通过调用 [ICLRPolicyManager](iclrpolicymanager-interface.md) 接口的方法来设置策略操作。</span><span class="sxs-lookup"><span data-stu-id="cdc52-127">The host sets policy actions by calling methods of the [ICLRPolicyManager](iclrpolicymanager-interface.md) interface.</span></span> <span data-ttu-id="cdc52-128">有关 "强制" 和 "正常中止" 的信息，请参阅 [EClrOperation](eclroperation-enumeration.md) 枚举。</span><span class="sxs-lookup"><span data-stu-id="cdc52-128">For information about rude and graceful aborts, see the [EClrOperation](eclroperation-enumeration.md) enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cdc52-129">要求</span><span class="sxs-lookup"><span data-stu-id="cdc52-129">Requirements</span></span>  

 <span data-ttu-id="cdc52-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cdc52-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cdc52-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cdc52-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cdc52-132">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cdc52-132">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cdc52-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cdc52-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdc52-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="cdc52-134">See also</span></span>

- [<span data-ttu-id="cdc52-135">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="cdc52-135">EClrFailure Enumeration</span></span>](eclrfailure-enumeration.md)
- [<span data-ttu-id="cdc52-136">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="cdc52-136">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="cdc52-137">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="cdc52-137">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
- [<span data-ttu-id="cdc52-138">承载枚举</span><span class="sxs-lookup"><span data-stu-id="cdc52-138">Hosting Enumerations</span></span>](hosting-enumerations.md)

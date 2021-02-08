---
description: 了解详细信息： EClrFailure 枚举
title: EClrFailure 枚举
ms.date: 03/30/2017
api_name:
- EClrFailure
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrFailure
helpviewer_keywords:
- EClrFailure enumeration [.NET Framework hosting]
ms.assetid: 37b95cce-9bfb-4ecf-a00b-33dcba782c67
topic_type:
- apiref
ms.openlocfilehash: 9f3a2270651e5b05d2d31ed90511b8eb05dd4d44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785575"
---
# <a name="eclrfailure-enumeration"></a><span data-ttu-id="5b74f-103">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="5b74f-103">EClrFailure Enumeration</span></span>

<span data-ttu-id="5b74f-104">描述主机可对其设置策略操作的失败集。</span><span class="sxs-lookup"><span data-stu-id="5b74f-104">Describes the set of failures for which a host can set policy actions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b74f-105">语法</span><span class="sxs-lookup"><span data-stu-id="5b74f-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    FAIL_NonCriticalResource,  
    FAIL_CriticalResource,  
    FAIL_FatalRuntime,  
    FAIL_OrphanedLock  
    FAIL_StackOverflow  
    FAIL_AccessViolation  
    FAIL_CodeContract  
} EClrFailure;  
```  
  
## <a name="members"></a><span data-ttu-id="5b74f-106">成员</span><span class="sxs-lookup"><span data-stu-id="5b74f-106">Members</span></span>  
  
|<span data-ttu-id="5b74f-107">成员</span><span class="sxs-lookup"><span data-stu-id="5b74f-107">Member</span></span>|<span data-ttu-id="5b74f-108">说明</span><span class="sxs-lookup"><span data-stu-id="5b74f-108">Description</span></span>|  
|------------|-----------------|  
|`FAIL_NonCriticalResource`|<span data-ttu-id="5b74f-109">尝试在非关键的代码区域中分配资源 (如线程、内存块或锁定) 时出现错误。</span><span class="sxs-lookup"><span data-stu-id="5b74f-109">A failure occurred during an attempt to allocate a resource (such as a thread, a block of memory, or a lock) in a non-critical region of code.</span></span>|  
|`FAIL_CriticalResource`|<span data-ttu-id="5b74f-110">尝试在关键的代码区域中分配资源 (如线程、内存块或锁定) 时出现错误。</span><span class="sxs-lookup"><span data-stu-id="5b74f-110">A failure occurred during an attempt to allocate a resource (such as a thread, a block of memory, or a lock) in a critical region of code.</span></span>|  
|`FAIL_FatalRuntime`|<span data-ttu-id="5b74f-111"> (CLR) 的公共语言运行时无法再运行进程中的托管代码。</span><span class="sxs-lookup"><span data-stu-id="5b74f-111">The common language runtime (CLR) is no longer able to run managed code in the process.</span></span> <span data-ttu-id="5b74f-112">之后，对任何宿主函数的调用都会返回 HOST_E_CLRNOTAVAILABLE 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="5b74f-112">Henceforth, calls to any hosting functions return an HRESULT value of HOST_E_CLRNOTAVAILABLE.</span></span>|  
|`FAIL_OrphanedLock`|<span data-ttu-id="5b74f-113">在从对象返回时，线程无法释放锁 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="5b74f-113">A thread has failed to release a lock upon returning from an <xref:System.AppDomain> object.</span></span> <span data-ttu-id="5b74f-114">宿主无法将此失败设置为导致线程中止。</span><span class="sxs-lookup"><span data-stu-id="5b74f-114">The host cannot set this failure to cause a thread to abort.</span></span>|  
|`FAIL_StackOverflow`|<span data-ttu-id="5b74f-115">发生堆栈溢出。</span><span class="sxs-lookup"><span data-stu-id="5b74f-115">A stack overflow has occurred.</span></span>|  
|`FAIL_AccessViolation`|<span data-ttu-id="5b74f-116">尝试读取或写入受保护的内存。</span><span class="sxs-lookup"><span data-stu-id="5b74f-116">An attempt was made to read or write protected memory.</span></span> <span data-ttu-id="5b74f-117">在 .NET Framework 4 中不受支持。</span><span class="sxs-lookup"><span data-stu-id="5b74f-117">Not supported in the .NET Framework 4.</span></span>|  
|`FAIL_CodeContract`|<span data-ttu-id="5b74f-118">发生代码协定失败。</span><span class="sxs-lookup"><span data-stu-id="5b74f-118">A code contract failure occurred.</span></span> <span data-ttu-id="5b74f-119">请参阅 [代码协定](../../debug-trace-profile/code-contracts.md)。</span><span class="sxs-lookup"><span data-stu-id="5b74f-119">See [Code Contracts](../../debug-trace-profile/code-contracts.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5b74f-120">备注</span><span class="sxs-lookup"><span data-stu-id="5b74f-120">Remarks</span></span>  

 <span data-ttu-id="5b74f-121">请参阅 [ICLRPolicyManager：： SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) 方法，以获取 [EPolicyAction](epolicyaction-enumeration.md) 值的列表，主机可以使用这些值来指定失败情况的策略操作。</span><span class="sxs-lookup"><span data-stu-id="5b74f-121">See the [ICLRPolicyManager::SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) method for a list of [EPolicyAction](epolicyaction-enumeration.md) values the host can use to specify the policy actions for failure conditions.</span></span> <span data-ttu-id="5b74f-122">有关代码的关键和非关键区域的详细信息，请参阅 [EClrOperation](eclroperation-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="5b74f-122">For more information about critical and non-critical regions of code, see [EClrOperation](eclroperation-enumeration.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b74f-123">要求</span><span class="sxs-lookup"><span data-stu-id="5b74f-123">Requirements</span></span>  

 <span data-ttu-id="5b74f-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5b74f-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b74f-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5b74f-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5b74f-126">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5b74f-126">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5b74f-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b74f-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b74f-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b74f-128">See also</span></span>

- [<span data-ttu-id="5b74f-129">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="5b74f-129">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="5b74f-130">SetActionOnFailure 方法</span><span class="sxs-lookup"><span data-stu-id="5b74f-130">SetActionOnFailure Method</span></span>](iclrpolicymanager-setactiononfailure-method.md)
- [<span data-ttu-id="5b74f-131">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="5b74f-131">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
- [<span data-ttu-id="5b74f-132">承载枚举</span><span class="sxs-lookup"><span data-stu-id="5b74f-132">Hosting Enumerations</span></span>](hosting-enumerations.md)

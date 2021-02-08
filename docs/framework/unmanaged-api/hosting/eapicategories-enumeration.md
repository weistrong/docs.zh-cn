---
description: 了解详细信息： EApiCategories 枚举
title: EApiCategories 枚举
ms.date: 03/30/2017
api_name:
- EApiCategories
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EApiCategories
helpviewer_keywords:
- EApiCategories enumeration [.NET Framework hosting]
ms.assetid: 3c4a8a5a-8a46-4ac9-947f-4959bc9d6ac6
topic_type:
- apiref
ms.openlocfilehash: 58a7d4fa4d0c965bf9158ad6713185782d4ae94a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785622"
---
# <a name="eapicategories-enumeration"></a><span data-ttu-id="61be8-103">EApiCategories 枚举</span><span class="sxs-lookup"><span data-stu-id="61be8-103">EApiCategories Enumeration</span></span>

<span data-ttu-id="61be8-104">描述宿主可阻止在部分受信任代码中运行的功能类别。</span><span class="sxs-lookup"><span data-stu-id="61be8-104">Describes the categories of capabilities that the host can block from running in partially trusted code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61be8-105">语法</span><span class="sxs-lookup"><span data-stu-id="61be8-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eNoCategory               = 0,  
    eSynchronization          = 0x1,  
    eSharedState              = 0x2,  
    eExternalProcessMgmt      = 0x4,  
    eSelfAffectingProcessMgmt = 0x8,  
    eExternalThreading        = 0x10,  
    eSelfAffectingThreading   = 0x20,  
    eSecurityInfrastructure   = 0x40,  
    eUI                       = 0x80,  
    eMayLeakOnAbort           = 0x100,  
    eAll                      = 0x1ff  
} EHostProtectionCategories;  
```  
  
## <a name="members"></a><span data-ttu-id="61be8-106">成员</span><span class="sxs-lookup"><span data-stu-id="61be8-106">Members</span></span>  
  
|<span data-ttu-id="61be8-107">成员</span><span class="sxs-lookup"><span data-stu-id="61be8-107">Member</span></span>|<span data-ttu-id="61be8-108">说明</span><span class="sxs-lookup"><span data-stu-id="61be8-108">Description</span></span>|  
|------------|-----------------|  
|`eAll`|<span data-ttu-id="61be8-109">指定阻止其他字段所涵盖的所有托管类和成员 `EApiCategories` 在部分受信任的代码中运行。</span><span class="sxs-lookup"><span data-stu-id="61be8-109">Specifies that all managed classes and members that are covered by other `EApiCategories` fields be blocked from running in partially trusted code.</span></span>|  
|`eExternalProcessMgmt`|<span data-ttu-id="61be8-110">指定禁止在部分受信任的代码中运行外部进程的创建、操作和析构的托管类和成员。</span><span class="sxs-lookup"><span data-stu-id="61be8-110">Specifies that managed classes and members that allow the creation, manipulation, and destruction of external processes be blocked from running in partially trusted code.</span></span>|  
|`eExternalThreading`|<span data-ttu-id="61be8-111">指定允许在部分受信任的代码中阻止创建、操作和销毁外部线程的托管类和成员。</span><span class="sxs-lookup"><span data-stu-id="61be8-111">Specifies that managed classes and members that allow the creation, manipulation, and destruction of external threads be blocked from running in partially trusted code.</span></span>|  
|`eMayLeakOnAbort`|<span data-ttu-id="61be8-112">指定在部分受信任的代码中阻止在中止时可能泄漏内存的托管类型和成员。</span><span class="sxs-lookup"><span data-stu-id="61be8-112">Specifies that managed types and members that could potentially leak memory on abort be blocked from running in partially trusted code.</span></span>|  
|`eNoCategory`|<span data-ttu-id="61be8-113">指定禁止在部分受信任的代码中运行托管代码类别。</span><span class="sxs-lookup"><span data-stu-id="61be8-113">Specifies that no managed code categories be blocked from running in partially trusted code.</span></span>|  
|`eSecurityInfrastructure`|<span data-ttu-id="61be8-114">指定公共语言运行时 (CLR) 安全基础结构被阻止部分受信任的代码使用。</span><span class="sxs-lookup"><span data-stu-id="61be8-114">Specifies that the common language runtime (CLR) security infrastructure be blocked from being used by partially trusted code.</span></span>|  
|`eSelfAffectingProcessMgmt`|<span data-ttu-id="61be8-115">指定在部分受信任的代码中阻止其功能影响托管进程的托管类和成员运行。</span><span class="sxs-lookup"><span data-stu-id="61be8-115">Specifies that managed classes and members whose capabilities can affect the hosted process be blocked from running in partially trusted code.</span></span>|  
|`eSelfAffectingThreading`|<span data-ttu-id="61be8-116">指定在部分受信任的代码中阻止其功能影响托管进程中的线程的托管类和成员。</span><span class="sxs-lookup"><span data-stu-id="61be8-116">Specifies that managed classes and members whose capabilities can affect threads in the hosted process be blocked from running in partially trusted code.</span></span>|  
|`eSharedState`|<span data-ttu-id="61be8-117">指定阻止公开共享状态的托管类和成员在部分受信任的代码中运行。</span><span class="sxs-lookup"><span data-stu-id="61be8-117">Specifies that managed classes and members that expose shared state be blocked from running in partially trusted code.</span></span>|  
|`eSynchronization`|<span data-ttu-id="61be8-118">指定允许用户代码持有锁的公共语言运行时类和成员阻止在部分受信任的代码中运行。</span><span class="sxs-lookup"><span data-stu-id="61be8-118">Specifies that common language runtime classes and members that allow user code to hold locks be blocked from running in partially trusted code.</span></span>|  
|`eUI`|<span data-ttu-id="61be8-119">指定在部分受信任的代码中阻止允许或要求人工交互的托管类和成员。</span><span class="sxs-lookup"><span data-stu-id="61be8-119">Specifies that managed classes and members that allow or require human interaction be blocked from running in partially trusted code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="61be8-120">备注</span><span class="sxs-lookup"><span data-stu-id="61be8-120">Remarks</span></span>  

 <span data-ttu-id="61be8-121">[ICLRHostProtectionManager：： SetProtectedCategories](iclrhostprotectionmanager-setprotectedcategories-method.md)方法采用类型的参数 `EApiCategories` 。</span><span class="sxs-lookup"><span data-stu-id="61be8-121">The [ICLRHostProtectionManager::SetProtectedCategories](iclrhostprotectionmanager-setprotectedcategories-method.md) method takes a parameter of type `EApiCategories`.</span></span>  
  
 <span data-ttu-id="61be8-122">`EApiCategories`枚举和方法与 `SetProtectedCategories` 托管类直接相关 <xref:System.Security.Permissions.HostProtectionAttribute?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="61be8-122">The `EApiCategories` enumeration and the `SetProtectedCategories` method are directly related to the managed <xref:System.Security.Permissions.HostProtectionAttribute?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="61be8-123">托管类与枚举一起使用 <xref:System.Security.Permissions.HostProtectionResource?displayProperty=nameWithType> ，其值直接对应于 `EApiCategories` 值，用于标记公开与所述的类别对应的功能的托管类型和成员 `EApiCategories` 。</span><span class="sxs-lookup"><span data-stu-id="61be8-123">The managed class is used with the <xref:System.Security.Permissions.HostProtectionResource?displayProperty=nameWithType> enumeration, whose values correspond directly to the `EApiCategories` values, to mark managed types and members that expose capabilities corresponding to the categories described by `EApiCategories`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61be8-124">要求</span><span class="sxs-lookup"><span data-stu-id="61be8-124">Requirements</span></span>  

 <span data-ttu-id="61be8-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="61be8-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61be8-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="61be8-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="61be8-127">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="61be8-127">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="61be8-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61be8-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61be8-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="61be8-129">See also</span></span>

- [<span data-ttu-id="61be8-130">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="61be8-130">ICLRHostProtectionManager Interface</span></span>](iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="61be8-131">承载枚举</span><span class="sxs-lookup"><span data-stu-id="61be8-131">Hosting Enumerations</span></span>](hosting-enumerations.md)

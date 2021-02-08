---
description: 了解详细信息： EContextType 枚举
title: EContextType 枚举
ms.date: 03/30/2017
api_name:
- EContextType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EContextType
helpviewer_keywords:
- EContextType enumeration [.NET Framework hosting]
ms.assetid: 92b926a9-b87e-408a-9036-df7b752c9492
topic_type:
- apiref
ms.openlocfilehash: b7d6ddb385386bb0616a01ef6fcc432f2c925d51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785522"
---
# <a name="econtexttype-enumeration"></a><span data-ttu-id="39f2d-103">EContextType 枚举</span><span class="sxs-lookup"><span data-stu-id="39f2d-103">EContextType Enumeration</span></span>

<span data-ttu-id="39f2d-104">描述当前正在执行的线程的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="39f2d-104">Describes the security context of the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39f2d-105">语法</span><span class="sxs-lookup"><span data-stu-id="39f2d-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eCurrentContext    = 0x00,  
    eRestrictedContext = 0x01  
} EContextType;  
```  
  
## <a name="members"></a><span data-ttu-id="39f2d-106">成员</span><span class="sxs-lookup"><span data-stu-id="39f2d-106">Members</span></span>  
  
|<span data-ttu-id="39f2d-107">成员</span><span class="sxs-lookup"><span data-stu-id="39f2d-107">Member</span></span>|<span data-ttu-id="39f2d-108">说明</span><span class="sxs-lookup"><span data-stu-id="39f2d-108">Description</span></span>|  
|------------|-----------------|  
|`eCurrentContext`|<span data-ttu-id="39f2d-109">指示当公共语言运行时 (CLR) 在调用[IHostSecurityManager：： SetSecurityContext](ihostsecuritymanager-setsecuritycontext-method.md)方法的调用中调用[IHostSecurityManager：： GETSECURITYCONTEXT](ihostsecuritymanager-getsecuritycontext-method.md)方法或 CLR 请求的上下文时，当前线程上的上下文。</span><span class="sxs-lookup"><span data-stu-id="39f2d-109">Indicates the context on the current thread at the time the common language runtime (CLR) calls the [IHostSecurityManager::GetSecurityContext](ihostsecuritymanager-getsecuritycontext-method.md) method, or the context requested by the CLR in a call to the [IHostSecurityManager::SetSecurityContext](ihostsecuritymanager-setsecuritycontext-method.md) method.</span></span>|  
|`eRestrictedContext`|<span data-ttu-id="39f2d-110">指示宿主具有更低权限的上下文，如垃圾回收器或类或模块构造函数。</span><span class="sxs-lookup"><span data-stu-id="39f2d-110">Indicates a context over which the host has lower privileges, such as the garbage collector, or class or module constructors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="39f2d-111">备注</span><span class="sxs-lookup"><span data-stu-id="39f2d-111">Remarks</span></span>  

 <span data-ttu-id="39f2d-112">`EContextType`在对和方法的调用中，CLR 将值之一作为参数值 `IHostSecurityManager::GetSecurityContext` 提供 `IHostSecurityManager::SetSecurityContext` 。</span><span class="sxs-lookup"><span data-stu-id="39f2d-112">The CLR supplies one of the `EContextType` values as a parameter value in calls to the `IHostSecurityManager::GetSecurityContext` and `IHostSecurityManager::SetSecurityContext` methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39f2d-113">要求</span><span class="sxs-lookup"><span data-stu-id="39f2d-113">Requirements</span></span>  

 <span data-ttu-id="39f2d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="39f2d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39f2d-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="39f2d-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="39f2d-116">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="39f2d-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="39f2d-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39f2d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39f2d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="39f2d-118">See also</span></span>

- [<span data-ttu-id="39f2d-119">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="39f2d-119">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="39f2d-120">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="39f2d-120">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="39f2d-121">承载枚举</span><span class="sxs-lookup"><span data-stu-id="39f2d-121">Hosting Enumerations</span></span>](hosting-enumerations.md)

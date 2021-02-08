---
description: 了解详细信息： EBindPolicyLevels 枚举
title: EBindPolicyLevels 枚举
ms.date: 03/30/2017
api_name:
- EBindPolicyLevels
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EBindPolicyLevels
helpviewer_keywords:
- EBindPolicyLevels enumeration [.NET Framework hosting]
ms.assetid: a9e00b4f-b6d0-4257-bd88-4fe9af97b8fa
topic_type:
- apiref
ms.openlocfilehash: 00e10cff79cdd782e8d9ab8e9b7e1e3f388fb1ee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785609"
---
# <a name="ebindpolicylevels-enumeration"></a><span data-ttu-id="d5832-103">EBindPolicyLevels 枚举</span><span class="sxs-lookup"><span data-stu-id="d5832-103">EBindPolicyLevels Enumeration</span></span>

<span data-ttu-id="d5832-104">提供用于指定应用或修改程序集策略的级别的标志。</span><span class="sxs-lookup"><span data-stu-id="d5832-104">Provides flags to specify the level at which to apply or modify assembly policy.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5832-105">语法</span><span class="sxs-lookup"><span data-stu-id="d5832-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    ePolicyLevelNone         = 0x0,  
    ePolicyLevelRetargetable = 0x1,  
    ePolicyUnifiedToCLR      = 0x2,  
    ePolicyLevelApp          = 0x4,  
    ePolicyLevelPublisher    = 0x8,  
    ePolicyLevelHost         = 0x10,  
    ePolicyLevelAdmin        = 0x20  
    ePolicyPortability       = 0x40  
} EBindPolicyLevels;  
```  
  
## <a name="members"></a><span data-ttu-id="d5832-106">成员</span><span class="sxs-lookup"><span data-stu-id="d5832-106">Members</span></span>  
  
|<span data-ttu-id="d5832-107">成员</span><span class="sxs-lookup"><span data-stu-id="d5832-107">Member</span></span>|<span data-ttu-id="d5832-108">说明</span><span class="sxs-lookup"><span data-stu-id="d5832-108">Description</span></span>|  
|------------|-----------------|  
|`ePolicyLevelAdmin`|<span data-ttu-id="d5832-109">指定应在管理员级别应用策略。</span><span class="sxs-lookup"><span data-stu-id="d5832-109">Specifies that policy should be applied at the administrator level.</span></span>|  
|`ePolicyLevelApp`|<span data-ttu-id="d5832-110">指定应在应用程序级别应用策略。</span><span class="sxs-lookup"><span data-stu-id="d5832-110">Specifies that policy should be applied at the application level.</span></span>|  
|`ePolicyLevelHost`|<span data-ttu-id="d5832-111">指定应在主机级别上应用策略。</span><span class="sxs-lookup"><span data-stu-id="d5832-111">Specifies that policy should be applied at the host level.</span></span>|  
|`ePolicyLevelNone`|<span data-ttu-id="d5832-112">不指定策略级别标志。</span><span class="sxs-lookup"><span data-stu-id="d5832-112">Specifies no policy-level flags.</span></span>|  
|`ePolicyLevelPublisher`|<span data-ttu-id="d5832-113">指定应在发布服务器级别应用策略。</span><span class="sxs-lookup"><span data-stu-id="d5832-113">Specifies that policy should be applied at the publisher level.</span></span>|  
|`ePolicyLevelRetargetable`|<span data-ttu-id="d5832-114">指定策略应在可变级别上适用。</span><span class="sxs-lookup"><span data-stu-id="d5832-114">Specifies that policy should be applicable at variable levels.</span></span>|  
|`ePolicyPortability`|<span data-ttu-id="d5832-115">指定策略应支持 .NET Framework 程序集的实现之间的可移植性。</span><span class="sxs-lookup"><span data-stu-id="d5832-115">Specifies that policy should support portability between implementations of a .NET Framework assembly.</span></span> <span data-ttu-id="d5832-116">请参阅 [\<supportPortability>](../../configure-apps/file-schema/runtime/supportportability-element.md) 配置文件元素。</span><span class="sxs-lookup"><span data-stu-id="d5832-116">See the [\<supportPortability>](../../configure-apps/file-schema/runtime/supportportability-element.md) configuration file element.</span></span>|  
|`ePolicyUnifiedToCLR`|<span data-ttu-id="d5832-117">指定应将策略统一到公共语言运行时的 (CLR) 。</span><span class="sxs-lookup"><span data-stu-id="d5832-117">Specifies that policy should be unified to that of the common language runtime (CLR).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d5832-118">备注</span><span class="sxs-lookup"><span data-stu-id="d5832-118">Remarks</span></span>  

 <span data-ttu-id="d5832-119">此枚举将传递给 [ICLRHostBindingPolicyManager](iclrhostbindingpolicymanager-interface.md) 接口的方法，以指定应用程序策略中的更改。</span><span class="sxs-lookup"><span data-stu-id="d5832-119">This enumeration is passed to methods of the [ICLRHostBindingPolicyManager](iclrhostbindingpolicymanager-interface.md) interface to specify changes in application policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5832-120">要求</span><span class="sxs-lookup"><span data-stu-id="d5832-120">Requirements</span></span>  

 <span data-ttu-id="d5832-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d5832-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5832-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d5832-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d5832-123">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d5832-123">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d5832-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5832-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5832-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5832-125">See also</span></span>

- [<span data-ttu-id="d5832-126">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="d5832-126">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="d5832-127">承载枚举</span><span class="sxs-lookup"><span data-stu-id="d5832-127">Hosting Enumerations</span></span>](hosting-enumerations.md)

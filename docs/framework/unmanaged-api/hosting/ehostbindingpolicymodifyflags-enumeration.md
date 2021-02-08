---
description: 了解详细信息： EHostBindingPolicyModifyFlags 枚举
title: EHostBindingPolicyModifyFlags 枚举
ms.date: 03/30/2017
api_name:
- EHostBindingPolicyModifyFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EHostBindingPolicyModifyFlags
helpviewer_keywords:
- EHostBindingPolicyModifyFlags enumeration [.NET Framework hosting]
ms.assetid: 0339af16-ee1d-48ec-837d-a79d9a9c89f8
topic_type:
- apiref
ms.openlocfilehash: be8a15cad49097d1ea2e206e01da2d5d5dcb165a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785479"
---
# <a name="ehostbindingpolicymodifyflags-enumeration"></a><span data-ttu-id="a24a1-103">EHostBindingPolicyModifyFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="a24a1-103">EHostBindingPolicyModifyFlags Enumeration</span></span>

<span data-ttu-id="a24a1-104">允许主机指定公共语言运行时 (CLR) 在将策略修改从源程序集应用到目标程序集时应执行的重定向类型。</span><span class="sxs-lookup"><span data-stu-id="a24a1-104">Allows the host to specify the type of redirection the common language runtime (CLR) should perform when applying policy modifications from a source assembly to a target assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a24a1-105">语法</span><span class="sxs-lookup"><span data-stu-id="a24a1-105">Syntax</span></span>  
  
```cpp  
typedef enum _hostBindingPolicyModifyFlags {  
    HOST_BINDING_POLICY_MODIFY_DEFAULT  = 0,  
    HOST_BINDING_POLICY_MODIFY_CHAIN    = 1,  
    HOST_BINDING_POLICY_MODIFY_REMOVE   = 2,  
    HOST_BINDING_POLICY_MODIFY_MAX      = 3  
} EHostBindingPolicyModifyFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="a24a1-106">成员</span><span class="sxs-lookup"><span data-stu-id="a24a1-106">Members</span></span>  
  
|<span data-ttu-id="a24a1-107">成员</span><span class="sxs-lookup"><span data-stu-id="a24a1-107">Member</span></span>|<span data-ttu-id="a24a1-108">说明</span><span class="sxs-lookup"><span data-stu-id="a24a1-108">Description</span></span>|  
|------------|-----------------|  
|`HOST_BINDING_POLICY_MODIFY_CHAIN`|<span data-ttu-id="a24a1-109">指定 CLR 将源程序集的策略值链接到目标程序集的策略值。</span><span class="sxs-lookup"><span data-stu-id="a24a1-109">Specifies that the CLR will chain policy values of the source assembly onto those of the target assembly.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_DEFAULT`|<span data-ttu-id="a24a1-110">指定 CLR 将执行默认操作。</span><span class="sxs-lookup"><span data-stu-id="a24a1-110">Specifies that the CLR will perform the default action.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_MAX`|<span data-ttu-id="a24a1-111">指定 CLR 将目标程序集的策略值设置为最大值。</span><span class="sxs-lookup"><span data-stu-id="a24a1-111">Specifies that the CLR will set the policy values of the target assembly to the maximum values.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_REMOVE`|<span data-ttu-id="a24a1-112">指定 CLR 将目标程序集的策略值替换为源程序集的策略值。</span><span class="sxs-lookup"><span data-stu-id="a24a1-112">Specifies that the CLR will replace policy values of the target assembly with those of the source assembly.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a24a1-113">备注</span><span class="sxs-lookup"><span data-stu-id="a24a1-113">Remarks</span></span>  

 <span data-ttu-id="a24a1-114">[ICLRHostBindingPolicyManager：： ModifyApplicationPolicy](iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)方法采用类型的参数 `EHostBindingPolicyModifyFlags` 。</span><span class="sxs-lookup"><span data-stu-id="a24a1-114">The [ICLRHostBindingPolicyManager::ModifyApplicationPolicy](iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md) method takes a parameter of type `EHostBindingPolicyModifyFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a24a1-115">要求</span><span class="sxs-lookup"><span data-stu-id="a24a1-115">Requirements</span></span>  

 <span data-ttu-id="a24a1-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a24a1-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a24a1-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a24a1-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a24a1-118">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a24a1-118">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a24a1-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a24a1-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a24a1-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="a24a1-120">See also</span></span>

- [<span data-ttu-id="a24a1-121">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="a24a1-121">ICLRHostBindingPolicyManager Interface</span></span>](iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="a24a1-122">承载枚举</span><span class="sxs-lookup"><span data-stu-id="a24a1-122">Hosting Enumerations</span></span>](hosting-enumerations.md)

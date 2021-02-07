---
description: 了解详细信息： METAHOST_CONFIG_FLAGS 枚举
title: METAHOST_CONFIG_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- METAHOST_CONFIG_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- METAHOST_CONFIG_FLAGS
helpviewer_keywords:
- METAHOST_CONFIG_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 6f1e389f-ed99-4d6a-a0ba-72d7d869a01d
topic_type:
- apiref
ms.openlocfilehash: 56d70f50d3b4c48b7fbf1aa3be6fc11cda904638
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679636"
---
# <a name="metahost_config_flags-enumeration"></a><span data-ttu-id="5f0a0-103">METAHOST_CONFIG_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="5f0a0-103">METAHOST_CONFIG_FLAGS Enumeration</span></span>

<span data-ttu-id="5f0a0-104">描述在 `pdwConfigFlags` [ICLRMetaHostPolicy：： GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md)方法的参数中返回的可能的标志，指示 `useLegacyV2RuntimeActivationPolicy` 配置文件的[ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)中的特性的状态和设置。</span><span class="sxs-lookup"><span data-stu-id="5f0a0-104">Describes the possible flags returned in the `pdwConfigFlags` parameter of the [ICLRMetaHostPolicy::GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md) method, indicating the presence and setting of the `useLegacyV2RuntimeActivationPolicy` attribute in the [\<startup> element](../../configure-apps/file-schema/startup/startup-element.md) of the configuration file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f0a0-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f0a0-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET  = 0x00,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE   = 0x01,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE  = 0x02,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK   = 0x03  
} METAHOST_CONFIG_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="5f0a0-106">成员</span><span class="sxs-lookup"><span data-stu-id="5f0a0-106">Members</span></span>  
  
|<span data-ttu-id="5f0a0-107">成员</span><span class="sxs-lookup"><span data-stu-id="5f0a0-107">Member</span></span>|<span data-ttu-id="5f0a0-108">说明</span><span class="sxs-lookup"><span data-stu-id="5f0a0-108">Description</span></span>|  
|------------|-----------------|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET`|<span data-ttu-id="5f0a0-109">`useLegacyV2RuntimeActivationPolicy` [ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)中不存在该特性。</span><span class="sxs-lookup"><span data-stu-id="5f0a0-109">The `useLegacyV2RuntimeActivationPolicy` attribute was not present in the [\<startup> Element](../../configure-apps/file-schema/startup/startup-element.md).</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE`|<span data-ttu-id="5f0a0-110">`useLegacyV2RuntimeActivationPolicy`特性存在并设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="5f0a0-110">The `useLegacyV2RuntimeActivationPolicy` attribute was present and set to `true`.</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE`|<span data-ttu-id="5f0a0-111">`useLegacyV2RuntimeActivationPolicy`特性存在并设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5f0a0-111">The `useLegacyV2RuntimeActivationPolicy` attribute was present and set to `false`.</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK`|<span data-ttu-id="5f0a0-112">将此掩码应用于在中返回的值，以 `pdwConfigFlags` 获取与相关的值 `useLegacyV2RuntimeActivationPolicy` 。</span><span class="sxs-lookup"><span data-stu-id="5f0a0-112">Apply this mask to the value returned in `pdwConfigFlags` to get the values relevant to `useLegacyV2RuntimeActivationPolicy`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5f0a0-113">备注</span><span class="sxs-lookup"><span data-stu-id="5f0a0-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f0a0-114">要求</span><span class="sxs-lookup"><span data-stu-id="5f0a0-114">Requirements</span></span>  

 <span data-ttu-id="5f0a0-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f0a0-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f0a0-116">**标头：** Metahost</span><span class="sxs-lookup"><span data-stu-id="5f0a0-116">**Header:** Metahost.h</span></span>  
  
 <span data-ttu-id="5f0a0-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f0a0-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5f0a0-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f0a0-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f0a0-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f0a0-119">See also</span></span>

- [<span data-ttu-id="5f0a0-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="5f0a0-120">Hosting Enumerations</span></span>](hosting-enumerations.md)
- [<span data-ttu-id="5f0a0-121">GetRequestedRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="5f0a0-121">GetRequestedRuntime Method</span></span>](iclrmetahostpolicy-getrequestedruntime-method.md)
- [<span data-ttu-id="5f0a0-122">\<startup> 元素</span><span class="sxs-lookup"><span data-stu-id="5f0a0-122">\<startup> Element</span></span>](../../configure-apps/file-schema/startup/startup-element.md)

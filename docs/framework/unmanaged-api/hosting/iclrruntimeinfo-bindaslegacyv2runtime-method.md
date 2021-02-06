---
description: 了解详细信息： ICLRRuntimeInfo：： BindAsLegacyV2Runtime 方法
title: ICLRRuntimeInfo::BindAsLegacyV2Runtime 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.BindAsLegacyV2Runtime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime
helpviewer_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime method [.NET Framework hosting]
- BindAsLegacyV2Runtime method [.NET Framework hosting]
ms.assetid: 65fd55ac-4a24-4479-9384-a2e8013bfb2b
topic_type:
- apiref
ms.openlocfilehash: 77b340cba18ea86546e1a8f4a17933f09289b1de
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637168"
---
# <a name="iclrruntimeinfobindaslegacyv2runtime-method"></a><span data-ttu-id="315fa-103">ICLRRuntimeInfo::BindAsLegacyV2Runtime 方法</span><span class="sxs-lookup"><span data-stu-id="315fa-103">ICLRRuntimeInfo::BindAsLegacyV2Runtime Method</span></span>

<span data-ttu-id="315fa-104">将所有旧公共语言运行时的当前运行时绑定 (CLR) 版本2激活策略决策。</span><span class="sxs-lookup"><span data-stu-id="315fa-104">Binds the current runtime for all legacy common language runtime (CLR) version 2 activation policy decisions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="315fa-105">语法</span><span class="sxs-lookup"><span data-stu-id="315fa-105">Syntax</span></span>  
  
```cpp  
HRESULT BindAsLegacyV2Runtime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="315fa-106">返回值</span><span class="sxs-lookup"><span data-stu-id="315fa-106">Return Value</span></span>  

 <span data-ttu-id="315fa-107">此方法返回以下特定 Hresult：</span><span class="sxs-lookup"><span data-stu-id="315fa-107">This method returns the following specific HRESULTs:</span></span>  
  
|<span data-ttu-id="315fa-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="315fa-108">HRESULT</span></span>|<span data-ttu-id="315fa-109">说明</span><span class="sxs-lookup"><span data-stu-id="315fa-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="315fa-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="315fa-110">S_OK</span></span>|<span data-ttu-id="315fa-111">绑定成功，或已将此运行时绑定为旧版 CLR 版本2激活策略运行时。</span><span class="sxs-lookup"><span data-stu-id="315fa-111">Either binding succeeded, or this runtime was already bound as the legacy CLR version 2 activation policy runtime.</span></span>|  
|<span data-ttu-id="315fa-112">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="315fa-112">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="315fa-113">已将其他运行时绑定到旧版 CLR 版本2激活策略。</span><span class="sxs-lookup"><span data-stu-id="315fa-113">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="315fa-114">备注</span><span class="sxs-lookup"><span data-stu-id="315fa-114">Remarks</span></span>  

 <span data-ttu-id="315fa-115">如果当前运行时已绑定到所有旧版 CLR 版本2激活策略决策 (例如，通过使用 `useLegacyV2RuntimeActivationPolicy` 配置文件) 中[ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)上的属性，则此方法不会返回错误结果，而是 S_OK 结果，就像在方法成功绑定了旧激活策略时一样。</span><span class="sxs-lookup"><span data-stu-id="315fa-115">If the current runtime is already bound for all legacy CLR version 2 activation policy decisions (for example, by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> element](../../configure-apps/file-schema/startup/startup-element.md) in the configuration file), this method does not return an error result; instead, the result is S_OK, just as it would be if the method had successfully bound legacy activation policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="315fa-116">要求</span><span class="sxs-lookup"><span data-stu-id="315fa-116">Requirements</span></span>  

 <span data-ttu-id="315fa-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="315fa-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="315fa-118">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="315fa-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="315fa-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="315fa-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="315fa-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="315fa-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="315fa-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="315fa-121">See also</span></span>

- [<span data-ttu-id="315fa-122">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="315fa-122">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="315fa-123">承载接口</span><span class="sxs-lookup"><span data-stu-id="315fa-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="315fa-124">承载</span><span class="sxs-lookup"><span data-stu-id="315fa-124">Hosting</span></span>](index.md)
- [<span data-ttu-id="315fa-125">\<startup> 元素</span><span class="sxs-lookup"><span data-stu-id="315fa-125">\<startup> Element</span></span>](../../configure-apps/file-schema/startup/startup-element.md)

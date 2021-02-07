---
description: 了解详细信息： IGCHost2 接口
title: IGCHost2 接口
ms.date: 03/30/2017
api_name:
- IGCHost2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost2
helpviewer_keywords:
- IGCHost2 interface [.NET Framework hosting]
ms.assetid: e5323fa4-18ac-424d-859d-a65a550d08d9
topic_type:
- apiref
ms.openlocfilehash: e32a4894fcff3600c9385f0f559443e23b2bc307
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709316"
---
# <a name="igchost2-interface"></a><span data-ttu-id="ed7d5-103">IGCHost2 接口</span><span class="sxs-lookup"><span data-stu-id="ed7d5-103">IGCHost2 Interface</span></span>

<span data-ttu-id="ed7d5-104">提供一些方法，用于获取有关垃圾回收系统的信息并控制垃圾回收的某些方面。</span><span class="sxs-lookup"><span data-stu-id="ed7d5-104">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed7d5-105">对于新开发，建议改为使用 [ICLRGCManager2](iclrgcmanager2-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="ed7d5-105">For new development, we recommend that you use the [ICLRGCManager2](iclrgcmanager2-interface.md) interface instead.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ed7d5-106">方法</span><span class="sxs-lookup"><span data-stu-id="ed7d5-106">Methods</span></span>  
  
|<span data-ttu-id="ed7d5-107">方法</span><span class="sxs-lookup"><span data-stu-id="ed7d5-107">Method</span></span>|<span data-ttu-id="ed7d5-108">说明</span><span class="sxs-lookup"><span data-stu-id="ed7d5-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ed7d5-109">SetGCStartupLimitsEx 方法</span><span class="sxs-lookup"><span data-stu-id="ed7d5-109">SetGCStartupLimitsEx Method</span></span>](igchost2-setgcstartuplimitsex-method.md)|<span data-ttu-id="ed7d5-110">设置第0代的段大小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="ed7d5-110">Sets the segment size and the maximum size for generation 0.</span></span> <span data-ttu-id="ed7d5-111">启用0代和大于的段大小 `DWORD` 。</span><span class="sxs-lookup"><span data-stu-id="ed7d5-111">Enables generation 0 and segment sizes larger than `DWORD`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ed7d5-112">要求</span><span class="sxs-lookup"><span data-stu-id="ed7d5-112">Requirements</span></span>  

 <span data-ttu-id="ed7d5-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed7d5-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed7d5-114">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="ed7d5-114">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="ed7d5-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ed7d5-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ed7d5-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed7d5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed7d5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed7d5-117">See also</span></span>

- [<span data-ttu-id="ed7d5-118">承载接口</span><span class="sxs-lookup"><span data-stu-id="ed7d5-118">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="ed7d5-119">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="ed7d5-119">CLR Hosting Interfaces</span></span>](clr-hosting-interfaces.md)
- [<span data-ttu-id="ed7d5-120">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="ed7d5-120">CorRuntimeHost Coclass</span></span>](corruntimehost-coclass.md)

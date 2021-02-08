---
description: 了解详细信息： ICLRHostBindingPolicyManager 接口
title: ICLRHostBindingPolicyManager 接口
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager
helpviewer_keywords:
- ICLRHostBindingPolicyManager interface [.NET Framework hosting]
ms.assetid: f9da168b-366b-4b2b-bdb9-330b6bad5a6b
topic_type:
- apiref
ms.openlocfilehash: 07a18d622ff8d8483fe6dcb0242cb5f1ee284b14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789939"
---
# <a name="iclrhostbindingpolicymanager-interface"></a><span data-ttu-id="f717e-103">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="f717e-103">ICLRHostBindingPolicyManager Interface</span></span>

<span data-ttu-id="f717e-104">为宿主提供方法，用于评估当前的绑定策略并传达指定程序集的策略更改。</span><span class="sxs-lookup"><span data-stu-id="f717e-104">Provides methods for the host to evaluate current binding policy and communicate policy changes for a specified assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f717e-105">方法</span><span class="sxs-lookup"><span data-stu-id="f717e-105">Methods</span></span>  
  
|<span data-ttu-id="f717e-106">方法</span><span class="sxs-lookup"><span data-stu-id="f717e-106">Method</span></span>|<span data-ttu-id="f717e-107">说明</span><span class="sxs-lookup"><span data-stu-id="f717e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f717e-108">EvaluatePolicy 方法</span><span class="sxs-lookup"><span data-stu-id="f717e-108">EvaluatePolicy Method</span></span>](iclrhostbindingpolicymanager-evaluatepolicy-method.md)|<span data-ttu-id="f717e-109">代表主机计算绑定策略。</span><span class="sxs-lookup"><span data-stu-id="f717e-109">Evaluates binding policy on behalf of the host.</span></span>|  
|[<span data-ttu-id="f717e-110">ModifyApplicationPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="f717e-110">ModifyApplicationPolicy Method</span></span>](iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)|<span data-ttu-id="f717e-111">修改指定程序集的绑定策略，并创建该策略的新版本。</span><span class="sxs-lookup"><span data-stu-id="f717e-111">Modifies the binding policy for the specified assembly, and creates a new version of the policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f717e-112">要求</span><span class="sxs-lookup"><span data-stu-id="f717e-112">Requirements</span></span>  

 <span data-ttu-id="f717e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f717e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f717e-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f717e-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f717e-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f717e-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f717e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f717e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f717e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="f717e-117">See also</span></span>

- [<span data-ttu-id="f717e-118">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="f717e-118">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="f717e-119">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="f717e-119">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
- [<span data-ttu-id="f717e-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="f717e-120">Hosting Interfaces</span></span>](hosting-interfaces.md)

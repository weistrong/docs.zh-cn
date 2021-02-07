---
description: 了解详细信息： ICLRProbingAssemblyEnum 接口
title: ICLRProbingAssemblyEnum 接口
ms.date: 03/30/2017
api_name:
- ICLRProbingAssemblyEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRProbingAssemblyEnum
helpviewer_keywords:
- ICLRProbingAssemblyEnum interface [.NET Framework hosting]
ms.assetid: e7d3ccab-b0f0-4872-8935-0ed72920171b
topic_type:
- apiref
ms.openlocfilehash: 1fd11e237f02bab85ec2b41df49d7d8a2f27e1e1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716492"
---
# <a name="iclrprobingassemblyenum-interface"></a><span data-ttu-id="74981-103">ICLRProbingAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="74981-103">ICLRProbingAssemblyEnum Interface</span></span>

<span data-ttu-id="74981-104">提供一些方法，这些方法使宿主可以通过使用公共语言运行时 (CLR) 内部的程序集的标识信息来获取程序集的探测标识，无需创建或了解该标识。</span><span class="sxs-lookup"><span data-stu-id="74981-104">Provides methods that enable the host to get the probing identities of an assembly by using the assembly's identity information that is internal to the common language runtime (CLR), without needing to create or understand that identity.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="74981-105">方法</span><span class="sxs-lookup"><span data-stu-id="74981-105">Methods</span></span>  
  
|<span data-ttu-id="74981-106">方法</span><span class="sxs-lookup"><span data-stu-id="74981-106">Method</span></span>|<span data-ttu-id="74981-107">说明</span><span class="sxs-lookup"><span data-stu-id="74981-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="74981-108">Get 方法</span><span class="sxs-lookup"><span data-stu-id="74981-108">Get Method</span></span>](iclrprobingassemblyenum-get-method.md)|<span data-ttu-id="74981-109">获取指定索引处的程序集标识。</span><span class="sxs-lookup"><span data-stu-id="74981-109">Gets the assembly identity at the specified index.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="74981-110">备注</span><span class="sxs-lookup"><span data-stu-id="74981-110">Remarks</span></span>  

 <span data-ttu-id="74981-111">方法（如 [ICLRAssemblyIdentityManager：： GetProbingAssembliesFromReference](iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md) ）返回 `ICLRProbingAssemblyEnum` 实例。</span><span class="sxs-lookup"><span data-stu-id="74981-111">Methods such as [ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference](iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md) return an `ICLRProbingAssemblyEnum` instance.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74981-112">要求</span><span class="sxs-lookup"><span data-stu-id="74981-112">Requirements</span></span>  

 <span data-ttu-id="74981-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="74981-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74981-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="74981-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="74981-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="74981-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="74981-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="74981-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74981-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="74981-117">See also</span></span>

- [<span data-ttu-id="74981-118">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="74981-118">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="74981-119">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="74981-119">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="74981-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="74981-120">Hosting Interfaces</span></span>](hosting-interfaces.md)

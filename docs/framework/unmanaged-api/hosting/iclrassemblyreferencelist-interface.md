---
description: 了解详细信息： ICLRAssemblyReferenceList 接口
title: ICLRAssemblyReferenceList 接口
ms.date: 03/30/2017
api_name:
- ICLRAssemblyReferenceList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyReferenceList
helpviewer_keywords:
- ICLRAssemblyReferenceList interface [.NET Framework hosting]
ms.assetid: 5f890fdf-d22a-429e-a35f-135273d1a636
topic_type:
- apiref
ms.openlocfilehash: f5ef4efd343ebc18c443482f4697a3d299c5aac1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716778"
---
# <a name="iclrassemblyreferencelist-interface"></a><span data-ttu-id="3a9bc-103">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="3a9bc-103">ICLRAssemblyReferenceList Interface</span></span>

<span data-ttu-id="3a9bc-104">管理由公共语言运行时 (CLR) 而不是由宿主加载的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="3a9bc-104">Manages a list of assemblies that are loaded by the common language runtime (CLR) and not by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3a9bc-105">方法</span><span class="sxs-lookup"><span data-stu-id="3a9bc-105">Methods</span></span>  
  
|<span data-ttu-id="3a9bc-106">方法</span><span class="sxs-lookup"><span data-stu-id="3a9bc-106">Method</span></span>|<span data-ttu-id="3a9bc-107">说明</span><span class="sxs-lookup"><span data-stu-id="3a9bc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3a9bc-108">IsAssemblyReferenceInList 方法</span><span class="sxs-lookup"><span data-stu-id="3a9bc-108">IsAssemblyReferenceInList Method</span></span>](iclrassemblyreferencelist-isassemblyreferenceinlist-method.md)|<span data-ttu-id="3a9bc-109">获取一个值，该值指示提供的指针是否引用列表中的程序集。</span><span class="sxs-lookup"><span data-stu-id="3a9bc-109">Gets a value that indicates whether the supplied pointer references an assembly in the list.</span></span>|  
|[<span data-ttu-id="3a9bc-110">IsStringAssemblyReferenceInList 方法</span><span class="sxs-lookup"><span data-stu-id="3a9bc-110">IsStringAssemblyReferenceInList Method</span></span>](iclrassemblyreferencelist-isstringassemblyreferenceinlist-method.md)|<span data-ttu-id="3a9bc-111">获取一个值，该值指示所提供的名称是否与列表中的程序集的名称相匹配。</span><span class="sxs-lookup"><span data-stu-id="3a9bc-111">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a9bc-112">备注</span><span class="sxs-lookup"><span data-stu-id="3a9bc-112">Remarks</span></span>  

 <span data-ttu-id="3a9bc-113">调用 [ICLRAssemblyIdentityManager：： GetCLRAssemblyReferenceList](iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md) 方法以获取指向实例的指针 `ICLRAssemblyReferenceList` 。</span><span class="sxs-lookup"><span data-stu-id="3a9bc-113">Call the [ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList](iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md) method to get a pointer to an instance of `ICLRAssemblyReferenceList`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a9bc-114">要求</span><span class="sxs-lookup"><span data-stu-id="3a9bc-114">Requirements</span></span>  

 <span data-ttu-id="3a9bc-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3a9bc-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a9bc-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3a9bc-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3a9bc-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3a9bc-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3a9bc-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a9bc-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a9bc-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a9bc-119">See also</span></span>

- [<span data-ttu-id="3a9bc-120">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="3a9bc-120">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="3a9bc-121">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="3a9bc-121">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
- [<span data-ttu-id="3a9bc-122">承载接口</span><span class="sxs-lookup"><span data-stu-id="3a9bc-122">Hosting Interfaces</span></span>](hosting-interfaces.md)

---
description: 了解详细信息： ICLRAssemblyIdentityManager 接口
title: ICLRAssemblyIdentityManager 接口
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager
helpviewer_keywords:
- ICLRAssemblyIdentityManager interface [.NET Framework hosting]
ms.assetid: 6a81c6fe-cc22-4062-ae27-d6eeee03a7b9
topic_type:
- apiref
ms.openlocfilehash: d6238ec51a8cc1bb61eaa96e5297656c447df785
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790044"
---
# <a name="iclrassemblyidentitymanager-interface"></a><span data-ttu-id="6709a-103">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="6709a-103">ICLRAssemblyIdentityManager Interface</span></span>

<span data-ttu-id="6709a-104">提供一些方法，这些方法支持宿主与公共语言运行时之间的通信 (CLR) 有关程序集的信息。</span><span class="sxs-lookup"><span data-stu-id="6709a-104">Provides methods that support communication between the host and the common language runtime (CLR) about assemblies.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6709a-105">方法</span><span class="sxs-lookup"><span data-stu-id="6709a-105">Methods</span></span>  
  
|<span data-ttu-id="6709a-106">方法</span><span class="sxs-lookup"><span data-stu-id="6709a-106">Method</span></span>|<span data-ttu-id="6709a-107">说明</span><span class="sxs-lookup"><span data-stu-id="6709a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6709a-108">GetBindingIdentityFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-108">GetBindingIdentityFromFile Method</span></span>](iclrassemblyidentitymanager-getbindingidentityfromfile-method.md)|<span data-ttu-id="6709a-109">获取指定文件路径处的程序集的程序集标识绑定数据。</span><span class="sxs-lookup"><span data-stu-id="6709a-109">Gets the assembly identity binding data for the assembly at the specified file path.</span></span>|  
|[<span data-ttu-id="6709a-110">GetBindingIdentityFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-110">GetBindingIdentityFromStream Method</span></span>](iclrassemblyidentitymanager-getbindingidentityfromstream-method.md)|<span data-ttu-id="6709a-111">获取指定流中的程序集的规范程序集标识数据。</span><span class="sxs-lookup"><span data-stu-id="6709a-111">Gets the canonical assembly identity data for the assembly in the specified stream.</span></span>|  
|[<span data-ttu-id="6709a-112">GetCLRAssemblyReferenceList 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-112">GetCLRAssemblyReferenceList Method</span></span>](iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md)|<span data-ttu-id="6709a-113">从提供的部分程序集标识列表中获取 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="6709a-113">Gets an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) instance from the supplied list of partial assembly identities.</span></span>|  
|[<span data-ttu-id="6709a-114">GetProbingAssembliesFromReference 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-114">GetProbingAssembliesFromReference Method</span></span>](iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md)|<span data-ttu-id="6709a-115">获取具有指定标识的程序集所引用的程序集标识的 [ICLRProbingAssemblyEnum](iclrprobingassemblyenum-interface.md) 枚举器。</span><span class="sxs-lookup"><span data-stu-id="6709a-115">Gets an [ICLRProbingAssemblyEnum](iclrprobingassemblyenum-interface.md) enumerator for the assembly identities referenced by the assembly with the specified identity.</span></span>|  
|[<span data-ttu-id="6709a-116">GetReferencedAssembliesFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-116">GetReferencedAssembliesFromFile Method</span></span>](iclrassemblyidentitymanager-getreferencedassembliesfromfile-method.md)|<span data-ttu-id="6709a-117">获取一个 [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) 实例，该实例包含程序集在指定文件路径处引用的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="6709a-117">Gets an [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) instance that contains a list of assemblies referenced by the assembly at the specified file path.</span></span>|  
|[<span data-ttu-id="6709a-118">GetReferencedAssembliesFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-118">GetReferencedAssembliesFromStream Method</span></span>](iclrassemblyidentitymanager-getreferencedassembliesfromstream-method.md)|<span data-ttu-id="6709a-119">获取一个指向 `ICLRReferenceAssemblyEnum` 对象的指针，该对象包含指定流中的程序集所引用的程序集的程序集标识数据。</span><span class="sxs-lookup"><span data-stu-id="6709a-119">Gets a pointer to an `ICLRReferenceAssemblyEnum` object that contains assembly identity data for the assemblies referenced by the assembly in the specified stream.</span></span>|  
|[<span data-ttu-id="6709a-120">IsStronglyNamed 方法</span><span class="sxs-lookup"><span data-stu-id="6709a-120">IsStronglyNamed Method</span></span>](iclrassemblyidentitymanager-isstronglynamed-method.md)|<span data-ttu-id="6709a-121">获取一个值，该值指示指定的程序集是否具有强名称。</span><span class="sxs-lookup"><span data-stu-id="6709a-121">Gets a value that indicates whether the specified assembly is strongly named.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6709a-122">备注</span><span class="sxs-lookup"><span data-stu-id="6709a-122">Remarks</span></span>  

 <span data-ttu-id="6709a-123">用于 `ICLRAssemblyIdentityManager` 获取的实例 `ICLRAssemblyReferenceList` 并枚举程序集标识。</span><span class="sxs-lookup"><span data-stu-id="6709a-123">Use `ICLRAssemblyIdentityManager` to get instances of `ICLRAssemblyReferenceList` and to enumerate assembly identities.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6709a-124">要求</span><span class="sxs-lookup"><span data-stu-id="6709a-124">Requirements</span></span>  

 <span data-ttu-id="6709a-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6709a-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6709a-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6709a-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6709a-127">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6709a-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6709a-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6709a-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6709a-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="6709a-129">See also</span></span>

- [<span data-ttu-id="6709a-130">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="6709a-130">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="6709a-131">ICLRProbingAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="6709a-131">ICLRProbingAssemblyEnum Interface</span></span>](iclrprobingassemblyenum-interface.md)
- [<span data-ttu-id="6709a-132">承载接口</span><span class="sxs-lookup"><span data-stu-id="6709a-132">Hosting Interfaces</span></span>](hosting-interfaces.md)

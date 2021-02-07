---
description: 了解详细信息： ModuleBindInfo 结构
title: ModuleBindInfo 结构
ms.date: 03/30/2017
api_name:
- ModuleBindInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ModuleBindInfo
helpviewer_keywords:
- ModuleBindInfo structure [.NET Framework hosting]
ms.assetid: 632d4adc-dbc9-4ce8-9397-abc3285c1c69
topic_type:
- apiref
ms.openlocfilehash: 0969c0ecc459414336800e8e7da5817ac0c1a8ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679597"
---
# <a name="modulebindinfo-structure"></a><span data-ttu-id="20394-103">ModuleBindInfo 结构</span><span class="sxs-lookup"><span data-stu-id="20394-103">ModuleBindInfo Structure</span></span>

<span data-ttu-id="20394-104">提供有关被引用模块和包含它的程序集的详细信息。</span><span class="sxs-lookup"><span data-stu-id="20394-104">Provides detailed information about the referenced module and the assembly that contains it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20394-105">语法</span><span class="sxs-lookup"><span data-stu-id="20394-105">Syntax</span></span>  
  
```cpp  
typedef struct _ModuleBindInfo {  
    DWORD    dwAppDomainId;  
    LPCWSTR  lpAssemblyIdentity;  
    LPCWSTR  lpModuleName  
} ModuleBindInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="20394-106">成员</span><span class="sxs-lookup"><span data-stu-id="20394-106">Members</span></span>  
  
|<span data-ttu-id="20394-107">成员</span><span class="sxs-lookup"><span data-stu-id="20394-107">Member</span></span>|<span data-ttu-id="20394-108">说明</span><span class="sxs-lookup"><span data-stu-id="20394-108">Description</span></span>|  
|------------|-----------------|  
|`dwAppDomainId`|<span data-ttu-id="20394-109">的唯一标识符，该标识符由要从中 `IStream` 加载所引用的模块的 [IHostAssemblyStore：:P rovidemodule](ihostassemblystore-providemodule-method.md) 方法的调用返回。</span><span class="sxs-lookup"><span data-stu-id="20394-109">A unique identifier for the `IStream` that is returned by a call to the [IHostAssemblyStore::ProvideModule](ihostassemblystore-providemodule-method.md) method from which the referenced module is to be loaded.</span></span>|  
|`lpAssemblyIdentity`|<span data-ttu-id="20394-110">包含所引用的模块的程序集的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="20394-110">A unique identifier for the assembly that contains the referenced module.</span></span>|  
|`lpModuleName`|<span data-ttu-id="20394-111">引用的模块的名称。</span><span class="sxs-lookup"><span data-stu-id="20394-111">The name of the referenced module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="20394-112">备注</span><span class="sxs-lookup"><span data-stu-id="20394-112">Remarks</span></span>  

 <span data-ttu-id="20394-113">`ModuleBindInfo` 作为参数传递给 `IHostAssemblyStore::ProvideModule` 。</span><span class="sxs-lookup"><span data-stu-id="20394-113">`ModuleBindInfo` is passed as a parameter to `IHostAssemblyStore::ProvideModule`.</span></span> <span data-ttu-id="20394-114">宿主 `dwAppDomainId` (CLR) 向公共语言运行时提供唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="20394-114">The host supplies the unique identifier `dwAppDomainId` to the common language runtime (CLR).</span></span> <span data-ttu-id="20394-115">调用 [IHostAssemblyStore：:P rovideassembly](ihostassemblystore-provideassembly-method.md) 方法返回后，运行时将使用标识符来确定是否已映射的内容 `IStream` 。</span><span class="sxs-lookup"><span data-stu-id="20394-115">After a call to the [IHostAssemblyStore::ProvideAssembly](ihostassemblystore-provideassembly-method.md) method returns, the runtime uses the identifier to determine whether the contents of the `IStream` have been mapped.</span></span> <span data-ttu-id="20394-116">如果是这样，则运行时加载现有副本，而不是重新映射流。</span><span class="sxs-lookup"><span data-stu-id="20394-116">If so, the runtime loads the existing copy rather than remapping the stream.</span></span> <span data-ttu-id="20394-117">运行时还会将此标识符用作从对方法的调用返回的流的查找密钥 `IHostAssemblyStore::ProvideAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="20394-117">The runtime also uses this identifier as a lookup key for streams that are returned from calls to the `IHostAssemblyStore::ProvideAssembly` method.</span></span> <span data-ttu-id="20394-118">因此，对于模块请求和程序集请求，标识符必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="20394-118">Therefore, the identifier must be unique for module requests as well as for assembly requests.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20394-119">要求</span><span class="sxs-lookup"><span data-stu-id="20394-119">Requirements</span></span>  

 <span data-ttu-id="20394-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20394-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20394-121">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="20394-121">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="20394-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="20394-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="20394-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20394-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20394-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="20394-124">See also</span></span>

- [<span data-ttu-id="20394-125">承载结构</span><span class="sxs-lookup"><span data-stu-id="20394-125">Hosting Structures</span></span>](hosting-structures.md)
- [<span data-ttu-id="20394-126">AssemblyBindInfo 结构</span><span class="sxs-lookup"><span data-stu-id="20394-126">AssemblyBindInfo Structure</span></span>](assemblybindinfo-structure.md)
- [<span data-ttu-id="20394-127">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="20394-127">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="20394-128">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="20394-128">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="20394-129">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="20394-129">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)

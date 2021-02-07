---
description: 了解详细信息： IHostAssemblyManager 接口
title: IHostAssemblyManager 接口
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager
helpviewer_keywords:
- IHostAssemblyManager interface [.NET Framework hosting]
ms.assetid: dfec05bb-3cd7-4bd5-b396-a4f097c3a636
topic_type:
- apiref
ms.openlocfilehash: 649771f79e65039adfa8c0ade9f167b1679bb917
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708991"
---
# <a name="ihostassemblymanager-interface"></a><span data-ttu-id="c654a-103">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="c654a-103">IHostAssemblyManager Interface</span></span>

<span data-ttu-id="c654a-104">提供一些方法，这些方法允许主机指定应由公共语言运行时 (CLR) 或主机加载的程序集集。</span><span class="sxs-lookup"><span data-stu-id="c654a-104">Provides methods that allow a host to specify sets of assemblies that should be loaded by the common language runtime (CLR) or by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c654a-105">方法</span><span class="sxs-lookup"><span data-stu-id="c654a-105">Methods</span></span>  
  
|<span data-ttu-id="c654a-106">方法</span><span class="sxs-lookup"><span data-stu-id="c654a-106">Method</span></span>|<span data-ttu-id="c654a-107">说明</span><span class="sxs-lookup"><span data-stu-id="c654a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c654a-108">GetAssemblyStore 方法</span><span class="sxs-lookup"><span data-stu-id="c654a-108">GetAssemblyStore Method</span></span>](ihostassemblymanager-getassemblystore-method.md)|<span data-ttu-id="c654a-109">获取一个接口指针，该指针指向表示宿主加载的程序集列表的 [IHostAssemblyStore](ihostassemblystore-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="c654a-109">Gets an interface pointer to an [IHostAssemblyStore](ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>|  
|[<span data-ttu-id="c654a-110">GetNonHostStoreAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="c654a-110">GetNonHostStoreAssemblies Method</span></span>](ihostassemblymanager-getnonhoststoreassemblies-method.md)|<span data-ttu-id="c654a-111">获取一个指向 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 的接口指针，该指针表示宿主预期 CLR 加载的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="c654a-111">Gets an interface pointer to an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) that represents the list of assemblies that the host expects the CLR to load.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c654a-112">备注</span><span class="sxs-lookup"><span data-stu-id="c654a-112">Remarks</span></span>  

 <span data-ttu-id="c654a-113">宿主无需实现 `IHostAssemblyManager` 或 `IHostAssemblyStore` 。</span><span class="sxs-lookup"><span data-stu-id="c654a-113">The host is not required to implement `IHostAssemblyManager` or `IHostAssemblyStore`.</span></span> <span data-ttu-id="c654a-114">如果主机实现了 `IHostAssemblyManager` ，则它还必须实现 `IHostAssemblyStore` 。</span><span class="sxs-lookup"><span data-stu-id="c654a-114">If the host does implement `IHostAssemblyManager`, it must also implement `IHostAssemblyStore`.</span></span>  
  
 <span data-ttu-id="c654a-115">运行时 `IHostAssemblyManager` 通过在使用 IID_IHostAssemblyManager 的初始化时调用 [IHostControl：： GetHostManager](ihostcontrol-gethostmanager-method.md) 来查询 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="c654a-115">The runtime queries for an `IHostAssemblyManager` by calling [IHostControl::GetHostManager](ihostcontrol-gethostmanager-method.md) upon initialization with an `IID` of IID_IHostAssemblyManager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c654a-116">要求</span><span class="sxs-lookup"><span data-stu-id="c654a-116">Requirements</span></span>  

 <span data-ttu-id="c654a-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c654a-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c654a-118">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c654a-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c654a-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c654a-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c654a-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c654a-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c654a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="c654a-121">See also</span></span>

- [<span data-ttu-id="c654a-122">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="c654a-122">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="c654a-123">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="c654a-123">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
- [<span data-ttu-id="c654a-124">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="c654a-124">IHostControl Interface</span></span>](ihostcontrol-interface.md)
- [<span data-ttu-id="c654a-125">承载接口</span><span class="sxs-lookup"><span data-stu-id="c654a-125">Hosting Interfaces</span></span>](hosting-interfaces.md)

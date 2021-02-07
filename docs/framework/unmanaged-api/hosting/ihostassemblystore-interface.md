---
description: 了解详细信息： IHostAssemblyStore 接口
title: IHostAssemblyStore 接口
ms.date: 03/30/2017
api_name:
- IHostAssemblyStore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyStore
helpviewer_keywords:
- IHostAssemblyStore interface [.NET Framework hosting]
ms.assetid: cccb650f-abe0-41e2-9fd1-b383788eb1f6
topic_type:
- apiref
ms.openlocfilehash: a05fee7916911687143d5953e26187162a2fa544
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709010"
---
# <a name="ihostassemblystore-interface"></a><span data-ttu-id="941b4-103">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="941b4-103">IHostAssemblyStore Interface</span></span>

<span data-ttu-id="941b4-104">提供允许主机独立于公共语言运行时加载程序集和模块 (CLR) 的方法。</span><span class="sxs-lookup"><span data-stu-id="941b4-104">Provides methods that allow a host to load assemblies and modules independently of the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="941b4-105">方法</span><span class="sxs-lookup"><span data-stu-id="941b4-105">Methods</span></span>  
  
|<span data-ttu-id="941b4-106">方法</span><span class="sxs-lookup"><span data-stu-id="941b4-106">Method</span></span>|<span data-ttu-id="941b4-107">说明</span><span class="sxs-lookup"><span data-stu-id="941b4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="941b4-108">ProvideAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="941b4-108">ProvideAssembly Method</span></span>](ihostassemblystore-provideassembly-method.md)|<span data-ttu-id="941b4-109">获取对[IHostAssemblyManager：： GetNonHostStoreAssemblies](ihostassemblymanager-getnonhoststoreassemblies-method.md)调用返回的[ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md)未引用的程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="941b4-109">Gets a reference to an assembly that is not referenced by the [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) returned from a call to [IHostAssemblyManager::GetNonHostStoreAssemblies](ihostassemblymanager-getnonhoststoreassemblies-method.md).</span></span>|  
|[<span data-ttu-id="941b4-110">ProvideModule 方法</span><span class="sxs-lookup"><span data-stu-id="941b4-110">ProvideModule Method</span></span>](ihostassemblystore-providemodule-method.md)|<span data-ttu-id="941b4-111">解析程序集内的模块或未嵌入) 资源文件的链接 (。</span><span class="sxs-lookup"><span data-stu-id="941b4-111">Resolves a module within an assembly or a linked (not embedded) resource file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="941b4-112">备注</span><span class="sxs-lookup"><span data-stu-id="941b4-112">Remarks</span></span>  

 <span data-ttu-id="941b4-113">`IHostAssemblyStore` 提供一种方法，使主机可以根据程序集标识有效地加载程序集。</span><span class="sxs-lookup"><span data-stu-id="941b4-113">`IHostAssemblyStore` provides a way for a host to load assemblies efficiently based on assembly identity.</span></span> <span data-ttu-id="941b4-114">宿主通过返回直接指向字节的实例来加载程序集 `IStream` 。</span><span class="sxs-lookup"><span data-stu-id="941b4-114">The host loads assemblies by returning `IStream` instances that point directly at the bytes.</span></span>  
  
 <span data-ttu-id="941b4-115">CLR `IHostAssemblyStore` 通过在初始化时调用来确定宿主是否已实现 `IHostAssemblyManager::GetNonHostAssemblyStores` 。</span><span class="sxs-lookup"><span data-stu-id="941b4-115">The CLR determines whether a host has implemented `IHostAssemblyStore` by calling `IHostAssemblyManager::GetNonHostAssemblyStores` upon initialization.</span></span> <span data-ttu-id="941b4-116">例如，这允许主机控制与用户程序集的绑定，但要依赖于运行时绑定到 .NET Framework 程序集。</span><span class="sxs-lookup"><span data-stu-id="941b4-116">This allows the host, for example, to control binding to user assemblies, but to rely on the runtime to bind to .NET Framework assemblies.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="941b4-117">在提供的实现中 `IHostAssemblyStore` ，主机指定其意图以解析从返回的未引用的所有程序集 `ICLRAssemblyReferenceList` `IHostAssemblyManager::GetNonHostStoreAssemblies` 。</span><span class="sxs-lookup"><span data-stu-id="941b4-117">In providing an implementation of `IHostAssemblyStore`, the host specifies its intent to resolve all assemblies that are not referenced by the `ICLRAssemblyReferenceList` returned from `IHostAssemblyManager::GetNonHostStoreAssemblies`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="941b4-118">.NET Framework 版本2.0 不向宿主提供一种方法来加载程序集的本机映像，如 [本机映像生成器 ( # A0) ](../../tools/ngen-exe-native-image-generator.md) 实用工具所提供。</span><span class="sxs-lookup"><span data-stu-id="941b4-118">The .NET Framework version 2.0 does not provide a way for the host to load the native image of an assembly, as provided by the [Native Image Generator (Ngen.exe)](../../tools/ngen-exe-native-image-generator.md) utility.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="941b4-119">要求</span><span class="sxs-lookup"><span data-stu-id="941b4-119">Requirements</span></span>  

 <span data-ttu-id="941b4-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="941b4-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="941b4-121">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="941b4-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="941b4-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="941b4-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="941b4-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="941b4-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="941b4-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="941b4-124">See also</span></span>

- [<span data-ttu-id="941b4-125">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="941b4-125">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="941b4-126">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="941b4-126">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
- [<span data-ttu-id="941b4-127">承载接口</span><span class="sxs-lookup"><span data-stu-id="941b4-127">Hosting Interfaces</span></span>](hosting-interfaces.md)

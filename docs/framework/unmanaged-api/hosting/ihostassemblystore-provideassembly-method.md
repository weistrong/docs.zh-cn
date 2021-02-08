---
description: 了解详细信息： IHostAssemblyStore：:P rovideAssembly 方法
title: IHostAssemblyStore::ProvideAssembly 方法
ms.date: 03/30/2017
api_name:
- IHostAssemblyStore.ProvideAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyStore::ProvideAssembly
helpviewer_keywords:
- ProvideAssembly method [.NET Framework hosting]
- IHostAssemblyStore::ProvideAssembly method [.NET Framework hosting]
ms.assetid: 625c3dd5-a3f0-442c-adde-310dadbb5054
topic_type:
- apiref
ms.openlocfilehash: f8917cb28dd3898343a7b6ee08bd54096df8cfa7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789497"
---
# <a name="ihostassemblystoreprovideassembly-method"></a><span data-ttu-id="718d3-103">IHostAssemblyStore::ProvideAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="718d3-103">IHostAssemblyStore::ProvideAssembly Method</span></span>

<span data-ttu-id="718d3-104">获取对程序集的引用，该程序集未由从[IHostAssemblyManager：： GetNonHostStoreAssemblies](ihostassemblymanager-getnonhoststoreassemblies-method.md)返回的[ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md)引用。</span><span class="sxs-lookup"><span data-stu-id="718d3-104">Gets a reference to an assembly that is not referenced by the [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) that is returned from [IHostAssemblyManager::GetNonHostStoreAssemblies](ihostassemblymanager-getnonhoststoreassemblies-method.md).</span></span> <span data-ttu-id="718d3-105">公共语言运行时 (CLR) 对 `ProvideAssembly` 列表中未显示的每个程序集的调用。</span><span class="sxs-lookup"><span data-stu-id="718d3-105">The common language runtime (CLR) calls `ProvideAssembly` for each assembly that does not appear in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="718d3-106">语法</span><span class="sxs-lookup"><span data-stu-id="718d3-106">Syntax</span></span>  
  
```cpp  
HRESULT ProvideAssembly (  
    [in]  AssemblyBindInfo *pBindInfo,  
    [out] UINT64           *pAssemblyId,  
    [out] UINT64           *pHostContext,  
    [out] IStream          **ppStmAssemblyImage,  
    [out] IStream          **ppStmPDB  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="718d3-107">参数</span><span class="sxs-lookup"><span data-stu-id="718d3-107">Parameters</span></span>  

 `pBindInfo`  
 <span data-ttu-id="718d3-108">中指向 [AssemblyBindInfo](assemblybindinfo-structure.md) 实例的指针，主机使用该实例来确定特定的绑定特征，包括是否存在任何版本控制策略以及要绑定到的程序集。</span><span class="sxs-lookup"><span data-stu-id="718d3-108">[in] A pointer to an [AssemblyBindInfo](assemblybindinfo-structure.md) instance that the host uses to determine certain bind characteristics, including the presence or absence of any versioning policy, and which assembly to bind to.</span></span>  
  
 `pAssemblyId`  
 <span data-ttu-id="718d3-109">弄指向此的请求程序集的唯一标识符的指针 `IStream` 。</span><span class="sxs-lookup"><span data-stu-id="718d3-109">[out] A pointer to a unique identifier for the requested assembly for this `IStream`.</span></span>  
  
 `pHostContext`  
 <span data-ttu-id="718d3-110">弄指向特定于主机的数据的指针，用于在不需要平台调用的情况下确定请求的程序集的证据。</span><span class="sxs-lookup"><span data-stu-id="718d3-110">[out] A pointer to host-specific data that is used to determine the evidence of the requested assembly without the need of a platform invoke call.</span></span> <span data-ttu-id="718d3-111">`pHostContext` 对应于 <xref:System.Reflection.Assembly.HostContext%2A> 托管类的属性 <xref:System.Reflection.Assembly> 。</span><span class="sxs-lookup"><span data-stu-id="718d3-111">`pHostContext` corresponds to the <xref:System.Reflection.Assembly.HostContext%2A> property of the managed <xref:System.Reflection.Assembly> class.</span></span>  
  
 `ppStmAssemblyImage`  
 <span data-ttu-id="718d3-112">弄指向的地址的指针， `IStream` 该地址包含可移植的可执行文件 (PE) 映像，如果未能找到该程序集，则为 null。</span><span class="sxs-lookup"><span data-stu-id="718d3-112">[out] A pointer to the address of an `IStream` that contains the portable executable (PE) image to be loaded, or null if the assembly could not be found.</span></span>  
  
 `ppStmPDB`  
 <span data-ttu-id="718d3-113">弄指向 `IStream` 包含程序调试 (pdb) 信息的的地址的指针; 如果找不到 .pdb 文件，则为 null。</span><span class="sxs-lookup"><span data-stu-id="718d3-113">[out] A pointer to the address of an `IStream` that contains the program debug (PDB) information, or null if the .pdb file could not be found.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="718d3-114">返回值</span><span class="sxs-lookup"><span data-stu-id="718d3-114">Return Value</span></span>  
  
|<span data-ttu-id="718d3-115">HRESULT</span><span class="sxs-lookup"><span data-stu-id="718d3-115">HRESULT</span></span>|<span data-ttu-id="718d3-116">说明</span><span class="sxs-lookup"><span data-stu-id="718d3-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="718d3-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="718d3-117">S_OK</span></span>|<span data-ttu-id="718d3-118">`ProvideAssembly` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="718d3-118">`ProvideAssembly` returned successfully.</span></span>|  
|<span data-ttu-id="718d3-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="718d3-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="718d3-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="718d3-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="718d3-121">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="718d3-121">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="718d3-122">调用超时。</span><span class="sxs-lookup"><span data-stu-id="718d3-122">The call timed out.</span></span>|  
|<span data-ttu-id="718d3-123">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="718d3-123">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="718d3-124">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="718d3-124">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="718d3-125">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="718d3-125">HOST_E_ABANDONED</span></span>|<span data-ttu-id="718d3-126">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="718d3-126">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="718d3-127">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="718d3-127">E_FAIL</span></span>|<span data-ttu-id="718d3-128">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="718d3-128">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="718d3-129">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="718d3-129">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="718d3-130">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="718d3-130">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="718d3-131">COR_E_FILENOTFOUND (0x80070002) </span><span class="sxs-lookup"><span data-stu-id="718d3-131">COR_E_FILENOTFOUND (0x80070002)</span></span>|<span data-ttu-id="718d3-132">找不到请求的程序集。</span><span class="sxs-lookup"><span data-stu-id="718d3-132">The requested assembly could not be located.</span></span>|  
|<span data-ttu-id="718d3-133">E_NOT_SUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="718d3-133">E_NOT_SUFFICIENT_BUFFER</span></span>|<span data-ttu-id="718d3-134">指定的缓冲区大小 `pAssemblyId` 不够大，无法容纳主机需要返回的标识符。</span><span class="sxs-lookup"><span data-stu-id="718d3-134">The buffer size specified by `pAssemblyId` is not large enough to hold the identifier that the host wants to return.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="718d3-135">备注</span><span class="sxs-lookup"><span data-stu-id="718d3-135">Remarks</span></span>  

 <span data-ttu-id="718d3-136">为返回的标识值 `pAssemblyId` 由主机指定。</span><span class="sxs-lookup"><span data-stu-id="718d3-136">The identity value returned for `pAssemblyId` is specified by the host.</span></span> <span data-ttu-id="718d3-137">标识符在进程的生存期内必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="718d3-137">Identifiers must be unique within the lifetime of a process.</span></span> <span data-ttu-id="718d3-138">CLR 使用此值作为流的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="718d3-138">The CLR uses this value as a unique identifier for the stream.</span></span> <span data-ttu-id="718d3-139">它会对照的值检查每个值，以使其他对的 `pAssemblyId` 调用返回 `ProvideAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="718d3-139">It checks each value against the values for `pAssemblyId` returned by other calls to `ProvideAssembly`.</span></span> <span data-ttu-id="718d3-140">如果主机为其他主机返回相同的 `pAssemblyId` 值 `IStream` ，则 CLR 将检查是否已映射该流的内容。</span><span class="sxs-lookup"><span data-stu-id="718d3-140">If the host returns the same `pAssemblyId` value for another `IStream`, the CLR checks whether the contents of that stream have already been mapped.</span></span> <span data-ttu-id="718d3-141">如果是这样，则运行时加载映像的现有副本，而不是映射一个新副本。</span><span class="sxs-lookup"><span data-stu-id="718d3-141">If so, the runtime loads the existing copy of the image instead of mapping a new one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="718d3-142">要求</span><span class="sxs-lookup"><span data-stu-id="718d3-142">Requirements</span></span>  

 <span data-ttu-id="718d3-143">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="718d3-143">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="718d3-144">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="718d3-144">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="718d3-145">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="718d3-145">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="718d3-146">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="718d3-146">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="718d3-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="718d3-147">See also</span></span>

- [<span data-ttu-id="718d3-148">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="718d3-148">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="718d3-149">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="718d3-149">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
- [<span data-ttu-id="718d3-150">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="718d3-150">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)

---
description: 了解详细信息： ICorDebugProcess6：： EnableVirtualModuleSplitting 方法
title: ICorDebugProcess6::EnableVirtualModuleSplitting 方法
ms.date: 03/30/2017
ms.assetid: e7733bd3-68da-47f9-82ef-477db5f2e32d
ms.openlocfilehash: e56e66744ab971deba18f3bdc66d0cfb2053087f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722017"
---
# <a name="icordebugprocess6enablevirtualmodulesplitting-method"></a><span data-ttu-id="835a5-103">ICorDebugProcess6::EnableVirtualModuleSplitting 方法</span><span class="sxs-lookup"><span data-stu-id="835a5-103">ICorDebugProcess6::EnableVirtualModuleSplitting Method</span></span>

<span data-ttu-id="835a5-104">启用或禁用虚拟模块拆分。</span><span class="sxs-lookup"><span data-stu-id="835a5-104">Enables or disables virtual module splitting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="835a5-105">语法</span><span class="sxs-lookup"><span data-stu-id="835a5-105">Syntax</span></span>  
  
```cpp  
HRESULT EnableVirtualModuleSplitting(  
   BOOL enableSplitting  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="835a5-106">参数</span><span class="sxs-lookup"><span data-stu-id="835a5-106">Parameters</span></span>  

 `enableSplitting`  
 <span data-ttu-id="835a5-107">`true` 来启用虚拟模块拆分；`false` 来将其禁用。</span><span class="sxs-lookup"><span data-stu-id="835a5-107">`true` to enable virtual module splitting; `false` to disable it.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="835a5-108">备注</span><span class="sxs-lookup"><span data-stu-id="835a5-108">Remarks</span></span>  

 <span data-ttu-id="835a5-109">虚拟模块拆分会导致 [ICorDebug](icordebug-interface.md) 识别在生成过程中合并在一起的模块，并将它们显示为一组单独的模块，而不是单个大模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-109">Virtual module splitting causes [ICorDebug](icordebug-interface.md) to recognize modules that were merged together during the build process and present them as a group of separate modules rather than a single large module.</span></span> <span data-ttu-id="835a5-110">执行此操作将更改以下所述的各种 [ICorDebug](icordebug-interface.md) 方法的行为。</span><span class="sxs-lookup"><span data-stu-id="835a5-110">Doing this changes the behavior of various [ICorDebug](icordebug-interface.md) methods described below.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="835a5-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="835a5-111">This method is available with .NET Native only.</span></span>  
  
 <span data-ttu-id="835a5-112">可随时调用方法并更改 `enableSplitting` 值。</span><span class="sxs-lookup"><span data-stu-id="835a5-112">This method can be called and the value of `enableSplitting` can be changed at any time.</span></span> <span data-ttu-id="835a5-113">它不会在 [ICorDebug](icordebug-interface.md) 对象中产生任何有状态的功能更改，而不是在调用 [虚拟模块拆分和非托管调试 api](#APIs) 部分中列出的方法的行为。</span><span class="sxs-lookup"><span data-stu-id="835a5-113">It does not cause any stateful functional changes in an [ICorDebug](icordebug-interface.md) object, other than altering the behavior of the methods listed in the [Virtual module splitting and the unmanaged debugging APIs](#APIs) section at the time they are called.</span></span> <span data-ttu-id="835a5-114">调用那些方法时，使用虚拟模块确实会导致性能显著下降。</span><span class="sxs-lookup"><span data-stu-id="835a5-114">Using virtual modules does incur a performance penalty when calling those methods.</span></span> <span data-ttu-id="835a5-115">此外，可能还需要对虚拟化的元数据进行大量的内存中缓存，才能正确实现 [IMetaDataImport](../metadata/imetadataimport-interface.md) api，并且即使在关闭虚拟模块拆分后，这些缓存也会保留。</span><span class="sxs-lookup"><span data-stu-id="835a5-115">In addition, significant in-memory caching of the virtualized metadata may be required to correctly implement the [IMetaDataImport](../metadata/imetadataimport-interface.md) APIs, and these caches may be retained even after virtual module splitting has been turned off.</span></span>  
  
## <a name="terminology"></a><span data-ttu-id="835a5-116">术语</span><span class="sxs-lookup"><span data-stu-id="835a5-116">Terminology</span></span>  

 <span data-ttu-id="835a5-117">描述虚拟模块拆分时会用到下列术语：</span><span class="sxs-lookup"><span data-stu-id="835a5-117">The following terms are used when describing virtual module splitting:</span></span>  
  
 <span data-ttu-id="835a5-118">容器模块，即容器</span><span class="sxs-lookup"><span data-stu-id="835a5-118">container modules, or containers</span></span>  
 <span data-ttu-id="835a5-119">聚合模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-119">The aggregate modules.</span></span>  
  
 <span data-ttu-id="835a5-120">子模块，即虚拟模块</span><span class="sxs-lookup"><span data-stu-id="835a5-120">sub-modules, or virtual modules</span></span>  
 <span data-ttu-id="835a5-121">在容器中发现的各模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-121">The modules found in a container.</span></span>  
  
 <span data-ttu-id="835a5-122">普通模块</span><span class="sxs-lookup"><span data-stu-id="835a5-122">regular modules</span></span>  
 <span data-ttu-id="835a5-123">未在生成过程中合并的模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-123">Modules that were not merged at build time.</span></span> <span data-ttu-id="835a5-124">它们既不是容器模块也不是子模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-124">They are neither container modules nor sub-modules.</span></span>  
  
 <span data-ttu-id="835a5-125">但 ICor调试模块接口对象会表示容器模块和子模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-125">Both container modules and sub-modules are represented by ICorDebugModule interface objects.</span></span> <span data-ttu-id="835a5-126">但是，在每种情况下，接口的行为稍有不同，如 \<x-ref to section> 部分所述。</span><span class="sxs-lookup"><span data-stu-id="835a5-126">However, the behavior of the interface is slightly different in each case, as the \<x-ref to section> section describes.</span></span>  
  
## <a name="modules-and-assemblies"></a><span data-ttu-id="835a5-127">模块和程序集</span><span class="sxs-lookup"><span data-stu-id="835a5-127">Modules and assemblies</span></span>  

 <span data-ttu-id="835a5-128">在程序集合并的情况下，多模块程序集不受支持，因此模块和程序集之间存在一对一的关系。</span><span class="sxs-lookup"><span data-stu-id="835a5-128">Multi-module assemblies are not supported for assembly merging scenarios, so there is a one-to-one relationship between a module and an assembly.</span></span> <span data-ttu-id="835a5-129">每个 ICor调试模块对象（不论其代表容器模块还是子模块）都拥有相应的 ICor调试程序集对象。</span><span class="sxs-lookup"><span data-stu-id="835a5-129">Each ICorDebugModule object, regardless of whether it represents a container module or a sub-module, has a corresponding ICorDebugAssembly object.</span></span> <span data-ttu-id="835a5-130">[ICorDebugModule：： GetAssembly](icordebugmodule-getassembly-method.md)方法从模块转换为程序集。</span><span class="sxs-lookup"><span data-stu-id="835a5-130">The [ICorDebugModule::GetAssembly](icordebugmodule-getassembly-method.md) method converts from the module to the assembly.</span></span> <span data-ttu-id="835a5-131">若要以其他方向映射， [ICorDebugAssembly：： EnumerateModules](icordebugassembly-enumeratemodules-method.md) 方法只枚举1个模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-131">To map in the other direction, the [ICorDebugAssembly::EnumerateModules](icordebugassembly-enumeratemodules-method.md) method enumerates only 1 module.</span></span> <span data-ttu-id="835a5-132">因为在此情况下的程序集和模块形成了一个紧密耦合对，术语程序集和模块变得在很大程度上可以互换。</span><span class="sxs-lookup"><span data-stu-id="835a5-132">Because assembly and module form a tightly coupled pair in this case, the terms assembly and module become largely interchangeable.</span></span>  
  
## <a name="behavioral-differences"></a><span data-ttu-id="835a5-133">行为差异</span><span class="sxs-lookup"><span data-stu-id="835a5-133">Behavioral differences</span></span>  

 <span data-ttu-id="835a5-134">容器模块包含以下行为和特征：</span><span class="sxs-lookup"><span data-stu-id="835a5-134">Container modules have the following behaviors and characteristics:</span></span>  
  
- <span data-ttu-id="835a5-135">所有组成子模块的元数据合并在一起。</span><span class="sxs-lookup"><span data-stu-id="835a5-135">Their metadata for all of the constituent sub-modules is merged together.</span></span>  
  
- <span data-ttu-id="835a5-136">类型名称可能改变。</span><span class="sxs-lookup"><span data-stu-id="835a5-136">Their type names may be mangled.</span></span>  
  
- <span data-ttu-id="835a5-137">[ICorDebugModule：： GetName](icordebugmodule-getname-method.md)方法返回磁盘上的模块的路径。</span><span class="sxs-lookup"><span data-stu-id="835a5-137">The [ICorDebugModule::GetName](icordebugmodule-getname-method.md) method returns the path to an on-disk module.</span></span>  
  
- <span data-ttu-id="835a5-138">[ICorDebugModule：： GetSize](icordebugmodule-getsize-method.md)方法返回该图像的大小。</span><span class="sxs-lookup"><span data-stu-id="835a5-138">The [ICorDebugModule::GetSize](icordebugmodule-getsize-method.md) method returns the size of that image.</span></span>  
  
- <span data-ttu-id="835a5-139">ICorDebugAssembly3.EnumerateContainedAssemblies 方法列举子模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-139">The ICorDebugAssembly3.EnumerateContainedAssemblies method lists the sub-modules.</span></span>  
  
- <span data-ttu-id="835a5-140">ICorDebugAssembly3.GetContainerAssembly 方法返回 `S_FALSE`。</span><span class="sxs-lookup"><span data-stu-id="835a5-140">The ICorDebugAssembly3.GetContainerAssembly method returns `S_FALSE`.</span></span>  
  
 <span data-ttu-id="835a5-141">子模块包含以下行为和特征：</span><span class="sxs-lookup"><span data-stu-id="835a5-141">Sub-modules have the following behaviors and characteristics:</span></span>  
  
- <span data-ttu-id="835a5-142">他们具有一套减少的元数据，这些元数据只对应合并的原始程序集。</span><span class="sxs-lookup"><span data-stu-id="835a5-142">They have a reduced set of metadata that corresponds only to the original assembly that was merged.</span></span>  
  
- <span data-ttu-id="835a5-143">元数据名未改变。</span><span class="sxs-lookup"><span data-stu-id="835a5-143">The metadata names are not mangled.</span></span>  
  
- <span data-ttu-id="835a5-144">元数据令牌经生成过程合并之前，不大可能与原始程序集中的令牌匹配。</span><span class="sxs-lookup"><span data-stu-id="835a5-144">Metadata tokens are unlikely to match the tokens in the original assembly before it was merged in the build process.</span></span>  
  
- <span data-ttu-id="835a5-145">[ICorDebugModule：： GetName](icordebugmodule-getname-method.md)方法返回程序集名称，而不是文件路径。</span><span class="sxs-lookup"><span data-stu-id="835a5-145">The [ICorDebugModule::GetName](icordebugmodule-getname-method.md) method returns the assembly name, not a file path.</span></span>  
  
- <span data-ttu-id="835a5-146">[ICorDebugModule：： GetSize](icordebugmodule-getsize-method.md)方法返回未合并的原始图像大小。</span><span class="sxs-lookup"><span data-stu-id="835a5-146">The [ICorDebugModule::GetSize](icordebugmodule-getsize-method.md) method returns the original unmerged image size.</span></span>  
  
- <span data-ttu-id="835a5-147">ICorDebugModule3.EnumerateContainedAssemblies 方法返回 `S_FALSE`。</span><span class="sxs-lookup"><span data-stu-id="835a5-147">The ICorDebugModule3.EnumerateContainedAssemblies method returns `S_FALSE`.</span></span>  
  
- <span data-ttu-id="835a5-148">ICorDebugAssembly3.GetContainerAssembly 方法返回包含模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-148">The ICorDebugAssembly3.GetContainerAssembly method returns the containing module.</span></span>  
  
## <a name="interfaces-retrieved-from-modules"></a><span data-ttu-id="835a5-149">从模块恢复的接口</span><span class="sxs-lookup"><span data-stu-id="835a5-149">Interfaces retrieved from modules</span></span>  

 <span data-ttu-id="835a5-150">模块可恢复或创建多个接口。</span><span class="sxs-lookup"><span data-stu-id="835a5-150">A variety of interfaces can be created or retrieved from modules.</span></span> <span data-ttu-id="835a5-151">其中包括：</span><span class="sxs-lookup"><span data-stu-id="835a5-151">Some of these include:</span></span>  
  
- <span data-ttu-id="835a5-152">ICorDebugClass 对象，由 [ICorDebugModule：： GetClassFromToken](icordebugmodule-getclassfromtoken-method.md) 方法返回。</span><span class="sxs-lookup"><span data-stu-id="835a5-152">An ICorDebugClass object, which is returned by the [ICorDebugModule::GetClassFromToken](icordebugmodule-getclassfromtoken-method.md) method.</span></span>  
  
- <span data-ttu-id="835a5-153">ICorDebugAssembly 对象，由 [ICorDebugModule：： GetAssembly](icordebugmodule-getassembly-method.md) 方法返回。</span><span class="sxs-lookup"><span data-stu-id="835a5-153">An ICorDebugAssembly object, which is returned by the [ICorDebugModule::GetAssembly](icordebugmodule-getassembly-method.md) method.</span></span>  
  
 <span data-ttu-id="835a5-154">这些对象始终由 [ICorDebug](icordebug-interface.md)缓存，它们具有相同的指针标识，无论是从容器模块还是子模块中创建或查询它们。</span><span class="sxs-lookup"><span data-stu-id="835a5-154">These objects are always cached by [ICorDebug](icordebug-interface.md), and they will have the same pointer identity regardless of whether they were created or queried from the container module or a sub-module.</span></span> <span data-ttu-id="835a5-155">子模块提供了这些缓存对象的筛选视图，而非包含各自副本的单独缓存。</span><span class="sxs-lookup"><span data-stu-id="835a5-155">The sub-module provides a filtered view of these cached objects, not a separate cache with its own copies.</span></span>  
  
<a name="APIs"></a>

## <a name="virtual-module-splitting-and-the-unmanaged-debugging-apis"></a><span data-ttu-id="835a5-156">虚拟模块拆分和未托管调试 API</span><span class="sxs-lookup"><span data-stu-id="835a5-156">Virtual module splitting and the unmanaged debugging APIs</span></span>  

 <span data-ttu-id="835a5-157">下表显示了虚拟模块拆分如何影响未托管调试 API 中的其他方法的行为。</span><span class="sxs-lookup"><span data-stu-id="835a5-157">The following table shows how virtual module splitting affects the behavior of other methods in the unmanaged debugging API.</span></span>  
  
|<span data-ttu-id="835a5-158">方法</span><span class="sxs-lookup"><span data-stu-id="835a5-158">Method</span></span>|`enableSplitting` = `true`|`enableSplitting` = `false`|  
|------------|---------------------------------|----------------------------------|  
|[<span data-ttu-id="835a5-159">ICorDebugFunction::GetModule</span><span class="sxs-lookup"><span data-stu-id="835a5-159">ICorDebugFunction::GetModule</span></span>](icordebugfunction-getmodule-method.md)|<span data-ttu-id="835a5-160">返回最初定义该功能的子模块</span><span class="sxs-lookup"><span data-stu-id="835a5-160">Returns the sub-module this function was originally defined in</span></span>|<span data-ttu-id="835a5-161">返回该功能合并到的容器模块</span><span class="sxs-lookup"><span data-stu-id="835a5-161">Returns the container module this function was merged into</span></span>|  
|[<span data-ttu-id="835a5-162">ICorDebugClass::GetModule</span><span class="sxs-lookup"><span data-stu-id="835a5-162">ICorDebugClass::GetModule</span></span>](icordebugclass-getmodule-method.md)|<span data-ttu-id="835a5-163">返回最初定义该类的子模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-163">Returns the sub-module this class was originally defined in.</span></span>|<span data-ttu-id="835a5-164">返回该类合并到的容器模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-164">Returns the container module this class was merged into.</span></span>|  
|<span data-ttu-id="835a5-165">ICorDebugModuleDebugEvent::GetModule</span><span class="sxs-lookup"><span data-stu-id="835a5-165">ICorDebugModuleDebugEvent::GetModule</span></span>|<span data-ttu-id="835a5-166">返回加载的容器模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-166">Returns the container module that was loaded.</span></span> <span data-ttu-id="835a5-167">不管此设置如何，子模块不会收到加载事件。</span><span class="sxs-lookup"><span data-stu-id="835a5-167">Sub-modules are not given load events regardless of this setting.</span></span>|<span data-ttu-id="835a5-168">返回加载的容器模块。</span><span class="sxs-lookup"><span data-stu-id="835a5-168">Returns the container module that was loaded.</span></span>|  
|[<span data-ttu-id="835a5-169">ICorDebugAppDomain::EnumerateAssemblies</span><span class="sxs-lookup"><span data-stu-id="835a5-169">ICorDebugAppDomain::EnumerateAssemblies</span></span>](icordebugappdomain-enumerateassemblies-method.md)|<span data-ttu-id="835a5-170">返回一组子程序集和普通程序集；不包含容器程序集。</span><span class="sxs-lookup"><span data-stu-id="835a5-170">Returns a list of sub-assemblies and regular assemblies; no container assemblies are included.</span></span> <span data-ttu-id="835a5-171">**注意：**  如果任何容器程序集缺少符号，则将不会枚举其任何子程序集。</span><span class="sxs-lookup"><span data-stu-id="835a5-171">**Note:**  If any container assembly is missing symbols, none of its sub-assemblies will be enumerated.</span></span> <span data-ttu-id="835a5-172">如果任一普通程序集缺少符号，则其可能被枚举或不枚举。</span><span class="sxs-lookup"><span data-stu-id="835a5-172">If any regular assembly is missing symbols, it may or may not be enumerated.</span></span>|<span data-ttu-id="835a5-173">返回一组子程序集和普通程序集；不包含子程序集。</span><span class="sxs-lookup"><span data-stu-id="835a5-173">Returns a list of container assemblies and regular assemblies; no sub-assemblies are included.</span></span> <span data-ttu-id="835a5-174">**注意：**  如果任何常规程序集缺少符号，则可以或不会枚举它。</span><span class="sxs-lookup"><span data-stu-id="835a5-174">**Note:**  If any regular assembly is missing symbols, it may or may not be enumerated.</span></span>|  
|<span data-ttu-id="835a5-175">) 仅当引用 IL 代码时， [ICorDebugCode：： GetCode](icordebugcode-getcode-method.md) (</span><span class="sxs-lookup"><span data-stu-id="835a5-175">[ICorDebugCode::GetCode](icordebugcode-getcode-method.md) (when referring to IL code only)</span></span>|<span data-ttu-id="835a5-176">返回可能在预合并程序集图像中有效的 IL。</span><span class="sxs-lookup"><span data-stu-id="835a5-176">Returns IL that would be valid in a pre-merge assembly image.</span></span> <span data-ttu-id="835a5-177">具体来说，当包含 IL 的虚拟模块未定义参考类型时，任一内联元数据令牌都可以作为 TypeRef 或 MemberRef 令牌。</span><span class="sxs-lookup"><span data-stu-id="835a5-177">Specifically, any inline metadata tokens will correctly be TypeRef or MemberRef tokens when the types being referred to are not defined in the virtual module containing the IL.</span></span> <span data-ttu-id="835a5-178">可以在对应的 virtual ICorDebugModule 对象的 [IMetaDataImport](../metadata/imetadataimport-interface.md) 对象中查找这些 TypeRef 或 MemberRef 标记。</span><span class="sxs-lookup"><span data-stu-id="835a5-178">These TypeRef or MemberRef tokens can be looked up in the [IMetaDataImport](../metadata/imetadataimport-interface.md) object for the corresponding virtual ICorDebugModule object.</span></span>|<span data-ttu-id="835a5-179">返回预合并程序集图像中的 IL。</span><span class="sxs-lookup"><span data-stu-id="835a5-179">Returns the IL in the post-merge assembly image.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="835a5-180">要求</span><span class="sxs-lookup"><span data-stu-id="835a5-180">Requirements</span></span>  

 <span data-ttu-id="835a5-181">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="835a5-181">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="835a5-182">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="835a5-182">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="835a5-183">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="835a5-183">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="835a5-184">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="835a5-184">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="835a5-185">请参阅</span><span class="sxs-lookup"><span data-stu-id="835a5-185">See also</span></span>

- [<span data-ttu-id="835a5-186">“ICor调试进程6”接口</span><span class="sxs-lookup"><span data-stu-id="835a5-186">ICorDebugProcess6 Interface</span></span>](icordebugprocess6-interface.md)
- [<span data-ttu-id="835a5-187">调试接口</span><span class="sxs-lookup"><span data-stu-id="835a5-187">Debugging Interfaces</span></span>](debugging-interfaces.md)

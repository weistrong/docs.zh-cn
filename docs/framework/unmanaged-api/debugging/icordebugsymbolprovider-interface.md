---
description: 了解详细信息： ICorDebugSymbolProvider 接口
title: ICorDebugSymbolProvider 接口
ms.date: 03/30/2017
ms.assetid: 85b24196-b6c6-4bda-9de3-47180bd6ff96
ms.openlocfilehash: bd47f294092ee87fc1f34bc68fe744b447e21f20
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659570"
---
# <a name="icordebugsymbolprovider-interface"></a><span data-ttu-id="eac3a-103">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="eac3a-103">ICorDebugSymbolProvider Interface</span></span>

<span data-ttu-id="eac3a-104">提供可用于检索调试符号信息的方法。</span><span class="sxs-lookup"><span data-stu-id="eac3a-104">Provides methods that can be used to retrieve debug symbol information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="eac3a-105">方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-105">Methods</span></span>  
  
|<span data-ttu-id="eac3a-106">方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-106">Method</span></span>|<span data-ttu-id="eac3a-107">说明</span><span class="sxs-lookup"><span data-stu-id="eac3a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="eac3a-108">GetAssemblyImageBytes 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-108">GetAssemblyImageBytes Method</span></span>](icordebugsymbolprovider-getassemblyimagebytes-method.md)|<span data-ttu-id="eac3a-109">给定合并程序集的相对虚拟地址 (RVA)，读取合并程序集中的数据。</span><span class="sxs-lookup"><span data-stu-id="eac3a-109">Reads data from a merged assembly given a relative virtual address (RVA) in the merged assembly.</span></span>|  
|[<span data-ttu-id="eac3a-110">GetAssemblyImageMetadata 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-110">GetAssemblyImageMetadata Method</span></span>](icordebugsymbolprovider-getassemblyimagemetadata-method.md)|<span data-ttu-id="eac3a-111">返回合并程序集中的元数据。</span><span class="sxs-lookup"><span data-stu-id="eac3a-111">Returns the metadata from a merged assembly.</span></span>|  
|[<span data-ttu-id="eac3a-112">GetCodeRange 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-112">GetCodeRange Method</span></span>](icordebugsymbolprovider-getcoderange-method.md)|<span data-ttu-id="eac3a-113">给定方法的相对虚拟地址 (RVA)，获取该方法的起始地址和大小。</span><span class="sxs-lookup"><span data-stu-id="eac3a-113">Gets the method start address and size given a relative virtual address (RVA) in a method.</span></span>|  
|[<span data-ttu-id="eac3a-114">GetInstanceFieldSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-114">GetInstanceFieldSymbols Method</span></span>](icordebugsymbolprovider-getinstancefieldsymbols-method.md)|<span data-ttu-id="eac3a-115">获取与 Typespec 签名相对应的实例字段符号。</span><span class="sxs-lookup"><span data-stu-id="eac3a-115">Gets the instance field symbols that correspond to a typespec signature.</span></span>|  
|[<span data-ttu-id="eac3a-116">GetMergedAssemblyRecords 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-116">GetMergedAssemblyRecords Method</span></span>](icordebugsymbolprovider-getmergedassemblyrecords-method.md)|<span data-ttu-id="eac3a-117">获取所有合并程序集的符号记录。</span><span class="sxs-lookup"><span data-stu-id="eac3a-117">Gets the symbol records for all the merged assemblies.</span></span>|  
|[<span data-ttu-id="eac3a-118">GetMethodLocalSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-118">GetMethodLocalSymbols Method</span></span>](icordebugsymbolprovider-getmethodlocalsymbols-method.md)|<span data-ttu-id="eac3a-119">给定方法的相对虚拟地址 (RVA)，获取该方法的本地符号。</span><span class="sxs-lookup"><span data-stu-id="eac3a-119">Gets a method's local symbols given the relative virtual address (RVA) of that method.</span></span>|  
|[<span data-ttu-id="eac3a-120">GetMethodParameterSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-120">GetMethodParameterSymbols Method</span></span>](icordebugsymbolprovider-getmethodparametersymbols-method.md)|<span data-ttu-id="eac3a-121">给定方法的相对虚拟地址 (RVA) 后，获取该方法的参数符号。</span><span class="sxs-lookup"><span data-stu-id="eac3a-121">Gets a method's parameter symbols given the relative virtual address (RVA) of that method.</span></span>|  
|[<span data-ttu-id="eac3a-122">GetMethodProps 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-122">GetMethodProps Method</span></span>](icordebugsymbolprovider-getmethodprops-method.md)|<span data-ttu-id="eac3a-123">给定方法的相对虚拟地址 (RVA)，返回有关该方法属性的信息，例如该方法的元数据标记及其泛型参数信息。</span><span class="sxs-lookup"><span data-stu-id="eac3a-123">Returns information about method properties, such as the method's metadata token and information about its generic parameters, given a relative virtual address (RVA) in that method.</span></span>|  
|[<span data-ttu-id="eac3a-124">GetObjectSize 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-124">GetObjectSize Method</span></span>](icordebugsymbolprovider-getobjectsize-method.md)|<span data-ttu-id="eac3a-125">基于对象的 TypeSpec 签名返回对象的大小。</span><span class="sxs-lookup"><span data-stu-id="eac3a-125">Returns the object size for an object based on its typespec signature.</span></span>|  
|[<span data-ttu-id="eac3a-126">GetStaticFieldSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-126">GetStaticFieldSymbols Method</span></span>](icordebugsymbolprovider-getstaticfieldsymbols-method.md)|<span data-ttu-id="eac3a-127">获取与 Typespec 签名相对应的静态字段符号。</span><span class="sxs-lookup"><span data-stu-id="eac3a-127">Gets the static field symbols that correspond to a typespec signature.</span></span>|  
|[<span data-ttu-id="eac3a-128">GetTypeProps 方法</span><span class="sxs-lookup"><span data-stu-id="eac3a-128">GetTypeProps Method</span></span>](icordebugsymbolprovider-gettypeprops-method.md)|<span data-ttu-id="eac3a-129">给定 vtable 中的相对虚拟地址 (RVA)，返回类型的属性信息（例如其泛型参数的签名数量）。</span><span class="sxs-lookup"><span data-stu-id="eac3a-129">Returns information about a type's properties, such as the number of signature of its generic parameters, given a relative virtual address (RVA) in a vtable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eac3a-130">备注</span><span class="sxs-lookup"><span data-stu-id="eac3a-130">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="eac3a-131">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="eac3a-131">This interface is available with .NET Native only.</span></span> <span data-ttu-id="eac3a-132">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="eac3a-132">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eac3a-133">要求</span><span class="sxs-lookup"><span data-stu-id="eac3a-133">Requirements</span></span>  

 <span data-ttu-id="eac3a-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eac3a-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eac3a-135">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eac3a-135">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eac3a-136">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eac3a-136">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eac3a-137">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eac3a-137">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eac3a-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="eac3a-138">See also</span></span>

- [<span data-ttu-id="eac3a-139">调试接口</span><span class="sxs-lookup"><span data-stu-id="eac3a-139">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="eac3a-140">调试</span><span class="sxs-lookup"><span data-stu-id="eac3a-140">Debugging</span></span>](index.md)

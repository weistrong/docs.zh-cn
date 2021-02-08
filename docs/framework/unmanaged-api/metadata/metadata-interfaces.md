---
description: 了解更多：元数据接口
title: 元数据接口
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged interfaces [.NET Framework], metadata
- metadata interfaces [.NET Framework]
- interfaces (.NET Framework metadata]
ms.assetid: f5cdac93-a28c-48ef-8a19-5773376e9e7c
ms.openlocfilehash: 4851fbc93bfa29f1b4b5015c82f05c1b200b9092
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799130"
---
# <a name="metadata-interfaces"></a><span data-ttu-id="25ec1-103">元数据接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-103">Metadata Interfaces</span></span>

<span data-ttu-id="25ec1-104">本节描述非托管接口，这些接口提供对由 .NET Framework 类型、方法、字段等公开的元数据的访问。</span><span class="sxs-lookup"><span data-stu-id="25ec1-104">This section describes the unmanaged interfaces that provide access to the metadata exposed by the .NET Framework types, methods, fields, and so on.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="25ec1-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="25ec1-105">In This Section</span></span>  

 [<span data-ttu-id="25ec1-106">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-106">ICeeGen Interface</span></span>](iceegen-interface.md)  
 <span data-ttu-id="25ec1-107">提供用于动态代码编译的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-107">Provides methods for dynamic code compilation.</span></span>  
  
 [<span data-ttu-id="25ec1-108">IHostFilter 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-108">IHostFilter Interface</span></span>](ihostfilter-interface.md)  
 <span data-ttu-id="25ec1-109">提供运行时主机用于标记待处理的元数据标记的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-109">Provides a method for the run-time host to mark metadata tokens for processing.</span></span>  
  
 [<span data-ttu-id="25ec1-110">IMapToken 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-110">IMapToken Interface</span></span>](imaptoken-interface.md)  
 <span data-ttu-id="25ec1-111">提供导入的和发出的元数据签名之间的映射功能。</span><span class="sxs-lookup"><span data-stu-id="25ec1-111">Provides mapping capabilities between imported and emitted metadata signatures.</span></span>  
  
 [<span data-ttu-id="25ec1-112">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-112">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)  
 <span data-ttu-id="25ec1-113">提供支持公共语言运行时 (CLR) 用于解析和使用资源的自描述模型的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-113">Provides methods that support the self-description model used by the common language runtime (CLR) to resolve and consume resources.</span></span>  
  
 [<span data-ttu-id="25ec1-114">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-114">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)  
 <span data-ttu-id="25ec1-115">提供访问和检查程序集清单内容的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-115">Provides methods to access and examine the contents of an assembly manifest.</span></span>  
  
 [<span data-ttu-id="25ec1-116">IMetaDataConverter 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-116">IMetaDataConverter Interface</span></span>](imetadataconverter-interface.md)  
 <span data-ttu-id="25ec1-117">提供将类型库映射到其元数据签名并进行相互转换的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-117">Provides methods to map type libraries to their metadata signatures, and to convert from one to the other.</span></span>  
  
 [<span data-ttu-id="25ec1-118">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-118">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)  
 <span data-ttu-id="25ec1-119">`IMetaDataDispenser` 已过时。</span><span class="sxs-lookup"><span data-stu-id="25ec1-119">`IMetaDataDispenser` is obsolete.</span></span> <span data-ttu-id="25ec1-120">请改用 `IMetaDataDispenserEx`。</span><span class="sxs-lookup"><span data-stu-id="25ec1-120">Use `IMetaDataDispenserEx` instead.</span></span>  
  
 [<span data-ttu-id="25ec1-121">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-121">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)  
 <span data-ttu-id="25ec1-122">提供映射用于创建或修改元数据的内存区域的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-122">Provides methods that map areas of memory for creating or modifying metadata.</span></span>  
  
 [<span data-ttu-id="25ec1-123">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-123">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)  
 <span data-ttu-id="25ec1-124">提供创建、修改和存储与当前定义的范围中的程序集相关的元数据的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-124">Provides methods to create, modify and store metadata about the assembly in the currently defined scope.</span></span>  
  
 [<span data-ttu-id="25ec1-125">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-125">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)  
 <span data-ttu-id="25ec1-126">提供用于定义和修改方法的元数据签名和带有 <xref:System.Type?displayProperty=nameWithType> 类型的参数的构造函数的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-126">Provides methods for defining and modifying the metadata signatures of methods and constructors with parameters of type <xref:System.Type?displayProperty=nameWithType>.</span></span>  
  
 [<span data-ttu-id="25ec1-127">IMetaDataError 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-127">IMetaDataError Interface</span></span>](imetadataerror-interface.md)  
 <span data-ttu-id="25ec1-128">提供用于在解析程序集的元数据签名期间报告错误的回调机制。</span><span class="sxs-lookup"><span data-stu-id="25ec1-128">Provides a callback mechanism for reporting errors during the resolution of the metadata signature for an assembly.</span></span>  
  
 [<span data-ttu-id="25ec1-129">IMetaDataFilter 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-129">IMetaDataFilter Interface</span></span>](imetadatafilter-interface.md)  
 <span data-ttu-id="25ec1-130">提供用于标记和筛选元数据标记以避免重复已进行的操作的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-130">Provides methods for marking and filtering metadata tokens to avoid repeating actions that have already been taken.</span></span>  
  
 [<span data-ttu-id="25ec1-131">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-131">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)  
 <span data-ttu-id="25ec1-132">提供用于从其他程序集导入和操作类型的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-132">Provides methods for importing and manipulating types from other assemblies.</span></span>  
  
 [<span data-ttu-id="25ec1-133">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-133">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)  
 <span data-ttu-id="25ec1-134">扩展 `IMetaDataImport` 以提供使用泛型类型的功能。</span><span class="sxs-lookup"><span data-stu-id="25ec1-134">Extends `IMetaDataImport` to provide the capability of working with generic types.</span></span>  
  
 [<span data-ttu-id="25ec1-135">IMetaDataInfo 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-135">IMetaDataInfo Interface</span></span>](imetadatainfo-interface.md)  
 <span data-ttu-id="25ec1-136">提供一种方法，使用此方法可获取关于将元数据从磁盘文件映射到内存中的信息。</span><span class="sxs-lookup"><span data-stu-id="25ec1-136">Provides a method that gets information about the mapping of metadata from an on-disk file into memory.</span></span>  
  
 [<span data-ttu-id="25ec1-137">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-137">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)  
 <span data-ttu-id="25ec1-138">提供存储和检索表中元数据信息的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-138">Provides methods for the storage and retrieval of metadata information in tables.</span></span>  
  
 [<span data-ttu-id="25ec1-139">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-139">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)  
 <span data-ttu-id="25ec1-140">扩展 `IMetaDataTables` 以包含用于处理元数据流的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-140">Extends `IMetaDataTables` to include methods for working with metadata streams.</span></span>  
  
 [<span data-ttu-id="25ec1-141">IMetaDataValidate 接口</span><span class="sxs-lookup"><span data-stu-id="25ec1-141">IMetaDataValidate Interface</span></span>](imetadatavalidate-interface.md)  
 <span data-ttu-id="25ec1-142">提供验证元数据签名的方法。</span><span class="sxs-lookup"><span data-stu-id="25ec1-142">Provides methods to use for validation of metadata signatures.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="25ec1-143">相关章节</span><span class="sxs-lookup"><span data-stu-id="25ec1-143">Related Sections</span></span>  

 [<span data-ttu-id="25ec1-144">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="25ec1-144">Metadata Global Static Functions</span></span>](metadata-global-static-functions.md)  
  
 [<span data-ttu-id="25ec1-145">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="25ec1-145">Metadata Enumerations</span></span>](metadata-enumerations.md)  
  
 [<span data-ttu-id="25ec1-146">元数据结构</span><span class="sxs-lookup"><span data-stu-id="25ec1-146">Metadata Structures</span></span>](metadata-structures.md)  
  
 [<span data-ttu-id="25ec1-147">元数据联合</span><span class="sxs-lookup"><span data-stu-id="25ec1-147">Metadata Unions</span></span>](metadata-unions.md)

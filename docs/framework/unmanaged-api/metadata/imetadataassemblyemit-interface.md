---
description: 了解详细信息： IMetaDataAssemblyEmit 接口
title: IMetaDataAssemblyEmit 接口
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit
helpviewer_keywords:
- IMetaDataAssemblyEmit interface [.NET Framework metadata]
ms.assetid: 34fb03cc-2285-4a45-ac48-ad993b7a921a
topic_type:
- apiref
ms.openlocfilehash: bcfca4eedc14f2292c40874d86c4984b4c1948f5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678206"
---
# <a name="imetadataassemblyemit-interface"></a><span data-ttu-id="e4dd4-103">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="e4dd4-103">IMetaDataAssemblyEmit Interface</span></span>

<span data-ttu-id="e4dd4-104">提供支持公共语言运行时用于解析和使用资源的自描述模型的方法。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-104">Provides methods that support the self-description model used by the common language runtime to resolve and consume resources.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e4dd4-105">方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-105">Methods</span></span>  
  
|<span data-ttu-id="e4dd4-106">方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-106">Method</span></span>|<span data-ttu-id="e4dd4-107">说明</span><span class="sxs-lookup"><span data-stu-id="e4dd4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e4dd4-108">DefineAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-108">DefineAssembly Method</span></span>](imetadataassemblyemit-defineassembly-method.md)|<span data-ttu-id="e4dd4-109">创建包含指定程序集的元数据的程序集数据结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-109">Creates an assembly data structure containing metadata for the specified assembly, and returns the associated metadata token.</span></span>|  
|[<span data-ttu-id="e4dd4-110">DefineAssemblyRef 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-110">DefineAssemblyRef Method</span></span>](imetadataassemblyemit-defineassemblyref-method.md)|<span data-ttu-id="e4dd4-111">创建包含此程序集引用的程序集的元数据的 `AssemblyRef` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-111">Creates an `AssemblyRef` structure containing metadata for the assembly that this assembly references, and returns the associated metadata token.</span></span>|  
|[<span data-ttu-id="e4dd4-112">DefineExportedType 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-112">DefineExportedType Method</span></span>](imetadataassemblyemit-defineexportedtype-method.md)|<span data-ttu-id="e4dd4-113">创建包含指定导出类型的元数据的 `ExportedType` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-113">Creates an `ExportedType` structure containing metadata for the specified exported type, and returns the associated metadata token.</span></span>|  
|[<span data-ttu-id="e4dd4-114">DefineFile 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-114">DefineFile Method</span></span>](imetadataassemblyemit-definefile-method.md)|<span data-ttu-id="e4dd4-115">创建包含此程序集引用的程序集的元数据的 `File` 元数据结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-115">Creates a `File` metadata structure containing metadata for assembly referenced by this assembly, and returns the associated metadata token.</span></span>|  
|[<span data-ttu-id="e4dd4-116">DefineManifestResource 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-116">DefineManifestResource Method</span></span>](imetadataassemblyemit-definemanifestresource-method.md)|<span data-ttu-id="e4dd4-117">创建包含指定清单资源的元数据的 `ManifestResource` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-117">Creates a `ManifestResource` structure containing metadata for the specified manifest resource, and returns the associated metadata token.</span></span>|  
|[<span data-ttu-id="e4dd4-118">SetAssemblyProps 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-118">SetAssemblyProps Method</span></span>](imetadataassemblyemit-setassemblyprops-method.md)|<span data-ttu-id="e4dd4-119">修改指定的 `Assembly` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-119">Modifies the specified `Assembly` metadata structure.</span></span>|  
|[<span data-ttu-id="e4dd4-120">SetAssemblyRefProps 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-120">SetAssemblyRefProps Method</span></span>](imetadataassemblyemit-setassemblyrefprops-method.md)|<span data-ttu-id="e4dd4-121">修改指定的 `AssemblyRef` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-121">Modifies the specified `AssemblyRef` metadata structure.</span></span>|  
|[<span data-ttu-id="e4dd4-122">SetExportedTypeProps 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-122">SetExportedTypeProps Method</span></span>](imetadataassemblyemit-setexportedtypeprops-method.md)|<span data-ttu-id="e4dd4-123">修改指定的 `ExportedType` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-123">Modifies the specified `ExportedType` metadata structure.</span></span>|  
|[<span data-ttu-id="e4dd4-124">SetFileProps 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-124">SetFileProps Method</span></span>](imetadataassemblyemit-setfileprops-method.md)|<span data-ttu-id="e4dd4-125">修改指定的 `File` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-125">Modifies the specified `File` metadata structure.</span></span>|  
|[<span data-ttu-id="e4dd4-126">SetManifestResourceProps 方法</span><span class="sxs-lookup"><span data-stu-id="e4dd4-126">SetManifestResourceProps Method</span></span>](imetadataassemblyemit-setmanifestresourceprops-method.md)|<span data-ttu-id="e4dd4-127">修改指定的 `ManifestResource` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-127">Modifies the specified `ManifestResource` metadata structure.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e4dd4-128">备注</span><span class="sxs-lookup"><span data-stu-id="e4dd4-128">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4dd4-129">要求</span><span class="sxs-lookup"><span data-stu-id="e4dd4-129">Requirements</span></span>  

 <span data-ttu-id="e4dd4-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4dd4-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4dd4-131">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e4dd4-131">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e4dd4-132">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e4dd4-132">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e4dd4-133">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4dd4-133">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4dd4-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4dd4-134">See also</span></span>

- [<span data-ttu-id="e4dd4-135">元数据接口</span><span class="sxs-lookup"><span data-stu-id="e4dd4-135">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="e4dd4-136">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="e4dd4-136">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)

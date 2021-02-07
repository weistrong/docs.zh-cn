---
description: 了解详细信息： IMetaDataAssemblyImport 接口
title: IMetaDataAssemblyImport 接口
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport
helpviewer_keywords:
- IMetaDataAssemblyImport interface [.NET Framework metadata]
ms.assetid: 29c6fba5-4cea-417d-b484-7ed22ebff1c9
topic_type:
- apiref
ms.openlocfilehash: bb9c5163e4f5b68700e5a3836fa55edbbebac01c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753635"
---
# <a name="imetadataassemblyimport-interface"></a><span data-ttu-id="790f0-103">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="790f0-103">IMetaDataAssemblyImport Interface</span></span>

<span data-ttu-id="790f0-104">提供访问和检查程序集清单内容的方法。</span><span class="sxs-lookup"><span data-stu-id="790f0-104">Provides methods to access and examine the contents of an assembly manifest.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="790f0-105">方法</span><span class="sxs-lookup"><span data-stu-id="790f0-105">Methods</span></span>  
  
|<span data-ttu-id="790f0-106">方法</span><span class="sxs-lookup"><span data-stu-id="790f0-106">Method</span></span>|<span data-ttu-id="790f0-107">说明</span><span class="sxs-lookup"><span data-stu-id="790f0-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="790f0-108">CloseEnum 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-108">CloseEnum Method</span></span>](imetadataassemblyimport-closeenum-method.md)|<span data-ttu-id="790f0-109">释放到指定枚举器的句柄。</span><span class="sxs-lookup"><span data-stu-id="790f0-109">Releases the handle to the specified enumerator.</span></span>|  
|[<span data-ttu-id="790f0-110">EnumAssemblyRefs 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-110">EnumAssemblyRefs Method</span></span>](imetadataassemblyimport-enumassemblyrefs-method.md)|<span data-ttu-id="790f0-111">获取一个接口指针，该指针指向包含 `mdAssemblyRef` 当前元数据范围内的程序集所引用的程序集的标记。</span><span class="sxs-lookup"><span data-stu-id="790f0-111">Gets an interface pointer to an enumerator that contains the `mdAssemblyRef` tokens of the assemblies referenced by the assembly in the current metadata scope.</span></span>|  
|[<span data-ttu-id="790f0-112">EnumExportedTypes 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-112">EnumExportedTypes Method</span></span>](imetadataassemblyimport-enumexportedtypes-method.md)|<span data-ttu-id="790f0-113">获取一个指向枚举数的接口指针，该枚举数包含 `mdExportedType` 当前元数据范围内的程序集引用的 COM 类型的标记。</span><span class="sxs-lookup"><span data-stu-id="790f0-113">Gets an interface pointer to an enumerator that contains the `mdExportedType` tokens of the COM types referenced by the assembly in the current metadata scope.</span></span>|  
|[<span data-ttu-id="790f0-114">EnumFiles 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-114">EnumFiles Method</span></span>](imetadataassemblyimport-enumfiles-method.md)|<span data-ttu-id="790f0-115">获取一个接口指针，该指针指向一个枚举数，该枚举数包含 `mdFile` 当前元数据范围内的程序集所引用的文件的标记。</span><span class="sxs-lookup"><span data-stu-id="790f0-115">Gets an interface pointer to an enumerator that contains the `mdFile` tokens of the files referenced by the assembly in the current metadata scope.</span></span>|  
|[<span data-ttu-id="790f0-116">EnumManifestResources 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-116">EnumManifestResources Method</span></span>](imetadataassemblyimport-enummanifestresources-method.md)|<span data-ttu-id="790f0-117">获取一个接口指针，该指针指向包含 `mdManifestResource` 当前元数据范围内的程序集所引用资源的标记的枚举数。</span><span class="sxs-lookup"><span data-stu-id="790f0-117">Gets an interface pointer to an enumerator that contains the `mdManifestResource` tokens of the resources referenced by the assembly in the current metadata scope.</span></span>|  
|[<span data-ttu-id="790f0-118">FindAssembliesByName 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-118">FindAssembliesByName Method</span></span>](imetadataassemblyimport-findassembliesbyname-method.md)|<span data-ttu-id="790f0-119">获取 `mdAssemblyRef` 具有指定名称的程序集的标记数组。</span><span class="sxs-lookup"><span data-stu-id="790f0-119">Gets an array of `mdAssemblyRef` tokens for the assemblies with the specified name.</span></span>|  
|[<span data-ttu-id="790f0-120">FindExportedTypeByName 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-120">FindExportedTypeByName Method</span></span>](imetadataassemblyimport-findexportedtypebyname-method.md)|<span data-ttu-id="790f0-121">获取 `mdExportedType` 具有指定名称的 COM 类型的标记。</span><span class="sxs-lookup"><span data-stu-id="790f0-121">Gets an `mdExportedType` token for the COM type with the specified name.</span></span>|  
|[<span data-ttu-id="790f0-122">FindManifestResourceByName 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-122">FindManifestResourceByName Method</span></span>](imetadataassemblyimport-findmanifestresourcebyname-method.md)|<span data-ttu-id="790f0-123">获取 `mdManifestResource` 具有指定名称的资源的标记。</span><span class="sxs-lookup"><span data-stu-id="790f0-123">Gets an `mdManifestResource` token for the resource with the specified name.</span></span>|  
|[<span data-ttu-id="790f0-124">GetAssemblyFromScope 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-124">GetAssemblyFromScope Method</span></span>](imetadataassemblyimport-getassemblyfromscope-method.md)|<span data-ttu-id="790f0-125">获取当前元数据范围内的程序集的标记。</span><span class="sxs-lookup"><span data-stu-id="790f0-125">Gets the token for the assembly in the current metadata scope.</span></span>|  
|[<span data-ttu-id="790f0-126">GetAssemblyProps 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-126">GetAssemblyProps Method</span></span>](imetadataassemblyimport-getassemblyprops-method.md)|<span data-ttu-id="790f0-127">获取指定程序集的属性设置。</span><span class="sxs-lookup"><span data-stu-id="790f0-127">Gets the property settings of the specified assembly.</span></span>|  
|[<span data-ttu-id="790f0-128">GetAssemblyRefProps 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-128">GetAssemblyRefProps Method</span></span>](imetadataassemblyimport-getassemblyrefprops-method.md)|<span data-ttu-id="790f0-129">获取指定标记的属性设置 `mdAssemblyRef` 。</span><span class="sxs-lookup"><span data-stu-id="790f0-129">Gets the property settings of the specified `mdAssemblyRef` token.</span></span>|  
|[<span data-ttu-id="790f0-130">GetExportedTypeProps 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-130">GetExportedTypeProps Method</span></span>](imetadataassemblyimport-getexportedtypeprops-method.md)|<span data-ttu-id="790f0-131">获取指定 COM 类型的属性设置。</span><span class="sxs-lookup"><span data-stu-id="790f0-131">Gets the property settings of the specified COM type.</span></span>|  
|[<span data-ttu-id="790f0-132">GetFileProps 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-132">GetFileProps Method</span></span>](imetadataassemblyimport-getfileprops-method.md)|<span data-ttu-id="790f0-133">获取指定文件的属性设置。</span><span class="sxs-lookup"><span data-stu-id="790f0-133">Gets the property settings of the specified file.</span></span>|  
|[<span data-ttu-id="790f0-134">GetManifestResourceProps 方法</span><span class="sxs-lookup"><span data-stu-id="790f0-134">GetManifestResourceProps Method</span></span>](imetadataassemblyimport-getmanifestresourceprops-method.md)|<span data-ttu-id="790f0-135">获取指定的清单资源的属性设置。</span><span class="sxs-lookup"><span data-stu-id="790f0-135">Gets the property settings of the specified manifest resource.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="790f0-136">要求</span><span class="sxs-lookup"><span data-stu-id="790f0-136">Requirements</span></span>  

 <span data-ttu-id="790f0-137">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="790f0-137">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="790f0-138">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="790f0-138">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="790f0-139">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="790f0-139">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="790f0-140">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="790f0-140">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="790f0-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="790f0-141">See also</span></span>

- [<span data-ttu-id="790f0-142">元数据接口</span><span class="sxs-lookup"><span data-stu-id="790f0-142">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="790f0-143">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="790f0-143">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)

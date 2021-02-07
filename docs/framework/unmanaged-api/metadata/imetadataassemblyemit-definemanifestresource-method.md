---
description: 了解详细信息： IMetaDataAssemblyEmit：:D efineManifestResource 方法
title: IMetaDataAssemblyEmit::DefineManifestResource 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineManifestResource
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineManifestResource
helpviewer_keywords:
- DefineManifestResource method [.NET Framework metadata]
- IMetaDataAssemblyEmit::DefineManifestResource method [.NET Framework metadata]
ms.assetid: 27f6d295-0fe9-4cda-b77e-6e7d5c53df09
topic_type:
- apiref
ms.openlocfilehash: 53994f1777cbd2e019f14c0ccae375e6424de509
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678323"
---
# <a name="imetadataassemblyemitdefinemanifestresource-method"></a><span data-ttu-id="5bb9e-103">IMetaDataAssemblyEmit::DefineManifestResource 方法</span><span class="sxs-lookup"><span data-stu-id="5bb9e-103">IMetaDataAssemblyEmit::DefineManifestResource Method</span></span>

<span data-ttu-id="5bb9e-104">创建包含指定清单资源的元数据的 `ManifestResource` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-104">Creates a `ManifestResource` structure containing metadata for the specified manifest resource, and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bb9e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5bb9e-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineManifestResource (  
    [in] LPCWSTR                szName,
    [in] mdToken                tkImplementation,
    [in] DWORD                  dwOffset,
    [in] DWORD                  dwResourceFlags,  
    [out] mdManifestResource    *pmdmr  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5bb9e-106">参数</span><span class="sxs-lookup"><span data-stu-id="5bb9e-106">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="5bb9e-107">中资源的名称。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-107">[in] The name of the resource.</span></span>  
  
 `tkImplementation`  
 <span data-ttu-id="5bb9e-108">中类型 `mdtFile` 或 `mdtAssemblyRef` 映射到资源提供程序的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-108">[in] A metadata token of type `mdtFile` or `mdtAssemblyRef` that maps to the resource provider.</span></span> <span data-ttu-id="5bb9e-109">NULL 值指示嵌入元数据的文件是资源提供程序。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-109">A NULL value indicates that the file in which the metadata is embedded is the resource provider.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="5bb9e-110">中文件中资源的起始位置的偏移量。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-110">[in] The offset to the beginning of the resource within the file.</span></span> <span data-ttu-id="5bb9e-111">对于独立文件中的资源，此值将始终为零。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-111">For resources in standalone files, this will always be zero.</span></span> <span data-ttu-id="5bb9e-112">如果资源嵌入在 PE (可移植可执行文件) 文件中，则这是资源 BLOB 的偏移量，它从 cor 头文件中指定的位置开始。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-112">If the resource is embedded in a PE (portable executable) file, this is an offset of the resource BLOB, which starts at the location specified in the cor.h header file.</span></span>  
  
 `dwResourceFlags`  
 <span data-ttu-id="5bb9e-113">中指定资源定义的属性设置的标志值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-113">[in] A bitwise combination of flag values that specify property settings for the resource definition.</span></span>  
  
 `pmdmr`  
 <span data-ttu-id="5bb9e-114">弄指向返回的元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-114">[out] A pointer to the returned metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5bb9e-115">备注</span><span class="sxs-lookup"><span data-stu-id="5bb9e-115">Remarks</span></span>  

 <span data-ttu-id="5bb9e-116">必须为每个 `ManifestResource` 在程序集的文件中实现的每个资源定义一个元数据结构。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-116">One `ManifestResource` metadata structure must be defined for each resource that is implemented in each of the assembly's files.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bb9e-117">要求</span><span class="sxs-lookup"><span data-stu-id="5bb9e-117">Requirements</span></span>  

 <span data-ttu-id="5bb9e-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5bb9e-118">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bb9e-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5bb9e-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5bb9e-120">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5bb9e-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5bb9e-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bb9e-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bb9e-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bb9e-122">See also</span></span>

- [<span data-ttu-id="5bb9e-123">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="5bb9e-123">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)

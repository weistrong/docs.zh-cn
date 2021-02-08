---
description: 了解详细信息： IMetaDataAssemblyImport：： FindManifestResourceByName 方法
title: IMetaDataAssemblyImport::FindManifestResourceByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindManifestResourceByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindManifestResourceByName
helpviewer_keywords:
- FindManifestResourceByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindManifestResourceByName method [.NET Framework metadata]
ms.assetid: 7b72fa11-3866-402b-bdea-2b966b77cfe0
topic_type:
- apiref
ms.openlocfilehash: 1d1312277675a1f2bf213221ab8d9d2a584733a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784166"
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a><span data-ttu-id="d625f-103">IMetaDataAssemblyImport::FindManifestResourceByName 方法</span><span class="sxs-lookup"><span data-stu-id="d625f-103">IMetaDataAssemblyImport::FindManifestResourceByName Method</span></span>

<span data-ttu-id="d625f-104">获取一个指针，该指针指向具有指定名称的清单资源。</span><span class="sxs-lookup"><span data-stu-id="d625f-104">Gets a pointer to the manifest resource with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d625f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d625f-105">Syntax</span></span>  
  
```cpp
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,
    [out] mdManifestResource     *ptkManifestResource  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="d625f-106">参数</span><span class="sxs-lookup"><span data-stu-id="d625f-106">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="d625f-107">中资源的名称。</span><span class="sxs-lookup"><span data-stu-id="d625f-107">[in] The name of the resource.</span></span>  
  
 `ptkManifestResource`  
 <span data-ttu-id="d625f-108">弄用于存储 `mdManifestResource` 元数据标记的数组，其中每个标记表示一个清单资源。</span><span class="sxs-lookup"><span data-stu-id="d625f-108">[out] The array used to store the `mdManifestResource` metadata tokens, each of which represents a manifest resource.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d625f-109">备注</span><span class="sxs-lookup"><span data-stu-id="d625f-109">Remarks</span></span>  

 <span data-ttu-id="d625f-110">`FindManifestResourceByName`方法使用公共语言运行时所使用的标准规则来解析引用。</span><span class="sxs-lookup"><span data-stu-id="d625f-110">The `FindManifestResourceByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d625f-111">要求</span><span class="sxs-lookup"><span data-stu-id="d625f-111">Requirements</span></span>  

 <span data-ttu-id="d625f-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d625f-112">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d625f-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d625f-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d625f-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d625f-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d625f-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d625f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d625f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d625f-116">See also</span></span>

- [<span data-ttu-id="d625f-117">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="d625f-117">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
- [<span data-ttu-id="d625f-118">运行时如何定位程序集</span><span class="sxs-lookup"><span data-stu-id="d625f-118">How the Runtime Locates Assemblies</span></span>](../../deployment/how-the-runtime-locates-assemblies.md)

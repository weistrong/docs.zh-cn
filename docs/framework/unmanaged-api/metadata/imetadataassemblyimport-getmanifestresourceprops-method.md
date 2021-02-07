---
description: 了解详细信息： IMetaDataAssemblyImport：： GetManifestResourceProps 方法
title: IMetaDataAssemblyImport::GetManifestResourceProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetManifestResourceProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetManifestResourceProps
helpviewer_keywords:
- GetManifestResourceProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetManifestResourceProps method [.NET Framework metadata]
ms.assetid: 00be4789-ac63-4397-b2ec-1629a5c5a585
topic_type:
- apiref
ms.openlocfilehash: d8f390f8eede5153df282cc30479ceff22fb552d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728252"
---
# <a name="imetadataassemblyimportgetmanifestresourceprops-method"></a><span data-ttu-id="c0b8a-103">IMetaDataAssemblyImport::GetManifestResourceProps 方法</span><span class="sxs-lookup"><span data-stu-id="c0b8a-103">IMetaDataAssemblyImport::GetManifestResourceProps Method</span></span>

<span data-ttu-id="c0b8a-104">获取具有指定元数据签名的清单资源的属性集。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-104">Gets the set of properties of the manifest resource with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0b8a-105">语法</span><span class="sxs-lookup"><span data-stu-id="c0b8a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetManifestResourceProps (  
    [in]  mdManifestResource   mdmr,
    [out] LPWSTR               szName,
    [in]  ULONG                cchName,
    [out] ULONG                *pchName,
    [out] mdToken              *ptkImplementation,
    [out] DWORD                *pdwOffset,
    [out] DWORD                *pdwResourceFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0b8a-106">参数</span><span class="sxs-lookup"><span data-stu-id="c0b8a-106">Parameters</span></span>  

 `mdmr`  
 <span data-ttu-id="c0b8a-107">中一个 `mdManifestResource` 标记，表示要获取其属性的资源。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-107">[in] An `mdManifestResource` token that represents the resource for which to get the properties.</span></span>  
  
 `szName`  
 <span data-ttu-id="c0b8a-108">弄资源的名称。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-108">[out] The name of the resource.</span></span>  
  
 `cchName`  
 <span data-ttu-id="c0b8a-109">中的大小（宽字符） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-109">[in] The size, in wide chars, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="c0b8a-110">弄一个指针，指向在中实际返回的宽字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-110">[out] A pointer to the number of wide chars actually returned in `szName`.</span></span>  
  
 `ptkImplementation`  
 <span data-ttu-id="c0b8a-111">弄一个指针，该指针指向 `mdFile` 包含资源的标记或 `mdAssemblyRef` 表示文件或程序集的标记。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-111">[out] A pointer to an `mdFile` token or an `mdAssemblyRef` token that represents the file or assembly, respectively, that contains the resource.</span></span>  
  
 `pdwOffset`  
 <span data-ttu-id="c0b8a-112">弄一个指向值的指针，该值指定文件中资源开始处的偏移量。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-112">[out] A pointer to a value that specifies the offset to the beginning of the resource within the file.</span></span>  
  
 `pdwResourceFlags`  
 <span data-ttu-id="c0b8a-113">弄一个指针，指向用于描述应用于资源的元数据的标志。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-113">[out] A pointer to flags that describe the metadata applied to a resource.</span></span> <span data-ttu-id="c0b8a-114">Flags 值是一个或多个 [CorManifestResourceFlags](cormanifestresourceflags-enumeration.md) 值的组合。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-114">The flags value is a combination of one or more [CorManifestResourceFlags](cormanifestresourceflags-enumeration.md) values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0b8a-115">要求</span><span class="sxs-lookup"><span data-stu-id="c0b8a-115">Requirements</span></span>  

 <span data-ttu-id="c0b8a-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b8a-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0b8a-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c0b8a-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c0b8a-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c0b8a-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c0b8a-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0b8a-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0b8a-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0b8a-120">See also</span></span>

- [<span data-ttu-id="c0b8a-121">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="c0b8a-121">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)

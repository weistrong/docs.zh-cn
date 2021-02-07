---
description: 了解详细信息： IMetaDataAssemblyImport：： EnumManifestResources 方法
title: IMetaDataAssemblyImport::EnumManifestResources 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumManifestResources
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumManifestResources
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumManifestResources method [.NET Framework metadata]
- EnumManifestResources method [.NET Framework metadata]
ms.assetid: 9543b111-5705-40c9-935c-a3ffc7a581aa
topic_type:
- apiref
ms.openlocfilehash: ff819ebb575626af6049558656637e7fabcbc322
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677970"
---
# <a name="imetadataassemblyimportenummanifestresources-method"></a><span data-ttu-id="9249d-103">IMetaDataAssemblyImport::EnumManifestResources 方法</span><span class="sxs-lookup"><span data-stu-id="9249d-103">IMetaDataAssemblyImport::EnumManifestResources Method</span></span>

<span data-ttu-id="9249d-104">获取一个指针，该指针指向当前程序集清单中引用的资源的枚举器。</span><span class="sxs-lookup"><span data-stu-id="9249d-104">Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9249d-105">语法</span><span class="sxs-lookup"><span data-stu-id="9249d-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumManifestResources (  
    [in, out] HCORENUM         *phEnum,
    [out] mdManifestResource   rManifestResources[],
    [in]  ULONG                cMax,
    [out] ULONG                *pcTokens  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="9249d-106">参数</span><span class="sxs-lookup"><span data-stu-id="9249d-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="9249d-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="9249d-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="9249d-108">第一次调用方法时，此值必须为 null 值 `EnumManifestResources` 。</span><span class="sxs-lookup"><span data-stu-id="9249d-108">This must be a null value when the `EnumManifestResources` method is called for the first time.</span></span>  
  
 `rManifestResources`  
 <span data-ttu-id="9249d-109">弄用于存储 `mdManifestResource` 元数据标记的数组。</span><span class="sxs-lookup"><span data-stu-id="9249d-109">[out] The array used to store the `mdManifestResource` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="9249d-110">中可以放入的标记的最大数目 `mdManifestResource` `rManifestResources` 。</span><span class="sxs-lookup"><span data-stu-id="9249d-110">[in] The maximum number of `mdManifestResource` tokens that can be placed in `rManifestResources`.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="9249d-111">弄 `mdManifestResource` 实际置于中的标记数 `rManifestResources` 。</span><span class="sxs-lookup"><span data-stu-id="9249d-111">[out] The number of `mdManifestResource` tokens actually placed in `rManifestResources`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9249d-112">返回值</span><span class="sxs-lookup"><span data-stu-id="9249d-112">Return Value</span></span>  
  
|<span data-ttu-id="9249d-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9249d-113">HRESULT</span></span>|<span data-ttu-id="9249d-114">说明</span><span class="sxs-lookup"><span data-stu-id="9249d-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="9249d-115">`EnumManifestResources` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="9249d-115">`EnumManifestResources` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="9249d-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="9249d-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="9249d-117">在这种情况下， `pcTokens` 设置为零。</span><span class="sxs-lookup"><span data-stu-id="9249d-117">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9249d-118">要求</span><span class="sxs-lookup"><span data-stu-id="9249d-118">Requirements</span></span>  

 <span data-ttu-id="9249d-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9249d-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9249d-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9249d-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9249d-121">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9249d-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9249d-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9249d-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9249d-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="9249d-123">See also</span></span>

- [<span data-ttu-id="9249d-124">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="9249d-124">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)

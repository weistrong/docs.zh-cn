---
description: 了解详细信息： IMetaDataAssemblyImport：： EnumAssemblyRefs 方法
title: IMetaDataAssemblyImport::EnumAssemblyRefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumAssemblyRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumAssemblyRefs
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumAssemblyRefs method [.NET Framework metadata]
- EnumAssemblyRefs method [.NET Framework metadata]
ms.assetid: 8844d0dd-730e-4592-8a7b-c1462d312c70
topic_type:
- apiref
ms.openlocfilehash: fc1d74d79edc21c6d3d13c80510440333d083801
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671051"
---
# <a name="imetadataassemblyimportenumassemblyrefs-method"></a><span data-ttu-id="b358a-103">IMetaDataAssemblyImport::EnumAssemblyRefs 方法</span><span class="sxs-lookup"><span data-stu-id="b358a-103">IMetaDataAssemblyImport::EnumAssemblyRefs Method</span></span>

<span data-ttu-id="b358a-104">枚举 `mdAssemblyRef` 在程序集清单中定义的实例。</span><span class="sxs-lookup"><span data-stu-id="b358a-104">Enumerates the `mdAssemblyRef` instances that are defined in the assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b358a-105">语法</span><span class="sxs-lookup"><span data-stu-id="b358a-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumAssemblyRefs (  
    [in, out] HCORENUM        *phEnum,
    [out]     mdAssemblyRef   rAssemblyRefs[],
    [in]      ULONG           cMax,
    [out]     ULONG           *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b358a-106">参数</span><span class="sxs-lookup"><span data-stu-id="b358a-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="b358a-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="b358a-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="b358a-108">第一次调用方法时，此值必须为 null 值 `EnumAssemblyRefs` 。</span><span class="sxs-lookup"><span data-stu-id="b358a-108">This must be a null value when the `EnumAssemblyRefs` method is called for the first time.</span></span>  
  
 `rAssemblyRefs`  
 <span data-ttu-id="b358a-109">弄 `mdAssemblyRef` 元数据标记的枚举。</span><span class="sxs-lookup"><span data-stu-id="b358a-109">[out] The enumeration of `mdAssemblyRef` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="b358a-110">中可置于数组中的最大标记数 `rAssemblyRefs` 。</span><span class="sxs-lookup"><span data-stu-id="b358a-110">[in] The maximum number of tokens that can be placed in the `rAssemblyRefs` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="b358a-111">弄实际置于中的标记数 `rAssemblyRefs` 。</span><span class="sxs-lookup"><span data-stu-id="b358a-111">[out] The number of tokens actually placed in `rAssemblyRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b358a-112">返回值</span><span class="sxs-lookup"><span data-stu-id="b358a-112">Return Value</span></span>  
  
|<span data-ttu-id="b358a-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b358a-113">HRESULT</span></span>|<span data-ttu-id="b358a-114">说明</span><span class="sxs-lookup"><span data-stu-id="b358a-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="b358a-115">`EnumAssemblyRefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b358a-115">`EnumAssemblyRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="b358a-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="b358a-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="b358a-117">在这种情况下， `pcTokens` 设置为零。</span><span class="sxs-lookup"><span data-stu-id="b358a-117">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b358a-118">要求</span><span class="sxs-lookup"><span data-stu-id="b358a-118">Requirements</span></span>  

 <span data-ttu-id="b358a-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b358a-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b358a-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b358a-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b358a-121">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b358a-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b358a-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b358a-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b358a-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b358a-123">See also</span></span>

- [<span data-ttu-id="b358a-124">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="b358a-124">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)

---
description: 了解详细信息： IMetaDataImport：： EnumTypeRefs 方法
title: IMetaDataImport::EnumTypeRefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeRefs
helpviewer_keywords:
- EnumTypeRefs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeRefs method [.NET Framework metadata]
ms.assetid: b4896b8f-8e97-469c-8089-e72a025661b5
topic_type:
- apiref
ms.openlocfilehash: 1155357e82c08660a852225f0b1a54629cbee0ca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670614"
---
# <a name="imetadataimportenumtyperefs-method"></a><span data-ttu-id="9ea97-103">IMetaDataImport::EnumTypeRefs 方法</span><span class="sxs-lookup"><span data-stu-id="9ea97-103">IMetaDataImport::EnumTypeRefs Method</span></span>

<span data-ttu-id="9ea97-104">枚举当前元数据范围内定义的 TypeRef 标记。</span><span class="sxs-lookup"><span data-stu-id="9ea97-104">Enumerates TypeRef tokens defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ea97-105">语法</span><span class="sxs-lookup"><span data-stu-id="9ea97-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumTypeRefs (  
   [in, out] HCORENUM    *phEnum,
   [out] mdTypeRef       rTypeRefs[],  
   [in]  ULONG           cMax,
   [out] ULONG           *pcTypeRefs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ea97-106">参数</span><span class="sxs-lookup"><span data-stu-id="9ea97-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="9ea97-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="9ea97-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="9ea97-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="9ea97-108">This must be NULL for the first call of this method.</span></span>  
  
 `rTypeRefs`  
 <span data-ttu-id="9ea97-109">弄用于存储 TypeRef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="9ea97-109">[out] The array used to store the TypeRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="9ea97-110">[in] `rTypeRefs` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="9ea97-110">[in] The maximum size of the `rTypeRefs` array.</span></span>  
  
 `pcTypeRefs`  
 <span data-ttu-id="9ea97-111">弄一个指针，指向中返回的 TypeRef 标记的数目 `rTypeRefs` 。</span><span class="sxs-lookup"><span data-stu-id="9ea97-111">[out] A pointer to the number of TypeRef tokens returned in `rTypeRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9ea97-112">返回值</span><span class="sxs-lookup"><span data-stu-id="9ea97-112">Return Value</span></span>  
  
|<span data-ttu-id="9ea97-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9ea97-113">HRESULT</span></span>|<span data-ttu-id="9ea97-114">说明</span><span class="sxs-lookup"><span data-stu-id="9ea97-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="9ea97-115">`EnumTypeRefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="9ea97-115">`EnumTypeRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="9ea97-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="9ea97-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="9ea97-117">在这种情况下， `pcTypeRefs` 为零。</span><span class="sxs-lookup"><span data-stu-id="9ea97-117">In that case, `pcTypeRefs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ea97-118">备注</span><span class="sxs-lookup"><span data-stu-id="9ea97-118">Remarks</span></span>  

 <span data-ttu-id="9ea97-119">TypeRef 标记表示对类型的引用。</span><span class="sxs-lookup"><span data-stu-id="9ea97-119">A TypeRef token represents a reference to a type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ea97-120">要求</span><span class="sxs-lookup"><span data-stu-id="9ea97-120">Requirements</span></span>  

 <span data-ttu-id="9ea97-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea97-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ea97-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9ea97-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9ea97-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9ea97-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9ea97-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ea97-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ea97-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ea97-125">See also</span></span>

- [<span data-ttu-id="9ea97-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="9ea97-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="9ea97-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="9ea97-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

---
description: 了解详细信息： IMetaDataImport：： EnumProperties 方法
title: IMetaDataImport::EnumProperties 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumProperties
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumProperties
helpviewer_keywords:
- IMetaDataImport::EnumProperties method [.NET Framework metadata]
- EnumProperties method [.NET Framework metadata]
ms.assetid: 60573ad7-8821-4721-a068-3f7a6d25926a
topic_type:
- apiref
ms.openlocfilehash: 7503dd14668e8ea4ccf8939e67b91a41db187105
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799351"
---
# <a name="imetadataimportenumproperties-method"></a><span data-ttu-id="dd12d-103">IMetaDataImport::EnumProperties 方法</span><span class="sxs-lookup"><span data-stu-id="dd12d-103">IMetaDataImport::EnumProperties Method</span></span>

<span data-ttu-id="dd12d-104">枚举 PropertyDef 标记，这些标记表示指定的 TypeDef 标记所引用的类型的属性。</span><span class="sxs-lookup"><span data-stu-id="dd12d-104">Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd12d-105">语法</span><span class="sxs-lookup"><span data-stu-id="dd12d-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumProperties (  
   [in, out] HCORENUM    *phEnum,  
   [in]      mdTypeDef   td,  
   [out]     mdProperty  rProperties[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcProperties  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dd12d-106">参数</span><span class="sxs-lookup"><span data-stu-id="dd12d-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="dd12d-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="dd12d-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="dd12d-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="dd12d-108">This must be NULL for the first call of this method.</span></span>  
  
 `td`  
 <span data-ttu-id="dd12d-109">中一个 TypeDef 标记，它表示具有要枚举的属性的类型。</span><span class="sxs-lookup"><span data-stu-id="dd12d-109">[in] A TypeDef token representing the type with properties to enumerate.</span></span>  
  
 `rProperties`  
 <span data-ttu-id="dd12d-110">弄用于存储 PropertyDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="dd12d-110">[out] The array used to store the PropertyDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="dd12d-111">[in] `rProperties` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="dd12d-111">[in] The maximum size of the `rProperties` array.</span></span>  
  
 `pcProperties`  
 <span data-ttu-id="dd12d-112">弄中返回的 PropertyDef 令牌数 `rProperties` 。</span><span class="sxs-lookup"><span data-stu-id="dd12d-112">[out] The number of PropertyDef tokens returned in `rProperties`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dd12d-113">返回值</span><span class="sxs-lookup"><span data-stu-id="dd12d-113">Return Value</span></span>  
  
|<span data-ttu-id="dd12d-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="dd12d-114">HRESULT</span></span>|<span data-ttu-id="dd12d-115">说明</span><span class="sxs-lookup"><span data-stu-id="dd12d-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="dd12d-116">`EnumProperties` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="dd12d-116">`EnumProperties` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="dd12d-117">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="dd12d-117">There are no tokens to enumerate.</span></span> <span data-ttu-id="dd12d-118">在这种情况下， `pcProperties` 为零。</span><span class="sxs-lookup"><span data-stu-id="dd12d-118">In that case, `pcProperties` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="dd12d-119">要求</span><span class="sxs-lookup"><span data-stu-id="dd12d-119">Requirements</span></span>  

 <span data-ttu-id="dd12d-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dd12d-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd12d-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="dd12d-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dd12d-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dd12d-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="dd12d-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd12d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd12d-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="dd12d-124">See also</span></span>

- [<span data-ttu-id="dd12d-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="dd12d-125">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="dd12d-126">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="dd12d-126">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

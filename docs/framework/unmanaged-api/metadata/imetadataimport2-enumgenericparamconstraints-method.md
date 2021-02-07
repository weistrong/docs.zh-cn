---
description: 了解详细信息： IMetaDataImport2：： EnumGenericParamConstraints 方法
title: IMetaDataImport2::EnumGenericParamConstraints 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumGenericParamConstraints
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumGenericParamConstraints
helpviewer_keywords:
- EnumGenericParamConstraints method [.NET Framework metadata]
- IMetaDataImport2::EnumGenericParamConstraints method [.NET Framework metadata]
ms.assetid: 8a7d4e40-28fe-4e14-b801-4049880130e7
topic_type:
- apiref
ms.openlocfilehash: d7ee44059796a943411750b66f5b45034f871a0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677538"
---
# <a name="imetadataimport2enumgenericparamconstraints-method"></a><span data-ttu-id="22aea-103">IMetaDataImport2::EnumGenericParamConstraints 方法</span><span class="sxs-lookup"><span data-stu-id="22aea-103">IMetaDataImport2::EnumGenericParamConstraints Method</span></span>

<span data-ttu-id="22aea-104">获取与指定标记表示的泛型参数关联的泛型参数约束数组的枚举器。</span><span class="sxs-lookup"><span data-stu-id="22aea-104">Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22aea-105">语法</span><span class="sxs-lookup"><span data-stu-id="22aea-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumGenericParamConstraints (  
    [in, out] HCORENUM                *phEnum,  
    [in]  mdGenericParam              tk,  
    [out] mdGenericParamConstraint    rGenericParamConstraints[],  
    [in]  ULONG                       cMax,  
    [out] ULONG                       *pcGenericParamConstraints  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22aea-106">参数</span><span class="sxs-lookup"><span data-stu-id="22aea-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="22aea-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="22aea-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="22aea-108">中  一个标记，表示要枚举其约束的泛型参数。</span><span class="sxs-lookup"><span data-stu-id="22aea-108">[in]   A token that represents the generic parameter whose constraints are to be enumerated.</span></span>  
  
 `rGenericParamConstraints`  
 <span data-ttu-id="22aea-109">弄要枚举的泛型参数约束的数组。</span><span class="sxs-lookup"><span data-stu-id="22aea-109">[out] The array of generic parameter constraints to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="22aea-110">中  要放入的请求的最大数量 `rGenericParamConstraints` 。</span><span class="sxs-lookup"><span data-stu-id="22aea-110">[in]   The requested maximum number of tokens to place in `rGenericParamConstraints`.</span></span>  
  
 `pcGenericParamConstraints`  
 <span data-ttu-id="22aea-111">弄一个指针，指向中放置的标记数 `rGenericParamConstraints` 。</span><span class="sxs-lookup"><span data-stu-id="22aea-111">[out] A pointer to the number of tokens placed in `rGenericParamConstraints`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="22aea-112">返回值</span><span class="sxs-lookup"><span data-stu-id="22aea-112">Return Value</span></span>  
  
|<span data-ttu-id="22aea-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="22aea-113">HRESULT</span></span>|<span data-ttu-id="22aea-114">说明</span><span class="sxs-lookup"><span data-stu-id="22aea-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="22aea-115">`EnumGenericParameterConstraints` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="22aea-115">`EnumGenericParameterConstraints` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="22aea-116">`phEnum` 没有成员元素。</span><span class="sxs-lookup"><span data-stu-id="22aea-116">`phEnum` has no member elements.</span></span> <span data-ttu-id="22aea-117">在这种情况下， `pcGenericParameterConstraints` 设置为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="22aea-117">In this case, `pcGenericParameterConstraints` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="22aea-118">要求</span><span class="sxs-lookup"><span data-stu-id="22aea-118">Requirements</span></span>  

 <span data-ttu-id="22aea-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22aea-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22aea-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="22aea-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="22aea-121">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="22aea-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="22aea-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22aea-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22aea-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="22aea-123">See also</span></span>

- [<span data-ttu-id="22aea-124">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="22aea-124">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="22aea-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="22aea-125">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)

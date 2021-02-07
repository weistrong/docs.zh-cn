---
description: 了解详细信息： IMetaDataImport：： EnumCustomAttributes 方法
title: IMetaDataImport::EnumCustomAttributes 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumCustomAttributes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumCustomAttributes
helpviewer_keywords:
- EnumCustomAttributes method [.NET Framework metadata]
- IMetaDataImport::EnumCustomAttributes method [.NET Framework metadata]
ms.assetid: 798513a0-68b1-4d04-bc5b-782a4445ea68
topic_type:
- apiref
ms.openlocfilehash: 1c55ea4b72483e5dc30425172b95be7f77e8a62a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677582"
---
# <a name="imetadataimportenumcustomattributes-method"></a><span data-ttu-id="033bd-103">IMetaDataImport::EnumCustomAttributes 方法</span><span class="sxs-lookup"><span data-stu-id="033bd-103">IMetaDataImport::EnumCustomAttributes Method</span></span>

<span data-ttu-id="033bd-104">枚举与指定的类型或成员关联的自定义属性定义标记。</span><span class="sxs-lookup"><span data-stu-id="033bd-104">Enumerates custom attribute-definition tokens associated with the specified type or member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="033bd-105">语法</span><span class="sxs-lookup"><span data-stu-id="033bd-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumCustomAttributes (
   [in, out] HCORENUM      *phEnum,  
   [in]  mdToken            tk,
   [in]  mdToken            tkType,
   [out] mdCustomAttribute  rCustomAttributes[],
   [in]  ULONG              cMax,  
   [out, optional] ULONG   *pcCustomAttributes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="033bd-106">参数</span><span class="sxs-lookup"><span data-stu-id="033bd-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="033bd-107">[in，out]指向返回的枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="033bd-107">[in, out] A pointer to the returned enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="033bd-108">中枚举的范围的标记，对于所有自定义特性，则为零。</span><span class="sxs-lookup"><span data-stu-id="033bd-108">[in] A token for the scope of the enumeration, or zero for all custom attributes.</span></span>  
  
 `tkType`  
 <span data-ttu-id="033bd-109">中要枚举的属性类型或所有类型的构造函数的标记 `null` 。</span><span class="sxs-lookup"><span data-stu-id="033bd-109">[in] A token for the constructor of the type of the attributes to be enumerated, or `null` for all types.</span></span>  
  
 `rCustomAttributes`  
 <span data-ttu-id="033bd-110">弄自定义特性标记的数组。</span><span class="sxs-lookup"><span data-stu-id="033bd-110">[out] An array of custom attribute tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="033bd-111">[in] `rCustomAttributes` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="033bd-111">[in] The maximum size of the `rCustomAttributes` array.</span></span>  
  
 `pcCustomAttributes`  
 <span data-ttu-id="033bd-112">[out，optional]返回的令牌值的实际数量 `rCustomAttributes` 。</span><span class="sxs-lookup"><span data-stu-id="033bd-112">[out, optional] The actual number of token values returned in `rCustomAttributes`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="033bd-113">返回值</span><span class="sxs-lookup"><span data-stu-id="033bd-113">Return Value</span></span>  
  
|<span data-ttu-id="033bd-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="033bd-114">HRESULT</span></span>|<span data-ttu-id="033bd-115">说明</span><span class="sxs-lookup"><span data-stu-id="033bd-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="033bd-116">`EnumCustomAttributes` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="033bd-116">`EnumCustomAttributes` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="033bd-117">没有要枚举的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="033bd-117">There are no custom attributes to enumerate.</span></span> <span data-ttu-id="033bd-118">在这种情况下， `pcCustomAttributes` 为零。</span><span class="sxs-lookup"><span data-stu-id="033bd-118">In that case, `pcCustomAttributes` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="033bd-119">要求</span><span class="sxs-lookup"><span data-stu-id="033bd-119">Requirements</span></span>  

 <span data-ttu-id="033bd-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="033bd-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="033bd-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="033bd-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="033bd-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="033bd-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="033bd-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="033bd-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="033bd-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="033bd-124">See also</span></span>

- [<span data-ttu-id="033bd-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="033bd-125">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="033bd-126">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="033bd-126">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

---
description: 了解详细信息： IMetaDataImport：： EnumFieldsWithName 方法
title: IMetaDataImport::EnumFieldsWithName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumFieldsWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumFieldsWithName
helpviewer_keywords:
- IMetaDataImport::EnumFieldsWithName method [.NET Framework metadata]
- EnumFieldsWithName method [.NET Framework metadata]
ms.assetid: 42145e8d-000f-4d0b-ae43-c08201190fa2
topic_type:
- apiref
ms.openlocfilehash: 88096b2b12a9571eb05d4550e6e26a348e28cfd2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799364"
---
# <a name="imetadataimportenumfieldswithname-method"></a><span data-ttu-id="a7442-103">IMetaDataImport::EnumFieldsWithName 方法</span><span class="sxs-lookup"><span data-stu-id="a7442-103">IMetaDataImport::EnumFieldsWithName Method</span></span>

<span data-ttu-id="a7442-104">枚举具有指定名称的指定类型的 FieldDef 标记。</span><span class="sxs-lookup"><span data-stu-id="a7442-104">Enumerates FieldDef tokens of the specified type with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7442-105">语法</span><span class="sxs-lookup"><span data-stu-id="a7442-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumFieldsWithName (  
   [in, out] HCORENUM    *phEnum,
   [in]  mdTypeDef       cl,
   [in]  LPCWSTR         szName,
   [out] mdFieldDef      rFields[],
   [in]  ULONG           cMax,
   [out] ULONG           *pcTokens
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a7442-106">参数</span><span class="sxs-lookup"><span data-stu-id="a7442-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="a7442-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="a7442-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="a7442-108">中要枚举其字段的类型的标记。</span><span class="sxs-lookup"><span data-stu-id="a7442-108">[in] The token of the type whose fields are to be enumerated.</span></span>  
  
 `szName`  
 <span data-ttu-id="a7442-109">中用于限制枚举的作用域的字段名称。</span><span class="sxs-lookup"><span data-stu-id="a7442-109">[in] The field name that limits the scope of the enumeration.</span></span>  
  
 `rFields`  
 <span data-ttu-id="a7442-110">弄用于存储 FieldDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="a7442-110">[out] Array used to store the FieldDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="a7442-111">[in] `rFields` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="a7442-111">[in] The maximum size of the `rFields` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="a7442-112">弄中返回的 FieldDef 令牌的实际数量 `rFields` 。</span><span class="sxs-lookup"><span data-stu-id="a7442-112">[out] The actual number of FieldDef tokens returned in `rFields`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a7442-113">备注</span><span class="sxs-lookup"><span data-stu-id="a7442-113">Remarks</span></span>  

 <span data-ttu-id="a7442-114">与 [IMetaDataImport：： EnumFields](imetadataimport-enumfields-method.md)不同，会 `EnumFieldsWithName` 丢弃所有不具有指定名称的字段标记。</span><span class="sxs-lookup"><span data-stu-id="a7442-114">Unlike [IMetaDataImport::EnumFields](imetadataimport-enumfields-method.md), `EnumFieldsWithName` discards all field tokens that do not have the specified name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a7442-115">返回值</span><span class="sxs-lookup"><span data-stu-id="a7442-115">Return Value</span></span>  
  
|<span data-ttu-id="a7442-116">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a7442-116">HRESULT</span></span>|<span data-ttu-id="a7442-117">说明</span><span class="sxs-lookup"><span data-stu-id="a7442-117">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="a7442-118">`EnumFieldsWithName` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a7442-118">`EnumFieldsWithName` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="a7442-119">没有要枚举的字段。</span><span class="sxs-lookup"><span data-stu-id="a7442-119">There are no fields to enumerate.</span></span> <span data-ttu-id="a7442-120">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="a7442-120">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a7442-121">要求</span><span class="sxs-lookup"><span data-stu-id="a7442-121">Requirements</span></span>  

 <span data-ttu-id="a7442-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a7442-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7442-123">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a7442-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a7442-124">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a7442-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a7442-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7442-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7442-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="a7442-126">See also</span></span>

- [<span data-ttu-id="a7442-127">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="a7442-127">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="a7442-128">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="a7442-128">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

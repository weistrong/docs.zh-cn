---
description: 了解详细信息： IMetaDataImport：： EnumFields 方法
title: IMetaDataImport::EnumFields 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumFields
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumFields
helpviewer_keywords:
- EnumFields method [.NET Framework metadata]
- IMetaDataImport::EnumFields method [.NET Framework metadata]
ms.assetid: 1d23247e-c58c-45db-afd8-83aa89cde18e
topic_type:
- apiref
ms.openlocfilehash: 5cb9b3a47dc4c51b9eba24b9519e4b97846c1a6d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799377"
---
# <a name="imetadataimportenumfields-method"></a><span data-ttu-id="3f0fd-103">IMetaDataImport::EnumFields 方法</span><span class="sxs-lookup"><span data-stu-id="3f0fd-103">IMetaDataImport::EnumFields Method</span></span>

<span data-ttu-id="3f0fd-104">枚举指定的 TypeDef 标记所引用的类型的 FieldDef 标记。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-104">Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f0fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="3f0fd-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumFields (
   [in, out] HCORENUM    *phEnum,
   [in]      mdTypeDef   cl,
   [out]     mdFieldDef  rFields[],
   [in]      ULONG       cMax,
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3f0fd-106">参数</span><span class="sxs-lookup"><span data-stu-id="3f0fd-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="3f0fd-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="3f0fd-108">中要枚举其字段的类的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-108">[in] The TypeDef token of the class whose fields are to be enumerated.</span></span>  
  
 `rFields`  
 <span data-ttu-id="3f0fd-109">弄FieldDef 标记的列表。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-109">[out] The list of FieldDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="3f0fd-110">[in] `rFields` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-110">[in] The maximum size of the `rFields` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="3f0fd-111">弄中返回的 FieldDef 令牌的实际数量 `rFields` 。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-111">[out] The actual number of FieldDef tokens returned in `rFields`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3f0fd-112">返回值</span><span class="sxs-lookup"><span data-stu-id="3f0fd-112">Return Value</span></span>  
  
|<span data-ttu-id="3f0fd-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3f0fd-113">HRESULT</span></span>|<span data-ttu-id="3f0fd-114">说明</span><span class="sxs-lookup"><span data-stu-id="3f0fd-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="3f0fd-115">`EnumFields` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-115">`EnumFields` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="3f0fd-116">没有要枚举的字段。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-116">There are no fields to enumerate.</span></span> <span data-ttu-id="3f0fd-117">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-117">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3f0fd-118">要求</span><span class="sxs-lookup"><span data-stu-id="3f0fd-118">Requirements</span></span>  

 <span data-ttu-id="3f0fd-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f0fd-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f0fd-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3f0fd-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3f0fd-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3f0fd-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3f0fd-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f0fd-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f0fd-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f0fd-123">See also</span></span>

- [<span data-ttu-id="3f0fd-124">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="3f0fd-124">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="3f0fd-125">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="3f0fd-125">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

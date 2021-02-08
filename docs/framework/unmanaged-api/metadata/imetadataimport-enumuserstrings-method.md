---
description: 了解详细信息： IMetaDataImport：： EnumUserStrings 方法
title: IMetaDataImport::EnumUserStrings 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUserStrings
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUserStrings
helpviewer_keywords:
- IMetaDataImport::EnumUserStrings method [.NET Framework metadata]
- EnumUserStrings method [.NET Framework metadata]
ms.assetid: 2b1f1418-4be8-4cdb-b418-b3abccc527a7
topic_type:
- apiref
ms.openlocfilehash: a4ead696f3d924fef9ebfed5c4f1eb97eb13e14e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799312"
---
# <a name="imetadataimportenumuserstrings-method"></a><span data-ttu-id="396b4-103">IMetaDataImport::EnumUserStrings 方法</span><span class="sxs-lookup"><span data-stu-id="396b4-103">IMetaDataImport::EnumUserStrings Method</span></span>

<span data-ttu-id="396b4-104">枚举表示当前元数据范围内的硬编码字符串的 String 标记。</span><span class="sxs-lookup"><span data-stu-id="396b4-104">Enumerates String tokens representing hard-coded strings in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="396b4-105">语法</span><span class="sxs-lookup"><span data-stu-id="396b4-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumUserStrings (  
   [in, out]  HCORENUM    *phEnum,  
   [out]  mdString        rStrings[],  
   [in]   ULONG           cMax,  
   [out]  ULONG           *pcStrings  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="396b4-106">参数</span><span class="sxs-lookup"><span data-stu-id="396b4-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="396b4-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="396b4-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="396b4-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="396b4-108">This must be NULL for the first call of this method.</span></span>  
  
 `rStrings`  
 <span data-ttu-id="396b4-109">弄用于存储字符串标记的数组。</span><span class="sxs-lookup"><span data-stu-id="396b4-109">[out] The array used to store the String tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="396b4-110">[in] `rStrings` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="396b4-110">[in] The maximum size of the `rStrings` array.</span></span>  
  
 `pcStrings`  
 <span data-ttu-id="396b4-111">弄中返回的字符串标记的数目 `rStrings` 。</span><span class="sxs-lookup"><span data-stu-id="396b4-111">[out] The number of String tokens returned in `rStrings`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="396b4-112">返回值</span><span class="sxs-lookup"><span data-stu-id="396b4-112">Return Value</span></span>  
  
|<span data-ttu-id="396b4-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="396b4-113">HRESULT</span></span>|<span data-ttu-id="396b4-114">说明</span><span class="sxs-lookup"><span data-stu-id="396b4-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="396b4-115">`EnumUserStrings` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="396b4-115">`EnumUserStrings` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="396b4-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="396b4-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="396b4-117">在这种情况下， `pcStrings` 为零。</span><span class="sxs-lookup"><span data-stu-id="396b4-117">In that case, `pcStrings` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="396b4-118">备注</span><span class="sxs-lookup"><span data-stu-id="396b4-118">Remarks</span></span>  

 <span data-ttu-id="396b4-119">字符串标记由 [IMetaDataEmit：:D efineuserstring](imetadataemit-defineuserstring-method.md) 方法创建。</span><span class="sxs-lookup"><span data-stu-id="396b4-119">The String tokens are created by the [IMetaDataEmit::DefineUserString](imetadataemit-defineuserstring-method.md) method.</span></span> <span data-ttu-id="396b4-120">此方法旨在由元数据浏览器而不是编译器使用。</span><span class="sxs-lookup"><span data-stu-id="396b4-120">This method is designed to be used by a metadata browser rather than by a compiler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="396b4-121">要求</span><span class="sxs-lookup"><span data-stu-id="396b4-121">Requirements</span></span>  

 <span data-ttu-id="396b4-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="396b4-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="396b4-123">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="396b4-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="396b4-124">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="396b4-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="396b4-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="396b4-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="396b4-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="396b4-126">See also</span></span>

- [<span data-ttu-id="396b4-127">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="396b4-127">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="396b4-128">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="396b4-128">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

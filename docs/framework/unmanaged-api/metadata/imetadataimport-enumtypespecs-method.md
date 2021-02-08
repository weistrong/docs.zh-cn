---
description: 了解详细信息： IMetaDataImport：： EnumTypeSpecs 方法
title: IMetaDataImport::EnumTypeSpecs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeSpecs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeSpecs
helpviewer_keywords:
- EnumTypeSpecs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeSpecs method [.NET Framework metadata]
ms.assetid: 75331c7b-988b-436c-9eb9-a270d37b4f06
topic_type:
- apiref
ms.openlocfilehash: 7446bbf3296ffb6cfa3a20f594b4a7da22acff5c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799338"
---
# <a name="imetadataimportenumtypespecs-method"></a><span data-ttu-id="17bac-103">IMetaDataImport::EnumTypeSpecs 方法</span><span class="sxs-lookup"><span data-stu-id="17bac-103">IMetaDataImport::EnumTypeSpecs Method</span></span>

<span data-ttu-id="17bac-104">枚举当前元数据范围内定义的 TypeSpec 标记。</span><span class="sxs-lookup"><span data-stu-id="17bac-104">Enumerates TypeSpec tokens defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17bac-105">语法</span><span class="sxs-lookup"><span data-stu-id="17bac-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumTypeSpecs (  
   [in, out] HCORENUM    *phEnum,  
   [out] mdTypeSpec      rTypeSpecs[],  
   [in]  ULONG           cMax,  
   [out] ULONG           *pcTypeSpecs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17bac-106">参数</span><span class="sxs-lookup"><span data-stu-id="17bac-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="17bac-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="17bac-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="17bac-108">此方法的第一次调用时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="17bac-108">This value must be NULL for the first call of this method.</span></span>  
  
 `rTypeSpecs`  
 <span data-ttu-id="17bac-109">弄用于存储 TypeSpec 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="17bac-109">[out] The array used to store the TypeSpec tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="17bac-110">[in] `rTypeSpecs` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="17bac-110">[in] The maximum size of the `rTypeSpecs` array.</span></span>  
  
 `pcTypeSpecs`  
 <span data-ttu-id="17bac-111">弄中返回的 TypeSpec 标记的数目 `rTypeSpecs` 。</span><span class="sxs-lookup"><span data-stu-id="17bac-111">[out] The number of TypeSpec tokens returned in `rTypeSpecs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="17bac-112">返回值</span><span class="sxs-lookup"><span data-stu-id="17bac-112">Return Value</span></span>  
  
|<span data-ttu-id="17bac-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="17bac-113">HRESULT</span></span>|<span data-ttu-id="17bac-114">说明</span><span class="sxs-lookup"><span data-stu-id="17bac-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="17bac-115">`EnumTypeSpecs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="17bac-115">`EnumTypeSpecs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="17bac-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="17bac-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="17bac-117">在这种情况下， `pcTypeSpecs` 为零。</span><span class="sxs-lookup"><span data-stu-id="17bac-117">In that case, `pcTypeSpecs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="17bac-118">备注</span><span class="sxs-lookup"><span data-stu-id="17bac-118">Remarks</span></span>  

 <span data-ttu-id="17bac-119">TypeSpec 标记由 [IMetaDataEmit：： GetTokenFromTypeSpec](imetadataemit-gettokenfromtypespec-method.md) 方法创建。</span><span class="sxs-lookup"><span data-stu-id="17bac-119">The TypeSpec tokens are created by the [IMetaDataEmit::GetTokenFromTypeSpec](imetadataemit-gettokenfromtypespec-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17bac-120">要求</span><span class="sxs-lookup"><span data-stu-id="17bac-120">Requirements</span></span>  

 <span data-ttu-id="17bac-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="17bac-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17bac-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="17bac-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="17bac-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="17bac-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="17bac-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17bac-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17bac-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="17bac-125">See also</span></span>

- [<span data-ttu-id="17bac-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="17bac-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="17bac-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="17bac-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

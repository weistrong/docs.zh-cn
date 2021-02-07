---
description: 了解详细信息： IMetaDataImport：： EnumMethodImpls 方法
title: IMetaDataImport::EnumMethodImpls 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethodImpls
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethodImpls
helpviewer_keywords:
- EnumMethodImpls method [.NET Framework metadata]
- IMetaDataImport::EnumMethodImpls method [.NET Framework metadata]
ms.assetid: 4e0f865d-88b5-44bd-be35-492622e5e08e
topic_type:
- apiref
ms.openlocfilehash: 3ae5795bdde36ad07c447370553e24e1ceacf493
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670690"
---
# <a name="imetadataimportenummethodimpls-method"></a><span data-ttu-id="cf780-103">IMetaDataImport::EnumMethodImpls 方法</span><span class="sxs-lookup"><span data-stu-id="cf780-103">IMetaDataImport::EnumMethodImpls Method</span></span>

<span data-ttu-id="cf780-104">枚举表示指定类型的方法的 MethodBody 和 MethodDeclaration 标记。</span><span class="sxs-lookup"><span data-stu-id="cf780-104">Enumerates MethodBody and MethodDeclaration tokens representing methods of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf780-105">语法</span><span class="sxs-lookup"><span data-stu-id="cf780-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMethodImpls (  
   [in, out] HCORENUM    *phEnum,
   [in]      mdTypeDef   td,
   [out]     mdToken     rMethodBody[],
   [out]     mdToken     rMethodDecl[],
   [in]      ULONG       cMax,
   [in]      ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cf780-106">参数</span><span class="sxs-lookup"><span data-stu-id="cf780-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="cf780-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="cf780-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="cf780-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="cf780-108">This must be NULL for the first call of this method.</span></span>  
  
 `td`  
 <span data-ttu-id="cf780-109">中要枚举其方法实现的类型的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="cf780-109">[in] A TypeDef token for the type whose method implementations to enumerate.</span></span>  
  
 `rMethodBody`  
 <span data-ttu-id="cf780-110">弄用于存储 MethodBody 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="cf780-110">[out] The array to store the MethodBody tokens.</span></span>  
  
 `rMethodDecl`  
 <span data-ttu-id="cf780-111">弄用于存储 MethodDeclaration 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="cf780-111">[out] The array to store the MethodDeclaration tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="cf780-112">中和数组的最大 `rMethodBody` 大小 `rMethodDecl` 。</span><span class="sxs-lookup"><span data-stu-id="cf780-112">[in] The maximum size of the `rMethodBody` and `rMethodDecl` arrays.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="cf780-113">中和中返回的实际方法数 `rMethodBody` `rMethodDecl` 。</span><span class="sxs-lookup"><span data-stu-id="cf780-113">[in] The actual number of methods returned in `rMethodBody` and `rMethodDecl`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cf780-114">返回值</span><span class="sxs-lookup"><span data-stu-id="cf780-114">Return Value</span></span>  
  
|<span data-ttu-id="cf780-115">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cf780-115">HRESULT</span></span>|<span data-ttu-id="cf780-116">说明</span><span class="sxs-lookup"><span data-stu-id="cf780-116">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="cf780-117">`EnumMethodImpls` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="cf780-117">`EnumMethodImpls` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="cf780-118">没有要枚举的方法标记。</span><span class="sxs-lookup"><span data-stu-id="cf780-118">There are no method tokens to enumerate.</span></span> <span data-ttu-id="cf780-119">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="cf780-119">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cf780-120">要求</span><span class="sxs-lookup"><span data-stu-id="cf780-120">Requirements</span></span>  

 <span data-ttu-id="cf780-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cf780-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf780-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="cf780-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cf780-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cf780-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cf780-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf780-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf780-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="cf780-125">See also</span></span>

- [<span data-ttu-id="cf780-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="cf780-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="cf780-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="cf780-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

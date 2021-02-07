---
description: 了解详细信息： IMetaDataImport：： EnumMethods 方法
title: IMetaDataImport::EnumMethods 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethods
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethods
helpviewer_keywords:
- IMetaDataImport::EnumMethods method [.NET Framework metadata]
- EnumMethods method [.NET Framework metadata]
ms.assetid: 8cc3b0c3-d97d-4f71-9e7d-ef2a92b4959a
topic_type:
- apiref
ms.openlocfilehash: 4fce3593d088a8d401335869eb49e598ac4c3fd2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670668"
---
# <a name="imetadataimportenummethods-method"></a><span data-ttu-id="3755f-103">IMetaDataImport::EnumMethods 方法</span><span class="sxs-lookup"><span data-stu-id="3755f-103">IMetaDataImport::EnumMethods Method</span></span>

<span data-ttu-id="3755f-104">枚举表示指定类型的方法的 MethodDef 标记。</span><span class="sxs-lookup"><span data-stu-id="3755f-104">Enumerates MethodDef tokens representing methods of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3755f-105">语法</span><span class="sxs-lookup"><span data-stu-id="3755f-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMethods (  
   [in, out] HCORENUM   *phEnum,
   [in]  mdTypeDef      cl,
   [out] mdMethodDef    rMethods[],
   [in]  ULONG          cMax,
   [out] ULONG          *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3755f-106">参数</span><span class="sxs-lookup"><span data-stu-id="3755f-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="3755f-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="3755f-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="3755f-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="3755f-108">This must be NULL for the first call of this method.</span></span>  
  
 `cl`  
 <span data-ttu-id="3755f-109">中一个 TypeDef 标记，它表示具有要枚举的方法的类型。</span><span class="sxs-lookup"><span data-stu-id="3755f-109">[in] A TypeDef token representing the type with the methods to enumerate.</span></span>  
  
 `rMethods`  
 <span data-ttu-id="3755f-110">弄用于存储 MethodDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="3755f-110">[out] The array to store the MethodDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="3755f-111">中MethodDef 数组的最大大小 `rMethods` 。</span><span class="sxs-lookup"><span data-stu-id="3755f-111">[in] The maximum size of the MethodDef `rMethods` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="3755f-112">弄中返回的 MethodDef 标记的数目 `rMethods` 。</span><span class="sxs-lookup"><span data-stu-id="3755f-112">[out] The number of MethodDef tokens returned in `rMethods`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3755f-113">返回值</span><span class="sxs-lookup"><span data-stu-id="3755f-113">Return Value</span></span>  
  
|<span data-ttu-id="3755f-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3755f-114">HRESULT</span></span>|<span data-ttu-id="3755f-115">说明</span><span class="sxs-lookup"><span data-stu-id="3755f-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="3755f-116">`EnumMethods` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="3755f-116">`EnumMethods` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="3755f-117">没有要枚举的 MethodDef 标记。</span><span class="sxs-lookup"><span data-stu-id="3755f-117">There are no MethodDef tokens to enumerate.</span></span> <span data-ttu-id="3755f-118">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="3755f-118">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3755f-119">要求</span><span class="sxs-lookup"><span data-stu-id="3755f-119">Requirements</span></span>  

 <span data-ttu-id="3755f-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3755f-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3755f-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3755f-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3755f-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3755f-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3755f-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3755f-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3755f-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="3755f-124">See also</span></span>

- [<span data-ttu-id="3755f-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="3755f-125">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="3755f-126">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="3755f-126">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

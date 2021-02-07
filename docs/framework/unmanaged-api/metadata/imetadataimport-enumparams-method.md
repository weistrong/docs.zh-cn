---
description: 了解详细信息： IMetaDataImport：： EnumParams 方法
title: IMetaDataImport::EnumParams 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumParams
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumParams
helpviewer_keywords:
- IMetaDataImport::EnumParams method [.NET Framework metadata]
- EnumParams method [.NET Framework metadata]
ms.assetid: 52118dc9-fe6e-4b39-aa48-c3cc3ea4214d
topic_type:
- apiref
ms.openlocfilehash: 3402e0277631cb54232269ad96194583cc466c4d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688788"
---
# <a name="imetadataimportenumparams-method"></a><span data-ttu-id="64674-103">IMetaDataImport::EnumParams 方法</span><span class="sxs-lookup"><span data-stu-id="64674-103">IMetaDataImport::EnumParams Method</span></span>

<span data-ttu-id="64674-104">枚举 ParamDef 标记，这些标记表示指定的 MethodDef 标记所引用的方法的参数。</span><span class="sxs-lookup"><span data-stu-id="64674-104">Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64674-105">语法</span><span class="sxs-lookup"><span data-stu-id="64674-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumParams (  
   [in, out] HCORENUM    *phEnum,  
   [in]  mdMethodDef     mb,  
   [out] mdParamDef      rParams[],  
   [in]  ULONG           cMax,  
   [out] ULONG          *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="64674-106">参数</span><span class="sxs-lookup"><span data-stu-id="64674-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="64674-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="64674-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="64674-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="64674-108">This must be NULL for the first call of this method.</span></span>  
  
 `mb`  
 <span data-ttu-id="64674-109">中一个 MethodDef 标记，它表示具有要枚举的参数的方法。</span><span class="sxs-lookup"><span data-stu-id="64674-109">[in] A MethodDef token representing the method with the parameters to enumerate.</span></span>  
  
 `rParams`  
 <span data-ttu-id="64674-110">弄用于存储 ParamDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="64674-110">[out] The array used to store the ParamDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="64674-111">[in] `rParams` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="64674-111">[in] The maximum size of the `rParams` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="64674-112">弄中返回的 ParamDef 令牌数 `rParams` 。</span><span class="sxs-lookup"><span data-stu-id="64674-112">[out] The number of ParamDef tokens returned in `rParams`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="64674-113">返回值</span><span class="sxs-lookup"><span data-stu-id="64674-113">Return Value</span></span>  
  
|<span data-ttu-id="64674-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="64674-114">HRESULT</span></span>|<span data-ttu-id="64674-115">说明</span><span class="sxs-lookup"><span data-stu-id="64674-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="64674-116">`EnumParams` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="64674-116">`EnumParams` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="64674-117">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="64674-117">There are no tokens to enumerate.</span></span> <span data-ttu-id="64674-118">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="64674-118">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="64674-119">要求</span><span class="sxs-lookup"><span data-stu-id="64674-119">Requirements</span></span>  

 <span data-ttu-id="64674-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="64674-120">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64674-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="64674-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="64674-122">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="64674-122">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="64674-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64674-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64674-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="64674-124">See also</span></span>

- [<span data-ttu-id="64674-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="64674-125">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="64674-126">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="64674-126">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

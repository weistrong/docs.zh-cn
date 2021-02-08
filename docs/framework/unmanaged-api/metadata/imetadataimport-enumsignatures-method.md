---
description: 了解详细信息： IMetaDataImport：： EnumSignatures 方法
title: IMetaDataImport::EnumSignatures 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumSignatures
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumSignatures
helpviewer_keywords:
- EnumSignatures method [.NET Framework metadata]
- IMetaDataImport::EnumSignatures method [.NET Framework metadata]
ms.assetid: d0d65060-6f90-42a2-95cf-6ffb04352996
topic_type:
- apiref
ms.openlocfilehash: ed41dd42151791e3d27950f30b10d91217ad7e7a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771621"
---
# <a name="imetadataimportenumsignatures-method"></a><span data-ttu-id="ce1b3-103">IMetaDataImport::EnumSignatures 方法</span><span class="sxs-lookup"><span data-stu-id="ce1b3-103">IMetaDataImport::EnumSignatures Method</span></span>

<span data-ttu-id="ce1b3-104">枚举当前范围内表示独立签名的 Signature 标记。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-104">Enumerates Signature tokens representing stand-alone signatures in the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce1b3-105">语法</span><span class="sxs-lookup"><span data-stu-id="ce1b3-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumSignatures (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdSignature  rSignatures[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcSignatures  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce1b3-106">参数</span><span class="sxs-lookup"><span data-stu-id="ce1b3-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="ce1b3-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="ce1b3-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-108">This must be NULL for the first call of this method.</span></span>  
  
 `rSignatures`  
 <span data-ttu-id="ce1b3-109">弄用于存储签名令牌的数组。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-109">[out] The array used to store the Signature tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="ce1b3-110">[in] `rSignatures` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-110">[in] The maximum size of the `rSignatures` array.</span></span>  
  
 `pcSignatures`  
 <span data-ttu-id="ce1b3-111">弄中返回的签名令牌数 `rSignatures` 。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-111">[out] The number of Signature tokens returned in `rSignatures`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ce1b3-112">返回值</span><span class="sxs-lookup"><span data-stu-id="ce1b3-112">Return Value</span></span>  
  
|<span data-ttu-id="ce1b3-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ce1b3-113">HRESULT</span></span>|<span data-ttu-id="ce1b3-114">说明</span><span class="sxs-lookup"><span data-stu-id="ce1b3-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="ce1b3-115">`EnumSignatures` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-115">`EnumSignatures` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="ce1b3-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="ce1b3-117">在这种情况下， `pcSignatures` 为零。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-117">In that case, `pcSignatures` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ce1b3-118">备注</span><span class="sxs-lookup"><span data-stu-id="ce1b3-118">Remarks</span></span>  

 <span data-ttu-id="ce1b3-119">签名令牌由 [IMetaDataEmit：： GetTokenFromSig](imetadataemit-gettokenfromsig-method.md) 方法创建。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-119">The Signature tokens are created by the [IMetaDataEmit::GetTokenFromSig](imetadataemit-gettokenfromsig-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce1b3-120">要求</span><span class="sxs-lookup"><span data-stu-id="ce1b3-120">Requirements</span></span>  

 <span data-ttu-id="ce1b3-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ce1b3-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce1b3-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ce1b3-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ce1b3-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ce1b3-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ce1b3-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce1b3-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce1b3-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="ce1b3-125">See also</span></span>

- [<span data-ttu-id="ce1b3-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="ce1b3-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="ce1b3-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="ce1b3-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

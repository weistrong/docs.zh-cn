---
description: 了解详细信息： IMetaDataImport：： EnumMembersWithName 方法
title: IMetaDataImport::EnumMembersWithName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMembersWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMembersWithName
helpviewer_keywords:
- IMetaDataImport::EnumMembersWithName method [.NET Framework metadata]
- EnumMembersWithName method [.NET Framework metadata]
ms.assetid: 7c9e9120-3104-42f0-86ce-19a025f20dcc
topic_type:
- apiref
ms.openlocfilehash: bb6d8f0769029dccaf1f52dd211c67d47bf32a73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670757"
---
# <a name="imetadataimportenummemberswithname-method"></a><span data-ttu-id="79af5-103">IMetaDataImport::EnumMembersWithName 方法</span><span class="sxs-lookup"><span data-stu-id="79af5-103">IMetaDataImport::EnumMembersWithName Method</span></span>

<span data-ttu-id="79af5-104">枚举表示具有指定名称的指定类型的成员的 MemberDef 标记。</span><span class="sxs-lookup"><span data-stu-id="79af5-104">Enumerates MemberDef tokens representing members of the specified type with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79af5-105">语法</span><span class="sxs-lookup"><span data-stu-id="79af5-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMembersWithName (  
   [in, out] HCORENUM    *phEnum,
   [in]      mdTypeDef   cl,
   [in]      LPCWSTR     szName,
   [out]     mdToken     rMembers[],
   [in]      ULONG       cMax,
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79af5-106">参数</span><span class="sxs-lookup"><span data-stu-id="79af5-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="79af5-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="79af5-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="79af5-108">中一个 TypeDef 标记，它表示具有要枚举的成员的类型。</span><span class="sxs-lookup"><span data-stu-id="79af5-108">[in] A TypeDef token representing the type with members to enumerate.</span></span>  
  
 `szName`  
 <span data-ttu-id="79af5-109">中限制枚举器范围的成员名称。</span><span class="sxs-lookup"><span data-stu-id="79af5-109">[in] The member name that limits the scope of the enumerator.</span></span>  
  
 `rMembers`  
 <span data-ttu-id="79af5-110">弄用于存储 MemberDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="79af5-110">[out] The array used to store the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="79af5-111">[in] `rMembers` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="79af5-111">[in] The maximum size of the `rMembers` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="79af5-112">弄中返回的 MemberDef 令牌的实际数量 `rMembers` 。</span><span class="sxs-lookup"><span data-stu-id="79af5-112">[out] The actual number of MemberDef tokens returned in `rMembers`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79af5-113">备注</span><span class="sxs-lookup"><span data-stu-id="79af5-113">Remarks</span></span>  

 <span data-ttu-id="79af5-114">此方法枚举字段和方法，而不是属性或事件。</span><span class="sxs-lookup"><span data-stu-id="79af5-114">This method enumerates fields and methods, but not properties or events.</span></span> <span data-ttu-id="79af5-115">与 [IMetaDataImport：： EnumMembers](imetadataimport-enummembers-method.md)不同，会 `EnumMembersWithName` 丢弃所有不具有指定名称的字段和成员标记。</span><span class="sxs-lookup"><span data-stu-id="79af5-115">Unlike [IMetaDataImport::EnumMembers](imetadataimport-enummembers-method.md), `EnumMembersWithName` discards all field and member tokens that do not have the specified name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="79af5-116">返回值</span><span class="sxs-lookup"><span data-stu-id="79af5-116">Return Value</span></span>  
  
|<span data-ttu-id="79af5-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="79af5-117">HRESULT</span></span>|<span data-ttu-id="79af5-118">说明</span><span class="sxs-lookup"><span data-stu-id="79af5-118">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="79af5-119">`EnumTypeDefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="79af5-119">`EnumTypeDefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="79af5-120">没有要枚举的 MemberDef 令牌。</span><span class="sxs-lookup"><span data-stu-id="79af5-120">There are no MemberDef tokens to enumerate.</span></span> <span data-ttu-id="79af5-121">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="79af5-121">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="79af5-122">要求</span><span class="sxs-lookup"><span data-stu-id="79af5-122">Requirements</span></span>  

 <span data-ttu-id="79af5-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79af5-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79af5-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="79af5-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="79af5-125">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="79af5-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="79af5-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79af5-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79af5-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="79af5-127">See also</span></span>

- [<span data-ttu-id="79af5-128">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="79af5-128">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="79af5-129">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="79af5-129">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

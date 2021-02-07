---
description: 了解详细信息： IMetaDataImport：： EnumMemberRefs 方法
title: IMetaDataImport::EnumMemberRefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMemberRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMemberRefs
helpviewer_keywords:
- EnumMemberRefs method [.NET Framework metadata]
- IMetaDataImport::EnumMemberRefs method [.NET Framework metadata]
ms.assetid: e97c97a6-6e4f-41f5-9af1-9b3cf3bdbd6b
topic_type:
- apiref
ms.openlocfilehash: 0c9b10342f73ae5b604ac25b6ff8ccec58deb5ab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670939"
---
# <a name="imetadataimportenummemberrefs-method"></a><span data-ttu-id="1b861-103">IMetaDataImport::EnumMemberRefs 方法</span><span class="sxs-lookup"><span data-stu-id="1b861-103">IMetaDataImport::EnumMemberRefs Method</span></span>

<span data-ttu-id="1b861-104">枚举表示指定类型成员的 MemberRef 标记。</span><span class="sxs-lookup"><span data-stu-id="1b861-104">Enumerates MemberRef tokens representing members of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b861-105">语法</span><span class="sxs-lookup"><span data-stu-id="1b861-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMemberRefs (  
   [in, out] HCORENUM    *phEnum,
   [in]   mdToken        tkParent,
   [out]  mdMemberRef    rMemberRefs[],
   [in]   ULONG          cMax,
   [out]  ULONG          *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1b861-106">参数</span><span class="sxs-lookup"><span data-stu-id="1b861-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="1b861-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="1b861-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `tkParent`  
 <span data-ttu-id="1b861-108">中要枚举其成员的类型的 TypeDef、TypeRef、MethodDef 或 ModuleRef 标记。</span><span class="sxs-lookup"><span data-stu-id="1b861-108">[in] A TypeDef, TypeRef, MethodDef, or ModuleRef token for the type whose members are to be enumerated.</span></span>  
  
 `rMemberRefs`  
 <span data-ttu-id="1b861-109">弄用于存储 MemberRef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="1b861-109">[out] The array used to store MemberRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="1b861-110">[in] `rMemberRefs` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="1b861-110">[in] The maximum size of the `rMemberRefs` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="1b861-111">弄中返回的 MemberRef 标记的实际数量 `rMemberRefs` 。</span><span class="sxs-lookup"><span data-stu-id="1b861-111">[out] The actual number of MemberRef tokens returned in `rMemberRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1b861-112">返回值</span><span class="sxs-lookup"><span data-stu-id="1b861-112">Return Value</span></span>  
  
|<span data-ttu-id="1b861-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1b861-113">HRESULT</span></span>|<span data-ttu-id="1b861-114">说明</span><span class="sxs-lookup"><span data-stu-id="1b861-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="1b861-115">`EnumMemberRefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="1b861-115">`EnumMemberRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="1b861-116">没有要枚举的 MemberRef 标记。</span><span class="sxs-lookup"><span data-stu-id="1b861-116">There are no MemberRef tokens to enumerate.</span></span> <span data-ttu-id="1b861-117">在这种情况下， `pcTokens` 将为零。</span><span class="sxs-lookup"><span data-stu-id="1b861-117">In that case, `pcTokens` is to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1b861-118">要求</span><span class="sxs-lookup"><span data-stu-id="1b861-118">Requirements</span></span>  

 <span data-ttu-id="1b861-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1b861-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b861-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1b861-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1b861-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1b861-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1b861-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b861-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b861-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="1b861-123">See also</span></span>

- [<span data-ttu-id="1b861-124">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="1b861-124">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="1b861-125">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="1b861-125">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

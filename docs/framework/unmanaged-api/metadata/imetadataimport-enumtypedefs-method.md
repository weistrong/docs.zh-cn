---
description: 了解详细信息： IMetaDataImport：： EnumTypeDefs 方法
title: IMetaDataImport::EnumTypeDefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeDefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeDefs
helpviewer_keywords:
- EnumTypeDefs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeDefs method [.NET Framework metadata]
ms.assetid: 4e508711-da92-4381-aaf8-6803075cdaa2
topic_type:
- apiref
ms.openlocfilehash: 28bd06b70573b780b687da9de0e13e17c29bb39a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670666"
---
# <a name="imetadataimportenumtypedefs-method"></a><span data-ttu-id="d9904-103">IMetaDataImport::EnumTypeDefs 方法</span><span class="sxs-lookup"><span data-stu-id="d9904-103">IMetaDataImport::EnumTypeDefs Method</span></span>

<span data-ttu-id="d9904-104">枚举表示当前范围内的所有类型的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="d9904-104">Enumerates TypeDef tokens representing all types within the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9904-105">语法</span><span class="sxs-lookup"><span data-stu-id="d9904-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumTypeDefs (  
   [out] HCORENUM   *phEnum,
   [in]  mdTypeDef  rTypeDefs[],  
   [in]  ULONG      cMax,
   [out] ULONG      *pcTypeDefs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9904-106">参数</span><span class="sxs-lookup"><span data-stu-id="d9904-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="d9904-107">弄指向新枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="d9904-107">[out] A pointer to the new enumerator.</span></span> <span data-ttu-id="d9904-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="d9904-108">This must be NULL for the first call of this method.</span></span>  
  
 `rTypeDefs`  
 <span data-ttu-id="d9904-109">中用于存储 TypeDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="d9904-109">[in] The array used to store the TypeDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="d9904-110">[in] `rTypeDefs` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="d9904-110">[in] The maximum size of the `rTypeDefs` array.</span></span>  
  
 `pcTypeDefs`  
 <span data-ttu-id="d9904-111">弄中返回的 TypeDef 标记的数目 `rTypeDefs` 。</span><span class="sxs-lookup"><span data-stu-id="d9904-111">[out] The number of TypeDef tokens returned in `rTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d9904-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d9904-112">Return Value</span></span>  
  
|<span data-ttu-id="d9904-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d9904-113">HRESULT</span></span>|<span data-ttu-id="d9904-114">说明</span><span class="sxs-lookup"><span data-stu-id="d9904-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="d9904-115">`EnumTypeDefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d9904-115">`EnumTypeDefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="d9904-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="d9904-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="d9904-117">在这种情况下， `pcTypeDefs` 为零。</span><span class="sxs-lookup"><span data-stu-id="d9904-117">In that case, `pcTypeDefs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d9904-118">备注</span><span class="sxs-lookup"><span data-stu-id="d9904-118">Remarks</span></span>  

 <span data-ttu-id="d9904-119">TypeDef 标记表示一种类型，如类或接口，以及通过扩展性机制添加的任何类型。</span><span class="sxs-lookup"><span data-stu-id="d9904-119">The TypeDef token represents a type such as a class or an interface, as well as any type added via an extensibility mechanism.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9904-120">要求</span><span class="sxs-lookup"><span data-stu-id="d9904-120">Requirements</span></span>  

 <span data-ttu-id="d9904-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9904-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9904-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d9904-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d9904-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d9904-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d9904-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9904-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9904-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="d9904-125">See also</span></span>

- [<span data-ttu-id="d9904-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="d9904-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="d9904-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="d9904-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

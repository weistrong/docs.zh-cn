---
description: 了解详细信息： IMetaDataImport：： EnumEvents 方法
title: IMetaDataImport::EnumEvents 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumEvents
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumEvents
helpviewer_keywords:
- IMetaDataImport::EnumEvents method [.NET Framework metadata]
- EnumEvents method [.NET Framework metadata]
ms.assetid: e1efedcb-3dd7-42ae-a399-21c24728aec5
topic_type:
- apiref
ms.openlocfilehash: e944c15a19314b315e01493836ce078fccc917eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799390"
---
# <a name="imetadataimportenumevents-method"></a><span data-ttu-id="b74f6-103">IMetaDataImport::EnumEvents 方法</span><span class="sxs-lookup"><span data-stu-id="b74f6-103">IMetaDataImport::EnumEvents Method</span></span>

<span data-ttu-id="b74f6-104">枚举指定的 TypeDef 标记的事件定义标记。</span><span class="sxs-lookup"><span data-stu-id="b74f6-104">Enumerates event definition tokens for the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b74f6-105">语法</span><span class="sxs-lookup"><span data-stu-id="b74f6-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumEvents (
   [in, out] HCORENUM    *phEnum,
   [in]      mdTypeDef   td,
   [out]     mdEvent     rEvents[],
   [in]      ULONG       cMax,  
   [out]    ULONG        *pcEvents  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b74f6-106">参数</span><span class="sxs-lookup"><span data-stu-id="b74f6-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="b74f6-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="b74f6-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `td`  
 <span data-ttu-id="b74f6-108">中要枚举其事件定义的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="b74f6-108">[in] The TypeDef token whose event definitions are to be enumerated.</span></span>  
  
 `rEvents`  
 <span data-ttu-id="b74f6-109">弄返回的事件的数组。</span><span class="sxs-lookup"><span data-stu-id="b74f6-109">[out] The array of returned events.</span></span>  
  
 `cMax`  
 <span data-ttu-id="b74f6-110">[in] `rEvents` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="b74f6-110">[in] The maximum size of the `rEvents` array.</span></span>  
  
 `pcEvents`  
 <span data-ttu-id="b74f6-111">弄中返回的实际事件数 `rEvents` 。</span><span class="sxs-lookup"><span data-stu-id="b74f6-111">[out] The actual number of events returned in `rEvents`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b74f6-112">返回值</span><span class="sxs-lookup"><span data-stu-id="b74f6-112">Return Value</span></span>  
  
|<span data-ttu-id="b74f6-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b74f6-113">HRESULT</span></span>|<span data-ttu-id="b74f6-114">说明</span><span class="sxs-lookup"><span data-stu-id="b74f6-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="b74f6-115">`EnumEvents` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b74f6-115">`EnumEvents` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="b74f6-116">没有要枚举的事件。</span><span class="sxs-lookup"><span data-stu-id="b74f6-116">There are no events to enumerate.</span></span> <span data-ttu-id="b74f6-117">在这种情况下， `pcEvents` 为零。</span><span class="sxs-lookup"><span data-stu-id="b74f6-117">In that case, `pcEvents` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b74f6-118">要求</span><span class="sxs-lookup"><span data-stu-id="b74f6-118">Requirements</span></span>  

 <span data-ttu-id="b74f6-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b74f6-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b74f6-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b74f6-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b74f6-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b74f6-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b74f6-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b74f6-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b74f6-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b74f6-123">See also</span></span>

- [<span data-ttu-id="b74f6-124">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="b74f6-124">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="b74f6-125">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="b74f6-125">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

---
description: 了解详细信息： IMetaDataFilter：： IsTokenMarked 方法
title: IMetaDataFilter::IsTokenMarked 方法
ms.date: 03/30/2017
api_name:
- IMetaDataFilter.IsTokenMarked
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter::IsTokenMarked
helpviewer_keywords:
- IMetaDataFilter::IsTokenMarked method [.NET Framework metadata]
- IsTokenMarked method [.NET Framework metadata]
ms.assetid: 7d90dcee-0206-4540-807b-06982fe65f1a
topic_type:
- apiref
ms.openlocfilehash: dddb0aa9040a2f5ef3ec972bb37a9e8778ddffe8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677764"
---
# <a name="imetadatafilteristokenmarked-method"></a><span data-ttu-id="57103-103">IMetaDataFilter::IsTokenMarked 方法</span><span class="sxs-lookup"><span data-stu-id="57103-103">IMetaDataFilter::IsTokenMarked Method</span></span>

<span data-ttu-id="57103-104">获取一个值，该值指示指定的元数据标记是否已标记为已处理。</span><span class="sxs-lookup"><span data-stu-id="57103-104">Gets a value indicating whether the specified metadata token has been marked as processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57103-105">语法</span><span class="sxs-lookup"><span data-stu-id="57103-105">Syntax</span></span>  
  
```cpp  
HRESULT IsTokenMarked (  
    [in]  mdToken  tk,
    [out] BOOL     *pIsMarked  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57103-106">参数</span><span class="sxs-lookup"><span data-stu-id="57103-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="57103-107">中要检查处理标记的标记。</span><span class="sxs-lookup"><span data-stu-id="57103-107">[in] The token to examine for a processing mark.</span></span>  
  
 `pIsMarked`  
 <span data-ttu-id="57103-108">弄如果已处理，则该值为 `true` `tk` ; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="57103-108">[out] A value that is `true` if `tk` has been processed; otherwise `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57103-109">要求</span><span class="sxs-lookup"><span data-stu-id="57103-109">Requirements</span></span>  

 <span data-ttu-id="57103-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="57103-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57103-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="57103-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="57103-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="57103-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="57103-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57103-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57103-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="57103-114">See also</span></span>

- [<span data-ttu-id="57103-115">IMetaDataFilter 接口</span><span class="sxs-lookup"><span data-stu-id="57103-115">IMetaDataFilter Interface</span></span>](imetadatafilter-interface.md)

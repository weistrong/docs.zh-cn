---
description: 了解详细信息： IMetaDataFilter：： MarkToken 方法
title: IMetaDataFilter::MarkToken 方法
ms.date: 03/30/2017
api_name:
- IMetaDataFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter::MarkToken
helpviewer_keywords:
- IMetaDataFilter::MarkToken method [.NET Framework metadata]
- MarkToken method, IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: bd492834-6529-4d39-b93d-f8cdbd3e297f
topic_type:
- apiref
ms.openlocfilehash: 97191533ae7d2bdc951521f1929a4c001c521b9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677770"
---
# <a name="imetadatafiltermarktoken-method"></a><span data-ttu-id="b42ac-103">IMetaDataFilter::MarkToken 方法</span><span class="sxs-lookup"><span data-stu-id="b42ac-103">IMetaDataFilter::MarkToken Method</span></span>

<span data-ttu-id="b42ac-104">设置一个值，该值指示已处理指定的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b42ac-104">Sets a value indicating that the specified metadata token has been processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b42ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="b42ac-105">Syntax</span></span>  
  
```cpp  
HRESULT MarkToken (  
    [in] mdToken   tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b42ac-106">参数</span><span class="sxs-lookup"><span data-stu-id="b42ac-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="b42ac-107">中标记为已处理的标记。</span><span class="sxs-lookup"><span data-stu-id="b42ac-107">[in] The token to mark as processed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b42ac-108">要求</span><span class="sxs-lookup"><span data-stu-id="b42ac-108">Requirements</span></span>  

 <span data-ttu-id="b42ac-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b42ac-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b42ac-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b42ac-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b42ac-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b42ac-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b42ac-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b42ac-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b42ac-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="b42ac-113">See also</span></span>

- [<span data-ttu-id="b42ac-114">IMetaDataFilter 接口</span><span class="sxs-lookup"><span data-stu-id="b42ac-114">IMetaDataFilter Interface</span></span>](imetadatafilter-interface.md)

---
description: 了解详细信息： IMetaDataImport：： ResetEnum 方法
title: IMetaDataImport::ResetEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.ResetEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::ResetEnum
helpviewer_keywords:
- ResetEnum method [.NET Framework metadata]
- IMetaDataImport::ResetEnum method [.NET Framework metadata]
ms.assetid: dda867b5-1050-49ba-b01c-fcc83b7a5617
topic_type:
- apiref
ms.openlocfilehash: 7b1572be2e2b905e6db5cf6e422643dbb76ca9be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670570"
---
# <a name="imetadataimportresetenum-method"></a><span data-ttu-id="f608a-103">IMetaDataImport::ResetEnum 方法</span><span class="sxs-lookup"><span data-stu-id="f608a-103">IMetaDataImport::ResetEnum Method</span></span>

<span data-ttu-id="f608a-104">将指定的枚举器重置到指定位置。</span><span class="sxs-lookup"><span data-stu-id="f608a-104">Resets the specified enumerator to the specified position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f608a-105">语法</span><span class="sxs-lookup"><span data-stu-id="f608a-105">Syntax</span></span>  
  
```cpp  
HRESULT ResetEnum (  
   [in] HCORENUM    hEnum,
   [in] ULONG       ulPos  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f608a-106">参数</span><span class="sxs-lookup"><span data-stu-id="f608a-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="f608a-107">中要重置的枚举数。</span><span class="sxs-lookup"><span data-stu-id="f608a-107">[in] The enumerator to reset.</span></span>  
  
 `ulPos`  
 <span data-ttu-id="f608a-108">中要放置枚举器的新位置。</span><span class="sxs-lookup"><span data-stu-id="f608a-108">[in] The new position at which to place the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f608a-109">要求</span><span class="sxs-lookup"><span data-stu-id="f608a-109">Requirements</span></span>  

 <span data-ttu-id="f608a-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f608a-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f608a-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f608a-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f608a-112">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f608a-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f608a-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f608a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f608a-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="f608a-114">See also</span></span>

- [<span data-ttu-id="f608a-115">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f608a-115">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f608a-116">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f608a-116">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

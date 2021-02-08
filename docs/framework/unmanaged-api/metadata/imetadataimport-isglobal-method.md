---
description: 了解详细信息： IMetaDataImport：： IsGlobal 方法
title: IMetaDataImport::IsGlobal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.IsGlobal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::IsGlobal
helpviewer_keywords:
- IsGlobal method [.NET Framework metadata]
- IMetaDataImport::IsGlobal method [.NET Framework metadata]
ms.assetid: 44cf6908-f555-4ae8-b2cf-24bd974bf2fe
topic_type:
- apiref
ms.openlocfilehash: 5230b2967990e3c52b429d62dd03566c3043e45f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789068"
---
# <a name="imetadataimportisglobal-method"></a><span data-ttu-id="57506-103">IMetaDataImport::IsGlobal 方法</span><span class="sxs-lookup"><span data-stu-id="57506-103">IMetaDataImport::IsGlobal Method</span></span>

<span data-ttu-id="57506-104">获取一个值，该值指示由指定的元数据标记表示的字段、方法或类型是否具有全局范围。</span><span class="sxs-lookup"><span data-stu-id="57506-104">Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57506-105">语法</span><span class="sxs-lookup"><span data-stu-id="57506-105">Syntax</span></span>  
  
```cpp  
HRESULT IsGlobal (  
   [in]  mdToken     pd,  
   [out] int         *pbGlobal  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57506-106">参数</span><span class="sxs-lookup"><span data-stu-id="57506-106">Parameters</span></span>  

 `pd`  
 <span data-ttu-id="57506-107">中表示类型、字段或方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="57506-107">[in] A metadata token that represents a type, field, or method.</span></span>  
  
 `pbGlobal`  
 <span data-ttu-id="57506-108">[out] 如果对象具有全局范围，则为 1;否则，0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="57506-108">[out] 1 if the object has global scope; otherwise, 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57506-109">要求</span><span class="sxs-lookup"><span data-stu-id="57506-109">Requirements</span></span>  

 <span data-ttu-id="57506-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="57506-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57506-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="57506-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="57506-112">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="57506-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="57506-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57506-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57506-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="57506-114">See also</span></span>

- [<span data-ttu-id="57506-115">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="57506-115">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="57506-116">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="57506-116">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

---
description: 了解详细信息： IMetaDataImport：： GetModuleFromScope 方法
title: IMetaDataImport::GetModuleFromScope 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetModuleFromScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetModuleFromScope
helpviewer_keywords:
- GetModuleFromScope method [.NET Framework metadata]
- IMetaDataImport::GetModuleFromScope method [.NET Framework metadata]
ms.assetid: add68d3f-45fd-4bef-af94-eb5273f26b11
topic_type:
- apiref
ms.openlocfilehash: 8c1e952a45b3827717102428fbd18ceac3951baf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753362"
---
# <a name="imetadataimportgetmodulefromscope-method"></a><span data-ttu-id="088fb-103">IMetaDataImport::GetModuleFromScope 方法</span><span class="sxs-lookup"><span data-stu-id="088fb-103">IMetaDataImport::GetModuleFromScope Method</span></span>

<span data-ttu-id="088fb-104">获取当前元数据范围内引用的模块的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="088fb-104">Gets a metadata token for the module referenced in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="088fb-105">语法</span><span class="sxs-lookup"><span data-stu-id="088fb-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleFromScope (  
   [out] mdModule    *pmd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="088fb-106">参数</span><span class="sxs-lookup"><span data-stu-id="088fb-106">Parameters</span></span>  

 `pmd`  
 <span data-ttu-id="088fb-107">弄一个指针，指向表示当前元数据范围内引用的模块的标记。</span><span class="sxs-lookup"><span data-stu-id="088fb-107">[out] A pointer to the token representing the module referenced in the current metadata scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="088fb-108">要求</span><span class="sxs-lookup"><span data-stu-id="088fb-108">Requirements</span></span>  

 <span data-ttu-id="088fb-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="088fb-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="088fb-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="088fb-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="088fb-111">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="088fb-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="088fb-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="088fb-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="088fb-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="088fb-113">See also</span></span>

- [<span data-ttu-id="088fb-114">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="088fb-114">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="088fb-115">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="088fb-115">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

---
description: 了解详细信息： IMetaDataEmit：： ApplyEditAndContinue 方法
title: IMetaDataEmit::ApplyEditAndContinue 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.ApplyEditAndContinue
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::ApplyEditAndContinue
helpviewer_keywords:
- ApplyEditAndContinue method [.NET Framework metadata]
- IMetaDataEmit::ApplyEditAndContinue method [.NET Framework metadata]
ms.assetid: 35991289-f389-495d-8caa-a6384fb1d557
topic_type:
- apiref
ms.openlocfilehash: 46454c4141aa220b43820307c86765a1827251df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753492"
---
# <a name="imetadataemitapplyeditandcontinue-method"></a><span data-ttu-id="8bd10-103">IMetaDataEmit::ApplyEditAndContinue 方法</span><span class="sxs-lookup"><span data-stu-id="8bd10-103">IMetaDataEmit::ApplyEditAndContinue Method</span></span>

<span data-ttu-id="8bd10-104">用在指定的元数据中进行的更改更新当前程序集范围。</span><span class="sxs-lookup"><span data-stu-id="8bd10-104">Updates the current assembly scope with the changes made in the specified metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8bd10-105">语法</span><span class="sxs-lookup"><span data-stu-id="8bd10-105">Syntax</span></span>  
  
```cpp  
HRESULT ApplyEditAndContinue (
    [in]  IUnknown    *pImport  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8bd10-106">参数</span><span class="sxs-lookup"><span data-stu-id="8bd10-106">Parameters</span></span>  

 `pImport`  
 <span data-ttu-id="8bd10-107">\[\]指向[IUnknown](/cpp/atl/iunknown)对象的指针，该对象表示来自可移植可执行文件的增量元数据 (PE) 文件。</span><span class="sxs-lookup"><span data-stu-id="8bd10-107">\[in\] Pointer to an [IUnknown](/cpp/atl/iunknown) object that represents the delta metadata from the portable executable (PE) file.</span></span>
  
 <span data-ttu-id="8bd10-108">增量元数据是元数据的块，其中包括对模块的实际元数据副本所做的更改。</span><span class="sxs-lookup"><span data-stu-id="8bd10-108">The delta metadata is the block of metadata that includes the changes that were made to the copy of the module's actual metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8bd10-109">要求</span><span class="sxs-lookup"><span data-stu-id="8bd10-109">Requirements</span></span>  

 <span data-ttu-id="8bd10-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8bd10-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8bd10-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8bd10-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8bd10-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8bd10-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8bd10-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8bd10-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8bd10-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="8bd10-114">See also</span></span>

- [<span data-ttu-id="8bd10-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8bd10-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="8bd10-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8bd10-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

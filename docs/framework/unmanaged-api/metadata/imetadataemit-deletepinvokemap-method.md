---
description: 了解详细信息： IMetaDataEmit：:D eletePinvokeMap 方法
title: IMetaDataEmit::DeletePinvokeMap 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeletePinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeletePinvokeMap
helpviewer_keywords:
- IMetaDataEmit::DeletePinvokeMap method [.NET Framework metadata]
- DeletePinvokeMap method [.NET Framework metadata]
ms.assetid: 3c4f6b54-5ce7-4a2a-83e1-6dec16441f50
topic_type:
- apiref
ms.openlocfilehash: 977fd600600cdfba0fd9fd5d383648ffbf63229f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783971"
---
# <a name="imetadataemitdeletepinvokemap-method"></a><span data-ttu-id="f69ae-103">IMetaDataEmit::DeletePinvokeMap 方法</span><span class="sxs-lookup"><span data-stu-id="f69ae-103">IMetaDataEmit::DeletePinvokeMap Method</span></span>

<span data-ttu-id="f69ae-104">销毁指定标记所引用的对象的 PInvoke 映射元数据。</span><span class="sxs-lookup"><span data-stu-id="f69ae-104">Destroys the PInvoke mapping metadata for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f69ae-105">语法</span><span class="sxs-lookup"><span data-stu-id="f69ae-105">Syntax</span></span>  
  
```cpp  
HRESULT DeletePinvokeMap (
    [in]  mdToken     tk
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f69ae-106">参数</span><span class="sxs-lookup"><span data-stu-id="f69ae-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="f69ae-107">中 `mdFieldDef` 或 `mdMethodDef` 标记，它表示要为其删除 PInvoke 映射元数据的对象。</span><span class="sxs-lookup"><span data-stu-id="f69ae-107">[in] An `mdFieldDef` or `mdMethodDef` token that represents the object for which to delete the PInvoke mapping metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f69ae-108">要求</span><span class="sxs-lookup"><span data-stu-id="f69ae-108">Requirements</span></span>  

 <span data-ttu-id="f69ae-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f69ae-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f69ae-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f69ae-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f69ae-111">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f69ae-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f69ae-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f69ae-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f69ae-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f69ae-113">See also</span></span>

- [<span data-ttu-id="f69ae-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="f69ae-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="f69ae-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="f69ae-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

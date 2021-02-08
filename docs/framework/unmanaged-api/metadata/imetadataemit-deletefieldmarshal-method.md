---
description: 了解详细信息： IMetaDataEmit：:D eleteFieldMarshal 方法
title: IMetaDataEmit::DeleteFieldMarshal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type:
- apiref
ms.openlocfilehash: 966f2ae20ad9ff4b9c1c9eec32974bc89aa76d13
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783958"
---
# <a name="imetadataemitdeletefieldmarshal-method"></a><span data-ttu-id="6e5dd-103">IMetaDataEmit::DeleteFieldMarshal 方法</span><span class="sxs-lookup"><span data-stu-id="6e5dd-103">IMetaDataEmit::DeleteFieldMarshal Method</span></span>

<span data-ttu-id="6e5dd-104">销毁指定标记所引用的对象的 PInvoke 封送元数据签名。</span><span class="sxs-lookup"><span data-stu-id="6e5dd-104">Destroys the PInvoke marshaling metadata signature for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e5dd-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e5dd-105">Syntax</span></span>  
  
```cpp  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e5dd-106">参数</span><span class="sxs-lookup"><span data-stu-id="6e5dd-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="6e5dd-107">中 `mdFieldDef` 或 `mdParamDef` 标记，它表示要删除封送处理元数据签名的字段或参数。</span><span class="sxs-lookup"><span data-stu-id="6e5dd-107">[in] An `mdFieldDef` or `mdParamDef` token that represents the field or parameter for which to delete the marshaling metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e5dd-108">要求</span><span class="sxs-lookup"><span data-stu-id="6e5dd-108">Requirements</span></span>  

 <span data-ttu-id="6e5dd-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e5dd-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e5dd-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="6e5dd-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6e5dd-111">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="6e5dd-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6e5dd-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e5dd-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e5dd-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e5dd-113">See also</span></span>

- [<span data-ttu-id="6e5dd-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="6e5dd-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="6e5dd-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="6e5dd-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

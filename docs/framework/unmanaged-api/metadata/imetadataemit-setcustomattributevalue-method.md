---
description: 了解详细信息： IMetaDataEmit：： SetCustomAttributeValue 方法
title: IMetaDataEmit::SetCustomAttributeValue 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetCustomAttributeValue
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetCustomAttributeValue
helpviewer_keywords:
- SetCustomAttributeValue method [.NET Framework metadata]
- IMetaDataEmit::SetCustomAttributeValue method [.NET Framework metadata]
ms.assetid: f721c863-9642-4e64-917a-65f9e55c25b9
topic_type:
- apiref
ms.openlocfilehash: 1eede765f27b371deb670242086d59b3d4320530
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706573"
---
# <a name="imetadataemitsetcustomattributevalue-method"></a><span data-ttu-id="64d7d-103">IMetaDataEmit::SetCustomAttributeValue 方法</span><span class="sxs-lookup"><span data-stu-id="64d7d-103">IMetaDataEmit::SetCustomAttributeValue Method</span></span>

<span data-ttu-id="64d7d-104">设置或更新通过之前对 IMetaDataEmit 的调用定义的自定义特性的值 [：:D efinecustomattribute](imetadataemit-definecustomattribute-method.md)。</span><span class="sxs-lookup"><span data-stu-id="64d7d-104">Sets or updates the value of a custom attribute defined by a prior call to [IMetaDataEmit::DefineCustomAttribute](imetadataemit-definecustomattribute-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64d7d-105">语法</span><span class="sxs-lookup"><span data-stu-id="64d7d-105">Syntax</span></span>  
  
```cpp  
HRESULT SetCustomAttributeValue (
    [in]  mdCustomAttribute       pcv,
    [in]  void const              *pCustomAttribute,
    [in]  ULONG                   cbCustomAttribute
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="64d7d-106">参数</span><span class="sxs-lookup"><span data-stu-id="64d7d-106">Parameters</span></span>  

 `pcv`  
 <span data-ttu-id="64d7d-107">中目标自定义属性的标记。</span><span class="sxs-lookup"><span data-stu-id="64d7d-107">[in] The token of the target custom attribute.</span></span>  
  
 `pCustomAttribute`  
 <span data-ttu-id="64d7d-108">中指向包含自定义特性的数组的指针。</span><span class="sxs-lookup"><span data-stu-id="64d7d-108">[in] A pointer to the array that contains the custom attribute.</span></span>  
  
 `cbCustomAttribute`  
 <span data-ttu-id="64d7d-109">中自定义属性的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="64d7d-109">[in] The size, in bytes, of the custom attribute.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64d7d-110">要求</span><span class="sxs-lookup"><span data-stu-id="64d7d-110">Requirements</span></span>  

 <span data-ttu-id="64d7d-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="64d7d-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64d7d-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="64d7d-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="64d7d-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="64d7d-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="64d7d-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64d7d-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64d7d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="64d7d-115">See also</span></span>

- [<span data-ttu-id="64d7d-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="64d7d-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="64d7d-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="64d7d-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

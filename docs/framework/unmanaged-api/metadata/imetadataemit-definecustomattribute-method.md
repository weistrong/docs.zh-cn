---
description: 了解详细信息： IMetaDataEmit：:D efineCustomAttribute 方法
title: IMetaDataEmit::DefineCustomAttribute 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineCustomAttribute
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineCustomAttribute
helpviewer_keywords:
- DefineCustomAttribute method [.NET Framework metadata]
- IMetaDataEmit::DefineCustomAttribute method [.NET Framework metadata]
ms.assetid: 7dd14854-b756-4401-b167-88ca576dc8f0
topic_type:
- apiref
ms.openlocfilehash: 5d802f590525b8b398ac270b1b7f59d122b45b73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753479"
---
# <a name="imetadataemitdefinecustomattribute-method"></a><span data-ttu-id="079a3-103">IMetaDataEmit::DefineCustomAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="079a3-103">IMetaDataEmit::DefineCustomAttribute Method</span></span>

<span data-ttu-id="079a3-104">使用指定的元数据签名创建要附加到指定对象的自定义属性的定义，并获取该自定义属性定义的标记。</span><span class="sxs-lookup"><span data-stu-id="079a3-104">Creates a definition for a custom attribute with the specified metadata signature, to be attached to the specified object, and gets a token to that custom attribute definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="079a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="079a3-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineCustomAttribute (
    [in]  mdToken     tkObj,
    [in]  mdToken     tkType,
    [in]  void const  *pCustomAttribute,
    [in]  ULONG       cbCustomAttribute,
    [out] mdCustomAttribute *pcv
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="079a3-106">参数</span><span class="sxs-lookup"><span data-stu-id="079a3-106">Parameters</span></span>  

 `tkObj`  
 <span data-ttu-id="079a3-107">中所有者项的标记。</span><span class="sxs-lookup"><span data-stu-id="079a3-107">[in] The token for the owner item.</span></span>  
  
 `tkType`  
 <span data-ttu-id="079a3-108">中标识自定义属性的标记。</span><span class="sxs-lookup"><span data-stu-id="079a3-108">[in] The token that identifies the custom attribute.</span></span>  
  
 `pCustomAttribute`  
 <span data-ttu-id="079a3-109">中指向自定义属性的指针。</span><span class="sxs-lookup"><span data-stu-id="079a3-109">[in] A pointer to the custom attribute.</span></span>  
  
 `cbCustomAttribute`  
 <span data-ttu-id="079a3-110">中中的字节数 `pCustomAttribute` 。</span><span class="sxs-lookup"><span data-stu-id="079a3-110">[in] The count of bytes in `pCustomAttribute`.</span></span>  
  
 `pcv`  
 <span data-ttu-id="079a3-111">弄 `mdCustomAttribute` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="079a3-111">[out] The `mdCustomAttribute` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="079a3-112">要求</span><span class="sxs-lookup"><span data-stu-id="079a3-112">Requirements</span></span>  

 <span data-ttu-id="079a3-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="079a3-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="079a3-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="079a3-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="079a3-115">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="079a3-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="079a3-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="079a3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="079a3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="079a3-117">See also</span></span>

- [<span data-ttu-id="079a3-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="079a3-118">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="079a3-119">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="079a3-119">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

---
description: 了解详细信息： IMetaDataEmit：： SetParent 方法
title: IMetaDataEmit::SetParent 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetParent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetParent
helpviewer_keywords:
- SetParent method [.NET Framework metadata]
- IMetaDataEmit::SetParent method [.NET Framework metadata]
ms.assetid: 02a02ff7-ae0e-4692-a20e-372405f23052
topic_type:
- apiref
ms.openlocfilehash: 9025d4a37de85a0e657059f63ef781dc4377c036
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771998"
---
# <a name="imetadataemitsetparent-method"></a><span data-ttu-id="13c86-103">IMetaDataEmit::SetParent 方法</span><span class="sxs-lookup"><span data-stu-id="13c86-103">IMetaDataEmit::SetParent Method</span></span>

<span data-ttu-id="13c86-104">确定由之前调用 [IMetaDataEmit：:D efinememberref](imetadataemit-definememberref-method.md)定义的指定成员是否为指定类型的成员，该成员由先前调用 [IMetaDataEmit：:D efinetypedef](imetadataemit-definetypedef-method.md)定义。</span><span class="sxs-lookup"><span data-stu-id="13c86-104">Establishes that the specified member, as defined by a prior call to [IMetaDataEmit::DefineMemberRef](imetadataemit-definememberref-method.md), is a member of the specified type, as defined by a prior call to [IMetaDataEmit::DefineTypeDef](imetadataemit-definetypedef-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13c86-105">语法</span><span class="sxs-lookup"><span data-stu-id="13c86-105">Syntax</span></span>  
  
```cpp  
HRESULT SetParent (
    [in]  mdMemberRef mr,
    [in]  mdToken     tk
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13c86-106">参数</span><span class="sxs-lookup"><span data-stu-id="13c86-106">Parameters</span></span>  

 `mr`  
 <span data-ttu-id="13c86-107">中 `mdMemberRef` 用于接收新父级的标记。</span><span class="sxs-lookup"><span data-stu-id="13c86-107">[in] The `mdMemberRef` token to receive a new parent.</span></span>  
  
 `tk`  
 <span data-ttu-id="13c86-108">中 `mdToken` 新父级的。</span><span class="sxs-lookup"><span data-stu-id="13c86-108">[in] The `mdToken` for the new parent.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13c86-109">要求</span><span class="sxs-lookup"><span data-stu-id="13c86-109">Requirements</span></span>  

 <span data-ttu-id="13c86-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13c86-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13c86-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="13c86-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="13c86-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="13c86-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="13c86-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13c86-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13c86-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="13c86-114">See also</span></span>

- [<span data-ttu-id="13c86-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="13c86-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="13c86-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="13c86-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

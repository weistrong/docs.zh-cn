---
description: 了解详细信息： IMetaDataEmit：： SetTypeDefProps 方法
title: IMetaDataEmit::SetTypeDefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetTypeDefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetTypeDefProps
helpviewer_keywords:
- SetTypeDefProps method [.NET Framework metadata]
- IMetaDataEmit::SetTypeDefProps method [.NET Framework metadata]
ms.assetid: 480d596a-759f-4d29-ac1a-3dbff8f3544d
topic_type:
- apiref
ms.openlocfilehash: 1160d20e7ceb422390f8cd725a75fdb4f42318e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706495"
---
# <a name="imetadataemitsettypedefprops-method"></a><span data-ttu-id="ddbf4-103">IMetaDataEmit::SetTypeDefProps 方法</span><span class="sxs-lookup"><span data-stu-id="ddbf4-103">IMetaDataEmit::SetTypeDefProps Method</span></span>

<span data-ttu-id="ddbf4-104">设置由之前调用 [IMetaDataEmit：:D efinetypedef](imetadataemit-definetypedef-method.md)定义的类型的功能。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-104">Sets features of a type defined by a prior call to [IMetaDataEmit::DefineTypeDef](imetadataemit-definetypedef-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddbf4-105">语法</span><span class="sxs-lookup"><span data-stu-id="ddbf4-105">Syntax</span></span>  
  
```cpp  
HRESULT SetTypeDefProps (  
    [in]  mdTypeDef   td,
    [in]  DWORD       dwTypeDefFlags,
    [in]  mdToken     tkExtends,
    [in]  mdToken     rtkImplements[]
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ddbf4-106">参数</span><span class="sxs-lookup"><span data-stu-id="ddbf4-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="ddbf4-107">中 `mdTypeDef` 从对 IMetaDataEmit 的原始调用获取的标记 [：:D efinetypedef](imetadataemit-definetypedef-method.md)。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-107">[in] An `mdTypeDef` token obtained from original call to [IMetaDataEmit::DefineTypeDef](imetadataemit-definetypedef-method.md).</span></span>  
  
 `dwTypeDefFlags`  
 <span data-ttu-id="ddbf4-108">[in] `TypeDef` 属性.</span><span class="sxs-lookup"><span data-stu-id="ddbf4-108">[in] `TypeDef` attributes.</span></span> <span data-ttu-id="ddbf4-109">这是一个值的位掩码 `CorTypeAttr` 。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-109">This is a bitmask of `CorTypeAttr` values.</span></span>  
  
 `tkExtends`  
 <span data-ttu-id="ddbf4-110">中 `mdToken` 基类的。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-110">[in] The `mdToken` of the base class.</span></span> <span data-ttu-id="ddbf4-111">从之前对 IMetaDataEmit 的调用中获取 [：:D efineimporttype](imetadataemit-defineimporttype-method.md)或 `null` 。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-111">Obtained from a previous call to [IMetaDataEmit::DefineImportType](imetadataemit-defineimporttype-method.md), or `null`.</span></span>  
  
 `rtkImplements[]`  
 <span data-ttu-id="ddbf4-112">中此类型实现的接口的标记数组。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-112">[in] An array of tokens for the interfaces that this type implements.</span></span> <span data-ttu-id="ddbf4-113">`mdTypeRef`使用[IMetaDataEmit：:D efineimporttype](imetadataemit-defineimporttype-method.md)获取这些令牌。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-113">These `mdTypeRef` tokens are obtained using [IMetaDataEmit::DefineImportType](imetadataemit-defineimporttype-method.md).</span></span> <span data-ttu-id="ddbf4-114">数组的最后一个元素必须是 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-114">The last element of the array is must be `mdTokenNil`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ddbf4-115">要求</span><span class="sxs-lookup"><span data-stu-id="ddbf4-115">Requirements</span></span>  

 <span data-ttu-id="ddbf4-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ddbf4-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ddbf4-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ddbf4-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ddbf4-118">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="ddbf4-118">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ddbf4-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ddbf4-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddbf4-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="ddbf4-120">See also</span></span>

- [<span data-ttu-id="ddbf4-121">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="ddbf4-121">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="ddbf4-122">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="ddbf4-122">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

---
description: 了解详细信息： IMetaDataEmit：:D efineNestedType 方法
title: IMetaDataEmit::DefineNestedType 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineNestedType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineNestedType
helpviewer_keywords:
- IMetaDataEmit::DefineNestedType method [.NET Framework metadata]
- DefineNestedType method [.NET Framework metadata]
ms.assetid: 1e994de6-4628-459c-b967-b34be1e9fe4f
topic_type:
- apiref
ms.openlocfilehash: 1b0c5c8d1bffa425b2019a4434042c84a0069907
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753375"
---
# <a name="imetadataemitdefinenestedtype-method"></a><span data-ttu-id="f30bc-103">IMetaDataEmit::DefineNestedType 方法</span><span class="sxs-lookup"><span data-stu-id="f30bc-103">IMetaDataEmit::DefineNestedType Method</span></span>

<span data-ttu-id="f30bc-104">创建类型定义的元数据签名，返回 `mdTypeDef` 该类型的标记，并指定该定义类型是参数所引用的类型的成员 `tdEncloser` 。</span><span class="sxs-lookup"><span data-stu-id="f30bc-104">Creates the metadata signature of a type definition, returns an `mdTypeDef` token for that type, and specifies that the defined type is a member of the type referenced by the `tdEncloser` parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f30bc-105">语法</span><span class="sxs-lookup"><span data-stu-id="f30bc-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineNestedType (
    [in]  LPCWSTR     szTypeDef,  
    [in]  DWORD       dwTypeDefFlags,
    [in]  mdToken     tkExtends,
    [in]  mdToken     rtkImplements[],
    [in]  mdTypeDef   tdEncloser,
    [out] mdTypeDef   *ptd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f30bc-106">参数</span><span class="sxs-lookup"><span data-stu-id="f30bc-106">Parameters</span></span>  

 `szTypeDef`  
 <span data-ttu-id="f30bc-107">中Unicode 中类型的名称。</span><span class="sxs-lookup"><span data-stu-id="f30bc-107">[in] The name of the type in Unicode.</span></span>  
  
 `dwTypeDefFlags`  
 <span data-ttu-id="f30bc-108">[in] `TypeDef` 属性.</span><span class="sxs-lookup"><span data-stu-id="f30bc-108">[in] `TypeDef` attributes.</span></span> <span data-ttu-id="f30bc-109">这是一个值的位掩码 `CorTypeAttr` 。</span><span class="sxs-lookup"><span data-stu-id="f30bc-109">This is a bitmask of `CorTypeAttr` values.</span></span>  
  
 `tkExtends`  
 <span data-ttu-id="f30bc-110">中基类的标记。</span><span class="sxs-lookup"><span data-stu-id="f30bc-110">[in] The token of the base class.</span></span> <span data-ttu-id="f30bc-111">这是 `mdTypeDef` 或 `mdTypeRef` 令牌。</span><span class="sxs-lookup"><span data-stu-id="f30bc-111">This is either a `mdTypeDef` or a `mdTypeRef` token.</span></span>  
  
 <span data-ttu-id="f30bc-112">`rtkImplements`[]</span><span class="sxs-lookup"><span data-stu-id="f30bc-112">`rtkImplements`[]</span></span>  
 <span data-ttu-id="f30bc-113">中标记的数组，该数组指定此类或接口实现的接口。</span><span class="sxs-lookup"><span data-stu-id="f30bc-113">[in] An array of tokens that specify the interfaces that this class or interface implements.</span></span>  
  
 `tdEncloser`  
 <span data-ttu-id="f30bc-114">中封闭类型的标记。</span><span class="sxs-lookup"><span data-stu-id="f30bc-114">[in] The token of the enclosing type.</span></span> <span data-ttu-id="f30bc-115">数组的最后一个元素必须是 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="f30bc-115">The last element of the array must be `mdTokenNil`.</span></span>  
  
 `ptd`  
 <span data-ttu-id="f30bc-116">弄 `mdTypeDef` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="f30bc-116">[out] The `mdTypeDef` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f30bc-117">要求</span><span class="sxs-lookup"><span data-stu-id="f30bc-117">Requirements</span></span>  

 <span data-ttu-id="f30bc-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f30bc-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f30bc-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f30bc-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f30bc-120">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f30bc-120">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f30bc-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f30bc-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f30bc-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="f30bc-122">See also</span></span>

- [<span data-ttu-id="f30bc-123">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="f30bc-123">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="f30bc-124">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="f30bc-124">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

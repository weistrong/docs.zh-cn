---
description: 了解详细信息： IMetaDataEmit：： SetPropertyProps 方法
title: IMetaDataEmit::SetPropertyProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPropertyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPropertyProps
helpviewer_keywords:
- SetPropertyProps method [.NET Framework metadata]
- IMetaDataEmit::SetPropertyProps method [.NET Framework metadata]
ms.assetid: e2501fc8-b2bc-4dcc-9205-e3acd5a53ffe
topic_type:
- apiref
ms.openlocfilehash: ad5efa86b4f774bcaa2251cb992c2dd52ac28bdd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771829"
---
# <a name="imetadataemitsetpropertyprops-method"></a><span data-ttu-id="107fb-103">IMetaDataEmit::SetPropertyProps 方法</span><span class="sxs-lookup"><span data-stu-id="107fb-103">IMetaDataEmit::SetPropertyProps Method</span></span>

<span data-ttu-id="107fb-104">设置由之前调用 [DefineProperty 方法](imetadataemit-defineproperty-method.md)定义的属性的元数据中存储的功能。</span><span class="sxs-lookup"><span data-stu-id="107fb-104">Sets the features stored in metadata for a property defined by a prior call to [DefineProperty Method](imetadataemit-defineproperty-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="107fb-105">语法</span><span class="sxs-lookup"><span data-stu-id="107fb-105">Syntax</span></span>  
  
```cpp  
HRESULT SetPropertyProps (
    [in]  mdProperty      pr,
    [in]  DWORD           dwPropFlags,
    [in]  DWORD           dwCPlusTypeFlag,
    [in]  void const      *pValue,
    [in]  ULONG           cchValue,
    [in]  mdMethodDef     mdSetter,
    [in]  mdMethodDef     mdGetter,
    [in]  mdMethodDef     rmdOtherMethods[]
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="107fb-106">参数</span><span class="sxs-lookup"><span data-stu-id="107fb-106">Parameters</span></span>  

 `pr`  
 <span data-ttu-id="107fb-107">中要更改的属性的标记</span><span class="sxs-lookup"><span data-stu-id="107fb-107">[in] The token for the property to be changed</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="107fb-108">中属性标志。</span><span class="sxs-lookup"><span data-stu-id="107fb-108">[in] Property flags.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="107fb-109">中属性的默认值的类型。</span><span class="sxs-lookup"><span data-stu-id="107fb-109">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="107fb-110">中属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="107fb-110">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="107fb-111">中中 (Unicode) 字符的计数 `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="107fb-111">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="107fb-112">中用于设置属性值的方法。</span><span class="sxs-lookup"><span data-stu-id="107fb-112">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="107fb-113">中获取属性值的方法。</span><span class="sxs-lookup"><span data-stu-id="107fb-113">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="107fb-114">中与属性关联的其他方法的数组。</span><span class="sxs-lookup"><span data-stu-id="107fb-114">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="107fb-115">使用标记终止此数组 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="107fb-115">Terminate this array with an `mdTokenNil` token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="107fb-116">要求</span><span class="sxs-lookup"><span data-stu-id="107fb-116">Requirements</span></span>  

 <span data-ttu-id="107fb-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="107fb-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="107fb-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="107fb-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="107fb-119">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="107fb-119">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="107fb-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="107fb-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="107fb-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="107fb-121">See also</span></span>

- [<span data-ttu-id="107fb-122">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="107fb-122">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="107fb-123">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="107fb-123">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

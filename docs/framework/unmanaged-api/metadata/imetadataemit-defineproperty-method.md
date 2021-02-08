---
description: 了解详细信息： IMetaDataEmit：:D efineProperty 方法
title: IMetaDataEmit::DefineProperty 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineProperty
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type:
- apiref
ms.openlocfilehash: c0c0b6009f8674a5edebf1c982e277f4ca5b185b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784023"
---
# <a name="imetadataemitdefineproperty-method"></a><span data-ttu-id="001cd-103">IMetaDataEmit::DefineProperty 方法</span><span class="sxs-lookup"><span data-stu-id="001cd-103">IMetaDataEmit::DefineProperty Method</span></span>

<span data-ttu-id="001cd-104">使用指定的和方法访问器创建指定类型的属性定义， `get` `set` 并获取该属性定义的标记。</span><span class="sxs-lookup"><span data-stu-id="001cd-104">Creates a property definition for the specified type, with the specified `get` and `set` method accessors, and gets a token to that property definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="001cd-105">语法</span><span class="sxs-lookup"><span data-stu-id="001cd-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineProperty (
    [in]  mdTypeDef          td,
    [in]  LPCWSTR            szProperty,
    [in]  DWORD              dwPropFlags,
    [in]  PCCOR_SIGNATURE    pvSig,
    [in]  ULONG              cbSig,
    [in]  DWORD              dwCPlusTypeFlag,
    [in]  void const         *pValue,
    [in]  ULONG              cchValue,
    [in]  mdMethodDef        mdSetter,
    [in]  mdMethodDef        mdGetter,
    [in]  mdMethodDef        rmdOtherMethods[],
    [out] mdProperty         *pmdProp
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="001cd-106">参数</span><span class="sxs-lookup"><span data-stu-id="001cd-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="001cd-107">中正在为其定义属性的类或接口的标记。</span><span class="sxs-lookup"><span data-stu-id="001cd-107">[in] The token for class or interface on which the property is being defined.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="001cd-108">中属性的名称。</span><span class="sxs-lookup"><span data-stu-id="001cd-108">[in] The name of the property.</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="001cd-109">中属性标志。</span><span class="sxs-lookup"><span data-stu-id="001cd-109">[in] The property flags.</span></span>  
  
 `pvSig`  
 <span data-ttu-id="001cd-110">中属性签名。</span><span class="sxs-lookup"><span data-stu-id="001cd-110">[in] The property signature.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="001cd-111">中中的字节数 `pvSig` 。</span><span class="sxs-lookup"><span data-stu-id="001cd-111">[in] The count of bytes in `pvSig`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="001cd-112">中属性的默认值的类型。</span><span class="sxs-lookup"><span data-stu-id="001cd-112">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="001cd-113">中属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="001cd-113">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="001cd-114">中中 (Unicode) 字符的计数 `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="001cd-114">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="001cd-115">中用于设置属性值的方法。</span><span class="sxs-lookup"><span data-stu-id="001cd-115">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="001cd-116">中获取属性值的方法。</span><span class="sxs-lookup"><span data-stu-id="001cd-116">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="001cd-117">中与属性关联的其他方法的数组。</span><span class="sxs-lookup"><span data-stu-id="001cd-117">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="001cd-118">使用终止数组 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="001cd-118">Terminate the array with an `mdTokenNil`.</span></span>  
  
 `pmdProp`  
 <span data-ttu-id="001cd-119">弄 `mdProperty` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="001cd-119">[out] The `mdProperty` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="001cd-120">要求</span><span class="sxs-lookup"><span data-stu-id="001cd-120">Requirements</span></span>  

 <span data-ttu-id="001cd-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="001cd-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="001cd-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="001cd-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="001cd-123">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="001cd-123">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="001cd-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="001cd-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="001cd-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="001cd-125">See also</span></span>

- [<span data-ttu-id="001cd-126">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="001cd-126">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="001cd-127">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="001cd-127">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

---
description: 了解详细信息： IMetaDataEmit：:D efineField 方法
title: IMetaDataEmit::DefineField 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineField
helpviewer_keywords:
- IMetaDataEmit::DefineField method [.NET Framework metadata]
- DefineField method, IMetaDataEmit interface [.NET Framework metadata
ms.assetid: 6b5be4fc-2e86-499c-8b09-833160bca767
topic_type:
- apiref
ms.openlocfilehash: 7636b1521de721cc183305e8a0763ff0a61f331b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753440"
---
# <a name="imetadataemitdefinefield-method"></a><span data-ttu-id="cc989-103">IMetaDataEmit::DefineField 方法</span><span class="sxs-lookup"><span data-stu-id="cc989-103">IMetaDataEmit::DefineField Method</span></span>

<span data-ttu-id="cc989-104">使用指定的元数据签名创建字段的定义，并获取该字段定义的标记。</span><span class="sxs-lookup"><span data-stu-id="cc989-104">Creates a definition for a field with the specified metadata signature, and gets a token to that field definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc989-105">语法</span><span class="sxs-lookup"><span data-stu-id="cc989-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineField (
    [in]  mdTypeDef   td,
    [in]  LPCWSTR     szName,
    [in]  DWORD       dwFieldFlags,
    [in]  PCCOR_SIGNATURE pvSigBlob,
    [in]  ULONG       cbSigBlob,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,
    [in]  ULONG       cchValue,
    [out] mdFieldDef  *pmd
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc989-106">参数</span><span class="sxs-lookup"><span data-stu-id="cc989-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="cc989-107">中 `mdTypeDef` 封闭类或接口的标记。</span><span class="sxs-lookup"><span data-stu-id="cc989-107">[in] The `mdTypeDef` token for the enclosing class or interface.</span></span>  
  
 `szName`  
 <span data-ttu-id="cc989-108">中Unicode 中的字段名称。</span><span class="sxs-lookup"><span data-stu-id="cc989-108">[in] The field name in Unicode.</span></span>  
  
 `dwFieldFlags`  
 <span data-ttu-id="cc989-109">中字段特性。</span><span class="sxs-lookup"><span data-stu-id="cc989-109">[in] The field attributes.</span></span> <span data-ttu-id="cc989-110">这是一个值的位掩码 `CorFieldAttr` 。</span><span class="sxs-lookup"><span data-stu-id="cc989-110">This is a bitmask of `CorFieldAttr` values.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="cc989-111">中作为 BLOB 的字段签名。</span><span class="sxs-lookup"><span data-stu-id="cc989-111">[in] The field signature as a BLOB.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="cc989-112">中中的字节数 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="cc989-112">[in] The count of bytes in `pvSigBlob`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="cc989-113">中`ELEMENT_TYPE_` *\** 常数值的。</span><span class="sxs-lookup"><span data-stu-id="cc989-113">[in] The `ELEMENT_TYPE_`*\** for the constant value.</span></span> <span data-ttu-id="cc989-114">这是一个 `CorElementType` 值。</span><span class="sxs-lookup"><span data-stu-id="cc989-114">This is a `CorElementType` value.</span></span> <span data-ttu-id="cc989-115">如果没有为字段定义常数值，请使用 `ELEMENT_TYPE_END` 。</span><span class="sxs-lookup"><span data-stu-id="cc989-115">If not defining a constant value for the field, use `ELEMENT_TYPE_END`.</span></span>  
  
 `pValue`  
 <span data-ttu-id="cc989-116">中字段的常数值。</span><span class="sxs-lookup"><span data-stu-id="cc989-116">[in] The constant value for the field.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="cc989-117">中 (Unicode) 字符的大小 `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="cc989-117">[in] The size in (Unicode) characters of `pValue`.</span></span>  
  
 `pmd`  
 <span data-ttu-id="cc989-118">弄 `mdFieldDef` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="cc989-118">[out] The `mdFieldDef` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc989-119">要求</span><span class="sxs-lookup"><span data-stu-id="cc989-119">Requirements</span></span>  

 <span data-ttu-id="cc989-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cc989-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc989-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="cc989-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cc989-122">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="cc989-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cc989-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc989-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc989-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc989-124">See also</span></span>

- [<span data-ttu-id="cc989-125">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="cc989-125">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="cc989-126">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="cc989-126">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

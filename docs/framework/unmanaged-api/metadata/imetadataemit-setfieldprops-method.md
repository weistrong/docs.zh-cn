---
description: 了解详细信息： IMetaDataEmit：： SetFieldProps 方法
title: IMetaDataEmit::SetFieldProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldProps
helpviewer_keywords:
- IMetaDataEmit::SetFieldProps method [.NET Framework metadata]
- SetFieldProps method [.NET Framework metadata]
ms.assetid: 47132dda-fa92-4bd1-ae4b-24cd9a60665a
topic_type:
- apiref
ms.openlocfilehash: ee9964077e556a1d0666a836ca0c3bab92540252
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658004"
---
# <a name="imetadataemitsetfieldprops-method"></a><span data-ttu-id="17144-103">IMetaDataEmit::SetFieldProps 方法</span><span class="sxs-lookup"><span data-stu-id="17144-103">IMetaDataEmit::SetFieldProps Method</span></span>

<span data-ttu-id="17144-104">设置或更新指定字段标记所引用的字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="17144-104">Sets or updates the default value for the field referenced by the specified field token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17144-105">语法</span><span class="sxs-lookup"><span data-stu-id="17144-105">Syntax</span></span>  
  
```cpp  
HRESULT SetFieldProps (  
    [in]  mdFieldDef  fd,
    [in]  DWORD       dwFieldFlags,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,
    [in]  ULONG       cchValue
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17144-106">参数</span><span class="sxs-lookup"><span data-stu-id="17144-106">Parameters</span></span>  

 `fd`  
 <span data-ttu-id="17144-107">中目标字段的标记。</span><span class="sxs-lookup"><span data-stu-id="17144-107">[in] The token for the target field.</span></span>  
  
 `dwFieldFlags`  
 <span data-ttu-id="17144-108">中字段特性。</span><span class="sxs-lookup"><span data-stu-id="17144-108">[in] Field attributes.</span></span> <span data-ttu-id="17144-109">这是一个值的位掩码 `CorFieldAttr` 。</span><span class="sxs-lookup"><span data-stu-id="17144-109">This is a bitmask of `CorFieldAttr` values.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="17144-110">中`ELEMENT_TYPE_` *\** 常数值的。</span><span class="sxs-lookup"><span data-stu-id="17144-110">[in] The `ELEMENT_TYPE_`*\** for the constant value.</span></span> <span data-ttu-id="17144-111">这是一个 `CorElementType` 值。</span><span class="sxs-lookup"><span data-stu-id="17144-111">This is a `CorElementType` value.</span></span> <span data-ttu-id="17144-112">如果未定义常数，请将此值设置为 `ELEMENT_TYPE_END` 。</span><span class="sxs-lookup"><span data-stu-id="17144-112">If a constant is not being defined, set this value to `ELEMENT_TYPE_END`.</span></span>  
  
 `pValue`  
 <span data-ttu-id="17144-113">中字段的常数值。</span><span class="sxs-lookup"><span data-stu-id="17144-113">[in] The constant value for the field.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="17144-114">中的大小（以 Unicode 字符为格式） `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="17144-114">[in] The size, in Unicode characters, of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17144-115">要求</span><span class="sxs-lookup"><span data-stu-id="17144-115">Requirements</span></span>  

 <span data-ttu-id="17144-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="17144-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17144-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="17144-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="17144-118">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="17144-118">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="17144-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17144-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17144-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="17144-120">See also</span></span>

- [<span data-ttu-id="17144-121">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="17144-121">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="17144-122">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="17144-122">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

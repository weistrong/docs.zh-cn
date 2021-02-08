---
description: 了解详细信息： IMetaDataEmit：： SetParamProps 方法
title: IMetaDataEmit::SetParamProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetParamProps
helpviewer_keywords:
- IMetaDataEmit::SetParamProps method [.NET Framework metadata]
- SetParamProps method [.NET Framework metadata]
ms.assetid: a95a3908-9f87-4084-937e-8e01ef03ad63
topic_type:
- apiref
ms.openlocfilehash: 35e839b05b3671c6c09f315ac636971c386e766e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772012"
---
# <a name="imetadataemitsetparamprops-method"></a><span data-ttu-id="33172-103">IMetaDataEmit::SetParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="33172-103">IMetaDataEmit::SetParamProps Method</span></span>

<span data-ttu-id="33172-104">设置或更改之前调用 [IMetaDataEmit：:D efineparam](imetadataemit-defineparam-method.md)时定义的方法参数的功能。</span><span class="sxs-lookup"><span data-stu-id="33172-104">Sets or changes features of a method parameter that was defined by a prior call to [IMetaDataEmit::DefineParam](imetadataemit-defineparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33172-105">语法</span><span class="sxs-lookup"><span data-stu-id="33172-105">Syntax</span></span>  
  
```cpp  
HRESULT SetParamProps (
    [in]  mdParamDef  pd,
    [in]  LPCWSTR     szName,
    [in]  DWORD       dwParamFlags,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,
    [in]  ULONG       cchValue
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="33172-106">参数</span><span class="sxs-lookup"><span data-stu-id="33172-106">Parameters</span></span>  

 `pd`  
 <span data-ttu-id="33172-107">中目标参数的标记。</span><span class="sxs-lookup"><span data-stu-id="33172-107">[in] The token for the target parameter.</span></span>  
  
 `szName`  
 <span data-ttu-id="33172-108">中Unicode 中参数的名称。</span><span class="sxs-lookup"><span data-stu-id="33172-108">[in] The name of the parameter in Unicode.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="33172-109">中参数的标志。</span><span class="sxs-lookup"><span data-stu-id="33172-109">[in] The flags for the parameter.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="33172-110">中常量值的 ELEMENT_TYPE_ \*。</span><span class="sxs-lookup"><span data-stu-id="33172-110">[in] The ELEMENT_TYPE_\* for the constant value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="33172-111">中参数的常数值。</span><span class="sxs-lookup"><span data-stu-id="33172-111">[in] The constant value for the parameter.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="33172-112">中 (Unicode) 字符的大小 `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="33172-112">[in] The size in (Unicode) characters of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="33172-113">要求</span><span class="sxs-lookup"><span data-stu-id="33172-113">Requirements</span></span>  

 <span data-ttu-id="33172-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="33172-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33172-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="33172-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="33172-116">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="33172-116">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="33172-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33172-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33172-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="33172-118">See also</span></span>

- [<span data-ttu-id="33172-119">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="33172-119">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="33172-120">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="33172-120">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

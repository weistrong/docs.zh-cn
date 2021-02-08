---
description: 了解详细信息： IMetaDataEmit：:D efineParam 方法
title: IMetaDataEmit::DefineParam 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineParam
helpviewer_keywords:
- IMetaDataEmit::DefineParam method [.NET Framework metadata]
- DefineParam method [.NET Framework metadata]
ms.assetid: d86a3d14-4796-4909-9591-dfafe3de5ce4
topic_type:
- apiref
ms.openlocfilehash: 300de3183b329773a8e6813d6b92c6d049d63195
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784088"
---
# <a name="imetadataemitdefineparam-method"></a><span data-ttu-id="47ad7-103">IMetaDataEmit::DefineParam 方法</span><span class="sxs-lookup"><span data-stu-id="47ad7-103">IMetaDataEmit::DefineParam Method</span></span>

<span data-ttu-id="47ad7-104">创建具有指定标记所引用的方法的指定签名的参数定义，并获取该参数定义的标记。</span><span class="sxs-lookup"><span data-stu-id="47ad7-104">Creates a parameter definition with the specified signature for the method referenced by the specified token, and gets a token for that parameter definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47ad7-105">语法</span><span class="sxs-lookup"><span data-stu-id="47ad7-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineParam (  
    [in]  mdMethodDef md,
    [in]  ULONG       ulParamSeq,
    [in]  LPCWSTR     szName,
    [in]  DWORD       dwParamFlags,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,  
    [in]  ULONG       cchValue,
    [out] mdParamDef  *ppd
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="47ad7-106">参数</span><span class="sxs-lookup"><span data-stu-id="47ad7-106">Parameters</span></span>  

 `md`  
 <span data-ttu-id="47ad7-107">中正在定义其参数的方法的标记。</span><span class="sxs-lookup"><span data-stu-id="47ad7-107">[in] The token for the method whose parameter is being defined.</span></span>  
  
 `ulParamSeq`  
 <span data-ttu-id="47ad7-108">中参数序列号。</span><span class="sxs-lookup"><span data-stu-id="47ad7-108">[in] The parameter sequence number.</span></span>  
  
 `szName`  
 <span data-ttu-id="47ad7-109">中Unicode 中参数的名称。</span><span class="sxs-lookup"><span data-stu-id="47ad7-109">[in] The name of the parameter in Unicode.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="47ad7-110">中参数的标志。</span><span class="sxs-lookup"><span data-stu-id="47ad7-110">[in] Flags for the parameter.</span></span> <span data-ttu-id="47ad7-111">这是一个值的位掩码 `CorParamAttr` 。</span><span class="sxs-lookup"><span data-stu-id="47ad7-111">This is a bitmask of `CorParamAttr` values.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="47ad7-112">[in] `ELEMENT_TYPE_` *\** 用于常量值。</span><span class="sxs-lookup"><span data-stu-id="47ad7-112">[in] `ELEMENT_TYPE_`*\** for the constant value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="47ad7-113">中参数的常数值。</span><span class="sxs-lookup"><span data-stu-id="47ad7-113">[in] The constant value for the parameter.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="47ad7-114">中的大小（以 Unicode 字符为格式） `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="47ad7-114">[in] The size, in Unicode characters, of `pValue`.</span></span>  
  
 `ppd`  
 <span data-ttu-id="47ad7-115">弄 `mdParamDef` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="47ad7-115">[out] The `mdParamDef` token assigned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="47ad7-116">备注</span><span class="sxs-lookup"><span data-stu-id="47ad7-116">Remarks</span></span>  

 <span data-ttu-id="47ad7-117">参数的序列值 `ulParamSeq` 从1开始。</span><span class="sxs-lookup"><span data-stu-id="47ad7-117">The sequence values in `ulParamSeq` begin with 1 for parameters.</span></span> <span data-ttu-id="47ad7-118">返回值的序列号为0。</span><span class="sxs-lookup"><span data-stu-id="47ad7-118">A return value has a sequence number of 0.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47ad7-119">要求</span><span class="sxs-lookup"><span data-stu-id="47ad7-119">Requirements</span></span>  

 <span data-ttu-id="47ad7-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="47ad7-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="47ad7-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="47ad7-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="47ad7-122">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="47ad7-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="47ad7-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="47ad7-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47ad7-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="47ad7-124">See also</span></span>

- [<span data-ttu-id="47ad7-125">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="47ad7-125">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="47ad7-126">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="47ad7-126">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

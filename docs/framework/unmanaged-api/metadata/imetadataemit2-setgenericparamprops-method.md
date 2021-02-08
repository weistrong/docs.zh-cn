---
description: 了解详细信息： IMetaDataEmit2：： SetGenericParamProps 方法
title: IMetaDataEmit2::SetGenericParamProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SetGenericParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SetGenericParamProps
helpviewer_keywords:
- IMetaDataEmit2::SetGenericParamProps method [.NET Framework metadata]
- SetGenericParamProps method [.NET Framework metadata]
ms.assetid: cd93a48d-1fed-4706-bec6-a05dc3b64fbd
topic_type:
- apiref
ms.openlocfilehash: 9c6946bbd301450203bc6fb2b1202352119dc792
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771634"
---
# <a name="imetadataemit2setgenericparamprops-method"></a><span data-ttu-id="ffb38-103">IMetaDataEmit2::SetGenericParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="ffb38-103">IMetaDataEmit2::SetGenericParamProps Method</span></span>

<span data-ttu-id="ffb38-104">设置指定的标记所引用的泛型参数定义的属性值。</span><span class="sxs-lookup"><span data-stu-id="ffb38-104">Sets property values for the generic parameter definition referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffb38-105">语法</span><span class="sxs-lookup"><span data-stu-id="ffb38-105">Syntax</span></span>  
  
```cpp  
HRESULT SetGenericParamProps (  
    [in] mdGenericParam   gp,
    [in] DWORD            dwParamFlags,
    [in] LPCWSTR          szName,
    [in] DWORD            reserved,
    [in] mdToken          rtkConstraints[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ffb38-106">参数</span><span class="sxs-lookup"><span data-stu-id="ffb38-106">Parameters</span></span>  

 `gp`  
 <span data-ttu-id="ffb38-107">中要为其设置值的泛型参数定义的标记。</span><span class="sxs-lookup"><span data-stu-id="ffb38-107">[in] The token for the generic parameter definition for which to set values.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="ffb38-108">中描述泛型参数类型的 [CorGenericParamAttr](corgenericparamattr-enumeration.md) 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="ffb38-108">[in] A value of the [CorGenericParamAttr](corgenericparamattr-enumeration.md) enumeration that describes the type for the generic parameter.</span></span>  
  
 `szName`  
 <span data-ttu-id="ffb38-109">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="ffb38-109">[in] Optional.</span></span> <span data-ttu-id="ffb38-110">要为其设置值的参数的名称。</span><span class="sxs-lookup"><span data-stu-id="ffb38-110">The name of the parameter for which to set values.</span></span>  
  
 `reserved`  
 <span data-ttu-id="ffb38-111">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="ffb38-111">[in] Reserved for future extensibility.</span></span>  
  
 `rtkConstraints`  
 <span data-ttu-id="ffb38-112">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="ffb38-112">[in] Optional.</span></span> <span data-ttu-id="ffb38-113">类型约束的零终止数组。</span><span class="sxs-lookup"><span data-stu-id="ffb38-113">A zero-terminated array of type constraints.</span></span> <span data-ttu-id="ffb38-114">数组成员必须是 `mdTypeDef` 、 `mdTypeRef` 或 `mdTypeSpec` 元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ffb38-114">Array members must be an `mdTypeDef`, `mdTypeRef`, or `mdTypeSpec` metadata token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffb38-115">要求</span><span class="sxs-lookup"><span data-stu-id="ffb38-115">Requirements</span></span>  

 <span data-ttu-id="ffb38-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ffb38-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffb38-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ffb38-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ffb38-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="ffb38-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ffb38-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffb38-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffb38-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="ffb38-120">See also</span></span>

- [<span data-ttu-id="ffb38-121">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="ffb38-121">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="ffb38-122">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="ffb38-122">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)

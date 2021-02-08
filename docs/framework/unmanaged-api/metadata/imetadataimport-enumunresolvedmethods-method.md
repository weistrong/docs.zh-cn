---
description: 了解详细信息： IMetaDataImport：： EnumUnresolvedMethods 方法
title: IMetaDataImport::EnumUnresolvedMethods 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUnresolvedMethods
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUnresolvedMethods
helpviewer_keywords:
- EnumUnresolvedMethods method [.NET Framework metadata]
- IMetaDataImport::EnumUnresolvedMethods method [.NET Framework metadata]
ms.assetid: eb3187d7-74cf-44b1-aeeb-7a8d2b60e3b7
topic_type:
- apiref
ms.openlocfilehash: e894ecdde91a2263783234d73fa50d890a13e413
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799325"
---
# <a name="imetadataimportenumunresolvedmethods-method"></a><span data-ttu-id="f4ed2-103">IMetaDataImport::EnumUnresolvedMethods 方法</span><span class="sxs-lookup"><span data-stu-id="f4ed2-103">IMetaDataImport::EnumUnresolvedMethods Method</span></span>

<span data-ttu-id="f4ed2-104">枚举表示当前元数据范围内未解析的方法的 MemberDef 标记。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-104">Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4ed2-105">语法</span><span class="sxs-lookup"><span data-stu-id="f4ed2-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumUnresolvedMethods (  
   [in, out] HCORENUM    *phEnum,  
   [out]     mdToken     rMethods[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f4ed2-106">参数</span><span class="sxs-lookup"><span data-stu-id="f4ed2-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="f4ed2-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="f4ed2-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-108">This must be NULL for the first call of this method.</span></span>  
  
 `rMethods`  
 <span data-ttu-id="f4ed2-109">弄用于存储 MemberDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-109">[out] The array used to store the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="f4ed2-110">[in] `rMethods` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-110">[in] The maximum size of the `rMethods` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="f4ed2-111">弄中返回的 MemberDef 令牌数 `rMethods` 。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-111">[out] The number of MemberDef tokens returned in `rMethods`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f4ed2-112">返回值</span><span class="sxs-lookup"><span data-stu-id="f4ed2-112">Return Value</span></span>  
  
|<span data-ttu-id="f4ed2-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f4ed2-113">HRESULT</span></span>|<span data-ttu-id="f4ed2-114">说明</span><span class="sxs-lookup"><span data-stu-id="f4ed2-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="f4ed2-115">`EnumUnresolvedMethods` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-115">`EnumUnresolvedMethods` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="f4ed2-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="f4ed2-117">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-117">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f4ed2-118">备注</span><span class="sxs-lookup"><span data-stu-id="f4ed2-118">Remarks</span></span>  

 <span data-ttu-id="f4ed2-119">未解析的方法是已声明但未实现的方法。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-119">An unresolved method is one that has been declared but not implemented.</span></span> <span data-ttu-id="f4ed2-120">如果方法已标记 `miForwardRef` 并且 `mdPinvokeImpl` 或 `miRuntime` 设置为零，则枚举中将包含方法。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-120">A method is included in the enumeration if the method is marked `miForwardRef` and either `mdPinvokeImpl` or `miRuntime` is set to zero.</span></span> <span data-ttu-id="f4ed2-121">换句话说，未解析的方法是已标记 `miForwardRef` 但未在非托管代码中实现的类方法 (通过 PInvoke) 或由运行时本身内部实现</span><span class="sxs-lookup"><span data-stu-id="f4ed2-121">In other words, an unresolved method is a class method that is marked `miForwardRef` but which is not implemented in unmanaged code (reached via PInvoke) nor implemented internally by the runtime itself</span></span>  
  
 <span data-ttu-id="f4ed2-122">枚举排除在模块范围 (全局) 或接口或抽象类中定义的所有方法。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-122">The enumeration excludes all methods that are defined either at module scope (globals) or in interfaces or abstract classes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4ed2-123">要求</span><span class="sxs-lookup"><span data-stu-id="f4ed2-123">Requirements</span></span>  

 <span data-ttu-id="f4ed2-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f4ed2-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4ed2-125">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f4ed2-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f4ed2-126">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f4ed2-126">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f4ed2-127">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4ed2-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4ed2-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="f4ed2-128">See also</span></span>

- [<span data-ttu-id="f4ed2-129">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f4ed2-129">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f4ed2-130">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f4ed2-130">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

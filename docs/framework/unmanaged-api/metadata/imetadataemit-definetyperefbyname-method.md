---
description: 了解详细信息： IMetaDataEmit：:D efineTypeRefByName 方法
title: IMetaDataEmit::DefineTypeRefByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineTypeRefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeRefByName
helpviewer_keywords:
- DefineTypeRefByName method [.NET Framework metadata]
- IMetaDataEmit::DefineTypeRefByName method [.NET Framework metadata]
ms.assetid: c30a4ce3-2d3e-411a-98df-e62ac4a5dd50
topic_type:
- apiref
ms.openlocfilehash: 836516e06105bb8ebc7c9bacf7b7d3837bf89eec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784010"
---
# <a name="imetadataemitdefinetyperefbyname-method"></a><span data-ttu-id="04334-103">IMetaDataEmit::DefineTypeRefByName 方法</span><span class="sxs-lookup"><span data-stu-id="04334-103">IMetaDataEmit::DefineTypeRefByName Method</span></span>

<span data-ttu-id="04334-104">获取在指定范围内定义的类型（位于当前范围之外）的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="04334-104">Gets a metadata token for a type that is defined in the specified scope, which is outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04334-105">语法</span><span class="sxs-lookup"><span data-stu-id="04334-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineTypeRefByName (
    [in]  mdToken     tkResolutionScope,
    [in]  LPCWSTR     szName,
    [out] mdTypeRef   *ptr
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="04334-106">参数</span><span class="sxs-lookup"><span data-stu-id="04334-106">Parameters</span></span>  

 `tkResolutionScope`  
 <span data-ttu-id="04334-107">中指定解析范围的标记。</span><span class="sxs-lookup"><span data-stu-id="04334-107">[in] The token specifying the resolution scope.</span></span> <span data-ttu-id="04334-108">以下令牌类型有效：</span><span class="sxs-lookup"><span data-stu-id="04334-108">The following token types are valid:</span></span>  
  
- <span data-ttu-id="04334-109">`mdModuleRef`如果在定义调用方的同一程序集中定义了该类型，则为。</span><span class="sxs-lookup"><span data-stu-id="04334-109">`mdModuleRef`, if the type is defined in the same assembly in which the caller is defined.</span></span>  
  
- <span data-ttu-id="04334-110">`mdAssemblyRef`如果类型是在定义调用方的程序集中定义的，则为。</span><span class="sxs-lookup"><span data-stu-id="04334-110">`mdAssemblyRef`, if the type is defined in an assembly other than the one in which the caller is defined.</span></span>  
  
- <span data-ttu-id="04334-111">`mdTypeRef`如果类型是嵌套类型，则为。</span><span class="sxs-lookup"><span data-stu-id="04334-111">`mdTypeRef`, if the type is a nested type.</span></span>  
  
- <span data-ttu-id="04334-112">`mdModule`如果在定义调用方的同一模块中定义了该类型，则为。</span><span class="sxs-lookup"><span data-stu-id="04334-112">`mdModule`, if the type is defined in the same module in which the caller is defined.</span></span>  
  
- <span data-ttu-id="04334-113">如果类型是全局定义的，则为 Null。</span><span class="sxs-lookup"><span data-stu-id="04334-113">Null, if the type is defined globally.</span></span>  
  
 `szName`  
 <span data-ttu-id="04334-114">中Unicode 中目标类型的名称。</span><span class="sxs-lookup"><span data-stu-id="04334-114">[in] The name of the target type in Unicode.</span></span>  
  
 `ptr`  
 <span data-ttu-id="04334-115">弄指向分配给类型的标记的指针 `mdTypeRef` 。</span><span class="sxs-lookup"><span data-stu-id="04334-115">[out] A pointer to the `mdTypeRef` token that is assigned to the type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04334-116">要求</span><span class="sxs-lookup"><span data-stu-id="04334-116">Requirements</span></span>  

 <span data-ttu-id="04334-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="04334-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04334-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="04334-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="04334-119">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="04334-119">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="04334-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04334-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04334-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="04334-121">See also</span></span>

- [<span data-ttu-id="04334-122">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="04334-122">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="04334-123">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="04334-123">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

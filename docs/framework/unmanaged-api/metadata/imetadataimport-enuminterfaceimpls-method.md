---
description: 了解详细信息： IMetaDataImport：： EnumInterfaceImpls 方法
title: IMetaDataImport::EnumInterfaceImpls 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumInterfaceImpls
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumInterfaceImpls
helpviewer_keywords:
- IMetaDataImport::EnumInterfaceImpls method [.NET Framework metadata]
- EnumInterfaceImpls method [.NET Framework metadata]
ms.assetid: ba6e178f-128b-4e47-a13c-b4be73eb106c
topic_type:
- apiref
ms.openlocfilehash: 5276d1edb3be0cae76b18a06241dc6b9952e1a72
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649398"
---
# <a name="imetadataimportenuminterfaceimpls-method"></a><span data-ttu-id="95fc7-103">IMetaDataImport::EnumInterfaceImpls 方法</span><span class="sxs-lookup"><span data-stu-id="95fc7-103">IMetaDataImport::EnumInterfaceImpls Method</span></span>

<span data-ttu-id="95fc7-104">枚举由指定实现的所有接口 `TypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="95fc7-104">Enumerates all interfaces implemented by the specified `TypeDef`.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="95fc7-105">语法</span><span class="sxs-lookup"><span data-stu-id="95fc7-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumInterfaceImpls (  
   [in, out]  HCORENUM       *phEnum,
   [in]   mdTypeDef          td,  
   [out]  mdInterfaceImpl    rImpls[],
   [in]   ULONG              cMax,  
   [out]  ULONG*             pcImpls  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="95fc7-106">参数</span><span class="sxs-lookup"><span data-stu-id="95fc7-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="95fc7-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="95fc7-107">[in, out] A pointer to the enumerator.</span></span>  
  
 `td`  
 <span data-ttu-id="95fc7-108">中要枚举其 MethodDef 标记表示接口实现的 TypeDef 的标记。</span><span class="sxs-lookup"><span data-stu-id="95fc7-108">[in] The token of the TypeDef whose MethodDef tokens representing interface implementations are to be enumerated.</span></span>  
  
 `rImpls`  
 <span data-ttu-id="95fc7-109">弄用于存储 MethodDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="95fc7-109">[out] The array used to store the MethodDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="95fc7-110">中数组的最大长度 `rImpls` 。</span><span class="sxs-lookup"><span data-stu-id="95fc7-110">[in] The maximum length of the `rImpls` array.</span></span>  
  
 `pcImpls`  
 <span data-ttu-id="95fc7-111">弄返回的标记的实际数量 `rImpls` 。</span><span class="sxs-lookup"><span data-stu-id="95fc7-111">[out] The actual number of tokens returned in `rImpls`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="95fc7-112">返回值</span><span class="sxs-lookup"><span data-stu-id="95fc7-112">Return Value</span></span>  
  
|<span data-ttu-id="95fc7-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="95fc7-113">HRESULT</span></span>|<span data-ttu-id="95fc7-114">说明</span><span class="sxs-lookup"><span data-stu-id="95fc7-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="95fc7-115">`EnumInterfaceImpls` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="95fc7-115">`EnumInterfaceImpls` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="95fc7-116">没有要枚举的 MethodDef 标记。</span><span class="sxs-lookup"><span data-stu-id="95fc7-116">There are no MethodDef tokens to enumerate.</span></span> <span data-ttu-id="95fc7-117">在这种情况下， `pcImpls` 设置为零。</span><span class="sxs-lookup"><span data-stu-id="95fc7-117">In that case, `pcImpls` is set to zero.</span></span>|  

## <a name="remarks"></a><span data-ttu-id="95fc7-118">备注</span><span class="sxs-lookup"><span data-stu-id="95fc7-118">Remarks</span></span>

<span data-ttu-id="95fc7-119">枚举返回 `mdInterfaceImpl` 由指定的实现的每个接口的令牌集合 `TypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="95fc7-119">The enumeration returns a collection of `mdInterfaceImpl` tokens for each interface implemented by the specified `TypeDef`.</span></span> <span data-ttu-id="95fc7-120">通过或)  (指定接口的顺序来返回接口令牌 `DefineTypeDef` `SetTypeDefProps` 。</span><span class="sxs-lookup"><span data-stu-id="95fc7-120">Interface tokens are returned in the order the interfaces were specified (through `DefineTypeDef` or `SetTypeDefProps`).</span></span> <span data-ttu-id="95fc7-121">`mdInterfaceImpl`可以使用[GetInterfaceImplProps](imetadataimport-getinterfaceimplprops-method.md)查询返回的标记的属性。</span><span class="sxs-lookup"><span data-stu-id="95fc7-121">Properties of the returned `mdInterfaceImpl` tokens can be queried using [GetInterfaceImplProps](imetadataimport-getinterfaceimplprops-method.md).</span></span>
  
## <a name="requirements"></a><span data-ttu-id="95fc7-122">要求</span><span class="sxs-lookup"><span data-stu-id="95fc7-122">Requirements</span></span>  

 <span data-ttu-id="95fc7-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="95fc7-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95fc7-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="95fc7-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="95fc7-125">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="95fc7-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="95fc7-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95fc7-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95fc7-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="95fc7-127">See also</span></span>

- [<span data-ttu-id="95fc7-128">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="95fc7-128">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="95fc7-129">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="95fc7-129">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

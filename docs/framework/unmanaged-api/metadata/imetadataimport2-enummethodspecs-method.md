---
description: 了解详细信息： IMetaDataImport2：： EnumMethodSpecs 方法
title: IMetaDataImport2::EnumMethodSpecs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumMethodSpecs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumMethodSpecs
helpviewer_keywords:
- IMetaDataImport2::EnumMethodSpecs method [.NET Framework metadata]
- EnumMethodSpecs method [.NET Framework metadata]
ms.assetid: b3fc1e6c-bcb6-4915-baf8-7dc0a31b8724
topic_type:
- apiref
ms.openlocfilehash: 19fff1d78599d968bb1fd0ab27b0f71e41fae20b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677517"
---
# <a name="imetadataimport2enummethodspecs-method"></a><span data-ttu-id="4e4d1-103">IMetaDataImport2::EnumMethodSpecs 方法</span><span class="sxs-lookup"><span data-stu-id="4e4d1-103">IMetaDataImport2::EnumMethodSpecs Method</span></span>

<span data-ttu-id="4e4d1-104">获取与指定的 MethodDef 或 MemberRef 标记相关联的 MethodSpec 标记数组的枚举器。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-104">Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e4d1-105">语法</span><span class="sxs-lookup"><span data-stu-id="4e4d1-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMethodSpecs (  
    [in, out] HCORENUM      *phEnum,
    [in]      mdToken       tk,  
    [out]     mdMethodSpec  rMethodSpecs[],  
    [in]      ULONG         cMax,  
    [out]     ULONG         *pcMethodSpecs  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="4e4d1-106">参数</span><span class="sxs-lookup"><span data-stu-id="4e4d1-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="4e4d1-107">[in，out]指向的枚举器的指针 `rMethodSpecs` 。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-107">[in, out] A pointer to the enumerator for `rMethodSpecs`.</span></span>  
  
 `tk`  
 <span data-ttu-id="4e4d1-108">中MemberRef 或 MethodDef 标记，表示要枚举其 MethodSpec 标记的方法。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-108">[in] The MemberRef or MethodDef token that represents the method whose MethodSpec tokens are to be enumerated.</span></span> <span data-ttu-id="4e4d1-109">如果的值 `tk` 为 0 (零) ，则将枚举范围内的所有 MethodSpec 标记。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-109">If the value of `tk` is 0 (zero), all MethodSpec tokens in the scope will be enumerated.</span></span>  
  
 `rMethodSpecs`  
 <span data-ttu-id="4e4d1-110">弄要枚举的 MethodSpec 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-110">[out] The array of MethodSpec tokens to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="4e4d1-111">中要放入的请求的最大数量 `rMethodSpecs` 。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-111">[in] The requested maximum number of tokens to place in `rMethodSpecs`.</span></span>  
  
 `pcMethodSpecs`  
 <span data-ttu-id="4e4d1-112">弄放入的标记数 `rMethodSpecs` 。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-112">[out] The returned number of tokens placed in `rMethodSpecs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4e4d1-113">返回值</span><span class="sxs-lookup"><span data-stu-id="4e4d1-113">Return Value</span></span>  
  
|<span data-ttu-id="4e4d1-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4e4d1-114">HRESULT</span></span>|<span data-ttu-id="4e4d1-115">说明</span><span class="sxs-lookup"><span data-stu-id="4e4d1-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="4e4d1-116">`EnumMethodSpecs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-116">`EnumMethodSpecs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="4e4d1-117">`phEnum` 没有成员元素。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-117">`phEnum` has no member elements.</span></span> <span data-ttu-id="4e4d1-118">在这种情况下， `pcMethodSpecs` 设置为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-118">In this case, `pcMethodSpecs` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4e4d1-119">要求</span><span class="sxs-lookup"><span data-stu-id="4e4d1-119">Requirements</span></span>  

 <span data-ttu-id="4e4d1-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4e4d1-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e4d1-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="4e4d1-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4e4d1-122">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="4e4d1-122">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4e4d1-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e4d1-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e4d1-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="4e4d1-124">See also</span></span>

- [<span data-ttu-id="4e4d1-125">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="4e4d1-125">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="4e4d1-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="4e4d1-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)

---
description: 了解详细信息： IMetaDataImport2：： GetGenericParamConstraintProps 方法
title: IMetaDataImport2::GetGenericParamConstraintProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetGenericParamConstraintProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetGenericParamConstraintProps
helpviewer_keywords:
- IMetaDataImport2::GetGenericParamConstraintProps method [.NET Framework metadata]
- GetGenericParamConstraintProps method [.NET Framework metadata]
ms.assetid: c5fee4a0-b132-4e5e-8730-e586ce314b9a
topic_type:
- apiref
ms.openlocfilehash: 03cc4df655f9ab7a1c04840e9d4fa782a90ce1ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688736"
---
# <a name="imetadataimport2getgenericparamconstraintprops-method"></a><span data-ttu-id="04ce9-103">IMetaDataImport2::GetGenericParamConstraintProps 方法</span><span class="sxs-lookup"><span data-stu-id="04ce9-103">IMetaDataImport2::GetGenericParamConstraintProps Method</span></span>

<span data-ttu-id="04ce9-104">获取与指定约束标记所表示的泛型参数约束关联的元数据。</span><span class="sxs-lookup"><span data-stu-id="04ce9-104">Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04ce9-105">语法</span><span class="sxs-lookup"><span data-stu-id="04ce9-105">Syntax</span></span>  
  
```cpp  
HRESULT GetGenericParamConstraintProps (  
   [in]  mdGenericParamConstraint  gpc,  
   [out] mdGenericParam            *ptGenericParam,  
   [out] mdToken                   *ptkConstraintType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="04ce9-106">参数</span><span class="sxs-lookup"><span data-stu-id="04ce9-106">Parameters</span></span>  

 `gpc`  
 <span data-ttu-id="04ce9-107">中要为其返回元数据的泛型参数约束的标记。</span><span class="sxs-lookup"><span data-stu-id="04ce9-107">[in] The token to the generic parameter constraint for which to return the metadata.</span></span>  
  
 `ptGenericParam`  
 <span data-ttu-id="04ce9-108">弄指向表示受约束的泛型参数的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="04ce9-108">[out] A pointer to the token that represents the generic parameter that is constrained.</span></span>  
  
 `ptkConstraintType`  
 <span data-ttu-id="04ce9-109">弄一个指针，指向表示上的约束的 TypeDef、TypeRef 或 TypeSpec 标记 `ptGenericParam` 。</span><span class="sxs-lookup"><span data-stu-id="04ce9-109">[out] A pointer to a TypeDef, TypeRef, or TypeSpec token that represents a constraint on `ptGenericParam`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04ce9-110">要求</span><span class="sxs-lookup"><span data-stu-id="04ce9-110">Requirements</span></span>  

 <span data-ttu-id="04ce9-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="04ce9-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04ce9-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="04ce9-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="04ce9-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="04ce9-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="04ce9-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04ce9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04ce9-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="04ce9-115">See also</span></span>

- [<span data-ttu-id="04ce9-116">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="04ce9-116">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="04ce9-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="04ce9-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)

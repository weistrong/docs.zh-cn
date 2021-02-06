---
description: 了解详细信息： IMetaDataEmit：： SetFieldMarshal 方法
title: IMetaDataEmit::SetFieldMarshal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldMarshal
helpviewer_keywords:
- SetFieldMarshal method [.NET Framework metadata]
- IMetaDataEmit::SetFieldMarshal method [.NET Framework metadata]
ms.assetid: be232314-7f69-4855-bfab-63361bd22307
topic_type:
- apiref
ms.openlocfilehash: 4694487479b0249e875abfd9ecd963a5dc404d46
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658043"
---
# <a name="imetadataemitsetfieldmarshal-method"></a><span data-ttu-id="3ec46-103">IMetaDataEmit::SetFieldMarshal 方法</span><span class="sxs-lookup"><span data-stu-id="3ec46-103">IMetaDataEmit::SetFieldMarshal Method</span></span>

<span data-ttu-id="3ec46-104">为指定的标记引用的字段、方法返回或方法参数设置 PInvoke 封送处理信息。</span><span class="sxs-lookup"><span data-stu-id="3ec46-104">Sets the PInvoke marshaling information for the field, method return, or method parameter referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ec46-105">语法</span><span class="sxs-lookup"><span data-stu-id="3ec46-105">Syntax</span></span>  
  
```cpp  
HRESULT SetFieldMarshal (  
    [in]  mdToken          tk,
    [in]  PCCOR_SIGNATURE  pvNativeType,
    [in]  ULONG            cbNativeType
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3ec46-106">参数</span><span class="sxs-lookup"><span data-stu-id="3ec46-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="3ec46-107">中目标数据项的标记。</span><span class="sxs-lookup"><span data-stu-id="3ec46-107">[in] The token for target data item.</span></span> <span data-ttu-id="3ec46-108">这是 `mdFieldDef` 或 `mdParamDef` 令牌。</span><span class="sxs-lookup"><span data-stu-id="3ec46-108">This is either a `mdFieldDef` or a `mdParamDef` token.</span></span>  
  
 `pvNativeType`  
 <span data-ttu-id="3ec46-109">中非托管类型的签名。</span><span class="sxs-lookup"><span data-stu-id="3ec46-109">[in] The signature for unmanaged type.</span></span>  
  
 `cbNativeType`  
 <span data-ttu-id="3ec46-110">中中的字节数 `pvNativeType` 。</span><span class="sxs-lookup"><span data-stu-id="3ec46-110">[in] The count of bytes in `pvNativeType`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ec46-111">要求</span><span class="sxs-lookup"><span data-stu-id="3ec46-111">Requirements</span></span>  

 <span data-ttu-id="3ec46-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3ec46-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3ec46-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3ec46-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3ec46-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3ec46-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3ec46-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ec46-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ec46-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="3ec46-116">See also</span></span>

- [<span data-ttu-id="3ec46-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="3ec46-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="3ec46-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="3ec46-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

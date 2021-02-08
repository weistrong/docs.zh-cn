---
description: 了解详细信息： IMetaDataImport：： GetMethodSemantics 方法
title: IMetaDataImport::GetMethodSemantics 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMethodSemantics
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMethodSemantics
helpviewer_keywords:
- GetMethodSemantics method [.NET Framework metadata]
- IMetaDataImport::GetMethodSemantics method [.NET Framework metadata]
ms.assetid: 5e018eaa-d60e-4a0b-a2c5-8c36bd09d905
topic_type:
- apiref
ms.openlocfilehash: 2b17e2ffaeef3a451850ce2cc9c4861d68df3a81
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783854"
---
# <a name="imetadataimportgetmethodsemantics-method"></a><span data-ttu-id="478d5-103">IMetaDataImport::GetMethodSemantics 方法</span><span class="sxs-lookup"><span data-stu-id="478d5-103">IMetaDataImport::GetMethodSemantics Method</span></span>

<span data-ttu-id="478d5-104">获取指示指定的 MethodDef 标记所引用的方法与指定的 EventProp 标记所引用的成对属性和事件之间的关系的标志。</span><span class="sxs-lookup"><span data-stu-id="478d5-104">Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="478d5-105">语法</span><span class="sxs-lookup"><span data-stu-id="478d5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodSemantics (  
   [in]  mdMethodDef   mb,  
   [in]  mdToken       tkEventProp,  
   [out] DWORD         *pdwSemanticsFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="478d5-106">参数</span><span class="sxs-lookup"><span data-stu-id="478d5-106">Parameters</span></span>  

 `mb`  
 <span data-ttu-id="478d5-107">中一个 MethodDef 标记，表示要获取其语义角色信息的方法。</span><span class="sxs-lookup"><span data-stu-id="478d5-107">[in] A MethodDef token representing the method to get the semantic role information for.</span></span>  
  
 `tkEventProp`  
 <span data-ttu-id="478d5-108">中一个标记，它表示要为其获取方法的角色的成对属性和事件。</span><span class="sxs-lookup"><span data-stu-id="478d5-108">[in] A token representing the paired property and event for which to get the method's role.</span></span>  
  
 `pdwSemanticsFlags`  
 <span data-ttu-id="478d5-109">弄指向关联语义标志的指针。</span><span class="sxs-lookup"><span data-stu-id="478d5-109">[out] A pointer to the associated semantics flags.</span></span> <span data-ttu-id="478d5-110">此值是 [CorMethodSemanticsAttr](cormethodsemanticsattr-enumeration.md) 枚举中的位掩码。</span><span class="sxs-lookup"><span data-stu-id="478d5-110">This value is a bitmask from the [CorMethodSemanticsAttr](cormethodsemanticsattr-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="478d5-111">备注</span><span class="sxs-lookup"><span data-stu-id="478d5-111">Remarks</span></span>  

 <span data-ttu-id="478d5-112">[IMetaDataEmit：:D efineproperty](imetadataemit-defineproperty-method.md)方法设置方法的语义标志。</span><span class="sxs-lookup"><span data-stu-id="478d5-112">The [IMetaDataEmit::DefineProperty](imetadataemit-defineproperty-method.md) method sets a method's semantics flags.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="478d5-113">要求</span><span class="sxs-lookup"><span data-stu-id="478d5-113">Requirements</span></span>  

 <span data-ttu-id="478d5-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="478d5-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="478d5-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="478d5-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="478d5-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="478d5-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="478d5-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="478d5-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="478d5-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="478d5-118">See also</span></span>

- [<span data-ttu-id="478d5-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="478d5-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="478d5-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="478d5-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

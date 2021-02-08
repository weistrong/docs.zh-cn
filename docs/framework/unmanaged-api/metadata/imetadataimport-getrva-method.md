---
description: 了解详细信息： IMetaDataImport：： GetRVA 方法
title: IMetaDataImport::GetRVA 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetRVA
helpviewer_keywords:
- GetRVA method [.NET Framework metadata]
- IMetaDataImport::GetRVA method [.NET Framework metadata]
ms.assetid: ea422217-988b-4acd-b2db-c55357938275
topic_type:
- apiref
ms.openlocfilehash: 8d6439bcad50a6311e7bb1408f4c86144a5026ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789159"
---
# <a name="imetadataimportgetrva-method"></a><span data-ttu-id="2a6b6-103">IMetaDataImport::GetRVA 方法</span><span class="sxs-lookup"><span data-stu-id="2a6b6-103">IMetaDataImport::GetRVA Method</span></span>

<span data-ttu-id="2a6b6-104">获取指定标记所表示的方法或字段的相对虚拟地址 (RVA) 和实现标志。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-104">Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a6b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="2a6b6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRVA (  
   [in]  mdToken     tk,
   [out] ULONG       *pulCodeRVA,
   [out]  DWORD      *pdwImplFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2a6b6-106">参数</span><span class="sxs-lookup"><span data-stu-id="2a6b6-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="2a6b6-107">中一个 MethodDef 或 FieldDef 元数据标记，它表示要为其返回 RVA 的代码对象。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-107">[in] A MethodDef or FieldDef metadata token that represents the code object to return the RVA for.</span></span> <span data-ttu-id="2a6b6-108">如果标记为 FieldDef，则字段必须是全局变量。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-108">If the token is a FieldDef, the field must be a global variable.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="2a6b6-109">弄指向由标记表示的代码对象的相对虚拟地址的指针。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-109">[out] A pointer to the relative virtual address of the code object represented by the token.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="2a6b6-110">弄一个指针，指向方法的实现标志。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-110">[out] A pointer to the implementation flags for the method.</span></span> <span data-ttu-id="2a6b6-111">此值是 [CorMethodImpl](cormethodimpl-enumeration.md) 枚举中的位掩码。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-111">This value is a bitmask from the [CorMethodImpl](cormethodimpl-enumeration.md) enumeration.</span></span> <span data-ttu-id="2a6b6-112">`pdwImplFlags`仅当为 MethodDef 标记时，的值才有效 `tk` 。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-112">The value of `pdwImplFlags` is valid only if `tk` is a MethodDef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a6b6-113">要求</span><span class="sxs-lookup"><span data-stu-id="2a6b6-113">Requirements</span></span>  

 <span data-ttu-id="2a6b6-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2a6b6-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a6b6-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="2a6b6-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2a6b6-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2a6b6-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2a6b6-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a6b6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a6b6-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="2a6b6-118">See also</span></span>

- [<span data-ttu-id="2a6b6-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="2a6b6-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="2a6b6-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="2a6b6-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)

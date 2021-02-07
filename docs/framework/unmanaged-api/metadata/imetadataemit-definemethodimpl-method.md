---
description: 了解详细信息： IMetaDataEmit：:D efineMethodImpl 方法
title: IMetaDataEmit::DefineMethodImpl 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMethodImpl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMethodImpl
helpviewer_keywords:
- DefineMethodImpl method [.NET Framework metadata]
- IMetaDataEmit::DefineMethodImpl method [.NET Framework metadata]
ms.assetid: 9dcc8b3d-33ee-4c7c-8d6f-322c57b94a0f
topic_type:
- apiref
ms.openlocfilehash: 9c79d713e61bfcc7b3191e570ed727b128422bf1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753401"
---
# <a name="imetadataemitdefinemethodimpl-method"></a><span data-ttu-id="8a8e7-103">IMetaDataEmit::DefineMethodImpl 方法</span><span class="sxs-lookup"><span data-stu-id="8a8e7-103">IMetaDataEmit::DefineMethodImpl Method</span></span>

<span data-ttu-id="8a8e7-104">创建一个定义，用于实现从接口继承的方法，并返回该方法实现定义的标记。</span><span class="sxs-lookup"><span data-stu-id="8a8e7-104">Creates a definition for implementation of a method inherited from an interface, and returns a token to that method-implementation definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a8e7-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a8e7-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineMethodImpl (
    [in]  mdTypeDef         td,
    [in]  mdToken           tkBody,
    [in]  mdToken           tkDecl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a8e7-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a8e7-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="8a8e7-107">中 `mdTypedef` 实现类的标记。</span><span class="sxs-lookup"><span data-stu-id="8a8e7-107">[in] The `mdTypedef` token of the implementing class.</span></span>  
  
 `tkBody`  
 <span data-ttu-id="8a8e7-108">中 `mdMethodDef` `mdMemberRef` 代码主体的或标记。</span><span class="sxs-lookup"><span data-stu-id="8a8e7-108">[in] The `mdMethodDef` or `mdMemberRef` token of the code body.</span></span>  
  
 `tkDecl`  
 <span data-ttu-id="8a8e7-109">中 `mdMethodDef` `mdMemberRef` 要实现的接口方法的或标记。</span><span class="sxs-lookup"><span data-stu-id="8a8e7-109">[in] The `mdMethodDef` or `mdMemberRef` token of the interface method being implemented.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a8e7-110">要求</span><span class="sxs-lookup"><span data-stu-id="8a8e7-110">Requirements</span></span>  

 <span data-ttu-id="8a8e7-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a8e7-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a8e7-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8a8e7-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8a8e7-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8a8e7-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8a8e7-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a8e7-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a8e7-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a8e7-115">See also</span></span>

- [<span data-ttu-id="8a8e7-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8a8e7-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="8a8e7-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8a8e7-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

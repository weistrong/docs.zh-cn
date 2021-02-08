---
description: 了解详细信息： IMetaDataEmit：:D eleteClassLayout 方法
title: IMetaDataEmit::DeleteClassLayout 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteClassLayout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteClassLayout
helpviewer_keywords:
- DeleteClassLayout method [.NET Framework metadata]
- IMetaDataEmit::DeleteClassLayout method [.NET Framework metadata]
ms.assetid: 65a4ad49-fa49-4b36-8ed1-76dd6a185ab4
topic_type:
- apiref
ms.openlocfilehash: 44be89f415087a1457a83bb1167e1017d26ed5ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783984"
---
# <a name="imetadataemitdeleteclasslayout-method"></a><span data-ttu-id="3c8a3-103">IMetaDataEmit::DeleteClassLayout 方法</span><span class="sxs-lookup"><span data-stu-id="3c8a3-103">IMetaDataEmit::DeleteClassLayout Method</span></span>

<span data-ttu-id="3c8a3-104">销毁由指定标记表示的类型的类布局元数据签名。</span><span class="sxs-lookup"><span data-stu-id="3c8a3-104">Destroys the class layout metadata signature for the type represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c8a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="3c8a3-105">Syntax</span></span>  
  
```cpp  
HRESULT DeleteClassLayout (  
    [in]  mdTypeDef   td  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3c8a3-106">参数</span><span class="sxs-lookup"><span data-stu-id="3c8a3-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="3c8a3-107">中一个 `mdTypeDef` 元数据标记，它表示将删除类布局的类型。</span><span class="sxs-lookup"><span data-stu-id="3c8a3-107">[in] An `mdTypeDef` metadata token that represents the type for which the class layout will be deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c8a3-108">要求</span><span class="sxs-lookup"><span data-stu-id="3c8a3-108">Requirements</span></span>  

 <span data-ttu-id="3c8a3-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c8a3-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c8a3-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3c8a3-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3c8a3-111">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3c8a3-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3c8a3-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c8a3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c8a3-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c8a3-113">See also</span></span>

- [<span data-ttu-id="3c8a3-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="3c8a3-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="3c8a3-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="3c8a3-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

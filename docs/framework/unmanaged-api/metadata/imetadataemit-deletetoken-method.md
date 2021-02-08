---
description: 了解详细信息： IMetaDataEmit：:D eleteToken 方法
title: IMetaDataEmit::DeleteToken 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteToken
helpviewer_keywords:
- DeleteToken method [.NET Framework metadata]
- IMetaDataEmit::DeleteToken method [.NET Framework metadata]
ms.assetid: a4926d0a-261b-46b1-9994-82633661a64b
topic_type:
- apiref
ms.openlocfilehash: 5c28b56b06f994057409ef8fa17179cb0b0e205b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783945"
---
# <a name="imetadataemitdeletetoken-method"></a><span data-ttu-id="5bbba-103">IMetaDataEmit::DeleteToken 方法</span><span class="sxs-lookup"><span data-stu-id="5bbba-103">IMetaDataEmit::DeleteToken Method</span></span>

<span data-ttu-id="5bbba-104">从当前的元数据范围中删除指定的标记。</span><span class="sxs-lookup"><span data-stu-id="5bbba-104">Deletes the specified token from the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bbba-105">语法</span><span class="sxs-lookup"><span data-stu-id="5bbba-105">Syntax</span></span>  
  
```cpp  
HRESULT DeleteToken (
    [in]  mdToken     tkObj
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5bbba-106">参数</span><span class="sxs-lookup"><span data-stu-id="5bbba-106">Parameters</span></span>  

 `tkObj`  
 <span data-ttu-id="5bbba-107">中要删除的标记。</span><span class="sxs-lookup"><span data-stu-id="5bbba-107">[in] The token to be deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bbba-108">要求</span><span class="sxs-lookup"><span data-stu-id="5bbba-108">Requirements</span></span>  

 <span data-ttu-id="5bbba-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5bbba-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bbba-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5bbba-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5bbba-111">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5bbba-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5bbba-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bbba-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bbba-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bbba-113">See also</span></span>

- [<span data-ttu-id="5bbba-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="5bbba-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="5bbba-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="5bbba-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)

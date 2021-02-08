---
description: 了解详细信息： ICorPublishEnum：： Skip 方法
title: ICorPublishEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorPublishEnum.Skip
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum::Skip
helpviewer_keywords:
- ICorPublishEnum::Skip method [.NET Framework debugging]
- Skip method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 1680ec06-4ab0-447e-93ad-cdb8693fde5c
topic_type:
- apiref
ms.openlocfilehash: f0124681c8051a5c05c1caf3edd06c697da486e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794593"
---
# <a name="icorpublishenumskip-method"></a><span data-ttu-id="e4660-103">ICorPublishEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="e4660-103">ICorPublishEnum::Skip Method</span></span>

<span data-ttu-id="e4660-104">按指定的项数在枚举中向前移动光标。</span><span class="sxs-lookup"><span data-stu-id="e4660-104">Moves the cursor forward in the enumeration by the specified number of items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4660-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4660-105">Syntax</span></span>  
  
```cpp  
HRESULT Skip (  
    [in] ULONG   celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4660-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4660-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="e4660-107">中游标向前移动的项数。</span><span class="sxs-lookup"><span data-stu-id="e4660-107">[in] The number of items by which to move the cursor forward.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4660-108">要求</span><span class="sxs-lookup"><span data-stu-id="e4660-108">Requirements</span></span>  

 <span data-ttu-id="e4660-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4660-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4660-110">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="e4660-110">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="e4660-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4660-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4660-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4660-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4660-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4660-113">See also</span></span>

- [<span data-ttu-id="e4660-114">ICorPublishEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e4660-114">ICorPublishEnum Interface</span></span>](icorpublishenum-interface.md)

---
description: 了解详细信息： ICorDebugEnum：： Skip 方法
title: ICorDebugEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.Skip
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::Skip
helpviewer_keywords:
- ICorDebugEnum::Skip method [.NET Framework debugging]
- Skip method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: e925d88a-67a5-4f76-88b8-09cedeed0232
topic_type:
- apiref
ms.openlocfilehash: f72e400b3c2c911f609aca19f1b7d6a3a4e785cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694352"
---
# <a name="icordebugenumskip-method"></a><span data-ttu-id="1a2a4-103">ICorDebugEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="1a2a4-103">ICorDebugEnum::Skip Method</span></span>

<span data-ttu-id="1a2a4-104">按指定的项数在枚举中向前移动光标。</span><span class="sxs-lookup"><span data-stu-id="1a2a4-104">Moves the cursor forward in the enumeration by the specified number of items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1a2a4-105">语法</span><span class="sxs-lookup"><span data-stu-id="1a2a4-105">Syntax</span></span>  
  
```cpp  
HRESULT Skip (  
    [in] ULONG celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1a2a4-106">参数</span><span class="sxs-lookup"><span data-stu-id="1a2a4-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="1a2a4-107">中游标向前移动的项数。</span><span class="sxs-lookup"><span data-stu-id="1a2a4-107">[in] The number of items by which to move the cursor forward.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a2a4-108">要求</span><span class="sxs-lookup"><span data-stu-id="1a2a4-108">Requirements</span></span>  

 <span data-ttu-id="1a2a4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1a2a4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a2a4-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1a2a4-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1a2a4-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1a2a4-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1a2a4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a2a4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a2a4-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="1a2a4-113">See also</span></span>

- [<span data-ttu-id="1a2a4-114">ICorDebugEnum 接口</span><span class="sxs-lookup"><span data-stu-id="1a2a4-114">ICorDebugEnum Interface</span></span>](icordebugenum-interface1.md)

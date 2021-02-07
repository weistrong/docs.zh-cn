---
description: 了解详细信息： ICorDebugEval：： IsActive 方法
title: ICorDebugEval::IsActive 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::IsActive
helpviewer_keywords:
- IsActive method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::IsActive method [.NET Framework debugging]
ms.assetid: bf2bba24-d278-43bd-b1c5-35680e748d3e
topic_type:
- apiref
ms.openlocfilehash: 2314814f8979f460063017ebdf46beb512417395
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694040"
---
# <a name="icordebugevalisactive-method"></a><span data-ttu-id="8857a-103">ICorDebugEval::IsActive 方法</span><span class="sxs-lookup"><span data-stu-id="8857a-103">ICorDebugEval::IsActive Method</span></span>

<span data-ttu-id="8857a-104">获取一个值，该值指示此 ICorDebugEval 对象当前是否正在执行。</span><span class="sxs-lookup"><span data-stu-id="8857a-104">Gets a value that indicates whether this ICorDebugEval object is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8857a-105">语法</span><span class="sxs-lookup"><span data-stu-id="8857a-105">Syntax</span></span>  
  
```cpp  
HRESULT IsActive (  
    [out] BOOL              *pbActive  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8857a-106">参数</span><span class="sxs-lookup"><span data-stu-id="8857a-106">Parameters</span></span>  

 `pbActive`  
 <span data-ttu-id="8857a-107">弄指向一个值的指针，该值指示此计算是否处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="8857a-107">[out] Pointer to a value that indicates whether this evaluation is active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8857a-108">要求</span><span class="sxs-lookup"><span data-stu-id="8857a-108">Requirements</span></span>  

 <span data-ttu-id="8857a-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8857a-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8857a-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8857a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8857a-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8857a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8857a-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8857a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

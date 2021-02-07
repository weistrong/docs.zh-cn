---
description: 了解详细信息： ICorDebugEval2：： RudeAbort 方法
title: ICorDebugEval2::RudeAbort 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.RudeAbort
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::RudeAbort
helpviewer_keywords:
- ICorDebugEval2::RudeAbort method [.NET Framework debugging]
- RudeAbort method, ICorDebugEval2 interface [.NET Framework debugging]
ms.assetid: 02468edf-d32b-4cb3-aaa8-3dd2abfc8b25
topic_type:
- apiref
ms.openlocfilehash: 2835fd635da007b5ee3f0e642b77f3954945f168
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693507"
---
# <a name="icordebugeval2rudeabort-method"></a><span data-ttu-id="5ae2c-103">ICorDebugEval2::RudeAbort 方法</span><span class="sxs-lookup"><span data-stu-id="5ae2c-103">ICorDebugEval2::RudeAbort Method</span></span>

<span data-ttu-id="5ae2c-104">中止此当前正在执行的计算 `ICorDebugEval2` 。</span><span class="sxs-lookup"><span data-stu-id="5ae2c-104">Aborts the computation that this `ICorDebugEval2` is currently performing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ae2c-105">语法</span><span class="sxs-lookup"><span data-stu-id="5ae2c-105">Syntax</span></span>  
  
```cpp  
HRESULT RudeAbort ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="5ae2c-106">备注</span><span class="sxs-lookup"><span data-stu-id="5ae2c-106">Remarks</span></span>  

 <span data-ttu-id="5ae2c-107">`RudeAbort` 不会释放该计算器持有的任何锁，因此会使调试会话处于不安全状态。</span><span class="sxs-lookup"><span data-stu-id="5ae2c-107">`RudeAbort` does not release any locks that the evaluator holds, so it leaves the debugging session in an unsafe state.</span></span> <span data-ttu-id="5ae2c-108">请特别小心调用此方法。</span><span class="sxs-lookup"><span data-stu-id="5ae2c-108">Call this method with extreme caution.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ae2c-109">要求</span><span class="sxs-lookup"><span data-stu-id="5ae2c-109">Requirements</span></span>  

 <span data-ttu-id="5ae2c-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5ae2c-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ae2c-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5ae2c-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5ae2c-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5ae2c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5ae2c-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5ae2c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

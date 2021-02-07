---
description: 了解详细信息： ICorDebugFrame：： CreateStepper 方法
title: ICorDebugFrame::CreateStepper 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.CreateStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::CreateStepper
helpviewer_keywords:
- ICorDebugFrame::CreateStepper method [.NET Framework debugging]
- CreateStepper method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 689e7f28-20c1-4d5c-9baa-17441cd63a88
topic_type:
- apiref
ms.openlocfilehash: 394418b89fd7a1c780a5bc33b97b8ef40bab8df2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693091"
---
# <a name="icordebugframecreatestepper-method"></a><span data-ttu-id="c160c-103">ICorDebugFrame::CreateStepper 方法</span><span class="sxs-lookup"><span data-stu-id="c160c-103">ICorDebugFrame::CreateStepper Method</span></span>

<span data-ttu-id="c160c-104">获取一个分档器，该分档器允许调试器执行相对于此 ICorDebugFrame 的单步执行操作。</span><span class="sxs-lookup"><span data-stu-id="c160c-104">Gets a stepper that allows the debugger to perform stepping operations relative to this ICorDebugFrame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c160c-105">语法</span><span class="sxs-lookup"><span data-stu-id="c160c-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateStepper (  
    [out] ICorDebugStepper   **ppStepper  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c160c-106">参数</span><span class="sxs-lookup"><span data-stu-id="c160c-106">Parameters</span></span>  

 `ppStepper`  
 <span data-ttu-id="c160c-107">弄指向 ICorDebugStepper 对象地址的指针，该对象允许调试器相对于当前帧执行单步操作。</span><span class="sxs-lookup"><span data-stu-id="c160c-107">[out] A pointer to the address of an ICorDebugStepper object that allows the debugger to perform stepping operations relative to the current frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c160c-108">备注</span><span class="sxs-lookup"><span data-stu-id="c160c-108">Remarks</span></span>  

 <span data-ttu-id="c160c-109">如果帧不处于活动状态，则在步骤完成之前，分档器对象通常需要返回到帧。</span><span class="sxs-lookup"><span data-stu-id="c160c-109">If the frame is not active, the stepper object will typically have to return to the frame before the step is completed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c160c-110">要求</span><span class="sxs-lookup"><span data-stu-id="c160c-110">Requirements</span></span>  

 <span data-ttu-id="c160c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c160c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c160c-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c160c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c160c-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c160c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c160c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c160c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

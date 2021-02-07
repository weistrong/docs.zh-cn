---
description: 了解详细信息： ICorDebugStepper：： SetRangeIL 方法
title: ICorDebugStepper::SetRangeIL 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.SetRangeIL
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::SetRangeIL
helpviewer_keywords:
- SetRangeIL method [.NET Framework debugging]
- ICorDebugStepper::SetRangeIL method [.NET Framework debugging]
ms.assetid: a20c95f0-6da7-4b41-b27f-584211cebb92
topic_type:
- apiref
ms.openlocfilehash: 8bccaf8ba8e52a7fe94555fa99b1c3cf92842efe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717676"
---
# <a name="icordebugsteppersetrangeil-method"></a><span data-ttu-id="e4df9-103">ICorDebugStepper::SetRangeIL 方法</span><span class="sxs-lookup"><span data-stu-id="e4df9-103">ICorDebugStepper::SetRangeIL Method</span></span>

<span data-ttu-id="e4df9-104">设置一个值，该值指定对 [ICorDebugStepper：： StepRange](icordebugstepper-steprange-method.md) 的调用是传递与本机代码相关的参数值，还是相对于 Microsoft 中间)  (语言传递参数值。</span><span class="sxs-lookup"><span data-stu-id="e4df9-104">Sets a value that specifies whether calls to [ICorDebugStepper::StepRange](icordebugstepper-steprange-method.md) pass argument values that are relative to the native code or relative to Microsoft intermediate language (MSIL) code of the method that is being stepped through.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4df9-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4df9-105">Syntax</span></span>  
  
```cpp  
HRESULT SetRangeIL (  
    [in] BOOL    bIL  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4df9-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4df9-106">Parameters</span></span>  

 `bIL`  
 <span data-ttu-id="e4df9-107">中如果设置为， `true` 则指定范围是相对于 MSIL 代码的。</span><span class="sxs-lookup"><span data-stu-id="e4df9-107">[in] Set to `true` to specify that the ranges are relative to the MSIL code.</span></span> <span data-ttu-id="e4df9-108">设置为， `false` 以指定范围相对于本机代码。</span><span class="sxs-lookup"><span data-stu-id="e4df9-108">Set to `false` to specify that the ranges are relative to the native code.</span></span> <span data-ttu-id="e4df9-109">默认值是 `true`。</span><span class="sxs-lookup"><span data-stu-id="e4df9-109">The default value is `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4df9-110">要求</span><span class="sxs-lookup"><span data-stu-id="e4df9-110">Requirements</span></span>  

 <span data-ttu-id="e4df9-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4df9-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4df9-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e4df9-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e4df9-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4df9-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4df9-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4df9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

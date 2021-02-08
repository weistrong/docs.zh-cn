---
description: 了解详细信息： ICorDebugStepper：:D eactivate 方法
title: ICorDebugStepper::Deactivate 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.Deactivate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::Deactivate
helpviewer_keywords:
- Deactivate method [.NET Framework debugging]
- ICorDebugStepper::Deactivate method [.NET Framework debugging]
ms.assetid: 855f4199-b62d-40ce-998e-1eb4a1772142
topic_type:
- apiref
ms.openlocfilehash: 039c52f5bc237506dcc648ace70789c8eb7ef8c9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794658"
---
# <a name="icordebugstepperdeactivate-method"></a><span data-ttu-id="67b0b-103">ICorDebugStepper::Deactivate 方法</span><span class="sxs-lookup"><span data-stu-id="67b0b-103">ICorDebugStepper::Deactivate Method</span></span>

<span data-ttu-id="67b0b-104">使此 ICorDebugStepper 取消其收到的最后一个步骤命令。</span><span class="sxs-lookup"><span data-stu-id="67b0b-104">Causes this ICorDebugStepper to cancel the last step command that it received.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67b0b-105">语法</span><span class="sxs-lookup"><span data-stu-id="67b0b-105">Syntax</span></span>  
  
```cpp  
HRESULT Deactivate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="67b0b-106">备注</span><span class="sxs-lookup"><span data-stu-id="67b0b-106">Remarks</span></span>  

 <span data-ttu-id="67b0b-107">在取消最近收到的步骤命令后，可能会发出新的单步执行命令。</span><span class="sxs-lookup"><span data-stu-id="67b0b-107">A new stepping command may be issued after the most recently received step command has been canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67b0b-108">要求</span><span class="sxs-lookup"><span data-stu-id="67b0b-108">Requirements</span></span>  

 <span data-ttu-id="67b0b-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="67b0b-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67b0b-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="67b0b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="67b0b-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="67b0b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="67b0b-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67b0b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

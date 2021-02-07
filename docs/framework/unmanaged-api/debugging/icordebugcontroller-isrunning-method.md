---
description: 了解详细信息： ICorDebugController：： IsRunning 方法
title: ICorDebugController::IsRunning 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.IsRunning
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::IsRunning
helpviewer_keywords:
- IsRunning method [.NET Framework debugging]
- ICorDebugController::IsRunning method [.NET Framework debugging]
ms.assetid: b33ff059-40c4-4dfe-9cb2-21bfed2de0b0
topic_type:
- apiref
ms.openlocfilehash: 6a0628cc39765d9cb295877d912d92dbb27937da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764575"
---
# <a name="icordebugcontrollerisrunning-method"></a><span data-ttu-id="5df01-103">ICorDebugController::IsRunning 方法</span><span class="sxs-lookup"><span data-stu-id="5df01-103">ICorDebugController::IsRunning Method</span></span>

<span data-ttu-id="5df01-104">获取一个值，该值指示进程中的线程当前是否可以自由运行。</span><span class="sxs-lookup"><span data-stu-id="5df01-104">Gets a value that indicates whether the threads in the process are currently running freely.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5df01-105">语法</span><span class="sxs-lookup"><span data-stu-id="5df01-105">Syntax</span></span>  
  
```cpp  
HRESULT IsRunning (  
    [out] BOOL *pbRunning  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5df01-106">参数</span><span class="sxs-lookup"><span data-stu-id="5df01-106">Parameters</span></span>  

 `pbRunning`  
 <span data-ttu-id="5df01-107">弄一个指向值的指针， `true` 如果进程中的线程自由运行，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5df01-107">[out] A pointer to a value that is `true` if the threads in the process are running freely; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5df01-108">要求</span><span class="sxs-lookup"><span data-stu-id="5df01-108">Requirements</span></span>  

 <span data-ttu-id="5df01-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5df01-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5df01-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5df01-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5df01-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5df01-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5df01-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5df01-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5df01-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5df01-113">See also</span></span>

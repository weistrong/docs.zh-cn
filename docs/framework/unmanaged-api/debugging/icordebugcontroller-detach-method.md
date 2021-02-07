---
description: 了解详细信息： ICorDebugController：:D etach 方法
title: ICorDebugController::Detach 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.Detach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Detach
helpviewer_keywords:
- Detach method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Detach method [.NET Framework debugging]
ms.assetid: 06fae364-f2c6-4a50-aa7e-3da9f2684dc3
topic_type:
- apiref
ms.openlocfilehash: 763386fa72fab023becf4a360556e61d500c7949
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764633"
---
# <a name="icordebugcontrollerdetach-method"></a><span data-ttu-id="5d489-103">ICorDebugController::Detach 方法</span><span class="sxs-lookup"><span data-stu-id="5d489-103">ICorDebugController::Detach Method</span></span>

<span data-ttu-id="5d489-104">将调试器与进程或应用程序域分离。</span><span class="sxs-lookup"><span data-stu-id="5d489-104">Detaches the debugger from the process or application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d489-105">语法</span><span class="sxs-lookup"><span data-stu-id="5d489-105">Syntax</span></span>  
  
```cpp  
HRESULT Detach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="5d489-106">备注</span><span class="sxs-lookup"><span data-stu-id="5d489-106">Remarks</span></span>  

 <span data-ttu-id="5d489-107">进程或应用程序域将继续正常执行，但 "ICorDebugProcess" 或 "ICorDebugAppDomain" 对象不再有效，且不会发生进一步的回调。</span><span class="sxs-lookup"><span data-stu-id="5d489-107">The process or application domain continues execution normally, but the "ICorDebugProcess" or "ICorDebugAppDomain" object is no longer valid and no further callbacks will occur.</span></span>  
  
 <span data-ttu-id="5d489-108">在 .NET Framework 版本2.0 中，如果启用了非托管调试，则此方法将因操作系统限制而失败。</span><span class="sxs-lookup"><span data-stu-id="5d489-108">In the .NET Framework version 2.0, if unmanaged debugging is enabled, this method will fail due to operating system limitations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5d489-109">要求</span><span class="sxs-lookup"><span data-stu-id="5d489-109">Requirements</span></span>  

 <span data-ttu-id="5d489-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5d489-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d489-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5d489-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5d489-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5d489-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5d489-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d489-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d489-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="5d489-114">See also</span></span>

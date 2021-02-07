---
description: 了解详细信息： ICorDebugAppDomain：： Attach 方法
title: ICorDebugAppDomain::Attach 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.Attach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::Attach
helpviewer_keywords:
- ICorDebugAppDomain::Attach method [.NET Framework debugging]
- Attach method [.NET Framework debugging]
ms.assetid: 0358b84a-4236-4c34-945b-4babff7df570
topic_type:
- apiref
ms.openlocfilehash: 94448937a735b30d0403a207992dae29920a93bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754272"
---
# <a name="icordebugappdomainattach-method"></a><span data-ttu-id="f55b8-103">ICorDebugAppDomain::Attach 方法</span><span class="sxs-lookup"><span data-stu-id="f55b8-103">ICorDebugAppDomain::Attach Method</span></span>

<span data-ttu-id="f55b8-104">将调试器附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="f55b8-104">Attaches the debugger to the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f55b8-105">语法</span><span class="sxs-lookup"><span data-stu-id="f55b8-105">Syntax</span></span>  
  
```cpp  
HRESULT Attach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="f55b8-106">备注</span><span class="sxs-lookup"><span data-stu-id="f55b8-106">Remarks</span></span>  

 <span data-ttu-id="f55b8-107">调试器必须附加到应用程序域，才能接收事件和启用应用程序域的调试。</span><span class="sxs-lookup"><span data-stu-id="f55b8-107">The debugger must be attached to the application domain to receive events and to enable debugging of the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f55b8-108">要求</span><span class="sxs-lookup"><span data-stu-id="f55b8-108">Requirements</span></span>  

 <span data-ttu-id="f55b8-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f55b8-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f55b8-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f55b8-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f55b8-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f55b8-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f55b8-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f55b8-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

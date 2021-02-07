---
description: 了解详细信息： ICorDebug：： Terminate 方法
title: ICorDebug::Terminate 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.Terminate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::Terminate
helpviewer_keywords:
- Terminate method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Terminate method [.NET Framework debugging]
ms.assetid: fffe5616-0896-4426-ab5e-21869b514883
topic_type:
- apiref
ms.openlocfilehash: c2de27a47bfd4c364a09180c75109679234f3cae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754285"
---
# <a name="icordebugterminate-method"></a><span data-ttu-id="457f9-103">ICorDebug::Terminate 方法</span><span class="sxs-lookup"><span data-stu-id="457f9-103">ICorDebug::Terminate Method</span></span>

<span data-ttu-id="457f9-104">终止 `ICorDebug` 对象。</span><span class="sxs-lookup"><span data-stu-id="457f9-104">Terminates the `ICorDebug` object.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="457f9-105">`Terminate` 在为所有正在调试的进程接收到 [ICorDebugManagedCallback：： ExitProcess](icordebugmanagedcallback-exitprocess-method.md) 回调之前，不应调用。</span><span class="sxs-lookup"><span data-stu-id="457f9-105">`Terminate` should not be called until an [ICorDebugManagedCallback::ExitProcess](icordebugmanagedcallback-exitprocess-method.md) callback has been received for all processes being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="457f9-106">语法</span><span class="sxs-lookup"><span data-stu-id="457f9-106">Syntax</span></span>  
  
```cpp  
HRESULT Terminate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="457f9-107">备注</span><span class="sxs-lookup"><span data-stu-id="457f9-107">Remarks</span></span>  

 <span data-ttu-id="457f9-108">`Terminate` 当不再需要对象时，必须调用 `ICorDebug` 。</span><span class="sxs-lookup"><span data-stu-id="457f9-108">`Terminate` must be called when the `ICorDebug` object is no longer needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="457f9-109">要求</span><span class="sxs-lookup"><span data-stu-id="457f9-109">Requirements</span></span>  

 <span data-ttu-id="457f9-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="457f9-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="457f9-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="457f9-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="457f9-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="457f9-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="457f9-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="457f9-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="457f9-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="457f9-114">See also</span></span>

- [<span data-ttu-id="457f9-115">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="457f9-115">ICorDebug Interface</span></span>](icordebug-interface.md)

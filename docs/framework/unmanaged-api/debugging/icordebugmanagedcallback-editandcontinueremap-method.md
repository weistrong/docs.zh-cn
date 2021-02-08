---
description: 了解详细信息： ICorDebugManagedCallback：： EditAndContinueRemap 方法
title: ICorDebugManagedCallback::EditAndContinueRemap 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EditAndContinueRemap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EditAndContinueRemap
helpviewer_keywords:
- EditAndContinueRemap method [.NET Framework debugging]
- ICorDebugManagedCallback::EditAndContinueRemap method [.NET Framework debugging]
ms.assetid: 24a8fcce-317e-48ff-aefc-d86123ada935
topic_type:
- apiref
ms.openlocfilehash: ad8932e41236cdb8ed213024efb4175292a5d5f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790994"
---
# <a name="icordebugmanagedcallbackeditandcontinueremap-method"></a><span data-ttu-id="1c2c8-103">ICorDebugManagedCallback::EditAndContinueRemap 方法</span><span class="sxs-lookup"><span data-stu-id="1c2c8-103">ICorDebugManagedCallback::EditAndContinueRemap Method</span></span>

<span data-ttu-id="1c2c8-104">此方法已被否决。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-104">This method has been deprecated.</span></span> <span data-ttu-id="1c2c8-105">它通知调试器已将重新映射事件发送到 (IDE) 的集成开发环境。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-105">It notifies the debugger that a remap event has been sent to the integrated development environment (IDE).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c2c8-106">语法</span><span class="sxs-lookup"><span data-stu-id="1c2c8-106">Syntax</span></span>  
  
```cpp  
HRESULT EditAndContinueRemap (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread *pThread,  
    [in] ICorDebugFunction *pFunction,  
    [in] BOOL fAccurate  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="1c2c8-107">备注</span><span class="sxs-lookup"><span data-stu-id="1c2c8-107">Remarks</span></span>  

 <span data-ttu-id="1c2c8-108">`EditAndContinueRemap`当尝试在旧版本的更新函数中执行代码时，将调用方法。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-108">The `EditAndContinueRemap` method is called when the execution of the code in an old version of an updated function has been attempted.</span></span> <span data-ttu-id="1c2c8-109">公共语言运行时调用 `EditAndContinueRemap` 方法，将重新映射事件发送到 IDE。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-109">The common language runtime calls the `EditAndContinueRemap` method to send a remap event to the IDE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c2c8-110">要求</span><span class="sxs-lookup"><span data-stu-id="1c2c8-110">Requirements</span></span>  

 <span data-ttu-id="1c2c8-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c2c8-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1c2c8-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1c2c8-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1c2c8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1c2c8-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c2c8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c2c8-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1c2c8-115">See also</span></span>

- [<span data-ttu-id="1c2c8-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="1c2c8-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)

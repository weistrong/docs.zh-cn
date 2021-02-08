---
description: 了解详细信息： ICorDebugManagedCallback：： CreateProcess 方法
title: ICorDebugManagedCallback::CreateProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateProcess
helpviewer_keywords:
- ICorDebugManagedCallback::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: 8e89d5ee-e4e3-4738-8302-0b7d1cf4846e
topic_type:
- apiref
ms.openlocfilehash: 564c9862dd90431f0626204fdfe49e59b85a124d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791044"
---
# <a name="icordebugmanagedcallbackcreateprocess-method"></a><span data-ttu-id="05af7-103">ICorDebugManagedCallback::CreateProcess 方法</span><span class="sxs-lookup"><span data-stu-id="05af7-103">ICorDebugManagedCallback::CreateProcess Method</span></span>

<span data-ttu-id="05af7-104">第一次附加或启动进程时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="05af7-104">Notifies the debugger when a process has been attached or started for the first time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05af7-105">语法</span><span class="sxs-lookup"><span data-stu-id="05af7-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05af7-106">参数</span><span class="sxs-lookup"><span data-stu-id="05af7-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="05af7-107">中指向 ICorDebugProcess 对象的指针，该对象表示已附加或已启动的进程。</span><span class="sxs-lookup"><span data-stu-id="05af7-107">[in] A pointer to an ICorDebugProcess object that represents the process that has been attached or started.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="05af7-108">备注</span><span class="sxs-lookup"><span data-stu-id="05af7-108">Remarks</span></span>  

 <span data-ttu-id="05af7-109">在公共语言运行时初始化之前，不会调用此方法。</span><span class="sxs-lookup"><span data-stu-id="05af7-109">This method is not called until the common language runtime is initialized.</span></span> <span data-ttu-id="05af7-110">大多数 [ICorDebug](icordebug-interface.md) 方法将在回调之前返回 CORDBG_E_NOTREADY `CreateProcess` 。</span><span class="sxs-lookup"><span data-stu-id="05af7-110">Most of the [ICorDebug](icordebug-interface.md) methods will return CORDBG_E_NOTREADY before the `CreateProcess` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05af7-111">要求</span><span class="sxs-lookup"><span data-stu-id="05af7-111">Requirements</span></span>  

 <span data-ttu-id="05af7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="05af7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05af7-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="05af7-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="05af7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="05af7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="05af7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05af7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05af7-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="05af7-116">See also</span></span>

- [<span data-ttu-id="05af7-117">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="05af7-117">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)

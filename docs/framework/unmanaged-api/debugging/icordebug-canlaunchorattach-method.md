---
description: 了解详细信息： ICorDebug：： CanLaunchOrAttach 方法
title: ICorDebug::CanLaunchOrAttach 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.CanLaunchOrAttach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::CanLaunchOrAttach
helpviewer_keywords:
- ICorDebug::CanLaunchOrAttach method [.NET Framework debugging]
- CanLaunchOrAttach method [.NET Framework debugging]
ms.assetid: ca7723db-7c07-4cdd-bd92-fba34928b623
topic_type:
- apiref
ms.openlocfilehash: cb813c4bae968941de731d9d5b74d8f804b3c8ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723226"
---
# <a name="icordebugcanlaunchorattach-method"></a><span data-ttu-id="dadad-103">ICorDebug::CanLaunchOrAttach 方法</span><span class="sxs-lookup"><span data-stu-id="dadad-103">ICorDebug::CanLaunchOrAttach Method</span></span>

<span data-ttu-id="dadad-104">返回一个 HRESULT，它指示是否可以在当前计算机和运行时配置的上下文中启动新进程或附加到指定的现有进程。</span><span class="sxs-lookup"><span data-stu-id="dadad-104">Returns an HRESULT that indicates whether launching a new process or attaching to the specified existing process is possible within the context of the current machine and runtime configuration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dadad-105">语法</span><span class="sxs-lookup"><span data-stu-id="dadad-105">Syntax</span></span>  
  
```cpp  
HRESULT CanLaunchOrAttach (  
    [in] DWORD      dwProcessId,  
    [in] BOOL       win32DebuggingEnabled  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dadad-106">参数</span><span class="sxs-lookup"><span data-stu-id="dadad-106">Parameters</span></span>  

 `dwProcessId`  
 <span data-ttu-id="dadad-107">中现有进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="dadad-107">[in] The ID of an existing process.</span></span>  
  
 `win32DebuggingEnabled`  
 <span data-ttu-id="dadad-108">中 `true` 如果计划在启用 win32 调试的情况下启动或附加到已启用 win32 调试，请 `false` 传入</span><span class="sxs-lookup"><span data-stu-id="dadad-108">[in] Pass in `true` if you plan to launch with Win32 debugging enabled, or to attach with Win32 debugging enabled; otherwise, pass `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dadad-109">返回值</span><span class="sxs-lookup"><span data-stu-id="dadad-109">Return Value</span></span>  

 <span data-ttu-id="dadad-110">在给定有关当前计算机和运行时配置的信息的情况下，如果调试服务确定启动新进程或附加到给定进程，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="dadad-110">S_OK if the debugging services determine that launching a new process or attaching to the given process is possible, given the information about the current machine and runtime configuration.</span></span> <span data-ttu-id="dadad-111">可能的 HRESULT 值为：</span><span class="sxs-lookup"><span data-stu-id="dadad-111">Possible HRESULT values are:</span></span>  
  
- <span data-ttu-id="dadad-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="dadad-112">S_OK</span></span>  
  
- <span data-ttu-id="dadad-113">CORDBG_E_DEBUGGING_NOT_POSSIBLE</span><span class="sxs-lookup"><span data-stu-id="dadad-113">CORDBG_E_DEBUGGING_NOT_POSSIBLE</span></span>  
  
- <span data-ttu-id="dadad-114">CORDBG_E_KERNEL_DEBUGGER_PRESENT</span><span class="sxs-lookup"><span data-stu-id="dadad-114">CORDBG_E_KERNEL_DEBUGGER_PRESENT</span></span>  
  
- <span data-ttu-id="dadad-115">CORDBG_E_KERNEL_DEBUGGER_ENABLED</span><span class="sxs-lookup"><span data-stu-id="dadad-115">CORDBG_E_KERNEL_DEBUGGER_ENABLED</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dadad-116">备注</span><span class="sxs-lookup"><span data-stu-id="dadad-116">Remarks</span></span>  

 <span data-ttu-id="dadad-117">此方法纯信息性。</span><span class="sxs-lookup"><span data-stu-id="dadad-117">This method is purely informational.</span></span> <span data-ttu-id="dadad-118">无论返回的值是什么，接口都不会阻止你启动或附加到进程 `CanLaunchOrAttach` 。</span><span class="sxs-lookup"><span data-stu-id="dadad-118">The interface will not stop you from launching or attaching to a process, regardless of the value returned by `CanLaunchOrAttach`.</span></span>  
  
 <span data-ttu-id="dadad-119">如果计划在启用 Win32 调试的情况下启动或附加启用了 Win32 调试，请传递 `true` for `win32DebuggingEnabled` 。</span><span class="sxs-lookup"><span data-stu-id="dadad-119">If you plan to launch with Win32 debugging enabled or attach with Win32 debugging enabled, pass `true` for `win32DebuggingEnabled`.</span></span> <span data-ttu-id="dadad-120">如果使用此选项，则返回的 HRESULT `CanLaunchOrAttach` 可能不同。</span><span class="sxs-lookup"><span data-stu-id="dadad-120">The HRESULT returned by `CanLaunchOrAttach` might differ if you use this option.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dadad-121">要求</span><span class="sxs-lookup"><span data-stu-id="dadad-121">Requirements</span></span>  

 <span data-ttu-id="dadad-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dadad-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dadad-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dadad-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dadad-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dadad-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dadad-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dadad-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dadad-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="dadad-126">See also</span></span>

- [<span data-ttu-id="dadad-127">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="dadad-127">ICorDebug Interface</span></span>](icordebug-interface.md)

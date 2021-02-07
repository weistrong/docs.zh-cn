---
description: 了解详细信息： ICorDebugController：： Continue 方法
title: ICorDebugController::Continue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.Continue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Continue
helpviewer_keywords:
- Continue method [.NET Framework debugging]
- ICorDebugController::Continue method [.NET Framework debugging]
ms.assetid: 8684cd06-ad3e-48ef-832e-15320e1f43a2
topic_type:
- apiref
ms.openlocfilehash: e5858a8c287e8dd5a493a85c9f427ad8acd9ecc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710785"
---
# <a name="icordebugcontrollercontinue-method"></a><span data-ttu-id="b2239-103">ICorDebugController::Continue 方法</span><span class="sxs-lookup"><span data-stu-id="b2239-103">ICorDebugController::Continue Method</span></span>

<span data-ttu-id="b2239-104">在调用 [Stop 方法](icordebugcontroller-stop-method.md)后继续执行托管线程。</span><span class="sxs-lookup"><span data-stu-id="b2239-104">Resumes execution of managed threads after a call to [Stop Method](icordebugcontroller-stop-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2239-105">语法</span><span class="sxs-lookup"><span data-stu-id="b2239-105">Syntax</span></span>

```cpp
HRESULT Continue (
    [in] BOOL fIsOutOfBand
);
```

## <a name="parameters"></a><span data-ttu-id="b2239-106">参数</span><span class="sxs-lookup"><span data-stu-id="b2239-106">Parameters</span></span>

`fIsOutOfBand`  
<span data-ttu-id="b2239-107">中 `true` 如果从带外事件继续，则设置为; 否则设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b2239-107">[in] Set to `true` if continuing from an out-of-band event; otherwise, set to `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2239-108">备注</span><span class="sxs-lookup"><span data-stu-id="b2239-108">Remarks</span></span>

<span data-ttu-id="b2239-109">`Continue` 在调用方法后继续此过程 `ICorDebugController::Stop` 。</span><span class="sxs-lookup"><span data-stu-id="b2239-109">`Continue` continues the process after a call to the `ICorDebugController::Stop` method.</span></span>

<span data-ttu-id="b2239-110">在执行混合模式调试时，不要 `Continue` 在 Win32 事件线程上调用，除非从带外事件继续。</span><span class="sxs-lookup"><span data-stu-id="b2239-110">When doing mixed-mode debugging, do not call `Continue` on the Win32 event thread unless you are continuing from an out-of-band event.</span></span>

<span data-ttu-id="b2239-111">*带内事件* 是托管事件或普通非托管事件，在此期间，调试器支持与进程的托管状态交互。</span><span class="sxs-lookup"><span data-stu-id="b2239-111">An *in-band event* is either a managed event or a normal unmanaged event during which the debugger supports interaction with the managed state of the process.</span></span> <span data-ttu-id="b2239-112">在这种情况下，调试器接收 [ICorDebugUnmanagedCallback：:D ebugevent](icordebugunmanagedcallback-debugevent-method.md) 回调，其 `fOutOfBand` 参数设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b2239-112">In this case, the debugger receives the [ICorDebugUnmanagedCallback::DebugEvent](icordebugunmanagedcallback-debugevent-method.md) callback with its `fOutOfBand` parameter set to `false`.</span></span>

<span data-ttu-id="b2239-113">带 *外事件* 是一种非托管事件，在此过程中，由于发生事件，进程停止时无法与进程的托管状态交互。</span><span class="sxs-lookup"><span data-stu-id="b2239-113">An *out-of-band event* is an unmanaged event during which interaction with the managed state of the process is impossible while the process is stopped due to the event.</span></span> <span data-ttu-id="b2239-114">在这种情况下，调试器会接收 `ICorDebugUnmanagedCallback::DebugEvent` 回叫，其 `fOutOfBand` 参数设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="b2239-114">In this case, the debugger receives the `ICorDebugUnmanagedCallback::DebugEvent` callback with its `fOutOfBand` parameter set to `true`.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2239-115">要求</span><span class="sxs-lookup"><span data-stu-id="b2239-115">Requirements</span></span>

<span data-ttu-id="b2239-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b2239-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="b2239-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b2239-117">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="b2239-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b2239-118">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="b2239-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2239-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

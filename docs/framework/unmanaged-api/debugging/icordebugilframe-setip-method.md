---
description: 了解详细信息： ICorDebugILFrame：： SetIP 方法
title: ICorDebugILFrame::SetIP 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.SetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::SetIP
helpviewer_keywords:
- SetIP method, ICorDebugILFrame interface [.NET Framework debugging]
- ICorDebugILFrame::SetIP method [.NET Framework debugging]
ms.assetid: 23f38dc1-85e4-4263-9235-2d05bbb6a833
topic_type:
- apiref
ms.openlocfilehash: 75d2530a3d9151c64980316757074141776a78d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791317"
---
# <a name="icordebugilframesetip-method"></a><span data-ttu-id="c2413-103">ICorDebugILFrame::SetIP 方法</span><span class="sxs-lookup"><span data-stu-id="c2413-103">ICorDebugILFrame::SetIP Method</span></span>

<span data-ttu-id="c2413-104">将指令指针设置为 Microsoft 中间语言 (MSIL) 代码中的指定偏移位置。</span><span class="sxs-lookup"><span data-stu-id="c2413-104">Sets the instruction pointer to the specified offset location in the Microsoft intermediate language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2413-105">语法</span><span class="sxs-lookup"><span data-stu-id="c2413-105">Syntax</span></span>  
  
```cpp  
HRESULT SetIP (  
    [in] ULONG32 nOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c2413-106">参数</span><span class="sxs-lookup"><span data-stu-id="c2413-106">Parameters</span></span>  

 `nOffset`  
 <span data-ttu-id="c2413-107">MSIL 代码中的偏移位置。</span><span class="sxs-lookup"><span data-stu-id="c2413-107">The offset location in the MSIL code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c2413-108">备注</span><span class="sxs-lookup"><span data-stu-id="c2413-108">Remarks</span></span>  

 <span data-ttu-id="c2413-109">调用将 `SetIP` 立即使当前线程的所有帧和链无效。</span><span class="sxs-lookup"><span data-stu-id="c2413-109">Calls to `SetIP` immediately invalidate all frames and chains for the current thread.</span></span> <span data-ttu-id="c2413-110">如果在调用后调试器需要帧信息 `SetIP` ，则它必须执行新的堆栈跟踪。</span><span class="sxs-lookup"><span data-stu-id="c2413-110">If the debugger needs frame information after a call to `SetIP`, it must perform a new stack trace.</span></span>  
  
 <span data-ttu-id="c2413-111">[ICorDebug](icordebug-interface.md) 将尝试保持堆栈帧处于有效状态。</span><span class="sxs-lookup"><span data-stu-id="c2413-111">[ICorDebug](icordebug-interface.md) will attempt to keep the stack frame in a valid state.</span></span> <span data-ttu-id="c2413-112">但是，即使帧处于有效状态，仍可能会出现一些问题，如未初始化的局部变量。</span><span class="sxs-lookup"><span data-stu-id="c2413-112">However, even if the frame is in a valid state, there still may be problems such as uninitialized local variables.</span></span> <span data-ttu-id="c2413-113">调用方负责确保正在运行的程序的一致性。</span><span class="sxs-lookup"><span data-stu-id="c2413-113">The caller is responsible for ensuring the coherency of the running program.</span></span>  
  
 <span data-ttu-id="c2413-114">在64位平台上，指令指针不能移出 `catch` 或 `finally` 块。</span><span class="sxs-lookup"><span data-stu-id="c2413-114">On 64-bit platforms, the instruction pointer cannot be moved out of a `catch` or `finally` block.</span></span> <span data-ttu-id="c2413-115">如果 `SetIP` 调用来在64位平台上进行此类移动，则它将返回一个指示失败的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="c2413-115">If `SetIP` is called to make such a move on a 64-bit platform, it will return an HRESULT indicating failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2413-116">要求</span><span class="sxs-lookup"><span data-stu-id="c2413-116">Requirements</span></span>  

 <span data-ttu-id="c2413-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c2413-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2413-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c2413-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c2413-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c2413-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c2413-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2413-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

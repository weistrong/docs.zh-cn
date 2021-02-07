---
description: 了解详细信息： ICorDebugMutableDataTarget：： SetThreadContext 方法
title: ICorDebugMutableDataTarget::SetThreadContext 方法
ms.date: 03/30/2017
ms.assetid: 8c0d01d5-67e5-4522-9ccf-c8f3a78cb4fd
ms.openlocfilehash: 4674df92b72b44e19eff663c9a17dd8ca4b5a1b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722472"
---
# <a name="icordebugmutabledatatargetsetthreadcontext-method"></a><span data-ttu-id="0598d-103">ICorDebugMutableDataTarget::SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="0598d-103">ICorDebugMutableDataTarget::SetThreadContext Method</span></span>

<span data-ttu-id="0598d-104">设置某个线程的上下文（寄存器值）。</span><span class="sxs-lookup"><span data-stu-id="0598d-104">Sets the context (register values) for a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0598d-105">语法</span><span class="sxs-lookup"><span data-stu-id="0598d-105">Syntax</span></span>  
  
```cpp  
HRESULT SetThreadContext(  
   [in] DWORD dwThreadID,  
   [in] ULONG32 contextSize,   [in, size_is(contextSize)] const BYTE * pContext);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0598d-106">参数</span><span class="sxs-lookup"><span data-stu-id="0598d-106">Parameters</span></span>  

 `dwThreadID`  
 <span data-ttu-id="0598d-107">[in] 由操作系统定义的线程标识符。</span><span class="sxs-lookup"><span data-stu-id="0598d-107">[in] The operating system-defined thread identifier.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="0598d-108">[in] 要写入的 `pContext` 缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="0598d-108">[in] The size of the `pContext` buffer to be written.</span></span>  
  
 `pContext`  
 <span data-ttu-id="0598d-109">[in] 指向要写入的字节的指针。</span><span class="sxs-lookup"><span data-stu-id="0598d-109">[in] A pointer to the bytes to be written.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0598d-110">备注</span><span class="sxs-lookup"><span data-stu-id="0598d-110">Remarks</span></span>  

 <span data-ttu-id="0598d-111">`SetThreadContext` 方法将更新由操作系统定义的 `dwThreadID` 参数指定的当前线程上下文。</span><span class="sxs-lookup"><span data-stu-id="0598d-111">The `SetThreadContext` method updates the current context for the thread specified by the operating system-defined `dwThreadID` argument.</span></span> <span data-ttu-id="0598d-112">上下文记录的格式由 [ICorDebugDataTarget：： GetPlatform](icordebugdatatarget-getplatform-method.md) 方法指示的平台决定。</span><span class="sxs-lookup"><span data-stu-id="0598d-112">The format of the context record is determined by the platform indicated by the [ICorDebugDataTarget::GetPlatform](icordebugdatatarget-getplatform-method.md) method.</span></span> <span data-ttu-id="0598d-113">在 Windows 上，这是一个 [上下文](/windows/win32/api/winnt/ns-winnt-arm64_nt_context) 结构。</span><span class="sxs-lookup"><span data-stu-id="0598d-113">On Windows, this is a [CONTEXT](/windows/win32/api/winnt/ns-winnt-arm64_nt_context) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0598d-114">要求</span><span class="sxs-lookup"><span data-stu-id="0598d-114">Requirements</span></span>  

 <span data-ttu-id="0598d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0598d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0598d-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0598d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0598d-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0598d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0598d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0598d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0598d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="0598d-119">See also</span></span>

- [<span data-ttu-id="0598d-120">ICorDebugMutableDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="0598d-120">ICorDebugMutableDataTarget Interface</span></span>](icordebugmutabledatatarget-interface.md)
- [<span data-ttu-id="0598d-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="0598d-121">Debugging Interfaces</span></span>](debugging-interfaces.md)

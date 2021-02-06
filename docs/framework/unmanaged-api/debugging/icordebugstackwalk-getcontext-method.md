---
description: 了解详细信息： ICorDebugStackWalk：： GetContext 方法
title: ICorDebugStackWalk::GetContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.GetContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::GetContext
helpviewer_keywords:
- GetContext method, ICorDebugStackWalk interface [.NET Framework debugging]
- ICorDebugStackWalk::GetContext method [.NET Framework debugging]
ms.assetid: 081d1c95-152b-4797-8552-18453eb7b14b
topic_type:
- apiref
ms.openlocfilehash: 30beefaa1e0e2e4c5043cae7213658ac24e8a1b6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649606"
---
# <a name="icordebugstackwalkgetcontext-method"></a><span data-ttu-id="87805-103">ICorDebugStackWalk::GetContext 方法</span><span class="sxs-lookup"><span data-stu-id="87805-103">ICorDebugStackWalk::GetContext Method</span></span>

<span data-ttu-id="87805-104">返回 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象中的当前帧的上下文。</span><span class="sxs-lookup"><span data-stu-id="87805-104">Returns the context for the current frame in the [ICorDebugStackWalk](icordebugstackwalk-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87805-105">语法</span><span class="sxs-lookup"><span data-stu-id="87805-105">Syntax</span></span>  
  
```cpp  
HRESULT GetContext([in]  ULONG32 contextFlags,  
                   [in]  ULONG32 contextBufSize,  
                   [out] ULONG32* contextSize,  
                   [out, size_is(contextBufSize)] BYTE contextBuf[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="87805-106">参数</span><span class="sxs-lookup"><span data-stu-id="87805-106">Parameters</span></span>  

 `contextFlags`  
 <span data-ttu-id="87805-107">中指示) 中定义的上下文缓冲区 (内容的标志。</span><span class="sxs-lookup"><span data-stu-id="87805-107">[in] Flags that indicate the requested contents of the context buffer (defined in WinNT.h).</span></span>  
  
 `contextBufSize`  
 <span data-ttu-id="87805-108">中上下文缓冲区的已分配大小。</span><span class="sxs-lookup"><span data-stu-id="87805-108">[in] The allocated size of the context buffer.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="87805-109">弄上下文的实际大小。</span><span class="sxs-lookup"><span data-stu-id="87805-109">[out] The actual size of the context.</span></span> <span data-ttu-id="87805-110">此值必须小于或等于上下文缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="87805-110">This value must be less than or equal to the size of the context buffer.</span></span>  
  
 `contextBuf`  
 <span data-ttu-id="87805-111">弄上下文缓冲区。</span><span class="sxs-lookup"><span data-stu-id="87805-111">[out] The context buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="87805-112">返回值</span><span class="sxs-lookup"><span data-stu-id="87805-112">Return Value</span></span>  

 <span data-ttu-id="87805-113">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="87805-113">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="87805-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="87805-114">HRESULT</span></span>|<span data-ttu-id="87805-115">说明</span><span class="sxs-lookup"><span data-stu-id="87805-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="87805-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="87805-116">S_OK</span></span>|<span data-ttu-id="87805-117">当前帧的上下文已成功返回。</span><span class="sxs-lookup"><span data-stu-id="87805-117">The context for the current frame was successfully returned.</span></span>|  
|<span data-ttu-id="87805-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87805-118">E_FAIL</span></span>|<span data-ttu-id="87805-119">未能返回上下文。</span><span class="sxs-lookup"><span data-stu-id="87805-119">The context could not be returned.</span></span>|  
|<span data-ttu-id="87805-120">HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT 缓冲区) </span><span class="sxs-lookup"><span data-stu-id="87805-120">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT BUFFER)</span></span>|<span data-ttu-id="87805-121">上下文缓冲区太小。</span><span class="sxs-lookup"><span data-stu-id="87805-121">The context buffer is too small.</span></span>|  
|<span data-ttu-id="87805-122">CORDBG_E_PAST_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="87805-122">CORDBG_E_PAST_END_OF_STACK</span></span>|<span data-ttu-id="87805-123">帧指针已位于堆栈末尾;因此，不能访问其他帧。</span><span class="sxs-lookup"><span data-stu-id="87805-123">The frame pointer is already at the end of the stack; therefore, no additional frames can be accessed.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="87805-124">例外</span><span class="sxs-lookup"><span data-stu-id="87805-124">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="87805-125">备注</span><span class="sxs-lookup"><span data-stu-id="87805-125">Remarks</span></span>  

 <span data-ttu-id="87805-126">因为展开仅还原一个寄存器子集，如非易失性寄存器，所以在调用时，上下文可能与注册状态不完全匹配。</span><span class="sxs-lookup"><span data-stu-id="87805-126">Because unwinding restores only a subset of the registers, such as non-volatile registers, the context may not exactly match the register state at the time of the call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="87805-127">要求</span><span class="sxs-lookup"><span data-stu-id="87805-127">Requirements</span></span>  

 <span data-ttu-id="87805-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="87805-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="87805-129">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="87805-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="87805-130">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="87805-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="87805-131">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="87805-131">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87805-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="87805-132">See also</span></span>

- [<span data-ttu-id="87805-133">调试接口</span><span class="sxs-lookup"><span data-stu-id="87805-133">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="87805-134">调试</span><span class="sxs-lookup"><span data-stu-id="87805-134">Debugging</span></span>](index.md)

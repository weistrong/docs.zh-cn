---
description: 了解详细信息： ICorDebugVirtualUnwinder：： GetContext 方法
title: ICorDebugVirtualUnwinder::GetContext 方法
ms.date: 03/30/2017
ms.assetid: fe502a76-3068-47e5-a0a0-85ccb72dfac3
ms.openlocfilehash: 864f32ce82149658b2d4a617b08e8d7aa41fe642
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790524"
---
# <a name="icordebugvirtualunwindergetcontext-method"></a><span data-ttu-id="46169-103">ICorDebugVirtualUnwinder::GetContext 方法</span><span class="sxs-lookup"><span data-stu-id="46169-103">ICorDebugVirtualUnwinder::GetContext Method</span></span>

<span data-ttu-id="46169-104">获取此展开器的当前上下文。</span><span class="sxs-lookup"><span data-stu-id="46169-104">Gets the current context of this unwinder.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46169-105">语法</span><span class="sxs-lookup"><span data-stu-id="46169-105">Syntax</span></span>  
  
```cpp  
HRESULT GetContext(  
   [in] ULONG32 contextFlags,  
   [in] ULONG32 cbContextBuf,  
   [out] ULONG32* contextSize,  
   [out, size_is(cbContextBuf)] BYTE contextBuf[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="46169-106">参数</span><span class="sxs-lookup"><span data-stu-id="46169-106">Parameters</span></span>  

 `contextFlags`  
 <span data-ttu-id="46169-107">[in] 指定要返回上下文的哪些部分的标记（在 WinNT.h 中定义）。</span><span class="sxs-lookup"><span data-stu-id="46169-107">[in] Flags that specify which parts of the context to return (defined in WinNT.h).</span></span>  
  
 `cbContextBuf`  
 <span data-ttu-id="46169-108">[in] `contextBuf` 中的字节数。</span><span class="sxs-lookup"><span data-stu-id="46169-108">[in] The number of bytes in `contextBuf`.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="46169-109">[out] 指向实际写入 `contextBuf` 的字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="46169-109">[out] A pointer to the number of bytes actually written to `contextBuf`.</span></span>  
  
 `contextBuf`  
 <span data-ttu-id="46169-110">[out] 包含此开卷机当前上下文的字节数组。</span><span class="sxs-lookup"><span data-stu-id="46169-110">[out] A byte array that contains the current context of this unwinder.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="46169-111">返回值</span><span class="sxs-lookup"><span data-stu-id="46169-111">Return Value</span></span>  

 <span data-ttu-id="46169-112">由 mscordbi 接收到的任何失败的 HRESULT 都被视为是致命的，并将导致 ICorDebug API 返回 `CORDBG_E_DATA_TARGET_ERROR`。</span><span class="sxs-lookup"><span data-stu-id="46169-112">Any failing HRESULT value received by mscordbi is considered fatal and will cause ICorDebug APIs to return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="46169-113">备注</span><span class="sxs-lookup"><span data-stu-id="46169-113">Remarks</span></span>  

 <span data-ttu-id="46169-114">将自变量的初始值设置 `contextBuf` 为通过调用 [ICorDebugStackWalk：： GetContext](icordebugstackwalk-getcontext-method.md) 方法返回的上下文缓冲区。</span><span class="sxs-lookup"><span data-stu-id="46169-114">You set the initial value of the `contextBuf` argument to the context buffer returned by calling the [ICorDebugStackWalk::GetContext](icordebugstackwalk-getcontext-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="46169-115">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="46169-115">This method is available with .NET Native only.</span></span>  
  
 <span data-ttu-id="46169-116">因为回退可能仅还原寄存器子集（例如非易失性寄存器），所以在实际方法调用时，上下文可能并不与寄存器状态完全匹配。</span><span class="sxs-lookup"><span data-stu-id="46169-116">Because unwinding may only restore a subset of the registers, such as the non-volatile registers only, the context may not exactly match the register state at the time of the actual method call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46169-117">要求</span><span class="sxs-lookup"><span data-stu-id="46169-117">Requirements</span></span>  

 <span data-ttu-id="46169-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46169-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46169-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46169-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46169-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46169-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46169-121">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46169-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46169-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="46169-122">See also</span></span>

- [<span data-ttu-id="46169-123">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="46169-123">ICorDebugMemoryBuffer Interface</span></span>](icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="46169-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="46169-124">Debugging Interfaces</span></span>](debugging-interfaces.md)

---
description: 了解详细信息： ICorDebugRegisterSet：： GetThreadContext 方法
title: ICorDebugRegisterSet::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetThreadContext
helpviewer_keywords:
- GetThreadContext method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::GetThreadContext method [.NET Framework debugging]
ms.assetid: 0f63400b-dc1c-48d6-b51a-75c3f7f28e03
topic_type:
- apiref
ms.openlocfilehash: be6384562858d04b6e139eda83c172c09f2dfc0d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690790"
---
# <a name="icordebugregistersetgetthreadcontext-method"></a><span data-ttu-id="a4861-103">ICorDebugRegisterSet::GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="a4861-103">ICorDebugRegisterSet::GetThreadContext Method</span></span>

<span data-ttu-id="a4861-104">获取当前线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="a4861-104">Gets the context of the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4861-105">语法</span><span class="sxs-lookup"><span data-stu-id="a4861-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadContext(  
    [in] ULONG32 contextSize,  
    [in, out, length_is(contextSize),  
        size_is(contextSize)] BYTE context[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a4861-106">参数</span><span class="sxs-lookup"><span data-stu-id="a4861-106">Parameters</span></span>  

 `contextSize`  
 <span data-ttu-id="a4861-107">中数组的大小（以字节为单位） `context` 。</span><span class="sxs-lookup"><span data-stu-id="a4861-107">[in] The size, in bytes, of the `context` array.</span></span>  
  
 `context`  
 <span data-ttu-id="a4861-108">[in，out]为当前平台构成 Win32 结构的字节数组 `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="a4861-108">[in, out] An array of bytes that compose the Win32 `CONTEXT` structure for the current platform.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a4861-109">备注</span><span class="sxs-lookup"><span data-stu-id="a4861-109">Remarks</span></span>  

 <span data-ttu-id="a4861-110">调试器应调用此函数，而不是 Win32 `GetThreadContext` 函数，因为该线程可能处于暂时更改其上下文的 "被劫持" 状态。</span><span class="sxs-lookup"><span data-stu-id="a4861-110">The debugger should call this function instead of the Win32 `GetThreadContext` function, because the thread may be in a "hijacked" state where its context has been temporarily changed.</span></span> <span data-ttu-id="a4861-111">返回的数据是 `CONTEXT` 当前平台的 Win32 结构。</span><span class="sxs-lookup"><span data-stu-id="a4861-111">The data returned is a Win32 `CONTEXT` structure for the current platform.</span></span>  
  
 <span data-ttu-id="a4861-112">对于非叶帧，客户端应使用 [ICorDebugRegisterSet：： GetRegistersAvailable](icordebugregisterset-getregistersavailable-method.md)检查哪些寄存器是有效的。</span><span class="sxs-lookup"><span data-stu-id="a4861-112">For non-leaf frames, clients should check which registers are valid by using [ICorDebugRegisterSet::GetRegistersAvailable](icordebugregisterset-getregistersavailable-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4861-113">要求</span><span class="sxs-lookup"><span data-stu-id="a4861-113">Requirements</span></span>  

 <span data-ttu-id="a4861-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a4861-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4861-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a4861-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a4861-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a4861-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a4861-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4861-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4861-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4861-118">See also</span></span>

- [<span data-ttu-id="a4861-119">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="a4861-119">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
- [<span data-ttu-id="a4861-120">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="a4861-120">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)

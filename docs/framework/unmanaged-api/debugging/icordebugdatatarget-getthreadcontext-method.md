---
description: 了解详细信息： ICorDebugDataTarget：： GetThreadContext 方法
title: ICorDebugDataTarget::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget.GetThreadContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget::GetThreadContext
helpviewer_keywords:
- ICorDebugDataTarget::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: c8954268-1821-4b23-b665-dbb55f2af31b
topic_type:
- apiref
ms.openlocfilehash: cf40579aa0a495af4e5e775334d177ca6f3da86f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710629"
---
# <a name="icordebugdatatargetgetthreadcontext-method"></a><span data-ttu-id="8a6df-103">ICorDebugDataTarget::GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="8a6df-103">ICorDebugDataTarget::GetThreadContext Method</span></span>

<span data-ttu-id="8a6df-104">返回指定线程的当前线程上下文。</span><span class="sxs-lookup"><span data-stu-id="8a6df-104">Returns the current thread context for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a6df-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a6df-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadContext(  
       [in] DWORD dwThreadID,  
       [in] ULONG32 contextFlags,  
       [in] ULONG32 contextSize,  
       [out, size_is(contextSize)] BYTE * pContext);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a6df-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a6df-106">Parameters</span></span>  

 `dwThreadID`  
 <span data-ttu-id="8a6df-107">中要检索其上下文的线程的标识符。</span><span class="sxs-lookup"><span data-stu-id="8a6df-107">[in] The identifier of the thread whose context is to be retrieved.</span></span> <span data-ttu-id="8a6df-108">标识符由操作系统定义。</span><span class="sxs-lookup"><span data-stu-id="8a6df-108">The identifier is defined by the operating system.</span></span>  
  
 `contextFlags`  
 <span data-ttu-id="8a6df-109">中平台相关标志的按位组合，用于指示应读取上下文的哪些部分。</span><span class="sxs-lookup"><span data-stu-id="8a6df-109">[in] A bitwise combination of platform-dependent flags that indicate which portions of the context should be read.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="8a6df-110">[输入] `pContext` 的大小。</span><span class="sxs-lookup"><span data-stu-id="8a6df-110">[in] The size of `pContext`.</span></span>  
  
 `pContext`  
 <span data-ttu-id="8a6df-111">弄将存储线程上下文的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="8a6df-111">[out] The buffer where the thread context will be stored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8a6df-112">备注</span><span class="sxs-lookup"><span data-stu-id="8a6df-112">Remarks</span></span>  

 <span data-ttu-id="8a6df-113">在 Windows 平台上， `pContext` 必须是 `CONTEXT`) 在 [ICorDebugDataTarget：： GetPlatform](icordebugdatatarget-getplatform-method.md) 方法指定的计算机类型中定义的结构 (。</span><span class="sxs-lookup"><span data-stu-id="8a6df-113">On Windows platforms, `pContext` must be a `CONTEXT` structure (defined in WinNT.h) that is appropriate for the machine type specified by the [ICorDebugDataTarget::GetPlatform](icordebugdatatarget-getplatform-method.md) method.</span></span> <span data-ttu-id="8a6df-114">`contextFlags` 必须与结构的字段具有相同的值 `ContextFlags` `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="8a6df-114">`contextFlags` must have the same values as the `ContextFlags` field of the `CONTEXT` structure.</span></span> <span data-ttu-id="8a6df-115">`CONTEXT`结构特定于处理器; 有关详细信息，请参阅 WinNT .h 文件。</span><span class="sxs-lookup"><span data-stu-id="8a6df-115">The `CONTEXT` structure is processor-specific; refer to the WinNT.h file for details.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a6df-116">要求</span><span class="sxs-lookup"><span data-stu-id="8a6df-116">Requirements</span></span>  

 <span data-ttu-id="8a6df-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a6df-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a6df-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8a6df-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8a6df-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a6df-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a6df-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a6df-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a6df-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a6df-121">See also</span></span>

- [<span data-ttu-id="8a6df-122">ICorDebugDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="8a6df-122">ICorDebugDataTarget Interface</span></span>](icordebugdatatarget-interface.md)
- [<span data-ttu-id="8a6df-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="8a6df-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="8a6df-124">调试</span><span class="sxs-lookup"><span data-stu-id="8a6df-124">Debugging</span></span>](index.md)

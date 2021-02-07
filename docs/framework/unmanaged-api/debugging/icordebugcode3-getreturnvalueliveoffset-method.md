---
description: 了解详细信息： ICorDebugCode3：： GetReturnValueLiveOffset 方法
title: ICorDebugCode3::GetReturnValueLiveOffset 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugCode3.GetReturnValueLiveOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode3::GetReturnValueLiveOffset
helpviewer_keywords:
- ICorDebugCode3::GetReturnValueLiveOffset method [.NET Framework debugging]
- GetReturnValueLiveOffset method [.NET Framework debugging]
ms.assetid: 8c2ff5d8-8c04-4423-b1e1-e1c8764b36d3
topic_type:
- apiref
ms.openlocfilehash: 6ec9a342805c047d7331c3ce2af2a4ffba596a26
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711006"
---
# <a name="icordebugcode3getreturnvalueliveoffset-method"></a><span data-ttu-id="9df02-103">ICorDebugCode3::GetReturnValueLiveOffset 方法</span><span class="sxs-lookup"><span data-stu-id="9df02-103">ICorDebugCode3::GetReturnValueLiveOffset Method</span></span>

<span data-ttu-id="9df02-104">对于指定的 IL 偏移量，获取应放置断点的本机偏移量，以便调试器可以从函数中获取返回值。</span><span class="sxs-lookup"><span data-stu-id="9df02-104">For a specified IL offset, gets the native offsets where a breakpoint should be placed so that the debugger can obtain the return value from a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9df02-105">语法</span><span class="sxs-lookup"><span data-stu-id="9df02-105">Syntax</span></span>  
  
```cpp
HRESULT GetReturnValueLiveOffset(  
    [in] ULONG32 ILoffset,  
    [in] ULONG32 bufferSize,
    [out] ULONG32 *pFetched,
    [out, size_is(buffersize), length_is(*pFetched)] ULong32 pOffsets[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9df02-106">参数</span><span class="sxs-lookup"><span data-stu-id="9df02-106">Parameters</span></span>  

 `ILoffset`  
 <span data-ttu-id="9df02-107">IL 偏移量。</span><span class="sxs-lookup"><span data-stu-id="9df02-107">The IL offset.</span></span> <span data-ttu-id="9df02-108">它必须是函数调用站点，否则函数调用将失败。</span><span class="sxs-lookup"><span data-stu-id="9df02-108">It must be a function call site or the function call will fail.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="9df02-109">可用于存储的字节数 `pOffsets` 。</span><span class="sxs-lookup"><span data-stu-id="9df02-109">The number of bytes available to store `pOffsets`.</span></span>  
  
 `pFetched`  
 <span data-ttu-id="9df02-110">指向实际返回的偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="9df02-110">A pointer to the number of offsets actually returned.</span></span> <span data-ttu-id="9df02-111">通常，其值为1，但单个 IL 指令可以映射到多个 `CALL` 程序集指令。</span><span class="sxs-lookup"><span data-stu-id="9df02-111">Usually, its value is 1, but a single IL instruction can map to multiple `CALL` assembly instructions.</span></span>  
  
 `pOffsets`  
 <span data-ttu-id="9df02-112">本机偏移量的数组。</span><span class="sxs-lookup"><span data-stu-id="9df02-112">An array of native offsets.</span></span> <span data-ttu-id="9df02-113">通常， `pOffsets` 包含单个偏移量，但单个 IL 指令可以映射到多个 `CALL` 程序集指令。</span><span class="sxs-lookup"><span data-stu-id="9df02-113">Typically, `pOffsets` contains a single offset, although a single IL instruction can map to multiple map to multiple `CALL` assembly instructions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9df02-114">备注</span><span class="sxs-lookup"><span data-stu-id="9df02-114">Remarks</span></span>  

 <span data-ttu-id="9df02-115">此方法与 [ICorDebugILFrame3：： GetReturnValueForILOffset](icordebugilframe3-getreturnvalueforiloffset-method.md) 方法一起使用，以获取返回引用类型的方法的返回值。</span><span class="sxs-lookup"><span data-stu-id="9df02-115">This method is used along with the [ICorDebugILFrame3::GetReturnValueForILOffset](icordebugilframe3-getreturnvalueforiloffset-method.md) method to get the return value of a method that returns a reference type.</span></span> <span data-ttu-id="9df02-116">如果将 IL 偏移量传递给函数调用站点，此方法将返回一个或多个本机偏移量。</span><span class="sxs-lookup"><span data-stu-id="9df02-116">Passing an IL offset to a function call site to this method returns one or more native offsets.</span></span> <span data-ttu-id="9df02-117">然后，调试器可以在函数中的这些本机偏移量上设置断点。</span><span class="sxs-lookup"><span data-stu-id="9df02-117">The debugger can then set breakpoints on these native offsets in the function.</span></span> <span data-ttu-id="9df02-118">当调试器遇到其中一个断点时，可以将传递给此方法的同一 IL 偏移传递给 [ICorDebugILFrame3：： GetReturnValueForILOffset](icordebugilframe3-getreturnvalueforiloffset-method.md) 方法以获取返回值。</span><span class="sxs-lookup"><span data-stu-id="9df02-118">When the debugger hits one of the breakpoints, you can then pass the same IL offset that you passed to this method to the [ICorDebugILFrame3::GetReturnValueForILOffset](icordebugilframe3-getreturnvalueforiloffset-method.md) method to get the return value.</span></span> <span data-ttu-id="9df02-119">调试器随后应清除它所设置的所有断点。</span><span class="sxs-lookup"><span data-stu-id="9df02-119">The debugger should then clear all the breakpoints that it set.</span></span>  
  
> [!WARNING]
> <span data-ttu-id="9df02-120">`ICorDebugCode3::GetReturnValueLiveOffset`和[ICorDebugILFrame3：： GetReturnValueForILOffset](icordebugilframe3-getreturnvalueforiloffset-method.md)方法只允许获取引用类型的返回值信息。</span><span class="sxs-lookup"><span data-stu-id="9df02-120">The `ICorDebugCode3::GetReturnValueLiveOffset` and [ICorDebugILFrame3::GetReturnValueForILOffset](icordebugilframe3-getreturnvalueforiloffset-method.md) methods allow you to get return value information for reference types only.</span></span> <span data-ttu-id="9df02-121">从值类型检索返回值信息 (也就是说，不支持从) 派生的所有类型 <xref:System.ValueType> 。</span><span class="sxs-lookup"><span data-stu-id="9df02-121">Retrieving return value information from value types (that is, all types that derive from <xref:System.ValueType>) is not supported.</span></span>  
  
 <span data-ttu-id="9df02-122">函数将返回 `HRESULT` 下表中显示的值。</span><span class="sxs-lookup"><span data-stu-id="9df02-122">The function returns the `HRESULT` values shown in the following table.</span></span>  
  
|<span data-ttu-id="9df02-123">`HRESULT` 值</span><span class="sxs-lookup"><span data-stu-id="9df02-123">`HRESULT` value</span></span>|<span data-ttu-id="9df02-124">说明</span><span class="sxs-lookup"><span data-stu-id="9df02-124">Description</span></span>|  
|---------------------|-----------------|  
|`S_OK`|<span data-ttu-id="9df02-125">成功。</span><span class="sxs-lookup"><span data-stu-id="9df02-125">Success.</span></span>|  
|`CORDBG_E_INVALID_OPCODE`|<span data-ttu-id="9df02-126">给定的 IL 偏移量站点不是调用指令，或该函数返回 `void` 。</span><span class="sxs-lookup"><span data-stu-id="9df02-126">The given IL offset site is not a call instruction, or the function returns `void`.</span></span>|  
|`CORDBG_E_UNSUPPORTED`|<span data-ttu-id="9df02-127">给定的 IL 偏移量是正确的调用，但不支持返回类型来获取返回值。</span><span class="sxs-lookup"><span data-stu-id="9df02-127">The given IL offset is a proper call, but the return type is unsupported for getting a return value.</span></span>|  
  
 <span data-ttu-id="9df02-128">`ICorDebugCode3::GetReturnValueLiveOffset`方法仅适用于基于 x86 的和 AMD64 系统。</span><span class="sxs-lookup"><span data-stu-id="9df02-128">The `ICorDebugCode3::GetReturnValueLiveOffset` method is available only on x86-based and AMD64 systems.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9df02-129">要求</span><span class="sxs-lookup"><span data-stu-id="9df02-129">Requirements</span></span>  

 <span data-ttu-id="9df02-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9df02-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9df02-131">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9df02-131">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9df02-132">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9df02-132">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9df02-133">**.NET Framework 版本：**[!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9df02-133">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9df02-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="9df02-134">See also</span></span>

- [<span data-ttu-id="9df02-135">GetReturnValueForILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="9df02-135">GetReturnValueForILOffset Method</span></span>](icordebugilframe3-getreturnvalueforiloffset-method.md)
- [<span data-ttu-id="9df02-136">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="9df02-136">ICorDebugCode3 Interface</span></span>](icordebugcode3-interface.md)

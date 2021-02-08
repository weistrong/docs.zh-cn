---
description: 了解详细信息： ICorDebugILFrame3：： GetReturnValueForILOffset 方法
title: ICorDebugILFrame3::GetReturnValueForILOffset 方法
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
api_name:
- ICorDebugILFrame3.GetReturnValueForILOffset
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 06522727-5f64-4391-9331-11386883c352
topic_type:
- apiref
ms.openlocfilehash: 4be4cb3a108394f2701f6690b06f6c2252ae25cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791265"
---
# <a name="icordebugilframe3getreturnvalueforiloffset-method"></a><span data-ttu-id="d2b61-103">ICorDebugILFrame3::GetReturnValueForILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="d2b61-103">ICorDebugILFrame3::GetReturnValueForILOffset Method</span></span>

<span data-ttu-id="d2b61-104">获取一个 "ICorDebugValue" 对象，该对象封装函数的返回值。</span><span class="sxs-lookup"><span data-stu-id="d2b61-104">Gets an "ICorDebugValue" object that encapsulates the return value of a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2b61-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2b61-105">Syntax</span></span>  
  
```cpp
HRESULT GetReturnValueForILOffset(  
    ULONG32 ILoffset,
    [out] ICorDebugValue **ppReturnValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2b61-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2b61-106">Parameters</span></span>  

 `ILOffset`  
 <span data-ttu-id="d2b61-107">IL 偏移量。</span><span class="sxs-lookup"><span data-stu-id="d2b61-107">The IL offset.</span></span> <span data-ttu-id="d2b61-108">请参阅“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="d2b61-108">See the Remarks section.</span></span>  
  
 `ppReturnValue`  
 <span data-ttu-id="d2b61-109">一个指向 "ICorDebugValue" 接口对象地址的指针，该对象提供有关函数调用的返回值的信息。</span><span class="sxs-lookup"><span data-stu-id="d2b61-109">A pointer to the address of an "ICorDebugValue" interface object that provides information about the return value of a function call.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d2b61-110">备注</span><span class="sxs-lookup"><span data-stu-id="d2b61-110">Remarks</span></span>  

 <span data-ttu-id="d2b61-111">此方法与 [ICorDebugCode3：： GetReturnValueLiveOffset](icordebugcode3-getreturnvalueliveoffset-method.md) 方法一起使用，以获取方法的返回值。</span><span class="sxs-lookup"><span data-stu-id="d2b61-111">This method is used along with the [ICorDebugCode3::GetReturnValueLiveOffset](icordebugcode3-getreturnvalueliveoffset-method.md) method to get the return value of a method.</span></span> <span data-ttu-id="d2b61-112">这对于返回值被忽略的方法特别有用，如以下两个代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="d2b61-112">It is particularly useful in the case of methods whose return values are ignored, as in the following two code examples.</span></span> <span data-ttu-id="d2b61-113">第一个示例调用 <xref:System.Int32.TryParse%2A?displayProperty=nameWithType> 方法，但忽略方法的返回值。</span><span class="sxs-lookup"><span data-stu-id="d2b61-113">The first example calls the <xref:System.Int32.TryParse%2A?displayProperty=nameWithType> method, but ignores the method's return value.</span></span>  
  
 [!code-csharp[Unmanaged.Debugging.MRV#1](../../../../samples/snippets/csharp/VS_Snippets_CLR/unmanaged.debugging.mrv/cs/mrv1.cs#1)]
 [!code-vb[Unmanaged.Debugging.MRV#1](../../../../samples/snippets/visualbasic/VS_Snippets_CLR/unmanaged.debugging.mrv/vb/mrv1.vb#1)]  
  
 <span data-ttu-id="d2b61-114">第二个示例演示了调试中更常见的问题。</span><span class="sxs-lookup"><span data-stu-id="d2b61-114">The second example illustrates a much more common problem in debugging.</span></span> <span data-ttu-id="d2b61-115">因为方法在方法调用中用作参数，所以仅当调试器逐步执行调用的方法时，才能访问其返回值。</span><span class="sxs-lookup"><span data-stu-id="d2b61-115">Because a method is used as an argument in a method call, its return value is accessible only when the debugger steps through the called method.</span></span> <span data-ttu-id="d2b61-116">在许多情况下，尤其是在外部库中定义了所调用的方法时，这是不可能的。</span><span class="sxs-lookup"><span data-stu-id="d2b61-116">In many cases, particularly when the called method is defined in an external library, that is not possible.</span></span>  
  
 [!code-csharp[Unmanaged.Debugging.MRV#2](../../../../samples/snippets/csharp/VS_Snippets_CLR/unmanaged.debugging.mrv/cs/mrv2.cs#2)]
 [!code-vb[Unmanaged.Debugging.MRV#2](../../../../samples/snippets/visualbasic/VS_Snippets_CLR/unmanaged.debugging.mrv/vb/mrv2.vb#2)]  
  
 <span data-ttu-id="d2b61-117">如果将 [ICorDebugCode3：： GetReturnValueLiveOffset](icordebugcode3-getreturnvalueliveoffset-method.md) 方法传递给函数调用站点的 IL 偏移量，它将返回一个或多个本机偏移量。</span><span class="sxs-lookup"><span data-stu-id="d2b61-117">If you pass the [ICorDebugCode3::GetReturnValueLiveOffset](icordebugcode3-getreturnvalueliveoffset-method.md) method an IL offset to a function call site, it returns one or more native offsets.</span></span> <span data-ttu-id="d2b61-118">然后，调试器可以在函数中的这些本机偏移量上设置断点。</span><span class="sxs-lookup"><span data-stu-id="d2b61-118">The debugger can then set breakpoints on these native offsets in the function.</span></span> <span data-ttu-id="d2b61-119">当调试器遇到其中一个断点时，您可以传递您传递给此方法的同一 IL 偏移量来获取返回值。</span><span class="sxs-lookup"><span data-stu-id="d2b61-119">When the debugger hits one of the breakpoints, you can then pass the same IL offset that you passed to this method to get the return value.</span></span> <span data-ttu-id="d2b61-120">调试器随后应清除它所设置的所有断点。</span><span class="sxs-lookup"><span data-stu-id="d2b61-120">The debugger should then clear all the breakpoints that it set.</span></span>  
  
> [!WARNING]
> <span data-ttu-id="d2b61-121">[ICorDebugCode3：： GetReturnValueLiveOffset 方法](icordebugcode3-getreturnvalueliveoffset-method.md)和 `ICorDebugILFrame3::GetReturnValueForILOffset` 方法仅允许获取引用类型的返回值信息。</span><span class="sxs-lookup"><span data-stu-id="d2b61-121">The [ICorDebugCode3::GetReturnValueLiveOffset Method](icordebugcode3-getreturnvalueliveoffset-method.md) and `ICorDebugILFrame3::GetReturnValueForILOffset` methods allow you to get return value information for reference types only.</span></span> <span data-ttu-id="d2b61-122">从值类型检索返回值信息 (也就是说，不支持从) 派生的所有类型 <xref:System.ValueType> 。</span><span class="sxs-lookup"><span data-stu-id="d2b61-122">Retrieving return value information from value types (that is, all types that derive from <xref:System.ValueType>) is not supported.</span></span>  
  
 <span data-ttu-id="d2b61-123">参数指定的 IL 偏移量 `ILOffset` 应位于函数调用站点上，并且调试对象应在 [ICorDebugCode3：： GetReturnValueLiveOffset](icordebugcode3-getreturnvalueliveoffset-method.md) 方法为同一 IL 偏移量返回的本机偏移量处停止。</span><span class="sxs-lookup"><span data-stu-id="d2b61-123">The IL offset specified by the `ILOffset` parameter should be at a function call site, and the debuggee should be stopped at a breakpoint set at the native offset returned by the [ICorDebugCode3::GetReturnValueLiveOffset](icordebugcode3-getreturnvalueliveoffset-method.md) method for the same IL offset.</span></span> <span data-ttu-id="d2b61-124">如果在指定的 IL 偏移量的正确位置没有停止调试对象，则 API 将失败。</span><span class="sxs-lookup"><span data-stu-id="d2b61-124">If the debuggee is not stopped at the correct location for the specified IL offset, the API will fail.</span></span>  
  
 <span data-ttu-id="d2b61-125">如果函数调用不返回值，则 API 将失败。</span><span class="sxs-lookup"><span data-stu-id="d2b61-125">If the function call doesn't return a value, the API will fail.</span></span>  
  
 <span data-ttu-id="d2b61-126">`ICorDebugILFrame3::GetReturnValueForILOffset`方法仅适用于基于 x86 的和 AMD64 系统。</span><span class="sxs-lookup"><span data-stu-id="d2b61-126">The `ICorDebugILFrame3::GetReturnValueForILOffset` method is available only on x86-based and AMD64 systems.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2b61-127">要求</span><span class="sxs-lookup"><span data-stu-id="d2b61-127">Requirements</span></span>  

 <span data-ttu-id="d2b61-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2b61-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2b61-129">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d2b61-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d2b61-130">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2b61-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2b61-131">**.NET Framework 版本：**[!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2b61-131">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2b61-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2b61-132">See also</span></span>

- [<span data-ttu-id="d2b61-133">GetReturnValueLiveOffset 方法</span><span class="sxs-lookup"><span data-stu-id="d2b61-133">GetReturnValueLiveOffset Method</span></span>](icordebugcode3-getreturnvalueliveoffset-method.md)
- [<span data-ttu-id="d2b61-134">ICorDebugILFrame3 接口</span><span class="sxs-lookup"><span data-stu-id="d2b61-134">ICorDebugILFrame3 Interface</span></span>](icordebugilframe3-interface.md)

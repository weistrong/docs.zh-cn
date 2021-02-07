---
description: 了解详细信息： ICorDebugDataTarget2：： CreateVirtualUnwinder 方法
title: ICorDebugDataTarget2::CreateVirtualUnwinder 方法
ms.date: 03/30/2017
ms.assetid: 354c8b4c-7d23-45c6-a7d7-3be4c2a5b772
ms.openlocfilehash: 0646c85000f42b303769d6587354b3105e2deabd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764406"
---
# <a name="icordebugdatatarget2createvirtualunwinder-method"></a><span data-ttu-id="93c51-103">ICorDebugDataTarget2::CreateVirtualUnwinder 方法</span><span class="sxs-lookup"><span data-stu-id="93c51-103">ICorDebugDataTarget2::CreateVirtualUnwinder Method</span></span>

<span data-ttu-id="93c51-104">创建一个从初始上下文（不一定是线程叶）开始展开的新堆栈开卷机。</span><span class="sxs-lookup"><span data-stu-id="93c51-104">Creates a new stack unwinder that starts unwinding from an initial context (which isn't necessarily the leaf of a thread).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93c51-105">语法</span><span class="sxs-lookup"><span data-stu-id="93c51-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateVirtualUnwinder(  
    [in] DWORD nativeThreadID,  
    [in] ULONG32 contextFlags,  
    [in] ULONG32 cbContext,  
    [in, size_is(cbContext)] BYTE initialContext[],  
    [out] ICorDebugVirtualUnwinder ** ppUnwinder);  
};  
```  
  
## <a name="parameters"></a><span data-ttu-id="93c51-106">参数</span><span class="sxs-lookup"><span data-stu-id="93c51-106">Parameters</span></span>  

 <span data-ttu-id="93c51-107">本机线程ID</span><span class="sxs-lookup"><span data-stu-id="93c51-107">nativeThreadID</span></span>  
 <span data-ttu-id="93c51-108">[输入] 线程（其堆栈未展开）的本机线程 ID。</span><span class="sxs-lookup"><span data-stu-id="93c51-108">[in] The native thread ID of the thread whose stack is to be unwound.</span></span>  
  
 <span data-ttu-id="93c51-109">上下文标记</span><span class="sxs-lookup"><span data-stu-id="93c51-109">contextFlags</span></span>  
 <span data-ttu-id="93c51-110">[输入] `initialContext` 中规定了指定上下文部分的标记。</span><span class="sxs-lookup"><span data-stu-id="93c51-110">[in] Flags that specify which parts of the context are defined in `initialContext`.</span></span>  
  
 <span data-ttu-id="93c51-111">cb上下文</span><span class="sxs-lookup"><span data-stu-id="93c51-111">cbContext</span></span>  
 <span data-ttu-id="93c51-112">[输入] `initialContext` 的大小。</span><span class="sxs-lookup"><span data-stu-id="93c51-112">[in] The size of `initialContext`.</span></span>  
  
 <span data-ttu-id="93c51-113">初始上下文</span><span class="sxs-lookup"><span data-stu-id="93c51-113">initialContext</span></span>  
 <span data-ttu-id="93c51-114">[输入] 上下文中的数据。</span><span class="sxs-lookup"><span data-stu-id="93c51-114">[in] The data in the context.</span></span>  
  
 <span data-ttu-id="93c51-115">pp开卷机</span><span class="sxs-lookup"><span data-stu-id="93c51-115">ppUnwinder</span></span>  
 <span data-ttu-id="93c51-116">[输出] 指针指向“ICor调试虚拟开卷机”接口对象的地址。</span><span class="sxs-lookup"><span data-stu-id="93c51-116">[out] A pointer to the address of an ICorDebugVirtualUnwinder interface object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="93c51-117">返回值</span><span class="sxs-lookup"><span data-stu-id="93c51-117">Return Value</span></span>  

 <span data-ttu-id="93c51-118">`S_OK` 如果成功。</span><span class="sxs-lookup"><span data-stu-id="93c51-118">`S_OK` if successful.</span></span> <span data-ttu-id="93c51-119">所有其他 `HRESULT` 都表示故障。</span><span class="sxs-lookup"><span data-stu-id="93c51-119">Any other `HRESULT` indicates failure.</span></span> <span data-ttu-id="93c51-120">`HRESULT`Mscordbi.dll 收到的任何失败都视为严重错误，并导致[ICorDebug](icordebug-interface.md)方法返回 `CORDBG_E_DATA_TARGET_ERROR` 。</span><span class="sxs-lookup"><span data-stu-id="93c51-120">Any failing `HRESULT` received by mscordbi is considered fatal and causes [ICorDebug](icordebug-interface.md) methods to return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="93c51-121">备注</span><span class="sxs-lookup"><span data-stu-id="93c51-121">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="93c51-122">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="93c51-122">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93c51-123">要求</span><span class="sxs-lookup"><span data-stu-id="93c51-123">Requirements</span></span>  

 <span data-ttu-id="93c51-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="93c51-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93c51-125">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="93c51-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="93c51-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93c51-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93c51-127">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93c51-127">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93c51-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="93c51-128">See also</span></span>

- [<span data-ttu-id="93c51-129">“ICor调试数据目标2”接口</span><span class="sxs-lookup"><span data-stu-id="93c51-129">ICorDebugDataTarget2 Interface</span></span>](icordebugdatatarget2-interface.md)
- [<span data-ttu-id="93c51-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="93c51-130">Debugging Interfaces</span></span>](debugging-interfaces.md)

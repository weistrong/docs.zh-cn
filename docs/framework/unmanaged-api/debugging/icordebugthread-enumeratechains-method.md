---
description: 了解详细信息： ICorDebugThread：： EnumerateChains 方法
title: ICorDebugThread::EnumerateChains 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.EnumerateChains
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::EnumerateChains
helpviewer_keywords:
- EnumerateChains method [.NET Framework debugging]
- ICorDebugThread::EnumerateChains method [.NET Framework debugging]
ms.assetid: ec00bc21-117e-4acd-9301-2cfafd5be8d3
topic_type:
- apiref
ms.openlocfilehash: b9184a1b298e1d29970c5e56ceca76715b0ed096
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659291"
---
# <a name="icordebugthreadenumeratechains-method"></a><span data-ttu-id="db516-103">ICorDebugThread::EnumerateChains 方法</span><span class="sxs-lookup"><span data-stu-id="db516-103">ICorDebugThread::EnumerateChains Method</span></span>

<span data-ttu-id="db516-104">获取一个接口指针，该指针指向包含此 ICorDebugThread 对象中所有堆栈链的 ICorDebugChainEnum 枚举器。</span><span class="sxs-lookup"><span data-stu-id="db516-104">Gets an interface pointer to an ICorDebugChainEnum enumerator that contains all the stack chains in this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db516-105">语法</span><span class="sxs-lookup"><span data-stu-id="db516-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateChains (  
    [out] ICorDebugChainEnum **ppChains  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db516-106">参数</span><span class="sxs-lookup"><span data-stu-id="db516-106">Parameters</span></span>  

 `ppChains`  
 <span data-ttu-id="db516-107">弄指向对象地址的指针，该 `ICorDebugChainEnum` 对象允许枚举此线程中的所有堆栈链，从活动 (开始，即最近的) 链。</span><span class="sxs-lookup"><span data-stu-id="db516-107">[out] A pointer to the address of an `ICorDebugChainEnum` object that allows enumeration of all the stack chains in this thread, starting at the active (that is, the most recent) chain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db516-108">备注</span><span class="sxs-lookup"><span data-stu-id="db516-108">Remarks</span></span>  

 <span data-ttu-id="db516-109">堆栈链表示线程的物理调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="db516-109">The stack chain represents the physical call stack for the thread.</span></span> <span data-ttu-id="db516-110">以下情况会创建堆栈链边界：</span><span class="sxs-lookup"><span data-stu-id="db516-110">The following circumstances create a stack chain boundary:</span></span>  
  
- <span data-ttu-id="db516-111">托管到非托管或非托管的转换。</span><span class="sxs-lookup"><span data-stu-id="db516-111">A managed-to-unmanaged or unmanaged-to-managed transition.</span></span>  
  
- <span data-ttu-id="db516-112">上下文切换。</span><span class="sxs-lookup"><span data-stu-id="db516-112">A context switch.</span></span>  
  
- <span data-ttu-id="db516-113">用户线程的调试器劫持。</span><span class="sxs-lookup"><span data-stu-id="db516-113">A debugger hijacking of a user thread.</span></span>  
  
 <span data-ttu-id="db516-114">在单个上下文中运行纯托管代码的线程的简单情况下，线程与堆栈链之间存在一对一的对应关系。</span><span class="sxs-lookup"><span data-stu-id="db516-114">In the simple case for a thread that is running purely managed code in a single context, a one-to-one correspondence will exist between threads and stack chains.</span></span>  
  
 <span data-ttu-id="db516-115">调试器可能需要将所有线程的物理调用堆栈重新排列为逻辑调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="db516-115">A debugger may want to rearrange the physical call stacks of all threads into logical call stacks.</span></span> <span data-ttu-id="db516-116">这涉及到通过其调用方/被调用方关系对所有线程链进行排序并 regrouping 它们。</span><span class="sxs-lookup"><span data-stu-id="db516-116">This would involve sorting all the threads' chains by their caller/callee relationships and regrouping them.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db516-117">要求</span><span class="sxs-lookup"><span data-stu-id="db516-117">Requirements</span></span>  

 <span data-ttu-id="db516-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db516-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db516-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db516-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db516-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db516-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db516-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db516-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

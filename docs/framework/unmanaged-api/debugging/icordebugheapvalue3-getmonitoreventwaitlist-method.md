---
description: 了解详细信息： ICorDebugHeapValue3：： GetMonitorEventWaitList 方法
title: ICorDebugHeapValue3::GetMonitorEventWaitList 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3.GetMonitorEventWaitList
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3::GetMonitorEventWaitList
helpviewer_keywords:
- ICorDebugHeapValue3::GetMonitorEventWaitList method [.NET Framework debugging]
- GetMonitorEventWaitList method [.NET Framework debugging]
ms.assetid: 035a9035-ac66-4953-b48a-99652b42b7fe
topic_type:
- apiref
ms.openlocfilehash: ffc849e83151719062133382989344a8f0057caf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791447"
---
# <a name="icordebugheapvalue3getmonitoreventwaitlist-method"></a><span data-ttu-id="40770-103">ICorDebugHeapValue3::GetMonitorEventWaitList 方法</span><span class="sxs-lookup"><span data-stu-id="40770-103">ICorDebugHeapValue3::GetMonitorEventWaitList Method</span></span>

<span data-ttu-id="40770-104">提供在与监视器锁关联的事件上排队的线程的排序列表。</span><span class="sxs-lookup"><span data-stu-id="40770-104">Provides an ordered list of threads that are queued on the event that is associated with a monitor lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40770-105">语法</span><span class="sxs-lookup"><span data-stu-id="40770-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMonitorEventWaitList (  
    [out] ICorDebugThreadEnum **ppThreadEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="40770-106">参数</span><span class="sxs-lookup"><span data-stu-id="40770-106">Parameters</span></span>  

 `ppThreadEnum`  
 <span data-ttu-id="40770-107">弄提供线程有序列表的 ICorDebugThreadEnum 枚举器。</span><span class="sxs-lookup"><span data-stu-id="40770-107">[out] The ICorDebugThreadEnum enumerator that provides the ordered list of threads.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="40770-108">返回值</span><span class="sxs-lookup"><span data-stu-id="40770-108">Return Value</span></span>  

 <span data-ttu-id="40770-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="40770-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="40770-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="40770-110">HRESULT</span></span>|<span data-ttu-id="40770-111">说明</span><span class="sxs-lookup"><span data-stu-id="40770-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="40770-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="40770-112">S_OK</span></span>|<span data-ttu-id="40770-113">该列表不为空。</span><span class="sxs-lookup"><span data-stu-id="40770-113">The list is not empty.</span></span>|  
|<span data-ttu-id="40770-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="40770-114">S_FALSE</span></span>|<span data-ttu-id="40770-115">列表为空。</span><span class="sxs-lookup"><span data-stu-id="40770-115">The list is empty.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="40770-116">例外</span><span class="sxs-lookup"><span data-stu-id="40770-116">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="40770-117">备注</span><span class="sxs-lookup"><span data-stu-id="40770-117">Remarks</span></span>  

 <span data-ttu-id="40770-118">列表中的第一个线程是下一次调用时释放的第一个线程 <xref:System.Threading.Monitor.Pulse%28System.Object%29?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="40770-118">The first thread in the list is the first thread that is released by the next call to <xref:System.Threading.Monitor.Pulse%28System.Object%29?displayProperty=nameWithType>.</span></span> <span data-ttu-id="40770-119">此列表中的下一个线程将在以下调用上释放，依此类推。</span><span class="sxs-lookup"><span data-stu-id="40770-119">The next thread in the list is released on the following call, and so on.</span></span>  
  
 <span data-ttu-id="40770-120">如果列表不为空，则此方法返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="40770-120">If the list is not empty, this method returns S_OK.</span></span> <span data-ttu-id="40770-121">如果列表为空，则该方法返回 S_FALSE;在这种情况下，枚举仍有效，但它是空的。</span><span class="sxs-lookup"><span data-stu-id="40770-121">If the list is empty, the method returns S_FALSE; in this case, the enumeration is still valid, although it is empty.</span></span>  
  
 <span data-ttu-id="40770-122">在任一情况下，枚举接口仅在当前已同步状态的持续时间内可用。</span><span class="sxs-lookup"><span data-stu-id="40770-122">In either case, the enumeration interface is usable only for the duration of the current synchronized state.</span></span> <span data-ttu-id="40770-123">但是，在线程退出之前，从它分配的线程的接口是有效的。</span><span class="sxs-lookup"><span data-stu-id="40770-123">However, the thread's interfaces dispensed from it are valid until the thread exits.</span></span>  
  
 <span data-ttu-id="40770-124">如果不是 `ppThreadEnum` 有效的指针，则结果是不确定的。</span><span class="sxs-lookup"><span data-stu-id="40770-124">If `ppThreadEnum` is not a valid pointer, the result is undefined.</span></span>  
  
 <span data-ttu-id="40770-125">如果发生错误，导致无法确定线程（如果有）正在等待监视器的线程，则该方法将返回一个指示失败的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="40770-125">If an error occurs such that it cannot be determined which, if any, threads are waiting for the monitor, the method returns an HRESULT that indicates failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40770-126">要求</span><span class="sxs-lookup"><span data-stu-id="40770-126">Requirements</span></span>  

 <span data-ttu-id="40770-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="40770-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40770-128">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="40770-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="40770-129">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="40770-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="40770-130">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40770-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40770-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="40770-131">See also</span></span>

- [<span data-ttu-id="40770-132">调试接口</span><span class="sxs-lookup"><span data-stu-id="40770-132">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="40770-133">调试</span><span class="sxs-lookup"><span data-stu-id="40770-133">Debugging</span></span>](index.md)

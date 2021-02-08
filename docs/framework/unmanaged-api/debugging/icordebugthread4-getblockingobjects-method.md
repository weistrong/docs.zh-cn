---
description: 了解详细信息： ICorDebugThread4：： GetBlockingObjects 方法
title: ICorDebugThread4::GetBlockingObjects 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread4.GetBlockingObjects Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4::GetBlockingObjects
helpviewer_keywords:
- GetBlockingObjects method [.NET Framework debugging]
- ICorDebugThread4::GetBlockingObjects method [.NET Framework debugging]
ms.assetid: a7e6c54e-7be9-4e52-bbb4-95f52458e8e4
topic_type:
- apiref
ms.openlocfilehash: 6a60ebe6f5f6dac93dcb11dad7658aba9c934329
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800950"
---
# <a name="icordebugthread4getblockingobjects-method"></a><span data-ttu-id="e47ec-103">ICorDebugThread4::GetBlockingObjects 方法</span><span class="sxs-lookup"><span data-stu-id="e47ec-103">ICorDebugThread4::GetBlockingObjects Method</span></span>

<span data-ttu-id="e47ec-104">提供 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的有序枚举，这些结构提供线程阻塞信息。</span><span class="sxs-lookup"><span data-stu-id="e47ec-104">Provides an ordered enumeration of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures that provide thread blocking information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e47ec-105">语法</span><span class="sxs-lookup"><span data-stu-id="e47ec-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBlockingObjects (  
    [out] ICorDebugBlockingObjectEnum **ppBlockingObjectEnum  
```  
  
## <a name="parameters"></a><span data-ttu-id="e47ec-106">参数</span><span class="sxs-lookup"><span data-stu-id="e47ec-106">Parameters</span></span>  

 `ppBlockingObjectEnum`  
 <span data-ttu-id="e47ec-107">弄指向 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的有序枚举的指针。</span><span class="sxs-lookup"><span data-stu-id="e47ec-107">[out] A pointer to an ordered enumeration of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e47ec-108">备注</span><span class="sxs-lookup"><span data-stu-id="e47ec-108">Remarks</span></span>  

 <span data-ttu-id="e47ec-109">返回的枚举中的第一个元素对应于阻塞线程的第一个结构。</span><span class="sxs-lookup"><span data-stu-id="e47ec-109">The first element in the returned enumeration corresponds to the first structure that is blocking the thread.</span></span> <span data-ttu-id="e47ec-110">第二个元素对应于在第一次阻塞时 (APC) 运行异步过程调用时遇到的阻塞项，依此类推。</span><span class="sxs-lookup"><span data-stu-id="e47ec-110">The second element corresponds to a blocking item that is encountered while running an asynchronous procedure call (APC) when blocked on the first, and so on.</span></span>  
  
 <span data-ttu-id="e47ec-111">枚举仅在当前已同步状态的持续时间内有效。</span><span class="sxs-lookup"><span data-stu-id="e47ec-111">The enumeration is valid only for the duration of the current synchronized state.</span></span>  
  
 <span data-ttu-id="e47ec-112">当调试对象处于已同步状态时，必须调用此方法。</span><span class="sxs-lookup"><span data-stu-id="e47ec-112">This method must be called while the debuggee is in a synchronized state.</span></span>  
  
 <span data-ttu-id="e47ec-113">如果不是 `ppBlockingObjectEnum` 有效的指针，则结果是不确定的。</span><span class="sxs-lookup"><span data-stu-id="e47ec-113">If `ppBlockingObjectEnum` is not a valid pointer, the result is undefined.</span></span>  
  
 <span data-ttu-id="e47ec-114">如果某个线程被阻止并且无法确定该错误，则该方法将返回一个指示失败的 HRESULT;否则，它将返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e47ec-114">If a thread is blocked and the error cannot be determined, the method returns an HRESULT that indicates failure; otherwise, it returns S_OK.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e47ec-115">要求</span><span class="sxs-lookup"><span data-stu-id="e47ec-115">Requirements</span></span>  

 <span data-ttu-id="e47ec-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e47ec-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e47ec-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e47ec-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e47ec-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e47ec-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e47ec-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e47ec-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e47ec-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e47ec-120">See also</span></span>

- [<span data-ttu-id="e47ec-121">ICorDebugThread4 接口</span><span class="sxs-lookup"><span data-stu-id="e47ec-121">ICorDebugThread4 Interface</span></span>](icordebugthread4-interface.md)
- [<span data-ttu-id="e47ec-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="e47ec-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="e47ec-123">调试</span><span class="sxs-lookup"><span data-stu-id="e47ec-123">Debugging</span></span>](index.md)

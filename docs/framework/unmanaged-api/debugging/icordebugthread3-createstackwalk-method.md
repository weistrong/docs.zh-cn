---
description: 了解详细信息： ICorDebugThread3：： CreateStackWalk 方法
title: ICorDebugThread3::CreateStackWalk 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread3.CreateStackWalk Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread3::CreateStackWalk
helpviewer_keywords:
- CreateStackWalk method [.NET Framework debugging]
- ICorDebugThread3::CreateStackWalk method [.NET Framework debugging]
ms.assetid: c55e35d9-f9aa-4268-94b5-dce44c61acf2
topic_type:
- apiref
ms.openlocfilehash: b36252160dbad14ca1bee0674b6d042072a36359
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800989"
---
# <a name="icordebugthread3createstackwalk-method"></a><span data-ttu-id="22778-103">ICorDebugThread3::CreateStackWalk 方法</span><span class="sxs-lookup"><span data-stu-id="22778-103">ICorDebugThread3::CreateStackWalk Method</span></span>

<span data-ttu-id="22778-104">为要展开其堆栈的线程创建 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="22778-104">Creates an [ICorDebugStackWalk](icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22778-105">语法</span><span class="sxs-lookup"><span data-stu-id="22778-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateStackWalk([out] ICorDebugStackWalk **ppStackWalk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22778-106">参数</span><span class="sxs-lookup"><span data-stu-id="22778-106">Parameters</span></span>  

 `ppStackWalk`  
 <span data-ttu-id="22778-107">弄指向要展开其堆栈的线程的 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="22778-107">[out] A pointer to address of the [ICorDebugStackWalk](icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="22778-108">返回值</span><span class="sxs-lookup"><span data-stu-id="22778-108">Return Value</span></span>  

 <span data-ttu-id="22778-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="22778-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="22778-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="22778-110">HRESULT</span></span>|<span data-ttu-id="22778-111">说明</span><span class="sxs-lookup"><span data-stu-id="22778-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="22778-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="22778-112">S_OK</span></span>|<span data-ttu-id="22778-113">已 `ICorDebugStackWalk` 成功创建对象。</span><span class="sxs-lookup"><span data-stu-id="22778-113">The `ICorDebugStackWalk` object was successfully created.</span></span>|  
|<span data-ttu-id="22778-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="22778-114">E_FAIL</span></span>|<span data-ttu-id="22778-115">`ICorDebugStackWalk`未创建对象。</span><span class="sxs-lookup"><span data-stu-id="22778-115">The `ICorDebugStackWalk` object was not created.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="22778-116">例外</span><span class="sxs-lookup"><span data-stu-id="22778-116">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="22778-117">备注</span><span class="sxs-lookup"><span data-stu-id="22778-117">Remarks</span></span>  

 <span data-ttu-id="22778-118">如果该 `CreateStackWalk` 方法成功，则返回的 `ICorDebugStackWalk` 对象的上下文将设置为线程的当前上下文。</span><span class="sxs-lookup"><span data-stu-id="22778-118">If the `CreateStackWalk` method succeeds, the returned `ICorDebugStackWalk` object's context is set to the thread's current context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22778-119">要求</span><span class="sxs-lookup"><span data-stu-id="22778-119">Requirements</span></span>  

 <span data-ttu-id="22778-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22778-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22778-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="22778-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="22778-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22778-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22778-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22778-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22778-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="22778-124">See also</span></span>

- [<span data-ttu-id="22778-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="22778-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="22778-126">调试</span><span class="sxs-lookup"><span data-stu-id="22778-126">Debugging</span></span>](index.md)

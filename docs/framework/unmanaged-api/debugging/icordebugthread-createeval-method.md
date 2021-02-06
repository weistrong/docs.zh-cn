---
description: 了解详细信息： ICorDebugThread：： CreateEval 方法
title: ICorDebugThread::CreateEval 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateEval
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateEval
helpviewer_keywords:
- CreateEval method [.NET Framework debugging]
- ICorDebugThread::CreateEval method [.NET Framework debugging]
ms.assetid: 36605067-33d3-4579-9c72-fb0e551ab0f1
topic_type:
- apiref
ms.openlocfilehash: a789840e099a14b584e5713bee12f5c4b0717fe7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659382"
---
# <a name="icordebugthreadcreateeval-method"></a><span data-ttu-id="706dd-103">ICorDebugThread::CreateEval 方法</span><span class="sxs-lookup"><span data-stu-id="706dd-103">ICorDebugThread::CreateEval Method</span></span>

<span data-ttu-id="706dd-104">创建一个 ICorDebugEval 对象，该对象收集并公开此 ICorDebugThread 的功能。</span><span class="sxs-lookup"><span data-stu-id="706dd-104">Creates an ICorDebugEval object that collects and exposes the functionality of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="706dd-105">语法</span><span class="sxs-lookup"><span data-stu-id="706dd-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateEval (  
    [out] ICorDebugEval   **ppEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="706dd-106">参数</span><span class="sxs-lookup"><span data-stu-id="706dd-106">Parameters</span></span>  

 `ppEval`  
 <span data-ttu-id="706dd-107">弄指向 `ICorDebugEval` 收集并公开此线程功能的对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="706dd-107">[out] A pointer to the address of an `ICorDebugEval` object that collects and exposes the functionality of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="706dd-108">备注</span><span class="sxs-lookup"><span data-stu-id="706dd-108">Remarks</span></span>  

 <span data-ttu-id="706dd-109">计算对象在计算之前会在线程上推送新的链。</span><span class="sxs-lookup"><span data-stu-id="706dd-109">The evaluation object will push a new chain on the thread before doing its computation.</span></span> <span data-ttu-id="706dd-110">这会中断当前正在线程上执行的计算，直到完成计算。</span><span class="sxs-lookup"><span data-stu-id="706dd-110">This interrupts the computation currently being performed on the thread until the evaluation completes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="706dd-111">要求</span><span class="sxs-lookup"><span data-stu-id="706dd-111">Requirements</span></span>  

 <span data-ttu-id="706dd-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="706dd-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="706dd-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="706dd-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="706dd-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="706dd-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="706dd-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="706dd-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

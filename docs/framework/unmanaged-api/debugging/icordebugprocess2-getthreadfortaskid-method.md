---
description: 了解详细信息： ICorDebugProcess2：： GetThreadForTaskID 方法
title: ICorDebugProcess2::GetThreadForTaskID 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.GetThreadForTaskID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::GetThreadForTaskID
helpviewer_keywords:
- ICorDebugProcess2::GetThreadForTaskId method [.NET Framework debugging]
- GetThreadForTaskID method [.NET Framework debugging]
ms.assetid: 32d54a5b-8ad3-405b-a1b9-0936a3b49d1e
topic_type:
- apiref
ms.openlocfilehash: aafb1223f6e2e73aae600fd482c76b84c57dae52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650126"
---
# <a name="icordebugprocess2getthreadfortaskid-method"></a><span data-ttu-id="a9606-103">ICorDebugProcess2::GetThreadForTaskID 方法</span><span class="sxs-lookup"><span data-stu-id="a9606-103">ICorDebugProcess2::GetThreadForTaskID Method</span></span>

<span data-ttu-id="a9606-104">获取正在执行具有指定标识符的任务的线程。</span><span class="sxs-lookup"><span data-stu-id="a9606-104">Gets the thread on which the task with the specified identifier is executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9606-105">语法</span><span class="sxs-lookup"><span data-stu-id="a9606-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadForTaskID (  
    [in]  TASKID            taskid,  
    [out] ICorDebugThread2  **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9606-106">参数</span><span class="sxs-lookup"><span data-stu-id="a9606-106">Parameters</span></span>  

 `taskid`  
 <span data-ttu-id="a9606-107">中任务的标识符。</span><span class="sxs-lookup"><span data-stu-id="a9606-107">[in] The identifier of the task.</span></span>  
  
 `ppThread`  
 <span data-ttu-id="a9606-108">弄指向 ICorDebugThread2 对象的地址的指针，该对象表示要检索的线程。</span><span class="sxs-lookup"><span data-stu-id="a9606-108">[out] A pointer to the address of an ICorDebugThread2 object that represents the thread to be retrieved.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9606-109">备注</span><span class="sxs-lookup"><span data-stu-id="a9606-109">Remarks</span></span>  

 <span data-ttu-id="a9606-110">主机可以使用 [ICLRTask：： SetTaskIdentifier](../hosting/iclrtask-settaskidentifier-method.md) 方法设置任务标识符。</span><span class="sxs-lookup"><span data-stu-id="a9606-110">The host can set the task identifier by using the [ICLRTask::SetTaskIdentifier](../hosting/iclrtask-settaskidentifier-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9606-111">要求</span><span class="sxs-lookup"><span data-stu-id="a9606-111">Requirements</span></span>  

 <span data-ttu-id="a9606-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9606-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9606-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a9606-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a9606-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a9606-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a9606-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9606-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

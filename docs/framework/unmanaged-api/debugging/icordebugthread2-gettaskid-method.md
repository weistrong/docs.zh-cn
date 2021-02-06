---
description: 了解详细信息： ICorDebugThread2：： GetTaskID 方法
title: ICorDebugThread2::GetTaskID 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetTaskID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetTaskID
helpviewer_keywords:
- ICorDebugThread2::GetTaskID method [.NET Framework debugging]
- GetTaskID method [.NET Framework debugging]
ms.assetid: 6ba3c6ee-4ba1-4c98-bf1e-8531acd3da09
topic_type:
- apiref
ms.openlocfilehash: 5429daee9150d63834c747dd5ebb763dd6f0da6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658654"
---
# <a name="icordebugthread2gettaskid-method"></a><span data-ttu-id="1bdf0-103">ICorDebugThread2::GetTaskID 方法</span><span class="sxs-lookup"><span data-stu-id="1bdf0-103">ICorDebugThread2::GetTaskID Method</span></span>

<span data-ttu-id="1bdf0-104">获取此线程上运行的任务的标识符。</span><span class="sxs-lookup"><span data-stu-id="1bdf0-104">Gets the identifier of the task running on this thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1bdf0-105">语法</span><span class="sxs-lookup"><span data-stu-id="1bdf0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTaskID (  
    [out] TASKID  *pTaskId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1bdf0-106">参数</span><span class="sxs-lookup"><span data-stu-id="1bdf0-106">Parameters</span></span>  

 `pTaskId`  
 <span data-ttu-id="1bdf0-107">弄一个指针，指向在此 ICorDebugThread2 对象表示的线程上运行的任务的标识符。</span><span class="sxs-lookup"><span data-stu-id="1bdf0-107">[out] A pointer to the identifier of the task running on the thread represented by this ICorDebugThread2 object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1bdf0-108">备注</span><span class="sxs-lookup"><span data-stu-id="1bdf0-108">Remarks</span></span>  

 <span data-ttu-id="1bdf0-109">任务只能在线程与连接关联时在线程上运行。</span><span class="sxs-lookup"><span data-stu-id="1bdf0-109">A task can only be running on the thread if the thread is associated with a connection.</span></span> <span data-ttu-id="1bdf0-110">`GetTaskID` 如果线程与连接无关，则返回零 `pTaskId` 。</span><span class="sxs-lookup"><span data-stu-id="1bdf0-110">`GetTaskID` returns zero in `pTaskId` if the thread is not associated with a connection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1bdf0-111">要求</span><span class="sxs-lookup"><span data-stu-id="1bdf0-111">Requirements</span></span>  

 <span data-ttu-id="1bdf0-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1bdf0-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1bdf0-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1bdf0-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1bdf0-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1bdf0-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1bdf0-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1bdf0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
